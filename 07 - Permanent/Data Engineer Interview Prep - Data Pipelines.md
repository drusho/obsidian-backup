---
title: Data Pipeline. Breakdown
published: [[2024-10-23]]
description: Dive deep into the realm of Data Pipeline with snippets from multiple sources
tags:
  - data
  - pipeline
  - engineering
  - interview
---

1. What is a database?
2. Components of a database?
3. What is a pipeline?
4. Components of a pipeline?
5. Difference between ETL and ELT
## What is a Data Pipeline?
A **data pipeline** is a system that takes data from its various sources, which can include a set of functions, tools, and techniques to process raw data. It’s one component of an organization’s data infrastructure.

AKA: abstract data from sources and transfer it to the destination

## Types of Data Pipelines
- **Batch Data Pipelines**: Interact with large portions of data all at once and at some specific time of the day.
- **Real-Time Data Pipelines**: Interact with data at the time of its creation for almost real-time outcome.
- **Cloud-Native Data Pipelines**: Built for running in cloud environments which are more malleable and more flexible.
- **Open-Source Data Pipelines**: Created with the implementation of the open-source technologies like Apache Kafka, Airflow or Spark.

## Components of a Pipeline

1. Stakeholders
2. Data Sources
3. Destination - Final location for “cleaned/organized” data
4. Data Flow
5. Processing
6. Workflow
7. Monitoring

## Data Pipeline Architecture
- **Ingestion Layer**: It retrieves data from an assortment of sources ranging from databases to APIs or even event streams.
- **Processing Layer:** Another operation on data involves the analysis of the said data followed by data cleaning through tools such as spark or Hadoop.
- **Storage Layer:** Held in data lakes, warehouses or other databases, data was kept for future reference or as a back up to be analyzed later.
- **Monitoring Layer:** It is the authority that is charged with the responsibility of providing quality data in the right time and increasing the efficiency of the system.
- **Consumption Layer**: Delivers the final data to BI tools or machine learning models where the data is analyzed at the next level for decision making.

## Design Pattern
**source: [[Data Pipeline Design Patterns - System Design - GeeksforGeeks]]**