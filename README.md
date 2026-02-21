**Project Overview**

This project implements a complete end-to-end ETL and analytics pipeline for iGenics, a U.S.-manufactured, GMP-certified health supplement.
Using Python and MySQL, the workflow ingests 83 weeks of raw weekly sales data, cleans and standardizes it, loads it into a relational database, and produces SQL-driven financial analytics and visual dashboards.

The pipeline demonstrates real-world skills in:

Data engineering (ETL pipelines, automation)

SQL analytics (MySQL queries, exports)

Python development (pandas, numpy, regex, SQLAlchemy)

Data visualization (matplotlib)

Business performance analysis

**Data Privacy Notice**

Raw source datasets are excluded due to proprietary restrictions.
A cleaned dataset sample and complete pipeline logic are provided for demonstration purposes.

**Files Included**

README.md → Project documentation

etl_weekly_summary_to_mysql.py → Raw python script used to create Python based ETL Pipeline and SQL Database

SQL Queries → Raw SQL Queries compiled together

project_summary.txt → output summary file rendered from python script

5 CSV output files :

-Total revenue per year

-Total net income per year

-Most profitable week

-Average weekly revenue per year

-Weekly revenue trend (for visualization)

4 png output files:

-Weekly net income 2024

-Weekly net income 2025

-Weekly revenue 2024

-Weekly revenue 2025


**Pipeline Capabilities**

🔹 ETL Processing (Python)

The ETL system:

Reads and validates all raw CSV sales files

Standardizes currency values and numeric formats

Parses week and year from labels like “Week 01, 2024”

Removes formatting inconsistencies and wide-format columns

Transforms weekly summaries into long-format analytical tables

Saves a cleaned dataset for reproducibility

🔹 Database Integration (MySQL)

During execution, the script automatically:

Creates a MySQL database (if not present)

Loads:

weekly_summary_raw — raw ingested data

weekly_metrics_clean — normalized long-format dataset

Executes SQL analytics queries through SQLAlchemy

🔹 SQL Analytics Performed

After loading data into MySQL, the pipeline executes several analytics queries and exports them as CSV reports:

Total revenue per year

Total net income per year

Most profitable week

Average weekly revenue per year

Weekly revenue trend (for visualization)

🔹 Visual Dashboards

Using matplotlib, the pipeline generates:

Annual revenue charts

Annual net income charts


**Key Outcomes**

Automated ingestion, cleaning, and transformation of 83 weeks of sales data

Loaded all processed data into a structured MySQL database

Produced 5 SQL-based analytics reports

Generated year-segmented visual dashboards for clear performance comparison

Derived business insights:

Revenue (2024): $854,969

Revenue (Jan–Jul 2025): $775,592

Net Income (2024): $188,184

Net Income (2025 Jan–Jul): $169,276
