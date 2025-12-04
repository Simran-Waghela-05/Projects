---

# **Fake News Detection using Machine Learning**

This project builds a machine learning model to automatically classify news articles as **Real** or **Fake**.
It involves text preprocessing, feature extraction, exploratory data analysis, model training, and evaluation.
The goal is to develop a reliable system that helps identify misinformation based on the content of the article.

---

## 📘 **Project Overview**

The Fake News Detection system uses natural language processing (NLP) techniques and traditional machine learning classifiers to analyze the text of news articles.

This project covers:

* Data cleaning and preprocessing
* Tokenization and text normalization
* TF-IDF vectorization
* Training multiple ML models
* Comparing classification performance
* Predicting whether unseen news is real or fake 

---

## 📂 **Project Structure**

```
Fake-News-Detection/
│
├── Fake News Detection Notebook.ipynb or PDF
├── dataset:(True.csv/Fake.csv)    # CSV files
└── README.md
```
---
This project uses the Fake and Real News Dataset from Kaggle, which contains two separate CSV files:

- **True.csv** – contains legitimate news articles  
- **Fake.csv** – contains fabricated or misleading news content
<br>Kaggle dataset link: https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset
---
---

## 🧹 **Data Preprocessing**

The following preprocessing steps are applied to clean the dataset:

* Handling missing values
* Removing punctuation and special symbols
* Converting text to lowercase
* Stopword removal
* Lemmatization/Stemming
* Tokenization
* Converting raw text into TF-IDF numeric vectors

These steps help normalize text for better model performance.

---

## 🤖 **Machine Learning Models Used**

The project evaluates two ML models, including:

* **Naive Bayes (MultinomialNB)**
* **Support Vector Machine (SVM)**

Model performance is compared using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## 🧪 **Evaluation Summary**

The notebook shows detailed evaluation metrics, including:

* False positives and false negatives
* Classifier comparison
* To improve model performance, the notebook includes k-Fold Cross-Validation for robust evaluation and RandomizedSearchCV for hyperparameter tuning.
* This helps identify the best model configuration while reducing overfitting and improving generalization.
---

## 📈 **Example Workflow**

1. Load training dataset
2. Clean and preprocess text
3. Convert text using TF-IDF vectorizer
4. Train ML models
5. Evaluate and compare performances
6. Save the best model 
7. Predict fake/real news for new input text

---

## ▶️ **How to Run the Project**

### **Option 1 — Open the Jupyter Notebook**

1. Install dependencies:

```bash
pip install pandas numpy sklearn matplotlib seaborn nltk
```

2. Open the notebook:

```bash
jupyter notebook "Fake News Detection Notebook.ipynb"
```

3. Run the cells sequentially.

---

## 🛠️ **Technologies Used**

* Python
* Pandas, NumPy
* Scikit-learn
* NLTK / SpaCy
* Matplotlib, Seaborn (for visualizations)
* Jupyter Notebook

---

## 🚀 **Future Improvements**

* Deep learning models (LSTMs, BiLSTM, BERT)
* Web application using Flask / FastAPI
* Real-time prediction with API
* Dataset expansion for multilingual fake news detection
* Explainability using SHAP/LIME

---
