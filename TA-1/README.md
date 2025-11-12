# Face Detection using Haar Cascade (Jetson Orin Nano)

This project demonstrates **real-time face detection** using OpenCV’s Haar Cascade classifier on **NVIDIA Jetson Orin Nano**.

## 🚀 Features
- Real-time detection using on-board camera
- Fast and lightweight (runs on CPU/GPU)
- Uses pre-trained Haar Cascade model

## ⚙️ Setup Instructions

### 1️⃣ Update system
```bash
sudo apt update && sudo apt upgrade -y
```

### 2️⃣ Install dependencies
```bash
sudo apt install python3-pip python3-opencv -y
```

### 3️⃣ Clone and install Python libs
```bash
git clone https://github.com/YourUsername/Face-Detection-Haarcascade-Jetson.git
cd Face-Detection-Haarcascade-Jetson
pip3 install -r requirements.txt
```

### 4️⃣ Run the program
```bash
python3 face_detection.py
```

> Press `q` to quit the camera window.

## 📂 Dataset
- Haarcascade model: [haarcascade_frontalface_default.xml](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml)
- Optional test dataset: [LFW Dataset](http://vis-www.cs.umass.edu/lfw/)

## 🧠 Future Improvements
- Add eye detection, smile detection
- Integrate with face recognition model (e.g., LBPH / Dlib)
- Deploy via Jetson container with Docker

---

👨‍💻 **Author**: Mahesh Swami
