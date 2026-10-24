# Bank Customer Churn Prediction

Predicts whether a bank customer will leave (churn) so that a bank can target retention efforts. Four models are built and compared: Logistic Regression, Random Forest, Gradient Boosting, and a Keras neural network.

## Overview

Customer retention is a core business problem for financial institutions. This project explores what drives churn and builds classifiers that estimate each customer's likelihood of leaving.

**Objectives**

- Explore the data and the relationship between features and churn
- Build several models behind a consistent preprocessing pipeline
- Compare them with accuracy and ROC-AUC and pick the best

## Dataset

The Bank Customer Churn dataset (`Churn_Modelling.csv`) has 10,000 customers and 14 columns, including credit score, geography, gender, age, tenure, balance, number of products, card and activity status, and estimated salary. The target is `Exited` (1 = churned).

The data is not included in this repository. See [data/README.md](data/README.md) for download instructions.

## Pipeline

<p align="center">
  <img width="378" height="927" alt="Churn prediction pipeline" src="https://github.com/user-attachments/assets/287e62ef-559c-49ee-8a23-3004de5660f5" />
</p>

1. **Exploratory analysis:** churn distribution, demographics (age, gender, geography), feature relationships with churn, correlation heatmap, and pairplots.
2. **Preprocessing:** scikit-learn `ColumnTransformer` with standard scaling for numeric features and one-hot encoding for categorical features.
3. **Modeling:** Logistic Regression, Random Forest (100 trees), Gradient Boosting, and an ANN with two hidden layers (64 and 32 units) trained with early stopping.
4. **Evaluation:** accuracy, ROC-AUC, and classification reports on a held-out test set of 2,000 customers.

## Results

| Model | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | 0.8080 | 0.7747 |
| Random Forest | 0.8640 | 0.8522 |
| **Gradient Boosting** | **0.8700** | **0.8708** |
| ANN | 0.8545 | 0.8528 |

**Best model: Gradient Boosting.**

Recall on the churn class is the weak point for every model (0.19 for Logistic Regression and about 0.49 for Gradient Boosting), because only about 20% of customers churn. Improving it, for example with class weights or threshold tuning, is the clearest next step.

## Key Insights

- Older customers and customers with higher balances show a higher tendency to churn.
- Geography plays a role in churn behavior.
- Ensemble models clearly outperform the linear baseline.

## Project Structure

```
customer-churn-prediction/
├── customer-churn-prediction.ipynb
├── data/
│   └── README.md
├── requirements.txt
└── README.md
```

## How to Run

```bash
pip install -r requirements.txt
# place Churn_Modelling.csv in data/ (see data/README.md)
jupyter notebook customer-churn-prediction.ipynb
```

## Tech Stack

Python, pandas, NumPy, scikit-learn, TensorFlow/Keras, Matplotlib, Seaborn

## Acknowledgements

- CODSOFT Internship Program
- The open-source dataset providers
