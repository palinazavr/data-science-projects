# 07. Machine Learning in Business: Choosing an Oil Well Location

## Goal

An oil mining company has oil samples from three regions (10,000 wells in each). Build a regression model that predicts the volume of reserves in a well, then choose the region with the highest expected profit and estimate the risk of losses.

## Tasks

1. Load and inspect the data.
2. Train and validate a linear regression model for each region.
3. Calculate the minimum volume of reserves per well required for break-even development.
4. Estimate profit, its 95% confidence interval and the risk of losses with the bootstrap technique (1000 samples, the 200 best wells out of 500).

## Results

- Region 1 is recommended: average profit 452.05 million RUB, risk of losses 1.5%.
- Regions 0 and 2 do not pass the risk threshold of 2.5% (6.0% and 8.0%).
- The model is the most accurate for region 1 (RMSE 0.89, against 37.76 and 40.15 for regions 0 and 2).

## Data

`geo_data_0.csv`, `geo_data_1.csv`, `geo_data_2.csv` with the columns `id`, `f0`, `f1`, `f2` and `product` (reserves in thousand barrels). The files are a training dataset from the course and are not included in the repository. Place them next to the notebook to run it.

## Stack

python, pandas, numpy, scikit-learn, scipy, matplotlib, seaborn

## Notebook

[ml_in_business.ipynb](ml_in_business.ipynb)
