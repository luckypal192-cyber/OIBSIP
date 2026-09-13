# Task 3 — Cleaning Data

## Objective

The objective of this task is to demonstrate a professional data cleaning workflow using a deliberately messy retail sales dataset. The process includes identifying data quality issues, handling missing values, removing duplicate records, standardizing data, correcting data types, detecting outliers, validating data consistency, and saving the cleaned dataset.

## Dataset

**Dataset Name:** Retail Store Sales — Dirty for Data Cleaning

The dataset contains retail transaction records with deliberately introduced data quality issues such as missing values, inconsistent formatting, duplicate records, and numerical anomalies.

### Dataset Details

- Rows: 12,575
- Columns: 11
- Format: CSV
- Dataset File: `retail_store_sales.csv`

## Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook

## Data Cleaning Process

### 1. Data Quality Assessment

The raw dataset was inspected to identify:

- Missing values
- Duplicate records
- Data type issues
- Inconsistent formatting
- Numerical value anomalies

### 2. Missing Value Handling

Missing values were handled according to the meaning of each variable.

- `Discount Applied`: Missing values were replaced with `Unknown`.
- `Item`: Missing values were replaced with `Unknown`.
- `Price Per Unit`: Missing values were reconstructed where possible using `Total Spent / Quantity`; remaining missing values were handled using the median.
- `Quantity`: Missing values were handled using the median.
- `Total Spent`: Missing values were reconstructed using `Price Per Unit × Quantity` where possible; remaining missing values were handled using the median.

### 3. Duplicate Removal

No duplicate records were found in the raw dataset, so no rows were removed due to duplication.

The number of duplicate records before and after removal was documented in the notebook.

### 4. Data Standardization

Text fields were standardized by:

- Removing leading and trailing spaces
- Converting multiple consecutive spaces into a single space

Date values were converted into proper datetime format.

### 5. Data Type Correction

Data types were inspected and verified to ensure that:

- Numerical variables use appropriate numeric data types.
- Transaction dates use datetime format.
- Categorical/text variables use appropriate object/string representation.

### 6. Outlier Detection

The Interquartile Range (IQR) method was used to detect numerical outliers.

The analysis identified:

- `Price Per Unit`: 0 outliers
- `Quantity`: 0 outliers
- `Total Spent`: 60 outliers

The 60 `Total Spent` outliers were inspected and retained because they represented mathematically valid high-value transactions rather than obvious data errors.

### 7. Data Consistency Validation

A consistency check was performed using:

`Total Spent = Price Per Unit × Quantity`

The validation produced:

- Maximum difference: `0.0`
- Inconsistent rows: `0`

This confirms that the transaction totals are internally consistent.

## Before vs After Cleaning

The notebook contains a before-versus-after data quality summary covering:

- Total row count
- Duplicate records
- Missing values

The cleaned dataset contains **12,575 rows and 11 columns**.

## Output

The cleaned dataset is saved separately as:

`cleaned_retail_store_sales.csv`

The original raw dataset remains unchanged.

## Project Structure

```text
DataAnalytics-L1-CleaningData/
│
├── dataset/
│   └── retail_store_sales.csv
│
├── screenshots/
│   ├── 01_data_quality_report.png
│   ├── 02_missing_values_report.png
│   ├── 03_duplicate_removal.png
│   ├── 04_outlier_detection.png
│   ├── 05_data_consistency_check.png
│   └── 06_before_after_summary.png
│
├── Data_Cleaning.ipynb
├── cleaned_retail_store_sales.csv
└── README.md