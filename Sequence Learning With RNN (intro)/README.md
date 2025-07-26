## 📘 `README.md` for: **IMDB Sentiment Classification using RNN (LSTM)**

---

### 📌 **Project Overview**

This project is a **Sentiment Analysis model** built using a **Recurrent Neural Network (RNN)** with **LSTM layers** on the **IMDB movie review dataset**.
It classifies whether a review is **positive** or **negative** based on its text content.

---

### 🚀 **Tech Stack**

* **Python**
* **TensorFlow / Keras**
* **Numpy**
* **Matplotlib**
* **Sklearn**

---

### 🧠 **Model Architecture**

```text
Input (Movie Review Sequences)
→ Embedding Layer
→ LSTM Layer (32 units)
→ Dense Layer (1 unit with Sigmoid activation)
→ Output: 0 (Negative) or 1 (Positive)
```

---

### 🗂️ **Key Steps**

1. **Load IMDB dataset** from `keras.datasets`
2. **Pad sequences** to ensure equal length
3. **Build RNN model** with LSTM layers
4. **Compile & train** using `binary_crossentropy` loss
5. **Evaluate** on test data and **plot confusion matrix**

---

### 📊 **Results**

* Training Accuracy: ✅ \~98%
* Validation Accuracy: ✅ \~89%
* Confusion Matrix: Good performance, with some misclassifications
* **Model correctly learned to differentiate positive vs. negative reviews**

---

### 📎 **How to Run**

1. Open the notebook in **Google Colab** or Jupyter
2. Run all cells step-by-step
3. You can experiment by:

   * Changing the number of LSTM units
   * Using Bidirectional LSTM
   * Trying GRU instead of LSTM

---

### ✅ **Learning Outcomes**

* Understood how RNNs (LSTMs) process sequential text data
* Learned padding, embedding, and how sequences are fed to LSTMs
* Used binary classification with sigmoid output
* Visualized model accuracy and confusion matrix
* Developed a complete end-to-end DL NLP project

---

### 🙌 **Author**

**Sushma Sandanshiv**
B.Tech Data Science | Aspiring Data Scientist
🌐 GitHub: [sushma-prog](https://github.com/sushma-prog)
🔗 LinkedIn: [Sushma Sandanshiv](https://www.linkedin.com/in/sushma-sandanshiv-2740422b7)

---
