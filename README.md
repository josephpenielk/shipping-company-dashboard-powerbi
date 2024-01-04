# Power BI Shipping Company Dashboard

Welcome to the Power BI Shipping Company Dashboard project! This dashboard provides insights into sales data for a shipping company, utilizing Power BI and a star schema with a central fact table.

## Project Overview

This project focuses on creating a comprehensive dashboard for a shipping company. It leverages a star schema, where the fact table, `fact_Sale`, is at the center, connected to dimension tables such as `dim_Currency`, `dim_Customer`, `dim_Product`, and a custom `dim_Date` table.

## Project Structure

- **dim_Currency:** Dimension table containing currency information.
- **dim_Customer:** Dimension table with customer details.
- **dim_Product:** Dimension table with product details.
- **fact_Sale:** Fact table containing sales data.
- **dim_Date:** Custom dimension table with date-related information.

## Power BI Report

The Power BI report includes visualizations, metrics, and interactive elements to analyze and understand the shipping company's sales performance.

### Date Table Enhancement

To enhance time-related analysis, a custom `dim_Date` table has been created. It includes Year, Month, Month Name, and Weekday columns.

```DAX
dim_Date = ADDCOLUMNS(
    CALENDAR(MIN(fact_Sale[ShipDate]), MAX(fact_Sale[ShipDate])),
    "Year", YEAR([Date]),
    "Month", MONTH([Date]),
    "Month Name", FORMAT([Date], "MMMM"),
    "Weekday", FORMAT([Date], "DDDD")
)

```

# How to View

To explore the dashboard, follow these steps:

1. **Download Report:**
   - Download the Power BI dashboard file.

2. **Open in Power BI Desktop:**
   - Open the downloaded .pbix file in Power BI Desktop.

3. **Interact with the Dashboard:**
   - Explore various visualizations and insights within Power BI Desktop.

# Screenshots

- **Sales Overview Dashboard:**
  - <img width="625" alt="Dashboard Screenshot 1" src="https://github.com/josephpenielk/shipping-company-dashboard-powerbi/assets/65491428/1308d58d-22ed-4bc4-9bb5-9cba1c55fd66">


- **Female Customer Insights Dashboard:**
  - <img width="631" alt="Dashboard Screenshot 2" src="https://github.com/josephpenielk/shipping-company-dashboard-powerbi/assets/65491428/32912075-fa24-4c5b-b19e-dc497befa3fb">


# Feedback

Your feedback is valuable! If you have any suggestions, improvements, or questions, feel free to open an issue or contact me.

Happy exploring!
