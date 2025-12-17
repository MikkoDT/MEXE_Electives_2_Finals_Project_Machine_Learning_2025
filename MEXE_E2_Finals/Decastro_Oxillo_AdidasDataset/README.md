 # Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: 
- Members:De Castro Rod & Oxillo Ivan Russ
- Topic: Adidas Sales Dataset
- Chosen Model: Logistic Regression

- ## 2. Dataset Overview
- Dataset Source: https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset
- Description: This dataset provides a detailed breakdown of Adidas' sales performance across the United States from 2020 to 2021, covering retailers, product categories, and profit margins to help analysts practice data visualization and business forecasting.
- **Target Variable:**  
Binary label indicating meal healthiness:
- `1` → High Profit (Operating Margin above 35%)  
- `0` → Low Profit (Operating Margin below 35%)
Classification is based on predefined nutritional thresholds.

- Features Used: The features used in the model include: Units Sold, Price per Unit, Total Sales, and Operating Profit

- ## 3. Preprocessing Summary
- Encoding: Categorical variables such as Region, Product, and Sales Method were converted into numerical values using One-Hot Encoding for model compatibility.
- Scaling: Standard scaling was applied to numerical features like Total Sales and Units Sold to prevent larger values from biasing the Logistic Regression model.
- Cleaning steps: Data cleaning involved formatting the 'Invoice Date' to datetime objects, removing currency symbols ($) from numeric columns, handling white spaces in strings, and removing duplicate transaction entries.
- Train–test split: The dataset was split into training (80%) and testing (20%) sets to validate the model’s ability to predict profitability on new sales data.

## 4. Model & Results
- Model used: Logistic Regression was selected for its efficiency in binary classification and its ability to provide clear coefficients showing which factors drive profit.
- Metrics: Performance was measured using Accuracy, a Confusion Matrix, and a Classification Report (Precision, Recall, and F1-Score).
- Visualizations:
