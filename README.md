# data-engineering_project-7
# Delta Lake Assignment - Incremental Data Processing using Delta Lake

## Author

**Himanshi Bhadauriyaa**

---

# Project Overview

This project demonstrates how to perform **incremental data processing** using **Apache Spark** and **Delta Lake** in **Databricks**.

The objective of this assignment is to load a dataset into a Delta Table, clean the data, simulate incremental data, perform an upsert operation using the Delta Lake **MERGE** command, validate the final dataset, and verify that the Delta Table has been updated correctly.

This project showcases one of the most important concepts used in modern Data Engineering pipelines for handling continuously arriving data.

---

# Objectives

- Load CSV data into a Delta Table
- Perform basic data cleaning
- Handle missing values
- Remove duplicate records
- Create an incremental dataset
- Perform UPDATE and INSERT using Delta MERGE
- Validate processed data
- Display final results

---

# Technologies Used

- Apache Spark
- Delta Lake
- Databricks Community Edition
- Python (PySpark)
- SQL
- GitHub

---

# Project Structure

```
delta-lake-assignment/
│
├── data/
│   ├── customer_master.csv
│   └── customer_incremental.csv
│
├── notebooks/
│   └── delta_scd_assignment.ipynb
│
├── screenshots/
│   ├── data_loading/
│   ├── data_cleaning/
│   ├── scd1/
│   ├── validation/
│   └── final_output/
│
└── README.md
```

---

# Dataset Description

The dataset contains customer order information including:

- Row ID
- Order ID
- Order Date
- Ship Date
- Customer Details
- Product Details
- Sales
- Quantity
- Discount
- Profit
- Region

An additional dataset was created to simulate newly arriving records.

---

# Workflow

## Step 1 : Load Dataset

- Read CSV file using Spark.
- Enabled Header.
- Enabled Schema Inference.
- Loaded data into a DataFrame.
- Saved data as a Delta Table.

---

## Step 2 : Data Cleaning

The following cleaning operations were performed:

- Removed duplicate records
- Replaced spaces in column names with underscores
- Checked for missing values
- Filled or removed null values where necessary

---

## Step 3 : Create Incremental Dataset

A second CSV dataset was prepared containing

- Updated existing records
- Newly inserted records

This dataset simulates real-world incremental data arriving into the system.

---

## Step 4 : Delta MERGE Operation

Performed an UPSERT operation using Delta Lake.

MERGE logic:

- Update existing records when Row_ID matches.
- Insert new records when Row_ID does not exist.

This is equivalent to **Slowly Changing Dimension (SCD Type 1)** behavior.

---

## Step 5 : Validation

Validation checks performed:

- Total row count
- Duplicate Row_ID count
- Updated records verification
- Newly inserted records verification

---

## Step 6 : Final Output

Displayed

- Final Delta Table
- Updated dataset
- Row counts
- Validation summary

---

# MERGE Logic

```
If Row_ID exists
        ↓
Update existing record

Else
        ↓
Insert new record
```

---

# Data Cleaning Summary

✔ Removed duplicate records

✔ Standardized column names

✔ Checked null values

✔ Created Delta Table

✔ Successfully merged incremental data

---

# Validation Summary

The following validations were completed successfully:

- Duplicate records removed
- Incremental records inserted
- Existing records updated
- Final row count verified
- Delta Table updated successfully

---

# Learning Outcomes

Through this assignment, I learned:

- Apache Spark DataFrames
- Delta Lake fundamentals
- Data Cleaning techniques
- Incremental Data Processing
- Delta MERGE operation
- Upsert implementation
- Validation of processed data
- Working with Databricks notebooks

---

# Future Improvements

Possible enhancements include:

- Automating pipeline execution
- Scheduling using Azure Data Factory
- Implementing SCD Type 2
- Partitioning Delta Tables
- Performance optimization
- Delta Table Versioning and Time Travel

---

# Screenshots

Project screenshots are available inside the **screenshots** folder.

They include:

- Data Loading
- Data Cleaning
- MERGE Operation
- Validation
- Final Output

---

# Conclusion

This project successfully demonstrates how Delta Lake can efficiently process incremental data using the MERGE operation. By combining Apache Spark with Delta Lake, both updates and new inserts can be handled in a single transaction while maintaining data consistency and reliability. This approach is widely used in real-world Data Engineering pipelines for building scalable and efficient ETL workflows.

---

# Author

## Himanshi Bhadauriyaa

Data Engineering Learner

Apache Spark | Delta Lake | Databricks | Python | SQL

---
