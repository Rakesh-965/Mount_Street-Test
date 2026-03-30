**Data Engineer Take-Home — Fabric End-to-End Solution**
Overview
This project demonstrates an end-to-end data engineering solution built using Microsoft Fabric, covering data ingestion, transformation, modelling, and reporting.
The pipeline processes semi-structured JSON/NDJSON data, transforms it into analytics-ready tables, and visualises insights via a report.

**Architecture**
The solution is built using the following Fabric components:

Workspace – Central environment for managing all assets
OneLake – Storage layer for raw and processed data
Notebook (PySpark) – Data ingestion, flattening, and transformation
Lakehouse / Warehouse – Structured data storage
Pipeline – Orchestration and automation
Power BI Report – Data visualisation and insights

**Data Processing Workflow**
  1. Data Ingestion
Loaded NDJSON/JSON data using PySpark notebooks
Stored raw data in OneLake (Bronze layer)
  2. Data Transformation
Flattened nested structures including:
departments
owners
contributors
attachments
tags
events
Normalised nested JSON into structured tables
Handled:
Mixed timestamp formats
Schema inconsistencies
  3. Data Modelling
Designed source schema
Created ERD diagram using dbdiagram.io
Built mart tables optimised for analytics
  4. SQL Transformations
Implemented transformations using SQL
Created fact and dimension tables

**Reporting**
Built a Power BI report
Created a semantic model:
   Defined relationships
   Identified fact and dimension tables
Added:
   Key business metrics
   Interactive slicers and filters

**Pipeline & Automation**
    Pipeline Design
Built a Fabric pipeline for orchestration
Supports:
   API-based ingestion
   Blob storage ingestion

**Data Quality & Governance**
Schema Drift Handling:
   Dynamic schema handling for evolving JSON fields
   Flexible parsing for CustomAttributeData
   Timestamp Normalisation
Standardised multiple formats:
   ISO timestamps
   Zulu format
   Epoch milliseconds
   Date-only values
Validation Checks:
   Primary key enforcement
   Referential integrity checks
   Data completeness validation
Bad Data Strategy:
   Quarantine invalid records
   Logging for debugging
   Reprocessing capability

**Deliverables**
 1.Data ingestion & transformation notebook
 2.ERD diagram
 3.Mart tables (SQL)
 4.Fabric pipeline
 5.Power BI dashboard

 **Notes**
This project focuses on building a scalable and maintainable data pipeline with proper handling of schema evolution, data quality, and automation.
