# 📚 Book Recommendation System

This project implements a complete **Book Recommendation System** using the **Book-Crossing dataset**. It combines **Collaborative Filtering**, **K-Means Clustering**, and a **Hybrid approach** to provide personalized and diverse book recommendations.

---

## 📋 Project Overview

A Jupyter Notebook–based recommendation engine that:

* Loads and preprocesses book, user, and rating data
* Builds a collaborative filtering model using **cosine similarity**
* Applies **K-Means clustering** on rating patterns
* Prioritizes books by the **same author**, sorted by average rating
* Evaluates models using **diversity** and **quality** metrics
* Provides a **hybrid recommendation system** combining both models

---

## 📊 Dataset

The system uses the **Book-Crossing Dataset**, composed of three CSV files:

* **`Books.csv`** – Book metadata (ISBN, title, author, year, publisher)
* **`Users.csv`** – User information (user ID, location, age)
* **`Ratings.csv`** – User ratings (user ID, ISBN, rating 0–10)

> **Note**
> Explicit ratings range from **1–10**. A rating of **0** indicates implicit feedback (the book was interacted with but not explicitly rated).

---

## 🛠️ Requirements

Create a virtual environment (optional but recommended), then install dependencies:

```txt
pandas
numpy
matplotlib
seaborn
scikit-learn
```

Install all dependencies with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 🚀 How to Run

1. Place the three CSV files (`Books.csv`, `Users.csv`, `Ratings.csv`) in the same directory as the notebook.
2. Open **`book-recommendations.ipynb`** in Jupyter Notebook, JupyterLab, or VS Code.
3. Run all cells sequentially to:

   * Load and preprocess the data
   * Train the models
   * Generate and evaluate recommendations

---

## 🧪 Example Usage (Python)

```python
# Collaborative Filtering Recommendations
recommend('1984')

# K-Means Clustering Recommendations
recommend_kmeans('The Notebook')

# Hybrid Recommendations (combines both models)
recommend_hybrid("Harry Potter and the Sorcerer's Stone (Book 1)")
```

---

## 🔍 Models Implemented

### 1. Collaborative Filtering (Cosine Similarity)

* Builds a **user–item rating pivot table**
* Computes **cosine similarity** between books
* Recommends books with similar rating patterns

**Strength**: High thematic relevance and personalization

---

### 2. K-Means Clustering

* Clusters books based on their rating profiles
* Uses the **silhouette score** to select the optimal number of clusters
* Recommends books from the same cluster

**Strength**: Encourages exploration and diversity

---

### 3. Hybrid Model

* Merges results from collaborative filtering and K-Means
* Highlights books recommended by **both models** (high confidence)
* Produces broader and more robust recommendations

---

## ✨ Additional Features

* Always prioritizes **top-rated books by the same author**
* Gracefully handles books not found in the dataset
* Model evaluation based on:

  * **Diversity**: Number of unique authors recommended
  * **Quality**: Average rating of recommended books

---

## 📈 Evaluation

The notebook compares models using the following metrics:

| Metric              | Description                                 |
| ------------------- | ------------------------------------------- |
| Diversity (Authors) | Number of unique authors in recommendations |
| Quality             | Average user rating of recommended books    |

**Observation:**

* Collaborative Filtering usually provides higher thematic relevance
* K-Means promotes broader discovery
* The Hybrid model balances both quality and diversity

---

## 📂 Project Structure

```text
.
├── book-recommendations.ipynb   # Main notebook with full implementation
├── Books.csv                    # Book metadata
├── Users.csv                    # User information
├── Ratings.csv                  # User ratings
├── README.md                    # Project documentation
└── requirements.txt             # Python dependencies (optional)
```

---

## 🤝 Contributing

Contributions are welcome! You can:

* Fork the repository
* Open issues for bugs or feature requests
* Submit pull requests (e.g., better preprocessing, new models, or a web app version)

---

## 📄 License

This project is open-source and licensed under the **MIT License**.

---

📖 **Happy reading — may your next book be your new favorite!** ✨
