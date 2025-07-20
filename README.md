
# 🎬 AI-Based Movie Recommender System

![banner](https://github.com/sonusinha1707/Movie_Recommender_system/blob/main/Movie_Recommender_system.png)

This project is a **content-based movie recommender system** built using **Python**, **Pandas**, **Scikit-learn**, and **Streamlit**. It suggests similar movies based on the one you choose from a list, using a similarity matrix and movie metadata. The system also fetches and displays movie posters using the **TMDb API**.

---

## 📁 Project Structure

```
├── Movie_Recommender_System.ipynb     # Jupyter notebook for data preprocessing and model creation
├── web_application_code.py            # Streamlit app for user interface
├── movie_dict.pkl                     # Pickle file storing processed movie data
├── similarity.pkl                     # Pickle file storing similarity matrix (not uploaded here)
└── README.md                          # Project documentation (you are here)
```

---

## 🚀 Features

- 📌 **Content-Based Filtering**: Uses cosine similarity to recommend top 5 movies similar to the selected one.
- 🧠 **Precomputed Similarity Matrix**: Enables lightning-fast recommendations.
- 🖼️ **Dynamic Poster Fetching**: Retrieves posters for recommended movies from **TMDb** API.
- 💡 **Interactive UI**: Built with Streamlit for easy use and fast deployment.

---

## 🧪 How It Works

1. The system loads a preprocessed dataset of movies from `movie_dict.pkl`.
2. It uses a **cosine similarity matrix** (`similarity.pkl`) to find related movies based on titles.
3. When the user selects a movie and clicks **Recommend**, the app:
   - Fetches the top 5 most similar movies.
   - Retrieves each movie’s poster from the TMDb API.
   - Displays the recommended titles with their posters in a grid layout.

---

## 🛠️ Installation & Usage

### ✅ Prerequisites

- Python 3.7+
- API key from [TMDb](https://www.themoviedb.org/)
- Install required packages:

```bash
pip install streamlit pandas scikit-learn requests
```

### ▶️ Run the Web App

Make sure you have `movie_dict.pkl` and `similarity.pkl` in the same directory as your script.

```bash
streamlit run web_application_code.py
```

Then, open the provided localhost URL in your browser.

---

## 🔐 TMDb API Key

The app uses TMDb to fetch movie posters. You must replace the placeholder API key in the script (`web_application_code.py`):

```python
# Replace with your own TMDb API key
url = "https://api.themoviedb.org/3/movie/{}?api_key=YOUR_API_KEY"
```

You can get an API key from the [TMDb Developer Portal](https://developers.themoviedb.org/3/getting-started/introduction).

---

## 📓 Notebook Usage

The Jupyter Notebook `Movie_Recommender_System.ipynb` includes:

- 📊 Data loading & cleaning
- 🧩 Feature engineering (e.g., genres, keywords)
- 🗣️ Text vectorization with CountVectorizer or Tfidf
- 🧠 Cosine similarity matrix creation
- 💾 Saving `movie_dict.pkl` and `similarity.pkl`

---

## 🌱 Future Improvements

- ✅ Add user ratings or hybrid filtering
- ✅ Include genre/category filters
- ✅ Pagination or scrollable UI for more recommendations
- ✅ Deploy using Heroku, AWS, or Streamlit Cloud

---

## 🤝 Acknowledgments

- [TMDb API](https://developers.themoviedb.org/)
- [Scikit-learn](https://scikit-learn.org/)
- [Streamlit](https://streamlit.io/)

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
