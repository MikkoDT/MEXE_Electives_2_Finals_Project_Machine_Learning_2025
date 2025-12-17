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
- Metrics:
- Visualizations:
- <p align="center"> Boxplot Matrix (Good vs Bad) </p>
<p align="center">
<img width="900" alt="image" src="" />
</p>

- <p align="center"> Scatter Matrix </p>
<p align="center">
<img width="900" alt="image" src="" />
</p>

- <p align="center"> Correlation Heatmap </p>
<p align="center">
<img width="900" alt="image" src="" />
</p>
- Insights (3–5):

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
