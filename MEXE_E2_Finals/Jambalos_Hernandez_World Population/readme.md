# Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: World pop
- **Members:**
  - Queian Kim Jambalos
  - Lelanie Lorraine Hernandez
- **Topic:** World Population Growth Rate Prediction
- **Chosen Model:** Linear Regression

## 2. Dataset Overview
- **Dataset Source:** https://www.kaggle.com/datasets/iamsouravbanerjee/world-population-dataset (World Population Dataset)
- **Description:** A dataset containing population counts and annual growth rates for 193 countries. The data represents a **2022 demographic snapshot**.
- **Target Variable:** `Growth Rate` (Continuous percentage representing annual population change).
- **Features Used:** `Population` (Transformed via Logarithm to normalize the distribution).

## 3. Preprocessing Summary
- **Encoding:** **None.** We explicitly dropped the `Country` column because it is a unique identifier (193 categories). Encoding it would have caused the "Curse of Dimensionality" and model overfitting.
- **Scaling:** `StandardScaler` (Applied to the Log-Transformed population data to center values around 0).
- **Cleaning steps:**
  1. Checked for and handled missing values (none found).
  2. Applied **Log Transformation** (`np.log`) to the `Population` column to fix the extreme "Power Law" skewness caused by outliers like China and India.
- **Train–test split:** 80% Training / 20% Testing (`random_state=123`).

## 4. Model & Results
- **Model used:** Linear Regression (`sklearn.linear_model.LinearRegression`)
- **Metrics:**
  - **MAE (Mean Absolute Error):** ~0.00604
  - **RMSE (Root Mean Squared Error):** ~0.00784
  - **R² Score:** ~0.02826 (Positive score indicating a statistically significant trend).
- **Visualizations:**
  - **Regression Plot:** A scatter plot showing Actual vs. Predicted values with a regression line, illustrating the negative correlation between size and growth.
    <img width="863" height="547" alt="image" src="https://github.com/user-attachments/assets/a4e3b145-7ce8-4dc8-9361-7316ccae108b" />
    
- **Insights:**
1. Model Performance (R² Shift)
Our Linear Regression model achieved an **R² score of ~0.02826**. While this number appears low, it represents a significant success compared to initial attempts using raw data (which resulted in negative scores). A positive R² indicates that the model successfully identified a **statistically significant signal**: there is a real, albeit weak, correlation between a country's size and its growth rate.
2. Feature Behavior ( The "Log" Effect)
The raw population data followed a **Power Law distribution** (a few massive outliers like China/India vs. many small nations), which distorted the linear model. By applying a **Logarithmic Transformation**, we successfully normalized this distribution. This allowed the model to process "orders of magnitude" rather than raw counts, revealing trends that were previously hidden by the massive size gaps.
3. Interpretation of Results
The regression line reveals a **negative correlation**: as population size increases, the growth rate tends to stabilize or slightly decline.
* **Small Nations:** Exhibit high volatility (extreme highs and lows).
* **Large Nations:** Tend to converge toward the global average.
This suggests that as countries become massive, their demographic transition usually leads to slower, more stable growth.
4. Improvement Suggestions
To increase the model's predictive power (aiming for R² > 0.8), future iterations should move beyond population size (which is just a proxy) and incorporate **causal biological factors**, specifically:
* **Fertility Rate:** The primary driver of natural increase.
* **Median Age:** To account for aging populations.
* **GDP per Capita:** To correlate economic development with demographic trends.

## 5. How to Run
1. Install **VS Code** + **Python** + **Jupyter Extension**.
2. Install dependencies by opening a terminal in the folder and running:
   ```bash
   pip install -r requirements.txt
