# Supermarket Sales Analysis
## Table of contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results/Findings](#resultsfindings)
- [Reccomendations](#recommendations)
- [Limitation](#limitations)
- [References](#references)

### Project Overview

The **Supermarket Sales Analysis** project is a comprehensive data analytics solution designed to evaluate,
track, and visualise retail performance metrics across multiple operational dimensions. This project empowers stakeholders with actionable intelligence regarding revenue generation, customer ordering behaviours, regionanal
profitability, and product-level demand.



### Data Sources


Maven Analytical Playground/sample Retail Transactional Datasets


### Tools

- Excel - Data cleaning [Download here](https://microsoft.com)
- SQL Server - Data Analysis [Download here](https://mysqlserver.com)
- PowerBI -DAX Measures & Creating report.



### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:
1. Data loading and Inspection
2. Handling missing values
3. Correcting data types
4. Correcting inconsistency in Names.



### Exploratory Data Analysis

EDA  involved exploring the sales data to answer key questions, such as:
- Total revenue generated
- Sales trend by Month
- Total Customer
- Top selling Products
- Total Order
- Total Sale by Region

### Data Analysis

Include some interesting code/feature worked with


```PowerBI Dax
Product YOY % = 
    VAR _PERC = DIVIDE([Total Product] -[Product Previous Year],[Product Previous Year])
    VAR _FORMAT =
    SWITCH(
        TRUE(),
        _PERC >0,UNICHAR(8593) & " " & FORMAT(_PERC,"0.00%"),
        _PERC<0,UNICHAR(8595) & " " & FORMAT(_PERC*-1,"0.00%"),
        FORMAT(_PERC,"0.00%")
    )
    RETURN
    _FORMAT
```
### Results/Findings

1. The **Supermarket** generated a cumulative multi-year revenue of **$2.30M** across **9994** totals Orders.
2. Revenue generation is led heavily by costal and regional markets, with the West($725k) and East($679k) outperforming the Central($501k) and South($392k) territories.
3. Market reach spans three primary business segments(Customer,Corporate and Home Office), with the Customer segment capturing the largest overall share of total revenue.
4. Customer fulfilment preferences heavily favor cost-efficiency over speed, with Standard Class shipping having yhe highest.
5. Sales trend demonstrate consistent mid-year stability followed by a sharp upward surge in late Q3, culminating in annual revenue peaks September($0.31M), November($0.35M),and December($0.33M).
6. High-volume inventory leaders include Phones($0.33M in sales, 3,289 quantity, $44,516 profit) and Storage ($223,844 in sales, 3,158 quantity, $21,279 profit).

### Recommendations

1. Invest targeted marketing and regional sales efforts into underperforming territories like the South and Central region to bridge the revenue gap with top-performing markets like the West and East
2. Use State-level sales density maps to pinpoint localised geographic pockets with high growth potential, tailoring regional ad spend and distribution logistics accordingly.
3. Leverage the overwhelming customer preference for Standard Class shipping by negotiating bulk carrier rates to further voptimize supply chain margins.
4. Implement targeted promotional campaigns during mid-year demand trough to smooth out revenue volatilityand maintain steady cash flow throughout Q1 & Q2.


### Limitations
- Inconsistency in Name
- Missing values
- Some columns have wrong dataset

### References

- **Reporting & visualisation**: Microsoft Power Bi Desktop(utilizing DAX data modeling, custom KPI cards, choropleth map visuals, and custom corporate emerald color themes).
- Maven Analytics Data [download here](https://mavenanalytics.io/data-playground)




