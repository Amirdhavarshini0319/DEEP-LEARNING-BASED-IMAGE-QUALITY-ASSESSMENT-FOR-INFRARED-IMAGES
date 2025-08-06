# Infrared Image Quality Assessment using Deep Learning

This project presents a deep learning-based **no-reference Image Quality Assessment (IQA)** framework tailored for **thermal infrared (IR) images**, aimed at improving perception in **autonomous driving systems** under challenging conditions like fog, rain, and low light.

## 🚀 Overview

- **Objective**: Predict the perceptual quality of IR images without reference images.
- **Model**: ResNet-50 fine-tuned to predict Mean Opinion Scores (MOS).
- **Application**: Real-time image quality monitoring in ADAS (Advanced Driver Assistance Systems).

## 📂 Dataset

- A large-scale dataset of infrared (IR) images was used.
- Each image's quality score (MOS – Mean Opinion Score) is provided via a separate CSV file.
- The dataset includes diverse weather scenarios such as **drizzle, fog, heavy rain, and frost**, simulating real-world driving conditions.
- 📥 **[Download Dataset Here](https://drive.google.com/drive/folders/1Coz7VG-Uu55qDj-w4nfNw18YUtWmnQhG?usp=sharing)** 

## 🛠️ Methodology

- **Preprocessing**: Images were resized to `224×224` and normalized using ImageNet mean and std.
- **Training**:
  - Optimizer: Adam
  - Learning Rate: 0.0001
  - Loss Function: MSELoss
- **Evaluation Metrics**: SROCC, MSE, RMSE, and R^2.

## 📊 Results

- **ResNet-50** achieved high correlation between predicted and ground truth MOS.
- Tight scatter plot clustering along the diagonal indicates minimal prediction error.

## 📦 Dependencies

- Python 3.10+
- PyTorch
- Torchvision
- Matplotlib
- Scikit-learn
- OpenCV

## 📝 Future Work

- Explore lightweight models like MobileNet and EfficientNet for real-time deployment.
- Integrate multi-modal data (e.g., IR + RGB) for improved robustness.



