# IBM Community Recommendation Engine - using Unsupervised learning

## Executive Summary
This project develops a multi-strategy recommendation system for the IBM Watson Studio community. By analyzing user-article interactions, the system personalizes the discovery of assets (notebooks, datasets, and articles) to reduce search friction and improve user engagement.

## Business Case
In a vast ecosystem of technical assets, users often face "choice paralysis." This engine implements a tiered fallback logic to ensure every user—from a first-time visitor to a power user—receives relevant content:

1. **New Users (Cold Start):** Rank-based recommendations using global popularity.
2. **Intermediate Users:** Content-based filtering using NLP (TF-IDF & K-Means) to find similar articles.
3. **Power Users:** Collaborative filtering (SVD & User-User) to leverage community-wide interaction patterns.

## Technical Stack
- **Data:** User-Item Interaction logs from IBM Watson Studio.
- **NLP:** TF-IDF Vectorization and Latent Semantic Analysis (SVD).
- **ML:** K-Means Clustering for content grouping and Matrix Factorization for predictive modeling.
- **Deployment:** [Future] Streamlit web application.  Consider ??? 

## Key Takeaways and Results 



## Starer 