# Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: Plantitoes 
- Members: de Gracia & Pasicaran
- Topic: Plants
- Chosen Model: Logistic Regression

## 2. Dataset Overview
- **Dataset Source:** 
	The dataset was sourced from the file plant_disease_dataset.csv included in the Final Project Electives 2 materials. It contains simulated environmental measurements used for building a classification model for plant disease detection.
- Description: 
The dataset consists of 10,000 records and 5 columns, representing various environmental conditions that influence plant health. It includes continuous numerical variables such as temperature, humidity, rainfall, and soil pH, along with a binary label indicating presence or absence of plant disease. The dataset contains no missing values, making it suitable for direct preprocessing and model training.
- Target Variable:
The target variable is disease, a binary categorical label where:

		0 = Healthy plant

		1 = Diseased plant

- Features Used:
The Logistic Regression model was trained using four numerical environmental variables:

	Temperature – measures ambient temperature (°C)

	Humidity – percentage of air moisture

	Rainfall – rainfall intensity (mm)

	Soil_pH – acidity or alkalinity level of soil

These features serve as predictors for classifying plant health conditions.

## 3. Preprocessing Summary
- Encoding:
No categorical encoding was required because all features (temperature, humidity, rainfall, soil pH) and the target variable (disease) were already in numerical form.
- Scaling:
A StandardScaler was applied to the feature set to normalize the values.
X_train was fit and transformed
X_test was transformed only
This ensured that all features had a mean of 0 and standard deviation of 1, improving model performance and stability.
- Cleaning steps:
Checked for missing values, none were found.
Verified dataset shape and descriptive statistics for consistency.
No additional cleaning, imputation, or outlier removal was required.
- Train–test split:
The dataset was split into:
80% training data (8,000 samples)
20% testing data (2,000 samples)
using train_test_split with a fixed random_state=123 for reproducibility.

## 4. Model & Results
- Model used:
The study utilized a Logistic Regression model to classify plant conditions based on environmental variables. This model was selected for its interpretability, efficiency, and suitability for binary classification tasks such as predicting the presence of plant disease.
- Metrics:
Model performance was evaluated using several standard classification metrics, including accuracy, precision, recall, F1-score, and the confusion matrix. The Logistic Regression model achieved an accuracy of 0.7695, indicating a moderate level of predictive reliability. Additional evaluation using the ROC curve and AUC score (0.71) further supported the model’s capability to distinguish between healthy and diseased plants.



- Visualizations:
<img width="823" height="684" alt="image" src="https://github.com/user-attachments/assets/909e86d2-f3be-4ca0-9f93-484bcb2aee03" />


<img width="663" height="484" alt="image" src="https://github.com/user-attachments/assets/1879aaf9-2892-4891-86ea-22861ee87835" />

<img width="1232" height="724" alt="image" src="https://github.com/user-attachments/assets/4bed82d2-0804-4b33-8b1d-c6a488847d89" />



To support the analysis, several visual outputs were generated:
- A confusion matrix heatmap illustrating correct and incorrect predictions across classes
- A ROC curve showing the trade-off between true positive and false positive rates
- A feature importance bar chart indicating the contribution of each environmental variable to the model’s predictions
These visualizations helped clarify model behavior and performance trends.

- Insights (3–5):
Humidity and rainfall emerged as the most influential predictors of plant disease, exhibiting the highest positive coefficients in the model. While the model showed strong performance in correctly identifying healthy plants (class 0), it struggled to recognize diseased plants (class 1), as indicated by the lower recall score. Soil pH displayed a negative coefficient, implying that plants in more neutral or slightly alkaline soil conditions may face a reduced risk of disease. The ROC curve and AUC value confirm that the model performs above chance level, although its predictive capability can still be enhanced. Overall, the model serves as a solid and interpretable baseline for examining how environmental factors contribute to plant health classification.


## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:
pip install -r requirements.txt
3. Open the .ipynb notebook
4. Upload the cleaned csv file
5. Code the Machine Learning tool 
6. Run cells

