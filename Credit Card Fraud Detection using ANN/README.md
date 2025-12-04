---

# 💳 Credit Card Fraud Detection Using Artificial Neural Network (ANN)

This project builds an **Artificial Neural Network (ANN)** model to identify fraudulent credit card transactions in a real-world, highly imbalanced dataset.
The objective is to develop a reliable classification system capable of detecting fraud with high recall while maintaining strong overall performance.

---

## 📘 Project Overview

Credit card fraud is a significant financial issue, with fraudulent transactions representing only a tiny fraction of all transactions.
Such imbalance makes fraud detection a challenging task for traditional machine learning models.

This project applies **deep learning (ANN)** techniques along with data preprocessing and balancing strategies to create a robust fraud classification model.
The full implementation is provided in a **Jupyter Notebook**.

---

## 🎯 Objectives

* Build a deep learning model (ANN) for binary classification
* Handle class imbalance effectively
* Improve recall to reduce missed fraud cases
* Analyze performance using multiple evaluation metrics
* Provide a clean, reproducible notebook for experimentation

---

## 🧠 Features of the Model

* **Artificial Neural Network architecture** built using TensorFlow/Keras
* **Balanced training data** through sampling techniques
* **Feature scaling** for improved learning performance
* **Training visualization** (loss & accuracy curves)
* **Comprehensive evaluation**, including:

  * Confusion Matrix
  * Classification Report
  * Precision, Recall, F1-Score
  * ROC Curve & AUC Score

---

## 📊 Dataset Details

* Contains anonymized credit card transaction data
* Features: **Time**, **Amount**, and PCA-transformed features (**V1–V28**)
* Target column:

  * `0` → Legitimate
  * `1` → Fraud
* Highly imbalanced (fraudulent transactions ≪ normal transactions)

---

## 🚀 Technologies & Libraries Used

* **Python**
* **Jupyter Notebook**
* **TensorFlow / Keras**
* **Pandas / NumPy**
* **Scikit-learn**
* **Matplotlib / Seaborn**

---

## 📁 Repository Contents

| File                                          | Description                                                                 |
| --------------------------------------------- | --------------------------------------------------------------------------- |
| `Credit_Card_Fraud_Detection_using_ANN.ipynb` | Complete ANN model: preprocessing, training, evaluation, and visualizations |
| `creditcard.csv`                                 | Credit card transaction dataset used for training and testing, kaggle dataset link: https://www.kaggle.com/datasets/arockiaselciaa/creditcardcsv <br>You can download the dataset from here|
| `README.md`                                   | Documentation for the project                                               |

---

## ▶️ How to Run the Project

1. Install required libraries:

   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn tensorflow
   ```

2. Launch the notebook:

   ```bash
   jupyter notebook Credit_Card_Fraud_Detection_using_ANN.ipynb
   ```

3. Run all cells in sequence to reproduce the results.

---

## 🔍 Key Takeaways

* ANN models can effectively detect fraud when trained with balanced data.
* Sampling techniques drastically improve recall.
* Deep learning provides flexibility for modeling complex patterns in transaction behavior.
* Proper evaluation ensures the model is suitable for high-risk, real-world financial applications.

---
