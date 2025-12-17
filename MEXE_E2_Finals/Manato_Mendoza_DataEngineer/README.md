 # Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: Trendineer
- Members:Manato, Charles Vazh & Mendoza Jancen
- Topic: Analysis on Data Engineer Jobs
- Chosen Model: Linear Regression

## 2. Dataset Overview
- Dataset Source: https://www.kaggle.com/datasets/andrewmvd/data-engineer-jobs
  
  Description: This project analyzes real-world job postings for Data Engineer roles to understand current hiring trends in the industry. The dataset includes key details such as job titles, experience levels, company locations, employment types, remote work ratios, and salary estimates. Using this information, the study explores salary distributions, career progression patterns, and regional differences in demand. The analysis also provides insights into how company attributes, such as size and founding year, relate to compensation and hiring practices.
  
Target Varible: 

- Average Salary

Features Used: 

- Job Title
  
- Rating
  
- Size
  
- Type of Ownership
  
- Indutry
  
- Sector
  
- Job State
  
- Revenue clean
  
- Job Seniority
  
- Company Age
  
- EasyApply Bin
  
- Cluster
  


 ## 3. Preprocessing Summary
- Handling Missing Values:
Missing values in numerical features were handled using median imputation, while missing values in categorical features were filled using the most frequent category. This approach preserves the dataset size and reduces bias caused by missing data.

- Label Encoding / One-Hot Encoding:
Categorical variables such as job title, industry, sector, job location, and company attributes were converted into numerical form using one-hot encoding. This encoding method was chosen to avoid introducing ordinal relationships between categories, making it suitable for Linear Regression.

- Feature Scaling:
Numerical features were standardized using StandardScaler, which scales features to have zero mean and unit variance. This ensures that numerical variables contribute equally to the model and prevents features with larger numeric ranges from dominating the learning process.

- Train–Test Split:
The dataset was divided into training and testing sets using an 80–20 split. This separation allows the model to be trained on one portion of the data and evaluated on unseen data, providing a reliable assessment of model performance.

## 4. Model And Result

### Model Used: ***Linear Regression**

Linear Regression is chosen because the goal is to predict a continuous numeric value, Average Salary.

The Linear Regression coefficients indicate that company rating has a positive relationship with average salary, suggesting that higher-rated companies tend to offer higher compensation, when other factors are held constant.

### Metrics:

- Mean Absolute Error (MAE): **17172.09**

- Mean Squared Error (RMSE): **22487.28**

- Coefficient of Determination (R²): **0.410**


### Viasualization:

**Actual vs. Predicted Plot:**

This is an Actual vs. Predicted Average Salary scatter plot.

X-axis (Actual Avg Salary)
→ The true salary from your dataset (Avg_Salary)

Y-axis (Predicted Avg Salary)
→ The salary predicted by your Linear Regression model

Each dot = one job posting

So each dot answers for this job, the real salary was X, and the model predicted Y.
<p align="center">
<img width="749" height="570" alt="image" src="https://github.com/user-attachments/assets/5e409ac4-be0d-4324-b447-a8dd6284f9ba" />


**Insights**
- Linear Regression was selected because the target variable, Avg_Salary, is a continuous numerical value.
  
- The model achieved an R² score that indicates how much salary variation can be explained by job and company attributes.

- Categorical variables such as job title, industry, and job location play a significant role in salary prediction.
  
- Proper preprocessing, including encoding and scaling, ensured stable and unbiased model training.
  
- Model performance may be improved further by incorporating text-based features from job descriptions or by applying advanced regression models. 


## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

   pip install -r requirements.txt

4. Open the `.ipynb` notebook
5. Run all cells
