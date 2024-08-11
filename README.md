# Article_Popularity_Prediction

## Objective
This project aims to predict the popularity of articles on Mashable by analyzing various predictive models. The goal is to automate article selection based on potential shares, which impacts revenue. In the current scenario, Mashable earns an estimated $0.75 in revenue per share when an article is shared 1000 times or less, and $2 for every share after that. Accurate predictions can help strategize content to maximize engagement and revenue.

## Dataset 
The dataset used in this project was retrieved from the UCI Machine Learning Repository. It contains 58 features related to the articles, which Mashable originally published. The features in the article are related to data channels, keyword statistics, publication details and text semantics and subjectivity. Please note that while this dataset includes statistics associated with the articles, it does not share the original content. The original articles can be accessed through the provided URLs.

## Models Used for Analysis 
1. **Linear Regression**: Initial model with a low R² value. Further refinement with selected features showed poor performance.
2. **Logistic Regression**: Two models created—one with all features and one with top features identified by XGBoost. The latter performed better.
3. **Random Forest**: Evaluated with all features and top features from XGBoost. Demonstrated high accuracy and sensitivity.
4. **Naive Bayes**: Used for benchmarking and comparison.

## Results
1. Random Forest with 9 features (as selected by XGBoost) outperformed other models in accuracy and sensitivity. It correctly identifies popular articles with high sensitivity (0.9049), and is recommended to be used in the article selection process at Mashable.
