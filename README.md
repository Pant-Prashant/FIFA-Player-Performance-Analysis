# FIFA Player Performance Analysis

## 📌 Project Overview

This project analyzes FIFA player performance data at the **match level** for the **2025/26 season**.

The analysis uses Python to clean the dataset, explore player and match-level performance, aggregate statistics by player, and create visualizations that help understand player performance across positions, nationalities, goals, assists, match ratings, and market value.

The project is designed as a **Data Analyst / Exploratory Data Analysis (EDA) portfolio project**.

---

## 🎯 Objectives

- Understand the structure and quality of the FIFA player performance dataset.
- Clean missing values and handle unknown nationality values.
- Identify the distribution of match records across player positions.
- Explore the most represented nationalities.
- Aggregate match-level data into player-level performance statistics.
- Identify top players by average match rating, goals, and assists.
- Compare average match ratings across different positions.
- Examine the relationship between player market value and match rating.
- Present findings through clear and readable visualizations.

---

## 📊 Dataset

The dataset contains **13,397 match-level records** and **21 columns**.

Each row represents **one player's performance in one match**, rather than one row per player.

### Dataset Coverage

- **Rows:** 13,397
- **Columns:** 21
- **Unique players:** 229
- **Unique clubs:** 47
- **Unique match records:** 13,397
- **Season:** 2025/26
- **Competitions:** 5

### Competitions Covered

- Champions League
- Domestic Cup
- FIFA World Cup 2026
- League
- World Cup Qualifiers

### Main Variables

| Category | Variables |
|---|---|
| Player Information | Player, Nationality, Club, Position, Age |
| Financial | Market Value Mil |
| Match Information | Season, Competition, Match Id, Minutes Played |
| Attacking | Goals, Assists, Shots On Target |
| Passing | Pass Accuracy Perc |
| Defensive | Tackles |
| Physical | Distance Covered Km |
| Performance | Match Rating |
| Discipline | Yellow Card, Red Card, Fouls Committed |
| Availability | Injured Flag |

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** — data manipulation and aggregation
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **Jupyter Notebook** — analysis environment

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Import
   ↓
Column Renaming
   ↓
Duplicate Check
   ↓
Missing Value Handling
   ↓
Data Understanding & Descriptive Statistics
   ↓
Exploratory Data Analysis
   ↓
Player-Level Aggregation
   ↓
Performance Analysis
   ↓
Data Visualization
   ↓
Correlation Analysis
```

---

## 🧹 Data Cleaning

The following cleaning steps were performed:

### 1. Column Renaming

Several original column names were renamed to make them easier to read and work with.

Examples include:

- `player_name` → `Player`
- `market_value_eur_m` → `Market Value Mil`
- `minutes_played` → `Minutes Played`
- `match_id` → `Match Id`
- `match_rating` → `Match Rating`

### 2. Duplicate Check

The dataset was checked for duplicate rows.

**Result:** No duplicate rows were found.

### 3. Missing Values

Missing values were handled using:

- Mean value for `Market Value Mil`
- Median value for `Pass Accuracy Perc`
- Median value for `Distance Covered Km`

### 4. Unknown Nationalities

Unknown nationality values were replaced using the player's known nationality from other records where available.

---

## 🔎 Exploratory Data Analysis

### Position Analysis

The project examines how match records are distributed across player positions.

The positions represented include:

- ST
- CM
- CAM
- RW
- LW
- CB
- CDM
- RB
- GK
- LB
- CF

A bar chart is used to visualize the number of match records for each position.

### Nationality Analysis

The project identifies the top 10 nationalities based on the number of match records.

The most represented nationalities in the dataset include:

- England
- France
- Brazil
- Germany
- Netherlands
- Spain
- Argentina
- Italy
- Portugal
- Morocco

### Player-Level Performance

Because the original dataset is at match level, the project aggregates records by player.

The resulting player-level analysis includes:

- Matches Played
- Position
- Nationality
- Club
- Total Goals
- Total Assists
- Total Shots On Target
- Average Pass Accuracy
- Average Distance Covered
- Average Match Rating
- Average Market Value

---

## 📈 Visualizations

The notebook creates the following visualizations:

1. **Match Records by Position**
2. **Top 10 Nationalities by Match Records**
3. **Top 10 Players by Average Match Rating**
4. **Top 10 Players by Total Goals**
5. **Top 10 Players by Total Assists**
6. **Average Match Rating by Position**
7. **Market Value vs Match Rating**

These visualizations are created using **Seaborn** and **Matplotlib**.

---

## 📊 Correlation Analysis

The project investigates whether player market value is associated with match rating.

The calculated Pearson correlation between:

- `Market Value Mil`
- `Match Rating`

is:

**-0.003**

This indicates that, within this dataset, there is essentially **no linear correlation** between market value and match rating.

Correlation should not be interpreted as proof of causation.

---

## 💡 Key Analytical Takeaways

The analysis demonstrates several important data-analysis concepts:

- The dataset is structured at the **match level**, so player-level insights require aggregation.
- Data cleaning is necessary before performing reliable analysis.
- Different types of missing values can require different imputation strategies.
- Grouping and aggregation can convert detailed match-level data into useful player-level summaries.
- Visualizations make comparisons between positions, players, and nationalities easier.
- Market value does not show a meaningful linear relationship with match rating in this dataset.

---

## 📁 Project Structure

```text
FIFA-Player-Performance-Analysis/
│
├── FIFA_Player_Performance_Analysis.ipynb
├── fifa2026_player_performance_clean.csv
├── README.md
└── images/
    └── charts and visualizations
```

> Update the file structure if additional files are added to the GitHub repository.

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the project directory

```bash
cd FIFA-Player-Performance-Analysis
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook

Open:

```text
FIFA_Player_Performance_Analysis.ipynb
```

Make sure the dataset file is available in the same working directory:

```text
fifa2026_player_performance_clean.csv
```

---

## 📌 Important Note

The analysis is based on the **2025/26 season** and the dataset available for this project. The results describe patterns within this dataset and should not automatically be generalized to all FIFA competitions, seasons, or players.

---

## 👨‍💻 Skills Demonstrated

This project demonstrates practical skills in:

- Data Cleaning
- Exploratory Data Analysis
- Data Aggregation
- GroupBy Operations
- Descriptive Statistics
- Missing Value Handling
- Data Visualization
- Correlation Analysis
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## ⭐ Project Purpose

This project was created as a portfolio project to demonstrate practical **Data Analyst skills**, especially the ability to take a structured dataset, clean it, explore it, derive meaningful summaries, and communicate the analysis visually.
