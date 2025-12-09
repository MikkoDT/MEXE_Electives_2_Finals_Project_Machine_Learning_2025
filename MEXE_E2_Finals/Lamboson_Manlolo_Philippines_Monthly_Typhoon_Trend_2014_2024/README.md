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

Encoding: All categorical columns (if any) were filled with the most frequent value and converted to numeric where necessary. Since all features used in the model were numeric, no additional encoding was required.

Scaling: No explicit feature scaling was applied. All numeric features were used as-is in the linear regression model.

Cleaning Steps:
- Removed duplicate rows.
