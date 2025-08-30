
# 👁️ Gender & Age Predictor

[![MIT License](https://img.shields.io/github/license/nikhil-rao-1907/gender-age-predictor?color=yellow)](LICENSE)  
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)  
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?logo=opencv)  
![Deep Learning](https://img.shields.io/badge/Deep_Learning-CNN-orange)  
![Status](https://img.shields.io/badge/Status-Active-success)  

---

## 🎯 Objective
A **Python + Deep Learning project** that detects **gender 👩 / 👨** and **predicts age ranges** of a person from:
- 🖼️ **Single Image**
- 🎥 **Live Webcam Feed**

Predicted **Age ranges**:  
`(0–2), (4–6), (8–12), (15–20), (25–32), (38–43), (48–53), (60–100)`  

---

## 📖 About
This project uses **pre-trained CNN models** for **age & gender classification**, trained on the **Adience Benchmark Dataset**.  

- 👨‍⚕️ Gender → *Male / Female* (binary classification)  
- 📅 Age → *8 grouped classes* (softmax classification)  
- ⚡ Face Detection → OpenCV DNN face detector `.pb` (TensorFlow)  
- ⚡ Age & Gender → Caffe Models (`.prototxt` + `.caffemodel`)  

💡 **Note:** Exact age prediction is hard due to makeup, lighting, expressions → so classification is more reliable than regression.  

---

## 📂 Dataset
- **Adience Dataset** → [Download from Kaggle](https://www.kaggle.com/ttungl/adience-benchmark-gender-and-age-classification)  
- 📸 26,580 face photos, 2,284 subjects, 8 age bins  
- ✅ Real-world conditions (lighting, angle, noise, expressions)  
- 🆓 Creative Commons licensed  

---

## 📦 Project Structure
```
gender-age-predictor/
├── detect.py                          # Main detection script
├── opencv_face_detector.pbtxt         # Face detector config
├── opencv_face_detector_uint8.pb      # Face detector weights
├── age_deploy.prototxt                # Age model architecture
├── age_net.caffemodel                 # Age model weights
├── gender_deploy.prototxt             # Gender model architecture
├── gender_net.caffemodel              # Gender model weights
├── Example/                           # Example output images
└── README.md                          # Documentation
```

---

## 📌 Requirements
Install dependencies:
```bash
pip install opencv-python argparse
```

- 🐍 Python **3.x**
- 📚 OpenCV **4.x**
- ⚙️ Argparse for argument parsing  

---

## ▶️ Usage

### 1. Predict age & gender on an **image**
```bash
python detect.py --image <image_name>
```
🔸 *Ensure the image is in the repo directory*  

### 2. Predict age & gender via **Webcam**
```bash
python detect.py
```
Press **CTRL + C** to quit.  

---

## 📹 Demo
[![Watch the demo](https://img.youtube.com/vi/ReeccRD21EU/0.jpg)](https://youtu.be/ReeccRD21EU)  
▶️ Click to watch full working demo!

---

## 📸 Example Predictions

| Input | Prediction | Output |
|-------|------------|---------|
| `girl1.jpg` | Female, 25–32 yrs | ![](Example/Detecting%20age%20and%20gender%20girl1.png) |
| `girl2.jpg` | Female, 8–12 yrs | ![](Example/Detecting%20age%20and%20gender%20girl2.png) |
| `kid1.jpg` | Male, 4–6 yrs | ![](Example/Detecting%20age%20and%20gender%20kid1.png) |
| `kid2.jpg` | Female, 4–6 yrs | ![](Example/Detecting%20age%20and%20gender%20kid2.png) |
| `man1.jpg` | Male, 38–43 yrs | ![](Example/Detecting%20age%20and%20gender%20man1.png) |
| `man2.jpg` | Male, 25–32 yrs | ![](Example/Detecting%20age%20and%20gender%20man2.png) |
| `woman1.jpg` | Female, 38–43 yrs | ![](Example/Detecting%20age%20and%20gender%20woman1.png) |

---

## 📜 License
This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author
- **Nikhil Rao**  
  🔗 [GitHub](https://github.com/nikhil-rao-1907)  

---

✨ *Predict gender & age from any face image using Deep Learning!* 🚀



---

👉 Do you want me to also design that **System Flow Diagram (architecture: webcam/image → detector → CNN model → output)** in Mermaid/PlantUML code so you can add to README just like we did for ER diagrams?
