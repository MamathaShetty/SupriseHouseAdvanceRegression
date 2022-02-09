# SupriseHouseAdvanceRegression

A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.

 

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

 

The company wants to know:

Which variables are significant in predicting the price of a house, and

How well those variables describe the price of a house.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
<!-- You can include any other section that is pertinent to your problem -->
## General Information
python jupyter notebook is used to write the code.
Multiple libraries used here are 
1. numpy
2. pandas
3. sns
4. matplotlib
5. seaborn
6. sklearn
7. statsmodel

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Conclusions
# Summary
1. First the housing data is read and analyzed dividing the features into numerical and categorical types.

2. SalePrice is the target column here.

3. All the features are then analyzed, missing data handling, outlier detection, data cleaning are done. Trend of SalePrice is observed for change in individual features.

4. New features are extracted, redundant features dropped and categorical features are encoded accordingly.

5. Then the data in split into train and test data and feature scaling is performed.

6. Target variable SalePrice is right skewed. Natural log of the same is Normal distributed, hence for model building, natural log of SalePrice is considered.

7. Creating dummy variables increased the number of features greatly, highly imbalanced columns are dropped.

8. Top 55 features are selected through RFE and adjusted R-square. 50 features : [''MSSubClass', 'LotFrontage', 'LotArea', 'LandSlope', 'OverallQual', 'OverallCond', 'YearBuilt', 'BsmtQual', 'BsmtExposure', 'BsmtFinSF1', 'HeatingQC', 'CentralAir', '1stFlrSF', '2ndFlrSF', 'BsmtFullBath', 'FullBath', 'HalfBath', 'KitchenQual', 'Functional', 'Fireplaces', 'FireplaceQu', 'GarageFinish', 'GarageArea', 'GarageQual', 'OpenPorchSF', 'MSZoning_RL', 'Street_Pave', 'LotConfig_CulDSac', 'Neighborhood_Edwards', 'Neighborhood_NAmes', 'Neighborhood_NWAmes', 'Neighborhood_NridgHt', 'Neighborhood_OldTown', 'Neighborhood_Somerst', 'Condition1_Norm', 'Condition2_Norm', 'RoofStyle_Gable', 'RoofStyle_Hip', 'RoofMatl_CompShg', 'Exterior1st_HdBoard', 'Exterior1st_Wd Sdng', 'Exterior2nd_HdBoard', 'Exterior2nd_Wd Sdng', 'MasVnrType_BrkFace', 'MasVnrType_None', 'MasVnrType_Stone', 'Foundation_PConc', 'Heating_GasA', 'GarageType_Attchd', 'GarageType_Detchd', 'GarageType_Not_applicable', 'PavedDrive_Y', 'SaleType_New', 'SaleCondition_Normal', 'SaleCondition_Partial']

9. Ridge and Lasso Regression Model are built with optimum alpha calculated in GridSearchCV method. Optimum alpha = 9.0 for ridge and 0.0001 for lasso model.

10. Model evaluation is done with R2 score and Root Mean Square Error.

11. Lasso Regression is chosen as final model for having slightly better R-square value on test data.

12. Out of 55 features in the final model, top 10 features in order of descending importance are ['1stFlrSF', '2ndFlrSF', 'OverallQual', 'OverallCond',
       'SaleCondition_Partial', 'SaleCondition_Normal', 'BsmtFinSF1',
       'LotArea', 'BsmtQual', 'GarageArea']

13. Model coefficients are listed in a table along with the corresponding features , for example natural log of SalePrice will change by 0.120217 with unit change in the feature '1stFlrSF' when all the features remain constant. Negative sign in the coefficient signifies negative correlation between the predictor and target variable.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->
## Technologies Used
- library - version 1.0
0 comments on commit df82fae
@MamathaShetty
 
 