# movie-recommendation-system
Movie recommendation system using collaborative filtering (KNN &amp; SVD) on MovieLens dataset


## Overview
This project builds a movie recommendation system using the **MovieLens 100k dataset**.  
The goal is to compare collaborative filtering approaches (KNN and matrix factorization) and generate personalized top-N movie recommendations.

## Dataset
- **Source:** MovieLens 100k (built-in from Surprise library)  
- **Users:** 943  
- **Movies:** 1,682  
- **Ratings:** 100,000 (1–5 scale)  

## Methodology
1. **Exploratory Data Analysis (EDA)**  
   - Rating distribution  
   - Median ratings per user and per movie  

2. **Models Implemented**  
   - **User-based KNN**: finds similar users and recommends what they liked  
   - **Item-based KNN**: recommends movies similar to those already rated  
   - **SVD (Matrix Factorization)**: learns latent factors for users and items  

3. **Evaluation Metrics**  
   - **RMSE**: how close predicted ratings are to actual ratings  
   - **Precision@10 / Recall@10**: quality of top-10 recommendations  

4. **Top-N Recommendations**  
   - Generated personalized top-10 movie recommendations per user  
   - Example recommendations included in notebook  

## Results
- **RMSE (lower is better):**  
  - KNN (user-based): ~X.XX  
  - KNN (item-based): ~Y.YY  
  - SVD: ~Z.ZZ (best)  

- **Precision@10 / Recall@10 (higher is better):**  
  - KNN (user-based): P=.., R=..  
  - KNN (item-based): P=.., R=..  
  - SVD: P=.., R=.. (best)  

- **Key Finding:**  
  The SVD model consistently outperformed KNN models in both rating accuracy (RMSE) and top-N recommendation quality.  

## Business Insights
- Collaborative filtering can personalize recommendations effectively with only user-item interactions.  
- Matrix factorization (SVD) is a strong baseline for production-ready recommenders.  
- For cold-start users/items, hybrid approaches (content + collaborative) would be the next step.  

## Visuals
<img width="567" height="435" alt="model_rmse_comparison" src="https://github.com/user-attachments/assets/96ec03f7-f30c-4b5c-9cf0-d28e5e383714" />
  


 <img width="576" height="435" alt="precision_at_10" src="https://github.com/user-attachments/assets/423a5c92-c82d-4553-b723-123565156b72" />


## Next Steps
- Address cold-start problem with hybrid methods (content + collaborative)  
- Experiment with implicit feedback (clicks, views)  
- Deploy as an interactive API or web app for real-time recommendations  

## How to Run
1. Open [Google Colab](https://colab.research.google.com/).  
2. Upload the notebook (`movie_recommender.ipynb`).  
3. Run all cells (MovieLens 100k dataset loads automatically via Surprise).  

---
