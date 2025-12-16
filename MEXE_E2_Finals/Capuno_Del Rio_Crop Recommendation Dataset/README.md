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
  - **Scaling:**
  - **Cleaning steps:** StandardScaler was used to standardize the independent numerical features (such as N, P, K, temperature, humidity, pH, and rainfall).
  - **Train–test split:**

## 4. Model and Results
- **Model used:**
- **Metrics:**
- **Visualization:**
- **Insights:**

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:
pip install -r requirements.txt
3. Open the `.ipynb` notebook
4. Run all cells

