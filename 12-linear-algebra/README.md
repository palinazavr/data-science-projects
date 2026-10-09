# 12. Linear Algebra: Protecting Customers' Personal Data

## Goal

Protect the personal data of the clients of an insurance company by encrypting the features so that the original values cannot be recovered easily, while the quality of linear regression does not change.

## Tasks

1. Load and inspect the data (5000 clients: gender, age, salary, number of family members, number of insurance payments).
2. Prove that multiplying the features by an invertible matrix does not change the quality of linear regression (the weights become `P^-1 w`).
3. Implement the encryption with a random invertible matrix.
4. Check that the R2 metric is the same before and after the transformation.

## Results

- Linear regression on the original and on the encrypted data gives the same R2 (**0.425**).
- The data can be recovered only with the key (the inverse matrix).

## Data

`insurance.csv` with gender, age, salary, number of family members and the number of insurance benefits received. The column names in the file are in Russian; the notebook renames them to English. The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it.

## Stack

python, pandas, numpy (matrix operations), scikit-learn

## Notebook

[linear_algebra.ipynb](linear_algebra.ipynb)
