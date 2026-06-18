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

## Dashboards

### Dashboard 1 - Product Sales
- Revenue 
- Profit
- Top/bottom performing products and brands
- Category breakdown
- Monthly trend
![Product Sales](https://github.com/adeolaolotu/Global-Electronics-Retailer-Power-BI-Analysis/blob/baa53963e07fbffdebb7f4f6b55f7a5085f737ed/Electronic%20Store%20-%20Product%20Sales.PNG)

### Dashboard 2 - Customer Analysis
- Customer demographics
- Age group segmentation
- Gender split
- Top customers by revenue
- Retention rate trends
- Revenue by age group
- Customer-level deep dive
![Customer Analysis](https://github.com/adeolaolotu/Global-Electronics-Retailer-Power-BI-Analysis/blob/baa53963e07fbffdebb7f4f6b55f7a5085f737ed/Electronic%20Store%20-%20Customer%20Analysis.PNG)

### Dashboard 3 - Store Analysis
- Store location performance
- Online vs. physical channel mix
- Store age category
- Revenue per square meter
![Store Analysis](https://github.com/adeolaolotu/Global-Electronics-Retailer-Power-BI-Analysis/blob/baa53963e07fbffdebb7f4f6b55f7a5085f737ed/Electronic%20Store%20-%20Store%20Analysis.PNG)

## Key Findings
- Revenue, profit, units sold, and orders all grew consistently from 2016 to 2019, then declined sharply in 2020 — most plausibly linked to COVID-19 disruption
- December is the peak sales month every year; April is the consistent low point. This is a recurring seasonal pattern, confirmed across individual years, not a one-time COVID effect
- Average Order Value declined 1.2% year-on-year despite growth in every volume metric
- Adventure Works, Contoso, and Wide World Importers are the top three brands by profit; Computers is the leading product category
- The United States generates the highest profit by a wide margin; physical stores account for 79.55% of revenue versus 20.45% online
- Veteran stores (15+ years) generate $27M in profit compared to just $2M from stores under 10 years old
- The United States also leads in revenue per square meter ($626); Australia trails at $227
- Customers aged 60+ are the highest-value segment, generating $26M in revenue, while customers aged 18–25 generate just $1M
- Year-over-year customer retention improved steadily from 10.9% (2016) to a peak of 30.1% (2019), before falling to 17.2% in 2020 alongside the broader downturn

## Insights & Recommendations
### Revenue & Profit Performance
- Growth from 2016–2019 reversed sharply in 2020 in line with COVID-19. Recommend tracking recovery against the 2019 baseline and building demand-shock contingency plans.
Seasonality
- December is consistently the strongest month; April is consistently the weakest, every year. Recommend aligning inventory, staffing, and promotions accordingly — heavier investment ahead of December, and using the April lull for clearance sales or internal initiatives like staff training.
- 
### Average Order Value
- AOV is slipping even as order volume grows. Recommend investigating product mix shifts and testing bundling or upsell strategies to lift basket size.
- 
### Product & Brand Performance
- A small number of brands and the Computers category drive most profit. Recommend prioritizing investment there while reviewing the long-term fit of consistently weak performers.
- 
### Geographic & Channel Performance
- The business is heavily reliant on physical stores and the US market. Recommend evaluating online channel investment given the shift toward e-commerce industry-wide.

### Store Maturity & Efficiency
- Older stores significantly outperform newer ones, and store efficiency (revenue per square meter) varies widely by country. Recommend reviewing new-store ramp-up support and auditing underperforming markets like Australia.

### Customer Base
- The 60+ age group is the most valuable customer segment by far, while 18–25 year-olds are underrepresented. Recommend protecting loyalty among older customers while developing strategies to attract younger buyers.

### Retention
- Retention grew steadily for four years before dropping in 2020. Recommend identifying what drove the 2016–2019 improvement and working to restore those conditions.
