Week 3: Multi-Source Data Integration Pipeline
📌 Project Overview

This project demonstrates the development of a multi-source data pipeline that integrates data from three different sources into a unified analytical dataset. The objective is to simulate a real-world data engineering workflow by combining internal operational data, live external API data, and relational database information to generate actionable business insights.

The project was completed as part of the Power Learn Project (PLP) Academy - Python Programming Week 3 Technical Challenge.

🎯 Objectives
Load and analyze an internal operational dataset.
Retrieve real-time external data using a REST API.
Build and query a SQLite database using SQLAlchemy.
Merge multiple data sources into a Master DataFrame.
Handle missing values and data inconsistencies.
Perform correlation analysis to uncover operational insights.
Document every processing step for reproducibility.
📂 Project Structure
Week3-Multi-Source-Pipeline/
│
├── week3_multi_source_pipeline.ipynb      # Main Jupyter Notebook
├── ops_sensor_log_cleaned.csv             # Cleaned operational dataset
├── README.md                              # Project documentation
└── images/                                # Optional screenshots/diagrams
📊 Data Sources
1. Internal Operational Dataset

The primary dataset contains cleaned operational sensor records from Week 2, including production and efficiency metrics.

Example columns include:

Date
Plant/Site
Throughput
Efficiency
Downtime
Temperature
Pressure
Shift
2. External API

Real-time data was retrieved using the Requests library.

Example API use cases include:

Weather information
Rainfall
Temperature
Humidity
Wind speed
Currency exchange rates
Commodity prices

The notebook includes:

API request handling
JSON parsing
Error handling using:
try:
    ...
except requests.exceptions.RequestException:
    ...
3. SQLite Database

A local SQLite database was created using SQLAlchemy containing supplementary operational information such as:

Employee shifts
Holiday calendar

SQL queries demonstrate:

JOIN operations
GROUP BY aggregation
Reading SQL results directly into Pandas using:
pd.read_sql()
🔄 Data Integration Workflow

The project combines all three sources into a single Master DataFrame.

Pipeline flow:

Operational CSV
        │
        ▼
External API
        │
        ▼
SQLite Database
        │
        ▼
Merge & Clean
        │
        ▼
Master DataFrame
        │
        ▼
Analysis & Visualization
🧹 Data Cleaning

Data preprocessing includes:

Handling missing values
Date conversion and alignment
Removing duplicates
Standardizing column names
Merging datasets using common keys
Filling null values created after joins
📈 Analysis Performed

The notebook performs correlation analysis to investigate relationships between operational performance and external factors.

Example analysis:

Rainfall vs Throughput
Temperature vs Efficiency
Holidays vs Operational Output

Correlation techniques include:

Pearson Correlation
Correlation Matrix
Scatter plots
Heatmaps (optional)
🛠️ Technologies Used
Python
Pandas
NumPy
Requests
SQLAlchemy
SQLite
Matplotlib
Jupyter Notebook
📚 Key Python Concepts Demonstrated
API Integration
JSON Processing
SQL Queries
Database Connectivity
DataFrame Merging
Exception Handling
Correlation Analysis
Data Cleaning
Data Engineering Pipeline
