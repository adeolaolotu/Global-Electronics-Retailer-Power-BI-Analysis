# Global-Electronics-Retailer-Power-BI-Analysis
## Overview
This project explores the full sales, customer, product, and store performance of a global electronics retailer using Power BI. It covers the complete analytics workflow: data cleaning in Power Query, star-schema data modeling, DAX measure creation, and a four-page interactive dashboard built for executive reporting.
### Dataset
The dataset consists of six related tables:
- **Sales**: 62,884 transaction line items (2016–2020), including order date, delivery date, customer, store, product, quantity, and currency
- **Customers**: 15,266 customer records with demographics and location
- **Products**: 2,517 products across 8 categories with cost and price data
- **Stores**: 67 stores across 8 countries plus one online store
- **Exchange Rates**: Daily currency exchange rates for USD, CAD, AUD, GBP, and EUR
- **Data Dictionary**: Field-level documentation for all tables
  
## Tools Used
- Power BI Desktop
- Power Query (ETL & Data Cleaning)
- DAX (Data Modelling & Calculations)

## Data Cleaning
**Key cleaning steps performed in Power Query:**
- Converted Order Date, Delivery Date, Birthday, and Open Date from text to proper date format (corrected a locale mismatch causing parsing errors)
- Confirmed null Delivery Date values were valid (physical store orders have no delivery, only online orders do)
- Cleaned Unit Cost USD and Unit Price USD by removing currency symbols and converting to numeric

## Data Modelling
The model follows a star schema, with Sales as the fact table at the center, connected to four dimension tables: Customers, Products, Stores, and a custom Calendar date table. 
![Data Modelling](https://github.com/adeolaolotu/Global-Electronics-Retailer-Power-BI-Analysis/blob/5a94469da467ce61849ea77a79a59becb6d91b72/Electronic%20Store%20-%20Data%20Modelling.PNG)

**Key DAX measures include:** Revenue, Profit, Profit Margin %, Average Order Value, Customer Retention Rate, Revenue per Square Meter, and a dynamic color-coded YoY indicator for KPI cards.
