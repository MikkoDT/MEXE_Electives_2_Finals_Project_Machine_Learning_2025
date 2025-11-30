# 📘 MEXE Electives 2 — Final Assessment: Machine Learning Model Development

## 🔹 Project Overview
For the Final Assessment, each pair (or individual) will build a Machine Learning Model using **Python in VS Code with Jupyter Notebook integration**.

You must create a notebook that applies **one (1)** of the following:
- **Linear Regression** (for numerical prediction), or  
- **Logistic Regression** (for classification)

Your chosen model must match your dataset and objective.

---

## 📅 Submission & Presentation Deadline
**December 14, 2025 (until 12:00 AM)**

Submit via this GitHub repository and prepare for your final presentation.

---

## 📂 Repository Structure
Each pair must submit a folder named:

<Pair1Surname><Pair2Surname><Topic>


Inside the folder:
MEXE_E2_Midterm/
│
<Pair1Surname>_<Pair2Surname>_<Topic>/
│
├── notebooks/
│   └── Topic_FinalModel_Pair1Surname_Pair2Surname.ipynb
│
├── data/
│   └── cleaned_data.csv   (from your midterm; or updated cleaned dataset)
│
├── README.md              # summary of your final model
│
└── requirements.txt       # list of Python libraries used


---

## 📝 Instructions

### **1. Choose Your Model**
Select one:

#### ✔️ Linear Regression
For predicting continuous values.

#### ✔️ Logistic Regression
For classification tasks (binary or multi-class).

Add in your README why this method fits your objective.

---

### **2. Create Your VS Code Notebook**

Your notebook must contain:

---

### **A. Dataset Loading**
- Load your cleaned dataset from the midterm.
- If re-cleaned, summarize changes.

---

### **B. Preprocessing**
- Handle missing values  
- Label encoding / One-hot encoding (if needed)  
- Feature scaling (`StandardScaler` recommended)  
- Train–test split  

Example:
```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=123)


---

## 📝 Instructions

### **1. Choose Your Model**
Select one:

#### ✔️ Linear Regression
For predicting continuous values.

#### ✔️ Logistic Regression
For classification tasks (binary or multi-class).

Add in your README why this method fits your objective.

---

### **2. Create Your VS Code Notebook**

Your notebook must contain:

---

### **A. Dataset Loading**
- Load your cleaned dataset from the midterm.
- If re-cleaned, summarize changes.

---

### **B. Preprocessing**
- Handle missing values  
- Label encoding / One-hot encoding (if needed)  
- Feature scaling (`StandardScaler` recommended)  
- Train–test split  

Example:
```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=123)

from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)

Logistic Regression Example

from sklearn.linear_model import LogisticRegression
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)

from sklearn.linear_model import LogisticRegression
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)

D. Model Evaluation
Linear Regression Metrics:

MAE

MSE / RMSE

R² Score

Logistic Regression Metrics:

Accuracy

Confusion Matrix

Precision, Recall, F1-score

(Optional) ROC Curve

E. Insights

Provide 3–5 insights, including:

Model performance

Feature behavior

Interpretation of results

Improvement suggestions

🔼 3. Upload to GitHub

Inside your folder:

Notebook → notebooks/

Dataset → data/

README → follow template below

requirements.txt → all imported Python libraries

🎤 4. Final Presentation

Duration: 4–7 minutes

Recommended flow:

Topic & Problem

Dataset Summary

Chosen Model & Rationale

Model Development

Evaluation Results

Discussion & Conclusion

📑 README Template (for student folders)

# Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name:
- Members:
- Topic:
- Chosen Model: Linear Regression / Logistic Regression

## 2. Dataset Overview
- Dataset Source:
- Description:
- Target Variable:
- Features Used:

## 3. Preprocessing Summary
- Encoding:
- Scaling:
- Cleaning steps:
- Train–test split:

## 4. Model & Results
- Model used:
- Metrics:
- Visualizations:
- Insights (3–5):

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells

🎯 Grading Criteria (100 pts)

| Category                       | Points |
| ------------------------------ | ------ |
| Model Development              | 30 pts |
| Evaluation & Interpretation    | 30 pts |
| Code Quality & Reproducibility | 20 pts |
| Documentation                  | 10 pts |
| Presentation                   | 10 pts |


