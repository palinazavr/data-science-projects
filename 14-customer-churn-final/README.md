# 14. Final Project: Telecom Customer Churn Prediction

## Goal

Predict the churn of customers of a telecom operator, so that the operator can offer discounts and special conditions to the customers who are about to leave. The main metric is ROC-AUC; accuracy is an additional metric.

## Tasks

1. Merge the four source tables (contracts, personal data, internet and phone services) and build the target (the customer left or not).
2. Explore the data and engineer features (for example `lifetime`, the number of months of using the services).
3. Train and compare a logistic regression, a random forest and CatBoost with cross-validation (stratified split because of the class imbalance).
4. Select the best model, check it on the test set and analyze the feature importance.

## Results

- Churn is imbalanced (the constant model has an accuracy of 0.734).
- CatBoost is the best model: ROC-AUC **0.894** and accuracy 0.842 on the test set (random forest: 0.860 and 0.812; logistic regression: ROC-AUC 0.846 in cross-validation).
- The most important features are `lifetime`, `Type` (payment type), `MonthlyCharges`, `TotalCharges` and `fiber_optic`.
- The customers who left paid more per month on average, often paid with electronic checks and often used fiber optic.

## Data

`contract.csv`, `personal.csv`, `internet.csv`, `phone.csv`: contract information as of February 1, 2020. The files are a training dataset from the course and are not included in the repository. Place them next to the notebook to run it.

## Stack

python, pandas, numpy, scikit-learn, CatBoost, imbalanced-learn, LOFO importance, matplotlib, seaborn

## Notebook

[client_churn_prediction.ipynb](client_churn_prediction.ipynb)
