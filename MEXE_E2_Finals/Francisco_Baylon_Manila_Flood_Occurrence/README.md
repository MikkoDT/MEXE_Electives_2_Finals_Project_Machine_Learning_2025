# 🌊 Flood Control Project: Flood Prediction (NCR, Philippines) — Logistic Regression 

![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

A simple Machine Learning model was developed to **predict flood occurrence (Yes/No)** using three environmental factors:
**Rainfall**, **Water Level**, and **Elevation**.  
The project is designed to be **easy to run and easy to explain**, using **Google Colab** as the main environment.

## 🎯 DISCLAMER
The model aims to predict:

- **FloodOccurrence = 1** → Flood is expected  
- **FloodOccurrence = 0** → No flood is expected  

This prediction is based only on and is limited to:
- **Rainfall (mm)**
- **Water Level (m)**
- **Elevation (m)**

---

## 👥 1) Pair Information
- **Pair Name:** SunEast Inc.
- **Members:** `Francisco`, `Baylon`
- **Topic:** Flood Prediction in NCR (Philippines)
- **Chosen Model:** **Logistic Regression** (Binary Classification)

---

## 🧾 2) Dataset Overview
- **Dataset file:** `data/cleaned_data.csv`
- **Target column:** `FloodOccurrence` (0/1)
- **Selected features:**

| Feature | Meaning | Unit |
|--------|---------|------|
| `Rainfall_mm` | Amount of rainfall | mm |
| `WaterLevel_m` | Measured water level | meters |
| `Elevation_m` | Area elevation | meters |

**Important note about the dataset:**  
Flood cases are typically **less frequent** than non-flood cases (class imbalance). Because of this, accuracy alone is not enough; the project focuses on metrics like **Recall** and **F1-score**.

---

## 🧹 3) Preprocessing Summary (What the notebook does)
A clean preprocessing workflow was applied to make training consistent and reliable:

### ✅ A. Feature Selection
Only the required columns were used:
- Inputs: `Rainfall_mm`, `WaterLevel_m`, `Elevation_m`
- Output: `FloodOccurrence`

### ✅ B. Data Quality Checks
The notebook checks for:

<img width="267" height="238" alt="image" src="https://github.com/user-attachments/assets/88793ff2-9b21-487d-9a53-867403244922" />
- Missing values 
- Invalid numeric values (e.g., negative rainfall)
- Correct numeric data types

### ✅ C. Feature Scaling (StandardScaler)
Because the inputs have different ranges (mm vs meters), the notebook applies:
- `StandardScaler()` to normalize feature scales  
This improves stability for Logistic Regression.

### ✅ D. Imbalance Handling
To improve flood detection (minority class), the model uses:
- `class_weight="balanced"`

This increases the importance of flood samples during training without requiring extra libraries.

### ✅ E. Train–Test Split
A stratified split is used:
- **80% training**
- **20% testing**
- `stratify=y` keeps flood/non-flood ratios consistent in both sets.

---

## 🤖 4) Model Description
### Logistic Regression (Binary Classification)
Logistic Regression is used because:
- The output is **two-class** (Flood vs No Flood)
- It can produce a **probability of flooding** (0–1)
- It is easy to interpret and present

The notebook implements a **pipeline** to ensure correct processing order:

> **StandardScaler → Logistic Regression (balanced)**

 Evaluation & Results
The model is evaluated using metrics suitable for imbalanced classification:

### Metrics Reported
- **Recall (Flood=1)** — measures how many real floods were correctly detected  
- **F1-score** — balances precision and recall
  <img width="583" height="455" alt="image" src="https://github.com/user-attachments/assets/7292f8c4-5925-44a5-ae65-ae4517f8dd4a" />
- **Confusion Matrix** — shows correct vs incorrect predictions  

### Outputs Included in Notebook
- Printed **classification report**
- Printed **F1-score and Recall**
- Displayed **confusion matrix plot**

> **Reminder for interpretation:**  
Why recal?
- Missing a flood (**False Negative**) is typically more critical than a false alarm (**False Positive**).  
That is why **Recall** is emphasized.

The notebook also features **threshold tuning**, where lowering the threshold increases flood probability (higher recall) but may increase false alarms.

---

## ▶️ 5) How to Run (Google Colab)
### Step 1 — Open the Notebook
Upload and open:
- `Flood_Control_Project.ipynb`

### Step 2 — Upload Dataset in Colab
In Colab:
- Left panel → **Files** → **Upload**
- Upload: `cleaned_data.csv`

### Step 3 — Run All Cells
- Click **Runtime → Run all**
- The notebook will train the model and display evaluation outputs.

✅ After running, the final cells can be used to test predictions with custom values.

---
