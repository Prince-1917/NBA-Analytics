# 🏀 NBA Analytics Dashboard (Statistella Competition)

A complete data analytics project built using **Python and Power BI**, focused on understanding NBA scoring trends, team performance, player impact, and conference-level dynamics from **2004 onwards**.

This project was developed as part of the **Statistella Data Analytics Competition**, with emphasis on:
- correct data cleaning
- proper aggregation logic
- clear analytical insights
- clean, professional dashboard design

---

## 📌 Project Objective

The objective of this project is to analyze historical NBA data and answer key analytical questions such as:

- How has NBA scoring evolved over time?
- How do teams differ in scoring trends across seasons?
- Is there a measurable home-court advantage?
- Which players consistently perform at the top level?
- How do the Eastern and Western Conferences compare over time?

The focus is on **accuracy, interpretability, and insight**, not just visualization.

---

## 🗂 Datasets Used

The project uses multiple NBA datasets provided for the competition, including:

- Games data (home/away scores, results, seasons)
- Game-level player statistics
- Team metadata
- Team rankings and standings by season

All datasets were inspected, cleaned, and validated before analysis.

---

## 🧹 Data Cleaning & Preparation (Python)

Data preparation was performed in **Jupyter Notebook using Pandas**.

Key steps included:

- Handling missing values correctly based on data meaning  
  (e.g., players with no minutes played were not force-filled)
- Dropping non-informative columns (e.g., constant-value columns)
- Filtering player-game records to include **only players who actually played**
- Validating uniqueness of keys such as `PLAYER_ID`, `GAME_ID`, and season-level identifiers
- Separating analysis logic from visualization logic
- Creating clean, analysis-ready output datasets

No artificial data filling or assumptions were made.

---

## 📊 Analysis Performed

All aggregations were done in Python and exported as CSV files for Power BI.

### 1️⃣ Season-wise Scoring Trend
- Calculated total points and average points per game per season
- Used game-level data to avoid duplication
- Identified long-term scoring trends across NBA seasons

### 2️⃣ Team-wise Scoring Trend
- Normalized games into team-level records (home + away)
- Computed average points per game for each team per season
- Enabled team comparison across time

### 3️⃣ Home vs Away Performance
- Compared home vs away average points per game
- Analyzed home vs away win percentages
- Quantified home-court advantage across seasons

### 4️⃣ Player Performance & Consistency
- Aggregated player statistics at the season level
- Ranked players using **points per game**
- Included games played to reflect consistency and availability
- Calculated shooting efficiencies correctly from made/attempted shots

### 5️⃣ East vs West Conference Analysis
- Used final season standings only (avoided early-season snapshots)
- Compared total wins and average win percentage by conference
- Examined long-term competitive balance between conferences

---

## 📁 Project Structure

NBA-Analytics/
├── analysis.ipynb
├── visualizations.ipynb
├── Statistella_NBA_Dashboard.pbix
├── outputs/
│   ├── season_scoring.csv
│   ├── team_season_scoring.csv
│   ├── home_away_season.csv
│   ├── player_season_stats.csv
│   └── conference_season_stats.csv
├── .gitignore
└── README.md

