# Credit Card Fraud Detection

Detects fraudulent credit card transactions in a highly imbalanced dataset using feature engineering, SMOTE oversampling, and three classifiers.

<p align="center">
  <img width="600" alt="Credit card fraud detection" src="https://github.com/user-attachments/assets/628cddd9-e57c-46d4-8700-4821cccb8de1" />
</p>

## Overview

The goal is to classify each transaction as fraudulent or legitimate. Fraud is rare (about 0.6% of the test set), so the project focuses on handling imbalance and on evaluating with precision, recall, and F1 for the fraud class rather than accuracy alone.

## Dataset

A simulated credit card transaction dataset covering 2019-2020, with 1,000 customers and 800 merchants. It includes transaction amount, merchant category, customer and merchant coordinates, timestamp, and customer demographics.

The data is not included in this repository. See [data/README.md](data/README.md) for download instructions.

## Approach

1. **Exploratory analysis:** class imbalance, fraud by hour of day, transaction amounts, and customer-to-merchant distance.
2. **Feature engineering:** hour, day, and month from the transaction time; customer age from date of birth; customer-to-merchant distance from the coordinates; and removal of identifier columns.
3. **Splitting:** stratified 80/20 train/test split so the fraud ratio is preserved in both sets.
4. **Imbalance handling:** SMOTE applied to the **training set only**, so the test set stays realistic.
5. **Modeling:** Logistic Regression, Decision Tree, and Random Forest.
6. **Evaluation:** confusion matrix, precision, recall, and F1 on the untouched test set (209,715 transactions, 1,201 fraudulent).

## Results

Metrics for the fraud class on the held-out test set:

| Model | Precision | Recall | F1 | Overall accuracy |
|---|---|---|---|---|
| Logistic Regression | 0.07 | 0.75 | 0.13 | 94% |
| Decision Tree | 0.12 | 0.88 | 0.20 | 96% |
| **Random Forest** | **0.63** | **0.79** | **0.70** | **99.6%** |

Random Forest gives the best balance: it catches 79% of fraud (951 of 1,201) while producing far fewer false alarms than the other models (565 vs 8,138 for the decision tree). The Decision Tree has the highest recall but flags many legitimate transactions as fraud.

The notebook ends with a sample prediction that takes a real transaction, sets a high amount and an unusual hour, and scores it with the trained Random Forest.

## Key Insights

- Fraud is highly imbalanced, so accuracy is misleading on its own.
- Fraud occurs more often during late-night hours.
- Higher transaction amounts are more likely to be fraudulent.
- A large distance between customer and merchant is associated with fraud.

## Project Structure

```
credit-card-fraud-detection/
├── credit-card-fraud-detection.ipynb
├── data/
│   └── README.md
├── requirements.txt
└── README.md
```

## How to Run

```bash
pip install -r requirements.txt
# place fraudTrain.csv in data/ (see data/README.md)
jupyter notebook credit-card-fraud-detection.ipynb
```

## Tech Stack

Python, pandas, NumPy, scikit-learn, imbalanced-learn (SMOTE), Matplotlib, Seaborn

## Future Improvements

- Tune the decision threshold and compare precision-recall curves
- Try gradient boosting models such as XGBoost or LightGBM
- Add cost-sensitive evaluation that reflects the real cost of missed fraud
- Evaluate on the separate `fraudTest.csv` for a time-based holdout
