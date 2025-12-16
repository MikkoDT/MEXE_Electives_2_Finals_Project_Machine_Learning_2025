<h2 align="center">Machine Learning Model</h2>
<hr>

## 1. Group Information
- **Group Name:**
  - Ha? Halaman
- **Members:**
  - Capuno, Raphael Juno
  - Del Rio, Francine Faith
- **Topic:**
  - Crop Recommendation Dataset
- **Chosen Model:**
  - Logistic Regression

## 2. Dataset Overview
- **Dataset Source:** https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset
  
- **Description:** The Crop Recommendation Dataset is an agricultural dataset that is used for crop categorization and recommendation using machine learning. The dataset's numerical features, which indicate environmental factors and soil nutrient composition, are used to forecast which crop would be best to grow in a particular setting. The crop type, which is label-encoded for use in supervised machine learning methods, is the target variable.
  
- **Target Variables:**
  - Label (recommended crop) - The recommended crop type based on the specified input parameters. In order to facilitate classification using machine learning models like Logistic Regression, this categorical variable is label-encoded into numerical form.
    
- **Features Used:**
  - N - ratio of Nitrogen content in soil
  - P - ratio of Phosphorous content in soil
  - K - ratio of Potassium content in soil
  - temperature - temperature in degree Celsius
  - humidity - relative humidity in %
  - pH - ph value of the soil
  - rainfall - rainfall in mm

## 3. Preprocessing Summary
  - **Encoding:**
    - Since the target variable (crop label) was categorical, Label Encoding was used to transform it into numerical form. The original label column was converted into a new column called label_encoded, in which each crop type was assigned a distinct integer value. The Logistic Regression model was able to process the class labels efficiently because to this encoding.
      
  - **Scaling:**
     - StandardScaler was used to standardize the independent numerical features, including temperature, humidity, pH, rainfall, N, P, and K. Because logistic regression is sensitive to changes in feature magnitude and scale, this step changed each feature to have a mean of zero and a standard deviation of one.
       
  - **Cleaning steps:**
     - The dataset was checked for invalid entries, duplicates, and missing values before modeling. The absence of missing data was verified with a null-value check. To evaluate feature distributions and identify outliers, descriptive statistics and visual inspection were employed. No rows were eliminated because the values remained within acceptable ranges, ensuring the dataset's authenticity and validity.
       
  - **Train–test split:**
     - An 80%–20% ratio was used to divide the cleaned and scaled dataset into training and testing sets. To ensure that the results could be repeated, the random_state option was fixed. Prior to splitting, feature variables (X) and the encoded target variable (y) were kept apart, enabling appropriate model training and objective performance assessment on unseen data.

## 4. Model and Results
- **Model used:**
    - Logistic Regression was chosen because the problem requires multi-class classification—predicting a specific crop label—which is the model's primary function. It is a simple, computationally efficient algorithm, making it ideal for use as an initial baseline model to quickly assess data predictability. This approach allows developers to confirm if a fast, linear solution is sufficient before committing to more complex, resource-intensive methods.

- **Metrics:**
    - Accuracy: Reported as 0.9539 or 95.39%.
    - Precision (Micro/Macro-average): Reported as 0.9569.
    - Recall (Micro/Macro-average): Reported as 0.9539.
    - F1-score (Micro/Macro-average): Reported as 0.9543.
    - Area Under the Curve (AUC): The Micro-average for the multiclass ROC Curve is reported as 0.99941.
    - Confusion Matrix: A confusion matrix was generated and used for visualization and assessment of class-specific errors.
  
- **Visualization:**
    - **Correlation Heatmap**
      This visualization shows that the Correlation Heatmap displays the pairwise linear relationships between the numerical features ($\text{N, P, K, temperature, humidity, pH, and rainfall}$). It uses a color gradient to represent the correlation coefficient, making it easy to see which feature pairs are positively, negatively, or weakly related.

    - 
- **Insights:**

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:
pip install -r requirements.txt
3. Open the `.ipynb` notebook
4. Run all cells

