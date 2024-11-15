# Deforestation Data Pipeline Project

## Overview

This project showcases a data pipeline built to analyze deforestation trends in Jammu and Kashmir using data from Global Forest Watch. The pipeline leverages multiple technologies to ingest, process, and visualize forest loss data. By combining data from APIs, PostgreSQL, Apache Spark, and Grafana, this project provides meaningful insights into forest cover changes over time.



## Data Source

We use the dataset provided by [Global Forest Watch](https://www.globalforestwatch.org/map/country/IND/), which contains detailed deforestation metrics for Jammu and Kashmir. The data is available in **CSV format** and includes key columns such as geographic regions, thresholds, time periods, and forest cover changes.

### File Used

- **IND.xlsx**: Contains annual deforestation metrics over multiple years.



## Project Goals

1. **Data Ingestion**: Load data from external sources and store it in a structured format within PostgreSQL.
2. **Data Processing**: Use Spark for processing and transforming large-scale deforestation data to derive trends and insights.
3. **Data Visualization**: Create interactive Grafana dashboards to visualize deforestation metrics and support decision-making.
4. **Efficiency Optimization**: Implement distributed processing with Spark to handle larger datasets efficiently.



## Tech Stack

- **API Integration**: To enable real-time data updates (optional).
- **PostgreSQL**: Stores raw and processed deforestation data for easy access.
- **Apache Spark (PySpark)**: Processes and aggregates data efficiently, especially useful for large datasets.
- **Grafana**: Visualizes processed data, allowing users to track deforestation trends interactively.
- **Docker**: Manages PostgreSQL, Spark, and Grafana containers for a seamless setup.



## Setup Instructions

1.	Clone the Repository:
```
git clone https://github.com/git-fahad/deforestration-gft.git
cd deforestration-gft
```
2. Launch Docker Containers:
Use docker-compose to start PostgreSQL, Spark, and Grafana.
```docker-compose up -d```

3. Data Ingestion:
Run the data_ingestion.py script to load IND.xlsx data into PostgreSQL.

4.	Data Processing with Spark:
Use spark_processing.py to process data within a Spark DataFrame. Aggregations and transformations will be saved back to PostgreSQL.

5.	Grafana Setup:
Import grafana_dashboard.json into Grafana to set up the dashboard.
Connect Grafana to PostgreSQL for visualization.

## Data Pipeline

The pipeline follows these steps:

1.	Data Ingestion: Loads deforestation data into PostgreSQL.
2.	Distributed Processing: Apache Spark aggregates large datasets by year, region, or other factors.
3.	Storage: Processed data is stored in PostgreSQL for easy querying.
4.	Visualization: Grafana provides interactive visualizations to analyze trends over time.

## SQL Queries for Grafana

Refer to sql_queries.md for the SQL queries used to set up Grafana visualizations. These queries provide insights such as:

	•	Annual Forest Loss: Aggregates total forest area lost per year.
	•	Regional Analysis: Breaks down forest loss metrics by geographic region.
	•	Trend Analysis: Displays forest loss trends over multiple years.

This project demonstrates a comprehensive data pipeline capable of analyzing and visualizing deforestation trends. By integrating PostgreSQL, Spark, and Grafana, it provides a robust solution for environmental data analysis.
