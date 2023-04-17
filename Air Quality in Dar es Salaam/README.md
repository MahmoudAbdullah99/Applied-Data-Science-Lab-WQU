# Air Quality in Dar es Salaam 🇹🇿

The goal of this project is to explore and analyze air quality data in Dar es Salaam, Tanzania. Specifically, we want to determine the site with the most sensor readings, extract PM2.5 readings from this site, and perform some time-series analysis on the PM2.5 data.

## Data
The data comes from the air quality collection in a MongoDB database. We first connect to the database, and then query the Dar es Salaam collection to get the data we need. The data includes timestamped measurements from various sensor sites around the city. The metadata for each measurement includes the site ID, measurement type, and sensor ID, among other information.


## Analysis
We begin by exploring the data to determine the site with the most sensor readings. We do this by querying the collection for distinct site IDs and counting the number of documents for each site. We then use this information to extract PM2.5 readings from the site with the most sensor readings, and clean and prepare the data for analysis.

Next, we perform some time-series analysis on the PM2.5 data. We create a time series plot of the data, and a rolling average plot with a window size of one week. We also create an autocorrelation function plot to determine the correlation between the PM2.5 readings and their lags.


## Results
Our analysis reveals some interesting patterns in the PM2.5 data. The time series plot shows that the PM2.5 levels in Dar es Salaam have been fairly stable over the past several years, with occasional spikes in pollution. The rolling average plot shows a slight upward trend in PM2.5 levels over the past few years, but the trend is not significant. The ACF plot shows a moderate correlation between PM2.5 levels and their lags, indicating that there is some seasonality in the data. Overall, our analysis suggests that air quality in Dar es Salaam is relatively stable, but there is still room for improvement in reducing pollution levels.