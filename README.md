# Black Friday Sales Analysis

Predicting customer purchase amounts from demographic and product attributes using multivariable linear regression in Python.

## Overview
Using a Black Friday retail transactions dataset, I built a regression model to find which customer and product factors drive purchase amount, and tested how well it predicts on unseen data.

## Approach
- Loaded and explored the data with pandas
- Encoded categorical variables (label encoding for Gender and Age, dummy variables for City Category)
- Tested eight predictors and removed Stay_In_Current_City_Years, as it was not statistically significant (p = 0.124)
- Final model uses seven predictors: gender, age, occupation, marital status, product category, and two city-category dummies
- Evaluated with an 80/20 train/test split (440,054 / 110,014 rows of 550,068 transactions) using MAE and RMSE

## Tools
Python, pandas, NumPy, statsmodels, scikit-learn, Matplotlib, Google Colab

## Data
Black Friday dataset from Kaggle (not included in this repo). To run the notebook, download `train.csv` from Kaggle and upload it to Colab.


## Key findings
- All seven predictors are statistically significant (p < 0.001), but together they explain only about 12.5% of the variation in purchase amount (R-squared = 0.125). Demographics alone are weak predictors of spend.
- City Category C customers spend about $686 more per transaction than City A, and City B about $162 more.
- Male customers spend about $514 more per transaction than female customers.
- Each step up in age band is associated with about $114 more per purchase. Marital status has a small negative effect (about -$55).

## Limitations
- Product_Category_1 was treated as a numeric variable, although it is really a category label. Its large coefficient (-438) mostly reflects how the categories happen to be numbered, so it shouldn't be read as a real effect. Encoding it as dummy variables would be a better next step.
- The low R-squared suggests important drivers of spend (such as the specific product or customer purchase history) are not captured by these variables.

