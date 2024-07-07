# data-engineering

## Overview
This project provides a high-level architecture for a data engineering platform designed to handle various data sizes ranging from 10MB to 100GB. The platform includes components for data ingestion, storage, processing, aggregation, and visualization using AWS services.

## Architecture Diagram

             +-------------------------+
             |       Data Sources      |
             |-------------------------|
             |  APIs, Databases, Files |
             +-------------------------+
                        |
                        v
             +-------------------------+
             |      Data Ingestion     |
             |-------------------------|
             | Kafka, NiFi, Kinesis    |
             +-------------------------+
                        |
                        v
             +-------------------------+
             |       Data Storage      |
             |-------------------------|
             | Data Lake (S3, GCS)     |
             | Data Warehouse (Redshift|
             | BigQuery, Snowflake)    |
             +-------------------------+
                        |
                        v
             +-------------------------+
             |     Data Processing     |
             |-------------------------|
             | Spark, Flink, Kafka     |
             | Streams, Storm          |
             +-------------------------+
                        |
                        v
             +-------------------------+
             |    Data Aggregation     |
             |-------------------------|
             | Airflow, Glue, dbt      |
             +-------------------------+
                        |
                        v
             +-------------------------+
             |    Data Visualization   |
             |-------------------------|
             | Tableau, Power BI,      |
             | Looker, Grafana         |
             +-------------------------+
