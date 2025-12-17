# 🍔 Fast Food Nutrition Classification (Logistic Regression)

> **Final Assessment — Machine Learning Model**


![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)


## 👥 Pair Information
- **Pair Name:** Preservation
- **Members:** Brian Arce & Steven Cometa
- **Topic:** Fast Food Nutrition
- **Chosen Model:** Logistic Regression
  
## 📊 Dataset Overview
- **Dataset Source:** https://docs.google.com/spreadsheets/d/14nmCo1Dlg04W9tTWNxHQjAPslzLVzLh2QVAiwENjqhw/edit?usp=sharing
- **Description:**
This dataset contains fast food meals and their nutritional components. The goal is to classify meals as **healthy** or **not healthy** based on nutritional thresholds.


### 🎯 Target Variable
- `1` → Healthy meal
- `0` → Not healthy


### 🧩 Features Used
- Calories
- Fat
- Carbs
- Sugar
- Sodium
  
## 3. Preprocessing Summary
- Encoding: Categorical values were encoded into numerical form to ensure compatibility with the Logistic Regression model.
- Scaling: Numerical features were standardized to ensure all values were on a similar scale and to improve model convergence.
- Cleaning steps: The dataset was cleaned by renaming columns, checking for missing values, removed duplicated data, and ensuring consistent data types before training.
- Train–test split: The dataset was divided into training and testing sets to evaluate how well the model performs on unseen data.

## 4. Model & Results
- Model used: Logistic Regression was implemented as the classification model due to its simplicity, efficiency, and effectiveness in binary classification tasks.
- Metrics: The model was evaluated using accuracy, confusion matrix, and classification report to measure prediction performance.
- Visualizations:
  
<p align="center"> A count plot for the newly created column </p>
<p align="center">
<img width="900" alt="image" src="https://github.com/user-attachments/assets/fadfcf2e-7881-410d-96d9-d2d6b08ecdd2" />
</p>

---

<p align="center">
A confusion matrix visualization was generated to show the number of correct and incorrect predictions made by the model.
</p>
<p align="center">
<img width="500" alt="image" src="https://github.com/user-attachments/assets/6aa494dc-4959-421c-b763-8a1a04c62886" />
</p>

---

<p align="center"> A ROC curve to show the model's performance across the threshold </p>
<p align="center">
<img width="500" alt="image" src="https://github.com/user-attachments/assets/dfa13a14-b0ae-4eb2-8e76-e868c5300e3f" />
</p>


**Insights:**
- The model achieved good accuracy in classifying meals based on nutritional values.
- Calories, fat, sugar, and sodium had the strongest influence on predictions.
- Logistic Regression performed effectively despite its simplicity.
- Some misclassifications occurred due to overlapping nutritional ranges.
- The results show that machine learning can support basic health-related meal classification.

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells
