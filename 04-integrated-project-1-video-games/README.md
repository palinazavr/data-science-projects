# 04. Integrated Project 1: Video Game Market Analysis

## Goal

Find the patterns that determine the commercial success of a video game, using historical data on sales, user and critic scores, genres and platforms. The results help to plan advertising campaigns.

## Tasks

1. Prepare the data: types, missing values, total sales across regions.
2. Choose the current period and the current platforms and compare their sales.
3. Study the influence of user and critic scores and of the genre on sales.
4. Build a user profile for North America, Europe and Japan (platforms, genres, ESRB ratings).
5. Test two hypotheses about average user scores (Xbox One vs PC, Action vs Sports).

## Results

- The current period is 2010-2016; the main platforms in 2016 are PS4, 3DS, XOne, WiiU and PC.
- The sales data is strongly right-skewed: most games sell up to about 1 million copies, a few sell tens of millions.
- Critic scores correlate weakly with sales (0.34-0.42); the correlation with user scores is weaker, except on WiiU.
- Shooter is the best selling genre by median sales (0.35 million copies); Puzzle, Adventure and Strategy sell the least.
- Europe and North America have similar tastes. Japan prefers its local platforms (the DS family), role-playing games and fighting games.
- The average user scores of Xbox One and PC are equal, the scores of Action and Sports are different.

## Data

`games.csv`: 16,715 games with the columns `Name`, `Platform`, `Year_of_Release`, `Genre`, regional sales, `Critic_Score`, `User_Score` and `Rating`. The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it.

## Stack

python, pandas, numpy, scipy (hypothesis tests), matplotlib, seaborn, plotly

## Notebook

[main_project1_data_preprocessing.ipynb](main_project1_data_preprocessing.ipynb)
