# D2C Customer Churn Intelligence – Part 1: Data Audit, EDA & Business Understanding

## Project Objective

The objective of this project is to understand customer behaviour, identify potential churn indicators, and assess data quality before building any retention strategy or machine learning model.

## Dataset

The analysis uses the following datasets:

* customers.csv
* orders.csv
* support_tickets.csv
* web_events_snapshot.csv
* intervention_history.csv
* churn_labels.csv

## Repository Structure

├── eda_audit.ipynb

├── data_quality_report.md

├── business_memo.md

├── requirements.txt

└── outputs/

## Tasks Performed

1. Data loading and schema inspection
2. Dataset joins and relationship validation
3. Missing value analysis
4. Duplicate and outlier detection
5. Leakage risk identification
6. Exploratory Data Analysis
7. Churn-risk hypothesis generation
8. Business recommendations

## Key Findings

* Churned customers show lower purchase frequency.
* Churned customers have lower recent activity.
* Longer inactivity periods correlate with churn.
* Low campaign engagement is associated with higher churn risk.
* Support interactions may indicate dissatisfaction leading to churn.

## How to Run

pip install -r requirements.txt

jupyter notebook eda_audit.ipynb

## Deliverables

* Data quality report
* Business memo
* EDA visualizations
* Churn-risk hypotheses
