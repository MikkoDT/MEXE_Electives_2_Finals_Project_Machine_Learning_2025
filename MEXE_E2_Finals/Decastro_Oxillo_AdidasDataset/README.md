 # Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: 
- Members: De Castro Rod Andrei & Oxillo Ivan Russ
- Topic: Adidas Sales Dataset
- Chosen Model: Linear Regression

## 2. Dataset Overview
- Dataset Source: https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset
- Description: This dataset provides a detailed breakdown of Adidas' sales performance across the United States from 2020 to 2021. The data, which you plan to analyze using a Linear Regression model, covers transactions, including retailers, geographical regions, product categories, units sold, total sales, and profit margins. It is an excellent resource for practicing data preprocessing, predictive modeling, and business forecasting.
  
Dependent Variable: 

- Total Sales

Independent Variables: 

- Month

- Retailer

- Region

- Product

- Price per Unit

- Operating Margin

- Sales Method

 ## 3. Preprocessing Summary
- Encoding: The categorical features were converted into a numerical format using One-Hot Encoding. This technique is used to ensure compatibility with the Linear Regression model, allowing it to process non-numerical data without assigning misleading numerical relationships between categories.
- Scaling: The numerical features were subjected to Standard Scaling. This step standardizes the values by ensuring all numerical data is on a similar scale. Scaling is vital to prevent features with large ranges (like Units Sold) from disproportionately influencing the model's convergence and training process.
- Cleaning steps: The dataset was prepared by performing a check for missing values (NaN). The notebook confirmed that the data was complete, meaning no imputation or filling of missing entries was necessary before training the model.
- Train–test split: The data was partitioned into a training set and a testing set (80% training / 20% testing). This split is a crucial step used to evaluate the model's performance on unseen data. By testing on a separate dataset, we ensure the model is not overfit to the training data and can generalize effectively to new information.

## 4. Model And Result

### Model Used: ***Linear Regression**

Linear Regression is chosen because the goal is to predict a continuous numeric value, Total Sales.

This model is a strong fit because Total Sales is mathematically derived from key features like Price per Unit and Units Sold, suggesting a highly linear relationship between the independent variables and the target variable. Furthermore, the simplicity, speed, and interpretability of Linear Regression are ideal for understanding how factors like retailer, region, product type, and sales method influence overall revenue.


### Metrics:

Mean Absolute Error (MAE): **76556.46201207295**

Mean Squared Error (MSE): **106200.20194934374**

Coefficient of Determination (R²): **0.4425561689284665**

Adjusted R²: **0.44052593645317994**

### Visualization:

**Actual vs. Predicted Sales Plot:**

This plot shows how the model's predicted sales figures relate to the true recorded sales. The tight clustering of all data points along the ideal diagonal line visually confirms the model’s exceptional fit and high predictive accuracy. This alignment indicates a minimal difference between the forecast and the actual sales outcomes.

<p align="center">
<img width="749" height="570" alt="image" src="https://github.com/user-attachments/assets/b527805f-66e8-49a0-ac53-2d175ba48564" />

**Residual Plot:**

This visualization displays the errors (residuals) of the model against the predicted sales. The key finding is the random, uniform scattering of these errors around the central zero line. This pattern is crucial as it validates a core assumption of Linear Regression: that the model's errors are purely random and unbiased, confirming the suitability of the model for this dataset.
<p align="center">
<img width="719" height="639" alt="image" src="https://github.com/user-attachments/assets/cb4c5806-ed9b-4d05-80d5-dd51dcc0db1a" />

**Insights**
- Model Performance:
  The linear regression model achieved an R² score of 0.44, indicating that approximately 44% of the variation in total sales is explained by the selected independent variables. This level of performance is considered reasonable for real-world sales data, where outcomes are influenced by many external and unpredictable factors not captured in the dataset. The close alignment between R² and adjusted R² further confirms that the model maintains stable explanatory power.

- Feature Behavior:
  The independent variables including price per unit, operating margin, product type, region, retailer, sales method, and month contribute meaningfully to the prediction of total sales. The minimal difference between R² and adjusted R² suggests that the included features provide relevant information rather than introducing redundancy. Categorical variables such as product, region, and sales method help capture market and distribution differences that affect sales performance.

- Interpretation and Improvement Opportunities:
  While the model explains a significant portion of sales variability, more than half of the variation remains unexplained. This indicates that total sales are also affected by external factors such as promotions, seasonal demand, marketing activities, and consumer behavior, which are not present in the dataset. Model performance could be improved by incorporating additional features such as promotional indicators, holiday effects, or by applying non-linear models to capture more complex relationships.



## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

   pip install -r requirements.txt

4. Open the `.ipynb` notebook
5. Run all cells

