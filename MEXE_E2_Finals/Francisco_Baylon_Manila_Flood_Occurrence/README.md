# Flood Prediction in NCR (Philippines) using Logistic Regression

## Overview
This repository presents a **simple machine learning-based flood prediction system** that classifies whether flooding will occur (**0 = No Flood, 1 = Flood**) using three environmental predictors: **Rainfall (mm)**, **Water Level (m)**, and **Elevation (m)**. The work is designed to be **clear, reproducible, and suitable for academic demonstration**, with implementation intended for **Google Colab**.

---

## Objectives
The project aims to:
1. Prepare a clean and minimal dataset for flood prediction using selected numerical features.
2. Build a **preprocessing + modeling pipeline** suitable for classification tasks with imbalanced data.
3. Train a **Logistic Regression** classifier and assess performance using **F1-score, Recall, and Confusion Matrix**.
4. Provide a straightforward function that predicts flood risk for **new input values**.

---

## Dataset Summary
- **File name (expected):** `Flood_Prediction_NCR_Philippines.csv` (or `cleaned_data.csv` if a cleaned version is used)
- **Target variable:** `FloodOccurrence`  
  - `0` → No Flood  
  - `1` → Flood  
- **Features used (inputs):**
  - `Rainfall_mm`
  - `WaterLevel_m`
  - `Elevation_m`

> Note: Flood occurrences are typically **rare**, which introduces **class imbalance**. For this reason, the model is trained with imbalance-aware settings and is evaluated using appropriate metrics beyond accuracy.

---

## Methodology
### 1) Preprocessing
The notebook implements a structured preprocessing workflow:
- **Feature selection**: only the required numerical predictors are retained.
- **Data validation**: missing or invalid values are checked (and handled if present).
- **Scaling**: `StandardScaler` is applied to normalize feature magnitudes, improving Logistic Regression stability.

### 2) Imbalance Handling
To address the low frequency of flood events, the model uses:
- `class_weight="balanced"`  
This approach increases the importance of minority-class samples during training without requiring external oversampling libraries.

### 3) Model Training
- **Model**: Logistic Regression (binary classification)
- **Train–test split**: 80% training / 20% testing
- **Split strategy**: stratified sampling to preserve class ratios across sets

### 4) Evaluation
The model is evaluated using:
- **Recall** (priority metric for flood detection; emphasizes minimizing missed floods)
- **F1-score** (balances precision and recall under class imbalance)
- **Confusion Matrix** (visual and numerical interpretation of correct vs. incorrect classifications)

### 5) Prediction Utility
A helper function is included to:
- accept new input values (rainfall, water level, elevation),
- return **flood probability** and **final class decision** based on a configurable threshold.

---

## Repository Structure
A recommended structure is shown below for clarity and clean organization:

