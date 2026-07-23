Project Overview  
The objective of this assignment is to design and implement a complete Big Data pipeline using modern data engineering tools and technologies.

The solution covers data ingestion, cleaning, transformation, warehousing, and analytical processing.



The pipeline simulates a real-world scenario for a UK-based online retailer, processing \~500,000 transactions to answer key business questions:

* Who are the highest-spending customers?
* What are the most popular products?
* How do returns and cancellations affect net sales?
* Which countries generate the most revenue?

\---



## Dataset Description



**Source:** [UK Online Retail Dataset (2010–2011)](https://www.kaggle.com/datasets/rokib55/online-retail-xlsx) — Kaggle



The dataset used in this project is based on retail transaction data containing information such as:

* Invoice Number
* Stock Code
* Product Description
* Quantity
* Invoice Date
* Unit Price
* Customer ID
* Country



**Scale:** 541,909 records · 25,900 invoices · 4,070 products · 4,373 customers · 38 countries



This dataset is used to analyze customer behavior, product performance, and country‑wise sales trends.

\---

## Technologies Used

* Python
* PySpark (DataFrame API, Window functions, Spark SQL)
* MongoDB Atlas (Spark–MongoDB Connector)
* Pandas
* Google Colab / Jupyter Notebook

\---

## Data Pipeline Architecture

The project follows a Medallion Architecture approach:

### Bronze Layer

* Raw dataset ingestion
* Initial storage without transformations

### Silver Layer

Data cleaning and preprocessing:

* Handling missing CustomerIDs
* Removing duplicate records
* Filtering cancelled invoices
* Handling negative quantities (returns)
* Removing invalid/negative prices

### Gold Layer

Business‑ready transformed data:

* Revenue calculations
* Customer segmentation features
* Aggregated invoice data
* Country and product analytics

\---

## Key Analyses Performed

* Top Customers by Revenue
* Top Products by Revenue
* Country‑wise Sales Performance
* Return Transaction Analysis
* Cancelled Invoice Analysis

\---

## Data Cleaning Summary

|Rule|Count|
|-|-|
|Total Records|541,909|
|Missing CustomerID (replaced)|135,080|
|Return Transactions|10,624|
|Cancelled Invoices|9,288|
|Invalid/Negative Prices Removed|2,521|
|Duplicate Records Removed|5,265|

\---

## How to Run the Project

1. Open the notebook in **Google Colab** or **Jupyter Notebook**
2. Install required libraries:

```bash
   pip install pyspark pymongo pandas
   ```

3. Configure MongoDB connection URI
4. Run cells sequentially from data ingestion → gold layer

\---

## Project Structure

* Data Ingestion
* Data Cleaning (Silver Layer)
* Feature Engineering
* Fact \& Dimension Creation
* MongoDB Storage
* Aggregation Queries

Notebook cells: 118

\---

## 

