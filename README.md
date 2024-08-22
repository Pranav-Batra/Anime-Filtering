# Anime Recommendation System - Learning KNN and Scipy
Enter in an anime name and get recommendations based on your filtering system - based on https://www.youtube.com/watch?v=XfAe-HLysOM&t=3641s

# Description
A lot of this project comes from this video: https://www.youtube.com/watch?v=XfAe-HLysOM&t=3641s. I used different datasets and added in a little more functionality to the recommendations provided by the algorithm and had to do a little of data preprocessing as the datasets didn't come fully cleaned, but a lot of the filtering algorithms' code and EDA was from the tutorial. 

For content based filtering, I used a matrix based on the genres of each show. Each show's genres were vectorized, and cosine similarity was used to find the genre vectors most similar to the searched anime. I used fuzzywuzzy for title matching and cleaned data with pandas. I also included an option to remove all recommendations from the same series(i.e. if season 1 of a show is inputted, later seasons won't be recommended).

For collaborative filtering, I used KNN with a matrix of each user ID matched with all the animes they had rated. I used scipy's sparse matrix in order to fill all the empty values. From there, I used KNN with a cosine metric from scikitlearn. The algorithm would take the name of an anime, identify all the users who had rated it and what ratings they gave it, and then find the closest vectors to that anime based on the inputted sparse matrix. These vectors would represent n other anime, where n is the amount of recommendations asked for by the user. 

# Data
Link to the Kaggle dataset with the animes and ratings file. https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database

