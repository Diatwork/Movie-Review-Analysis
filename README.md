# 🎬 Movie Review Analysis: Impact of User and Critic Reviews on Movie Release

This project explores how audience and critic reviews influence the release trends of movies. We leveraged the **DistilBERT** transformer model to perform sentiment analysis on web-scraped **IMDB user reviews** and **Rotten Tomatoes critic reviews**, followed by insightful visualizations on trends across genres and years (2010–2020).

---

## 📌 Objective

To determine the **influence of critic vs. user reviews** on movie production and release decisions, and identify **genre-specific trends** in audience and critic sentiments.

---

## 📊 Datasets Used

| Source            | Description                                                       |
|-------------------|-------------------------------------------------------------------|
| Kaggle (RT)       | Rotten Tomatoes Critic Reviews + Movie Metadata                  |
| Kaggle (IMDB)     | IMDB User Reviews (Web Scraped ~28,600 Reviews)                  |
| TMDB API          | Additional movie metadata (e.g., actors, release info, genres)    |

---

## 🧠 Methodology

### 1. **Data Collection**
- Rotten Tomatoes critic reviews (~10 million)
- IMDB user reviews (web scraped, 25 reviews/movie)
- Movie metadata from TMDB and Kaggle

### 2. **Database Management**
- MongoDB used for NoSQL storage and management
- Stored raw, unstructured data in flexible JSON format

### 3. **Preprocessing Steps**
- Dropped irrelevant/missing data and duplicates
- Converted dates to uniform `yyyy-mm-dd` format
- Sorted data by release date

### 4. **Sentiment Analysis**
- Used `DistilBERT` from Hugging Face Transformers
- Labels: 0 = Negative, 1 = Positive
- Confidence scores used for filtering reliable sentiments
- Model fine-tuned with:
  - 2 epochs
  - Batch size: 8
  - Adam optimizer with learning rate `2e-5`

### 5. **Visualization**
- Sentiment trends by **genre/year**
- Impact of reviews on **movie release volume**
- Actor-specific genre trends (e.g., Robert Downey Jr.)
- Seasonal patterns in genre popularity

---

## 🔍 Key Findings

- Positive reviews significantly influence release volumes, especially in **Drama**, **Sci-Fi**, and **Thriller** genres.
- Notable decline in **Romance** releases aligns with fall in positive sentiment.
- Seasonal and genre-based spikes observed over 10 years.

---

## 🛠️ Tools and Libraries

- **Python**, **Jupyter Notebook**
- **Pandas**, **Matplotlib**, **Seaborn**
- **BeautifulSoup** (for web scraping)
- **Hugging Face Transformers** (`DistilBERT`)
- **MongoDB** (for storage)

---

## 🔮 Future Work

- Integrate Twitter/X reviews for more real-time sentiment signals.
- Compare different transformer models like RoBERTa or DeBERTa.
- Automate scraping pipelines and integrate live data APIs.

---

## 🧑‍💻 Contributors

- **Madni Ali Hussain** – [x23158859@student.ncirl.ie](mailto:x23158859@student.ncirl.ie)  
- **Gaurav** – [x23189487@student.ncirl.ie](mailto:x23189487@student.ncirl.ie)  
- **Diya Srivastava** – [x23177608@student.ncirl.ie](mailto:x23177608@student.ncirl.ie)

---

## 📚 References

- Hugging Face: [DistilBERT Sentiment Model](https://huggingface.co/sarahai/movie-sentiment-analysis)
- Rotten Tomatoes Dataset: [Kaggle - Stefanoleone](https://www.kaggle.com/datasets/stefanoleone992/rotten-tomatoes-movies-and-critic-reviews-dataset)
- IMDB User Reviews: [Kaggle - Jai Dalmotra](https://www.kaggle.com/datasets/jaidalmotra/movies-review)
- TMDB API: [The Movie Database](https://developer.themoviedb.org/)

---

## 📂 Repository Structure
