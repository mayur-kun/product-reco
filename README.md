# Product Recommendation System
This repository demonstrates building a product recommendation system using combined Content-Based Filtering (CBF) and Collaborative Filtering (CF) with an interactive user interface (UI) powered by Streamlit.

The dataset was taken from Target India's website - https://india.target.com/work/teams/target-tech/solve-for-target


# Here's an overview 🌟

There are 2 code files - 

solution.ipynb - Focuses on recommending products based on hybrid filtering methods.

solution_3.ipynb - Focuses on understanding the distribution and popularity of the products.

**1. Data Import and Exploratory Data Analysis (EDA):**
* Import necessary libraries and the dataset
* Explore the dataset by checking data types, unique values, missing values, etc.
* Handle missing values by dropping columns or imputing values

**2. Preprocess Textual Data:**
* Convert text data to lowercase
* Remove punctuation and duplicates from product names
* Extract product and source entities from text using regular expressions
* Calculate sentiment scores for reviews and titles using VADER

**3. Exploratory Data Analysis (EDA):**
* Perform EDA to gain insights into the dataset, including the distribution of product ratings, most frequently rated products, lowest and highest-rated products, and analysis of product categories.
* Identify the top-selling products across different categories based on the number of reviews and average ratings.
* Build a machine learning model to analyze the least-selling products and provide recommendations based on unfavorable reviews.

**4. Content-Based Filtering:**
* Text features are created by combining **product entities** - derived from product names using Named Entity Recognition, and **product reviews**.
* Vectorization is applied to these text features to create a TF-IDF matrix.
* Cosine similarity between the TF-IDF vectors is calculated using linear kernel.
* A function is defined to get top-N content-based recommendations for a given product, based on cosine similarity scores.

**5. Collaborative Filtering:**
* A rating matrix is created by grouping the data by product names and applying a list of ratings.
* Cosine similarity between product rating vectors is calculated.
* A function is defined to get top-N collaborative recommendations for a given product, based on similarity of rating vectors.

**Next phase (will update soon):**
* To improve the model's performance, particularly for identifying the 'True' cases (least selling products with unfavorable reviews), follow these steps:

    1. Address Class Imbalance: As previously suggested, use techniques like SMOTE to balance the classes.
    2. Feature Engineering: Ensure the features are robust and meaningful.
    3. Model Tuning: Experiment with different models and hyperparameters to improve performance.

* Creating a UI and generating product descriptions based on product features. Planning to use LLM models like GPT-4, Gemini or Llama2.


<!-- # Lessons 📝
**Importance of Data Preprocessing:**

The code highlights the importance of thorough data preprocessing, including handling missing values, converting data types, and extracting relevant features from textual data.
Techniques like regular expressions and natural language processing (NLP) can be effective in extracting meaningful information from unstructured text data.

**Feature Engineering:**

The code demonstrates the importance of feature engineering, especially for textual data.
Techniques like sentiment analysis (using VADER) and TF-IDF vectorization are employed to extract meaningful features from text.
These features can significantly improve the performance of recommendation systems.

**Modularity and Reusability:**

The code is structured into separate functions for content-based filtering, collaborative filtering, and hybrid recommendations.
This modular approach promotes code reusability and maintainability, making it easier to extend or modify the solution as needed. -->