# 05. Introduction to Machine Learning: Recommending a Mobile Plan

## Goal

Build a classification model that picks a suitable new plan ("Smart" or "Ultra") for the subscribers of a mobile operator, using the monthly behavior of users who already moved to the new plans. The accuracy on the test set must be at least 0.75.

## Tasks

1. Load and inspect the data (3,214 users: calls, minutes, messages, traffic).
2. Split the data into training, validation and test sets (3:1:1).
3. Tune a decision tree, a random forest, logistic regression, k-nearest neighbors and a support vector machine on the validation set.
4. Evaluate the best model on the test set and run a sanity check.

## Results

- The best model is a random forest: accuracy 0.81 on both the validation and the test set, above the 0.75 requirement.
- Its accuracy stops growing at about 7 trees and a depth of 6 (accuracy 0.82), so larger forests are not needed.
- About 6.5% of the values are outliers; they were kept.

## Data

`users_behavior.csv`: for each user the number of calls, minutes, messages, internet traffic (MB) and the target `is_ultra` (plan). The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it.

## Stack

python, pandas, numpy, scikit-learn, matplotlib, seaborn

## Notebook

[intro_to_machine_learning.ipynb](intro_to_machine_learning.ipynb)
