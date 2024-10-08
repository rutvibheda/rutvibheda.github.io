---
title:  "AWS ETL Pipeline on YouTube Data"
summary: End to end ETL data pipeline on AWS
tags:
  - Data Engineering
date: '2023-11-15T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''


links:
- name: Quicksight Dashboard
  url: AWS_Quicksight_Dashboard.pdf
date: '2024-09-29T00:00:00Z'


# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

This project focused on building a scalable and serverless data pipeline utilizing a variety of AWS services to manage the storage, processing, transformation, and analysis of the YouTube trending videos dataset. The dataset contains over 1 million rows, including key attributes such as video titles, views, likes, dislikes, categories, and regions. The pipeline was designed to handle this volume efficiently, process data in real time, and provide actionable insights through visualization. The key components of this pipeline are AWS S3 for storage, Lambda for event-driven processing, Spark and AWS Glue for ETL operations, Athena for querying, and QuickSight for creating dynamic dashboards.

Data Ingestion and Storage (AWS S3):
The first step of the pipeline involves data ingestion and storage in AWS S3. The raw YouTube trending videos dataset, typically in CSV or JSON format, is uploaded to an S3 bucket. AWS S3 was chosen for its scalability, reliability, and cost-effectiveness, making it ideal for handling large datasets. The data was partitioned by region allowing for more efficient querying and processing.

Event-Driven Processing (AWS Lambda):
To automate and trigger various processes in the pipeline, AWS Lambda was used for event-driven data processing. Lambda functions were configured to trigger whenever new data is uploaded to the S3 bucket, making the process entirely serverless and automated. Once data is ingested, Lambda functions extract relevant metadata and push it to AWS Glue for further ETL (Extract, Transform, Load) processing. 

Data Transformation and ETL (AWS Glue and Spark):
The ETL process is handled using AWS Glue crawler, which simplifies data extraction, transformation, and loading by automatically detecting the schema using Glue crawlers. AWS Glue uses Spark under the hood, allowing the pipeline to efficiently process and transform large datasets. The data is cleaned, transformed, and normalized to facilitate analysis.The transformed data is then written back to S3 in a format optimized for querying, such as Parquet or ORC.

Data Querying and Analysis (Amazon Athena):
Once the data is transformed and stored in S3, Amazon Athena is used to query it. Athena is a serverless query service that allows users to run SQL-like queries directly on data stored in S3, making it an ideal solution for ad-hoc querying without needing to set up complex database infrastructure. Using Athena, the dataset can be queried to derive insights like which video categories are trending, which regions generate the most views and many more.

Data Visualization and Insights (AWS QuickSight):
To provide actionable insights and visual representations of the YouTube data, AWS QuickSight was used to build dynamic dashboards. QuickSight connects directly to Athena, allowing real-time visualization of data through interactive charts, graphs, and tables. The dashboards enable users to track video trends across different regions, analyze patterns in user engagement, and identify key metrics.