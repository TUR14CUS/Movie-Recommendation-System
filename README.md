# Movie Recommendation System with Collaborative Filtering and Content-Based Filtering

This Python script demonstrates a hybrid movie recommendation system that combines collaborative filtering (CF) using Surprise and content-based filtering (CBF) using TF-IDF similarity for richer recommendations.

## Dataset:

movies.csv: Contains movie information (title, overview, vote_count, vote_average, etc.).
credits.csv: Additional movie information (cast, crew, etc.). Not directly used in this version.
ratings.csv: User ratings for movies.
Code Breakdown:

## Data Preparation:

Import libraries: pandas for data manipulation, sklearn.feature_extraction.text for TF-IDF, sklearn.metrics.pairwise for similarity, and surprise for CF.###
Read data: Load movies, credits, and ratings.
Filter movies: Keep movies with sufficient votes using quantiles (m) and average rating (C).
Calculate weighted rating: Combine vote count and average rating to prioritize popular and well-rated movies.
### Content-Based Recommendations:

Preprocess overview: Fill missing overview text and create TF-IDF matrix.
Compute similarity: Calculate pairwise movie similarities using linear kernel similarity.
Example:

Find similar movies to "John Carter" (replace with your desired movie).
Retrieve movie indices based on highest similarity scores.
Print titles of the 5 most similar movies.
Collaborative Filtering Recommendations:

Prepare ratings: Filter ratings DataFrame and create Surprise dataset.
Build trainset: Build a full training set for the CF model.
Train SVD model: Use Singular Value Decomposition for collaborative filtering.
Make prediction: Predict a rating for a specific user-movie pair.
Cross-validation (optional): Evaluate model performance using RMSE and MAE.
Key Improvements:

Clarity and Structure: Enhanced code organization, comments, and explanations.
Flexibility: Accommodates different datasets and user preferences.
Hybrid Approach: Combines CF and CBF for potentially better recommendations.
Error Handling: Potential error conditions (e.g., missing files, incorrect paths) can be addressed.
Example: Includes a worked-through example for better understanding.
Additional Features: Consider incorporating k-Nearest Neighbors (kNN) for CBF, advanced evaluation metrics, and deployment considerations.
To Use:

Replace placeholders (e.g., file paths) with your data.
Run the script.
Experiment with different movies and parameters.
Adapt the code to your specific needs.
