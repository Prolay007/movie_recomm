Movie Recommendation System - Collaborative Filtering
Overview
This project is a Movie Recommendation System that uses Collaborative Filtering to suggest movies to users based on the ratings provided by similar users. The system leverages the K-Nearest Neighbors (KNN) algorithm with cosine similarity to find users with similar tastes and recommends movies accordingly.

The system is designed using the Surprise library, which provides efficient tools for building and evaluating recommender systems.

Features
User-Based Collaborative Filtering: Recommends movies to a user based on the preferences of other users who have similar tastes.
Movie Recommendation: Suggests top N movies that the user has not watched based on predicted ratings.
Performance Evaluation: Uses Root Mean Squared Error (RMSE) to evaluate the accuracy of predictions.
Customizable: The number of recommended movies (top N) and the similarity algorithm can be customized.
Technologies Used
Python: Core programming language.
Surprise Library: Used for building the collaborative filtering model.
Pandas: For loading and preprocessing the movie ratings dataset.
Scikit-learn: For additional machine learning utilities if needed.
How It Works
Data Loading: The system reads a dataset of user ratings for movies from a CSV file (ratings.csv). The dataset should have columns for userId, movieId, and rating.

Data Preparation: The ratings data is prepared for training the recommendation model using the Surprise library.

Collaborative Filtering:

The system uses user-based collaborative filtering, where similar users are identified based on their movie ratings using cosine similarity.
The model then predicts ratings for movies that the user hasn't watched, based on ratings from similar users.
Recommendations:

The system provides top N movie recommendations by predicting the highest ratings for movies the user has not yet rated.
Movies are recommended based on the predicted ratings calculated using KNN-based collaborative filtering.
Evaluation: The accuracy of the recommendation system is measured using Root Mean Squared Error (RMSE) by comparing predicted ratings to the actual user ratings in the test data.