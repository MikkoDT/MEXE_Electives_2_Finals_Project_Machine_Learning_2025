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
  <p align="justify">The Telco Customer Churn dataset contains information on around 7,000 telecom customers, with each row representing a single customer and columns describing subscribed services, account details, and billing information, along with a target variable called <b>Churn</b> that indicates whether the customer left the company. </p>
- **Target Variable:** `Churn`

  Churn refers to the situation where customers stop using a company’s products or services within a given period.

- **Features Used:**
  - `tenure`
  - `PhoneService`
  - `Contract`
  - `PaperlessBilling`
  - `PaymentMethod`
  - `MonthlyCharges`
  - `TotalCharges`


## 3. Preprocessing Summary

- **Encoding:** 

  Categorical variables such as `PhoneService`, `Contract`, `PaperlessBilling`, `PaymentMethod`, and the target variable `Churn` were transformed into numerical values using label encoding.

- **Scaling:** 

  Feature scaling was applied using standardization to transform the input variables to a common scale with zero mean and unit variance. This step improves the stability and convergence of the Logistic Regression model and prevents features with larger values from dominating the learning process.

- **Cleaning steps:**

  The `TotalCharges` column was converted from a string data type to a numeric format using a type conversion method. This step ensures that numerical computations required for statistical analysis and machine learning can be performed correctly.

  Missing values that resulted from the data type conversion were addressed by removing the affected rows from the dataset.

  The `customerID` column was removed from the dataset since it is a unique identifier and does not contribute meaningful information for predicting customer churn.

- **Train–test split:**

  The data was split into training and testing sets, with 80% of the data used for training and 20% reserved for testing.


## 4. Model & Results
- **Model used:** Logistic Regression
    <p align="justify">Logistic Regression was chosen because the objective is binary classification, predicting whether a customer will churn (Yes) or not (No). Logistic Regression is simple, efficient, and interpretable, and it works well with datasets containing both categorical and numerical features. It also aligns well with the evaluation metrics used in this study, including accuracy, confusion matrix, precision, recall, F1-score, and the ROC curve, making it suitable for churn prediction. </p>
- **Metrics:**
  - ***Accuracy:*** `0.794889992902768 = 79.5%`

    
    
  - ***Confusion Matrix:***

    <img src="https://github.com/user-attachments/assets/cad667c4-ae51-48be-9d66-161fbc2faa76" width="450">

  - ***Precision, Recall, F1-score:***

    <img src="https://github.com/user-attachments/assets/68614637-996f-4906-be72-268a5c192d96" width="450">
  
  - ***ROC Curve:***

    <img src="https://github.com/user-attachments/assets/9bb4d566-d202-485a-a95b-6192b19de6b6" width="450">

- **Visualizations:**

  - ***Bar Plot***

      <img src="https://github.com/user-attachments/assets/9d5109ad-7ebd-4108-9e7f-e86ae88a4c4f" width="600">
  
      **Description:** The chart shows churn counts for customers with and without paperless billing.
  
      **Insight:** Paperless billing users churn more often.

  - ***Grouped Heatmap***
    
     <img src="https://github.com/user-attachments/assets/dbd62343-4938-44d3-bc6f-244a3b304982" width="600">
  
     **Description:** The heatmap shows churn rates across different contract types and payment methods.
  
     **Insight:** Month-to-month customers using electronic checks have the highest churn.
  
   - ***Scatter Plot***

     <img src="https://github.com/user-attachments/assets/c371b522-9b37-423a-85cd-5c79b900ae4c" width="600">
  
     **Description:** The plot compares monthly and total charges for churn and non-churn customers.
  
     **Insight:** High-monthly-charge customers with low total charges churn more frequently.
  
- **Insights:**

1. ***Model Performance***

    The logistic regression model showed good overall performance based on accuracy, precision, recall, and the ROC curve. The results indicate that the model can reliably classify customers who are likely to   churn and those who are not. Although the performance is not perfect, it is acceptable for generating useful business insights.

2. ***Feature Behavior*** 

    The analysis showed that features such as contract type, tenure, and monthly charges have the strongest influence on churn. Customers with month-to-month contracts had a noticeably higher churn rate. Customers with longer tenure tended to stay, while higher monthly charges increased the likelihood of churn. These patterns highlight which customer groups are more at risk.

3. ***Interpretation of Results*** 

    Based on the model outputs, customers who leave the company usually have short tenure and higher monthly bills. This suggests that new customers may still be evaluating the service and can easily switch if they are not satisfied. The results also show that payment and billing preferences can affect churn behavior, which may be connected to customer convenience or satisfaction.

4. ***Improvement Suggestions***

    The model can be improved by addressing class imbalance if churn cases are fewer than non-churn cases. Techniques such as class weighting or SMOTE may help improve recall for the minority class. Additional customer data, such as service complaint history or usage behavior, could also strengthen the model. Testing other machine learning models like Random Forest or XGBoost may provide higher accuracy and better overall performance.

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

   pip install -r requirements.txt

4. Open the `.ipynb` notebook
5. Run all cells
