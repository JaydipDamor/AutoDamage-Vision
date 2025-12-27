# 📂 Dataset Guide for Week 2 (PCA & t-SNE Tasks)

For both **PCA** and **t-SNE** notebooks, we will use a **single, simple, and standardized dataset** so that everyone focuses on **concepts and math**, not data collection.

---

## ✅ Dataset Chosen: **Fashion-MNIST**

### What is Fashion-MNIST?
Fashion-MNIST is a dataset of grayscale images of clothing items such as shirts, shoes, coats, and bags.

- Each image is **28 × 28 pixels**
- Each image belongs to **1 of 10 classes**
- Each image can be viewed as a **784-dimensional vector**

This makes it **perfect for PCA and t-SNE**, which are designed for **high-dimensional data**.

---

## 🎯 Why We Are Using This Dataset
- No manual download required
- High-dimensional (good for PCA math intuition)
- Labels available (useful for visualization)
- Fast to run on CPU
- Widely used in ML education

---

## 📥 How to Load the Dataset (IMPORTANT)

You **do not need to download anything manually**.

Fashion-MNIST comes built-in with TensorFlow/Keras.

In BOTH notebooks (`week2_pca_task.ipynb` and `week2_tsne_task.ipynb`), use:

```python
from tensorflow.keras.datasets import fashion_mnist

(X_train, y_train), (_, _) = fashion_mnist.load_data()

