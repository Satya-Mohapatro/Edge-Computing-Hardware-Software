# 🛠️ Metal Surface Defect Detection

AI-powered real-time quality inspection system using **YOLOv8** deployed on **NVIDIA Jetson Orin Nano**

---

## 📌 Overview

This project implements an automated defect detection system for metal surfaces using **deep learning** and **edge AI**.
The goal is to replace manual, error-prone inspection with a **fast, accurate, and scalable** solution that works in real time on the factory floor.

The system detects the following metal surface defects:

* **Crazing**
* **Inclusion**
* **Patches**
* **Pitted Surface**
* **Rolled-in Scale**
* **Scratches**

It is trained on the **NEU surface defect dataset** and optimized using **TensorRT** for high-speed inference (< 30 FPS) on Jetson Orin Nano.

---

## 🚀 Key Features

### 🔍 1. AI-based Defect Detection

* YOLOv8 object detection model
* Trained on NEU dataset
* Detects 6 metal surface defect types

### ⚡ 2. Optimized Edge Deployment

* Model converted to **TensorRT FP16**
* Runs on **NVIDIA Jetson Orin Nano**
* Real-time performance (<30 ms per frame)

### 📦 3. Dockerized System

* Reproducible environment
* Easy deployment across Jetson devices

### 📡 4. MQTT Alerts & Monitoring

* Sends defect alerts instantly
* Can integrate with dashboards, PLCs, mobile apps
* Supports remote monitoring of factory line

### 🖼️ 5. Image Logging

* Saves images of detected defects
* Useful for audit and quality analysis

---

## 🏗️ System Architecture

1. **Model Training (Google Colab)**

   * YOLOv8s trained for 150 epochs
   * Data augmentation and fine-tuning

2. **Model Optimization (On Jetson)**

   * Convert PyTorch → ONNX → TensorRT
   * FP16 precision for faster inference

3. **Real-Time Inference**

   * Live camera feed processed on Orin Nano
   * Multi-frame confirmation reduces false positives

4. **MQTT-Based Alerts**

   * Sends structured data (defect type, timestamp, image)
   * Works with dashboards like Node-RED, ThingsBoard, Home Assistant

---

## 📂 Project Structure

```
├── data/                # Training dataset (NEU surface defects)
├── models/              # Trained YOLOv8 + TensorRT model
├── src/
│   ├── train.py         # YOLOv8 training pipeline
│   ├── inference.py     # Real-time defect detection
│   ├── trt_convert.py   # PyTorch → TensorRT conversion
│   ├── mqtt_client.py   # MQTT communication
│   └── utils.py
├── docker/
│   └── Dockerfile        # Jetson-compatible Docker image
└── README.md
```

---

## 🧪 Results

### 📈 Model Training

* YOLOv8s
* 150 epochs
* High accuracy across five major defect categories


### 📊 MQTT Dashboard

Shows:

* Live detections
* Defect history
* Image logs

---

## 🏁 Conclusion

This project demonstrates an efficient and practical approach to industrial defect detection using **lightweight deep learning** and **edge AI**.
The system delivers:

✔ High accuracy
✔ Low latency
✔ Scalability
✔ Reduced manual labor and human error

It is suitable for real-world deployments in manufacturing industries requiring continuous quality assurance.

---

## 👨‍💻 Contributors

* **Rohit Khatri (MITU22BTCS0659)**
* **Mahesh Swami (MITU22BTCS0414)**
* **Siddharth Suryawanshi (MITU22BTCS0823)**
* **Satyanarayan Mohapatro (MITU22BTCS0751)**

**Guide:** Prof. Harshad Lokhande
MIT School of Computing, MIT ADT University

