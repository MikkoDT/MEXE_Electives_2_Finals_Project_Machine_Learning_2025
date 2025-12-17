# Final Assessment — Machine Learning Model

## 1. Pair Information
- **Members:**
  - Queian Kim Jambalos
  - Lelanie Lorraine Hernandez
- **Topic:** World Population Growth Rate Prediction
- **Chosen Model:** Linear Regression

## 2. Dataset Overview
- **Dataset Source:** `world_population_cleaned.csv` (World Population Dataset)
- **Description:** A dataset containing population counts and annual growth rates for 193 countries. It represents a "snapshot" of global demographics.
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
  - **MAE (Mean Absolute Error):** ~0.0073
  - **RMSE (Root Mean Squared Error):** ~0.0108
  - **R² Score:** ~0.117 (Positive score indicating a statistically significant trend).
- **Visualizations:**
  - **Regression Plot:** A scatter plot showing Actual vs. Predicted values with a regression line, illustrating the negative correlation between size and growth.
- **Insights:**
  1. **Model Success:** By applying Log Transformation, we turned a failing model (negative R²) into a successful one (positive R²), proving that data distribution matters more than model complexity.
  2. **Feature Behavior:** Small nations show high volatility (extreme growth or decline), while massive nations tend to stabilize near the global average growth rate.
  3. **Interpretation:** There is a weak but real negative correlation: as countries get larger, their growth rate tends to slow down due to demographic transitions.

## 5. How to Run
1. Install **VS Code** + **Python** + **Jupyter Extension**.
2. Install dependencies by opening a terminal in the folder and running:
   ```bash
   pip install -r requirements.txt
