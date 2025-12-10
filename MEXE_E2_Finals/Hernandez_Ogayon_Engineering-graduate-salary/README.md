# Final Assessment — Machine Learning Model

### 1. Group Information
Members:
- Hernandez, Jhonas R.
- Ogayon, Neil John

Topic: **Engineering Graduate Salary**  
Chosen Model: **Logistic Regression**

---

### 2. Dataset Overview

**Dataset Source:**  
https://docs.google.com/spreadsheets/d/1eUE6iiKm10bQzOcxsAPgzdmn3Gol80OASiSlJO1egME/edit?gid=814979604#gid=814979604

**Description:**  
This dataset contains academic background, technical skills, cognitive scores, personality traits, and employment-related variables of engineering graduates. It was cleaned and processed for machine learning to predict the College Tier using Logistic Regression.

**Target Variable:**
- CollegeTier  
  - 1 = Tier 1 College  
  - 2 = Tier 2 College  

**Features Used:**
- Gender  
- 10percentage  
- 12graduation  
- 12percentage  
- CollegeID  
- collegeGPA  
- CollegeCityID  
- CollegeCityTier  
- GraduationYear  
- English  
- Logical  
- Quant  
- Domain  
- ComputerProgramming  
- ElectronicsAndSemicon  
- ComputerScience  
- MechanicalEngg  
- ElectricalEngg  
- TelecomEngg  
- CivilEngg  
- conscientiousness  
- agreeableness  
- extraversion  
- nueroticism  
- openess_to_experience  

---

### 3. Preprocessing Summary

**Encoding:**
- Gender was encoded into numerical values.
- All categorical columns were converted into numeric format.

**Scaling:**
- All features were standardized using StandardScaler.

**Cleaning Steps:**
- Removed duplicate rows.
- Dropped irrelevant and text-based columns.
- Ensured all remaining columns were numeric.
- Verified that there were no missing values.
- Exported cleaned dataset as `cleaned_college_tier_dataset.csv`.

**Train–test split:**  
- 80% Training Data  
- 20% Testing Data  

---

### 4. Model And Result

### Model Used:
**Logistic Regression**

---

### Metrics:
- **Accuracy:** 92.33%
- **Confusion Matrix:**
  [[ 4 42]
  [ 4 550]]

---

### Visualization:

- **Confusion Matrix (Heatmap)**  
<img width="516" height="467" alt="image" src="https://github.com/user-attachments/assets/1001afb2-8888-4550-b748-b0c7c7ebbc59" />

The confusion matrix shows the prediction performance of the Logistic Regression model.

- **True Positives (550):** Correctly predicted Tier 2
- **True Negatives (4):** Correctly predicted Tier 1
- **False Positives (42):** Predicted Tier 2 but actually Tier 1
- **False Negatives (4):** Predicted Tier 1 but actually Tier 2


- **ROC Curve (Receiver Operating Characteristic Curve)**  
<img width="535" height="468" alt="image" src="https://github.com/user-attachments/assets/5cc57b26-0e8c-40d5-bf22-581dec068152" />

The ROC curve illustrates the model’s ability to distinguish between Tier 1 and Tier 2.

- Shows the relationship between **True Positive Rate** and **False Positive Rate**
- The model achieved an **AUC score of 0.791**


---

### Insights:

#### Model Performance
- The model achieved high overall accuracy (92.33%).  
- Performs strongly when predicting Tier 2 colleges due to a large number of examples.

#### Error Analysis
- Confusion matrix shows misclassification mostly occurs in Tier 1 due to class imbalance.  
- Logistic Regression still maintains stable decision boundaries even with uneven classes.

#### Trends Observed
- Technical skills (e.g., ComputerProgramming, Domain) and cognitive scores (English, Logical, Quant) contribute significantly.  
- Personality traits also show moderate influence.  
- Model predictions follow expected trends with no extreme outliers.
