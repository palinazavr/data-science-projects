# 06. Supervised Learning: Bank Customer Churn

## Goal

Predict whether a bank customer will leave in the near future, using the history of customer behavior and contract terminations. The metric is F1 (at least 0.59); AUC-ROC is measured as well.

## Tasks

1. Prepare the data: scaling, one-hot encoding, handling the missing values in `Tenure`.
2. Train a decision tree, a random forest and logistic regression without accounting for the class imbalance.
3. Fix the class imbalance (class weights, upsampling, downsampling) and compare the models.
4. Evaluate the best models on the test set.

## Results

- The classes are imbalanced 4:1; without a fix the best F1 is 0.58 (random forest), below the target.
- Class weights did not help much; upsampling and downsampling did.
- On the test set the random forest reaches F1 0.63 and AUC-ROC 0.77, and the decision tree F1 0.62 and AUC-ROC 0.78. Both satisfy the requirement.

## Data

`Churn.csv`: customer features (credit score, geography, gender, age, tenure, balance, number of products, activity) and the target `Exited`. The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it.

## Stack

python, pandas, numpy, scikit-learn, matplotlib, seaborn

## Notebook

[supervised_machine_learning.ipynb](supervised_machine_learning.ipynb)
