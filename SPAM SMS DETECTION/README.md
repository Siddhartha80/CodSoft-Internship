# 📩 SMS Spam Detection using Machine Learning

🚀 This project focuses on building a machine learning model to classify SMS messages as **Spam** or **Ham (Legitimate)** using Natural Language Processing (NLP) techniques.

---

## 📊 Dataset

- **Name:** SMS Spam Collection Dataset  
- **Size:** 5,574 messages  
- **Classes:**
  - Ham (Legitimate) → ~87%
  - Spam → ~13%

Each message contains:
- `label` → spam / ham  
- `message` → raw SMS text  

---

## 🎯 Objective

To develop an accurate classification model that can automatically detect spam messages using machine learning techniques.

---

## Architecture Diagram

<img width="457" height="790" alt="SMS" src="https://github.com/user-attachments/assets/4b723328-97e8-483a-a419-2b89e43e9527" />

---

## 🔍 Exploratory Data Analysis (EDA)

Performed extensive EDA to understand patterns in the data:

- 📌 Class distribution analysis  
- 📏 Message length analysis  
- 🧮 Word count analysis  
- 🔠 Uppercase usage  
- ✨ Special character frequency  
- 🔗 Feature correlation heatmap  
- 📊 Histograms & boxplots  
- 🔝 Top words in spam vs ham  
- ☁️ WordCloud visualization  

---

## 🧹 Data Preprocessing

- Converted text to lowercase  
- Removed punctuation and numbers  
- Cleaned text data  
- Removed duplicates and null values  
- Label encoding (ham → 0, spam → 1)

---

## 🧠 Feature Engineering

- TF-IDF Vectorization used to convert text into numerical features  

---

## 🤖 Machine Learning Models

The following models were implemented and compared:

- Logistic Regression  
- Naive Bayes  
- Support Vector Machine (SVM)  
- Decision Tree  
- Random Forest  
- K-Nearest Neighbors (KNN)  

---

## 📊 Model Performance

| Model                | Accuracy |
|---------------------|---------|
| SVM ⭐              | **97.38%** |
| Random Forest       | 96.61% |
| Naive Bayes         | 95.94% |
| Logistic Regression | 95.36% |
| Decision Tree       | 94.48% |
| KNN                 | 90.42% |

🏆 **Best Model: Support Vector Machine (SVM)**

---

## 📈 Evaluation Metrics

- Accuracy Score  
- Precision, Recall, F1-score  
- Confusion Matrix  
- Model Comparison Visualization  

---

## 💡 Key Insights

- Spam messages tend to be longer  
- Frequent use of words like: *free, win, urgent*  
- Higher use of special characters in spam messages  
- Clear textual patterns help distinguish spam from ham  

---

## 🛠️ Tech Stack

- Python 🐍  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  
- NLP (TF-IDF, text preprocessing)  

---


