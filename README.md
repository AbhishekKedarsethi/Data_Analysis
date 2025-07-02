
# 📊 End-to-End Data Analytics Project

In this project, I designed and implemented a complete data analytics pipeline simulating a real-world business workflow.
The process included data ingestion, cleaning, transformation, exploratory data analysis (EDA), visualization, and dashboard reporting — all built using Python, PostgreSQL, and Power BI, following industry best practices.

The goal was to demonstrate how raw, unstructured data can be systematically transformed into actionable business insights through automation, reproducible processes, and intuitive visualization.

## 📦 Tools & Technologies Used
### Tool & Purpose
**Python** (pandas, numpy, os, logging)	- Automate data ingestion & process monitoring.   
**SQL** (PostgreSQL) - Central data storage, cleaning, transformation and performing EDA.  
**Power BI** - Data visualization, EDA, and dashboard reporting


## ✅ Step 1: Collecting Data & Understanding Business Problems
In my company, we use Azure Data Factory (ADF) pipelines and triggers to automate the periodic retrieval of data.   
To demonstrate a similar approach in my personal project, I built a Python script that automates the daily ingestion of CSV files into a PostgreSQL database. The script leverages libraries such as pandas, sqlalchemy, os, and logging. The logging module helps monitor the ingestion process by recording key events and execution time, ensuring better visibility and debugging. I have kept the logging data in another folder so that it will be easy to understand and maintain in a structured format.  
which might include:
- Internal databases (SQL, NoSQL)
- Flat files and semi-structured data (Excel, CSV, JSON)
- APIs and web scraping for external datasets
- ERP or CRM systems

Once data is collected, it is essential to:
- Understand the data structure and schema to identify how different tables and fields relate.
- Validate data quality to spot anomalies, missing fields, and inconsistencies.
- Map business objectives and questions to data availability, so the analysis can produce targeted insights.

Example business problems explored:
- Are there stores consistently underperforming across time?
- Which RFM segment contributes the most to total revenue?
- Which products are underperforming due to high returns or poor customer feedback?

Business Problems

By grounding the technical process in clear business questions, the pipeline ensures every step contributes directly to solving real-world challenges.

## 🛠 Step 2: Automated Data Ingestion
To simulate real business workflows as in my company project, I automated data ingestion using Python, making the process repeatable and maintainable.

Key components:
- **Python libraries:**
	- pandas and numpy for data manipulation
	- os for file management
	- logging to monitor the process and capture errors
- **PostgreSQL Database** to store both raw and cleaned datasets.
- Raw data is first imported into the database unchanged to preserve original information.

Logging was set up to:
- Record the success or failure of each ingestion step.
- Track runtime statistics.
- Save logs in separate files for clear historical records and easier debugging.

This ensures transparency and makes the process easier to audit, which is critical in enterprise environments.

Python Script 

## 🧹 Step 3: Data Cleaning & Transformation
Once data is loaded into PostgreSQL, I performed cleaning directly in SQL using a structured four-step approach:
1. Detect & remove duplicates to ensure data consistency
2. Standardize data (e.g., text casing, date formats) to enable accurate analysis
3. Identify and handle null or blank values by filling, replacing, or removing them based on context
4. Remove irrelevant or redundant columns and rows to streamline datasets

To protect data integrity:
- Raw data was kept in its own schema/database
- Cleaning and transformation occurred on a copy to preserve the original data for traceability.

This step laid a strong foundation by transforming messy raw data into analysis-ready datasets.

SQL Queries

## 📈 Step 4: Exploratory Data Analysis (EDA) & Visualization
The next step was to explore and visualize the cleaned data to identify trends, patterns, and outliers.

Key actions:
- Established a live connection between Power BI and the PostgreSQL database, so the dashboards update automatically whenever new data is ingested.
- Created a Calendar table in Power BI to enable accurate time-based calculations and visuals, such as month-over-month growth.
- Built measures and calculated columns (e.g., average order value, customer frequency) tailored to answer the business questions.
- Designed an RFM_Table (Recency, Frequency, Monetary) to segment customers by behavior and value.

#### ER_Diagram
![Alt text](https://github.com/AbhishekKedarsethi/Data_Analysis/blob/main/ER%20Diagram/ER_Diagram.png)

Visual exploration included:
- Trends over time (e.g., sales growth, churn rate)
- Top vs. bottom-performing customers and products
- Relationships between variables (e.g., customer loyalty vs. revenue)
This step uncovered actionable insights and set the stage for interactive dashboards.

## 📊 Step 5: Dashboard & Report Generation
The final deliverable was an interactive Power BI dashboard that presents data-driven answers in a visually compelling way.

Design and features:
- Color theme: Purple highlights combined with a dark gray background to enhance readability and give a professional look.
- Visuals included:
		
  - KPI cards to highlight key metrics
  - Slicers for interactive filtering (by time, region, product, etc.)
  - Bar charts, line graphs, scatterplots, tables, and matrix visuals
  - Clear labeling and tooltips to ensure stakeholders easily interpret the visuals

The dashboard:
- Addresses the original business questions
- Provides actionable insights (e.g., target high RFM score customers for loyalty campaigns)
- Supports data-driven decisions with clarity and transparency

![Alt text](https://github.com/AbhishekKedarsethi/Data_Analysis/blob/main/Dash%20Board/dashboard_pic.png)

Report

Dashboard 
https://app.powerbi.com/groups/me/reports/83463653-3da7-4c8f-9697-d19b8d203e07/8773f0ddb8aa75e548bd?experience=power-bi

## ✨ Key Highlights & Business Value
- ✅ Automated, repeatable data pipeline from raw data to insights
- ✅ Detailed logging and separation of raw vs. cleaned data for traceability
- ✅ Customer segmentation (RFM) to identify high-value and at-risk customers
- ✅ Visual storytelling to translate complex data into simple, actionable insights
- ✅ End-to-end workflow closely aligned with real-world business needs

## 📍 Conclusion
By building this complete analytics pipeline — from data collection to automated reporting — I simulated a real-world analytics workflow that’s scalable, maintainable, and directly tied to business value.  
This project highlights my ability to combine technical skills (Python, SQL, Power BI) with business understanding to turn raw data into insights that drive better decisions.
