# Data Science Projects

A collection of 14 data science projects completed during a data science course (with a mentor). The projects cover the full path from data preprocessing and statistics to classical machine learning, time series, NLP and computer vision.

Each project has its own folder with a short README (goal, tasks, results, data, stack) and a Jupyter notebook with the code, commented in English.

## Projects

| # | Project | Task | Main methods and tools | Key result |
|---|---------|------|------------------------|------------|
| 01 | [Credit reliability of bank customers](01-data-preprocessing) | Data preprocessing | missing values, lemmatization (`pymystem3`), categorization, pivot tables | the share of debts differs by at most 3.5 pp between customer groups |
| 02 | [Apartment sale listings](02-exploratory-data-analysis) | Exploratory data analysis | cleaning, feature engineering, outliers, correlations | price depends mostly on area, rooms and distance to the center |
| 03 | [Telecom plans](03-statistical-data-analysis) | Statistical analysis | descriptive statistics, t-test, Mann-Whitney, Levene | "Ultra" is the more promising plan; revenue differs between plans, not between regions |
| 04 | [Video game market](04-integrated-project-1-video-games) | Integrated project: analysis | EDA, user profiles by region, hypothesis tests | main factors of game sales by platform, genre and region |
| 05 | [Recommending a mobile plan](05-intro-to-machine-learning) | Classification | decision tree, random forest, logistic regression, kNN, SVM | accuracy 0.81 (requirement 0.75) |
| 06 | [Bank customer churn](06-supervised-learning-churn) | Classification, imbalanced classes | class weights, upsampling, downsampling, F1, AUC-ROC | F1 0.63 (requirement 0.59), AUC-ROC 0.77 |
| 07 | [Choosing an oil well location](07-ml-in-business) | Regression and business risk | linear regression, bootstrap, confidence intervals | region 1: profit 452 million RUB, risk of losses 1.5% |
| 08 | [Gold recovery rate](08-integrated-project-2-gold-recovery) | Integrated project: regression | Lasso, ElasticNet, permutation importance, custom sMAPE | final sMAPE 8.70% (constant model 9.66%) |
| 09 | [Used car prices](09-numerical-methods) | Regression, speed vs quality | linear models, LightGBM, GridSearchCV | RMSE 1639 with LightGBM against 3005 for linear models |
| 10 | [Taxi orders forecast](10-time-series) | Time series | resampling, seasonality, lags, rolling mean, Lasso | RMSE 35.7 (baseline 53.4, requirement below 48) |
| 11 | [Toxic comments](11-ml-for-text) | Text classification | `nltk`, TF-IDF, logistic regression, NB-SVM | F1 0.788 (requirement 0.75) |
| 12 | [Protecting personal data](12-linear-algebra) | Linear algebra | matrix encryption, linear regression | R2 0.425 before and after encryption |
| 13 | [Age from photos](13-computer-vision) | Computer vision | ResNet50, transfer learning, Keras | MAE 6.2 years (requirement 8) |
| 14 | [Telecom customer churn](14-customer-churn-final) | Final project: classification | feature engineering, CatBoost, LOFO importance | ROC-AUC 0.894 |

## Skills and stack

- **Languages and data:** Python, pandas, numpy, table joins and aggregations
- **Statistics:** descriptive statistics, hypothesis testing (t-test, Mann-Whitney, Levene), bootstrap, confidence intervals
- **Machine learning:** scikit-learn, LightGBM, CatBoost, imbalanced-learn, cross-validation, hyperparameter search, feature selection (permutation importance, LOFO)
- **Time series, NLP, deep learning:** statsmodels, nltk, TF-IDF, TensorFlow/Keras
- **Visualization:** matplotlib, seaborn, plotly

## Repository structure

```
.
├── 01-data-preprocessing/        README.md + notebook
├── ...
├── 14-customer-churn-final/      README.md + notebook
├── requirements.txt
└── README.md
```

## Data

The datasets come from the course and are not redistributed here. Each project README lists the files it needs; place them next to the notebook to run it. Some datasets contain Russian text values (for example city names or loan purposes); they are kept as they are in the data.

## How to run

```bash
pip install -r requirements.txt
jupyter notebook
```
