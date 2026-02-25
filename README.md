# 🎬 Netflix Big Data Analysis using PySpark

## 📖 Project Overview
This project performs Big Data Analysis on the Netflix Movies and TV Shows dataset using Apache Spark (PySpark).  
The goal of this project is to clean, transform, and analyze large-scale streaming data efficiently using distributed computing.

The dataset contains information such as:
- Title
- Type (Movie / TV Show)
- Director
- Cast
- Country
- Release Year
- Rating
- Duration
- Date Added

---

## 🚀 Technologies Used

- Python
- Apache Spark (PySpark)
- Jupyter Notebook
- Hadoop (if configured)
- CSV Dataset

---

## 📂 Dataset

Dataset Used: Netflix Movies and TV Shows Dataset  
Format: CSV  

Columns include:
- show_id
- type
- title
- director
- cast
- country
- date_added
- release_year
- rating
- duration
- listed_in
- description

---

## 🛠 Project Workflow

### 1️⃣ Data Loading
- Loaded CSV file into Spark DataFrame
- Applied schema inference

### 2️⃣ Data Cleaning
- Handled null values
- Replaced missing values with "Unknown"
- Removed duplicates

### 3️⃣ Data Transformation
- Extracted year from date_added
- Converted columns to proper data types
- Created cleaned DataFrame

### 4️⃣ Data Analysis

Performed analysis such as:

- Top 10 countries with most content
- Count of Movies vs TV Shows
- Most common ratings
- Content distribution by year
- Duration analysis

Example Query:
```python
df_cleaned.groupBy("country").count().orderBy("count", ascending=False).show(10)
