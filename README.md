# Movie-Recommender-System---Big-Data
Simple Movie Recommender System


PROBLEM SETTING:
Build a movie recommender system using the MovieLens dataset that aims at predicting movie ratings and recommending movies to users based on their average rating. We implement this with the technique of collaborative filtering.

DATA DESCRIPTION:
We have used the MovieLens Small and Full Datasets for the project containing Movies and Ratings files.
1. Small dataset: 100,000 ratings applied to 9000 movies by 600 users
2. Full dataset: 27,000,000 ratings applied to 58,000 movies by 280,000 users
File attributes are:
1. Movies: movieId, title
2. Ratings: userId, movieId, rating

DATA PREPROCESSING:
Loading and parsing the data:
Before working with the dataset, we first remove the headers that is present in the dataset as we do not need them.
1. For each line in the Movies dataset, we have created a tuple formatted as (movieId, title).
2. For each line in the Ratings dataset, we have created a tuple formatted as (userId, movieId, rating).

TECHNIQUES:
1. Model Based Collaborative Filtering
The first major step involved in this step is to predict the movie ratings for a particular user which the user has not rated yet. Later these predicted rating helps us tor recommend movies to users based.
2. Spark Mlib library for Machine Learning provides a collaborative filtering implementation by using Alternating Least Squares.

METHODOLOGY:
1. Load, examine and pre-process the data to create the required tuples.
2. The small dataset is selected to determine the ALS parameters. The data is split into train, validation and test datasets.
3. Select the best model with the least RMSE.
4. Applying the ALS parameters determined from the model obtained in step 2 to the full dataset.
5. Adding new user ratings RDD to the complete dataset RDD to frame a new RDD which will be the input to train our recommender model.
6. Obtain the highest rated recommendations.
7. Also, built an extra application where we could use the model to predict the rating of an individual given rating.
