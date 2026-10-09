# 02. Exploratory Data Analysis: Apartment Sale Listings

## Goal

Determine which parameters influence the market value of real estate, using the sale listings of Saint Petersburg and nearby localities. The results are the basis for an automated system that detects anomalies and fraudulent listings.

## Tasks

1. Explore the data and handle missing values, anomalies and data types.
2. Add new parameters: price per square meter, publication weekday, month and year, floor category and others.
3. Study the distributions of area, price, number of rooms and ceiling height, and the time it takes to sell an apartment.
4. Find the factors that affect the price and compare the median price per square meter in the 10 localities with the most listings.
5. Find the boundary of the central district of Saint Petersburg and compare it with the rest of the city.

## Results

- The data has 5-65% missing values in different columns. They were restored from other parameters where possible and left as they are otherwise.
- Most apartments are sold in 45-232 days; sales faster than 4 days or longer than 512 days are outliers.
- The price depends mostly on the total area, the number of rooms and the distance to the city center. Prices fell in 2014-2015, most clearly in the central district.
- The most expensive locality is Saint Petersburg (about 114,700 per square meter), the cheapest is Vyborg (about 58,200).
- The central district of Saint Petersburg ends about 3 km from the center.

## Data

`real_estate_data.csv`: listings with the columns `last_price`, `total_area`, `rooms`, `ceiling_height`, `floor`, `floors_total`, `cityCenters_nearest`, `locality_name` and others. The file is a training dataset from the course and is not included in the repository. Place it next to the notebook to run it.

## Stack

python, pandas, matplotlib

## Notebook

[exploratory_data_analysis.ipynb](exploratory_data_analysis.ipynb)
