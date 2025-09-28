## Project Overview

This repository contains a comprehensive Business Intelligence project that analyzes sales, customer, and profitability data. The primary objective was to transform three raw, disconnected CSV datasets into a fully interactive and insightful Power BI dashboard. This dashboard serves as a single source of truth for stakeholders, enabling them to make data-driven decisions by monitoring key performance indicators (KPIs) and exploring trends across different dimensions.

---

## Dashboard Preview

The final deliverable is an interactive, two-page report that provides a holistic view of the business performance.

### Page 1: Sales Performance & Customer Insights
This page focuses on sales activities, customer loyalty, and product performance at the transaction level.

### Page 2: Profitability & Revenue Analysis
This page provides a higher-level financial overview, focusing on net revenue and profit margins by country, product, and over time.

---

## Business Objectives

The project was designed to address key business challenges related to data fragmentation. The dashboard provides clear answers to critical questions such as:

-   Which countries are our most profitable markets and which have the most loyal customers?
-   What are our top-selling products and how much net revenue do they contribute?
-   How have our sales and profit margins trended over time, and are there any anomalies to investigate?
-   What is the distribution of sales across different regions and products?

---

## Technical Process

The project followed a structured BI development lifecycle from data preparation to final visualization.

### 1. Data Transformation and Loading (ETL)

-   **Tool:** Power Query
-   **Source:** Three raw CSV files (`data/` directory).
-   **Process:**
    -   Connected to the data sources and performed an initial data profiling to identify inconsistencies.
    -   Applied a series of transformations including:
        -   Standardizing data types (e.g., converting text to dates and numbers).
        -   Handling null values and removing duplicate records to ensure data integrity.
        -   Pivoting/Unpivoting columns as needed to create a clean, tabular structure.
    -   Created a dedicated **Calendar Table** using DAX to enable robust time-intelligence analysis.

### 2. Data Modeling

A crucial step was to design an efficient and scalable data model.

-   **Schema:** I implemented a **Star Schema**, which is a BI best practice. This model consists of:
    -   A central **Fact Table** containing quantitative sales transaction data.
    -   Several **Dimension Tables** containing descriptive attributes (e.g., Countries, Products, Dates).
-   **Relationships:** Created one-to-many relationships from the dimension tables to the fact table. This optimized model is the analytical backbone of the report, ensuring fast performance and accurate calculations.

### 3. DAX for KPIs and Measures

To perform meaningful analysis, I created several custom measures using Data Analysis Expressions (DAX).

-   **Key Measures Created:**
    -   `Total Net Revenue`: The sum of all revenue, forming the basis for many analyses.
    -   `Year To Date Profit Margin`: A time-intelligent measure to track profitability within the current year.
    -   `Median Sales`: Chosen over `AVERAGE` to provide a more robust measure of central tendency that is less skewed by unusually high or low transaction values.

---

## Key Insights & Findings

The dashboard successfully uncovered several actionable insights:

1.  **High-Value Market Identification:** While the UK and USA show the highest customer engagement (via loyalty points), **UAE is the most valuable market**, contributing over **45% of the median sales value**. This suggests an opportunity to focus marketing efforts on acquiring more high-spending customers in Australia.

2.  **Profitability Anomaly:** A significant and alarming dip in the **yearly profit margin to 34.38% occurred in October 2023**. This is a critical deviation from the stable ~62% margin and requires immediate investigation into product costs, sales discounts, or a change in product mix during that month.

3.  **Revenue Concentration:** The **'Modular Sofa Set' is the top revenue-generating product** by a substantial margin. This product should be a primary focus for the investigation into the October profit margin dip, as its performance has a major impact on overall profitability.

---

## How to Use This Repository

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    ```
2.  **Explore the files:**
    -   `/data/`: Contains the three original raw CSV files used for the project.
    -   `Executive Dashboard.pbix`: The final Power BI project file. You will need **Power BI Desktop** (a free application from Microsoft) to open and interact with the report.

---

## Tools & Technologies

-   **BI & Visualization:** Microsoft Power BI
-   **Data Transformation:** Power Query
-   **Data Modeling & Calculations:** DAX (Data Analysis Expressions)
-   **Version Control:** Git & GitHub

---

## Author & Contact

-   **Addakhili Ibrahim**
