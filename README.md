# Transaction Risk Monitoring and Fraud Detection

## Overview

This project analyzes digital banking transaction data to identify unusual account behaviour and develop risk indicators for transaction monitoring.

The analysis focuses on account-level behavioural patterns such as transaction frequency, login failures, device diversity, location diversity, and transaction amounts.

## Business Problem

Banks process large volumes of digital transactions, making it challenging to manually identify unusual behaviour.

This project aims to:

* Identify behavioural indicators associated with higher risk
* Aggregate transaction-level data into account-level profiles
* Develop a risk scoring framework
* Detect anomalous accounts using Isolation Forest
* Segment accounts using K-Means clustering
* Visualize risk patterns for monitoring purposes

## Dataset

**Dataset:** Bank Transaction Dataset for Fraud Detection

**Records:** 2,512 transactions

**After aggregation:** 495 unique accounts

## Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Excel

## Data Processing

The workflow included:

1. Data loading
2. Data quality assessment
3. Data type conversion
4. Data cleaning
5. Feature engineering
6. Account-level aggregation
7. Exploratory data analysis

## Feature Engineering

Key behavioural indicators included:

* Total transaction count
* Total login failures
* Maximum transaction/withdrawal amount
* Distinct device count
* Distinct location count
* Unusual transaction hours
* Customer demographics

## Risk Analysis

A weighted risk score was developed using selected behavioural and demographic indicators.

Isolation Forest was then applied to identify accounts exhibiting unusual combinations of behavioural characteristics.

K-Means clustering was used to further segment accounts based on their behavioural profiles.

## Key Findings

* 25 of 495 accounts (5.05%) were flagged as high-risk by the defined anomaly-detection approach.
* High-risk accounts showed higher average transaction frequency, login failures, device diversity, and location diversity.
* Distinct device count and transaction frequency showed relationships with the constructed risk score.
* Customer groups showed different behavioural patterns across the clustering analysis.

## Limitations

This dataset does not contain confirmed fraud labels. Therefore, the analysis identifies anomalous or high-risk behaviour rather than confirmed fraudulent transactions.

The results should be treated as a fraud-monitoring support framework rather than a definitive fraud classification model.

## Future Improvements

* Use a labelled fraud dataset
* Apply supervised classification models
* Evaluate precision, recall, F1-score, and PR-AUC
* Incorporate transaction velocity features
* Develop real-time monitoring
* Add device/IP behavioural analysis

