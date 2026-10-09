# 03. Statistical Data Analysis: Choosing a Telecom Plan

## Goal

Compare two prepaid plans ("Smart" and "Ultra") of a mobile operator on a sample of 500 customers, describe the behavior of the users and decide which plan is more promising for the operator.

## Tasks

1. Load five tables (users, calls, messages, internet sessions, plans), fix the data types and drop broken columns.
2. Calculate monthly calls, minutes, messages, traffic and revenue for each user and remove outliers.
3. For each plan calculate the mean, variance and standard deviation of the usage, and the share of users who exceed their included allowance.
4. Test two hypotheses about the average revenue: Ultra vs Smart, and Moscow vs other regions (Student's t-test, then Levene's and Mann-Whitney tests).

## Results

- Smart users exceed their allowance often: 29.4% in minutes, 26.0% in messages and 60.6% in traffic. Ultra users hardly exceed it (only 10.2% in traffic).
- The share of overage payments in the revenue from a Smart user grows from about 10% to about 50% during the year; for Ultra it stays around 5%.
- The average revenue of Ultra and Smart users is significantly different (p-value about 0).
- The average revenue in Moscow and in other regions does not differ (p-value 0.47; Mann-Whitney confirms it).
- Ultra is recommended for promotion, with a possible smaller package of minutes and messages for a lower fee.

## Data

`users.csv`, `calls.csv`, `messages.csv`, `internet.csv`, `tariffs.csv`: usage records of 500 customers for one year. The files are a training dataset from the course and are not included in the repository. Place them next to the notebook to run it. The city names in `users.csv` are in Russian, as in the dataset.

## Stack

python, pandas, numpy, scipy (hypothesis tests), matplotlib, seaborn, plotly

## Notebook

[statistical_data_analysis.ipynb](statistical_data_analysis.ipynb)
