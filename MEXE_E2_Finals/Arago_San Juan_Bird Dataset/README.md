# 🐦 Final Assessment — Machine Learning Model

> **Bird Flight Capability Prediction using Logistic Regression**

---

## 👥 1. Pair Information
- **Pair Name:** Due2daydo2day  
- **Members:**  
  -  Arago, Allan Jhasper P.
  -  San Juan, John Christian C.
- **Topic:** Bird Flight Capability Classification  
- **Chosen Model:** 📈 Logistic Regression

---


## 📊 2. Dataset Overview
- **Dataset Source:**  https://springernature.figshare.com/articles/dataset/BIRDBASE_A_Global_Database_of_Avian_Biogeography_Conservation_Ecology_and_Life_History_Traits/27051040?file=55634729
- **Description:**  
  A biological dataset containing bird species information used to predict whether a bird is **flighted** or **flightless** based on physical and ecological characteristics.
- **Target Variable:**  
  🏷️ Flight Capability (`Flighted` / `Flightless`)
- **Features Used:**  
  - 🧬 `Genus`
  - ⚖️ `Average Mass`  
  - 🌍 `Primary Habitat`  
  - 🥗 `Primary Diet`  

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
- **Class Imbalance Handling:**  
  🔹 SMOTE (Synthetic Minority Over-sampling Technique)
- **Train–Test Split:**  
  🔹 Stratified split (80% training / 20% testing)  

  ---

## 🤖 4. Model & Results
- **Model Used:**  
  Logistic Regression 
- **Evaluation Metrics:**  
  - ✅ Accuracy = 99.18%
  - 🎯 Precision = 77.31%
  - 🔁 Recall =  88.33%
  - 📊 F1-Score = 81.87%
    
- **Visualizations:**  
  - Class distribution (Before & After SMOTE)  
  - Confusion Matrix  
  - ROC Curve  
  - Precision–Recall Curve  
  
- **Key Insights:**  
  - 
---

## ▶️ 5. How to Run
1. Install **VS Code**, **Python**, and the **Jupyter Notebook Extension**
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt

