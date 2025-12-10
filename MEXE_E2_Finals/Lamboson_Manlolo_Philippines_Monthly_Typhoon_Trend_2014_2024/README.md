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
Description: This dataset contains monthly climate and typhoon-related variables in the Philippines from 2014 to 2024. It was used in our machine learning analysis, where Vertical Wind Shear was treated as the dependent variable, and Month, Niño 3.4 Sea Surface Temperature (SST) Anomaly, Western Pacific SST, Midlevel Humidity, Sea Level Pressure, and MJO Phase were used as independent variables. The dataset was used to develop a linear regression model for predicting and analyzing the behavior of vertical wind shear.
</p>

Target Varible: 

- Vertical Wind Shear

Features Used: 

- Month

- Nino3.4_SST_anomaly

- Western_Pacific_SST

- Midlevel_Humidity

- SeaLevelPressure

- MJO_Phase

## 3. Preprocessing Summary

Encoding: All categorical columns (if any) were filled with the most frequent value and converted to numeric if needed. All features used in the model were numeric, so no additional encoding was applied.

Scaling: All features were standardized using StandardScaler to have zero mean and unit variance before training the linear regression model.

Cleaning Steps:

- Removed duplicate rows.

- Stripped spaces and invisible characters from column names.

- Filled missing values with the mean for numeric columns and mode for categorical columns.

- Dropped irrelevant columns such as unnamed or ID columns.
  
Train–test split: The dataset was split into training and testing sets, with X_train and y_train used to train the model, and X_test and y_test used to evaluate its performance.

## 4. Model And Result

### Model Used: ***Linear Regression**

Linear Regression is chosen because the goal is to predict a continuous numeric value (Vertical Wind Shear). The dataset shows linear relationships between wind shear and key climate variables like sea‑level pressure and humidity, making linear regression a good fit. It is also simple, fast, and easy to interpret, which is ideal for smaller datasets and research where understanding which factors influence wind shear is important.

### Metrics:

Mean Absolute Error (MAE): **0.4933110943244657**

Mean Squared Error (MSE): **0.43336684690612526**

Coefficient of Determination (R²): **0.896277428576965**

Adjusted R²: **0.8651606571500545**

### Visualization:

**Scatter Plot**

These scatter plots show how each climate variable relates to Vertical Wind Shear. They help visualize whether the relationship is positive, negative, or weak. Patterns in the plots make it easier to see which variables influence wind shear the most.

<p align="center">
<img src="https://github.com/user-attachments/assets/23900f14-07c0-4819-9b49-f3de8d66afb1" width="800">

**Heat Map**

The heatmap displays the strength and direction of the relationships between the independent variables and Vertical Wind Shear. Higher positive values indicate stronger increasing relationships, while negative values show decreasing relationships. This visualization makes it easy to identify which features are the strongest predictors.

<p align="center">
<img src="https://github.com/user-attachments/assets/ef50089d-385b-43c3-a310-4256ac45cd3e" width="800">

### Insights:

1. **Model Performance**

The model shows acceptable performance based on the R² and Adjusted R² values. This indicates that the selected climate variables explain a meaningful portion of the variation in Vertical Wind Shear. While not perfect, the model captures the main patterns in the data.

2. **Error Analysis**

The MAE, MSE, and RMSE values show that the average difference between predicted and actual wind shear values is reasonably small. This means the model can produce predictions that stay close to the real observations, with no major errors across the test data.

3. **Trends Observed**

The scatter plots and heatmap reveal strong relationships between Vertical Wind Shear and several climate factors, especially Sea‑Level Pressure and Midlevel Humidity. Predicted values follow stable patterns, suggesting no extreme jumps or drops in wind shear for the evaluated months. Seasonal effects (Month) also contribute moderately to the observed patterns.
