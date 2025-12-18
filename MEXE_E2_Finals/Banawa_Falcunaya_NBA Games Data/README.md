
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
    <strong>The NBA Games dataset</strong> is a collection of historical National Basketball Association (NBA) data covering seasons from 2004 up through around 2020. It’s designed for analytics, machine learning, and exploration of NBA game results, player stats, team info, and rankings.
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
  - Since every feature chosen for the final model is numerical, the feature set did not need to be categorically encoded.
- **Scaling**  
  - Standardization was applied to ensures that features with large ranges (like total points) do not overshadow features with small ranges (like shooting percentages) during model training.
- **Cleaning Steps**  
  - Handling Missing Values: Removes rows with null data so the model trains only on complete and reliable game records, preventing errors and inaccurate learning caused by incomplete statistics. 
  - Feature Selection: Eliminates irrelevant columns such as IDs, dates, and text fields to reduce noise and ensure the model focuses only on meaningful numerical features that influence game outcomes.
  - Target Variable Verification: Defines or verifies the outcome being predicted by ensuring the HOME_TEAM_WINS column exists, creating it from home and away team scores if necessary so the model has a correct label for supervised learning.
- **Train–Test Split**  
  - The dataset was divided into training and testing sets, with 80% of the data used for training and 20% reserved for testing to evaluate performance on unseen data.

</div>

---

##  4. Model & Results
- **Model Used:**  Logistic Regression 
- **Metrics:**  
  -  **Accuracy** = `83%`
  -  **Precision** = `86%`
  -  **Recall** = `86%`
  -  **Error** = `17%`<br/>


- **Visualizations:**  
**Confusion Matrix**
  <p align="center">
    <img width="658" height="547" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/7b90e6f8-c281-43de-8a5f-6b7ef7e54c35" /><br/>
     Figure 1: Confusion matrix with 1717 True Negative, 457 False Positive, 430 False Negative and 2707 True positive
 <p/>

**Correlation Heatmap**
  <p align="center">
    <img width="869" height="775" alt="Correlation Heatmap" src="https://github.com/user-attachments/assets/48874e8b-6bdb-44a7-9763-29193dee8c8d" /><br/>
     Figure 2: This heatmap provides valuable insights into how different performance metrics for home and away teams influence each other.
 <p/>

**Correlation Heatmap**
  <p align="center">
    <img width="1589" height="989" alt="Box plot" src="https://github.com/user-attachments/assets/3677a86f-91be-47a8-99db-0d64d9793239" /><br/>
     Figure 3: This heatmap provides valuable insights into how different performance metrics for home and away teams influence each other.
 <p/>



 
  
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
