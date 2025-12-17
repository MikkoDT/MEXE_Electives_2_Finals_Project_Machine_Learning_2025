# 🍛 Final Assessment - Machine Learning Model
## :one: 👥 Pair Information
- **Pair Name:** NutriGPT
- **Members:**
  - Earl Yuan L. Balabag
  - Nina Mika C. Espina
- **Topic:** Macronutrient-Based Meal Classification  
- **Chosen Model:** Logistic Regression
---
## :two: 📖 Dataset Overview
- **Dataset Source:** https://www.kaggle.com/datasets/adilshamim8/daily-food-and-nutrition-dataset
- **Description:**
  - <p align="justify">The dataset contains nutritional information of various food items, with each row representing a single food entry. It includes both raw nutrient values (grams, milligrams, calories) and derived macronutrient ratios (percentage of calories coming from protein, carbohydrates, and fat). The goal of the dataset is to analyze nutrient patterns and classify foods into meal types (Breakfast, Lunch, Dinner, Snack) based on nutritional composition.
- **Target Variable:** `Meal_Type`
  - 🥓`Breakfast`
  - 🍔`Lunch`
  - 🍫`Snacks`
  - 🍲`Dinner`
- **Features Used:** `Macronutrients`
  - **Numerical Features:**
    - `Calories (kcal)`
    - `Carbohydrates (g)`
    - `Protein (g)`
    - `Fat (g)`
    - `Sugars (g)`
    - `Sodium (mg)`
    - `Fiber (g)`
    - `Cholesterol (mg)`
  - **Engineered Features:**
    - `Protein_pct` = *percentage of total calories coming from protein*
    - `Carbs_pct` = *percentage of total calories coming from carbohydrates*
    - `Fat_pct` = *percentage of total calories coming from fat*
## :three: 💻 Preprocessing Summary
### 1. Handling Missing Values

- To ensure clean and consistent data, missing values were addressed using two approaches:
  - Numeric features (e.g., calories, protein, fat, sodium): Filled with the mean of each column.
  - Categorical features (e.g., food item, category, meal type): Filled with the mode of each column.
- This prevents model errors and keeps the dataset statistically stable.
### 2. Feature Engineering
- New useful variables were created to capture dietary patterns better:
  - `Total_kcal_macros` - A calculated value representing total calories from macros: `Protein*4 + Carbs*4 + Fat*9`
- Macronutrient ratios
  - Percentage of total calories coming from each macronutrient:
    - `Protein_pct`
    - `Carbs_pct`
    - `Fat_pct`

These help the model understand the “nutritional profile” of meals.

- `Rule_Meal_Type` - A rule‑based classifier that assigns a meal type (Breakfast, Lunch, Dinner, Snack) based on ranges of macros and calories.
### 3. 


