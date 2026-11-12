# Black Friday Sales Analysis

Predicting customer purchase amounts from demographic and product attributes using multivariable linear regression in Python.

## Overview
Using a Black Friday retail transactions dataset, I built a regression model to find which customer and product factors drive purchase amount, and tested how well it predicts on unseen data.

## Approach
- Loaded and explored the data with pandas
- Encoded categorical variables (label encoding for Gender and Age, dummy variables for City Category)
- Tested eight predictors and removed Stay_In_Current_City_Years, as it was not statistically significant (p = 0.124)
- Final model uses seven predictors: gender, age, occupation, marital status, product category, and two city-category dummies
- Evaluated with an 80/20 train/test split using MAE and RMSE

## Tools
Python, pandas, NumPy, statsmodels, scikit-learn, Matplotlib, Google Colab

## Data
Black Friday dataset from Kaggle (not included in this repo). To run the notebook, download `train.csv` from Kaggle and upload it to Colab.

You still need to fill in two things:

Key findings. Copy your R-squared and the top predictors from your model summary. Don’t guess them. Your earlier report draft had made-up figures, so pull the numbers straight from the notebook output.
The split. I assumed 80/20. Check your train_test_split line (look for test_size=0.2) and correct it if it’s different.
