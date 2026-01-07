# Azure Data Engineering End-to-End Project
End-to-end Azure Data Engineering project using ADF, ADLS, Databricks, and Synapse

## Project Overview
This project demonstrates an end-to-end data engineering pipeline using Azure services.

## Architecture
Source Data → Azure Data Factory → ADLS Gen2 → Databricks (PySpark) → Azure Synapse Analytics

## Technologies Used
- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Databricks (PySpark)
- Azure Synapse Analytics
- Azure SQL Database

## Key Learnings
- Built ingestion pipelines using ADF
- Performed transformations using PySpark
- Designed storage layers (Raw, Processed)
- Queried data using Synapse SQL

## Data Flow
1. Source data is stored in Azure SQL Database.
2. Azure Data Factory ingests data into ADLS Gen2 (Raw layer).
3. Data is transformed using PySpark in Azure Databricks.
4. Processed data is stored back in ADLS Gen2.
5. Azure Synapse Analytics is used for querying and analytics.

## Current Status
- [x] GitHub repository setup
- [x] Project documentation
- [ ] Azure Data Factory pipeline
- [ ] ADLS storage layers
- [ ] Databricks transformations
- [ ] Synapse analytics

