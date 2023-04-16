# Housing in Brazil

This repository contains a Jupyter notebook that uses Python to explore and analyze a dataset of homes for sale in Brazil. The goal of the analysis is to determine if there are regional differences in the real estate market, and to look at southern Brazil to see if there is a relationship between home size and price.
Libraries Used

* pandas
* matplotlib
* plotly

## Dataset

The dataset used in this analysis consists of two CSV files:

* `data/brasil-real-estate-1.csv`
* `data/brasil-real-estate-2.csv`

## Cleaning the Data

Before beginning the analysis, the following steps were taken to clean the data:

1. Import the CSV file `data/brasil-real-estate-1.csv` into the DataFrame `df1`.
2. Drop all rows with NaN values from the DataFrame df1.
3. Use the `"lat-lon"` column to create two separate columns in df1: `"lat"` and `"lon"`. Make sure that the data type for these new columns is float.
4. Use the `"place_with_parent_names"` column to create a `"state"` column for `df1`.
5. Transform the `"price_usd"` column of df1 so that all values are floating-point numbers instead of strings.
6. Drop the `"lat-lon"` and `"place_with_parent_names"` columns from `df1`.
7. Import the CSV file `brasil-real-estate-2.csv` into the DataFrame `df2`.
8. Use the `"price_brl"` column to create a new column named `"price_usd"`.
9. Drop the `"price_brl"` column from `df2`, as well as any rows that have `NaN` values.
10. Concatenate `df1` and `df2` to create a new DataFrame named `df`.

## Exploring the Data

The analysis begins by creating a `scatter_mapbox` showing the location of the properties in `df`. This helps to visualize the regional differences in the Brazilian real estate market.

Then, a histogram is created to show the distribution of property prices in each state.

Finally, the relationship between home size and price is explored by creating a scatter plot of `price_usd` against `surface_total_in_m2` for the southern states of Brazil.

Please see the Jupyter notebook for the full code and visualizations.