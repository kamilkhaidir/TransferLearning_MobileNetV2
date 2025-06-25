# 🐶🐱 Cats vs Dogs Classifier using MobileNetV2 (Transfer Learning)

This project applies **transfer learning** with **MobileNetV2** to build a binary image classifier that can distinguish between cats and dogs. It was developed using TensorFlow and trained on the Cats vs Dogs dataset from `tensorflow_datasets`.

---

## 📌 Overview

- **Problem**: Binary classification — Cat (0) vs Dog (1)
- **Model**: Pre-trained `MobileNetV2` (feature extractor)
- **Approach**: Freeze base layers, train custom classifier
- **Framework**: TensorFlow 2 / Keras
- **Dataset**: [`cats_vs_dogs`](https://www.tensorflow.org/datasets/catalog/cats_vs_dogs) via `tensorflow_datasets`

---

## ⚙️ Model Architecture

- Base: `MobileNetV2(include_top=False, weights='imagenet', trainable=False)`
- Classifier:
  - `GlobalAveragePooling2D()`
  - `Dense(1, activation='sigmoid')`

---

## 🧠 Training Setup

- Dataset split:  
  - 70% training  
  - 15% validation  
  - 15% test
- Epochs: 5
- Optimizer: `adam`
- Loss: `binary_crossentropy`
- Metrics: `accuracy`

---

## 📊 Results

| Metric     | Value         |
|------------|---------------|
| Validation Accuracy | ~98%        |
| Test Accuracy       | Consistent with validation |
| Overfitting         | No major signs (loss curves stable) |

📸 See `screenshots/` folder for:
- Code implementation
- Prediction examples on test data

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/cats-vs-dogs-mobilenet.git
   cd cats-vs-dogs-mobilenet
