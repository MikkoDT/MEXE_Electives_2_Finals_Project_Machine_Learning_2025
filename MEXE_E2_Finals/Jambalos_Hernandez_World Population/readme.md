
# Final Assessment — Machine Learning Model

## 1. Pair Information
- **Pair Name:** Jambalos_Hernandez
- **Members:**
  - Queian Kim Jambalos
  - Lelanie Lorraine Hernandez
- **Topic:** World Population Growth Rate Prediction
- **Chosen Model:** Linear Regression

## 2. Dataset Overview
- **Dataset Source:** `world_population_cleaned.csv` (World Population Dataset)
- **Description:** A snapshot of 193 countries containing their total population counts and current annual growth rates.
- **Target Variable:** `Growth Rate` (Continuous percentage)
- **Features Used:** `Population` (Transformed via Logarithm to handle skewness).

## 3. Preprocessing Summary
- **Encoding:** **None.** We explicitly dropped the `Country` column because it is a high-cardinality identifier (193 unique values). Encoding it would have caused the "Curse of Dimensionality" and overfitting.
- **Scaling:** `StandardScaler` (Applied to the Log-Transformed population data).
- **Cleaning steps:**
  1. Checked for missing values.
  2. Applied **Log Transformation** (`np.log`) to the `Population` column to normalize the distribution (fixing the huge gap between countries like China and Tuvalu).
- **Train–test split:** 80% Training / 20% Testing (`random_state=123`).

## 4. Model & Results
- **Model used:** Linear Regression
- **Metrics:**
  - **MAE:** ~0.0073 (Low average error)
  - **RMSE:** ~0.0108
  - **R² Score:** ~0.117 (Positive score, indicating the model successfully found a trend).
- **Visualizations:**
  - Scatter plot with a Regression Line showing the negative correlation between Size and Growth Rate.
- **Insights:**
  1. **Model Performance:** We achieved a positive $R^2$ score by fixing the data skewness, proving that population size has a weak but statistically significant impact on growth.
  2. **Feature Behavior:** Small countries exhibit high volatility (extreme growth or decline), while large nations tend to stabilize near the global average.
  3. **Data Constraint:** Population size acts as a proxy for development; to improve predictive power further, future iterations would require biological features like Fertility Rate or Median Age.

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
