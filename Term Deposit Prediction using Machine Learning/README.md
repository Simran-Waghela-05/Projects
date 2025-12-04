# **Term Deposit Prediction using Machine Learning**

This project builds a machine learning pipeline to predict whether a customer will subscribe to a **term deposit** based on the **Bank Marketing Dataset**.
It includes exploratory data analysis (EDA), data preprocessing, model training, evaluation, and feature importance analysis using **Logistic Regression** and **Random Forest**.

---

## 📂 **Project Structure**

```
.
├── Term Deposit Prediction using Machine Learning.ipynb
├── bank-full.csv
└── README.md
```

---

## 📘 **Overview**

Banks often run marketing campaigns to encourage customers to subscribe to term deposits. Predicting customer behavior helps optimize marketing budget and improve targeting.

This notebook walks through:

* Importing and cleaning the dataset
* Exploring features and target imbalance
* Handling missing/unknown values
* Encoding categorical variables
* Model training & evaluation
* Feature importance extraction
* ROC Curve and AUC comparison
* Threshold tuning for improving recall

---

## 📊 **Dataset Information**

**Source:** Bank Marketing Dataset
**Rows:** ~45,000
**Columns:** 17
**Target Variable:**

* `y` → whether the customer subscribed to a term deposit (`yes`/`no`)

The features include:

* **Demographics:** age, job, marital status, education
* **Financial:** balance, housing loan, personal loan
* **Campaign-related:** contact type, number of contacts, previous outcomes
* **Economic indicators:** euribor rate, employment variation rate, etc.

---

## 🧹 **Data Preprocessing**

* Checked for missing values and handled `"unknown"` categories
* Separated numerical and categorical features
* Performed label encoding / one-hot encoding
* Standardized numerical variables where necessary
* Split data into **train-test sets**

---

## 🤖 **Models Trained**

### 1️⃣ **Logistic Regression**

* Baseline linear model
* Evaluated with accuracy, precision, recall, and F1-score

### 2️⃣ **Random Forest Classifier**

* Ensemble model that outperformed Logistic Regression
* Extracted **top 3 important features**

### 📈 **Metrics Compared**

* Accuracy
* Precision
* Recall
* F1-score
* ROC Curve & AUC
* Decision threshold tuning at 0.5, 0.4, 0.3

---

## 🎯 **Key Results**

* Random Forest achieved better **recall**, **precision**, and **AUC** than Logistic Regression
* Top important features identified from Random Forest
* Lowering the decision threshold increased recall at the cost of precision
* ROC Curve plotted for best model


---

## 🛠️ **Technologies & Libraries Used**

* Python 3
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

---

## 📌 **How to Run**

1. Clone or download this repository
2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook "Term Deposit Prediction using Machine Learning.ipynb"
```

4. Run all cells to reproduce the results.

---

## 📚 **Future Improvements**

* Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)
* Gradient Boosting models (XGBoost, LightGBM, CatBoost)
* Handling class imbalance with SMOTE
* Deploying the model via Flask or FastAPI
* Adding a UI dashboard

---

## 🙌 **Acknowledgments**

Dataset inspired by the UCI Machine Learning Repository – Bank Marketing Dataset.

---
