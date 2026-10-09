# 01. Data Preprocessing: Credit Reliability of Bank Customers

## Goal

Practice data preprocessing (missing values, data types, duplicates, lemmatization, categorization) and study how family status, number of children, income level and the purpose of a loan affect whether a customer repays a loan on time.

## Tasks

1. Inspect the data and fill in the missing values in `days_employed` and `total_income` (income is filled with the median of the customers with the same education level).
2. Convert data types and remove duplicates.
3. Lemmatize the loan purposes (Russian texts, `pymystem3`) and group them into 5 categories.
4. Categorize education, family status, income level and number of children into separate dictionaries.
5. Compare the share of customers with a debt across the groups with pivot tables.

## Results

- In every group the share of customers with a debt is below 10%, and the groups differ by at most 3.5 percentage points.
- Customers without children have the lowest share of debts (7.5%, against about 9.5% with one or two children).
- Customers with a high income (> 230k) have the lowest share of debts (7%).
- Loans for repairs and real estate are repaid more often (debt shares 5.7% and 7.3%) than loans for a car or education (9-9.5%).
- Some groups are small, so the conclusions for them are tentative.

## Data

A table with the solvency statistics of bank customers (`children`, `days_employed`, `dob_years`, `education`, `family_status`, `gender`, `income_type`, `debt`, `total_income`, `purpose`). The file is a training dataset from the course and is not included in the repository. The text values in the dataset (education, family status, loan purposes) are in Russian and are kept as they are in the data.

## Stack

python, pandas, pymystem3 (Russian lemmatization)

## Notebook

[data_preparation.ipynb](data_preparation.ipynb)
