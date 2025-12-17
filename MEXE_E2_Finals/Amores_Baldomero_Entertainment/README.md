# Final Assessment — Machine Learning Model

## 1. Pair Information
- Pair Name: Young Stunna
- Danielle Genly C. Baldomero
- Shawn Michael B. Amores
- Topic: Entertainment (Predicting IMDB rating)
- Chosen Model: Logistic Regression

## 2. Dataset Overview
- Dataset Source: https://www.kaggle.com/datasets/ggtejas/tmdb-imdb-merged-movies-dataset
- Description: This dataset merges movie information from The Movie Database (TMDb) and IMDb, providing a detailed collection of movie-related data. The dataset includes a variety of movie attributes such as titles, release dates, ratings, genres, production companies, and more, making it a valuable resource for movie-related analysis, recommendation systems, and other data science tasks.
- Target Variable: IMDb Rating (Average Rating on actual Dataset)
- Features Used:

## 3. Preprocessing Summary
- Encoding:
- Scaling:
- Cleaning steps:
- Train–test split:

## 4. Model & Results
- Model used:
  
  The model used is a binary classification model that predicts whether a movie can be considered good or bad based on selected numerical features such as ratings, popularity, and financial data. Movies were labeled according to a set rating threshold, allowing the model to learn patterns from past examples. Through this process, the model identifies relationships between the input variables and movie quality, helping evaluate how these factors influence audience perception.
- Metrics:
  
  The boxplot matrix is used to compare how the values of selected features are distributed between good and bad movies, making it easier to see differences in spread and typical values as well as areas where the two groups overlap. The scatter matrix shows how numerical variables relate to one another by plotting them in pairs, which helps in observing general trends and patterns between movie ratings and other factors. Lastly, the correlation heatmap provides a summary of how strongly the numerical features are related, indicating which variables move together and which have little to no linear relationship.
- Visualizations:
<p align="center"> Boxplot Matrix (Good vs Bad) </p>
<p align="center">
<img width="1490" height="789" alt="image" src="https://github.com/user-attachments/assets/a77c2dcf-19db-494e-8c4d-740cde582e3e" />
</p>

<p align="center"> Scatter Matrix </p>
<p align="center">
<img width="1384" height="1184" alt="16bae691-f6b7-4284-8fb2-0b2855185dbf" src="https://github.com/user-attachments/assets/b7aa0327-3272-45b2-acfc-de688e23740e" />
</p>

<p align="center"> Correlation Heatmap </p>
<p align="center">
<img width="890" height="784" alt="d0fac5ec-a9ac-46fc-b212-11eb5535634f" src="https://github.com/user-attachments/assets/04374592-21bf-4ec9-985a-fa54202a0f67" />
</p>
- Insights:

- Boxplot Matrix (Good vs Bad)

 The boxplot matrix reveals that budget, revenue, and profit distributions largely overlap between good and bad movies, showing that financial performance alone does not clearly distinguish movie quality. Popularity shows only a slight difference between the two groups. The normalized rating provides the clearest separation, supporting its use as the primary feature for classification.

- Scatter Matrix

 The scatter matrix shows that IMDb ratings have weak relationships with budget, revenue, and popularity, indicating that higher spending or earnings do not directly lead to better ratings. In contrast, budget and revenue are strongly related to each other, reflecting expected industry behavior. Overall, the plot suggests that movie quality is influenced more by non-financial factors than by production scale.
    
- Correlation Heatmap

 The heatmap highlights strong correlations among financial and engagement variables such as budget, revenue, and vote counts. However, IMDb ratings show weak correlations with these features, indicating that audience ratings are largely independent of financial success or popularity.


## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells
