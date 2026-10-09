# 10. Time Series: Taxi Order Forecast

## Goal

Predict the number of taxi orders for the next hour to help a taxi company attract more drivers during rush hours. The RMSE on the test set must not exceed 48.

## Tasks

1. Load the data and resample it to hourly values.
2. Decompose the series into trend, seasonality and residuals.
3. Create features (day of the week, lags, rolling mean) and train linear models with different hyperparameters; the test set is the last 20% of the series (no shuffling).
4. Check the models on the test set.

## Results

- All linear models give a similar RMSE; the best features are a rolling window of 40-50 hours and lags up to 100 hours.
- The Lasso model reaches an RMSE of 35.7 on the test set, 33% lower than the baseline (53.4), and satisfies the requirement (below 48).
- The model catches the daily pattern accurately but cannot predict rare spikes.

## Data

`taxi.csv`: the number of taxi orders over time (`datetime`, `num_orders`), aggregated to hourly values in the notebook. The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it.

## Stack

python, pandas, numpy, scikit-learn, statsmodels, matplotlib, seaborn

## Notebook

[time_series.ipynb](time_series.ipynb)
