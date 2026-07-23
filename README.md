# Analytics-Data-Engineering-Pipeline
End-to-End Employee Analytics ETL Pipeline using AWS S3, PySpark, Python and Power BI.

# Analytics Data Engineering Pipeline

## Project Overview

This project demonstrates an end-to-end ETL pipeline built using PySpark and AWS S3. Employee data is ingested from Amazon S3, processed using PySpark for cleaning, validation, and feature engineering, and written back to Amazon S3 in Parquet format. The processed dataset is then used for HR analytics in Power BI.

---

## Architecture

![Architecture](architecture/architecture.png)

---

## Tech Stack

- Python
- PySpark
- AWS S3
- boto3
- Google Colab
- Parquet
- Power BI

---

## ETL Pipeline

```
Employee CSV
      ↓
AWS S3 (Raw)
      ↓
PySpark ETL
      ↓
Cleaning
Validation
Feature Engineering
      ↓
Parquet
      ↓
AWS S3 (Processed)
      ↓
Power BI Dashboard
```

---

## Data Cleaning

- Renamed columns using snake_case naming convention
- Removed duplicate employee records
- Trimmed whitespace from text fields
- Converted numeric columns to appropriate data types
- Standardized categorical values

---

## Data Validation

Implemented validation checks for:

- Duplicate Employee IDs
- Invalid Age values
- Invalid Monthly Income
- Invalid Years at Company
- Null value analysis

---

## Feature Engineering

Created new analytical features:

- Income Band
- Experience Level
- Attrition Flag
- Annual Salary
- Promotion Status
- Years to Retirement
- Attrition Risk

---

## Output

Processed data is stored in Parquet format for efficient analytical workloads.

---

## Dashboard

![Dashboard](screenshots/dashboard.png)

---

## Future Enhancements

- Load processed data into Snowflake
- Orchestrate the pipeline using Apache Airflow
- Implement incremental data loading
- Add automated monitoring and alerting
