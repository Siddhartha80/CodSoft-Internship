# Movie Genre Classification using NLP

Predicts the genre of a movie from its plot description using text preprocessing, TF-IDF features, and classical machine learning classifiers.

<p align="center">
  <img src="https://github.com/user-attachments/assets/75d7f09e-4b2d-4313-bd11-168bdd647e65" alt="Genre classification overview" width="450"/>
</p>

## Overview

The goal is to turn raw plot text into numerical features and classify each movie into one of many genres such as Drama, Comedy, or Thriller. Three models are trained and compared on a held-out validation split, and Logistic Regression is then used to predict genres for the unlabeled test set.

## Dataset

**Genre Classification Dataset (IMDb)**, split into `train_data.txt` (labeled) and `test_data.txt` (unlabeled). Fields are separated by ` ::: `.

The data is not included in this repository. See [data/README.md](data/README.md) for download instructions.

## Approach

1. **Exploratory analysis:** genre distribution (strong class imbalance), description length, word frequencies, bigrams, and word clouds.
2. **Preprocessing:** lowercasing, removing special characters and digits, and collapsing extra whitespace, applied to both train and test sets.
3. **Feature engineering:** TF-IDF with up to 20,000 features, unigrams and bigrams, English stop words removed, and rare and overly frequent terms filtered out.
4. **Modeling:** Naive Bayes, Logistic Regression (`class_weight='balanced'`), and a Linear SVM.
5. **Evaluation:** accuracy and a per-genre classification report on the validation split.

## Results

| Model | Validation accuracy |
|---|---|
| Naive Bayes | 50.2% |
| Logistic Regression | 49.6% |
| **Linear SVM** | **57.3%** |

Accuracy is modest because this is a 27-class problem with heavy imbalance. The per-class report in the notebook shows good precision on the most frequent genres (about 0.7-0.8) and weak precision and recall on rare ones. Linear SVM gave the best validation accuracy.

## Key Takeaways

- Genres have distinctive vocabulary, which TF-IDF captures well.
- Adding bigrams helps by preserving some local context.
- Class imbalance is the main limiting factor, so accuracy alone overstates how well rare genres are handled.

## Project Structure

```
movie-genre-classification/
├── movie-genre-classification.ipynb
├── data/
│   └── README.md
├── requirements.txt
└── README.md
```

## How to Run

```bash
pip install -r requirements.txt
# place train_data.txt and test_data.txt in data/ (see data/README.md)
jupyter notebook movie-genre-classification.ipynb
```

The final cell writes `submission.csv` with Logistic Regression predictions for the test set. It is git-ignored.

## Tech Stack

Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn, WordCloud

## Future Improvements

- Try transformer-based models such as BERT
- Tune hyperparameters with GridSearchCV or RandomizedSearchCV
- Report macro-averaged F1 and handle rare genres explicitly
- Serve the model with Flask or FastAPI and add a simple UI
