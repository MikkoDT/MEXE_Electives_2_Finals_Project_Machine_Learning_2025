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

**1. Bar Plot**

   
  <img src="https://github.com/user-attachments/assets/9d5109ad-7ebd-4108-9e7f-e86ae88a4c4f"></p>
  
  **Description:** The chart shows churn counts for customers with and without paperless billing.
  
  **Insight:** Paperless billing users churn more often.
  
---
**2. Grouped Heatmap**
    
  
  <img src="https://github.com/user-attachments/assets/dbd62343-4938-44d3-bc6f-244a3b304982"></p>
  
  **Description:** The heatmap shows churn rates across different contract types and payment methods.
  
  **Insight:** Month-to-month customers using electronic checks have the highest churn.
  
---  
**3. Scatter Plot**
    
  
  <img src="https://github.com/user-attachments/assets/c371b522-9b37-423a-85cd-5c79b900ae4c"></p>
  
  **Description:** The plot compares monthly and total charges for churn and non-churn customers.
  
  **Insight:** High-monthly-charge customers with low total charges churn more frequently.
  
---
- **Insights:**

**1. Model Performance**

The logistic regression model showed good overall performance based on accuracy, precision, recall, and the ROC curve. The results indicate that the model can reliably classify customers who are likely to churn and those who are not. Although the performance is not perfect, it is acceptable for generating useful business insights.

**2. Feature Behavior** 

The analysis showed that features such as contract type, tenure, and monthly charges have the strongest influence on churn. Customers with month-to-month contracts had a noticeably higher churn rate. Customers with longer tenure tended to stay, while higher monthly charges increased the likelihood of churn. These patterns highlight which customer groups are more at risk.

**3. Interpretation of Results** 

Based on the model outputs, customers who leave the company usually have short tenure and higher monthly bills. This suggests that new customers may still be evaluating the service and can easily switch if they are not satisfied. The results also show that payment and billing preferences can affect churn behavior, which may be connected to customer convenience or satisfaction.

**4. Improvement Suggestions**

The model can be improved by addressing class imbalance if churn cases are fewer than non-churn cases. Techniques such as class weighting or SMOTE may help improve recall for the minority class. Additional customer data, such as service complaint history or usage behavior, could also strengthen the model. Testing other machine learning models like Random Forest or XGBoost may provide higher accuracy and better overall performance.

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells
