---
title:  "DynamoDB: A Comprehensive Analysis for a NoSQL Solution"
summary: Implementation of a NoSQL database  
tags:
  - NoSQL Databases
  - Amazon Web Services
date: '2024-08-07T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''


links:
  - name: Paper
    url: DynamoDB_Final_Report.pdf
  - icon: github
    icon_pack: fab
    name: Link
    url: https://github.com/rutvibheda/DynamoDB_NoSQLProject
  - name: Demo + Presentation
    url: https://rit.zoom.us/rec/play/PclSr-4GBwOtaZg3ew3uXc255Xe4vjzc8CukSuR4i8qF2ODhHKQ4G39U6-X6CNhvKXjY8RF-cq-TzCzz.X3XR_XhU_bH4ESPB

  

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---


NoSQL databases offer significant advantages, including scalability, flexibility, and high performance, making them ideal for modern applications that need to handle large volumes of data efficiently. They allow for horizontal scaling, support various data models (such as document, key-value, wide-column, and graph), and provide low-latency read and write operations, which are essential for applications with high-performance requirements.

This project is a web application for loan approval was developed using AWS services, integrating a React frontend with AWS Amplify for continuous integration and continuous delivery (CI/CD) and hosting. The serverless backend processing was managed with AWS Lambda, and Amazon DynamoDB was used to store user data securely, leveraging DynamoDB's scalability and flexibility. The application featured a responsive user interface that allowed customers to input their details, including credit scores and income, to determine loan eligibility based on configurable thresholds set by the admin. To ensure secure and scalable API interactions, AWS API Gateway was implemented along with AWS Identity and Access Management (IAM) policies, ensuring that only authorized AWS Lambda functions could access data in DynamoDB, thus enhancing the overall security and reliability of the application.