## Housing in Mexico City

This repository contains a Jupyter notebook with code for predicting apartment prices in Mexico City. The notebook contains the following sections:
1. Importing libraries
2. Data preparation
3. Data exploration
4. Feature engineering
5. Modeling and prediction

## Data
The data used for this project comes from five CSV files containing data on real estate in Mexico City. The data includes information about each property's location, size, price, and other features. The goal of this project is to build a model that can predict the price of an apartment in Mexico City based on these features.

## Code
The `Housing-in-Mexico-City.ipynb` notebook contains all the code used for this project. The code is organized into the following sections:

## Importing Libraries
This section imports the libraries that are used throughout the project, including `pandas`, `matplotlib`, `plotly`, `category_encoders`, `sklearn`.

## Data Preparation
This section includes a wrangle function that performs data cleaning on the raw real estate data. The function performs the following operations:

1. Subsets the data to include only apartments in Mexico City that cost less than $100,000.
2. Removes outliers by trimming the bottom and top 10% of properties in terms of `surface_covered_in_m2`.
3. Creates separate `lat` and `lon` columns.
4. Creates a `borough` feature from the `place_with_parent_names` column.
5. Drops columns that are more than 50% null values.
6. Drops columns containing low- or high-cardinality categorical values.
7. Drops any columns that would constitute leakage for the target `price_aprox_usd`.
8. Drops any columns that would create issues of multicollinearity.

The section also reads in the data from five CSV files, applies the `wrangle` function to each file, and concatenates the results into a single DataFrame.

## Data Exploration
This section includes code that explores the distribution of apartment prices and the relationship between apartment size and price. It includes a histogram of apartment prices and a scatter plot of price vs. area.

## Feature Engineering
This section includes code that performs feature engineering on the data. It includes one-hot encoding of categorical variables and imputation of missing values.

## Modeling and Prediction
This section includes code that trains and evaluates a linear regression model and a ridge regression model on the data. It also includes code that uses the models to predict the prices of new apartments.

## Conclusion
This project demonstrates how to use machine learning techniques to predict the price of apartments in Mexico City. By cleaning and preprocessing the data, performing feature engineering, and training and evaluating models, we can build a predictive model that can help people make more informed decisions about buying or renting apartments in Mexico City.