# 🧠 Skin Disease Classification with Deep Learning

This project explores the use of **Convolutional Neural Networks (CNNs)** and **transfer learning** for **automated classification of skin conditions** using the Fitzpatrick17k dataset. Our approach integrates both image data and Fitzpatrick skin type labels, aiming to build fair, accurate, and generalizable models in the dermatology domain.

---

## 🧪 Project Summary

- **Task**: Multi-class classification of 114 skin conditions.
- **Dataset**: [Fitzpatrick17k](https://github.com/mattgroh/fitzpatrick17k) – a combination of clinical skin images and Fitzpatrick skin type labels.
- **Objective**: Improve diagnosis performance while reducing bias across skin tones.
- **Approach**:
  - Baseline CNNs: LeNet, AlexNet
  - Transfer Learning: VGG16, InceptionV3, ResNet101V2
  - Multi-Input Models: Combine image data + skin type metadata

---

## 📊 Results (Best Model)

- **Model**: Multi-Input ResNet101V2 + Dropout 0.4
- **Accuracy**: 0.374
- **F1-Score**: 0.471
- **Loss**: 3.826

---

## 🧰 Tech Stack & Libraries Used

This project was implemented in **Python** using the following core tools and libraries:

### 📦 Data Handling & Utilities
- **Pandas** and **NumPy** – Handling datasets and numerical processing
- **os, shutil, urllib, tqdm, pickle** – File system operations, data downloads, progress bars, and object storage

### 🖼️ Image Processing
- **OpenCV (cv2)** and **PIL (Pillow)** – Image manipulation (resize, format, color channels, etc.)
- **Matplotlib** – Visualization of training curves and evaluation results

### 🧪 Model Evaluation
- **Scikit-learn** – Metrics such as F1-Score, classification reports, and train/test split
- **Custom weighted F1 implementation** – To address dataset imbalance

### 🧠 Deep Learning with TensorFlow / Keras
- **Keras (Sequential & Functional API)** – For building and training CNN and multi-input models
- **Transfer Learning** – Using pretrained models: `VGG16`, `InceptionV3`, `ResNet101V2`
- **ImageDataGenerator** – Data augmentation (zoom, flip, rotation, brightness)
- **EarlyStopping** – Training regularization to avoid overfitting
- **Adam / RMSProp optimizers** – Model optimization

---
