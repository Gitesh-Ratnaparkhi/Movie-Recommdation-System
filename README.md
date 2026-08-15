<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/4ad7736d-635b-4214-904f-766efa889483" />


# 🎬 Movie Recommendation System (Content-Based Filtering)

A machine learning-powered **Movie Recommendation System** built to suggest relevant films based on item metadata and content similarity. By analyzing features such as genres, cast, crew, keywords, and plot summaries, the system computes similarity scores between titles to deliver accurate, personalized recommendations without requiring prior user history.

---

## 📌 Project Overview

Traditional recommendation engines rely heavily on user behavior (**Collaborative Filtering**), which often struggles with the cold-start problem for new users. This project implements a **Content-Based Filtering** approach, focusing on intrinsic movie attributes to evaluate proximity across a multi-dimensional feature space.

* 🗃️ **Dataset:** TMDB 5000 Movies / MovieLens metadata (overviews, genres, keywords, cast, and director).
* 🧮 **Core Algorithm:** Text Vectorization (TF-IDF / Bag of Words) paired with **Cosine Similarity** scoring.
* 🖥️ **Interface:** Interactive web dashboard for real-time querying, recommendation lists, and poster rendering.

---

## ⚙️ How It Works

* 🧹 **Data Preprocessing & Cleaning:**
  * Extracts essential fields: `movie_id`, `title`, `overview`, `genres`, `keywords`, `cast`, and `director`.
  * Parses stringified JSON objects and cleans missing values.
  * Normalizes text by converting to lowercase, collapsing multi-word names (e.g., `Sam Worthington` -> `SamWorthington`), and applying stemming.

* 🏷️ **Tag Generation:**
  * Merges all processed attributes into a unified `tags` column per movie.

* 📐 **Vectorization:**
  * Converts textual tags into high-dimensional numerical vectors using `CountVectorizer` / `TfidfVectorizer` (filtering standard English stop words).

* 🎯 **Similarity Computation:**
  * Evaluates similarity using **Cosine Similarity**:
    $$\text{Cosine Similarity}(A, B) = \frac{A \cdot B}{\|A\| \|B\|}$$
  * Returns and ranks the top $k$ highest-scoring titles relative to the query movie.

---

## 🚀 Key Features

* 🎯 **Thematic Matching:** Delivers recommendations based on deep narrative and categorical overlap.
* ❄️ **Cold-Start Resilient:** Produces high-quality recommendations instantly without requiring user watch logs or ratings.
* 🔢 **Top-N Outputs:** Retrieves the top 5–10 closest matches ranked by similarity score.
* 🖼️ **Dynamic Visuals:** Fetches live movie posters and metadata via **TMDB API** integration.

---

## 🛠️ Tech Stack

* 🐍 **Language:** Python
* 📊 **Machine Learning & Data Processing:** Pandas, NumPy, Scikit-learn, NLTK
* 🌐 **Web Framework:** Streamlit / Flask
* 🔌 **API Integration:** The Movie Database (TMDB) API
* 💾 **Model Serialization:** Pickle

---

## 📥 Installation & Setup

```bash
# 1. Clone the repository
git clone [https://github.com/your-username/movie-recommendation-system.git](https://github.com/your-username/movie-recommendation-system.git)
cd movie-recommendation-system

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install required packages
pip install -r requirements.txt

# 4. Run the application
streamlit run app.py
