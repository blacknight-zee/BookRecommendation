Book Recommendation System:          
A machine learning-based Book Recommendation System that uses K-Nearest Neighbors (KNN) and content-based filtering to suggest similar books based on user input. It includes detailed EDA, visualizations, and an interactive function to recommend books by title.

Features:      
1. Analyzes a dataset of popular books and ratings.
2. Recommends books similar to a given title using Nearest Neighbors algorithm.
3. Visualizes trends in ratings, reviews, and number of pages.
4. Performs feature engineering with:
5. Rating ranges
6. Language code
7. Normalized features (MinMaxScaler)

Dataset:  
books.csv (uploaded manually via files.upload() in Colab)  
Columns include:  
title, average_rating, ratings_count, num_pages, language_code, etc.  
Dataset Source: Kaggle   

Exploratory Data Analysis (EDA):  
1. Top 10 highest-rated books (with >1M reviews)
2. Most reviewed books overall
3. Distribution of average ratings
4. Correlation between ratings_count and average_rating
5. Visual relationship between average_rating and num_pages

Recommendation Logic:  
Feature Engineering:  
1. Categorical features: One-hot encoded (rating_between, language_code)
2. Numerical features: average_rating, ratings_count
3. Combined into a single feature set and normalized using MinMaxScaler

K-Nearest Neighbors Model:  
1. Trained using NearestNeighbors from Scikit-learn
2. Retrieves top 6 similar books based on feature similarity

Interactive Recommender Function:    
1. BookRecommender('Harry Potter and the Half-Blood Prince (Harry Potter  #6)')
2. Returns a list of similar book titles.
For example,  
['Harry Potter and the Half-Blood Prince (Harry Potter  #6)',
 "Harry Potter and the Order of the Phoenix (Harry Potter  #5)",
 "Harry Potter and the Goblet of Fire (Harry Potter  #4)",
 "Harry Potter and the Chamber of Secrets (Harry Potter  #2)",
 "Harry Potter and the Prisoner of Azkaban (Harry Potter  #3)",
 "Harry Potter and the Sorcerer's Stone (Harry Potter  #1)"]

To Run the Project:  
1. Upload the books.csv file via files.upload() in Google Colab.
2. Run the notebook cells step by step.
3. Use BookRecommender('Book Title') to get personalized book suggestions.
