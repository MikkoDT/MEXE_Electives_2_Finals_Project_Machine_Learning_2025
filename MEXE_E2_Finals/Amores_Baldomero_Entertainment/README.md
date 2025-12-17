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
### Encoding
- Converted genre columns into one‑hot encoded binary features (1 = genre present, 0 = not present).
- Encoded cast, writer, director, and company using ID-based score features, representing each contributor’s average IMDb performance instead of raw IDs.
- Ensured all categorical inputs were transformed into numerical values suitable for model training.

### Scaling
- Applied StandardScaler to continuous numeric features, including:
  - Budget
  - Revenue
  - Profit / Profit Normalized
  - Popularity
  - Contributor reputation scores
- Scaling helps the model handle differences in magnitude and prevents large values (e.g., revenue) from dominating the learning process.

### Cleaning Steps
- Converted columns such as IMDb rating, vote average, popularity, budget, and revenue to numeric types with errors='coerce'.
- Filled NA / missing values with zeros or safe defaults.
- Computed additional engineered features:
- Profit = revenue – budget
- Created scores for categorical IDs. (e.g. cast, writer, director and company)
- Removed unused or irrelevant columns that did not contribute to the model.

### Train–Test Split
- Split the full processed dataset into:
  - 80% training data
  - 20% testing data
- Random state fixed to ensure reproducibility.
- Ensured the target variable (“GoodBad”) was distributed similarly across both sets.

## 4. Model & Results
- Model used:
  
  The model used is a binary classification model that predicts whether a movie can be considered good (1) or bad (0) based on inputs such as genres, 3 cast, 2 writers, director company and numerical categories such as budget and revenue. Movies were labeled according to a set rating threshold of 6 above being depicted as Good, allowing the model to learn patterns from past examples. Through this process, the model identifies relationships between the input variables and movie quality, helping evaluate how these factors influence audience perception.
  
- Metrics:
  
  The boxplot matrix is used to compare how the values of selected features are distributed between good and bad movies, making it easier to see differences in spread and typical values as well as areas where the two groups overlap. The scatter matrix shows how numerical variables relate to one another by plotting them in pairs, which helps in observing general trends and patterns between movie ratings and other factors. Lastly, the correlation heatmap provides a summary of how strongly the numerical features are related, indicating which variables move together and which have little to no linear relationship.
- Visualizations:
<p align="center"> Boxplot Matrix (Good vs Bad) </p>
<p align="center">
<img width="1483" height="786" alt="0072cb4e-87e2-4acf-9482-1357f9535ad9" src="https://github.com/user-attachments/assets/53435682-a3ab-4beb-b70f-2556b5ddf819" />
</p>
The boxplot matrix shows heavy overlap between good and bad movies for budget, revenue, and profit, indicating limited discriminative power. Popularity shows only a slight difference between groups, while the normalized score clearly separates good and bad movies, making it the most effective feature for classification.

<p align="center"> Scatter Matrix </p>
<p align="center">
<img width="1384" height="1184" alt="16bae691-f6b7-4284-8fb2-0b2855185dbf" src="https://github.com/user-attachments/assets/b7aa0327-3272-45b2-acfc-de688e23740e" />
</p>
The scatter plots indicate that IMDb ratings vary widely across all levels of budget, revenue, and popularity, showing no strong relationship between these factors and movie ratings. Both high- and low-performing movies can receive similar ratings, and profit shows only a weak association with audience scores.

<p align="center"> Correlation Heatmap </p>
<p align="center">
<img width="890" height="784" alt="d0fac5ec-a9ac-46fc-b212-11eb5535634f" src="https://github.com/user-attachments/assets/04374592-21bf-4ec9-985a-fa54202a0f67" />
</p>
The heatmap shows that rating-related features are strongly correlated with each other, confirming they measure the same aspect of movie quality. Budget, revenue, and vote related features are also strongly related, indicating that financial scale and audience engagement move together. However, these financial features show weak correlations with IMDb ratings, suggesting movie quality is not directly tied to financial performance.

### Insights based on Findings and Visualizations
#### Model Insights
- *The model achieved a performance accuracy of approximately 88%, with the confusion matrix indicating that it is more effective at identifying BAD movies than GOOD ones. The prediction probabilities show clear confidence separation, meaning the model reliably distinguishes strong GOOD indicators from weak ones. Additionally, this kind of percentage or accuracy is highly expected due to IMDb ratings complexity and more audience influenced as past data checking showed how movie trends and popularity are randomized and throughout the years have no predictable pattern- though genre, cast, directors, writers, budget, company and revenue have influence, the bigger impact lays on audience impact.*
#### Visualization Insights
- Boxplot Matrix (Good vs Bad)

 *The boxplot matrix reveals that budget, revenue, and profit distributions largely overlap between good and bad movies, showing that financial performance alone does not clearly distinguish movie quality. Popularity shows only a slight difference between the two groups. The normalized rating provides the clearest separation, supporting its use as the primary feature for classification.*

- Scatter Matrix

 *The scatter matrix shows that IMDb ratings have weak relationships with budget, revenue, and popularity, indicating that higher spending or earnings do not directly lead to better ratings. In contrast, budget and revenue are strongly related to each other, reflecting expected industry behavior. Overall, the plot suggests that movie quality is influenced more by non-financial factors than by production scale.*
    
- Correlation Heatmap

 *The heatmap highlights strong correlations among financial and engagement variables such as budget, revenue, and vote counts. However, IMDb ratings show weak correlations with these features, indicating that audience ratings are largely independent of financial success or popularity.*


## 5. How to Run
1. Install VS Code + Python + Jupyter Extension
2. Install dependencies:

pip install -r requirements.txt

3. Open the `.ipynb` notebook
4. Run all cells
