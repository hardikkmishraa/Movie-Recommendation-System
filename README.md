# 🎥 Movie Recommendation System

## 📌 Project Overview

This project implements a **Movie Recommendation System** that suggests movies to users based on **similarity between movies**.

It uses **content-based filtering**, where recommendations are made by analyzing movie features instead of user ratings.

---

## 🧠 Problem Statement

With thousands of movies available, users often struggle to find content that matches their interests.

This project solves that problem by recommending movies that are **similar to a movie selected by the user**, based on movie metadata.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Natural Language Processing (NLP)

---

## 📂 Dataset

The dataset contains information about movies such as:

- Movie Title
- Genres
- Keywords / Overview
- Cast
- Crew

These attributes are used to understand movie content and calculate similarity.

---

## 🔄 Workflow

1. Load and clean movie dataset
2. Select important features
3. Combine features into a single text representation
4. Convert text into numerical vectors
5. Calculate similarity between movies
6. Recommend top similar movies

---

## ⚙️ Working of the Movie Recommendation System

### 1️⃣ Data Loading

The movie dataset is loaded using **Pandas**.

Unnecessary or missing values are handled to ensure clean data.

---

### 2️⃣ Feature Selection

Important columns such as:

- Genres
- Keywords
- Overview
- Cast
- Crew

are selected because they describe the **content of a movie**.

---

### 3️⃣ Feature Combination

All selected features are combined into **one single text string** for each movie.

This creates a unified representation of the movie’s content.

Example:

```
Action Adventure hero battle war

```

---

### 4️⃣ Vectorization

The combined text data is converted into numerical form using **CountVectorizer**.

- Each movie becomes a vector
- Each word represents a feature
- Frequency of words is counted

This allows mathematical comparison between movies.

---

### 5️⃣ Similarity Calculation

**Cosine Similarity** is used to calculate how similar two movies are.

- Value ranges from 0 to 1
- Higher value = more similar movies

A similarity matrix is created where each movie is compared with every other movie.

---

### 6️⃣ Recommendation Generation

When a user enters a movie name:

1. The system finds that movie in the dataset
2. Retrieves similarity scores
3. Sorts movies based on similarity
4. Returns the **top recommended movies**

---

## ▶️ How to Run

1. Clone the repository:
    
    ```bash
    gitclone <repository-url>
    
    ```
    
2. Open the notebook:
    
    ```bash
    jupyter notebook Movie_recommendation.ipynb
    
    ```
    
3. Run all cells sequentially
4. Enter a movie name to get recommendations

---

## ✨ Example Output

Input:

```
Avatar

```

Output:

```
1. Guardians of the Galaxy
2. Star Trek
3. John Carter
4. Interstellar
5. Avengers

```

---

## 📌 Applications

- OTT platforms (Netflix, Prime Video)
- Movie streaming websites
- Personalized content recommendation
- Entertainment analytics

---

## 🚀 Future Enhancements

- Add **collaborative filtering**
- Use **TF-IDF Vectorization**
- Integrate user ratings
- Build a web interface using Flask or Streamlit
