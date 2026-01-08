# malaria-detection-cnn
Deep Learning model (CNN) to detect Malaria parasites in blood cell images with 95%+ accuracy. Built with TensorFlow/Keras.
# Malaria Detection using Deep Learning (CNN)

[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat-square&logo=tensorflow)](https://www.tensorflow.org/)
[![Keras](https://img.shields.io/badge/Keras-Applied-red?style=flat-square&logo=keras)](https://keras.io/)
[![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)](https://www.python.org/)

## 📌 Project Overview
This project focuses on automating the diagnosis of malaria from blood smear images. Using a **Convolutional Neural Network (CNN)**, the model classifies cell images as either "Parasitized" or "Uninfected".

- **Dataset:** 27,558 cell images from the NIH (National Institutes of Health).
- **Goal:** Provide a high-accuracy diagnostic tool to assist medical professionals in resource-constrained environments.

## 🔬 Exploratory Data Analysis (EDA)
Real-world medical images vary in resolution. By analyzing the dataset distribution, I determined an optimal input size to balance detail retention and computational efficiency.
- **Average Dimensions:** ~130x130 pixels.
- **Input Shape:** `(130, 130, 3)`.



## 🛠️ Data Preprocessing & Augmentation
To prevent **overfitting** and ensure the model generalizes well to new samples, I implemented:
- **Rescaling:** Pixel normalization (1/255).
- **Real-time Augmentation:** Random rotations, zooms, and horizontal flips using `ImageDataGenerator`.

## 🏗️ Model Architecture
The CNN architecture is designed to capture spatial hierarchies in cell features:
1. **Convolutional Layers (3x):** Feature extraction (edges, textures, parasite shapes).
2. **MaxPooling:** Spatial reduction for translation invariance.
3. **Dropout (0.5):** Strong regularization to prevent co-dependency between neurons.
4. **Output Layer:** Single neuron with **Sigmoid** activation for binary classification.



## 📊 Performance Evaluation
The model was evaluated using a **Confusion Matrix** and a **Classification Report**. In medical diagnostics, minimizing **False Negatives (Recall)** is the priority.

| Metric | Score |
| :--- | :--- |
| **Accuracy** | 95%+ |
| **Recall (Infected)** | Optimized via custom threshold |



## 🚀 How to use
1. Clone the repository.
2. Install dependencies: `pip install tensorflow pandas numpy matplotlib seaborn scikit-learn`.
3. Run the notebook: `Malaria_Detection.ipynb`.

## 👨‍💻 Author
**Karim**
*Graduate Engineer from IMT Atlantique*
*Specialized in Machine Learning & Data Science*
