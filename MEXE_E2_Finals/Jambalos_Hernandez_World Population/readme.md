# Final Assessment — Machine Learning Model

## 1. Pair Information

* **Pair Name:** World pop
* **Members:**
1. Queian Kim Jambalos
2. Lelanie Lorraine Hernandez


* **Topic:** World Population Classification
* **Chosen Model:** Logistic Regression

**Why this model?**
We chose **Logistic Regression** as our baseline model because our objective was to determine if there is a linear relationship between demographic statistics (like population size and density) and geographical location. By using a standard classification algorithm, we aimed to test the hypothesis that population trends are distinct per continent.

## 2. Dataset Overview

* **Dataset Source:** `world_population.csv`
* **Description:** The dataset contains population statistics for 234 countries/territories. The goal is to predict the continent of a country based solely on its demographic figures.
* **Target Variable:** `Continent` (Categorical: Asia, Europe, Africa, Oceania, North America, South America)
* **Features Used:**
* `Area (km²)`
* `Density (per km²)`
* `Growth Rate`
* `World Population Percentage`
* `2022 Population`
* `2020 Population`



## 3. Preprocessing Summary

* **Cleaning steps:** Checked for missing values and filled any potential nulls with `0` to prevent runtime errors.
* **Encoding:** No categorical encoding was required for the features as the input variables selected were all numerical.
* **Scaling:** Applied `StandardScaler`. This converted values into Z-scores to ensure that large numbers (like Population in the millions) did not overpower small decimals (like Growth Rate).
* **Train–test split:** 80% Training / 20% Testing. We used `stratify=y` to ensure that the Test set included a representative sample of countries from every continent.

## 4. Model & Results

* **Model used:** Logistic Regression (`multi_class='multinomial'`, `max_iter=5000`)
* **Metrics:**
* **Accuracy:** ~40%
* **Confusion Matrix:** Shows high confusion between developing nations in different continents.


* **Visualizations:**
* Class Distribution Bar Chart
* Confusion Matrix Heatmap
* ROC Curve


* **Insights:**
1. **Demographics ≠ Geography:** The modest accuracy proves that population statistics are **global traits**, not continental ones. A small, developing country in Asia looks mathematically identical to one in Africa.
2. **Growth Rate is the Strongest Predictor:** The model successfully learned to distinguish **Africa** (consistently high growth > 2%) from **Europe** (low or negative growth).
3. **Density as a Separator:** High population density helped separate Asian countries from North American ones, though significant overlap remains.
4. **Limitation:** To achieve near-perfect accuracy, **Geospatial Data (Latitude/Longitude)** would be required, as demographics alone are insufficient for precise location prediction.



## 5. How to Run

1. **Install VS Code + Python + Jupyter Extension**
2. **Install dependencies:**
Run the following command in your terminal:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn

```


3. **Open the Notebook:**
Open `World-Population_FinalModel_Jambalos_Hernandez.ipynb` in VS Code.
4. **Run all cells:**
Click "Run All" to load the data, train the model, and see the evaluation results.
*Note: You can use the Live Prediction Tool (Section 3.4) to manually test specific countries.*
