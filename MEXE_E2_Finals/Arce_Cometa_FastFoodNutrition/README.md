  # Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: Preservation
- Members: Brian Arce & Steven Cometa
- Topic: Fast Food Nutrition
- Chosen Model: Logistic Regression

## 2. Dataset Overview
- Dataset Source: https://docs.google.com/spreadsheets/d/14nmCo1Dlg04W9tTWNxHQjAPslzLVzLh2QVAiwENjqhw/edit?usp=sharing
- Description: The dataset focuses on fast food meals and their nutritional components with the goal of identifying healthy meal options. It includes key nutritional values such as calories, total fat, carbohydrates, sugars, protein, and sodium, which are commonly used to assess the nutritional quality of food.
- **Target Variable:**  
Binary label indicating meal healthiness:
- `1` → Healthy meal  
- `0` → Not healthy  
Classification is based on predefined nutritional thresholds.

- Features Used: The features used in the model include calories, total fat, carbohydrates, sugars, protein, and sodium.

## 3. Preprocessing Summary
- Encoding: Categorical values were encoded into numerical form to ensure compatibility with the Logistic Regression model.
- Scaling: Numerical features were standardized to ensure all values were on a similar scale and to improve model convergence.
- Cleaning steps: The dataset was cleaned by renaming columns, checking for missing values, and ensuring consistent data types before training.
- Train–test split: The dataset was divided into training and testing sets to evaluate how well the model performs on unseen data.

## 4. Model & Results
- Model used: Logistic Regression was implemented as the classification model due to its simplicity, efficiency, and effectiveness in binary classification tasks.
- Metrics: The model was evaluated using accuracy, confusion matrix, and classification report to measure prediction performance.
- Visualizations: A confusion matrix visualization was generated to show the number of correct and incorrect predictions made by the model.
<img width="900" alt="image" src="https://github.com/user-attachments/assets/fadfcf2e-7881-410d-96d9-d2d6b08ecdd2" />

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
