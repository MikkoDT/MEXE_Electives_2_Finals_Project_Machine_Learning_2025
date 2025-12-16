# 🦟 Dengue Prediction Project (Philippines) — Linear Regression


A simple **Machine Learning project** that uses **Linear Regression** to predict dengue case trends in the Philippines based on historical data.  
The project is designed to be **easy to run**, **easy to understand**, and suitable for **academic machine learning assessments**.

---

## 👥 1) Pair Information

- **Pair Name:** SAH
- **Members:**
  - Mayuga, Kiersten Sean N.
  - Lirio, Zyrus A.
- **Topic:**
  - Dengue Prediction Project (Philippines) — Linear Regression
- **Chosen Model:** Linear Regression (Regression Analysis)

---

## 🎯 2) Objective

The model aims to:

- Predict the **number of dengue cases** based on historical data
- Identify **dengue-prone months and periods**
- Provide a baseline regression model for trend analysis

The prediction is based on the following inputs:

- **Year**
- **Month**
- **Region** (encoded)

---

## 📊 3) Dataset Overview

- **Dataset Source:**  
- **Description:**  
  The dataset contains historical dengue records in the Philippines, organized by **month**, **year**, and **region**.
- **Target Variable:**  
  - `Dengue_Cases`
- **Features Used:**  
  - Year  
  - Month (numeric conversion)  
  - Region (one-hot encoded)

---

## 🛠️ 4) Data Preprocessing

- Converted month names to numerical values
- Applied **one-hot encoding** to the Region feature
- Checked data types and missing values
- Split data into:
  - **80% training**
  - **20% testing**

---

## 📈 5) Model & Results

- **Model Used:** Linear Regression
- **Evaluation Metrics:**
  - Mean Absolute Error (MAE)
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R² Score
- **Visualization:**
  - Actual vs. Predicted Dengue Cases scatter plot

### Key Insights
- Temporal patterns strongly influence dengue case trends
- Regional data improves prediction accuracy
- Linear Regression provides a clear baseline for analysis
- Predictions can be used to classify dengue-prone periods

---

## ▶️ 6) How to Run

1. Install **VS Code**, **Python**, and the **Jupyter Extension**
2. Install dependencies:
   
pip install -r requirements.txt

3. Open the .ipynb notebook
4. Run all cells
