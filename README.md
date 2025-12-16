# 🧠 CNN Deep Learning Project (MNIST)

## 📌 Project Overview
This project explores Convolutional Neural Networks (CNNs) for image classification using the MNIST handwritten digits dataset.  
The goal is to analyze how architectural changes affect **performance, accuracy, training time, and model cost**.

A **baseline CNN** is implemented first, followed by two different **architecture variations** to observe trade-offs between model complexity and performance.

---

## 📊 Dataset
- **Dataset:** MNIST
- **Classes:** 10 (digits 0–9)
- **Input Shape:** 28 × 28 grayscale images
- **Preprocessing:**
  - Normalization (pixel values scaled to [0,1])
  - Reshaping to `(28, 28, 1)`
  - One-hot encoding for labels

---

## 🏗️ Model Architectures

### 1️⃣ CNN Basic (Reference Model)
- Conv2D (32 filters) → MaxPooling
- Conv2D (64 filters) → MaxPooling
- Flatten
- Dense (128)
- Output Dense (10, Softmax)

This model serves as the **baseline** for performance and cost comparison.

---

### 2️⃣ CNN Variation 1 – Lightweight Model
- Reduced number of filters (16 → 32)
- Same overall structure as the baseline
- Significantly fewer parameters

**Goal:** Reduce computational cost while maintaining accuracy.

---

### 3️⃣ CNN Variation 2 – Deeper Model
- Additional convolutional layer added
- Increased representational capacity

**Goal:** Observe accuracy gains versus increased training time and parameter count.

---

## ⚙️ Training Setup
- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Metric:** Accuracy
- **Epochs:** 10
- **Batch Size:** 32
- **Validation Split:** 20%

---

## 📈 Evaluation Metrics
Each model is evaluated using:
- Test Accuracy
- Test Loss
- Training Time (seconds)
- Total Trainable Parameters

These metrics allow direct comparison of **performance vs. cost**.

---

## 🔍 Key Observations
- The **baseline CNN** achieves high accuracy with moderate cost.
- The **lightweight model** significantly reduces parameters and training time with minimal accuracy loss.
- The **deeper model** slightly improves accuracy but increases training time and complexity.
- Dense layers contribute the majority of model parameters and computational cost.

---

## 🧪 Technologies Used
- Python
- TensorFlow / Keras
- NumPy
- Google Colab

---



## 🎯 Conclusion
This project demonstrates how CNN architecture design directly impacts performance and computational efficiency.  
It provides a clear comparison between **baseline, lightweight, and deeper CNN models**, highlighting practical trade-offs in deep learning model design.

