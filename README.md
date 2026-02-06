# PCA Dimensionality Reduction on Digits Dataset

This project demonstrates how Principal Component Analysis (PCA) can be used to reduce high-dimensional image data while preserving important variance. The sklearn digits dataset is scaled, compressed using PCA, and evaluated using Logistic Regression.

---

## Dataset

The project uses the sklearn digits dataset where each image is flattened into a numerical feature vector.

---

## Explained Variance Analysis

PCA was applied with multiple component values (2, 10, 30, 50).  
The cumulative explained variance was tracked to understand how much information is retained as dimensions are reduced.

This helps in selecting an optimal number of components that balance compression and performance.

---

## Reduced Dataset

After identifying an effective number of principal components, the original high-dimensional dataset was transformed into a lower-dimensional representation using PCA.

This reduced dataset preserves most of the important variance while significantly lowering feature count.

---

## Accuracy Comparison Report

Two Logistic Regression models were trained:

• One using the original scaled dataset  
• One using the PCA-reduced dataset  

The classification accuracy of both models was evaluated and compared to measure the impact of dimensionality reduction.

The results show that PCA achieves strong compression with minimal loss in predictive performance.

---

## Technologies Used

- Python  
- Scikit-learn  
- Matplotlib  
- NumPy  

---

## Project Highlights

- Feature scaling for proper PCA performance  
- Multiple PCA configurations tested  
- Visualized variance retention  
- 2D PCA class separation plot  
- Performance comparison before and after reduction  

---

## What I Learned

Before using PCA, working with high-dimensional data felt heavy and slow, especially with image features. PCA helped solve that by compressing the dataset into fewer dimensions while still keeping most of the important information. It basically removes redundancy and makes models faster and easier to train.

While applying PCA, I understood explained variance as a way to measure how much information each principal component keeps from the original data. When the cumulative variance gets high (like 90–95%), it means the reduced dataset is still representing most of the original structure.

Scaling turned out to be really important because PCA depends on distances and variance. If features aren’t on the same scale, larger-value features dominate the components and the result becomes misleading.

I also realized PCA is different from feature selection. Feature selection keeps some original features and drops others, while PCA creates completely new transformed features that are combinations of the original ones.

One limitation of PCA is that it can make data harder to interpret since the new components don’t directly represent real features anymore. It also works best for linear patterns and may not capture complex nonlinear relationships.
