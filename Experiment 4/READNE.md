# Café Sales Data Cleaning Using Power Query

## Project Overview

This project focuses on cleaning and preparing a dirty café sales dataset using **Microsoft Power BI and Power Query**.

The dataset contains 10,000 café transaction records with missing values, duplicate records, `ERROR` and `UNKNOWN` entries, incorrect data types, extra spaces, hidden characters, and invalid quantity and price values.

The main objective was to clean and transform the raw dataset into a structured, consistent, and reliable dataset suitable for further analysis and business reporting.

## Objectives

* Import café sales data into Power BI.
* Identify data quality problems in the raw dataset.
* Clean and transform the data using Power Query.
* Handle missing and incorrect values.
* Recalculate missing sales-related values wherever possible.
* Remove invalid and duplicate records.
* Standardize text values and column names.
* Apply appropriate data types.
* Prepare the final dataset for further analysis.

## Dataset

The project uses a single CSV file:

**File:** `dirty_cafe_sales.csv`

**Number of Records:** 10,000

### Dataset Columns

* Transaction ID
* Item
* Quantity
* Price Per Unit
* Total Spent
* Payment Method
* Location
* Transaction Date

## Tools Used

* Microsoft Power BI
* Power Query
* CSV

## Data Import

The dataset was imported into Power BI using:

**Get Data → Text/CSV**

The raw CSV file was then opened in **Power Query Editor** for data cleaning and transformation.

## Data Cleaning and Transformation

A total of **22 Power Query transformation steps** were applied to progressively clean the raw café sales dataset.

### 1. Get Data

Imported `dirty_cafe_sales.csv` into Power Query Editor.

### 2. Keep Data as Text

Initially changed all columns to Text to prevent incorrect automatic data type conversions.

### 3. Set Headers

Promoted the first row to become the column headers.

### 4. Keep Columns as Text

Reconfirmed Text data types as a safe baseline before deeper cleaning.

### 5. Fix ERROR Values

Replaced `ERROR` values with blanks across the affected columns.

### 6. Fix UNKNOWN Values

Replaced `UNKNOWN` values with blanks so they could be handled during later cleaning steps.

### 7. Set Correct Data Types

Applied appropriate data types:

| Column           | Data Type                     |
| ---------------- | ----------------------------- |
| Quantity         | Decimal Number / Whole Number |
| Price Per Unit   | Decimal Number                |
| Total Spent      | Decimal Number                |
| Transaction Date | Date                          |
| Transaction ID   | Text                          |
| Item             | Text                          |
| Payment Method   | Text                          |
| Location         | Text                          |

### 8. Fix Missing Total Spent

Calculated missing `Total Spent` values using:

```text
Total Spent = Quantity × Price Per Unit
```

A total of **173 missing Total Spent values** were recalculated where sufficient information was available.

### 9. Fix Missing Quantity

Calculated missing Quantity values using:

```text
Quantity = Total Spent ÷ Price Per Unit
```

A total of **138 missing Quantity values** were handled.

### 10. Fix Missing Unit Price

Calculated missing Price Per Unit values using:

```text
Price Per Unit = Total Spent ÷ Quantity
```

A total of **179 missing Unit Price values** were handled.

### 11. Remove Old Columns

Removed unnecessary original or temporary columns after creating the corrected values.

### 12. Fix Column Names

Renamed columns where necessary to make them clear, consistent, and easier to understand.

### 13. Check Data Types

Re-verified the data types after performing calculations and transformations.

### 14. Fix Missing Items

Replaced **333 blank Item values** with a default value such as:

```text
Unknown Item
```

### 15. Fix Missing Payment Method

Replaced **2,579 blank Payment Method values** with a default value such as:

```text
Unknown
```

### 16. Fix Missing Location

Handled **3,265 blank Location values**, which represented the largest missing-data issue in the dataset.

### 17. Remove Missing Dates

Removed **159 rows** where Transaction Date was blank because valid dates are required for reliable date-based analysis.

### 18. Remove Duplicate Records

Checked the dataset for duplicate records. No exact duplicate rows were found, and Transaction ID values were confirmed to be unique.

### 19. Fix Extra Spaces

Used the Trim operation to remove leading and trailing spaces from text values.

For example:

```text
" Coffee"
"Coffee "
```

were cleaned so they could be treated consistently.

### 20. Clean Text Values

Removed non-printable and hidden characters from text fields using the Clean operation.

### 21. Remove Invalid Quantity

Removed records containing invalid or negative Quantity values.

### 22. Remove Invalid Price

Removed records containing invalid or negative Price Per Unit values.

## Data Cleaning Summary

| Data Issue               | Cleaning Method                         |
| ------------------------ | --------------------------------------- |
| ERROR values             | Replaced with blanks                    |
| UNKNOWN values           | Replaced with blanks                    |
| Missing Total Spent      | Calculated using Quantity × Price       |
| Missing Quantity         | Calculated using Total Spent ÷ Price    |
| Missing Unit Price       | Calculated using Total Spent ÷ Quantity |
| Missing Item             | Replaced with Unknown Item              |
| Missing Payment Method   | Replaced with Unknown                   |
| Missing Location         | Handled during cleaning                 |
| Missing Transaction Date | Rows removed                            |
| Duplicate records        | Checked and removed if present          |
| Extra spaces             | Trim operation                          |
| Hidden characters        | Clean operation                         |
| Invalid Quantity         | Rows removed                            |
| Invalid Price            | Rows removed                            |
| Incorrect data types     | Correct data types applied              |

## Outcome

After applying the 22 transformation steps, the dirty café sales dataset was successfully cleaned and organized.

The cleaning process handled:

* Missing values
* `ERROR` values
* `UNKNOWN` values
* Duplicate records
* Incorrect data types
* Extra spaces
* Hidden characters
* Invalid Quantity values
* Invalid Price values

Missing `Total Spent`, `Quantity`, and `Price Per Unit` values were recalculated wherever sufficient information was available.

The resulting dataset is more accurate, consistent, and reliable and is ready for further analysis in Power BI.

## Business Insights

The cleaned dataset provides a reliable foundation for future business analysis.

The cleaning process helps the café to:

1. Maintain accurate sales records.
2. Recover missing sales-related values where possible.
3. Prevent duplicate transactions from affecting analysis.
4. Improve reliability by correcting `ERROR` and `UNKNOWN` values.
5. Ensure Quantity and Price values are realistic.
6. Standardize Item, Payment Method, and Location information.
7. Maintain accurate date-based sales records.
8. Perform future analysis using correctly formatted data.
9. Support better decisions related to sales, pricing, inventory, and customer preferences.
10. Convert raw and inconsistent café sales data into clean and reliable information.


## Conclusion

This project demonstrates a complete **data cleaning and preparation workflow using Power Query**.

The raw café sales dataset was imported into Power BI and systematically transformed through 22 cleaning steps. Missing values were calculated or replaced where appropriate, invalid records were removed, text values were standardized, and correct data types were applied.

The final dataset is clean, organized, and reliable, making it suitable for further Power BI analysis and business reporting.



[Business Analysis Projects](https://github.com/Bhumikaravi/Business-Analysis-Projects)
