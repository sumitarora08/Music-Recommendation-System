# Music-Recommendation-System
This project is a content-based music recommendation engine that suggests songs based on their lyrical similarity. The system leverages Natural Language Processing (NLP) to analyze song lyrics and provides a user-friendly web interface for discovering new music.

**Features**
Content-Based Filtering: Recommends songs by calculating the cosine similarity between TF-IDF vectorized song lyrics.

Interactive Web App: A Streamlit-based interface allowing users to select a song and instantly receive five similar recommendations.

Visual Enhancements: Integrates with the Spotify API to fetch and display real-time album artwork for recommended tracks.

Text Processing: Includes a full pipeline for data cleaning, lowercasing, and stemming using the NLTK library.

**Project Structure**
Model training.ipynb: The primary Jupyter Notebook used for data exploration, preprocessing (cleaning and stemming), and building the similarity matrix.
app.py: The Streamlit application script that serves the frontend and handles backend logic for recommendations and Spotify API integration.
spotify_millsongdata.csv: The source dataset containing over 57,000 songs, including artist names, song titles, and lyrics.
df.pkl & similarity.pkl: Serialized pickle files containing the processed dataframe and the pre-computed cosine similarity matrix for fast retrieval.

**Technical Stack**
Language: Python

**Libraries:**
Pandas: Data manipulation and analysis.
NLTK: Natural Language Toolkit for text tokenization and stemming.
Scikit-Learn: Implementing TF-IDF Vectorization and Cosine Similarity.
Streamlit: Framework for building the web application.
Spotipy: A lightweight Python library for the Spotify Web API.

**Implementation Details**
Data Preprocessing: The system takes a sample of 10,000 songs, removes irrelevant columns, and cleans the text by removing special characters and performing Porter Stemming.

Vectorization: The lyrics are transformed into a numerical format using TfidfVectorizer, which weights the importance of words across the entire dataset.

Similarity Calculation: A cosine similarity matrix is generated, representing how closely related every song is to every other song based on lyrical content.

Recommendation Engine: When a user selects a song, the system identifies its index, sorts the similarity scores, and retrieves the top five most similar tracks.
