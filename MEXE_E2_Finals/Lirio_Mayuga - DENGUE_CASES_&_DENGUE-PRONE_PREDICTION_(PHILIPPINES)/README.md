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

* **Dataset Source:** (https://www.kaggle.com/datasets/vincentgupo/dengue-cases-in-the-philippines)
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

  * Feature scaling was not applied because the features were already in comparable numeric ranges and the model served as a baseline regression approach.

* **Cleaning Steps:**

  * Data types were checked and corrected where necessary.
  * Missing values were inspected prior to training. The dataset contained minimal to no missing values and therefore did not require extensive imputation.

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

* Mean Absolute Error (MAE)  : 745.47
* Mean Squared Error (MSE)  : 1640069.20
* Root Mean Squared Error (RMSE) : 1280.65
* R² Score   : 0.0691

### Visualizations

* Scatter plot comparing **Actual vs. Predicted Dengue Cases** to assess model fit and prediction behavior.

The scatter plot compares actual and predicted dengue cases, showing that the linear regression model performs reasonably well for low to moderate case counts, where most data points are clustered. However, as actual dengue cases increase, predictions become more dispersed, indicating reduced accuracy during high-outbreak periods. This suggests that the model captures general trends but has limitations in predicting extreme dengue spikes.

  <img width="704" height="547" alt="image" src="https://github.com/user-attachments/assets/3b529202-ef4a-4604-98de-312e90c2a60e" />

* Average Dengue Cases per Month (Seasonality Plot)


The monthly dengue case trend shows a clear seasonal pattern, with higher average cases occurring during specific months. This supports the inclusion of the month variable in the linear regression model and demonstrates the seasonal nature of dengue transmission in the Philippines.

<img width="859" height="597" alt="image" src="https://github.com/user-attachments/assets/a7b83929-8ce4-4179-a105-42c026bd34e3" />



* Heatmap of Dengue-Prone Months per Region

This visualization is needed to quickly identify which regions are most at risk during specific months, supporting the model’s use of month and region as key predictors and aiding dengue-prone planning and interpretation.
The heatmap shows the average dengue cases across Philippine regions by month, where darker shades indicate more dengue-prone periods. It highlights clear seasonal and regional patterns, with higher risk concentrated in specific months and regions.
  <img width="1125" height="751" alt="image" src="https://github.com/user-attachments/assets/63bd64ae-3002-4a5d-8425-8eb6c6c28725" />


### Insights 

🔍 Insight 1: The model captures seasonal and regional trends but struggles with extreme outbreaks

The linear regression model is able to learn the general relationship between month, year, and region and dengue case counts, as shown by reasonable predictions for low to moderate dengue levels. However, the “Actual vs Predicted Dengue Cases” plot shows increased dispersion at higher case values, indicating that the model has difficulty accurately predicting extreme outbreak periods. This suggests that dengue incidence is influenced by nonlinear factors (e.g., sudden weather changes or localized outbreaks) that are not fully captured by a simple linear model.

🔍 Insight 2: Month and region are key predictors of dengue incidence in the Philippines

The seasonality and heatmap visualizations demonstrate that dengue cases are not evenly distributed across the year or across regions. Certain months consistently show higher average dengue cases, and some regions exhibit stronger susceptibility during these periods. This supports the inclusion of month and region as important independent variables, confirming that dengue transmission in the Philippines is highly seasonal and geographically dependent.

🔍 Insight 3: Linear regression is suitable for trend estimation but limited for outbreak prediction

The evaluation metrics (such as R², MAE, and RMSE) indicate that linear regression is effective for estimating overall dengue trends and average case behavior. However, its reduced accuracy during peak dengue months highlights its limitation for precise outbreak prediction. This implies that while the model is useful for baseline forecasting and dengue-prone identification, more advanced models (e.g., polynomial regression or time-series models) could improve prediction performance for sudden spikes.

---

## ▶️ 5. How to Run

1. Install **VS Code**, **Python**, and the **Jupyter Extension**
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the `.ipynb` notebook located in the `notebooks/` folder
4. Run all cells to reproduce the results
