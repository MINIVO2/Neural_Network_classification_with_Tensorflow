# Neural Network Classification with TensorFlow

This notebook demonstrates how to build, train, and evaluate neural networks using TensorFlow and Keras for both binary and multiclass classification problems. It includes hands-on experiments, evaluation techniques, and techniques to optimize model performance such as learning rate scheduling and data normalization.

---

## 📚 Table of Contents

- [Introduction](#introduction)
- [Binary Classification](#binary-classification)
  - Creating the dataset
  - Understanding input and output shapes
  - Building and training multiple models
  - Evaluating models
  - Visualizing decision boundaries
  - Confusion Matrix and Accuracy
- [Multiclass Classification](#multiclass-classification)
  - Using Fashion MNIST dataset
  - Visualizing data samples
  - Model building (one-hot vs non-one-hot)
  - Normalizing input data
  - Comparing normalized vs non-normalized performance
  - Finding the ideal learning rate
- [Key Takeaways](#key-takeaways)

---

## 🧠 Introduction

This notebook serves as an introduction to neural networks with TensorFlow. It focuses on binary and multiclass classification tasks using dense (fully connected) layers and common activation functions like ReLU and softmax.

---

## ✅ Binary Classification

### 📊 Dataset
A custom 2D dataset is generated for classification purposes using helper functions.

### 🔧 Steps in Modeling:
1. Define the model using `Sequential`
2. Compile with appropriate `loss`, `optimizer`, and `metrics`
3. Train with `fit`
4. Evaluate with `evaluate`

### 🔁 Models Trained
- **Model 1–9:** Experimented with different architectures and learning rates
- **Model 10:** Introduced **Binary Focal Crossentropy** with a tuned learning rate (0.017)

### 🔍 Evaluation
- Loss and Accuracy tracked over 100 epochs
- Visualized using Matplotlib
- Found optimal learning rate with exponential scaling

### 📉 Visualizations
- Decision boundary plots for train and test data
- Confusion matrix using `sklearn.metrics.confusion_matrix`

---

## 👗 Multiclass Classification

### 📁 Dataset
- **Fashion MNIST** from TensorFlow Datasets
- 10 classes like "T-shirt", "Trouser", "Sneaker", etc.

### 📊 Data Preprocessing
- Normalized pixel values (0–255 → 0–1)
- Used both **One-hot encoded** and **sparse** labels

### 🏗️ Models
- **Model 11:** One-hot encoded output, without normalization
- **Model 12:** Sparse categorical crossentropy with normalized input
- **Model 13:** Learning Rate Finder
- **Model 14:** Final optimized model using fixed learning rate

### 📉 Evaluation & Visualization
- Accuracy and loss trends over epochs
- Learning rate vs loss (semilog plot)
- Final evaluation with predictions and confusion matrix

---

## 📌 Key Takeaways

- Learning rate significantly affects model performance
- Normalizing input data improves accuracy
- Confusion matrix helps in visualizing classification performance
- Binary vs Multiclass classification require different approaches
- One-hot encoding is optional, but must match the loss function

---

## 📦 Technologies Used

- Python
- TensorFlow / Keras
- NumPy, Pandas
- Matplotlib
- Scikit-learn

---

## 🚀 How to Run

1. Install dependencies:
   ```bash
   pip install tensorflow numpy matplotlib pandas scikit-learn
   ```
2. Run the Jupyter Notebook:
   ```bash
   jupyter notebook 02_neural_network_classification_with_tf.ipynb
   ```

---

Let me know if you want to include a badge, GitHub link, or contributor section as well!
