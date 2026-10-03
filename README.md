# Uber Real-Time Data Engineering Pipeline

An end-to-end real-time data engineering project that demonstrates how ride-booking data can be generated, ingested, processed, transformed, and prepared for analytics using Azure cloud services and Databricks.

## Project Overview

This project implements a real-time data pipeline for Uber ride-booking data using **Azure Event Hubs, Azure Data Factory, Azure Data Lake Storage Gen2, and Databricks**. The pipeline uses **PySpark and Spark Structured Streaming** to process incoming ride events and follows a **Medallion Architecture** to organize data into Bronze, Silver, and Gold layers.

## Architecture

```text
Uber Ride Data Generator
          │
          ▼
    Azure Event Hubs
          │
          ▼
       ADLS Gen2
          │
          ▼
      Databricks
          │
    ┌─────┴─────┐
    ▼           ▼
 Bronze       Silver
    │           │
    └─────┬─────┘
          ▼
         Gold
          │
          ▼
   Analytics-Ready Data
```

## Technologies Used

- **Python** – Ride data generation and pipeline scripting
- **Azure Event Hubs** – Real-time event ingestion
- **Azure Data Factory** – Data pipeline orchestration and movement
- **Azure Data Lake Storage Gen2** – Cloud data storage
- **Databricks** – Data processing and transformation
- **PySpark** – Batch and distributed data processing
- **Spark Structured Streaming** – Real-time stream processing
- **Delta Lake** – Reliable storage and data management
- **Star Schema** – Analytics-oriented data modeling
- **Git/GitHub** – Version control

## Key Features

- Generated simulated Uber ride-booking events using Python.
- Published ride events to Azure Event Hubs.
- Ingested and stored data in Azure Data Lake Storage Gen2.
- Processed data using Databricks and PySpark.
- Implemented batch and streaming transformations using Spark Structured Streaming.
- Applied Medallion Architecture with Bronze, Silver, and Gold layers.
- Created analytics-ready fact and dimension datasets.
- Applied data transformation and dimensional modeling concepts for downstream analytics.

## Medallion Architecture

### Bronze Layer
Stores the raw ride-booking events received from the ingestion layer with minimal transformation.

### Silver Layer
Cleans, validates, and transforms the raw data into structured datasets suitable for further processing.

### Gold Layer
Contains curated, analytics-ready datasets organized using dimensional modeling concepts such as fact and dimension tables.

## Project Objective

The primary objective of this project is to demonstrate an end-to-end **real-time data engineering workflow** using Azure and Databricks, covering data generation, streaming ingestion, cloud storage, distributed processing, transformation, and analytical data modeling.



