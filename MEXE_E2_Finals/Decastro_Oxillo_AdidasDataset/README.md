 # Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: 
- Members:De Castro Rod & Oxillo Ivan Russ
- Topic: Adidas Sales Dataset
- Chosen Model: Logistic Regression

- ## 2. Dataset Overview
- Dataset Source: https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset
- Description: This dataset provides a detailed breakdown of Adidas' sales performance across the United States from 2020 to 2021. The data, which you plan to analyze using a Linear Regression model, covers transactions, including retailers, geographical regions, product categories, units sold, total sales, and profit margins. It is an excellent resource for practicing data preprocessing, predictive modeling, and business forecasting.
- **Target Variable:**  
- Total Sales
- The total revenue generated from a single transaction.

- **Features Used:**
  The primary features available in the dataset that are used to predict the target variable include:
- Retailer
- Region
- State
- City
- Product
- Price per Unit
- Units Sold
- Operating Profit
- Operating Margin
- Sales Method

- ## 3. Preprocessing Summary
- Encoding: The categorical features were converted into a numerical format using One-Hot Encoding. This technique is used to ensure compatibility with the Linear Regression model, allowing it to process non-numerical data without assigning misleading numerical relationships between categories.
- Scaling: The numerical features were subjected to Standard Scaling. This step standardizes the values by ensuring all numerical data is on a similar scale. Scaling is vital to prevent features with large ranges (like Units Sold) from disproportionately influencing the model's convergence and training process.
- Cleaning steps: he dataset was prepared by performing a check for missing values (NaN). The notebook confirmed that the data was complete, meaning no imputation or filling of missing entries was necessary before training the model.
- Train–test split: The data was partitioned into a training set and a testing set (80% training / 20% testing). This split is a crucial step used to evaluate the model's performance on unseen data. By testing on a separate dataset, we ensure the model is not overfit to the training data and can generalize effectively to new information.

## 4. Model & Results
- Model used: Logistic Regression was selected for its efficiency in binary classification and its ability to provide clear coefficients showing which factors drive profit.
- Metrics: Performance was measured using Accuracy, a Confusion Matrix, and a Classification Report (Precision, Recall, and F1-Score).
- Visualizations:
