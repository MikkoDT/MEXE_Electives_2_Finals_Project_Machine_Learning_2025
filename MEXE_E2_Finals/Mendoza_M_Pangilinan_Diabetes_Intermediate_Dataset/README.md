#  Final Assessment — Machine Learning Model

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

##  Preprocessing Summary

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
  -  Accuracy = `%`
  -  Precision = `%`
  -  Recall =  `%`
  -  F1-Score = `%`
  - image ng Accuracy, Precision, Recall, at F1-Score
  
  - Confusion Matrix 
  <img width="401" height="351" alt="image" src="https://github.com/user-attachments/assets/bdd042d8-67fe-4f3c-b672-a78f0c55cde8" />

  - ROC Curve  
  <img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/674aaf48-5362-41f0-a15c-77b68a0fd311" />

- **Visualizations:**  
  - Scatterplot
  <img width="1489" height="1356" alt="image" src="https://github.com/user-attachments/assets/9d99e36c-54c3-4be4-bc81-4dcd17a6ed9f" />

  
  - Correlation Heatmap  
  <img width="914" height="691" alt="image" src="https://github.com/user-attachments/assets/44a9c60d-5b10-409d-b18b-d483a68e7f1a" />

  
- **Key Insights:**  
  - lagay dito
  
---

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

- pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells
