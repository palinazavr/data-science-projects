# 13. Computer Vision: Determining the Age of Customers from Photos

## Goal

Build a model that determines the age of a person from a photo for a supermarket chain, to analyze purchases by age group and to control the sale of alcohol. The mean absolute error (MAE) must not exceed 8 years.

## Tasks

1. Explore the dataset of 7,591 face photos with ages (`labels.csv`) and the distribution of the ages.
2. Train a ResNet50 network pretrained on ImageNet with a regression head (5 epochs, Adam, MSE loss).
3. Analyze the result against the business tasks.

## Results

- The final validation MAE is 6.23 years, below the 8-year requirement.
- The model is good enough to group customers by age for recommendations, but too imprecise (an error of more than 6 years) to control the sale of alcohol.
- The training MAE (3.4) is much lower than the validation MAE, a sign of overfitting.

## Data

`labels.csv` (`file_name`, `real_age`) and the folder `final_files/` with the photos. The dataset is a training dataset from the course and is not included in the repository. The training code was run on a GPU, so it is shown in the notebook as a text block together with its output. The photo grid from the exploratory analysis is also removed from the notebook to avoid publishing photos of people.

## Stack

python, TensorFlow/Keras (ResNet50, transfer learning), pandas, numpy, matplotlib, seaborn

## Notebook

[computer_vision.ipynb](computer_vision.ipynb)
