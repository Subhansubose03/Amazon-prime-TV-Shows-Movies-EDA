<div align="center">

# 🎬 Amazon Prime Video: TV Shows & Movies EDA

### Exploratory Data Analysis of Amazon Prime's US Content Library

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-4c72b0?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

## 📑 Table of Contents
- [Overview](#-overview)
- [Business Objectives](#-business-objectives)
- [Problem Statements](#-problem-statements)
- [Dataset](#-dataset)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Key Findings](#-key-findings)
- [Business Insights](#-business-insights)
- [Tech Stack](#-tech-stack)
- [How to Run](#-how-to-run)
- [Conclusion](#-conclusion)
- [Author](#-author)

---

## 📌 Overview

This project analyzes **Amazon Prime Video's US content library** to uncover patterns in content diversity, regional distribution, catalog growth and audience ratings.

Using Python, Pandas and data visualization, the analysis turns raw catalog data into clear, business-focused insights that could support content strategy and acquisition decisions.

---

## 🎯 Business Objectives

| Area | Goal |
|------|------|
| **Content Strategy** | Understand whether movies or TV shows dominate and which genres lead |
| **Regional Insights** | Identify which countries contribute the most content |
| **Growth Monitoring** | Evaluate how the catalog has evolved over time |
| **Audience Reception** | Find top-rated titles and examine ratings vs. popularity |

---

## ❓ Problem Statements

**A. Content Diversity**
- Do Movies or TV Shows dominate the platform?
- What are the most prevalent genres?

**B. Regional Availability**
- Which production countries contribute the most content?

**C. Trends Over Time**
- How has the content library evolved over the years?
- Have content additions increased over time?

**D. IMDb Ratings & Popularity**
- Which titles are the highest rated?
- Is there a relationship between IMDb ratings and TMDb popularity?
- Which titles are the most popular?

---

## 📊 Dataset

The analysis uses two files:

| File | Rows | Columns | Description |
|------|------|---------|-------------|
| `titles.csv` | 9,871 | 15 | Title details: type, genres, release year, runtime, production countries, IMDb and TMDb scores |
| `credits.csv` | 124,235 | 5 | Cast and crew details: actor and director names, roles, characters |

**Key columns:** `title`, `type`, `release_year`, `genres`, `production_countries`, `imdb_score`, `imdb_votes`, `tmdb_score`, `tmdb_popularity`, `name`, `role`

---

## 🧹 Data Cleaning & Preparation

- ✅ Removed **3 duplicate rows** from `titles` and **56 duplicate rows** from `credits`
- ✅ Checked missing values across both datasets (for example, `seasons` was mostly empty because movies have no seasons)
- ✅ Converted `genres` and `production_countries` from string-lists into real Python lists using `ast.literal_eval`
- ✅ Used `explode()` so each genre and country is counted individually
- ✅ Built a ratings subset of **7,319 titles** with valid IMDb and TMDb scores to avoid distorted results
- ✅ Separated actors and directors from the credits data for participation analysis

---

## 🔍 Key Findings

### 🎞️ Movies vs. TV Shows
| Type | Titles | Share |
|------|--------|-------|
| Movies | 8,511 | **86.2%** |
| TV Shows | 1,357 | 13.8% |

### 🎭 Top 5 Genres
| Genre | Titles |
|-------|--------|
| Drama | 4,762 |
| Comedy | 2,987 |
| Thriller | 2,119 |
| Action | 1,820 |
| Romance | 1,751 |

### 🌍 Top 5 Production Countries
| Country | Titles |
|---------|--------|
| 🇺🇸 United States | 5,331 |
| 🇮🇳 India | 1,072 |
| 🇬🇧 United Kingdom | 928 |
| 🇨🇦 Canada | 530 |
| 🇫🇷 France | 250 |

### 📈 Growth Over Time
- Titles per year grew steadily from **176 in 2008** to **856 in 2021**, with faster growth after 2015
- The lower 2022 count (89) reflects **incomplete data for that year**, not a real decline

### ⭐ Ratings vs. Popularity
- The correlation between IMDb score and TMDb popularity is only **0.08**, a very weak relationship
- Highly rated content is **not necessarily the most popular**
- The most popular titles are mostly recent releases from 2020 to 2022

### 🎬 Talent Participation
- Most frequent actors and directors are linked to **classic films and Westerns** (for example Roy Rogers and director Joseph Kane), reflecting the older titles in the catalog

---

## 💡 Business Insights

1. **Movie-heavy catalog:** The platform focuses on standalone films, so there may be room to grow its TV series library.
2. **Drama leads:** Drama, Comedy and Thriller dominate, which shows where audience demand and acquisition effort are concentrated.
3. **US-centered but global:** India and the UK contribute significantly, signalling international diversification.
4. **Expansion phase:** Strong catalog growth after 2015 matches rising competition in streaming.
5. **Quality ≠ popularity:** Ratings and popularity behave independently, so both metrics should be tracked when evaluating content.

---

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Environment:** Google Colab / Jupyter Notebook

---

## 🚀 How to Run

1. Clone the repository
```bash
   git clone https://github.com/Subhansubose03/Amazon-prime-TV-Shows-Movies-EDA.git
   cd Amazon-prime-TV-Shows-Movies-EDA
```
2. Install the required libraries
```bash
   pip install pandas numpy matplotlib seaborn
```
3. Place `titles.csv` and `credits.csv` in the project folder
4. Open `Amazon_Prime_TV_Shows_And_Movies_EDA.ipynb` in Jupyter Notebook or Google Colab and run all cells

> **Note:** In Google Colab, upload both CSV files when the upload cell runs.

---

## ✅ Conclusion

This EDA shows that Amazon Prime Video's US catalog is **movie-dominated (86%)**, led by **Drama, Comedy and Thriller**, and **US-centered with strong contributions from India and the UK**. The library expanded sharply after 2015, and the very weak correlation (0.08) between IMDb ratings and TMDb popularity shows that audience-perceived quality and popularity are distinct.

Together, these findings give a clear picture of the platform's content strategy, regional mix, growth and audience reception.

---

## 👤 Author

**Subhansu Bose**
Aspiring Data Analyst | Python • SQL • Power BI • Excel

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/subhansu-bose-576872246/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Subhansubose03)

⭐ If you found this project helpful, consider giving it a star!
