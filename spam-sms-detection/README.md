# SMS Spam Detection using Machine Learning

Classifies SMS messages as **spam** or **ham** (legitimate) using NLP preprocessing, TF-IDF features, and a comparison of six classifiers.

## Overview

The aim is to build an accurate model that automatically flags spam messages. Six algorithms are trained on the same TF-IDF pipeline and compared on a held-out test set.

## Dataset

**SMS Spam Collection Dataset**: 5,574 labeled messages, roughly 87% ham and 13% spam. After dropping duplicate and null rows, 5,169 messages remain.

| Column | Description |
|---|---|
| `label` | `spam` or `ham` |
| `message` | raw SMS text |

The data is not included in this repository. See [data/README.md](data/README.md) for download instructions.

## Pipeline

<p align="center">
  <img width="457" height="790" alt="SMS spam detection pipeline" src="https://github.com/user-attachments/assets/4b723328-97e8-483a-a419-2b89e43e9527" />
</p>

1. **Exploratory analysis:** class distribution, message length, word count, uppercase usage, special-character frequency, correlation heatmap, top words in spam vs ham, and word clouds.
2. **Preprocessing:** lowercasing, removing punctuation and digits, dropping duplicates and nulls, and encoding labels (ham = 0, spam = 1).
3. **Feature engineering:** TF-IDF vectorization with English stop words removed.
4. **Modeling:** Logistic Regression, Naive Bayes, SVM, Decision Tree, Random Forest, and KNN.
5. **Evaluation:** accuracy, precision, recall, F1, and confusion matrices.

## Results

| Model | Accuracy |
|---|---|
| **SVM** | **97.39%** |
| Random Forest | 96.62% |
| Naive Bayes | 95.94% |
| Logistic Regression | 95.36% |
| Decision Tree | 94.49% |
| KNN | 90.43% |

**Best model: Support Vector Machine.**

## Key Insights

- Spam messages tend to be longer than legitimate ones.
- Spam frequently uses words such as *free*, *win*, and *urgent*.
- Spam contains more special characters.
- Because only about 13% of messages are spam, recall on the spam class matters as much as overall accuracy. See the per-model classification reports in the notebook.

## Project Structure

```
spam-sms-detection/
├── spam-sms-detection.ipynb
├── data/
│   └── README.md
├── requirements.txt
└── README.md
```

## How to Run

```bash
pip install -r requirements.txt
# place spam.csv in data/ (see data/README.md)
jupyter notebook spam-sms-detection.ipynb
```

## Tech Stack

Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn, WordCloud
