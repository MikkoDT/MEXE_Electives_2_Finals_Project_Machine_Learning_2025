
# <p align="center">Final Assessment — Machine Learning Model</p>

##  1. Pair Information

- **Pair Name:** Ballers
- **Members:**
  - Banawa, Kian Isaac P.
  - Falcunaya, Vince Ian F.
- **Topic:**  NBA Games
- **Chosen Model:**  Logistic Regression

---

##  2. Dataset Overview

- **Dataset Source:**
  - https://www.kaggle.com/datasets/nathanlauga/nba-games

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
- **Data Shuffling**  
  ▸ A data shuffling was utilize for gradient descent optimization and prevents ordering bias when training and testing sets.
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
  -  **Accuracy** = `80%`
  -  **Precision** = `82%`
  -  **Recall** = `62%`
  -  **F1-Score** = `70%`<br/>
  <p align="center">
    <img width="776" height="294" alt="image" src="https://github.com/user-attachments/assets/62f8435e-4fe5-4b08-9515-44de1e5c90ac" /><br/>
      Figure 1: Classification report of the model with macro average and weighted average 
  <p/>


  - **Confusion Matrix**
  <p align="center">
    <img width="653" height="542" alt="{1D49CD24-3450-4050-BE94-15D83EF1DFCA}" src="https://github.com/user-attachments/assets/4ba130a6-feff-47fe-bbaf-a023a0197c78" /><br/>
     Figure 2: Confusion matrix with 109 True Positive, 28 False Positive, 10 False Negative and 45 True Negative
 <p/>

  - **ROC Curve**
<p align="center">
 <img width="851" height="683" alt="output" src="https://github.com/user-attachments/assets/036cf605-5ea5-4987-a112-deb2a19a7713" /><br/>
    Figure 3: Receiver Operating Characteristic Curve with metric about 0.8 of True Positive Rate
  
<p/>
 

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
