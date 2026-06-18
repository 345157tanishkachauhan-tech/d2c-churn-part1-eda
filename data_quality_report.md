# Data Quality Report

## Overview

The dataset consists of customer, order, support ticket, campaign, web activity, and churn information used for churn analysis.

## Missing Values

Missing value checks were performed across all datasets. Any columns containing missing values should be reviewed before production deployment.

## Duplicate Records

Duplicate record checks were performed on all datasets. Duplicate observations can impact customer counts, revenue calculations, and churn analysis.

## Join Integrity

The customer_id field serves as the primary key across datasets and was used for customer-level analysis.

## Outlier Analysis

Potential outliers were observed in:

* monetary_180d
* frequency_180d
* ticket_count_90d
* sessions_30d

These observations may represent legitimate customer behaviour and were retained for exploratory analysis.

## Data Leakage Considerations

Future information should not be used for churn prediction.

Potential leakage-sensitive fields include:

* churn_next_60d
* post-snapshot customer activity
* future campaign outcomes

These fields should only be used as targets and not as predictive features.

## Recommendations

1. Validate missing values before model deployment.
2. Monitor extreme spending and activity patterns.
3. Standardize date formats across datasets.
4. Verify customer_id uniqueness.
5. Follow snapshot-date restrictions during model development.
