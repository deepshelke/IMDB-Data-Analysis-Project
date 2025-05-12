# 🎬 IMDb Data Engineering & Analytics Project

This project is a complete end-to-end data pipeline and BI dashboard built using IMDb data. We used AWS Lambda (via Docker), Alteryx, and Tableau to clean, transform, and visualize top 1000 IMDb-rated movies.

---

## 📁 Data Sources

IMDb official datasets in `.tsv` format:

| File Name             | Description                                 |
|----------------------|---------------------------------------------|
| title.basics.tsv     | Title type, primary title, start year, etc. |
| title.ratings.tsv    | Average IMDb rating and number of votes     |
| title.crew.tsv       | Director and writer details                 |
| title.episode.tsv    | Episode-to-series mappings                  |
| title.principals.tsv | Principal cast and crew info                |
| name.basics.tsv      | People info (birth year, professions)       |
| title.akas.tsv       | Alternate titles by region/language         |

---

## 🧠 Objective

- Build an automated ETL pipeline using AWS Lambda + Docker
- Convert `.tsv` data to `.parquet` using Pandas and PyArrow
- Store clean data in S3 and register schema in AWS Glue
- Use Alteryx for advanced filtering, ranking, and joins
- Design an interactive dashboard in Tableau Cloud

---

## 🛠️ Tools & Technologies

- **Python (pandas, pyarrow)**
- **AWS Lambda (Docker container)**
- **Amazon S3**
- **AWS Glue Data Catalog**
- **Alteryx Designer**
- **Tableau Cloud**

## 🧪 Alteryx Workflow

The data transformation and filtering were handled in **Alteryx Designer**, where we:

- 🔗 Joined multiple IMDb datasets (titles, ratings, crew, etc.)
- 🔍 Filtered movies with:
  - IMDb Rating > 8.0
  - Minimum 1000 votes
- 📊 Extracted the **Top 1000 Movies**
- 🎬 Identified the **Most Frequently Featured Directors**
- 📤 Exported the final output as `Top_1000_Movies.csv` for use in Tableau

  ![FC63E0FE-D6DC-422A-B01E-DFF6CEE019A8_1_105_c](https://github.com/user-attachments/assets/cf786cc2-b356-480d-a522-663222874351)


### 🧩 Workflow Features
- Multi-step Joins
- Filtering Logic
- String Parsing
- Ranking & Sorting

---

## 📊 Tableau Dashboard (Cloud)

The final insights were visualized using **Tableau Cloud** with an intuitive, YouTube-themed design.

### 📈 Dashboard Sections
![image](https://github.com/user-attachments/assets/558ddbae-3546-4084-8196-aa321d7c79a1)

- **Top IMDb Genres by Average Rating**
- **Runtime Distribution of Top IMDb Movies**
- **Most Frequent Directors in Top-Rated Titles**
- **Trends in Ratings Over the Years**
- **Interactive Table: Top 1000 IMDb Movies**

