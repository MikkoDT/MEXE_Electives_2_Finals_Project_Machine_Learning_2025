# Final Assessment — Machine Learning Model

## Project Overview

This project demonstrates the use of **Linear Regression** to analyze school-related data and predict a continuous target variable. It is part of a final machine learning assessment and focuses on understanding how different educational factors influence student outcomes.

---

## Pair Information

* **Pair Name:** Eskwelaaa
* **Members:** Marco Calaton & Megildo Perez
* **Topic:** School
* **Model Used:** Linear Regression

---

## Dataset Overview

* **Dataset Source:** *(add dataset link here)*

* **Description:**
  The dataset contains information related to school and educational factors and their relationship to a target variable.

* **Target Variable:**
  *(e.g., Final Score, Performance Index, Academic Performance)*

* **Features Used:**

  * Feature 1
  * Feature 2
  * Feature 3

---

## Data Preprocessing

The following preprocessing steps were applied before training the model:

* **Encoding:** Converted categorical variables into numerical values
* **Scaling:** Standardized numerical features for better model performance
* **Data Cleaning:**

  * Renamed columns for consistency
  * Handled missing values
  * Removed duplicate records
  * Ensured correct data types
* **Train–Test Split:** Split the dataset into training and testing sets

---

## Model & Evaluation

* **Algorithm:** Linear Regression
* **Reason for Selection:**

  * Simple and interpretable
  * Effective for predicting continuous values

### Evaluation Metrics

* R² Score
* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

### Visualizations

* Actual vs. Predicted Values Plot
* Residuals Plot

(All visualizations are generated inside the Jupyter Notebook.)

---

## Key Insights

1. The Linear Regression model shows a clear relationship between school-related features and the target variable.
2. The model produces reasonable predictions but still shows some errors, indicating that additional factors may affect the outcome.
3. Certain features have a stronger impact on predictions, emphasizing the importance of feature selection.

---

## How to Run the Project

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

## Project Structure

```text
├── dataset/
│   └── data.csv
├── notebook.ipynb
├── requirements.txt
└── README.md
```

---

## Conclusion

This project demonstrates how Linear Regression can be applied to educational data to identify trends and relationships between features and academic outcomes. The model serves as a solid baseline for further improvements and more advanced techniques.

