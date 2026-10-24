# Machine Learning Projects: CODSOFT Internship

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Jupyter](https://img.shields.io/badge/Notebooks-Jupyter-orange)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

Four end-to-end machine learning projects completed during the **CODSOFT Machine Learning Internship**. Each project walks through the full workflow: data loading, exploratory analysis, preprocessing, feature engineering, model training, evaluation, and a written summary of the findings.

## Projects

| Project | Task | Techniques | Best model | Result |
|---|---|---|---|---|
| [Movie Genre Classification](movie-genre-classification/) | Multi-class text classification | TF-IDF (unigrams + bigrams) | Linear SVM | 57.3% validation accuracy |
| [Credit Card Fraud Detection](credit-card-fraud-detection/) | Imbalanced binary classification | SMOTE, feature engineering | Random Forest | Fraud class: 0.63 precision, 0.79 recall, 0.70 F1 |
| [Customer Churn Prediction](customer-churn-prediction/) | Binary classification | Pipelines, ensembles, Keras ANN | Gradient Boosting | 87.0% accuracy, 0.871 ROC-AUC |
| [Spam SMS Detection](spam-sms-detection/) | Binary text classification | TF-IDF, model comparison | SVM | 97.39% accuracy |

Results are taken directly from the saved outputs in each notebook.

## Skills Demonstrated

- **Machine learning:** logistic regression, naive Bayes, SVM, decision trees, random forests, gradient boosting, k-nearest neighbours, and a feed-forward neural network
- **NLP:** text cleaning, TF-IDF vectorization, n-grams, word clouds
- **Imbalanced data:** SMOTE oversampling, class weighting, stratified splits, precision/recall trade-offs
- **Evaluation:** accuracy, precision, recall, F1, ROC-AUC, confusion matrices
- **Tooling:** Python, pandas, NumPy, scikit-learn, imbalanced-learn, TensorFlow/Keras, Matplotlib, Seaborn

## Repository Structure

```
.
├── movie-genre-classification/
│   ├── movie-genre-classification.ipynb
│   ├── data/              # dataset goes here (see data/README.md)
│   ├── requirements.txt
│   └── README.md
├── credit-card-fraud-detection/
├── customer-churn-prediction/
├── spam-sms-detection/
├── LICENSE
└── README.md
```

Every project folder follows the same layout.

## Getting Started

```bash
git clone https://github.com/Siddhartha80/codsoft-internship.git
cd codsoft-internship/spam-sms-detection      # or any other project folder

python -m venv .venv
source .venv/bin/activate                      # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# Download the dataset as described in data/README.md, then:
jupyter notebook
```

Datasets are not stored in this repository. Each project's `data/README.md` explains what to download and where to put it. The notebooks read from the relative `data/` path.

## Author

**Siddhartha Mettu**, M.S. Data Science student at Arizona State University.

- LinkedIn: [siddhartha-mettu](https://www.linkedin.com/in/siddhartha-mettu/)
- GitHub: [Siddhartha80](https://github.com/Siddhartha80)

## License

Released under the [MIT License](LICENSE).
