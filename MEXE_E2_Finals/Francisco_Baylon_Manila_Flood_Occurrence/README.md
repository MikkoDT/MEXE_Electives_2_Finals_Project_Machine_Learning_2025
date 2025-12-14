# 🌊 Flood Prediction (NCR, Philippines) — Logistic Regression Classifier

![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

This repository presents a **machine learning classification model** that predicts **flood occurrence** using three environmental indicators: **rainfall (mm)**, **water level (m)**, and **elevation (m)**. The project is implemented in **Python** using a reproducible notebook workflow and standard evaluation metrics suitable for imbalanced flood datasets.

---

## 📌 Table of Contents
- [1. Pair Information](#1-pair-information)
- [2. Dataset Overview](#2-dataset-overview)
- [3. Preprocessing Summary](#3-preprocessing-summary)
- [4. Model & Results](#4-model--results)
- [5. How to Run](#5-how-to-run)

---

## 1. Pair Information
- **Pair Name:** `<Pair Name>`
- **Members:** `<Member 1>`, `<Member 2>`
- **Topic:** Flood Prediction (NCR, Philippines)
- **Chosen Model:** Logistic Regression (Binary Classification)

---

## 2. Dataset Overview
- **Dataset Source:** `Flood_Prediction_NCR_Philippines.csv` *(provided/collected dataset)*
- **Description:** The dataset contains environmental measurements used to classify whether a flood event occurs.
- **Target Variable:** `FloodOccurrence`  
  - `0` = No Flood  
  - `1` = Flood
- **Features Used (Inputs):**
  - `Rainfall_mm` — rainfall in millimeters
  - `WaterLevel_m` — water level in meters
  - `Elevation_m` — elevation in meters

> **Scope Note:** Only the three listed features were used to maintain a focused and interpretable flood prediction model.

---

## 3. Preprocessing Summary
The dataset was prepared using a minimal but effective preprocessing workflow designed for classification with uneven class distribution.

- **Feature Selection:** Only `Rainfall_mm`, `WaterLevel_m`, and `Elevation_m` were retained as predictors.
- **Missing/Invalid Value Handling:** The dataset was checked for missing values and invalid entries; any required treatment is documented inside the notebook.
- **Scaling:** `StandardScaler` was applied to normalize feature scales, improving stability for Logistic Regression.
- **Class Imbalance Handling:** `class_weight="balanced"` was used to reduce bias toward the majority (non-flood) class.
- **Train–Test Split:** 80% training / 20% testing using **stratified splitting** to preserve the flood ratio across sets.

---

## 4. Model & Results
### Model Used
- **Logistic Regression** (binary classifier) with:
  - standardized inputs (scaling)
  - imbalance compensation (`class_weight="balanced"`)

### Evaluation Metrics
To ensure meaningful performance interpretation on imbalanced data, the following were used:
- **F1-score**
- **Recall**
- **Confusion Matrix**

### Results Summary (Fill-in after running)
- **F1-score:** `__`
- **Recall:** `__`

### Insights (3–5)
1. The model treats flood prediction as a **classification task**, producing a probability that is mapped to a flood/no-flood decision.
2. Because flood events are typically rare, **imbalance handling** is necessary to prevent the model from over-predicting the “No Flood” class.
3. **Feature scaling** improves numerical stability and supports consistent model convergence.
4. **Recall** is emphasized because failing to detect a true flood case is generally more critical than producing a false alarm.
5. The decision **threshold** may be adjusted (e.g., below 0.50) if higher sensitivity is needed for warning scenarios.

---

## 5. How to Run
### A. Environment Setup
1. Install **Python 3.x**
2. Clone/download this repository
3. Install dependencies:

   ```bash
   pip install -r requirements.txt

