# Digital Allyship Toolkit - Data & Analytics Layer
# Project Overview

This repository contains the data warehouse, analytics, and intelligence layer that powers the Digital Allyship Toolkit website.

The data team is responsible for transforming raw learning platform data into reliable metrics, insights, and predictions that can be consumed by the website for dashboards, impact reporting, and smart insights.

# Data Team Scope & Responsibilities

The data team delivers the backend analytics foundation for the website, including:

- Clean, structured analytics tables

- Engagement-based revenue proxy metrics

- Adhoc analytical queries

- Machine-learning-ready feature tables

The website consumes pre-aggregated analytics data, not raw logs, ensuring performance, reliability, and clarity.

# Data Architecture

The project follows a Medallion Architecture:

# 🟤 Bronze Layer - Raw Data

Raw LMS data ingested from CSV files:

- Users

- Modules

- Learning activity

- Quiz attempts

- Confidence surveys

- Certifications

# ⚪ Silver Layer - Cleaned & Standardized Data

- Removed duplicates

- Standardized timestamps

- Validated quiz score ranges

- Normalized categorical values

- Created consistent user and module records

# 🟡 Gold Layer - Analytics & Business Logic

Business-ready tables optimized for analytics and website consumption:

- Engagement metrics

- Retention trends

- Learning performance

- Certification outcomes

- Machine learning feature sets

# Key Analytics Outputs
# 1. Engagement & Revenue Analytics (Proxy Model)

Because the platform does not process payments, revenue is modeled using engagement value proxies:

| Action                   | Engagement Value |
| ------------------------ | ---------------- |
| Module completion        | $5               |
| Certification completion | $50              |
| Monthly active user      | $10              |


This enables the website to display:

- Total engagement value

- Value generated over time

- High-value users and segments

# 2. Adhoc Analytics

Flexible SQL queries allow stakeholders and the website to answer questions such as:

- Which modules generate the most engagement?

- Who are the top contributors?

- Where do users drop off?

- How does engagement change month-to-month?

 # 3. Machine Learning (Pre-Computed Intelligence)

The data team engineered ML-ready feature tables to support predictive insights.

Features include:

- Average quiz score

- Time spent learning

- Modules completed

- Confidence levels

Target variable:

- Certification completion (Yes / No)

These features can be used for:

- Certification prediction

- User segmentation

- Targeted interventions

For the website MVP, predictions are pre-computed, not run in real time.

# Repository Structure

sql_warehouse/
├── scripts/
│   ├── bronze/      # Raw data ingestion
│   ├── silver/      # Data cleaning & standardization
│   ├── gold/        # Fact & dimension tables
│   └── analytics/  # Dashboard & adhoc queries
├── doc/             # Architecture & schema diagrams
└── README.md

# Website Integration

The website connects to this data layer to display:

- Impact dashboards

- Engagement trends

- Revenue/value analytics

- Smart insights powered by data

Data flow:

Raw Data → Data Warehouse → Analytics Tables → Website UI

# Skills Demonstrated

- SQL Development

- Data Engineering

- Data Modeling (Star Schema)

- Analytics & Product Metrics

- Feature Engineering for Machine Learning

# Project Status

✔ Data warehouse implemented
✔ Analytics tables created
✔ Website-ready metrics delivered
✔ ML feature engineering completed
