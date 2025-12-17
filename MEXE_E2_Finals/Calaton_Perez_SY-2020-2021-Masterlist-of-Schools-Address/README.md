# 📑 Final Assessment — Machine Learning Model

## Project Overview
This project applies **Linear Regression** to school masterlist data to examine how different school-related factors relate to a target outcome. It is part of a final machine learning assessment and focuses on using data-driven analysis to understand patterns in educational datasets.

---

## 1. Pair Information
- **Pair Name:** Error 404: School Not Found 
- **Members:**
  -  Marco Calaton
  -  Megildo Perez  
- **Topic:** School  
- **Model Used:** Linear Regression  

---

## 2. Dataset Overview
- **Dataset Source:**  
  https://www.kaggle.com/datasets/bwandowando/deped-philippine-school-masterlist-2020-21  

- **Description:**  
  The dataset is based on the Department of Education (DepEd) Philippine School Masterlist for School Year 2020–2021. It contains structured school records and location details useful for educational data analysis.

- **Target Variable:**  
  Urban/Rural (encoded numerically)
  
  **Features Used**
  - Sector
  - Barangay
  - Legislative District

---

## 3. Data Preprocessing
The following preprocessing steps were applied before training the model:

1. **Data Loading**  
   The dataset was imported from a CSV file using Pandas to enable structured data handling and analysis.

2. **Data Cleaning**  
   Unnecessary spaces in column names were removed to ensure consistent and error-free referencing during data processing.

3. **Feature Selection (Data Reduction)**  
   Only relevant columns—**Barangay, Sector, Legislative District, and Urban/Rural**—were retained to reduce data complexity and focus the analysis on important features.

4. **Data Validation**  
   A validation check was performed to ensure that only existing columns were selected, preventing errors caused by missing or inconsistent data fields.

**- Visualization**

**Confusion Matrix**
<img width="660" height="541" alt="image" src="https://github.com/user-attachments/assets/d413d188-7e3d-48ba-8cf2-0c757e52a63a" />
- The confusion matrix compares true class labels (rows) with predicted class labels (columns).
- Correct predictions appear along the diagonal.
- The model never predicts class 0, as shown by the zero values in the first column.
- Most predictions are concentrated in class 1, indicating model bias toward the majority class.
- Class 1 has the highest correct classification count, suggesting it is the easiest class for the model to learn.
- Misclassifications occur mainly when class 0 and class 2 are predicted as class 1.

**Accuracy, Precision, Recall, F-1 Score**
<img width="566" height="431" alt="image" src="https://github.com/user-attachments/assets/be8676ac-a791-4bca-a1c7-b63179a87350" />
- Accuracy (~79%)
  - Overall, the model correctly predicts nearly 4 out of 5 samples.
- Precision (~72%)
  - Some predicted classes are incorrect, indicating false positives exist.
- Recall (~79%)
  - The model successfully identifies most actual instances.
- F1 Score (~73%)
  - Indicates a balanced trade-off between precision and recall.
 
**Feature Importance**
<img width="657" height="457" alt="image" src="https://github.com/user-attachments/assets/ba31f033-c4e4-4337-b4f0-20e5d08a554b" />

**ROC Curve**
<img width="701" height="544" alt="image" src="https://github.com/user-attachments/assets/ab641845-c1c3-4c1b-a0e9-5aaecb65ba94" />

---

## 4. Model & Results

### Evaluation Metrics
- **Accuracy** – Measures the overall percentage of correct predictions made by the model.  
- **Precision** – Shows how many schools predicted as **Urban** were actually Urban, helping reduce false positives.  
- **Recall** – Measures how many actual **Urban** schools were correctly identified by the model, helping reduce false negatives.  
- **F1-score** – Combines precision and recall into a single metric, useful when class distribution is imbalanced.  
- **ROC-AUC Score** – Evaluates how well the model distinguishes between Urban and Rural schools across different thresholds.

---

##  Insights
- **Model Performance:**  
  The model demonstrates acceptable performance in distinguishing between Urban and Rural schools, supported by consistent evaluation metrics and ROC curve behavior.

- **Feature Behavior:**  
  Location-related features such as legislative district and sector have a stronger influence on predictions compared to more granular attributes like barangay.

- **Interpretation of Results:**  
  The results suggest that school location patterns can be reasonably inferred from structured geographic and administrative data, although overlaps between classes still exist.

- **Limitations:**  
  Some misclassifications occur due to similarities in attributes between Urban and Rural schools, indicating that the current feature set may not fully capture all distinguishing factors.

- **Improvement Suggestions:**  
  Model performance could be improved by adding more features, applying feature engineering, or using more advanced machine learning models.

---

## 5. How to Run the Project

### Requirements
- VS Code  
- Python 3.x  
- Jupyter Notebook Extension  

### Installation
```bash
pip install -r requirements.txt

