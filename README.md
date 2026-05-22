# SalesInsightsLakehouse

Enterprise-style Azure Lakehouse project implementing incremental ingestion, medallion architecture, Delta Lake processing, dimensional modeling, workflow orchestration, CI/CD automation, and analytics reporting using Azure services and Databricks.

## Architecture

HTTP API  
↓  
Azure SQL Database  
↓  
Azure Data Factory  
↓  
ADLS Gen2 Bronze Layer  
↓  
Databricks Silver Layer  
↓  
Gold Layer Star Schema  
↓  
Power BI Dashboard

## Tech Stack

Azure Data Factory  
Azure Databricks  
Delta Lake  
ADLS Gen2  
Unity Catalog  
Azure SQL Database  
Azure DevOps  
Power BI  
PySpark  
SQL

## Project Overview

This project implements an end-to-end medallion architecture pipeline using Azure services and Databricks.

Incremental records are extracted from Azure SQL Database using watermark-based ingestion in ADF and stored as batch parquet files in the Bronze layer. Databricks notebooks process incremental batches into curated Silver Delta tables and Gold dimensional models.

The Gold layer contains fact and dimension tables built using surrogate keys and SCD Type 1 merge logic.

The project also includes Git integration, parameterized notebook execution, dynamic batch folder orchestration, and CI/CD integration using Azure DevOps.

## Features

Incremental batch ingestion using watermark logic

Dynamic batch folder creation in ADLS Gen2

Bronze, Silver, and Gold medallion architecture

Delta Lake merge and upsert operations

SCD Type 1 dimensional modeling

Parameterized Databricks notebook execution from ADF

Unity Catalog integration

Azure DevOps Git integration

Power BI reporting layer

## Repository Structure

```text
ADF/
    pipelines
    datasets
    linked services
    triggers

Databricks/
    silver notebooks
    gold notebooks
    fact processing
    catalog setup

screenshots/
README.md

## Screenshots

Data Lake Bronze Batch Structure

Silver Layer Processing with Invalid Row Isolation

Gold Layer Fact and Dimension Tables

ADF Source Preparation and Ingestion Pipeline

Incremental ADF Orchestration Pipeline

Dynamic Batch Path Parameterization

Unity Catalog and Workspace Structure

Databricks Workflow Pipeline

ADF Triggered Databricks Job Runs

Azure DevOps Repositories

ADF CI/CD Pipeline and YAML Deployment

Power BI Reporting Layer