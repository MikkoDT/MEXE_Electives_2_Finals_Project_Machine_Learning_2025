# Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: **Name**
- Members:
  - **Florendo, Karlo S.**
  - **Pasumbal, Bea Carmela V.**
- Topic: **Machine Failure Prediction using Sensor Data**
- Chosen Model: **Logistic Regression**

## 2. Dataset Overview
- Dataset Source: </br>
  **https://www.kaggle.com/datasets/umerrtx/machine-failure-prediction-using-sensor-data** 
- Description: </br>
  This dataset contains sensor readings collected from various machines and is designed to help predict machine failures in advance. It includes multiple types of sensor measurements along with records indicating whether a failure occurred.
- Target Variable: </br>
  - `fail` - binary indicator of machine failure (1 for failure, 0 for no failure)
- Features Used: </br>
  - `footfall` - number of people or objects passing by the machine
  - `USS` - ultrasonic sensor data, indicating proximity measurements
  - `VOC` - volatile organic compounds level detected near the machine
  - `RP` - rotational position or RPM of the machine parts
  - `Temperature` - the operating temperature of the machine

## 3. Preprocessing Summary
- Encoding: </br>
  No encoding was required because all selected features were already numerical, and the target variable `fail` was already in binary form (0 and 1).
- Scaling: </br>
  Standard Scaler was applied to normalize the numerical sensor readings. This helps improve model performance by ensuring all features contribute proportionally.
- Cleaning steps: </br>
  Irrelevant columns were removed to simplify the dataset and focus the model on the most meaningful features.
- Train–test split: </br>
  The dataset was divided into training (80%) and testing (20%) subsets to evaluate the model’s performance on unseen data.

## 4. Model & Results
### Model used
- ***Logistic Regression***
  * This model were used to predict the machine failure based on the sensor data. Logistic Regression is a Machine Learning algorithm that is great for binary classification problems making this an appropiate for determining whether the machine will fail or not.
 
- ***Metrics***
  * Accuracy : `90.48%`
    <p align="center"> 
      <img src="https://github.com/user-attachments/assets/4c2fcd87-ff46-429d-942b-5b86f78368cc" width="800">

  * True Negative : `96 cases`
  * False Negative: `9 cases`
  * False Positive: `9 cases`
  * True Positive : `75 cases`
    <p align="center"> 
      <img src="https://github.com/user-attachments/assets/d02d2033-b451-4bbe-bf0f-8f8dce152933" width="800">
      
  * Precision: `91.43%` for `0` and `89.29%` for `1`
  * Recall   : `91.43%` for `0` and `89.29%` for `1`
  * F1 Score : `91.43%` for `0` and `89.29%` for `1`
    <p align="center"> 
      <img src="https://github.com/user-attachments/assets/bd17fa42-9a36-40a1-b0c2-b00b84aa2c80" width="800">

  * AUC      : `0.778`
    <p align="center"> 
      <img src="https://github.com/user-attachments/assets/09ad6293-2b0e-4c8e-8403-e51deca67fdd" width="800">

- ***Visualization***
  * Correlation Heatmap
    <p align="center"> 
      <img src="https://github.com/user-attachments/assets/1d0ba27c-c54b-4a85-be7e-20684033a239" width="800">
  The correlation heatmap shows that VOC has a strong correlation with machine failure, which means higher VOC levels indicate failure occurrence.  USS exhibits a moderate negative correlation with negative value, lower ultrasonic sensor readings are more observed during failure cases. Other variables show weak positive correlation values, indicating minimal direct influence on machine failure. 
  * Violin Plot
    <p align="center"> 
      <img src="https://github.com/user-attachments/assets/ef0a18b0-4b9e-49c7-8e9e-8af6f46a0c12" width="800">
  The violin plot demonstrates that VOC and USS are the most influential features in predicting machine failure. It supports the analysis that VOC is the most significant indicator of machine malfunction

    
- ***Insights***
  1. The model demonstrates high accuracy, precision, recall, and F-1 score between machine failure and non-failure cases/variables.
  2. The model exhibits strong performance with 90% accuracy and an AUC of 0.778 that reliably distinguishes failing from non-failing machines. 
  3. The Volatile Organic Compounds (VOC) feature stands as a reliable indicator of potential malfunction, contrasting footfall and USS.
  4. The model can be useful in early failure detection with continuous monitoring of the variables.
  5. The model can be improved by integrating more sensor data.
  

## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:
   pip install -r requirements.txt
4. Open the `.ipynb` notebook
5. Run all cells
