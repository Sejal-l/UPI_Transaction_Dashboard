# UPI Transaction Analysis Dashboard

## About the Project

UPI payments are used for everyday transactions, but transaction data can reveal much more than the total amount paid. It can help understand customer payment activity, transaction success and failure, popular UPI applications, bank performance, and possible risk patterns.

This project analyzes **UPI transaction data for May 2026** using Microsoft Power BI. The dashboard presents transaction activity through interactive charts, key performance indicators, and filters. It helps explore when transactions happen, which apps and banks are commonly used, how transactions perform, and where activity is concentrated.

## Problem Statement

The objective is to turn raw UPI transaction records into useful information that can help answer questions such as:

- How many UPI transactions took place during May 2026?
- What was the total transaction value?
- What percentage of transactions were successful?
- How does transaction activity change by date and hour?
- Which UPI applications and banks appear most often in the dataset?
- How are transactions distributed by type, status, and location?
- How many transactions are marked as suspected fraud in the dataset?

## Dataset

- **File:** `UPI_TRANSACTION_dataset.xlsx`
- **Period covered:** 1 May 2026 to 31 May 2026
- **Number of records:** 502,887
- **Format:** Excel workbook

The dataset contains transaction details such as transaction ID, date, time, amount, UPI app, customer, merchant, bank, location, transaction type, transaction status, cashback, fees, risk score, and suspected-fraud indicator.


## Dashboard Preview

### UPI Transaction Dashboard

![UPI Transaction Dashboard](IMAGES/upi-dashboard.png)

### Data Model – Star Schema

![UPI Star Schema](IMAGES/upi-star-schema.png)

## Dashboard Features and Analysis

### 1. Key Performance Indicators (KPIs)

The dashboard displays important metrics at a glance:

- **Total Transactions:** Total number of transaction records.
- **Total Transaction Amount:** Combined value of all transactions.
- **Total Cashback:** Total cashback recorded in the dataset.
- **Success Rate:** Percentage of transactions marked successful.
- **Suspected Fraud Transactions:** Number of records marked as suspected fraud.

### 2. Daily Transaction Analysis

Shows how transaction amounts change from day to day during May 2026. This helps identify days with higher or lower transaction activity.

### 3. Transaction Amount by Hour

Displays transaction amounts across different hours of the day. It helps identify the hours when transaction activity is relatively high or low.

### 4. Day and Hour Analysis

A day-and-hour matrix makes it easier to compare transaction activity across different days and times. It helps reveal recurring activity patterns.

### 5. UPI App-wise Analysis

Compares transaction activity across the UPI applications included in the dataset. This helps identify which apps account for a larger share of the recorded transactions.

### 6. Transaction Status Analysis

Shows the distribution of successful, failed, and other transaction statuses available in the data. This gives an overview of transaction outcomes.

### 7. Bank-wise Analysis

Compares transaction activity across banks in the dataset, making it easier to explore differences in transaction volume and value.

### 8. Transaction Type Analysis

Displays how transactions are distributed across the transaction types recorded in the dataset.

### 9. State-wise Transaction Analysis

Uses a map to show the geographical distribution of transaction activity across states represented in the dataset.

### 10. Interactive Filters

Slicers allow users to filter the dashboard and explore the data by available fields such as date, UPI app, bank, transaction status, and location.





## Business Questions Answered

The dashboard helps explore the following questions:

1. What is the overall volume and value of UPI transactions?
2. What proportion of transactions are successful?
3. On which dates is transaction activity higher or lower?
4. During which hours does the dataset show more transaction activity?
5. Which UPI apps and banks have higher transaction activity?
6. How are transactions distributed across different types and statuses?
7. Which states show higher transaction activity?


## Data Preparation

The data was prepared in Power BI before building the dashboard. The preparation and modeling work included:

- Loading the Excel dataset into Power BI.
- Checking the data and reviewing duplicate records.
- Organizing transaction data for analysis.
- Creating separate date, bank, customer, location, merchant, and UPI app dimension tables.
- Establishing relationships between the fact table and dimension tables.
- Creating DAX measures for the dashboard KPIs and analysis.


## Data Modeling – Star Schema

A star schema was used to organize the data model. The central fact table stores transaction-level information and connects to dimension tables that provide descriptive details for analysis.

**Tables used:**

- `Fact_Transactions`
- `Dim_Date`
- `Dim_Bank`
- `Dim_Customer`
- `Dim_Location`
- `Dim_Merchant`
- `Dim_UPI_App`

This structure helps organize the data and supports analysis across dates, banks, customers, locations, merchants, and UPI applications.

## Tools Used

- **Microsoft Power BI** – Data modeling, DAX measures, and dashboard development.
- **Microsoft Excel** – Source dataset.

## Future Improvements

Possible extensions to the project include:

- Adding data from multiple months to compare transaction trends over time.
- Analyzing transaction failure reasons in more detail, if the required data is available.
- Exploring suspected-fraud indicators and risk scores in detail.
- Using Python to build a simple anomaly-detection model.
- Using SQL to store and query transaction data.



