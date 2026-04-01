# 🎬 Movie Genre Classification using NLP & Machine Learning

## 📌 Project Overview

This project focuses on building a **Machine Learning model** that predicts the **genre of a movie** based on its plot description. It leverages **Natural Language Processing (NLP)** techniques such as text preprocessing and **TF-IDF vectorization**, combined with multiple classification algorithms.

The primary goal is to transform raw textual data into meaningful numerical features and accurately classify movies into genres like **Drama, Comedy, Thriller**, and more.

---

## 🖼️ Project Visualization

<p align="center">
  <img src="https://github.com/user-attachments/assets/75d7f09e-4b2d-4313-bd11-168bdd647e65" alt="Genre Classification" width="450"/>
</p>

---

## 📊 Exploratory Data Analysis (EDA)

The dataset was analyzed to extract meaningful insights:

* **📌 Genre Distribution**

  * Identified class imbalance across genres

* **📌 Text Length Analysis**

  * Observed variation in description lengths

* **📌 Word Frequency Analysis**

  * Extracted most common words

* **📌 Bigram Analysis**

  * Identified frequently occurring word pairs

* **📌 WordCloud Visualization**

  * Visual representation of genre-specific words

👉 **Insight:** Certain genres have distinctive vocabulary patterns, which significantly helps in classification.

---

## 🧹 Data Preprocessing

A custom preprocessing pipeline was implemented:

* Converted text to lowercase
* Removed special characters and numbers
* Removed extra spaces
* Cleaned both training and test datasets

---

## 🔠 Feature Engineering

Used **TF-IDF Vectorization** to convert text into numerical features:

* **Max Features:** 20,000
* **N-grams:** Unigrams + Bigrams
* **Stopwords:** Removed
* **Filtering:** Rare and overly frequent words removed

👉 This improved model performance by capturing contextual relationships between words.

---

## 🤖 Models Implemented

### 1️⃣ Naive Bayes

* Fast and efficient for text classification
* Performs well with TF-IDF features

### 2️⃣ Logistic Regression

* Handles high-dimensional sparse data effectively
* Used `class_weight='balanced'` to address class imbalance

### 3️⃣ Support Vector Machine (SVM)

* Strong performance for text classification
* Effective in high-dimensional feature spaces

---

## 🚀 Key Highlights

* ✅ End-to-end NLP pipeline
* ✅ Comparative analysis of multiple ML models
* ✅ Effective feature engineering using TF-IDF
* ✅ Handles class imbalance
* ✅ Scalable for advanced models like BERT

---

## 🛠️ Tech Stack

* **Programming Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn
* **Visualization:** Matplotlib, Seaborn
* **NLP Techniques:** TF-IDF, Text Preprocessing

---

## 📌 Conclusion

This project demonstrates how **text data can be transformed into structured numerical features** and used to build powerful classification models. It highlights the importance of:

* Exploratory Data Analysis (EDA)
* Data preprocessing
* Feature engineering

in achieving strong performance in NLP-based classification tasks.

---

## 🔮 Future Improvements

* Implement **BERT or Transformer-based models** for improved accuracy
* Hyperparameter tuning using GridSearchCV / RandomizedSearchCV
* Deploy the model using Flask or FastAPI
* Build an interactive UI for real-time predictions

---

