
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
  ▸ Since every feature chosen for the final model is numerical, the feature set did not need to be categorically encoded.
- **Scaling**  
  ▸ Standardization was applied to ensures that features with large ranges (like total points) do not overshadow features with small ranges (like shooting percentages) during model training.
- **Cleaning Steps**  
  ▸ Handling Missing Values: The notebook uses dataset.dropna(inplace=True) to remove any rows containing null values, ensuring the model only trains on complete game records. 
  ▸ Feature Selection (Dropping Irrelevant Data): Non-predictive columns such as GAME_DATE_EST, GAME_ID, and GAME_STATUS_TEXT are removed because they do not contribute to the mathematical prediction of a win.
  ▸ Target Variable Verification: A check is performed to ensure the HOME_TEAM_WINS column exists; if not, it is programmatically created by comparing PTS_home and PTS_away.
- **Train–Test Split**  
  ▸ The dataset was divided into training and testing sets, with 80% of the data used for training and 20% reserved for testing to evaluate performance on unseen data.

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

  ***2. Balanced Evaluation Using Multiple Metrics***

  Instead of relying on accuracy alone, the notebook evaluated the model using precision, recall, error rate, and a confusion matrix. The confusion matrix visualization highlights how well the model distinguishes between home and away wins, revealing areas where false positives or false negatives are more common.

  ***3. Importance of Game Statistics as Predictors***

  The analysis shows that game-related numerical features are influential in predicting the target variable. These features capture relative team strength and in-game dominance, which are crucial factors in determining whether the home team wins.

  ***4. Opportunities for Model Improvement***

  Although Logistic Regression performs well, investigating more complex machine learning models like Random Forests, Gradient Boosting Machines, or Neural Networks could potentially lead to even higher accuracy and robustness.
  
---

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

```bash

pip install -r requirements.txt
```
3. Open the `.ipynb` notebook
4. Run all cells
