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
  - ✅ Accuracy = `99.18%`
  - 🎯 Precision = `77.31%`
  - 🔁 Recall =  `88.33%`
  - 📊 F1-Score = `81.87%`
    
- **Visualizations:**  
  - Class distribution (Before & After SMOTE)  
  - Confusion Matrix  
  - ROC Curve  
  - Precision–Recall Curve  
  
- **Key Insights:**  
  ## Key Insights and Design Decisions

During the development of the Machine Learning model, several important considerations were identified to improve model stability, interpretability, and overall performance:

- **Class Merging for Stability**  
  Due to the extremely small number of *partially flightless* bird samples, this category was merged with the *flightless* class. The original multiclass formulation led to unstable learning behavior and unreliable evaluation metrics. Merging the classes reduced class sparsity, improved model stability, and preserved biological interpretability, resulting in a more reliable **Macro F1-score**.

- **Use of One-Hot Encoding for Categorical Features**  
  One-Hot Encoding was applied instead of Label Encoding because the categorical variables are nominal in nature. Label Encoding would have introduced artificial ordinal relationships that could mislead the logistic regression model. One-Hot Encoding preserves category independence, enables meaningful coefficient interpretation, and contributed to improved **Macro F1-score** and model stability.

- **Handling Class Imbalance with SMOTE**  
  SMOTE (Synthetic Minority Over-sampling Technique) was used to address severe class imbalance in the bird flight dataset. Without resampling, the model was biased toward the dominant *flighted* class, resulting in misleadingly high accuracy but poor recall for minority classes. SMOTE synthetically increased the number of *flightless* samples, allowing the model to learn more balanced decision boundaries and significantly improving the **Macro F1-score**.

---

 ## 6.1 Model Performance

The overall evaluation results indicate that the model demonstrates strong, stable, and reliable performance in handling the classification task. The combination of balanced data, accurate predictions, and meaningful evaluation metrics suggests that the model has effectively learned the underlying patterns in the dataset and is capable of making informed decisions rather than random guesses.

- **Class Distribution (Before and After Balancing):**  
  The balanced class distribution shows that the model was trained on equally represented classes, which reduces bias toward the majority class. This allows the model to better learn features from the minority class, contributing to more fair and consistent predictions.

- **Confusion Matrix:**  
  The high number of correct predictions, especially for the majority class, indicates strong accuracy. At the same time, the relatively low number of false positives and false negatives shows that the model maintains good control over misclassification errors.

- **ROC Curve and AUC:**  
  The strong separation between classes across different thresholds reflects the model’s ability to clearly distinguish between positive and negative outcomes. A high AUC value supports the claim that the model performs significantly better than random classification.

- **Precision–Recall Curve and Average Precision (AP):**  
  The precision–recall behavior highlights the model’s effectiveness in detecting minority cases while managing false positives. An AP value around 0.71 suggests a good balance between correctly identifying positive cases and maintaining prediction reliability.

Overall, these supporting results reinforce the insight that the model is well-trained, robust, and suitable for the problem, with room for further improvement in minority class detection.

---

## 6.2 Feature Behavior

The behavior of the selected features indicates that they contribute effectively to the model’s ability to learn meaningful patterns rather than introducing noise. The strong class separation observed suggests that these features contain sufficient and relevant information to support accurate predictions. Stable performance across evaluation metrics also implies that no single feature disproportionately influences the model, allowing it to generalize well. Even after data balancing, the features remain informative, further supporting consistent and reliable model performance.

- **Genus:**  
  Provides categorical biological context that helps the model group organisms with similar characteristics, improving class differentiation.

- **Average Mass:**  
  Adds numerical information that supports separation based on size-related patterns, helping distinguish organisms with different physical traits.

- **Primary Diet:**  
  Contributes behavioral and ecological insights by associating feeding habits with specific classifications.

- **Primary Habitat:**  
  Supplies environmental context that reinforces distinctions based on typical living conditions and ecological niches.

Together, these features complement one another by combining biological, physical, behavioral, and environmental information, enabling the model to make well-informed and reliable predictions.

---

## 6.3 Interpretation of Results

The results gathered from the evaluation indicate that the model demonstrates strong and consistent performance across multiple evaluation measures. The preprocessing steps and balanced training data allowed the model to learn meaningful patterns, leading to accurate predictions and reliable class separation. The evaluation plots collectively show that the model does not rely on chance and is capable of handling both majority and minority classes effectively.

- **Class Distribution (Before and After Balancing):**  
  This graph illustrates the number of samples in each class before and after applying the balancing technique. Initially, the majority class significantly outnumbers the minority class, which could bias predictions. After balancing, both classes have nearly equal sample counts, improving fairness and learning stability.

- **Confusion Matrix:**  
  The matrix compares actual versus predicted class labels. High values along the main diagonal represent correct predictions, while the relatively low off-diagonal values indicate few misclassifications such as false positives and false negatives.

- **ROC Curve and AUC:**  
  The ROC curve plots the true positive rate against the false positive rate across different thresholds. The curve staying well above the diagonal line indicates strong class separation, and a high AUC value reflects strong overall discrimination capability.

- **Precision–Recall Curve and Average Precision (AP):**  
  This curve focuses on performance for the positive (minority) class. Precision measures prediction accuracy for positive cases, while recall measures how many actual positives are detected. An AP value around 0.71 indicates a good balance between accuracy and coverage of the positive class.

Overall, these results indicate that the model is well-trained, balanced, and capable of producing accurate and reliable predictions, with remaining opportunities for improvement mainly focused on enhancing minority class detection.

---

## 6.4 Improvement Suggestions

The evaluation results suggest that although the model already achieves strong and reliable performance, there are clear opportunities for further improvement to enhance accuracy and robustness. A closer examination highlights areas where targeted adjustments could improve generalization and yield more precise predictions, particularly for less frequent cases.

- **Increase Dataset Size:**  
  Expanding the dataset, especially by collecting more real samples for the minority class, would help the model learn more representative patterns and reduce dependence on synthetically generated data.

- **Feature Engineering and Selection:**  
  Refining existing features or introducing new meaningful features, such as grouping similar diets or habitats, can help capture deeper relationships within the data and improve predictive accuracy.

- **Model Tuning:**  
  Fine-tuning hyperparameters and experimenting with alternative algorithms may further improve performance, particularly in reducing false negatives and improving minority class detection.

- **Threshold Optimization:**  
  Adjusting the classification threshold instead of relying on the default setting can help better balance precision and recall, depending on whether false positives or false negatives are more critical.

- **Cross-Validation:**  
  Implementing k-fold cross-validation provides a more robust estimate of model performance and reduces the risk of overfitting to a single train–test split, leading to more stable and trustworthy results.



---

## ▶️ 5. How to Run
1. Install **VS Code**, **Python**, and the **Jupyter Notebook Extension**
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt

