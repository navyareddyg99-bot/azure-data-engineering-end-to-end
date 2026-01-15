# Azure Data Engineering End-to-End Project
End-to-end Azure Data Engineering project using ADF, ADLS, Databricks, and Synapse

## Project Overview
This project demonstrates an end-to-end data engineering pipeline using Azure services.

## Architecture
Source Data → Azure Data Factory → ADLS Gen2 → Databricks (PySpark) → Azure Synapse Analytics

## Tools Used
- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks (PySpark)
- Azure Synapse Analytics
- Azure SQL Database

## Data Layers (Bronze–Silver–Gold)

### Bronze
- Raw data ingestion implemented using Azure Data Factory
- Dynamic pipeline using Lookup and ForEach activities
- Data landed in ADLS Gen2 with minimal transformation

![Bronze Pipeline]("C:\Users\Navya\OneDrive\Pictures\Screenshots\Screenshot 2026-01-15 144710.png")

### Silver
- Data cleaning and standardization implemented using Spark
- Deduplication and schema enforcement applied
- Data stored in Parquet format for optimized analytics

### Gold
- Business-level aggregations exposed using Synapse Serverless SQL
- SQL views created for analytics and BI consumption

## Data Flow
1. Source data is stored in Azure SQL Database.
2. Azure Data Factory ingests data into ADLS Gen2 (Raw layer).
3. Data is transformed using PySpark in Azure Databricks.
4. Processed data is stored back in ADLS Gen2.
5. Azure Synapse Analytics is used for querying and analytics.

## Key Design Decisions
- Implemented a Lakehouse architecture using ADLS, Spark, and parquet
- Designed Bronze-Silver-Gold layers for seperation of concerns
- Used overwrite strategy to ensure idempotent pipeline reruns
- Exposed curated data using Synapse Serverless SQL views
- Secured data access using Managed Identity

## Current Status
- [x] GitHub repository setup
- [x] Project documentation
- [X] Azure Data Factory pipeline
- [X] ADLS storage layers
- [X] Databricks transformations
- [X] Synapse analytics

