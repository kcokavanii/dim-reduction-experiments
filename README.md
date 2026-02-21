# Dimensionality Reduction Playground: From Theory to Practice

A comprehensive exploration of dimensionality reduction techniques (PCA, SVD, t-SNE, UMAP, LLE) and their real-world applications in recommendation systems, image compression, video analysis, and facial editing.

Notebook on Google Colab: https://colab.research.google.com/drive/1cTysi_2NMBYwPB6HDt69Ds8_VLZiYvrz?usp=sharing

## Overview
Through five hands-on experiments, I demonstrate how these techniques solve the "curse of dimensionality" and enable practical applications in computer vision and recommender systems.

# Key Experiments
## 1. Book Recommendation System
**Task:** Predict user age category from reading history

**Data:** Book-Crossing dataset (340k books, 105k users)

**Key finding:** SVD reduction from 340k to 500 features maintained accuracy (42%) while reducing training time by 60%

## 2. MNIST Visualization Showdown
**Task:** Compare 6 dimensionality reduction methods

**Results:**
  - t-SNE/UMAP: Best for visualization (silhouette scores: 0.235/0.258)
  - PCA/SVD: Fastest (0.04s), best global structure preservation
  - UMAP: Best balance of speed, local AND global structure

## 3. Image Compression via SVD
**Task:** Compress images with controlled quality loss

**Demo:** From k=1 (blurry) to k=150 (near-perfect), with compression ratio up to 20x at 95% variance

## 4. Video Background Extraction
**Task:** Separate static background from moving objects

**Method:** Low-rank SVD approximation (first 5-10 components = pure background)

## 5. Facial Expression Editing
**Task:** Add/remove smiles using PCA on LFW dataset

**Method:** Found "smile vector" as difference between smiling/neutral face projections → controllable expression editing
