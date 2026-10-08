# 🎭 Real-Time Face Emotion Detection

A webcam application that detects faces in a live video feed and classifies each one into one of seven emotions, with a confidence score and smoothed output so the label doesn't flicker.

Built with **Python, OpenCV, TensorFlow/Keras and MTCNN**.

---

## ✨ Features

- Real-time emotion detection from a webcam
- Accurate face detection with **MTCNN**
- Emotion smoothing over the last 10 predictions to reduce flickering
- Confidence score shown next to every prediction
- Frame skipping (the heavy model runs every 3rd frame) for low latency
- Pre-trained Keras model (`emotion_model.h5`)
- Small, modular codebase

## 🧠 Model

| | |
|---|---|
| **Input** | 64×64 grayscale face crop, scaled to 0-1 |
| **Classes** | Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral |
| **Format** | Keras `.h5`, loaded with `compile=False` for compatibility with newer Keras versions |

## 🔄 How it works

1. OpenCV captures a frame and resizes it to 640×480.
2. Every third frame, MTCNN detects faces; in between, the last detections are reused.
3. Each face crop is converted to grayscale, resized to 64×64 and normalised.
4. The Keras model predicts a probability for each emotion.
5. The most frequent label across the last 10 predictions is shown, with the bounding box and confidence.

## 🛠️ Tech stack

Python · OpenCV · TensorFlow / Keras · MTCNN · NumPy · Pillow

## 📂 Project structure

```
Face-Emotion-Detection/
├── app.py              # Webcam loop, face detection, prediction and drawing
├── emotion_utils.py    # Face preprocessing and prediction smoothing
├── emotion_model.h5    # Trained emotion classifier
├── requirements.txt    # Dependencies
└── README.md
```

## ⚡ Installation

```bash
git clone https://github.com/rajtanmay81/Face-Emotion-Detection.git
cd Face-Emotion-Detection

python -m venv venv
venv\Scripts\activate          # Windows
# source venv/bin/activate     # macOS / Linux

pip install -r requirements.txt
python app.py
```

Press **Q** to quit.

> **Platform note:** `app.py` opens the camera with `cv2.CAP_DSHOW`, which is a Windows backend. On macOS or Linux, change `cv2.VideoCapture(0, cv2.CAP_DSHOW)` to `cv2.VideoCapture(0)`.

## 🚧 Future improvements

- Serve the model as a web app with FastAPI or Flask
- Track multiple faces across frames
- Retrain on a larger dataset and report accuracy per emotion
- Run on mobile or edge devices

## 📧 Contact

**Tanmay Raj** · [rajtanmay81@gmail.com](mailto:rajtanmay81@gmail.com)
