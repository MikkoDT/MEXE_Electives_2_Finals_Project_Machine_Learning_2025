# 📑 Final Assessment — Machine Learning Model

## Project Overview
This project applies **Linear Regression** to school masterlist data to examine how different school-related factors relate to a target outcome. It is part of a final machine learning assessment and focuses on using data-driven analysis to understand patterns in educational datasets.

---

## 1. Pair Information
- **Pair Name:** Eskwelaaa  
- **Members:** Marco Calaton & Megildo Perez  
- **Topic:** School  
- **Model Used:** Linear Regression  

---

## 2. Dataset Overview
- **Dataset Source:**  
  https://www.kaggle.com/datasets/bwandowando/deped-philippine-school-masterlist-2020-21  

- **Description:**  
  The dataset is based on the Department of Education (DepEd) Philippine School Masterlist for School Year 2020–2021. It contains structured school records and location details useful for educational data analysis.

- **Target Variable:**  
  **Urban/Rural** (encoded numerically)

---

## 3. Data Preprocessing
The following preprocessing steps were applied before training the model:

1. **Data Loading**  
   The dataset was imported from a CSV file using Pandas to enable structured data handling and analysis.

2. **Data Cleaning**  
   Unnecessary spaces in column names were removed to ensure consistent and error-free referencing during data processing.

3. **Feature Selection (Data Reduction)**  
   Only relevant columns—**Barangay, Sector, Legislative District, and Urban/Rural**—were retained to reduce data complexity and focus the analysis on important features.

4. **Data Validation**  
   A validation check was performed to ensure that only existing columns were selected, preventing errors caused by missing or inconsistent data fields.

---

## 4. Model & Results

---

## 5. Insights
- **Model Performance:**  
  The model demonstrates acceptable performance in distinguishing between Urban and Rural schools, as reflected by consistent results and ROC curve behavior.

- **Feature Behavior:**  
  Location-related features such as legislative district and sector show stronger influence on predictions compared to more granular attributes like barangay.

- **Interpretation of Results:**  
  The results indicate that school location patterns can be reasonably inferred from structured geographic and administrative data, though overlaps between classes still exist.

- **Limitations:**  
  Some misclassifications occur due to similarities in attributes between Urban and Rural schools, suggesting that the current feature set may not fully capture all distinguishing factors.

- **Improvement Suggestions:**  
  Performance could be improved by incorporating additional features, applying feature engineering, or experimenting with more advanced models.

---

## 6. How to Run the Project

### Requirements
- VS Code  
- Python 3.x  
- Jupyter Notebook Extension  


