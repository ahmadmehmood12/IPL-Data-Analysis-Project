# IPL Data Analysis using PySpark and Azure Databricks

This project is an end-to-end **IPL (Indian Premier League) Data Analysis** pipeline built using **Apache Spark on Azure Databricks**, with data hosted on **AWS S3**. The goal was to clean, transform, model, and analyze IPL data to uncover key cricket insights through **data engineering** and **analytical processing**.

## 📘 Overview

This project focuses on building a scalable data pipeline and performing analytics on IPL datasets using Spark SQL and PySpark.
The complete process includes data ingestion, schema definition, data cleaning, transformation, dimensional modeling, and visualization.

---

## 🧩 Architecture

1. **Data Source:** CSV files hosted in AWS S3
2. **Processing Engine:** Azure Databricks (Apache Spark)
3. **Data Storage:** S3 Data Lake
4. **Visualization:** Matplotlib and Seaborn
5. **Modeling Approach:** Dimensional Data Modeling (Fact and Dimension tables)

---

## 📊 Datasets Used

* **Ball_By_Ball.csv**
* **Match.csv**
* **Player.csv**
* **Player_match.csv**
* **Team.csv**

---

## ⚙️ Data Engineering Process

### 1. **Data Ingestion**

Data was loaded directly from S3 using Spark’s `read.csv()` method with defined schemas for each dataset.

### 2. **Data Cleaning and Transformation**

* Filtered invalid deliveries (wides and no-balls)
* Normalized player names using regex and string functions
* Replaced missing values in `Batting_hand` and `Bowling_skill` columns
* Derived new columns such as:

  * `Batting_Style` (Left/Right handed)
  * `Veteran_Status` (based on age)
  * `Years_Since_Debut`
  * `Win_Margin_Category`
  * `High_Impact` flag for impactful deliveries

### 3. **Dimensional Modeling**

Created dimension and fact tables for analytical querying:

* **dim_team** – Team information
* **dim_player** – Player attributes and career data
* **dim_date** – Date hierarchy (day, month, year, quarter)
* **dim_match** – Match-level data with team and player references
* **fact_ball_by_ball** – Core fact table for granular match statistics

---

## 🔍 Analytical Queries and Insights

* Top-scoring batsmen per season
* Most economical bowlers in powerplay overs
* Toss impact on match outcomes
* Average runs scored by batsmen in winning matches
* Venue-wise scoring trends
* Most frequent dismissal types
* Team performance after winning toss
* Total matches played in each IPL season
* Team with the highest number of wins overall

---

## 📈 Visualizations

Built visual insights using **Matplotlib** and **Seaborn**:

* Most economical bowlers in powerplay overs
* Toss impact on match outcomes
* Average runs by batsmen in winning matches
* Venue-wise score distributions
* Frequency of dismissal types
* Team performance after winning toss
* Total matches played per season

---

## 🧠 Key Learnings

* Implemented a complete data engineering workflow using Spark
* Designed and built a dimensional data model suitable for analytical queries
* Applied SQL on Spark for large-scale data aggregation
* Visualized insights to better understand IPL performance trends

---

## 🚀 Tech Stack

* **Language:** Python (PySpark)
* **Platform:** Azure Databricks
* **Data Storage:** AWS S3
* **Libraries:** PySpark, Matplotlib, Seaborn
* **Data Modeling:** Star Schema (Fact & Dimension Tables)

---

## 📬 Author

**Project by:** [Your Name]
**LinkedIn:** [Your LinkedIn Profile URL]
**GitHub:** [Your GitHub URL]

---
