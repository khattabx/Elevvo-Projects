# Elevvo Traning Projects

# SQL-ChinookDB-Analysis

## Data Model

- The data is about a digital media store, featuring tables for **artists**, **albums**, **media tracks**, **invoices**, and **customers**.
- To explore the full story behind the **Chinook Database** - its purpose, origin, and details - visit [lerocha](https://github.com/lerocha/chinook-database).

![ERD](images/ERD.png)

---

## Overview

Analyze the Chinook Database using SQL to extract business insights—such as top-selling products, revenue by region, and monthly performance—through JOINs, aggregations, and window functions.

## Why SQL Analysis ?

The data is only in a database format, so I have to use SQL queries to answer the business questions.

### Business Questions

- Top-Selling Products.
- Revenue Per Region.
- Monthly Performance.

### Update

After answering the business questions, it was found that:

- Top-Selling Products: Dazed and Confused, **The Trooper**.
- Top Region by Total Revenue: **USA — 523.06**.
- Highest Monthly Performance: **April 2023 — 51.62** (with all other months included in the results).

### Steps to Follow

- **You will find all the SQL Queries in the [sql_script.sql](SQL/mysql_script.sql) file, and the most important file to fully understand the whole process is the [sql_process.md](SQL/sql_process.md).**

**Main Files to Check:**

- `SQL/sql_process.md` → This file documents the project process.
- `images/ Q1:Q4` → Screenshots of the query executions.
- `SQL/Chinook_MySql.sql` → Database scripts.
- `LICENSE.md` → Outher License

## Getting Started

**Clone the repository:**

```bash
git clone git@github.com:khattabx/SQL-ChinookDB-Analysis.git
```

---

# Superstore Sales Dashboard - Power BI

![Dashboard](images/dashboard.png)

## Overview

This project presents an **interactive Power BI dashboard** built on the Superstore Sales dataset.  
It provides insights into sales performance, profitability, and return rates across products, categories, and regions.

---

## Data Model

- **Orders**: Category, City, Country/Region, Customer Name, Discount, Order Date, Order ID, Postal Code, Product Name, Profit, Quantity, Region, Sales, Segment, State/Province, Sub-Category.  
- **Returns**: Order ID  
- **Date**: Calendar table for time intelligence  

---

## Key Measures

- **Metrics**
  - % Returned Orders  
  - Profit  
  - Sales  
- **Previous Year (PY) Metrics**
  - % Returned Orders PY  
  - Profit PY  
  - Sales PY  
- **Comparisons**
  - Total Revenue vs PY  
  - Sales by Product  

---

## Features

- Clean and structured data model.  
- KPI cards for top-level metrics (Revenue, Profit, Returns).  
- Sales analysis by Product, Category, Region, and Customer Segment.  
- Year-over-Year performance tracking.  
- Interactive filters and slicers for better exploration.  

---

## Cloning

To clone this repository and explore the project locally:

```bash
git clone https://github.com/your-username/superstore-sales-dashboard.git
cd superstore-sales-dashboard
```
---

# Titanic Exploratory Data Analysis (EDA)

## Overview

This project performs an Exploratory Data Analysis (EDA) on the classic Titanic dataset. The goal is to understand the dataset's structure, identify missing values, clean the data, and visualize key patterns and correlations related to passenger survival. This analysis is a foundational step in machine learning projects, providing insights that can inform feature engineering and model selection.

## Project Structure

The project is implemented in a Jupyter Notebook (`titanic_report.ipynb`) and utilizes Python libraries such as Pandas for data manipulation and Seaborn/Matplotlib for data visualization.

## Main Topics Covered

### 1. Data Loading and Initial Exploration

- Loading the `train.csv` dataset into a Pandas DataFrame.
- Checking the dimensions of the dataset (rows and columns).
- Viewing the first and last few rows to get a glimpse of the data.

### 2. Data Types and Missing Data Handling

- Examining the data types of each column to ensure they are appropriate for analysis.
- Identifying and quantifying missing values across all columns. This is crucial for data cleaning.

### 3. Data Visualization

- Generating various plots to understand the distribution of key features and their relationship with survival.
- Visualizations include:
    - **Death vs. Survival Count**: A bar plot showing the number of passengers who survived versus those who did not.
    - **Passenger Class Counts**: A bar plot illustrating the distribution of passengers across different classes (1st, 2nd, 3rd).
    - **Gender Counts**: A bar plot displaying the distribution of male and female passengers.
    - **Embarked Counts**: A bar plot showing the number of passengers who embarked from different ports.
    - **Age Histogram**: A histogram to visualize the distribution of passenger ages.

## Bonus: Survival Rate Visualizations

- Further analysis includes visualizing survival rates based on different categorical variables such as gender and passenger class using bar plots and potentially heatmaps to show correlations.

## How to Run the Project

1. Clone the repository:

   ```bash
   git clone git@github.com:khattabx/Titanic-Report.git
   cd Titanic-Report
   ```

2. Ensure you have Python and Jupyter Notebook installed. If not, you can install Anaconda, which includes both.
3. Install the required libraries:

   ```bash
   pip install pandas numpy pylab seaborn
   ```

4. Open the Jupyter Notebook:

   ```bash
   jupyter notebook titanic_report.ipynb
   ```

5. Run all cells in the notebook to reproduce the analysis and visualizations.

## Dataset

The dataset used is the classic Titanic: Machine Learning from Disaster dataset, commonly found on Kaggle. It contains various information about the passengers on the Titanic, including their age, gender, passenger class, and whether they survived the disaster.

---

# RFM Customer Segmentation

This project applies **RFM (Recency, Frequency, Monetary)** analysis to an online retail dataset in order to perform structured customer segmentation. The workflow demonstrates the use of Python, data cleaning, and visualization techniques for actionable business insights.

---

## Project Workflow

The end-to-end process included:

- Acquiring and exploring raw transactional data  
- Cleaning and preprocessing the dataset (Excel and Python)  
- Implementing RFM logic to calculate customer metrics  
- Visualizing customer segments and related business insights  
- Documenting the entire pipeline in a Jupyter Notebook  

---

## Dataset Information

- **Dataset**: Online Retail  
- **Source**: UCI Machine Learning Repository  
- **Format**: Excel (`Online Retail.xlsx`)  
- **Description**: Contains historical transactional data from a UK-based online store  
- **Key Columns**: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country  

---

## Data Preparation

- Converted `InvoiceDate` to datetime format  
- Filtered out rows with missing `CustomerID`  
- Excluded canceled transactions (`InvoiceNo` starting with "C")  
- Added computed column `TotalPrice = Quantity × UnitPrice`  
- Ensured dataset integrity for RFM calculations  

---

## Notebook: `Customer_Segmentation_RFM.ipynb`

The notebook contains:

1. Data loading and inspection  
2. Data preprocessing and filtering  
3. Calculation of RFM metrics:  
   - **Recency**: Days since last purchase  
   - **Frequency**: Number of transactions  
   - **Monetary**: Total spending  
4. Scoring of RFM values using quintiles (1–5)  
5. Creation of composite RFM scores (e.g., 543, 111)  
6. Customer segmentation mapping (Champions, Loyal, At Risk, etc.)  
7. Merging RFM results back into the dataset for advanced analysis  

---

## Visualizations

Implemented using **Matplotlib**:

- Customer distribution across segments (bar and pie charts)  
- Average monetary value by segment  
- Top countries ranked by segment volume  
- Overview of key business metrics (customers, revenue, order value, etc.)  

---

## Project Files

| File                              | Description                                                     |
|-----------------------------------|-----------------------------------------------------------------|
| `Customer_Segmentation_RFM.ipynb` | Jupyter Notebook with full workflow and visualizations          |
| `Online Retail.xlsx`              | Raw dataset from UCI                                            |
| `full_dataset_with_rfm.csv`       | Processed dataset including RFM scores and segment labels       |
| `README.md`                       | Project documentation                                           |

---

## How to Run

Clone or download the repository  

```bash
   git clone git@github.com:khattabx/Customer-Segmentation-RFM.git
   cd Customer-Segmentation-RFM
```

Install required libraries:  

   ```bash
   pip install pandas matplotlib openpyxl
   ```
