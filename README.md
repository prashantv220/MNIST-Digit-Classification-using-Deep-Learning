# 🔢 MNIST Digit Classification using Deep Learning

This project implements **digit classification** on the **MNIST dataset** using **Deep Learning (Keras/TensorFlow)**.  
The objective is to build, train, and evaluate a **Convolutional Neural Network (CNN)** that can recognize handwritten digits (0–9) with high accuracy.

---

## 📂 Dataset

The **MNIST dataset** is a benchmark dataset for image classification. It contains:

- **60,000 training images** (28×28 pixels, grayscale)  
- **10,000 test images** (28×28 pixels, grayscale)  
- Each image corresponds to a digit **0–9**  

This dataset is directly available in Keras.

---

## ⚙️ Project Workflow

The project follows these steps:

### 1. **Importing Libraries**
We use:
- **TensorFlow/Keras** for deep learning  
- **NumPy** for numerical computations  
- **Matplotlib** for visualization  

---

### 2. **Loading the Dataset**
The MNIST dataset is loaded and split into **training** and **test** sets.

---

### 3. **Preprocessing**
- Normalize pixel values from `[0–255]` → `[0–1]`  
- Reshape images into CNN-friendly format `(28, 28, 1)`  
- Convert labels to **one-hot encoded vectors**  

---

### 4. **Model Architecture**
We design a **CNN model** with the following layers:

- **Conv2D** (32 filters) + **MaxPooling2D**  
- **Conv2D** (64 filters) + **MaxPooling2D**  
- **Flatten** → fully connected layer (128 units, ReLU)  
- **Dropout (0.5)** to prevent overfitting  
- **Dense (10 units, Softmax)** for classification into digits 0–9  

---

### 5. **Compiling the Model**
- Optimizer: **Adam**  
- Loss function: **Categorical Crossentropy**  
- Metric: **Accuracy**  

---

### 6. **Training**
- Trained for **10 epochs**  
- **Batch size:** 128  
- **Validation split:** 10% of training data  

---

### 7. **Evaluation**
- **Test Accuracy:** ~98%  
- Model generalizes well on unseen data  

---

### 8. **Visualization**
We plot:
- **Training vs Validation Accuracy**  
- **Training vs Validation Loss**  

Additionally, predictions are visualized for random test samples, showing both **predicted** and **true labels**.

---

## 📊 Results

- **Training Accuracy:** ~99%  
- **Test Accuracy:** ~98%  
- Misclassifications mostly occur for visually similar digits (e.g., 4 vs 9).  

CNN significantly outperforms fully connected networks on MNIST.

---
   git clone https://github.com/yourusername/mnist-classification.git
   cd mnist-classification
