# iGenics Sales Data Pipeline

This project implements a complete **end-to-end ETL and analytics pipeline** for **iGenics**, a U.S.-manufactured, GMP-certified health supplement product.  

Using **Python and MySQL**, the system ingests raw weekly sales reports, cleans and standardizes the data, loads it into a relational database, and performs SQL-based financial analytics and visual reporting.

The pipeline processes **83 weeks of historical sales data** and produces structured outputs that support business performance analysis and decision making.

---

# Project Overview

The project demonstrates practical skills in modern **data engineering and analytics workflows**, including:

- ETL pipeline development
- Automated data ingestion and cleaning
- Relational database design and loading
- SQL-based financial analytics
- Python-based visualization and reporting

The system converts unstructured weekly summary reports into a **structured analytics dataset** suitable for database querying and business intelligence.

---

# Data Privacy Notice

Raw source datasets are excluded from this repository due to **proprietary business restrictions**.

To maintain transparency and reproducibility:

- The **complete ETL pipeline code** is included
- A **cleaned dataset sample** is provided
- All **SQL analytics queries** and generated outputs are included

This allows the full analytics workflow to be understood without exposing sensitive source data.

---

# Files Included

| File / Folder | Description |
|---------------|-------------|
| `README.md` | Project documentation describing the pipeline architecture and analytics workflow |
| `etl_weekly_summary_to_mysql.py` | Python ETL pipeline that ingests raw sales data, cleans it, loads it into MySQL, and generates analytics outputs |
| `SQL Queries.sql` | Collection of SQL queries used to generate financial analytics from the database |
| `project_summary.txt` | Automatically generated summary file containing pipeline execution metrics and results |
| `outputs/` | Folder containing generated analytics reports and visualizations |


---

# Project Workflow

The system follows a structured **data engineering pipeline** designed to simulate real-world business analytics workflows.

## 1. Data Ingestion

Raw weekly sales CSV files are automatically discovered and loaded by the ETL script.

The ingestion process:

- Detects all raw CSV files in the dataset directory
- Reads multiple file encodings
- Combines all weekly reports into a single dataset
- Tracks source files for traceability

---

## 2. Data Cleaning and Standardization

The ETL pipeline transforms raw weekly reports into a structured format suitable for analytics.

Cleaning steps include:

- Removing formatting inconsistencies
- Standardizing currency values (e.g., `$2,345` → `2345`)
- Converting accounting-style negative numbers `(1,234)`
- Removing corrupted or unnamed columns
- Normalizing metric names

---

## 3. Data Transformation

The raw wide-format reports are reshaped into a **long-format analytical dataset**.

Transformations include:

- Parsing week and year from labels such as `Week 01, 2024`
- Extracting product channel identifiers (`CB`, `BG`, `DS`, `Total`)
- Creating normalized metric fields
- Producing structured time-series records

This results in a dataset optimized for **SQL analytics and time-series analysis**.

---

## 4. Database Integration (MySQL)

The ETL pipeline automatically creates and populates a **MySQL database**.

Two database tables are generated:

**weekly_summary_raw**

Stores the original ingested weekly reports.

**weekly_metrics_clean**

Stores the cleaned and normalized analytical dataset used for SQL queries.

Database creation and loading are handled automatically using **SQLAlchemy**.

The ETL pipeline implementation is available in:  
:contentReference[oaicite:0]{index=0}

---

# SQL Analytics Queries

After the dataset is loaded into MySQL, several SQL analytics queries are executed to produce financial insights.

The queries are stored in:  
:contentReference[oaicite:1]{index=1}

## Queries Included

### Total Revenue per Year

Calculates total annual revenue across all sales channels.

### Total Net Income per Year

Computes total yearly net income.

### Most Profitable Week

Identifies the week with the highest net income.

### Average Weekly Revenue per Year

Calculates the average weekly revenue for each year.

### Weekly Revenue Trend

Produces time-series revenue data used for visualization dashboards.

---

# Data Visualization

The pipeline generates visual dashboards using **Matplotlib**.

Visual outputs include:

- Weekly revenue trends
- Weekly net income trends
- Year-segmented performance charts

These visualizations provide an intuitive overview of sales performance across time.

---

# Python Libraries Used

The ETL pipeline was implemented using the following Python libraries:

| Library | Purpose |
|--------|--------|
| pandas | Data ingestion, transformation, and analysis |
| numpy | Numerical processing and data handling |
| matplotlib | Visualization of financial metrics |
| SQLAlchemy | Database connection and SQL execution |
| PyMySQL | MySQL database driver |
| python-dotenv | Secure database credential management |
| glob | Automatic discovery of dataset files |
| re (regex) | Parsing week and year information |
| os | File system and directory management |

---

# Key Outcomes

The pipeline successfully automated the full analytics workflow for iGenics sales data.

Key outputs include:

- Automated ingestion and processing of **83 weeks of sales data**
- Creation of a structured **MySQL analytics database**
- Generation of **5 SQL-based analytics reports**
- Production of **visual dashboards for financial trends**

---

# Business Insights

The analysis produced the following key financial insights:

**Revenue**

2024 Revenue: **$854,969**

2025 Revenue (Jan–Jul): **$775,592**

**Net Income**

2024 Net Income: **$188,184**

2025 Net Income (Jan–Jul): **$169,276**

These metrics provide a clear overview of the product’s financial performance across the analyzed time period.

---

# Technologies Used

Python  
MySQL  
SQLAlchemy  
Pandas  
NumPy  
Matplotlib  

---

# Author

**Munem Shariar Shams**

Data Analytics | Data Engineering | SQL | Python
