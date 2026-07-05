# 📰 Document Clustering & Topic Discovery

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-NLP-green?style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Unsupervised-FF4F8B?style=for-the-badge)

## 📌 Project Overview
This repository contains the source code and documentation for **Minor Project 2**. The objective of this project is to solve a real-world Natural Language Processing (NLP) problem using an **Unsupervised Machine Learning** approach. 

Specifically, this project applies **K-Means Clustering** to automatically categorize and discover hidden thematic topics within a vast corpus of unlabelled news articles, demonstrating the ability to organize unstructured text data without human intervention.

## 🗄️ Dataset
* **Source:** `bbc_news.csv`
* **Description:** The dataset comprises news article headlines and their corresponding brief descriptions. 
* **Note:** To maintain the strict requirements of unsupervised learning, all potential categorical labels were stripped prior to model training.

## ⚙️ Machine Learning Pipeline

### 1. Advanced Data Preprocessing
* **Text Normalization:** Removal of punctuation, special characters, and numbers using Regular Expressions (Regex).
* **Lemmatization:** Reduced words to their base linguistic root using the `WordNetLemmatizer` (NLTK) to improve semantic grouping.
* **Feature Encoding:** Converted unstructured text into a numerical matrix using **TF-IDF (Term Frequency-Inverse Document Frequency)**, prioritizing highly relevant terms while penalizing frequent but uninformative filler words.

### 2. Model Development
* **Algorithm:** K-Means Clustering
* **Configuration:** Initialized with `k=5` distinct clusters based on domain estimation and optimization parameters (`n_init=10`).

### 3. Model Evaluation
The model's structural integrity and separation capabilities were validated using three rigorous internal metrics:
* **Silhouette Score:** Measures cluster cohesion versus separation.
* **Davies-Bouldin Index:** Evaluates the average similarity ratio between clusters.
* **Calinski-Harabasz Index:** Assesses cluster validity based on dispersion between versus within clusters.

## 📊 Visualizations
Because the vectorized text data contains hundreds of dimensions, **Principal Component Analysis (PCA)** was utilized to perform dimensionality reduction. 

The project generates high-quality, publication-ready graphics using `seaborn`:
1. `Document Clusters Visualized in 2D Space (PCA).png`: A 2D spatial representation of the clustered documents.<img width="402" height="257" alt="Document Clusters Visualized in 2D Space (PCA)" src="https://github.com/user-attachments/assets/b6b45972-dc60-4dbd-acdf-41ed8d18c85a" />

2. `Distribution of Documents Across Clusters.png`: A bar chart illustrating the volume of articles assigned to each discovered topic.
<img width="599" height="355" alt="Distribution of Documents Across Clusters" src="https://github.com/user-attachments/assets/8d198072-5c20-40d0-b69e-d1aec99aada6" />

## 🚀 How to Run

1. Ensure the `bbc_news.csv` dataset is located in the root directory.
2. Install the required dependencies:
   ```bash
   pip install pandas numpy scikit-learn nltk matplotlib seaborn

  
