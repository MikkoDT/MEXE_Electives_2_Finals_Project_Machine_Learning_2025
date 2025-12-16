# 🐦 Final Assessment — Machine Learning Model

> **Bird Flight Capability Prediction using Logistic Regression**

---

## 👥 1. Pair Information
- **Pair Name:**  
- **Members:**  
  -  Arago, 
  -  San Juan, John Christian C.
- **Topic:** Bird Flight Capability Classification  
- **Chosen Model:** 📈 Logistic Regression (Binary Classification)

---


## 📊 2. Dataset Overview
- **Dataset Source:**  
- **Description:**  
  A biological dataset containing bird species information used to predict whether a bird is **flighted** or **flightless** based on physical and ecological characteristics.
- **Target Variable:**  
  🏷️ Flight Capability (`Flighted` / `Flightless`)
- **Features Used:**  
  - 🧬 Genus  
  - ⚖️ Average Mass  
  - 🌍 Primary Habitat  
  - 🥗 Primary Diet  

---

## 🧹 3. Preprocessing Summary
- **Encoding:**  
  🔹 One-Hot Encoding for categorical features  
- **Scaling:**  
  🔹 Not applied (logistic regression with one-hot encoded features)  
- **Cleaning Steps:**  
  - Removed irrelevant columns  
  - Handled missing values using median imputation  
  - Merged *partial flight* with *flightless* due to class sparsity  
- **Train–Test Split:**  
  🔹 Stratified split (80% training / 20% testing)  
- **Class Imbalance Handling:**  
  🔹 SMOTE (Synthetic Minority Over-sampling Technique)

