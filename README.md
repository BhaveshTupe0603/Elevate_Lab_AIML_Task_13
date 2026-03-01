# 📉 Task 13: PCA Dimensionality Reduction

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit_Learn-orange?logo=scikit-learn)

## 📖 Overview
**Task 13** explores **Unsupervised Dimensionality Reduction**. We used **PCA (Principal Component Analysis)** to compress the 64-feature Digits dataset while retaining 95% of the useful information.

## ⚙️ Workflow
1.  **Scaling:** Applied `StandardScaler` (Crucial step for PCA).
2.  **Variance Analysis:** Plotted Cumulative Explained Variance to find the optimal number of components.
3.  **Transformation:** Reduced dimensions from **64 → ~40**.
4.  **Comparison:** Trained Logistic Regression on both Original and Reduced datasets to verify performance retention.

## 📊 Key Results
* **Compression:** Reduced feature count by **~37%** while retaining **95%** variance.
* **Accuracy:** The model trained on reduced data performed nearly identical to the full model, proving that PCA successfully removed noise without losing signal.

## 🖼️ Visualizations
| Variance Plot | 2D Projection |
| :---: | :---: |
| <img width="846" height="547" alt="image" src="https://github.com/user-attachments/assets/c403255b-feb5-488c-8eb3-12a4ed0e5ee7" />| <img width="991" height="790" alt="image" src="https://github.com/user-attachments/assets/9037ca0e-5dd9-45e2-9341-b912ed46a380" />|

## 📂 Deliverables
* [📓 Jupyter Notebook](./Task 13.ipynb)
