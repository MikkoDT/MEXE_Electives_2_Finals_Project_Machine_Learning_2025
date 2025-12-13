# <p align="center">Final Assessment — Machine Learning Model</p>

## 1. Pair Information
- **Pair Name:** Busy-ness Duo
- **Members:**
  -   Jhann-rey Naz
  -   Beaver Freud Virrey
- **Topic:** Telco Customer Churn
- **Chosen Model:** Logistic Regression

## 2. Dataset Overview
- **Dataset Source:** https://www.kaggle.com/datasets/syedumeerr/telco-customer-churn 
- **Description:**
  <p align="justify">The Telco Customer Churn dataset contains information on around 7,000 telecom customers, with each row representing a single customer and columns describing subscribed services, account details, and billing information, along with a target variable called <b>Churn</b> that indicates whether the customer left the company. The features include customer tenure, contract type, phone services, payment method, monthly charges, and total charges. This dataset is used for classification tasks, especially for building logistic regression to predict customer churn and derive business insights for customer retention strategies. </p>
- **Target Variable:** Churn
- **Features Used:**
  - Tenure
  - Phone Service
  - Contract
  - Paperless Billing
  - Payment Method
  - Monthly Charges
  - Total Charges 


## 3. Preprocessing Summary
- **Encoding:**
- **Scaling:**
- **Cleaning steps:**
- **Train–test split:**

## 4. Model & Results
- **Model used:** Logistic Regression
  <p align="justify">Logistic Regression was chosen because the objective is binary classification predicting whether a customer will churn (Yes) or not (No). Logistic Regression is a simple, efficient, and interpretable model that performs well for datasets with mixed categorical and numerical features. It also provides useful metrics such as probabilities, feature weights, and decision boundaries, making it suitable for churn prediction. </p>
- **Metrics:**
  - Accuracy
  - Confusion Matrix
  - Precision, Recall, F1-score
  - ROC Curve
- **Visualizations:**

1. Bar Plot
   <p align="center">
  <img src="https://github.com/user-attachments/assets/9d5109ad-7ebd-4108-9e7f-e86ae88a4c4f"></p>


2. Grouped Heatmap
  <p align="center">
  <img src="https://github.com/user-attachments/assets/dbd62343-4938-44d3-bc6f-244a3b304982"></p>

   
3. Scatter Plot
  <p align="center">
  <img src="https://github.com/user-attachments/assets/c371b522-9b37-423a-85cd-5c79b900ae4c"></p>

  
- **Insights (3–5):**

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells
