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

---

## :three: 💻 Preprocessing Summary
### 📟 Encoding
<p align="justify"> No feature encoding was applied during preprocessing because the model only used numerical nutritional features. Categorical variables were excluded from the input features, and the target labels were handled directly by the classifier.

### ⚖️ Scaling
All numeric features were standardized using StandardScaler, converting them to:
- `Mean = 0`
- `Standard deviation = 1`
<p align="justify"> This step is essential for machine learning models, such as Logistic Regression, to ensure features are treated equally, regardless of their units.

### 🧹 Cleaning Steps
1. **Handling Missing Values**
  - To ensure clean and consistent data, missing values were addressed using two approaches:
    - Numeric features (e.g., calories, protein, fat, sodium): Filled with the mean of each column.
    - Categorical features (e.g., food item, category, meal type): Filled with the mode of each column.
  - This prevents model errors and keeps the dataset statistically stable.

2. **Feature Engineering**
  - New useful variables were created to capture dietary patterns better:
    - `Total_kcal_macros` - A calculated value representing total calories from macros: `Protein*4 + Carbs*4 + Fat*9`
  - Macronutrient ratios
    - Percentage of total calories coming from each macronutrient:
      - `Protein_pct`
      - `Carbs_pct`
      - `Fat_pct`

  - These help the model understand the “nutritional profile” of meals.

  - `Rule_Meal_Type` - A rule‑based classifier that assigns a meal type (Breakfast, Lunch, Dinner, Snack) based on ranges of macros and calories.

3. **Data Filtering**
  - <p align="justify"> To improve the quality of the training data, rows labeled `Unknown` by the rule-based classifier were removed. These items did not match any meal-type nutritional pattern and would introduce noise. The final dataset used for training only includes items with clear, rule‑based meal classifications.

### 🏋️ Train-Test Split
  - The processed dataset was divided into:
    - `80% Training set`
    - `20% Testing set`

  - <p align="justify"> With stratification, meaning the distribution of meal types is preserved in both sets. This ensures fair and balanced evaluation of the model’s performance.

---

## 4️⃣ 🤖 Model and Test Results
### 🦾 Model Used
- **Logistic Regression**
  - <p align="justify">  This model was selected because it is well‑suited for multi‑class classification using numerical features, provides interpretable results, and performs reliably even when class boundaries overlap.

### 📊 Metrics
- `Accuracy = 81.2603648424544%`
- `Precision = 81.06743264352367%`
- `Recall: 81.2603648424544%`
- `F1-score: 81.12784415735238%`

<p align="center"> <img width="702" height="547" alt="image" src="https://github.com/user-attachments/assets/9eaaa9e3-f9b1-4179-977c-44e10153530d" />

### 👀 Visualizations
1. **Confusion Matrix**
<p align="center"> <img width="539" height="434" alt="image" src="https://github.com/user-attachments/assets/e84937cc-1e3a-430b-8b4f-9a7a032515a0" />
<p align="center"> The model classifies snacks and breakfasts well, but has difficulty distinguishing lunch and dinner due to overlapping nutritional features. This shows that meals with similar calorie and macronutrient profiles are harder to separate using nutrition data alone.

2. **Correlation Heatmap**
<p align="center"> <img width="1021" height="795" alt="image" src="https://github.com/user-attachments/assets/7b806f16-48ff-4441-a1c1-8a5950769163" />
<p align="center"> The correlation heatmap shows that the strongest relationships occur among the macronutrients and the total calorie count. Total_kcal_macros is highly correlated with carbohydrates (0.79) and fat (0.87), indicating that these nutrients contribute most to overall energy intake. Meanwhile, protein shows a moderate correlation with calories (0.32). Macronutrient ratios (Protein_pct, Carbs_pct, Fat_pct) show negative correlations with each other, which is expected because the percentages must sum to 100%. Nutrients such as sodium, fiber, sugars, and cholesterol have close‑to‑zero correlations with most features, meaning they vary independently and do not help distinguish meal types. This supports why the rule‑based classifier performs better when using macronutrient-based features.

3. **Box Plot**
<p align="center"> <img width="691" height="528" alt="image" src="https://github.com/user-attachments/assets/2e61c3b9-ccaa-4fbe-93c1-da00c64cc2b8" />
<p align="center"> The boxplot of macronutrient ratios reveals that carbohydrates contribute the largest proportion of calories across most foods (median ≈ 45%), followed by fat (≈ 33%) and protein (≈ 20%). Protein ratios show the least variability, while carbohydrates display the widest range
