# 🐶🐱 Dog vs Cat Image Classification using CNN

## 📌 Overview

This project implements a **Convolutional Neural Network (CNN)** using **TensorFlow/Keras** to classify images of dogs and cats. The model is trained on the popular Kaggle Dogs vs Cats dataset and learns to distinguish between the two classes by extracting visual features from images.

---

## 🚀 Features

* Binary Image Classification (Dog vs Cat)
* Built using TensorFlow and Keras
* Custom CNN Architecture
* Image Normalization and Preprocessing
* Training and Validation Accuracy & Loss Visualization
* Overfitting Reduction using Dropout Layers
* Easy to Train and Extend

---

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* OpenDatasets
* Kaggle Dataset

---

## 📂 Dataset

Dataset: **Dogs vs Cats**

Source: Kaggle

https://www.kaggle.com/datasets/salader/dogsvscats

The dataset contains two classes:

* Dogs 🐶
* Cats 🐱

Dataset Structure:

```text
dogsvscats/
│
├── train/
│   ├── cats/
│   └── dogs/
│
└── test/
    ├── cats/
    └── dogs/
```

---

## 🧠 CNN Architecture

```text
Input Image (256×256×3)
        │
        ▼
Conv2D (32 Filters, 3×3, ReLU)
        │
MaxPooling2D (2×2)
        │
        ▼
Conv2D (64 Filters, 3×3, ReLU)
        │
MaxPooling2D (2×2)
        │
        ▼
Conv2D (128 Filters, 3×3, ReLU)
        │
MaxPooling2D (2×2)
        │
        ▼
Flatten
        │
Dense (128, ReLU)
        │
Dropout (0.1)
        │
Dense (64, ReLU)
        │
Dropout (0.1)
        │
Dense (1, Sigmoid)
        │
        ▼
Prediction (Dog / Cat)
```

---

## 📊 Data Preprocessing

* Images resized to **256 × 256**
* Pixel values normalized from **[0,255] → [0,1]**
* Batch size = **32**
* Labels automatically inferred from directory names

---

## ⚙️ Installation

### Clone the Repository

```bash
git clone https://github.com/abhi26shakya/Dog-vs-Cat-Image-Classification-Project.git
cd Dog-vs-Cat-Image-Classification-Project
```

### Install Dependencies

```bash
pip install tensorflow matplotlib opendatasets
```

---

## ▶️ Run the Project

### Download the Dataset

```python
import opendatasets as od
od.download("https://www.kaggle.com/datasets/salader/dogsvscats")
```

### Run the Training Script

```bash
python train.py
```

---

## 📈 Training Results

The model tracks:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss

### Accuracy Curve
<img width="549" height="403" alt="Screenshot 2026-06-01 at 2 34 02 PM" src="https://github.com/user-attachments/assets/7ed4b9fd-bf1f-4add-8850-ed5e9f8b8a27" />


### Loss Curve
<img width="541" height="405" alt="Screenshot 2026-06-01 at 2 34 47 PM" src="https://github.com/user-attachments/assets/1135cc59-18b1-4454-9878-e913d9c0cba0" />



## 📷 Sample Prediction

```text
Input Image → CNN Model → Prediction

Dog Image  → 0.97 → Dog 🐶
Cat Image  → 0.04 → Cat 🐱
```

---

## 🔮 Future Improvements

* Data Augmentation
* Transfer Learning (VGG16, ResNet50, MobileNet)
* Hyperparameter Tuning
* Model Deployment using Flask/Streamlit
* Real-Time Image Classification
* Higher Accuracy through Advanced CNN Architectures

---

## 📚 Learning Outcomes

Through this project, I learned:

* Image Preprocessing
* Convolutional Neural Networks (CNNs)
* TensorFlow/Keras Model Development
* Training and Validation Techniques
* Overfitting Prevention using Dropout
* Performance Evaluation and Visualization

---

## ⭐ Support

If you found this project helpful, please consider giving it a ⭐ on GitHub.

---

## 📄 License

This project is intended for educational and learning purposes. Feel free to use, modify, and improve it.
