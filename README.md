# IBM Community Recommendation Engine - using Unsupervised learning

## Executive Summary
This project develops a multi-strategy recommendation system for the IBM Watson Studio community. By analyzing user-article interactions, the system personalizes the discovery of assets (notebooks, datasets, and articles) to reduce search friction and improve user engagement.

## Business Case
In a vast ecosystem of technical assets, users often face "choice paralysis." This project aims to connect users to the most relevent articles they should be reading. Machine learning / unsupervised is a great use case to find "neighbours" that read similar articles, and then show a user what articles they should be reading (but have'nt yet). 

This engine implements a tiered fallback logic to ensure every user—from a first-time visitor to a power user—receives relevant content:

1. **New Users (Cold Start):** Rank-based recommendations using global popularity.
2. **Intermediate Users:** Content-based filtering using NLP (TF-IDF & K-Means) to find similar articles.
3. **Power Users:** Collaborative filtering (SVD & User-User) to leverage community-wide interaction patterns.

The approach taken has many business applications; essentially we are looking at users and finding who is most similar to them (in this case in regards to articles). In finance, we could use this technique when considering create scores or borrowing rise, marketing segments and/or risk of churn. 

## Technical Stack
- **Data:** User-Item Interaction logs from IBM Watson Studio.
- **NLP:** TF-IDF Vectorization and Latent Semantic Analysis (SVD).
- **ML:** K-Means Clustering for content grouping and Matrix Factorization for predictive modeling.
- **Deployment:** [Future] Streamlit web application.  Consider ??? 

## Key Takeaways and Results 

The methodoology when looking at user similairy was creating a very large matrix with binary results. This simple layout allowed a similarity measure to be applied, in our case we looked at a dot-product method for overlap and then a Cosine similarity (which is essentially a normalized dot product). Doing it this way, we also had to be careful to not compare each user to themselves, as that will have a perfect similarity. 

## Starer 



## Futuer implimentations
A next stage implimentation could involve A/B Testing to measrue the click through rates for users (??)