# Final Assessment — Machine Learning Model

## 1. Pair Information

* **Pair Name:** Eskwelaaa
* **Members:** Marco Calaton & Megildo Perez
* **Topic:** School
* **Chosen Model:** Linear Regression

---

## 2. Dataset Overview

* **Dataset Source:** *(add dataset link here)*

* **Description:**
  This dataset contains information related to school/education factors and their relationship to the target variable.

* **Target Variable:**
  *(Specify the variable being predicted, e.g., Final Score, Performance Index, etc.)*

* **Features Used:**

  * Feature 1
  * Feature 2
  * Feature 3
    *(List all input features used in the model)*

---

## 3. Preprocessing Summary

* **Encoding:**
  Categorical features were encoded into numerical values to ensure compatibility with the Linear Regression model.

* **Scaling:**
  Numerical features were standardized to place them on a similar scale and improve model performance.

* **Data Cleaning:**

  * Renamed columns for consistency
  * Checked and handled missing values
  * Removed duplicated records
  * Ensured consistent data types

* **Train–Test Split:**
  The dataset was split into training and testing sets to evaluate model performance on unseen data.

---

## 4. Model & Results

* **Model Used:**
  Linear Regression was selected due to its simplicity, interpretability, and effectiveness for predicting continuous values.

* **Evaluation Metrics:**

  * R² Score
  * Mean Absolute Error (MAE)
  * Mean Squared Error (MSE) / Root Mean Squared Error (RMSE)

* **Visualizations:**

  * Actual vs. Predicted values plot
  * Residuals plot
    *(Images generated inside the Jupyter Notebook)*

* **Insights:**

  * The model demonstrates a clear relationship between the selected features and the target variable.
  * Errors are reasonably distributed, indicating acceptable model performance.

---

## 5. How to Run the Project

### Requirements

* VS Code
* Python 3.x
* Jupyter Notebook Extension

### Installation

```bash
git clone <repository-url>
cd <repository-folder>
pip install -r requirements.txt
```

### Running the Model

1. Open the project folder in VS Code
2. Open the `.ipynb` notebook file
3. Run all cells sequentially
4. View the outputs, evaluation metrics, and visualizations

---

## 6. Repository Structure

```text
├── data/
│   └── dataset.csv
├── notebook/
│   └── linear_regression_model.ipynb
├── README.md
└── requirements.txt
```

---

## 7. Conclusion

This project demonstrates the application of Linear Regression in predicting a school-related outcome using proper data preprocessing, evaluation, and visualization techniques.
