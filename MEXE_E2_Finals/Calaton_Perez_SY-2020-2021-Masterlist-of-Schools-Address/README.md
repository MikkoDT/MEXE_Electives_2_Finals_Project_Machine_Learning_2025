📑 Final Assessment — Machine Learning Model
Project Overview

This project presents the application of Linear Regression in analyzing school-related data to examine how various educational factors relate to a target outcome. It is conducted as part of a final machine learning assessment and aims to demonstrate how data-driven methods can be used to understand patterns within educational datasets.

Pair Information

Pair Name: Eskwelaaa

Members: Marco Calaton & Megildo Perez

Topic: School Data Analysis

Model Used: Linear Regression

Dataset Overview

Dataset Source:
(Insert School Masterlist dataset link here)

Description:
The dataset is based on a school masterlist and contains information related to school characteristics and location attributes that may influence classification or outcomes.

Target Variable:
School location classification encoded numerically:

Urban

Rural

Data Preprocessing

Before model training, several preprocessing steps were performed to ensure data quality and compatibility:

Encoding:
Categorical variables were transformed into numerical values to allow processing by the regression model.

Scaling:
Numerical features were standardized to improve model stability and performance.

Data Cleaning:

Column names were standardized for consistency

Missing values were handled appropriately

Duplicate records were removed

Data types were verified and corrected where necessary

Train–Test Split:
The dataset was split into training and testing sets to evaluate model performance on unseen data.

Model & Results

Algorithm Used: Linear Regression

Reason for Selection

Easy to understand and interpret

Suitable for identifying relationships between variables

Serves as a strong baseline model for prediction tasks

Evaluation Metrics

The model was evaluated using the following metrics:

R² Score

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

Visualizations

Actual vs. Predicted Values Plot

Residuals Plot

All visualizations are generated within the Jupyter Notebook.

Key Insights

The Linear Regression model reveals a noticeable relationship between school-related features and the target variable.

Predictions are generally reasonable, though some errors remain, suggesting the influence of additional factors not captured in the dataset.

Certain features contribute more strongly to the predictions, highlighting the importance of proper feature selection.

How to Run the Project
Requirements

VS Code

Python 3.x

Jupyter Notebook Extension

Installation
git clone <repository-url>
cd <repository-folder>
pip install -r requirements.txt

Running the Model

Open the project folder in VS Code

Open the .ipynb notebook file

Run all cells sequentially

Review the outputs, evaluation metrics, and visualizations

Project Structure
├── dataset/
│   └── data.csv
├── notebook.ipynb
├── requirements.txt
└── README.md

Conclusion

This project demonstrates how Linear Regression can be applied to school masterlist data to identify trends and relationships among educational features. The model provides a solid baseline for analysis and can be further improved by incorporating additional variables or more advanced machine learning techniques.
