# 🎓 Online Learning Enrollment Analytics Platform

## 📌 Project Overview

The **Online Learning Enrollment Analytics Platform** is an end-to-end data engineering project developed using Databricks, SQL, and Lakeflow Spark Declarative Pipelines.

The main objective of this project is to process online course enrollment data, improve data quality, transform raw records into business-ready datasets, and generate meaningful insights through interactive dashboards.

This project follows the **Medallion Architecture (Bronze, Silver, and Gold)** to organize the data processing workflow.

## 🎯 Project Objectives

- Ingest raw online learning enrollment data into Databricks.
- Clean and transform enrollment records.
- Identify and handle duplicate and invalid records.
- Implement data quality checks and validation.
- Build business-level aggregated datasets.
- Develop interactive dashboards to analyze enrollment and revenue performance.

## 📂 Dataset Description

The project uses an online course enrollment dataset in CSV format.

**Dataset:** `course_enrollments_raw.csv`

- Total Records: 1,283
- Total Columns: 20

### Dataset Attributes

| Column | Description |
|---|---|
| enrollment_id | Unique enrollment identifier |
| learner_id | Learner identifier |
| learner_email | Learner email address |
| learner_city | Learner location |
| age_group | Learner age category |
| course_id | Course identifier |
| course_name | Course name |
| category | Course category |
| course_level | Course difficulty level |
| instructor_name | Instructor name |
| enrollment_date | Enrollment date |
| enrollment_channel | Enrollment source |
| list_price | Original course price |
| discount_amount | Discount provided |
| price_paid | Final amount paid |
| payment_method | Payment method |
| progress_pct | Course progress percentage |
| hours_watched | Total hours watched |
| course_rating | Course rating |
| certificate_issued | Certificate status |

## 🏗️ Data Engineering Architecture

The project follows the Medallion Architecture with three processing layers.

### 🥉 1. Bronze Layer – Raw Data Ingestion

- Loaded the CSV dataset into Databricks using Unity Catalog Volumes.
- Created a Bronze streaming table to preserve raw records.
- Captured source file information and ingestion timestamps.
- Maintained the original data for further processing.

### 🥈 2. Silver Layer – Data Cleaning & Transformation

- Removed duplicate enrollment records.
- Standardized inconsistent text values and learner email addresses.
- Handled missing categories, cities, and payment values.
- Applied data quality expectations to identify invalid progress percentages and negative prices.
- Created learner status using SQL CASE WHEN.
- Maintained separate clean and rejected datasets.

### 🥇 3. Gold Layer – Business Aggregation

Created four business summary tables to support analytical reporting:

- Monthly Enrollment and Revenue Trends
- Category Performance
- Course Performance
- Enrollment Channel Performance

Additional processing:
- Calculated total revenue and enrollment metrics.
- Analyzed course completion rates.
- Identified unique learners.
- Created a data quality summary table.
- Performed reconciliation validation.

## 📊 Databricks AI/BI Dashboard

Developed an interactive dashboard with three pages using Gold-layer datasets.

### 1. Overview Dashboard

- Total Enrollments
- Total Revenue
- Course Completions
- Total Hours Watched
- Monthly Revenue Trends
- Revenue by Course Category
- Learner Status Distribution

### 2. Courses & Channels Dashboard

- Top 10 Courses by Revenue
- Course Completion Rates
- Average Course Ratings
- Category-wise Completion Performance
- Enrollment and Revenue by Channel

### 3. Data Quality Dashboard

- Bronze and Silver Record Counts
- Rejected Records
- Duplicate Records
- Learner Email Standardization Impact
- Data Quality Issue Counts
- Reconciliation Validation

## 📈 Data Processing Results

| Metric | Result |
|---|---:|
| Raw Records | 1,283 |
| Clean Records | 1,241 |
| Rejected Records | 19 |
| Duplicate Records | 23 |
| Reconciliation Status | Passed |

The reconciliation confirms that the raw records are accounted for across clean, rejected, and duplicate records.

## 🛠️ Technologies & Tools Used

- **Databricks:** Data engineering and processing platform.
- **SQL:** Data transformation, cleaning, and aggregation.
- **Lakeflow Spark Declarative Pipelines:** Pipeline development and data processing.
- **Unity Catalog:** Data governance and management.
- **Medallion Architecture:** Bronze, Silver, and Gold data organization.
- **Databricks AI/BI Dashboards:** Interactive data visualization and reporting.

## 🔄 End-to-End Workflow

Raw CSV Data  
↓  
Bronze Layer – Raw Data Ingestion  
↓  
Silver Layer – Data Cleaning and Validation  
↓  
Gold Layer – Business Aggregation  
↓  
Databricks AI/BI Dashboards  
↓  
Business Insights and Reporting

## 💡 Key Learnings

Through this project, I gained practical experience in:

- Building end-to-end data engineering pipelines.
- Working with Databricks SQL.
- Implementing Medallion Architecture.
- Cleaning and validating real-world datasets.
- Applying data quality expectations.
- Creating business-ready analytical tables.
- Developing interactive AI/BI dashboards.

## 👩‍💻 Acknowledgements

This project was completed as part of my learning journey at **Innomatics Research Labs**.

Special thanks to my trainer **Deepraj Vadhwane** and mentor **Karthik Reddy Dappili** for their valuable guidance and support.

---

⭐ If you find this project useful, feel free to explore the repository!

#Databricks #DataEngineering #SQL #Lakeflow #MedallionArchitecture #DataAnalytics
