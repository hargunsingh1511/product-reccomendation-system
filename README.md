## Product-reccomendation-system


# Overview
The Product Recommendation System leverages machine learning algorithms to provide personalized product suggestions based on user behavior, such as browsing and purchase history. It uses collaborative filtering and content-based methods to enhance the shopping experience and drive sales for e-commerce platforms.

# Dataset
The system uses an Amazon dataset of user ratings for electronic products, available [here](https://www.kaggle.com/datasets/vibivij/amazon-electronics-rating-datasetrecommendation/download?datasetVersionNumber=1). To minimize bias, products and users are assigned unique identifiers instead of names.

Additional datasets can be found [here](https://jmcauley.ucsd.edu/data/amazon/).

# Approach
# 1.  Rank-Based Product Recommendation

Objective: Recommend popular products to new customers and solve the cold start problem. 
Method:            
    Calculate average and total ratings for each product.
    Sort products by average rating.
    Recommend the top 5 products with at least 50/100 ratings.
# 2.  Similarity-Based Collaborative Filtering

- Objective: Provide personalized recommendations by finding similar users.
- Method:
    Convert user IDs to integers.
    Compute similarity scores between users using cosine similarity.
    Recommend products interacted with by similar users but not by the original user.
 # 3.  Model-Based Collaborative Filtering

Objective: Offer personalized recommendations addressing sparsity and scalability challenges.
Method:
    Convert rating matrix to a compressed sparse row (CSR) matrix.
    Perform Singular Value Decomposition (SVD) to reduce dimensionality.
    Calculate predicted ratings and recommend top 5 products based on these ratings.
Evaluation:
    Compare average actual and predicted ratings.
    Compute RMSE to assess model accuracy.
