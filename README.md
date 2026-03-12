# Real-World-Swiggy-Sales-SQL

# Swiggy Sales Analysis – SQL Data Analytics Project

## Project Overview

In this project, I performed a **complete SQL-based analytical workflow** on Swiggy food delivery data.
The objective was to transform raw food delivery records into a **structured analytical model** and generate meaningful business insights.

The project includes:

* Data cleaning and validation
* Duplicate detection and removal
* Dimensional modelling using a **Star Schema**
* Development of business KPIs
* Advanced SQL analysis for restaurant, location, and food performance

This project demonstrates my ability to design **analytics-ready datasets and perform business intelligence analysis using SQL**.

---

## Problem Statement

Food delivery platforms generate large volumes of transactional data. However, raw datasets often contain:

* Missing values
* Blank fields
* Duplicate records
* Unstructured tables that are not optimized for analysis

To solve this problem, I designed a **data cleaning and dimensional modelling process** to convert the raw Swiggy dataset into a **structured analytics model** that supports efficient querying and reporting.

The goal of the project was to answer key business questions such as:

* Which cities generate the most orders?
* Which restaurants are the most popular?
* Which dishes are ordered most frequently?
* What are the revenue and rating patterns across categories?

---

## Dataset Description

The raw dataset contains food delivery order records with the following attributes:

* State
* City
* Restaurant Name
* Location
* Category (Cuisine Type)
* Dish Name
* Price (INR)
* Rating
* Rating Count
* Order Date

---

## Data Cleaning & Validation

### Null Value Detection

I identified missing values in the dataset for the following fields:

* State
* City
* Order_Date
* Restaurant_Name
* Location
* Category
* Dish_Name
* Price_INR
* Rating
* Rating_Count

### Blank Value Detection

I checked for blank or empty string values that could affect data aggregation and analysis.

### Duplicate Detection

To detect duplicate rows, I grouped records based on all business-critical columns to identify repeated entries.

### Duplicate Removal

I removed duplicate records using a window function:

```
ROW_NUMBER() OVER (PARTITION BY columns)
```

This ensured that only one valid record remained for each unique transaction.

---

## Dimensional Modelling (Star Schema)

After cleaning the dataset, I designed a **Star Schema** to optimize analytical queries and reporting.

### Dimension Tables I Created

**dim_date**

* Year
* Month
* Quarter
* Week

**dim_location**

* State
* City
* Location

**dim_restaurant**

* Restaurant_Name

**dim_category**

* Cuisine Category

**dim_dish**

* Dish_Name

### Fact Table

**fact_swiggy_orders**

This table stores measurable metrics including:

* Price_INR
* Rating
* Rating_Count
* Foreign keys referencing all dimension tables

This structure allows efficient joins and faster analytical queries.

---

## KPI Development

After building the schema, I created SQL queries to calculate key business metrics.

### Basic KPIs

* Total Orders
* Total Revenue (INR Million)
* Average Dish Price
* Average Rating

---

## Business Analysis Performed

### Date-Based Analysis

* Monthly order trends
* Quarterly order trends
* Year-wise growth
* Day-of-week order patterns

### Location-Based Analysis

* Top 10 cities with highest order volume
* Revenue contribution by state

### Restaurant Performance Analysis

* Top 10 restaurants by total orders
* Most popular restaurants across cities

### Food Category Analysis

* Most popular cuisine categories
* Most ordered dishes
* Cuisine performance based on orders and average rating

### Customer Spending Analysis

I categorized orders into spending ranges:

* Under 100 INR
* 100–199 INR
* 200–299 INR
* 300–499 INR
* 500+ INR

This helped identify customer purchasing patterns.

### Ratings Analysis

I analyzed the distribution of ratings from **1 to 5 stars** to evaluate customer satisfaction across dishes and restaurants.

---

## Technologies Used

* SQL
* Data Cleaning Techniques
* Window Functions
* Dimensional Modelling
* Star Schema Design
* Git & GitHub

---

## Project Structure

```
Real-World-Swiggy-Sales-SQL
│
├── dataset
│   └── swiggy_data.csv
│
├── sql
│   ├─Swiggy_data.sql
│
├── diagrams
│   └── star_schema_erd.png
│
└── README.md
```

---

## Key Skills Demonstrated

Through this project, I demonstrated the following skills:

* SQL Data Cleaning
* Data Validation
* Duplicate Handling with Window Functions
* Dimensional Data Modelling
* Star Schema Design
* Business KPI Development
* Advanced Analytical SQL Query Writing

---

## Author

**Mithun Appuhamy**
BSc IT Undergraduate – SLIIT
Interested in **Data Engineering, BI Engineering, and Data Analytics**
