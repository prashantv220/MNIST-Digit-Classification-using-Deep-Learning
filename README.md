# 🔢 MNIST Digit Classification using Deep Learning

This repository contains an end-to-end implementation of **digit classification** on the **MNIST dataset** using **Deep Learning (Keras/TensorFlow)**.  
The goal is to build, train, and evaluate a neural network that can recognize handwritten digits (0–9) with high accuracy.

---

## 📂 Dataset

The **MNIST dataset** is included in Keras and contains:

- **60,000 training images** (28×28 pixels, grayscale)
- **10,000 test images** (28×28 pixels, grayscale)
- Each image corresponds to a digit **0–9**
- Labels are integers (0–9)

---

## ⚙️ Project Workflow

### 1. **Importing Libraries**
```python
import numpy as np
import matplotlib.pyplot as plt
from tensorflow.keras.datasets import mnist
from tensorflow.keras.utils import to_categorical
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Dense, Flatten, Conv2D, MaxPooling2D, Dropout
