# Olist E-Commerce Data Analysis

Business-Oriented Analysis of the Olist Brazilian E-Commerce Public Dataset

**Author:** Youssef Atef Tayh

---

## Project Overview

This project explores the Olist Brazilian E-Commerce Public Dataset from both a data and business perspective.

The goal was not only to analyze the data, but to understand the business context behind the dataset, evaluate data quality, identify meaningful patterns, and translate the findings into practical business questions and potential Data / AI opportunities.

The project follows a structured analytical workflow:

Research → Dataset Understanding → Data Quality → Exploratory Analysis → Business Findings → Data / AI Opportunities

---

## Objectives

The main objectives of this project are to:

- Understand the Olist business model and historical context.
- Understand the structure and relationships between the dataset tables.
- Identify data quality issues and document their impact.
- Explore customer, seller, order, product, payment, delivery, freight, and review data.
- Identify meaningful patterns from the historical data.
- Translate analytical findings into business questions.
- Identify areas where Data and AI could support business decisions.
- Prepare the analysis as a foundation for dashboards, reporting, and further business validation.

---

## Dataset

The project uses the **Olist Brazilian E-Commerce Public Dataset**, which contains historical e-commerce data covering approximately the 2016–2018 period.

The dataset is organized into multiple related tables representing different parts of the e-commerce ecosystem.

### Main Tables

| Table | Description |
|---|---|
| Customers | Customer information and geographic identifiers |
| Orders | Order records and order lifecycle timestamps |
| Order Items | Products and sellers associated with orders |
| Payments | Payment methods, values, and installments |
| Reviews | Customer review scores and review information |
| Products | Product attributes and categories |
| Sellers | Seller information and geographic identifiers |
| Geolocation | Geographic information based on postal code prefixes |
| Category Translation | Portuguese-to-English product category translation |

---

## Project Workflow

### 1. Historical Company Research

Before analyzing the data, the historical business context of Olist was researched to understand:

- Who Olist served
- What business problems it addressed
- How Olist connected merchants with online marketplaces
- The role of orders, payments, logistics, and customer experience
- The relationship between Olist's business activities and the available dataset

The research uses a historical perspective because the dataset represents the 2016–2018 period.

---

### 2. Dataset Understanding

The first analytical stage focused on understanding the structure of the dataset.

This included:

- Loading and inspecting all tables
- Reviewing columns and data types
- Understanding the grain of each table
- Identifying primary keys and relationship keys
- Reviewing missing values
- Checking duplicate records
- Understanding the order lifecycle
- Reviewing geographic information
- Understanding category translation

The goal of this stage was to understand what each table represents before performing business analysis.

---

### 3. Data Quality

The data quality stage examined potential issues that could affect the analysis.

Checks included:

- Missing values
- Exact duplicate rows
- Negative values
- Invalid payment installment values
- Order lifecycle inconsistencies
- Delivery date inconsistencies
- Duplicate geographic records

Important findings were documented rather than silently changing the original data.

For example, some records contain unusual order lifecycle timestamps. These records were flagged for investigation instead of being automatically removed.

This approach keeps the analysis transparent and preserves the original dataset.

---

### 4. Exploratory Data Analysis

The EDA stage focuses on understanding the main business dimensions represented in the dataset.

The analysis covers:

- Order activity
- Sales value
- Customer behavior
- Seller activity
- Product categories
- Geographic distribution
- Payment methods
- Payment behavior
- Delivery performance
- Freight value
- Customer reviews

Visualizations were used to make important patterns easier to interpret.

---

## Business Questions

The analysis was structured around business questions rather than only technical statistics.

Examples include:

### Sales and Demand

- How does order activity change over time?
- Which product categories generate higher sales value?
- How concentrated is sales activity among sellers?

### Customers

- Where are customers geographically concentrated?
- What patterns can be observed in customer purchasing behavior?

### Sellers

- How is seller activity distributed?
- Are sales values concentrated among a smaller group of sellers?

### Payments

- Which payment methods are most frequently used?
- How are payment installments distributed?

### Logistics

- How long does the order lifecycle take?
- How frequently are orders delivered after the estimated delivery date?
- How significant is freight value relative to item sales value?

### Customer Experience

- How are customer review scores distributed?
- Is there an observable relationship between delivery performance and review scores?

These questions are intended to support further business validation rather than claim that the dataset proves a current Olist problem.

---

## Key Analytical Areas

### Order and Sales Analysis

Order-level and item-level data were combined to examine sales activity and order value patterns.

The analysis distinguishes between:

- Order count
- Item count
- Item sales value
- Freight value

This prevents different business metrics from being treated as the same measure.

### Seller Analysis

Seller performance was explored using item-level sales value and item activity.

The analysis helps identify how marketplace activity is distributed across sellers and provides a basis for further seller segmentation.

### Geographic Analysis

Customer and seller geographic information was analyzed using postal code prefixes.

This provides a high-level view of where marketplace participants are distributed across Brazil.

### Payment Analysis

Payment records were analyzed to understand:

- Payment methods
- Payment value
- Installment behavior

Payment records were also interpreted carefully because one order can contain multiple payment records.

### Delivery Analysis

Order timestamps were used to examine the order lifecycle:

Purchase → Approval → Carrier Handoff → Customer Delivery

