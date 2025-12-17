# 👨‍💻 Final Assessment — Machine Learning Model

## ℹ️ 1. Pair Information
- ✍️ **Pair Name**: Navigators
- 👥 **Members**: Jhun Kenji Jusay and Dianne Mae Vinegas 
- 🤖 **Topic**: Robot Navigation in Dynamic 3D Environments 
- ✅ **Chosen Model**: Logistic Regression

## 📰 2. Dataset Overview

- **Dataset Source**: https://www.kaggle.com/datasets/ziya07/robot-navigation-in-dynamic-3d-environments 
- **Description**: This dataset evaluates the performance of pathfinding algorithms in robot navigation tasks across varying levels of environmental complexity and obstacle density. It contains simulated data for robot navigation in dynamic 3D environments, intended for studying path planning and obstacle avoidance.
- **Target Variable**: Pathfinding Success
- **Features Used**:
  
  - Start Position (X, Y, Z)
  - Destination Position (X, Y, Z)
  - Static Object Count
  - Dynamic Object Count
  - Obstacle Position (X, Y, Z)
  - Obstacle Velocity (X, Y, Z)
  - Path Length (m)
  - Obstacle Height (m)
  - Obstacle Width (m)
  - Obstacle Depth (m)
  - Energy Efficiency (%)
  - Collision Avoidance (%)
  - Computation Time (ms)
  - Pathfinding Algorithm_ABC
  - Pathfinding Algorithm_MABC
  <p align="center">

## 📃 3. Preprocessing Summary
- **Encoding**: All categorical variables such as `Pathfinding Success` were were transformed into numerical values using one-hot encoding to make them compatible with the machine learning model.
- **Scaling**: Numerical features were scaled to a common range to prevent any single feature from dominating the model.
- **Cleaning steps**: Missing values and inconsistent data entries were checked and handled to ensure data quality.
- **Train–test split**: The dataset was divided into training and testing sets to evaluate model performance on unseen data.

## 📊 4. Model & Results
- **Model used**: Logistic Regression

- **Metrics**:
  -  **Accuracy** = 87%
  <p align="center">

![IMG_2587](https://github.com/user-attachments/assets/0928d426-a872-4197-b25b-9f57454c6a2a)

    Figure 1. Classification Performance Metrics of the Robot Navigation Model
  <p/>

![IMG_2593](https://github.com/user-attachments/assets/3e1ac20d-9678-4d73-8fed-50410f0e46ce)

    Figure 2. Confusion Matrix of the Robot Navigation Failure Prediction Model
  <p/>

![IMG_2592](https://github.com/user-attachments/assets/b5c53008-736e-4897-a2eb-ae9008c98e27) 

    Figure 3. ROC Curve of the Robot Navigation Failure Prediction Model 
  <p/>


- **Visualizations**:
- **Insights**:

  - The model demonstrates strong overall performance, correctly predicting the majority of cases with an accuracy of approximately 87%, indicating reliable classification results. In addition, the AUC value of 0.94 is exceptionally high, showing that the model has an excellent ability to distinguish between successful and unsuccessful robot pathfinding outcomes across various decision thresholds.

  - Predicting Class 0 more effectively with higher precision and recall, while performance for Class 1 is slightly lower, indicating greater difficulty in correctly identifying this class

  - Collision avoidance rate and energy efficiency strongly influence the model’s predictions, showing consistent effects on pathfinding success and making them the primary predictors in decision-making.

  - To further improve performance, evaluate other models such as Random Forest, Gradient Boosting, or Nueral Network, as these can better capture nonlinear relationships and complex feature interactions.
  <p align="center">

## ▶️ 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells
