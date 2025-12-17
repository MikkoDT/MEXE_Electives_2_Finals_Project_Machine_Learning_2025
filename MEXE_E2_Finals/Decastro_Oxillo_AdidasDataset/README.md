 # Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: 
- Members:De Castro Rod & Oxillo Ivan Russ
- Topic: Adidas Sales Dataset
- Chosen Model: Logistic Regression

- ## 2. Dataset Overview
- Dataset Source: https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset
- Description: This dataset provides a detailed breakdown of Adidas' sales performance across the United States from 2020 to 2021. The data, which you plan to analyze using a Linear Regression model, covers transactions, including retailers, geographical regions, product categories, units sold, total sales, and profit margins. It is an excellent resource for practicing data preprocessing, predictive modeling, and business forecasting.
  
Target Varible: 

- Total Sales

Features Used: 

- Retailer

- Region

- State

- City

- Product

- Price per Unit

- Units Sold

- Operating Profit

- Operating Margin

- Sales Method'

- ## 3. Preprocessing Summary
- Encoding: The categorical features were converted into a numerical format using One-Hot Encoding. This technique is used to ensure compatibility with the Linear Regression model, allowing it to process non-numerical data without assigning misleading numerical relationships between categories.
- Scaling: The numerical features were subjected to Standard Scaling. This step standardizes the values by ensuring all numerical data is on a similar scale. Scaling is vital to prevent features with large ranges (like Units Sold) from disproportionately influencing the model's convergence and training process.
- Cleaning steps: he dataset was prepared by performing a check for missing values (NaN). The notebook confirmed that the data was complete, meaning no imputation or filling of missing entries was necessary before training the model.
- Train–test split: The data was partitioned into a training set and a testing set (80% training / 20% testing). This split is a crucial step used to evaluate the model's performance on unseen data. By testing on a separate dataset, we ensure the model is not overfit to the training data and can generalize effectively to new information.

## 4. Model And Result

### Model Used: ***Linear Regression**

Linear Regression is chosen because the goal is to predict a continuous numeric value, Total Sales.

This model is a strong fit because Total Sales is mathematically derived from key features like Price per Unit and Units Sold, suggesting a highly linear relationship between the independent variables and the target variable. Furthermore, the simplicity, speed, and interpretability of Linear Regression are ideal for understanding how factors like retailer, region, product type, and sales method influence overall revenue.


### Metrics:

Mean Absolute Error (MAE): **560.84**

Mean Squared Error (MSE): **444,738.93**

Coefficient of Determination (R²): **0.9999719**

Adjusted R²: **0.9999713**

### Viasualization:

Actual vs. Predicted Sales Plot: This plot shows how the model's predicted sales figures relate to the true recorded sales . The close alignment of all data points to the ideal diagonal line visually confirms the model's exceptional fit and high predictive accuracy.

<img width="749" height="570" alt="image" src="https://github.com/user-attachments/assets/b527805f-66e8-49a0-ac53-2d175ba48564" />

Residual Plot: This plot displays the differences between actual and predicted sales (the errors, or residuals) . The random, uniform scattering of these errors around the zero line validates a key assumption of Linear Regression: that the model's mistakes are random and unbiased.

<img width="719" height="639" alt="image" src="https://github.com/user-attachments/assets/cb4c5806-ed9b-4d05-80d5-dd51dcc0db1a" />



Mean Absolute Error (MAE): **560.84**

Mean Squared Error (MSE): **444,738.93**

Coefficient of Determination (R²): **0.9999719**

Adjusted R²: **0.9999713**
