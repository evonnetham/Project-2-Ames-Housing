# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Ames Housing Price Watch

## Problem Statement

![image](https://www.realtyprima.com/chandigarh/images/banner.jpg)

As investing in a property involves a large sum of money, and it would be advisable to do a substantial amount of research with the correct data. Whether you are a buyer, a seller or a property investor, everyone wants to buy low and sell high. There are tons of property calculator out there where most can use. However what actually determines the price of a property, what property features are most important in accurately predicting sale prices of the properties in Ames, IA. Accuracy of prediction could increase enormously after having to identify these factors. However, how to you mesure this accuracy?

---
## Executive Summary
In order to better understand what are the factors influencing sale prices of the property in Ames, Iowa, we will be looking at the dataset that contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010. 

This data requires cleaning of the null values by filling up with zero or the mean and the removal of corrupted rows. As the data consist of continuous, oridinal, nominal and discrete data, several methods were use to standize and help retain important details. Features engineering was done to look at what features affect the sale price. After which, we will be looking at the accuracy of the prediction by using models such as Linear Regression, Ridge and Lasso where Lasso seemed to outperform the rest. 

---
## Content
- [1. Data Cleaning and EDA](./codes/01_EDA_and_Cleaning.ipynb)
- [2. Full Exploratory Data Analysis](./codes/02_Preprocessing_and_Feature_Engineering.ipynb)
- [3. Data Visualisation and Inference](./codes/03_Modeling _and_Kaggle_Submission.ipynb)

---
## Data Dictionary

The data for this project is taken from [here](https://www.kaggle.com/c/dsi-us-6-project-2-regression-challenge/data), which contains the dataset of housing prices in Ames, Iowa from 2006 to 2010. As such, the data dictionary provides a thorough breakdown of the variables involved.

---
## Conclusions and Recommendations

In order to have a model that predict the price of house accurate first we will need to clean up our data with the help of Exploratory Data Analysis, where we will be looking at data for completeness through imputation of the null values, convertion of discrete, continous, ordinal and nominal values in variables, identifying which are the outlier. 

Feature Exploration 
- seaborn Heatmap, we will be able to identify which features are of the highest correlation with saleprice.
- pairplot allow us to take a close look at the correlation and the distribution 
- boxplot help to identify which are the outlier.

Which features appear to add the most value to a home?
Feature Correlation with Sale price with a significant positive correlation of more than 0.6 
1.total square feet (0.84)
2.Overall quality (0.81)
3.External quality (0.72)
4.Ground Living Area (0.72)
5.kitchen quality(0.69)
6.Total basement square feet (0.67)
7.garage area (0.65)

Which features hurt the value of a home the most?
Feature Correlation with Sale price with a significant negative correlation of less than than -0.6
1.Housing age (-0.58)

What modeling approaches yield the most accurate prediction
1. Dummy variables: Replace catergorical variables
2. Ordinal Values: Assigning values to those scaled variables with the use of mapping. 
3. Train test split
4. Comparison between linear regression, lasso and ridge


Which model has the best prediction?
Lasso has the highest accurate prediction whcih are R^2 score of 89% on the test Prediction.

What are things that homeowners could improve in their homes to increase the value?
1. as age of the house can hurt the value of a home hence, remodelling might come in handy if homeowners are planning to increase the value. 


Other Recommendation
Rather than only looking at the features of a property, there are other factors that might affect the sale price. This to consider to further investigate that may help to predict the price of property even more accurately. For instance, a recession or a pandemic might cause a drop in the sale price due to supply and demand. 











