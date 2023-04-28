# Earthquake Damage in Kavrepalanchok
## Overview

This project aims to build a machine learning classification model to predict building damage in the district of Kavrepalanchok, Nepal, following the 2015 earthquake. We will be using data from the Open Data for Resilience Initiative (OpenDRI) that includes information about building structures, damage grade, and more.
Dataset

We will be using the Nepal Earthquake Data that contains the following tables:

* building_ownership: Contains ownership details of each building in the dataset.
* building_structure: Contains building structure details such as age, height, foundation type, and roof type.
* building_damage: Contains building damage details such as damage grade, repair cost, and post-earthquake inspection details.
* id_map: Contains the mapping between building IDs and geographical locations.

## Methodology

We will start by connecting to the nepal.sqlite database, wrangle and preprocess the data, and then build a classification model to predict the severity of building damage in Kavrepalanchok. To evaluate the performance of our model, we will use the accuracy metric.
Tools and Libraries

* Python 3
* pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SQLite

## Results
After preprocessing the data, we split the dataset into training and test sets using a 75/25 ratio. We experimented with two different encoding techniques: ordinal encoding and one-hot encoding. We trained and evaluated our models using decision tree and logistic regression algorithms. Here are the accuracy results:

| Model                | Encoding | Training Accuracy | Testing Accuracy |
|----------------------|----------|-------------------|------------------|
| Decision Tree        | Ordinal  | 70.2%             | 71.7%            |
| Logistic Regression	| One-Hot  | 65.1%             | 65.3%            |

Based on the results, we can conclude that the logistic regression model using one-hot encoding performed the best, with an accuracy of 0.727.

## Conclusion

In this project, we successfully built a machine learning model to predict building damage in Kavrepalanchok following the 2015 earthquake. We demonstrated the importance of preprocessing and feature engineering in the model-building process. Our best model achieved an accuracy of 72.7%, which can be improved upon with further tuning or using different algorithms.