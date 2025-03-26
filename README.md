# Movie Recommendation System using MinHash and LSH

This project explores user behavior in a UK-based video-on-demand platform and builds a scalable movie recommendation system using MinHash and Locality Sensitive Hashing (LSH).

---

## Dataset

We used the `vodclickstream_uk_movies_03` dataset, which contains anonymized user clickstream data, including timestamps, user IDs, and movie titles.

---

## Objectives

- Understand user preferences through exploratory data analysis (EDA)
- Build a recommendation system based on user similarity using MinHash and LSH
- Evaluate recommendation quality using Jaccard similarity with a train/test split approach
- Engineer meaningful user-level features

---

## Exploratory Data Analysis (EDA)

Key visualizations include:

- **Top 10 Most Clicked Movies**: A bar chart showing the most popular content across all users.
- **Click Distribution**: Histogram of total clicks per movie to understand long-tail behavior.

---

## Feature Engineering

For each user, we extracted the following features:

| Feature                             | Description                                        |
|-------------------------------------|----------------------------------------------------|
| `user_id`                           | Anonymized unique identifier                      |
| `favorite_genre`                    | Genre most frequently clicked                     |
| `total_clicks_count`                | Total number of clicks made by the user           |
| `number_of_unique_movies_watched`  | How many different movies the user interacted with|
| `favourite_movie`                   | The movie with the most clicks for the user       |
| `most_active_month`                | The month with the highest user activity          |

---

## Recommendation System

Use MinHash to represent each user’s movie preferences as a compact signature, and LSH to efficiently find users with similar tastes.

### Steps

1. For each user, build a MinHash signature of their top-clicked movies.
2. Use LSH to find similar users.
3. Recommend movies watched by similar users that the target user hasn’t seen yet.

---

## Evaluation

Evaluate recommendations using Jaccard similarity between the system's recommendations and a held-out test set of the user's actual preferences (train/test split). Metrics include:

- Average Jaccard similarity score over a sample of users
- Proportion of users with successful recommendations

---

## Technologies Used

- Python (Pandas, NumPy, Matplotlib/Seaborn)
- [Datasketch](https://ekzhu.github.io/datasketch/) for MinHash and LSH
- Jupyter Notebooks for development and visualization
