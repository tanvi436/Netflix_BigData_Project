# 🎬 Netflix Big Data Analysis using PySpark

## 📖 Project Overview
This project performs Big Data Analysis on the Netflix Movies and TV Shows dataset using Apache Spark (PySpark). The objective is to clean, transform, and analyze large-scale streaming data efficiently using distributed computing concepts.

The dataset includes information such as:
- Title
- Type (Movie / TV Show)
- Director
- Cast
- Country
- Release Year
- Rating
- Duration
- Date Added
- Category
- Description

---

## 🚀 Technologies Used
- Python
- Apache Spark (PySpark)
- Jupyter Notebook
- Hadoop (Windows Configuration)
- CSV Dataset

---

## 📂 Dataset Information
Dataset: Netflix Movies and TV Shows Dataset  
Format: CSV  

Columns:
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
- Used header=True and inferSchema=True
- Verified schema and data types

### 2️⃣ Data Cleaning
- Handled null values using fillna("Unknown")
- Removed duplicate records
- Converted date columns into proper format
- Extracted year from date_added

### 3️⃣ Data Transformation
- Created cleaned DataFrame
- Converted categorical columns
- Applied Spark SQL queries
- Grouped and aggregated dataset

### 4️⃣ Data Analysis Performed
- Count of Movies vs TV Shows
- Top 10 countries with most content
- Most common ratings
- Content distribution by release year
- Category-based analysis

Example Query:
```python
df_cleaned.groupBy("country").count().orderBy("count", ascending=False).show(10)
```

---

## 📊 Sample Insights
- United States has the highest number of titles.
- TV-MA and TV-PG are the most frequent ratings.
- Movies are more than TV Shows in total count.
- Major content growth observed after 2015.

---

## 📁 Project Structure

Netflix_BigData_Project/
│
├── dataset/
│   └── netflix_titles.csv
│
├── output/
│   └── netflix_cleaned_final.csv
│
└── Netflix_BigData_Project.ipynb

---

## ▶️ How to Run This Project

1. Install Python (3.8+ recommended)
2. Install PySpark:
   pip install pyspark

3. Open Jupyter Notebook:
   jupyter notebook

4. Open:
   Netflix_BigData_Project.ipynb

5. Run all cells

---

## 💡 Key Learning Outcomes
- Practical understanding of Apache Spark
- Distributed data processing concepts
- Data cleaning using PySpark
- Spark SQL and DataFrame operations
- Handling Big Data on local Windows setup
- Exporting Spark results to CSV

---

## 📌 Conclusion
This project demonstrates how Apache Spark efficiently processes large-scale streaming datasets. It showcases the importance of distributed computing in real-world analytics such as OTT platforms like Netflix.

---

## 👩‍💻 Author
Tanvi  
Big Data & Data Engineering Enthusiast  
