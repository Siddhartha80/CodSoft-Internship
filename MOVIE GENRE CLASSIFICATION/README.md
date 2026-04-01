## 🎬 Movie Genre Classification using NLP & Machine Learning

📌 Project Overview

This project focuses on building a Machine Learning model that predicts the genre of a movie based on its plot description. The system leverages Natural Language Processing (NLP) techniques such as text preprocessing and TF-IDF vectorization, combined with multiple classification algorithms.

The goal is to transform raw textual data into meaningful numerical features and accurately classify movies into genres like drama, comedy, thriller, etc.


<img width="438" height="678" alt="Genre Classification" src="https://github.com/user-attachments/assets/75d7f09e-4b2d-4313-bd11-168bdd647e65" />


📊 Exploratory Data Analysis (EDA)

The dataset was analyzed to extract meaningful insights:

📌 Genre Distribution: Identified class imbalance across genres

📌 Text Length Analysis: Observed variation in description lengths

📌 Word Frequency Analysis: Extracted most common words

📌 Bigram Analysis: Identified frequently occurring word pairs

📌 WordCloud Visualization: Visual representation of genre-specific words

👉 Insight: Certain genres have distinctive vocabulary patterns, which helps in classification.

🧹 Data Preprocessing

A custom preprocessing pipeline was implemented:
  Converted text to lowercase
  Removed special characters and numbers
  Removed extra spaces
  Cleaned both training and test datasets

🔠 Feature Engineering

Used TF-IDF Vectorization to convert text into numerical features:
  Max Features: 20,000
  N-grams: Unigrams + Bigrams
  Stopwords removed
  Rare and overly frequent words filtered

👉 This significantly improved model performance by capturing contextual information.

🤖 Models Implemented
1. Naive Bayes
  Fast and efficient for text classification
  Works well with TF-IDF features
2. Logistic Regression
  Handles high-dimensional sparse data effectively
  Used with class_weight='balanced' to address imbalance
3. Support Vector Machine (SVM)
  Strong performance for text classification
  Effective in high-dimensional space

