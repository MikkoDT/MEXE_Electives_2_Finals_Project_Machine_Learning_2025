
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
    <strong>The NBA Games dataset</strong> is a collection of historical National Basketball Association (NBA) data covering seasons from 2004 up through around 2020 (depending on the file). It’s designed for analytics, machine learning, and exploration of NBA game results, player stats, team info, and rankings.
</p>

- **Target Variable:**
  -  **HOME_TEAM_WINS** (*`Win`* / *`Lose`*)

- **Features Used:**
  -  *`FG_PCT_home`*
  -  *`FT_PCT_home	`*
  -  *`FG3_PCT_home`*
  -  *`AST_home`*
  -  *`REB_home`*
  -  *`FG_PCT_away`*
  -  *`FT_PCT_away`*
  -  *`FG3_PCT_away`*
  -  *`AST_away`*
  -  *`REB_away`*

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
  -  **Accuracy** = `83%`
  -  **Precision** = `86%`
  -  **Recall** = `86%`
  -  **Error** = `17%`<br/>

  - **Confusion Matrix**
  <p align="center">
    <img width="658" height="547" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/7b90e6f8-c281-43de-8a5f-6b7ef7e54c35" /><br/>
     Figure 1: Confusion matrix with 109 True Positive, 28 False Positive, 10 False Negative and 45 True Negative
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

  ***1. Strategic Feature Selection***

  By including features like FG_PCT_home, FT_PCT_home, and REB_home, the machine learning process aims to identify the underlying drivers of a win rather than just the outcome itself. This allows the model to generalize better to future games where only these stats might be estimated.

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