Actual delivery dates were also compared with estimated delivery dates to identify late deliveries.

### Freight Analysis

Freight value was compared with item sales value to understand the relative weight of shipping costs within the historical transaction data.

This metric is treated as an analytical indicator rather than Olist revenue.

### Review Analysis

Customer review scores were analyzed to understand the distribution of customer feedback.

Delivery-related metrics were also compared with review outcomes as an observational analysis.

The analysis does not treat correlation as proof of causation.

---

## Data Quality Considerations

The project does not automatically remove every unusual record.

Instead, the approach is:

1. Detect the issue.
2. Quantify the affected records.
3. Inspect representative records where necessary.
4. Document the issue.
5. Decide whether the issue should affect a specific analysis.

This makes the analytical process more transparent and reproducible.

---

## Business Interpretation

The analysis moves beyond describing charts by connecting observed patterns to possible business questions.

Examples of potential areas for further investigation include:

- Delivery performance and logistics efficiency
- Seller performance monitoring
- Customer experience analysis
- Payment behavior
- Geographic demand patterns
- Product and category performance
- Freight and delivery cost analysis

These are analytical opportunities derived from the historical dataset and should be validated against current business priorities before being treated as confirmed operational problems.

---

## Potential Data / AI Opportunities

Based on the analysis, several areas could be explored in a future Data / AI solution.

### Analytics & Decision Systems

Centralized dashboards and KPI monitoring could help decision-makers track:

- Orders
- Sales value
- Delivery performance
- Seller activity
- Customer experience
- Freight indicators

### Logistics Intelligence

Historical delivery data could support:

- Delivery performance monitoring
- Late-delivery analysis
- Geographic logistics analysis
- Carrier performance analysis

### Customer Intelligence

Customer and review data could support:

- Customer segmentation
- Review analysis
- Customer experience monitoring
- Identification of patterns associated with lower review scores

### Forecasting & Predictive Analytics

Historical order and sales patterns could potentially support:

- Demand forecasting
- Category-level forecasting
- Seller activity forecasting
- Operational planning

### Automation & Data Pipelines

The multi-table structure of the dataset also provides a foundation for automated:

- Data ingestion
- Data validation
- Transformation
- KPI generation
- Reporting

These opportunities represent potential directions for future work, not implemented production systems.

---

## Project Structure

```text
olist-ecommerce-data-analysis/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_Olist_Dataset_Understanding.ipynb
│   ├── 02_Olist_Data_Quality.ipynb
│   └── 03_Olist_EDA_Business_Insights.ipynb
│
├── research/
│   └── olist_company_research.md
│
├── powerbi/
│
├── reports/
│
├── presentation/
│
├── src/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Notebooks

### `01_Olist_Dataset_Understanding.ipynb`

Focuses on:

- Dataset structure
- Table inventory
- Data grain
- Columns and data types
- Relationships
- Missing values
- Duplicate records
- Order lifecycle
- Geographic structure

### `02_Olist_Data_Quality.ipynb`

Focuses on:

- Missing-value analysis
- Duplicate analysis
- Invalid values
- Payment anomalies
- Lifecycle inconsistencies
- Data quality documentation

### `03_Olist_EDA_Business_Insights.ipynb`

Focuses on:

- Order and sales analysis
- Customers
- Sellers
- Products and categories
- Geography
- Payments
- Delivery performance
- Freight
- Customer reviews
- Business questions
- Data / AI opportunities

---

## Technologies

The project uses:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Power BI
- Git
- GitHub

---

## Analytical Approach

The project follows a business-oriented data analysis approach:

```text
Historical Research
        ↓
Dataset Understanding
        ↓
Data Quality
        ↓
Exploratory Data Analysis
        ↓
Business Findings
        ↓
Business Questions
        ↓
Data / AI Opportunities
```

The main principle is to avoid treating a dataset as a collection of isolated columns.

Instead, the analysis connects:

**Business Context → Data → Evidence → Interpretation → Opportunity**

---

## Limitations

Several limitations should be considered when interpreting the results.

### Historical Dataset

The dataset represents a historical period around 2016–2018.

Therefore, the findings should not automatically be interpreted as a description of Olist's current operations.

### Dataset Scope

The dataset provides transaction-level and operational information, but it does not contain every aspect of Olist's business.

For example, it does not provide a complete view of:

- Company financial performance
- Internal operating costs
- Marketing spend
- Customer acquisition costs
- Current business strategy
- Current operational priorities

### Business Validation

The analytical findings represent evidence from the dataset.

They should be treated as hypotheses and business questions that require validation with current Olist stakeholders before being used to make operational decisions.

---

## Future Work

Potential next steps include:

- Building an executive Power BI dashboard
- Creating reusable analysis-ready datasets
- Developing deeper seller and customer segmentation
- Performing advanced logistics analysis
- Building demand forecasting models
- Exploring predictive delivery analysis
- Developing customer review intelligence
- Creating automated data pipelines
- Connecting analytical findings to current business requirements

---

## Author

**Youssef Atef Tayh**

Computer Science and Information Technology

Data Analytics | Data Science | AI

---

## Note

This repository is an analytical and educational project based on the public Olist Brazilian E-Commerce dataset.

The analysis is intended to demonstrate a complete business-oriented Data Analytics workflow, from research and data understanding to business interpretation and potential Data / AI opportunities.
