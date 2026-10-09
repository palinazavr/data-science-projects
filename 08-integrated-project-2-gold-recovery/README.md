# 08. Integrated Project 2: Predicting the Gold Recovery Rate

## Goal

Build a model that predicts the recovery rate of gold from ore after the flotation and the cleaning stages, to optimize the production and to avoid unprofitable parameters.

## Tasks

1. Check that the recovery rate in the data is calculated correctly and prepare the features available in the test set.
2. Analyze the concentrations of Au, Ag and Pb at each stage, compare the feed granule size in the training and the test sets and remove anomalous total concentrations.
3. Build a custom metric, the final sMAPE (25% flotation, 75% cleaning).
4. Train linear regression, ElasticNet and Lasso models for both stages with cross-validation, select features with permutation importance and check the result on the test set.

## Results

- The recovery rate calculated from the data matches the reported one.
- Objects with a total concentration below 31 were removed from the training set (733 objects, about 5%).
- The best model is Lasso: final sMAPE **8.70%** on the test set (8.15% for flotation, 8.88% for cleaning), against 9.66% for the constant model.

## Data

`gold_recovery_train_new.csv`, `gold_recovery_test_new.csv` and `gold_recovery_full_new.csv`: process parameters at every stage (named `stage.parameter_type.parameter_name`, for example `rougher.input.feed_ag`) and the two targets `rougher.output.recovery` and `final.output.recovery`. The files are a training dataset from the course and are not included in the repository. Place them next to the notebook to run it.

## Stack

python, pandas, numpy, scikit-learn, scipy, matplotlib, seaborn

## Notebook

[main_project2_supervised_ml.ipynb](main_project2_supervised_ml.ipynb)
