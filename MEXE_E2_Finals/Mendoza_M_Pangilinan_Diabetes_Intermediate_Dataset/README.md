# <p align="center">Final Assessment — Machine Learning Model</p>

##  1. Pair Information

- **Pair Name:** Corona Chronicles
- **Members:**
  - Mendoza, Mark Jason  
  - Pangilinan, Von Mathew
- **Topic:**  Diabetes Intermediate Dataset
- **Chosen Model:**  Logistic Regression

---

##  2. Dataset Overview

- **Dataset Source:**
  - https://www.kaggle.com/datasets/samira1992/diabetes-intermediate-dataset/data

- **Description:**
    <p align="justify">
<strong>Diabetes Intermediate Dataset</strong> is a well-organized collection of health-related factors that include patient categories, diagnostic measures, and treatment results intended to support research and analysis of diabetes and its progression. The dataset contains a large number of features that can be used to examine the relationships between various medical parameters and the occurrence or management of diabetes in individuals.
</p>

- **Target Variable:**
  -  **Outcome** (*`Non-Diabetic`* / *`Diabetic`*)

- **Features Used:**
  -  *`Pregnancies`*
  -  *`Glucose`*
  -  *`BloodPressure`*
  -  *`SkinThickness`*
  -  *`Insulin`*
  -  *`BMI`*
  -  *`DiabetesPedigreeFunction`*
  -  *`Age`*

---

##  3. Preprocessing Summary

<div style="text-align: justify">

- **Encoding**  
  ▸ All features in the dataset are numerical; therefore, no categorical encoding was required. 
- **Scaling**  
  ▸ Standardization was applied to transform input features to zero mean and unit variance, ensuring equal contribution of variables and improving the stability of the Logistic Regression model.

- **Cleaning Steps**  
  ▸ The dataset was checked for missing values and shuffled to eliminate potential ordering bias.  
  ▸ The target variable was separated from the feature set to prepare the data for supervised learning.

- **Train–Test Split**  
  ▸ The dataset was divided into training and testing sets, with 75% of the data used for training and 25% reserved for testing to evaluate performance on unseen data.

</div>

---

##  4. Model & Results
- **Model Used:**  
  Logistic Regression 
- **Metrics:**  
  -  **Accuracy** = `%`
  -  **Precision** = `%`
  -  **Recall** =  `%`
  -  **F1-Score** = `%`
  - image ng Accuracy, Precision, Recall, at F1-Score
  
  - **Confusion Matrix** 
  <img width="401" height="351" alt="image" src="https://github.com/user-attachments/assets/bdd042d8-67fe-4f3c-b672-a78f0c55cde8" />

  - **ROC Curve**  
  <img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/674aaf48-5362-41f0-a15c-77b68a0fd311" />

- **Visualizations:**  
  - **Scatterplot**
  <img width="1489" height="1356" alt="image" src="https://github.com/user-attachments/assets/9d99e36c-54c3-4be4-bc81-4dcd17a6ed9f" />
  
  **Description:** The scatter plots compare each health variable with the diabetes outcome, showing how data points are distributed for diabetic and non-diabetic individuals. They highlight overlaps and separations between the two outcome groups across features.
  
  **Insight:** Glucose and BMI show noticeable clustering where higher values are more frequently associated with diabetic outcomes. Other variables such as blood pressure and skin thickness show significant overlap, indicating weaker separation.
  
  - **Correlation Heatmap**  
  <img width="914" height="691" alt="image" src="https://github.com/user-attachments/assets/44a9c60d-5b10-409d-b18b-d483a68e7f1a" />
  
  **Description:** The correlation heatmap visualizes the relationships among all numerical features and the diabetes outcome. Brighter colors indicate stronger correlations, while darker colors represent weaker relationships.
  
  **Insight:** Glucose has the strongest positive correlation with diabetes outcome, followed by BMI and age. Most remaining features show weak correlations, suggesting they contribute less individually to diabetes prediction.
  
- **Key Insights:** 

  ***1. Classification Effectiveness***

  The logistic regression model demonstrated solid predictive performance based on accuracy and classification metrics. While the model is not flawless, it effectively distinguishes between diabetic and non-diabetic cases and is suitable for basic medical risk prediction.

  ***2. Key Predictive Factors***

  The analysis indicates that variables such as glucose level, BMI, and age play a major role in predicting diabetes. Higher glucose readings and increased body mass index significantly raise the likelihood of a diabetes diagnosis.

  ***3. Insights from Model Outcomes***

  The results show that individuals with elevated glucose levels and higher BMI are more frequently classified as diabetic. These findings align with established medical understanding of diabetes risk factors.

  ***4. Opportunities for Model Enhancement***

  The model could be strengthened by addressing class imbalance and applying proper feature scaling. Testing more advanced models such as Random Forest or Support Vector Machines may lead to improved accuracy and robustness.
  
---

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

```bash

pip install -r requirements.txt
```
3. Open the `.ipynb` notebook
4. Run all cells
