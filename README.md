
# 🎬 Netflix Content Analytics – Excel → SQL → Power BI

## 📌 Project Overview

This project demonstrates an end-to-end **data analytics pipeline** applied on the popular **Netflix titles dataset**. It begins with raw **CSV/Excel data**, progresses through structured analysis using **SQL**, and concludes with an **interactive Power BI dashboard**.

The main objective is to uncover insights about Netflix’s catalog across genres, ratings, countries, and trends over time.

---

## 🧾 Step 1: Data Understanding & Excel Preparation

The dataset consisted of ~8,800 rows with 12 columns, including:
- `show_id`: Unique identifier  
- `type`: Movie or TV Show  
- `title`: Title of the content  
- `director`, `casts`: People involved  
- `country`: Country of origin  
- `date_added`: When added to Netflix  
- `release_year`: Year of release  
- `rating`: TV/Movie rating (e.g., TV-MA, PG-13)  
- `duration`: Runtime (for Movies) / Seasons (for TV Shows)  
- `listed_in`: Genres/categories  
- `description`: Brief summary  

Tasks in Excel included:
- Handling null values in `director`, `country`
- Splitting columns such as `listed_in` (genres) for analysis
- Ensuring uniform date formats
- Saving the dataset as a CSV for SQL import

---

## 🗃️ Step 2: SQL Data Analysis (PostgreSQL)

The dataset was imported into a **PostgreSQL database** (`netflix`) for structured querying. Several SQL queries were written to derive insights:

Key queries included:
1. **Movies vs TV Shows count**
2. **Most common ratings** for both Movies and TV Shows
3. **All movies released in a specific year** (e.g., 2020)
4. **Top 5 countries with most Netflix content**
5. **Longest movie** by duration
6. **Content added in the last 5 years**
7. **Titles by a specific director** (e.g., Rajiv Chilaka)
8. **TV Shows with more than 5 seasons**
9. **Content count in each genre**
10. **Annual releases in India with % share**
11. **All documentaries**
12. **Content with missing directors**
13. **Actor-specific appearances** (e.g., Salman Khan in last 10 years)
14. **Top 10 actors in Indian content**
15. **Categorizing content as Good/Bad based on violent keywords**

These queries used PostgreSQL features such as:
- `STRING_TO_ARRAY` and `UNNEST` for splitting genres and casts
- `SPLIT_PART` for handling durations
- Aggregations (`COUNT`, `ROUND`)
- Date functions for filtering recent releases

---

## 📊 Step 3: Data Visualization with Power BI

The analysis culminated in an interactive **Power BI dashboard** highlighting:
- **KPIs**: Total Titles, Movies vs TV Shows, Most Popular Rating, Top Genres
- **Trend Analysis**: Releases per year, Content added by date
- **Country Insights**: Map showing content distribution, Top producing countries
- **Genre Distribution**: Bar charts, Tree maps, and Word Cloud of categories
- **Duration Insights**: Movie runtime patterns and TV show seasons
- **People Analytics**: Top directors and actors with most appearances

The dashboard enables **dynamic exploration** with filters for Type, Year, Country, and Genre.

---

## 🧠 Skills Demonstrated

- **Excel**: Data cleaning, handling missing values, splitting categorical columns
- **SQL (PostgreSQL)**: Aggregations, string functions, date filtering, ranking queries
- **Power BI**: Dashboard design, KPIs, interactive visuals, map visualizations
- **Data Analysis**: Content trends, regional insights, genre distribution, actor/director profiling

---

## 📈 Conclusion

This project demonstrates how a raw dataset of Netflix titles can be transformed into **actionable insights** through structured SQL queries and compelling Power BI visualizations.

It provides a comprehensive look into Netflix’s global catalog – uncovering trends by year, country, genre, and rating – and showcases the value of combining **SQL + BI tools** for real-world content analytics.
