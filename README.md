# Telco Customer Churn Analysis (Power BI)

## Overview
Analysis of 7,043 telecom customers to identify the strongest drivers of churn and provide recommendations for customer retention. Built in Power BI Desktop using DAX measures, calculated columns, and cross-tabulation to test both individual churn drivers and any existing relationships between them.

## Key Findings
- **Contract Type is the strongest single driver of churn**: **month-to-month** customers churn at **42.7%**, a **36.0** percentage-point gap compared to customers on longer contracts.
- **The overlap analysis reveals a root cause behind most drivers.** **91.2%** of first-year customers are on month-to-month contracts, and month-to-month customers are also far more likely to pay by electronic check and skip on add-on services.
- **Internet Service Type and Monthly Charges are also dependent on each other.**: Fiber optic customers are almost all concentrated in the highest price bracket ($81-100+/month), suggesting Fiber optic's high churn (41.9%) reflects a price vs. value effect.
- Ten drivers were tested and ranked using a **percentage-point-gap** ranking methodology; gender was tested and ruled out (*0.7-point gap, considered negligible*).

## Dashboard Structure
The report is built across four pages:
1. **Executive Summary** - headline KPIs, ranked driver chart, top recommendations
2. **Driver Deep-Dive** - individual breakdowns of churn rate across Contract Type, Tenure, Payment Method, Internet Service, Monthly Charges, and add-on services
3. **Overlap Analysis** - cross-tabulations to test whether top drivers are independent or overlapping
4. **Customer Explorer** - table with filters for browsing individual customer records

It also includes a persistent left-side navigation panel with slicers and page-navigation buttons.

## File
- `Telco Customer Churn Project.pbix`
(Open in **Power BI Desktop** for full interactivity, including slicers, drill-down, and navigation buttons.)
- A static PDF export is included for quick preview.

## Tools
Power BI Desktop (Power Query (data cleaning), DAX measures and calculated columns, cross-tabulation via Matrix visuals, custom report theme, interactive navigation)

## Methodology
Churn drivers were ranked by **percentage-point gap** between each risk group and the rest of the customer base. Thresholds were set at the point where churn rate showed the **sharpest shift** in the data (especially where continuous variables required grouping (Tenure and Monthly Charges)) rather than using evenly-sized brackets. This improved accuracy over pure consistent bucketing (e.g., Monthly Charges' gap increased from **12.0** to **20.2** points once the threshold was set at the actual point of inflection rather than an arbitrary high-end cutoff).

## Dataset
https://www.kaggle.com/datasets/blastchar/telco-customer-churn
