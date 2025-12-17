# 🦟 Final Assessment — Machine Learning Model

## 👥 1. Pair Information

* **Pair Name:** SAH
* **Members:**

  * Mayuga, Kiersten Sean N.
  * Lirio, Zyrus A.
* **Topic:** Dengue Prediction Project (Philippines) — Linear Regression
* **Chosen Model:** Linear Regression

---

## 📊 2. Dataset Overview

* **Dataset Source:** Historical dengue surveillance data (Philippines)
* **Description:**
  The dataset contains historical records of reported dengue cases in the Philippines, organized by **year**, **month**, and **region**. Each record represents the total number of dengue cases for a given region and month.
* **Target Variable:**

  * `Dengue_Cases`
* **Features Used:**

  * `Year`
  * `Month` (converted from month names to numeric values)
  * `Region` (one-hot encoded)

---

## 🛠️ 3. Preprocessing Summary

* **Encoding:**

  * Month names were converted into numeric values (1–12).
  * The categorical `Region` feature was transformed using **one-hot encoding** to allow the regression model to process regional information.

* **Scaling:**

  * Feature scaling was **not applied**, as Linear Regression does not strictly require scaled inputs and all features were already represented in comparable numeric ranges.

* **Cleaning Steps:**

  * Data types were checked and corrected where necessary.
  * Missing values were inspected to ensure dataset completeness before training.

* **Train–Test Split:**

  * The dataset was split into **80% training** and **20% testing** sets using a fixed random state to ensure reproducibility:

  ```python
  train_test_split(X, y, test_size=0.2, random_state=123)
  ```

---

## 📈 4. Model & Results

* **Model Used:**

  * Linear Regression

### Model Rationale

Linear Regression was selected because the objective of the project is to predict **continuous numerical values** (number of dengue cases). Additionally, Linear Regression provides a clear and interpretable baseline model for analyzing temporal and regional trends in dengue incidence.

### Evaluation Metrics

The model was evaluated on the test dataset using the following regression metrics:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

### Visualizations

* Scatter plot comparing **Actual vs. Predicted Dengue Cases** to assess model fit and prediction behavior.

### Insights 

1. The model achieved a reasonable R² score, indicating that **temporal features such as year and month significantly influence dengue case trends**.
2. Monthly patterns suggest seasonality, with higher dengue cases occurring during specific periods of the year, consistent with known rainy-season outbreaks.
3. Incorporating regional data through one-hot encoding improved prediction accuracy by capturing **geographic variability** in dengue incidence.
4. Prediction errors tend to increase during outbreak peaks, suggesting that Linear Regression may underfit extreme values and sudden surges in cases.
5. Future improvements could include **Polynomial Regression or tree-based models** to better capture non-linear patterns in dengue transmission.

---

## ▶️ 5. How to Run

1. Install **VS Code**, **Python**, and the **Jupyter Extension**
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the `.ipynb` notebook located in the `notebooks/` folder
4. Run all cells to reproduce the results
