# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Ames Housing Price Watch

![image](./images/housing.png)

## Problem Statement
As investing in a property involves a large sum of money, and it would be advisable to do a substantial amount of research with the correct data. Whether you are a buyer, a seller or a property investor, everyone wants to buy low and sell high. There are tons of property calculator out there where most can use. However what actually determines the price of a property, what property features are most important in accurately predicting sale prices of the properties in Ames, IA. Accuracy of prediction could increase enormously after having to identify these factors. However, how to you mesure this accuracy?


## Executive Summary
In order to better understand what are the factors influencing sale prices of the property in Ames, Iowa, we will be looking at the dataset that contains information from the Ames Assessor’s Office used in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010. 

This data requires cleaning of the null values by filling up with zero or the mean and the removal of corrupted rows. As the data consist of continuous, oridinal, nominal and discrete data, several methods were use to standize and help retain important details. Features engineering was done to look at what features affect the sale price. After which, we will be looking at the accuracy of the prediction by using models such as Linear Regression, Ridge and Lasso where Lasso seemed to outperform the rest. 


## Content
1. [Data Cleaning and EDA](./codes/01_Data_Cleaning.ipynb)
2. [Exploratory Data Analysis](./codes/02_Exploratory_Data_Analysis.ipynb)
3. [Preprocessing and Feature Engineering](./codes/03_Preprocessing_and_Feature_Engineering.ipynb)
4. [Modeling and Kaggle Submission](./codes/04_Modeling_and_Kaggle_Submission.ipynb)


## Data Dictionary

The data for this project is taken from [here](https://www.kaggle.com/c/dsi-us-6-project-2-regression-challenge/data), which contains the dataset of housing prices in Ames, Iowa from 2006 to 2010. As such, the data dictionary provides a thorough breakdown of the variables involved.

Here are some of the features:


|Feature|Type|Dataset|Description|
|---|---|---|---|
| id | int | train | Property number |
| pid | int | train | Row number |
| ms_subclass | int | train | The building class |
| ms_zoning | string | train | Identifies the general zoning classification of the sale. |
| lot_frontage | float | train | Linear feet of street connected to property |
| lot_area | int | train | Lot size in square feet |
| street | string | train | Type of road access to property |
| alley | string | train | Type of alley access to property |
| lot_shape | string | train | General shape of property |
| land_contour | string | train | Flatness of the property |
| utilities | string | train | Type of utilities available |
| lot_config | string | train | Lot configuration |
| land_slope | string | train | Slope of property |
| neighborhood | string | train | Physical locations within Ames city limits |
| condition_1 | string | train | Proximity to main road or railroad |
| condition_2 | string | train | Proximity to main road or railroad (if a second is present) |
| bldg_type | string | train | Type of dwelling |
| house_style | string | train | Style of dwelling |
| overall_qual | int | train | Overall material and finish quality |
| overall_cond | int | train | Overall condition rating |
| year_built | int | train | Original construction date |
| year_remod/add | int | train | Remodel date (same as construction date if no remodeling or additions) |
| roof_style | string | train | Type of roof |
| roof_matl | string | train | Roof material |
| exterior_1st | string | train | Exterior covering on house |
| exterior_2nd | string | train | Exterior covering on house (if more than one material) |
| mas_vnr_type | string | train | Masonry veneer type |
| mas_vnr_area | float | train | Masonry veneer area in square feet |
| exter_qual | string | train | Exterior material quality |
| exter_cond | string | train | Present condition of the material on the exterior |
| foundation | string | train | Type of foundation |
| bsmt_qual | string | train | Height of the basement |
| bsmt_cond | string | train | General condition of the basement |
| bsmt_exposure | string | train | Walkout or garden level basement walls |
| bsmtfin_type_1 | string | train | Quality of basement finished area |
| bsmtfin_sf_1 | float | train | Type 1 finished square feet |
| bsmtfin_type_2 | string | train | Quality of second finished area (if present) |
| bsmtfin_sf_2 | float | train | Type 2 finished square feet |
| bsmt_unf_sf | float | train | Unfinished square feet of basement area |
| total_bsmt_sf | float | train | Total square feet of basement area |
| heating | string | train | Type of heating |
| heating_qc | string | train | Heating quality and condition |
| central_air | string | train | Central air conditioning |
| electrical | string | train | Electrical system |
| 1st_flr_sf | int | train | First Floor square feet |
| 2nd_flr_sf | int | train | Second floor square feet |
| low_qual_fin_sf | int | train | Low quality finished square feet (all floors) |
| gr_liv_area | int | train | Above grade (ground) living area square feet |
| bsmt_full_bath | float | train | Basement full bathrooms |
| bsmt_half_bath | float | train | Basement half bathrooms |
| full_bath | int | train | Full bathrooms above grade |
| half_bath | int | train | Half baths above grade |
| bedroom_abvgr | int | train | Number of bedrooms above basement level |
| kitchen_abvgr | int | train | Number of kitchens |
| kitchen_qual | string | train | Kitchen quality |
| totrms_abvgrd | int | train | Total rooms above grade (does not include bathrooms) |
| functional | string | train | Home functionality rating |
| fireplaces | int | train | Number of fireplaces |
| fireplace_qu | string | train | Fireplace quality |
| garage_type | string | train | Garage location |
| garage_yr_blt | float | train | Year garage was built |
| garage_finish | string | train | Interior finish of the garage |
| garage_cars | float | train | Size of garage in car capacity |
| garage_area | float | train | Size of garage in square feet |
| garage_qual | string | train | Garage quality |
| garage_cond | string | train | Garage condition |
| paved_drive | string | train | Paved driveway |
| wood_deck_sf | int | train | Wood deck area in square feet |
| open_porch_sf | int | train | Open porch area in square feet |
| enclosed_porch | int | train | Enclosed porch area in square feet |
| 3ssn_porch | int | train | Three season porch area in square feet |
| screen_porch | int | train | Screen porch area in square feet |
| pool_area | int | train | Pool area in square feet |
| pool_qc | string | train | Pool quality |
| fence | string | train | Fence quality |
| misc_feature | string | train | Miscellaneous feature not covered in other categories |
| misc_val | int | train | $Value of miscellaneous feature |
| mo_sold | int | train | Month Sold |
| yr_sold | int | train | Year Sold |
| sale_type | string | train | Type of sale |
| saleprice | int | train | Price property was sold for |


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
