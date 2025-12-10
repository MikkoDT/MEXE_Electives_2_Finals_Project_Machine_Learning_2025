Final Assessment — Machine Learning Model
1. Group Information
Members:

Hernandez, Jhonas R. 
Ogayon, Neil John

Topic: Engineering Graduate Salary 

Chosen Model: Logistics Regression

2. Dataset Overview
Dataset Source: [https://docs.google.com/spreadsheets/d/1eUE6iiKm10bQzOcxsAPgzdmn3Gol80OASiSlJO1egME/edit?gid=814979604#gid=814979604]

Description: This dataset contains monthly climate and typhoon-related variables in the Philippines from 2014 to 2024. It was used in our machine learning analysis, where Vertical Wind Shear was treated as the dependent variable, and Month, Number of Typhoons, Oceanic Niño Index (ONI), Niño 3.4 Sea Surface Temperature (SST) Anomaly, Western Pacific SST, Midlevel Humidity, Sea Level Pressure, MJO Phase, and Previous Month Typhoon Count were used as independent variables. The dataset was used to develop a linear regression model for predicting and analyzing the behavior of vertical wind shear.

Target Varible:


Features Used:



3. Preprocessing Summary
Encoding: All categorical columns (if any) were filled with the most frequent value and converted to numeric if needed. All features used in the model were numeric, so no additional encoding was applied.

Scaling: All features were standardized using StandardScaler to have zero mean and unit variance before training the linear regression model.

Cleaning Steps:

Removed duplicate rows.

Stripped spaces and invisible characters from column names.

Filled missing values with the mean for numeric columns and mode for categorical columns.

Dropped irrelevant columns such as unnamed or ID columns.

Train–test split: The dataset was split into training and testing sets, with X_train and y_train used to train the model, and X_test and y_test used to evaluate its performance.

4. Model And Result
Model Used:
Metrics:
Visualization:
Insights:
