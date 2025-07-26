## 🧥👟 `README.md` for: **Fashion MNIST Image Classification using CNN**

---

### 📌 **Project Overview**

This project builds a **Convolutional Neural Network (CNN)** from scratch using **TensorFlow/Keras** to classify images from the **Fashion MNIST dataset**.
The model identifies items like **shirts, shoes, bags, trousers, and coats** from grayscale images.

---

### 🧠 **What You’ll Learn**

* How CNNs work for **image classification**
* Layer-wise understanding: `Conv2D`, `MaxPooling2D`, `Flatten`, and `Dense`
* Visualizing training **accuracy and loss**
* Evaluating model using **confusion matrix**
* Preprocessing image data for deep learning

---

### 🧪 **Dataset: Fashion MNIST**

* 70,000 grayscale images of size **28×28**
* 10 clothing classes:

  * T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot

---

### 🚀 **Tech Stack**

* **Python**
* **TensorFlow / Keras**
* **Matplotlib**
* **Numpy**
* **Sklearn (Confusion Matrix)**

---

### 🧱 **Model Architecture**

```text
Input: (28, 28, 1) grayscale image

→ Conv2D(32 filters, 3×3 kernel, ReLU)
→ MaxPooling2D(2×2)
→ Flatten
→ Dense(64 neurons, ReLU)
→ Dense(10 neurons, Softmax for 10 classes)
```

---

### 📊 **Model Results**

* Training Accuracy: ✅ \~99%
* Validation Accuracy: ✅ \~91%
* Final Evaluation on test set showed strong generalization.
* Confusion Matrix revealed minor misclassifications (e.g., shirt vs. top).

---

### 📈 **Visualizations**

* Accuracy vs. Epochs
* Loss vs. Epochs
* Confusion Matrix using `ConfusionMatrixDisplay`

---

### 📎 **How to Run**

1. Run the notebook in Google Colab or Jupyter Notebook
2. It will:

   * Load and normalize Fashion MNIST data
   * Build CNN using Keras
   * Train & evaluate model
   * Plot performance metrics
3. Modify architecture, change filters, or add dropout to experiment further!

---

### 🧠 **Skills Practiced**

* Convolutional Neural Networks (CNN)
* Image data preprocessing
* Understanding `SparseCategoricalCrossentropy` loss
* Using softmax activation for multiclass classification
* Plotting learning curves

---

### 🙋‍♀️ **Author**

**Sushma Sandanshiv**
B.Tech Data Science | AI Enthusiast
🔗 LinkedIn: [Sushma Sandanshiv](https://www.linkedin.com/in/sushma-sandanshiv-2740422b7)
🌐 GitHub: [sushma-prog](https://github.com/sushma-prog)

---
