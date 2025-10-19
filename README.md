# 🎬 Netflix Exploratory Data Analysis

**Goal:**  
Analyze Netflix’s movie and TV show catalog to uncover content trends, genre diversity, ratings, and regional production patterns — plus build a lightweight model to classify titles by type.

---

## 📊 Dataset
- Source: [Netflix Movies and TV Shows (Kaggle)](https://www.kaggle.com/shivamb/netflix-shows)  
- Records: 8,807 titles  
- Columns: type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description  

---

## 🧹 Data Cleaning
- Parsed `date_added` → extracted `year_added`  
- Normalized ratings (`TV PG` → `TV-PG`)  
- Split `duration` into **minutes** (movies) & **seasons** (TV)  
- Filled missing text fields (`director`, `cast`, `country`)  
- Added `content_age = 2025 − release_year`  

---

## 📈 Key Analyses
| Topic | Description |
|-------|--------------|
| 🌍 Countries | U.S., India, U.K. lead Netflix’s catalog |
| 🎞 Movies vs TV | Movies still dominate, but TV share rising since 2015 |
| 🔢 Ratings | Adult-oriented ratings (TV-MA, TV-14) are most common |
| 📅 Trends | Rapid growth 2015-2020, TV > Movies from 2018 |
| 🎭 Genres | Dramas, Comedies, Documentaries top; strong international mix |
| 🔥 Genre × Type | Docuseries & Kids’ TV → TV shows; Dramas & Docs → Movies |
| ⏱ Content Length | Movies ≈ 100 min; most TV shows = 1 season |
| 🤖 NLP Model | TF-IDF + LogReg (~72–80 % accuracy) predicts type from description |

---

## 🧠 Insights
- Netflix’s focus has shifted toward episodic content post-2015.  
- Global diversity ↑ — India, Japan, Korea contribute heavily.  
- Mature-audience content forms majority of releases.  
- Descriptive text alone carries strong signal about content type.  

---

## ⚙️ How to Run
```bash
pip install -r requirements.txt
jupyter notebook netflix_eda.ipynb
