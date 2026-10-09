# 09. Numerical Methods: Used Car Price Prediction

## Goal

Build a model that predicts the market value of a used car from its technical characteristics for the app of a car sales company. The company cares about the prediction quality, the prediction speed and the training time.

## Tasks

1. Clean the data (duplicates, anomalous prices, power and registration years, missing values) and encode the categorical features.
2. Train a linear regression and its regularized versions (Lasso, Ridge) and a LightGBM model with `GridSearchCV`.
3. Compare the models by RMSE, training time and prediction time.

## Results

- All models beat the constant baseline (RMSE 4530).
- On the test set, linear models give an RMSE of about 3023 and LightGBM about 1644, almost twice lower.
- Linear models are fast to train and to predict; LightGBM takes longer to predict (an order of magnitude) but is the clear winner on quality.

## Data

`autos.csv`: used car ads with the columns `Price` (target), `VehicleType`, `RegistrationYear`, `Gearbox`, `Power`, `Model`, `Kilometer`, `FuelType`, `Brand`, `NotRepaired` and others. The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it.

## Stack

python, pandas, numpy, scikit-learn, LightGBM, matplotlib, seaborn

## Notebook

[numerical_methods.ipynb](numerical_methods.ipynb)
