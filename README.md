# Product Recommendation System

This repository demonstrates building a product recommendation system using combined Content-Based Filtering (CBF) and Collaborative Filtering (CF) with an interactive user interface (UI) powered by Streamlit. 

The dataset was taken from Target India's website - https://india.target.com/work/teams/target-tech/solve-for-target

# Key Steps:

 - Preprocess data: Clean and transform textual data (reviews, titles, categories).
 - Extract features: Use TF-IDF for CBF and implicit ratings/dummy variables for CF.
 - Combine features: Create a single feature matrix.
 - Build models: Train KNN (CBF) and SVD++ (CF) models.
 - Set target variable: Use ratings/purchases if available, else "doRecommend".
 - Evaluate and refine: Assess model performance and adjust parameters as needed.
 - Make recommendations: For a new user/product, predict recommendations using the combined model.
 - Develop a user-friendly interface using Streamlit to:

# Benefits:

- Leverages both content and user interactions for personalized recommendations.
- Interactive UI allows for easy exploration and experimentation.