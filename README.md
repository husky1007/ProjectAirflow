# Kaggle Data Extraction with Airflow
 This project demonstrates how to use Apache Airflow to automate the process of extracting data from Kaggle. It provides a robust and scalable solution for retrieving dataset files, partitioning the data, and storing it in both an S3 bucket and a PostgreSQL database.

Keywords: Airflow, Python, AWS RDS, AWS S3, Postgres Database, Data lake, Kaggle, API, Docker

![Airflow Graph](assets/airflow_graph.png)


## Features
* Automatically collects inputs from the user, such as the dataset topic, filters (hottest, newest), and the desired quantity of datasets to download.
* Downloads the dataset files locally using the Kaggle API.
* Partitions the downloaded data into YYYY/MM/DD format for efficient storage and retrieval.
* Stores the raw CSV files in an S3 bucket for long-term data archival.
* Transforms the raw data into the more efficient Parquet file format.
* Stores the transformed Parquet files in the same S3 bucket.
* Loads both the raw and transformed data into an RDS database for further analysis or querying.
* Utilizes the powerful scheduling capabilities of Airflow to automate the data extraction process.

