# 📑 Final Assessment — Machine Learning Model

## Project Overview
This project applies **Linear Regression** to school masterlist data to examine how different school-related factors relate to a target outcome. It is part of a final machine learning assessment and focuses on using data-driven analysis to understand patterns in educational datasets.

---

## 1. Pair Information
- **Pair Name:** Error 404: School Not Found 
- **Members:** Marco Calaton & Megildo Perez  
- **Topic:** School  
- **Model Used:** Logistic Regression

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

- **Encoding:** Converted categorical variables into numerical form  
- **Scaling:** Standardized numerical features for improved stability  
- **Data Cleaning:**
  - Renamed columns for consistency  
  - Handled missing values  
  - Removed duplicate records  
  - Verified and corrected data types  
- **Train–Test Split:** Split the dataset into training and testing sets  

---

## 4. Model & Results
- **Algorithm:** Linear Regression  

### Reason for Selection
- Simple and easy to interpret  
- Useful for identifying relationships between variables  
- Works well as a baseline model for continuous prediction tasks  

---

## 5. Key Insights
- The Linear Regression model shows a clear relationship between school-related features and the target variable.  
- Predictions are generally reasonable, but errors still exist, suggesting other factors may influence the outcome.  
- Some features contribute more strongly than others, emphasizing the importance of feature selection.  

---

## 6. How to Run the Project

### Requirements
- VS Code  
- Python 3.x  
- Jupyter Notebook Extension  

### Installation
```bash
git clone <repository-url>
cd <repository-folder>
pip install -r requirements.txt
