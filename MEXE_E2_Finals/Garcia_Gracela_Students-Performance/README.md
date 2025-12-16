<h1 align="center">Final Assessment — Machine Learning Model</h1>

## 1. Pair Information
Pair Name: GG
 
Members: 
- Garcia, Ron Ivan
- Gracela, Jharry

Topic: Students' Performance in Exams
 
Chosen Model: Linear Regression

## 2. Dataset Overview

Dataset Source: https://www.kaggle.com/datasets/spscientist/students-performance-in-exams

Description: This dataset is designed to analyze the factors that influence high school students' performance in exams. It typically contains 1,000 observations (students) and explores the correlation between socioeconomic factors and academic outcomes. We used this data set in our machine learning model, where the math scores are treated as the dependent variable.  The primary goal is to understand the influence of a student's background, writing and reading scores, and preparation on their math scores.

Dependent/Target Variable:

- num__Math_Score

Features Used:

- num__Reading_Score
- num__Writing_Score
- nom__Ethnicity_group B
- nom__Ethnicity_group C
- nom__Ethnicity_group D
- nom__Ethnicity_group E
- nom__Lunch_standard
- nom__Test_Prep_none
- nom__Gender_male
- ord__Parental_LOE_high school
- ord__Parental_LOE_some college
- ord__Parental_LOE_associate's degree
- ord__Parental_LOE_bachelor's degree
- ord__Parental_LOE_master's degree

## 3. Preprocessing Summary

Categorical Encoding: Converts non-ordinal variables into a numerical format using One-Hot Encoding to prevent models from inferring an incorrect order.

Scaling: The independent variables was scaled using StandardScaler after splitting to have a fair balance between low and high values.

Cleaning Steps:
- Handle Missing Values
- Create Categorical Features

Train-Test Split: Splitting the dataset into train and test to be able to test as well as train the data for the preparation of machine learning.

## 4. Model and Result
### Model Used: **Linear Regression**

The target variable, num_Math_score, is a continuous numerical outcome, which is the primary domain for the use of Linear Regression is the reason that this model type is used. Furthermore, the past evaluation of preprocessed data show a strong quantified linearity, therefore, Linear Regression is preferred for its simplicity, efficiency, and high interpretability—it provides a clear, additive representation of how both continuous and binary (0/1) predictor variables contribute to the predicted Math Score.

### Metrics:

**Mean Absolute Value**

- 4.39484274852452

**Mean Score Value**
  
- 31.046790272758408

**Coefficient of Determination (R²)**
  
- 0.8629895363812152

**Adjusted R²**
  
- 0.8526211769722261

### Visualizations:
<div align="center">
 

<h3 id="visualization-1-histogram-plot"> Visualization 1: Scatter Plot - Numeric Features vs. Math Scores</h3>

The Scatter Plots demonstrated an exceptionally strong, positive linear relationship between Math Score and the other two continuous outcome variables, Reading Score and Writing Score, where the points clustered tightly along an upward-sloping trend line.

<img width="1189" height="490" alt="image" src="https://github.com/user-attachments/assets/2be7bfda-d208-49ea-a010-9d4c7cbd8246" />


<h3 id="visualization-1-histogram-plot"> Visualization 2: Bar Plot - Categorical Features vs. Math Scores</h3>

The Bar Plots shown an easy but very informative visualization to how the categorical features affect the num_Math_Scores of the students. It shows the significance of the categorical features in determining one's scores in exams.

<img width="1489" height="1189" alt="image" src="https://github.com/user-attachments/assets/47e14892-4cd6-4ae8-bec6-6595cd2779af" />

<h3 id="visualization-1-histogram-plot"> Visualization 3: Heatmap Correlation</h3>

This visual evidence of linearity was quantitatively confirmed by the Correlation Heatmap, which revealed high Pearson correlation coefficients ($r$) of approximately $0.80$ to $0.82$ between the Math Score and the other two subject scores. In addition to confirming these strong linear ties, the heatmap also served to quantify the weaker, yet significant, linear associations between Math Score and various binary socioeconomic/background features, providing a comprehensive statistical measure of all relationships within the dataset.

<img width="1132" height="989" alt="image" src="https://github.com/user-attachments/assets/84fd7c08-3718-4da5-9a6e-8294ffa8a549" />

<h3 id="visualization-1-histogram-plot"> Visualization 4: Corr Plot</h3>

The Correlation plot shows the features that affects the num__Math_Scores positively as it extends to the right while the features that affects it negatively are those that are extending towards the left side.

<img width="805" height="590" alt="image" src="https://github.com/user-attachments/assets/dc68631b-6275-4cd7-8c0c-863299015d3c" />

</div>

### Key Insights:

**1. The Predictive Model is Highly Accurate**

The Linear Regression model for predicting Math Score achieved an R-Squared Value of 0.86 and had an adjusted R-Squared of 0.85. This shows that the independent variables, which are the scores and socioeconomic factors explain the variability in the Math score, demonstrating the model's predictive power.

**2. Academic Interdependence is the Dominant Factor**

The high R-Squared is primarily driven by the exceptionally strong linear correlation between Math Score and the other continuous variables, Reading Score and Writing Score. This suggests that a student's general academic ability and performance across all core subjects is the most powerful determinant of their Math Score.

**3. Socioeconomic Factors Provide Measurable Incremental Gain**

Although less correlated than the other scores, the analysis confirmed that key socioeconomic binary factors, such as receiving Standard Lunch and completing the Test Preparation Course, are significantly associated with a positive shift in the Math Score distribution. These variables are important, measurable contributors to the model's predictive accuracy, indicating external support and preparation have a tangible impact on performance.
