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

* Mean Absolute Error (MAE)  : 745.47
* Mean Squared Error (MSE)  : 1640069.20
* Root Mean Squared Error (RMSE) : 1280.65
* R² Score   : 0.0691

### Visualizations

* Scatter plot comparing **Actual vs. Predicted Dengue Cases** to assess model fit and prediction behavior.

### Insights 

1. Seasonal patterns are evident, with higher dengue cases occurring during certain months of the year.

2. Regional information helps capture geographic variation but remains insufficient to explain outbreak behavior.

3. Dengue case data is highly non-linear and outbreak-driven, making it poorly suited for Linear Regression and resulting in higher prediction errors and a low R² value.

4. Errors increase during peak outbreaks, indicating that the model underfits sudden surges in dengue cases.

5. More advanced or non-linear models may better capture the complexity of dengue transmission.

---

## ▶️ 5. How to Run

1. Install **VS Code**, **Python**, and the **Jupyter Extension**
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the `.ipynb` notebook located in the `notebooks/` folder
4. Run all cells to reproduce the results
