# ADM-HW4

### This is the repository dedicated to Homework 4 for ADM course. 
#### Group 31 - Zhansaya Jumasheva.

- [__`main.ipynb`__]( ): - contains answers to Questions 1 and 2

# Project Description

This Python project focuses on building a recommendation system using Locality-Sensitive Hashing (LSH) algorithm based on user clickstream data from the provided dataset "vodclickstream_uk_movies_03.csv".

## Recommendation System using LSH Algorithm

### 1.2 Minhash Signatures

Utilizing movie genre and user_ids, the project implements min-hash signatures to group users with similar interests in a genre into the same bucket. 

### 1.3 Locality-Sensitive Hashing (LSH)

Once the buckets are prepared, the project proceeds with executing queries. Given specific user_ids, the system recommends at most five movies for the user to watch, based on movies clicked by similar users. The recommendation procedure involves:

- Identifying the two most similar users to the target user.
- Recommending movies based on the total number of clicks by these similar users, prioritizing common movies.
- Proposing the most clicked movies by the most similar user first, followed by the other user.

### Clustering Algorithms

To further enhance the recommendation system, clustering algorithms are employed to group Netflix users with similar preferences.

#### 2.1 Getting Your Data + Feature Engineering

Accessing the provided dataset, the project conducts feature engineering to enrich the dataset with meaningful features for each user. This involves:

Grouping data by user_id to create new features, including:
  a) **Favorite Genre:** Calculated as the genre with the highest total duration of clicks by the user.
  b) **Total Clicks Count:** The total number of clicks made by the user.
  c) **Unique Movies Watched:** The number of unique movies watched by the user.
  d) **Favorite Movie:** The movie with the highest total duration of clicks by the user.
  e) **Most Active Month:** The month in which the user is most active, based on the mode of click timestamps.

## Conclusion

This project aims to develop a recommendation system utilizing the LSH algorithm and feature engineering techniques to provide personalized movie recommendations to users based on their interests and behaviors. By implementing minhash signatures and LSH, along with extensive feature engineering, the system enhances user experience by offering relevant and tailored movie suggestions.
