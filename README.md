# HR Data Pipeline Project

## Goal
Purpose of this project is to ingest employee data into the Lakehouse, transform it and load into the data warehouse.
Employee data is available through a NoSQL Database and also comes in as events.
Important to maintain the consistency and quality of the data also when different events (like promotion or resignation) happen.

## Architecture
Initial data is available in Azure Cosmos DB instance in different containers that store different data:
- Employees
- Employee events

Data ingestion and transformation is developed in Databricks, where we make use of the Medallion Architecture:
- bronze layer: source data ingestion with minimal transformation
- silver layer: heavylifting of transformations
- gold layer: prepared, enriched and cleaned data to support reliable business decisions

# TODO: Architecture Diagram