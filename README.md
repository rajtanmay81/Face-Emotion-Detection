# 🎭 Advanced Face Emotion Detection (Real-Time)

## 🚀 Overview

This project is a **real-time Face Emotion Detection system** built using Deep Learning, OpenCV, and MTCNN. It captures live webcam input and predicts human emotions with improved accuracy and smooth performance.

---

## 🧠 Features

* Real-time emotion detection via webcam
* Optimized performance with low latency
* High-accuracy face detection using **MTCNN**
* Emotion smoothing to reduce prediction flickering
* Confidence score display for predictions
* Modular and clean code structure
* Pre-trained **TensorFlow/Keras (.h5)** model

---

## 🛠️ Tech Stack

* Python
* OpenCV
* TensorFlow / Keras
* MTCNN
* NumPy

---

## 📂 Project Structure

```
face-emotion-detection/
│── app.py                # Main application
│── emotion_utils.py      # Preprocessing & smoothing logic
│── emotion_model.h5      # Trained model
│── requirements.txt      # Dependencies
│── README.md             # Documentation
```

---

## ⚡ Installation & Setup

### 1. Clone the Repository

```
git clone https://github.com/dharam9005/face-emotion-detection.git
cd face-emotion-detection
```

### 2. Create Virtual Environment

```
python -m venv venv
venv\Scripts\activate   # For Windows
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

### 4. Run the Project

```
python app.py
```

---

## 🎯 Model Details

* **Input Shape:** 64×64 (grayscale)
* **Output Classes:** Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral

---

## 🔥 Recent Improvements

* Fixed Keras model compatibility (`compile=False`)
* Optimized FPS for smoother webcam performance
* Implemented frame skipping for performance boost
* Improved preprocessing with proper input alignment
* Added modular utility functions (`emotion_utils.py`)
* Reduced prediction flickering with smoothing logic

---

## 📸 Output

The system displays a real-time webcam feed with:

* Face bounding box
* Predicted emotion label
* Confidence percentage
* Smooth and stable predictions

---

## 📌 Future Enhancements

* Deploy as a web app using Flask/FastAPI
* Add support for multiple face tracking
* Improve model accuracy using larger datasets
* Integrate with mobile or edge devices

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

---

## 📧 Contact

For any queries or collaboration:
**Tanmay Raj**
📩 [rajtanmay81@gmail.com](mailto:rajtanmay81@gmail.com)
