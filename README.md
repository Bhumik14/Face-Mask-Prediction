# Face Mask Detection Using Convolutional Neural Network (CNN)

## 📌 Overview
This project implements a face mask detection system using a **Convolutional Neural Network (CNN)**.  
The model classifies images or video frames to determine if a person is **wearing a mask** or **not wearing a mask**.  
It can be used for public health safety systems, workplace compliance, or automated monitoring.

---

## ✨ Features
- 🖼 Detects whether a person is **wearing a mask** or **not**.
- ⚡ Works in real-time or with static images/videos.
- 🛠 Image preprocessing for robust predictions.
- 💻 Lightweight CNN model architecture for easy deployment.

---

## 🛠 Technology Stack
- **Language:** Python
- **Deep Learning:** TensorFlow / Keras
- **Image Processing:** OpenCV
- **Utilities:** NumPy, scikit-learn
- **Visualization:** Matplotlib (for training curves)

---

## 📂 Dataset
The model is trained on a labeled dataset containing:
- Images of people **with masks**
- Images of people **without masks**

The dataset undergoes normalization, resizing, and augmentation to improve model generalization.

---

## 📁 Project Structure
├── train.py # Script for training the CNN model
├── detect.py # Script for running mask detection
├── model.h5 # Saved trained model
├── dataset/ # Training & validation datasets
├── requirements.txt # Dependencies
└── README.md # Project documentation

---

## ⚙️ Installation
1. **Clone the repository**
git clone <your-repo-url>
cd <repo-folder>
2. **Create a virtual environment** *(optional but recommended)*
python -m venv venv
source venv/bin/activate # For Windows: venv\Scripts\activate

3. **Install dependencies**
pip install -r requirements.txt
---

## 🚀 Usage

### ✔ Train the Model
python train.py

### ✔ Run Detection
- On an **image**:
python detect.py --image path_to_image.jpg

- On **webcam feed**:

  
---

## 🧠 Model Architecture
The CNN model consists of:
- Convolutional layers with **ReLU activation**
- Max-pooling layers for spatial reduction
- Flatten layer for feature vector conversion
- Fully connected (Dense) layers
- Final Dense layer with **Softmax** activation for 2-class classification (`Mask`, `No Mask`)

---

## 📊 Results
- **Accuracy:** High accuracy on test images
- **Real-time performance:** Smooth detection on webcam feeds
- Performance may vary depending on dataset quality and lighting conditions

---

## 🤝 Contributing
Contributions are welcome!  
Please open an **issue** or submit a **pull request** to improve the project.

---

## 📜 License
This project is released under the **MIT License**.  
Feel free to use and modify it as per your needs.

