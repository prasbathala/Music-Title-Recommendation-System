# Music-Title-Recommendation-System

This repository consists of the implementation of a music recommendation system. We have analyzed various techniques and processed as much as possible for the recommendation system.

Pipeline for this project

  1. Performed Exploratory Data Analysis to identify how skewed the data is, and to identify the correlation between the users and the products.
  2. First we implemented a Content Based recommendation System, where we recommned similar music titles to which the user has liked.
  3. Secondly, we implemented a Collabrative Recommender System, where we implemented Memory-based system, and model based system.
        i. In Memory Based System, we consider a pivot table between the products and users and their corresponding ratings. In the memory based recommender system, we just use this data and compute the similarity score recommend similar products for a particular product.
        ii. In Model Based System, we performed a technique called matrix factorization with the help of library called [Surprise](https://surprise.readthedocs.io/en/stable/index.html). We used GridSearch CV to identify how many latent factors to be considered for the factorization. once we get the optimal value from the gridsearch CV method, we trained the model and predicted the ratings of products which the user has not predicted.
        
        With respect to Model Based System, we also implemented a AutoEncoder (AE) approach to recommend music titles. For this we used Restrcited Boltzmann Machines (RBM) with the visible layer being Gaussian distribution and hidden layer being Bernouli distribution. Since, we modeled the output layer to be bernouli random variable, we were not able to get the score of a particular recommended product.
