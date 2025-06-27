# 😷 Face-Mask-Prediction (YOLO-based)

A real-time face mask detection system using the YOLO (You Only Look Once) object detection algorithm. This project detects faces and classifies them as **wearing a mask** or **not wearing a mask** using a single-shot detection pipeline, making it suitable for deployment in live video streams, CCTV footage, and public health systems.

---

## 🧭 Table of Contents

1. [Introduction](#introduction)  
2. [Features](#features)  
3. [Tech Stack](#tech-stack)  
4. [Model & Dataset](#model--dataset)  
5. [Installation](#installation)  
6. [Usage](#usage)  
7. [Output Examples](#output-examples)  
8. [Performance](#performance)  

---

## 📌 Introduction

This project implements a YOLO-based pipeline for detecting whether people are wearing face masks. It's optimized for real-time performance and can be deployed on surveillance cameras, embedded systems, or mobile applications.

---

## ✅ Features

- 🎯 Real-time object detection using YOLOv5 or YOLOv8
- 😷 Detects multiple classes: `Mask`, `No Mask`
- 🎥 Supports webcam, image, or video input
- ⚡ Fast inference speed with high accuracy
- 🧩 Easily extendable to other PPE (gloves, helmet, etc.)

---

## 🧱 Tech Stack

- **Object Detection**: YOLOv5 / YOLOv8 (Ultralytics)
- **Framework**: PyTorch (via Ultralytics' YOLO package)
- **Computer Vision**: OpenCV
- **Tools**: Python, argparse, NumPy, Matplotlib

---

## 📦 Model & Dataset

### 🔍 Dataset:
- Masked and unmasked faces collected from open datasets (e.g., [Kaggle Mask Dataset](https://www.kaggle.com/datasets))
- Annotated in YOLO format (`images/`, `labels/` with `.txt` files)

### 🧠 Model:
- YOLOv5s or YOLOv8n trained using `ultralytics` package
- Custom-trained for 2 classes: `mask`, `no_mask`
- Output model file: `best.pt`

---

## 🛠 Installation

```bash
# Clone the repository
git clone https://github.com/Bhumik14/Face-Mask-Prediction.git
cd Face-Mask-Prediction

# Create a virtual environment (optional)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
# Or directly:
pip install ultralytics opencv-python

# Usuage
# 1. Run on webcam (default)
yolo task=detect mode=predict model=best.pt source=0
# 2. Run on image
yolo task=detect mode=predict model=best.pt source=examples/sample.jpg
# 3. Run on video
yolo task=detect mode=predict model=best.pt source=examples/sample_video.mp4
