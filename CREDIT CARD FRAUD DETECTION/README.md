# 💳 Credit Card Fraud Detection

This project focuses on detecting fraudulent credit card transactions using Machine Learning techniques. The dataset used is a simulated real-world dataset containing both legitimate and fraudulent transactions.

---

## 📌 Project Overview

The goal of this project is to build a classification model that can accurately identify whether a transaction is fraudulent or legitimate.

---

## 📊 Dataset

- Simulated credit card transaction dataset (2019–2020)
- 1000 customers, 800 merchants
- Includes transaction details such as:
  - Amount
  - Merchant category
  - Location (lat/long)
  - Time of transaction
  - Customer demographics

---

## ⚙️ Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Imbalanced-learn (SMOTE)

---

## 🔍 Exploratory Data Analysis

Key insights:
- Fraud transactions are highly imbalanced
- Fraud occurs more during late-night hours
- High transaction amounts are more suspicious
- Large distance between customer and merchant indicates fraud

---

## 🤖 Models Used

- Logistic Regression
- Decision Tree
- Random Forest (Best Performing)

---

## ⚖️ Handling Imbalance

- Applied SMOTE to balance the dataset and improve fraud detection

---

## 📈 Model Evaluation

Models were evaluated using:
- Confusion Matrix
- Precision, Recall, F1-score

Random Forest achieved the best performance in detecting fraudulent transactions.

---

## 🧪 Sample Prediction

The model can predict fraud for new transactions by analyzing features like:
- Transaction amount
- Time
- Location distance

---

## 📌 Conclusion

This project demonstrates how Machine Learning can be effectively used to detect fraud in financial transactions and highlights the importance of feature engineering and handling imbalanced data.

