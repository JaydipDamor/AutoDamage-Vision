# Week 2 – Problem Set (PCA & t-SNE)

## Problem 1 (Easy)
Why must data be mean-centered before applying PCA?
PCA identifies directions of maximum variance based on the covariance matrix. If data is not mean-centered, the first principal component may simply point toward the mean instead of capturing true variance patterns. Mean-centering ensures that PCA measures variation around the origin rather than absolute values. This allows principal components to represent meaningful directions of data spread, ensuring correct eigenvectors, accurate variance decomposition, and proper dimensionality reduction.

---

## Problem 2 (Medium)
PCA preserves variance but not class separability.  
Explain with an example.
PCA maximizes overall variance without considering class labels. For example, in a digit dataset, variations in handwriting thickness may dominate variance, while class-discriminating features (such as loops distinguishing 6 and 9) may have lower variance. PCA will prioritize thickness rather than class boundaries, causing different classes to overlap in reduced space. Thus, high variance directions are preserved, but class separability may be lost.

---

## Problem 3 (Hard)
t-SNE shows clean clusters, but classifiers perform poorly.  
Explain this paradox using high-dimensional geometry.
t-SNE shows clean clusters, but classifiers perform poorly. Explain this paradox using high-dimensional geometry.

t-SNE preserves local neighborhood relationships while distorting global distances. In high-dimensional spaces, distances become less meaningful due to the curse of dimensionality. t-SNE exaggerates small differences to create visually separable clusters, but these clusters do not represent true linear or global decision boundaries. Classifiers rely on consistent geometric structure, which t-SNE destroys, leading to poor generalization despite visually clean clusters.
