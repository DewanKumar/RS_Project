# ShopSense – E-commerce Recommendation System

This project is a **Hybrid Product Recommendation System** developed as part of an academic project. It demonstrates how **content-based filtering** and **collaborative filtering** can be combined to recommend products in an **e-commerce environment**.

---

## Project Overview
Recommender systems are widely used in e-commerce platforms to improve **user experience** and **sales conversions**.
The goal of this project is to suggest relevant products to users by combining:
  - **Content-based filtering (CBF):** Uses the category hierarchy (category_tree.csv) to compute item-to-item similarity with cosine similarity.
  - **Collaborative filtering (CF):** Learns user–item relationships from purchase/rating data using ALS (Alternating Least Squares) and the Surprise library (SVD, KNN).
  - **Hybrid approach:** Combines both methods to overcome cold-start problems and improve accuracy.
Our implementation is provided in a Jupyter Notebook:
`Rs_Project (1).ipynb`

---

## Features
 - Builds a category-based similarity model using cosine similarity.
 - Implements collaborative filtering for personalized recommendations.
 - Supports both implicit feedback (purchases) and explicit feedback (ratings).
 - Provides a hybrid scoring function combining CBF and CF.
 -  Evaluates recommendations with Precision@K, Recall@K, RMSE, and MAE.

---

## Purpose
 - The main objectives of this project are to:
 - Explore real-world recommendation techniques in e-commerce.
 - Understand the strengths and limitations of content-based and collaborative approaches.
 - Develop a hybrid system that handles data sparsity and cold-start challenges.
 - Provide a foundation for future enhancements such as popularity-based re-ranking and interactive demos.

---

## Implementation Details
- **Language/Tools:** Python, Jupyter Notebook
- **Libraries Used:**
     - `pandas`, `numpy`, `scikit-learn`
     - `implicit` (ALS for implicit feedback)
     - `scikit-surprise` (SVD/KNN for ratings)
- **Dataset:**
     - `category_tree.csv` (categoryid, parentid) for content-based similarity
     - User–item interactions (purchase/rating data) used inside the notebook
- **Algorithm Steps:**
   - Build product similarity matrix from category tree (CBF).
   - Train collaborative models (ALS/SVD).
   - Blend predictions using hybrid formula.
   - Rank and recommend top-N items for each user.
   - Evaluate with ranking and rating metrics.
 
---

## Output

 - **Content-based filtering:** Returns top-N items similar to a product based on category.
 - **Collaborative filtering:** Returns top-N items personalized for a user.
 - **Hybrid system:** Combines both, achieving higher accuracy and reducing cold-start issues.

---

## Future Enhancements
   - Add **user input** for interactive recommendation queries.
   - Implement **popularity & diversity re-ranking**.
   - Use **deep learning embeddings** for categories and products.
   - Build a **Streamlit web demo** to visualize recommendations interactively.

