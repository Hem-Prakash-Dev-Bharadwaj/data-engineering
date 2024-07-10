# data-engineering

## Overview
This project provides a high-level architecture for a data engineering platform designed to handle various data sizes ranging from 10MB to 100GB. The platform includes components for data ingestion, storage, processing, aggregation, and visualization using AWS services.

## Architecture Diagram

             
             |       Data Sources      |
             |-------------------------|
             |  APIs, Databases, Files |
             
                        |
                        v
             
             |      Data Ingestion     |
             |-------------------------|
             | Kafka, NiFi, Kinesis    |
             
                        |
                        v
             
             |       Data Storage      |
             |-------------------------|
             | Data Lake (S3, GCS)     |
             | Data Warehouse (Redshift|
             | BigQuery, Snowflake)    |
             
                        |
                        v
            
             |     Data Processing     |
             |-------------------------|
             | Spark, Flink, Kafka     |
             |    Streams, Storm       |
             
                        |
                        v
             
             |    Data Aggregation     |
             |-------------------------|
             |   Airflow, Glue, dbt    |
             
                        |
                        v
             
             |    Data Visualization   |
             |-------------------------|
             | Tableau, Power BI,      |
             | Looker, Grafana         |
             


High-Level Architecture Design
             
1.	Data Ingestion:
   
*	Tools: AWS Kinesis, AWS S3, AWS Glue, Kafka

* Functionality: Captures data from various sources like databases, APIs, and streaming data sources. For small to medium-sized data, S3 and Glue would suffice. For larger data, Kinesis or Kafka for real-time ingestion would be necessary.

2.	Data Storage
   
*Tools: AWS S3, Amazon Redshift, Amazon RDS, Amazon DynamoDB

* Functionality: Stores raw and processed data. S3 can be used for raw data storage due to its scalability and cost-effectiveness. Redshift for structured, query-able data, RDS for transactional data, and DynamoDB for NoSQL storage needs.

3.	Data Processing
   
*	Tools: AWS Glue, AWS Lambda, Apache Spark (on EMR), AWS Fargate, AWS Batch

*	Functionality: Processes data to transform, clean, and aggregate it. For small data sizes, Lambda and Glue are efficient. For larger data, Spark on EMR or AWS Batch for batch processing can be used.

4.	Data Aggregation
   
*	Tools: AWS Glue, AWS Redshift, AWS Athena

*	Functionality: Aggregates processed data for analysis. Glue and Redshift can be used for ETL and aggregation tasks. Athena provides a server less option to query data directly from S3.

5.	Data Visualization
   
*	Tools: Amazon QuickSight, Tableau, Power BI

*	Functionality: Visualizes data for business intelligence. QuickSight is a native AWS tool that integrates well with other AWS services. Tableau and Power BI can be used for more advanced visualization needs.

