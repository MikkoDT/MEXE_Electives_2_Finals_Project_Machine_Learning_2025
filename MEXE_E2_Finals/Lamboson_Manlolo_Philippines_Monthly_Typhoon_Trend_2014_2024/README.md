# Final Assessment — Machine Learning Model

## 1. Group Information
- Members:

     **Lamboson, Jaycel L.**
 
     **Manlolo, Noel Alexis C.**

- Topic: **Phillippines Monthly Typhoon Trend (2014-2024)**

- Chosen Model: **Linear Regression**

## 2. Dataset Overview
Dataset Source: https://www.kaggle.com/datasets/denvermagtibay/philippines-monthly-typhoon-trend-2014-2024

<p align="justify">
Description: This dataset contains monthly climate and typhoon-related variables in the Philippines from 2014 to 2024. It was used in our machine learning analysis, where Vertical Wind Shear was treated as the dependent variable, and Month, Number of Typhoons, Oceanic Niño Index (ONI), Niño 3.4 Sea Surface Temperature (SST) Anomaly, Western Pacific SST, Midlevel Humidity, Sea Level Pressure, MJO Phase, and Previous Month Typhoon Count were used as independent variables. The dataset was used to develop a linear regression model for predicting and analyzing the behavior of vertical wind shear.
</p>

Target Varible: 

- Vertical Wind Shear

Features Used: 

- Month

- Number_of_Typhoons

- ONI

- Nino3.4_SST_anomaly

- Western_Pacific_SST

- Midlevel_Humidity

- SeaLevelPressure

- MJO_Phase

- Prev_month_typhoons

## 3. Preprocessing Summary

Encoding: All categorical columns (if any) were filled with the most frequent value and converted to numeric if needed. All features used in the model were numeric, so no additional encoding was applied.

Scaling: All features were standardized using StandardScaler to have zero mean and unit variance before training the linear regression model.

Cleaning Steps:

- Removed duplicate rows.

- Stripped spaces and invisible characters from column names.

- Filled missing values with the mean for numeric columns and mode for categorical columns.

- Dropped irrelevant columns such as unnamed or ID columns.
  
Train–test split:

The dataset was split into training and testing sets, with X_train and y_train used to train the model, and X_test and y_test used to evaluate its performance.
