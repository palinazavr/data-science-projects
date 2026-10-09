# 11. Machine Learning for Texts: Toxic Comment Detection

## Goal

Train a model that classifies user comments as toxic or non-toxic, so that an online service can send negative comments to its support team. The F1 metric on the test set must be at least 0.75.

## Tasks

1. Clean and lemmatize the comments (`nltk`), remove punctuation and stop words.
2. Vectorize the texts with TF-IDF.
3. Train logistic regression, NB-SVM (implemented with logistic regression) and a linear SVM (`LinearSVC`) with `GridSearchCV`.
4. Evaluate the models on the test set.

## Results

- 10% of the 159,292 comments are toxic, so accuracy alone is misleading (a constant model already has 0.90).
- All three models reach an F1 of 0.775-0.788 on the test set, above the 0.75 requirement.
- The best result is given by NB-SVM (F1 0.788).

## Data

`toxic_comments.csv`: the comment text (`text`) and the label (`toxic`). The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it. The `nltk` resources `wordnet`, `punkt` and `stopwords` are downloaded by the notebook.

## Stack

python, pandas, numpy, scikit-learn, nltk (TF-IDF, NLP)

## Notebook

[ml_for_text_classification.ipynb](ml_for_text_classification.ipynb)
