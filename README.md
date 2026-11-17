# Retail Sales Analysis

An Excel-based retail sales analysis project focused on data cleaning, exploratory data analysis, and interactive dashboard development.

### Project Overview

This project analyzes retail sales data from 2022 to 2024 to identify revenue trends, country performance, product performance, and order status patterns.

The main objective is to transform raw data into meaningful business insights using Microsoft Excel.

**Dataset Source:** Kaggle

### 💡 Key Highlights

- Cleaned and transformed raw retail sales data.
- Analyzed revenue across countries and customer segments.
- Examined monthly revenue trends and product performance.
- Evaluated order statuses, discounts, and payment methods.
- Developed an interactive Excel dashboard using Pivot Tables, Pivot Charts, and Slicers.

### Dataset Overview

| Description | Records |
|---|---:|
| Original dataset | 17,010 |
| Cleaned dataset | 13,776 |
| Total removed and excluded | 3,234 |

The dataset covers the period from 2022 to 2024.

### Data Structure & Sheets

The Excel workbook contains seven worksheets:

| Sheet | Description |
|---|---|
| Orders | Original raw dataset |
| Orders_Clean | Cleaned dataset |
| Data_Cleaning_Notes | Documentation of cleaning steps |
| Analyze | Analysis calculations |
| Findings | Key analytical findings |
| Chart_Data | Data prepared for visualizations |
| Dashboard | Interactive sales dashboard |

### Data Cleaning & Transformation

The cleaning process involved removing duplicate and blank records, handling invalid values, and transforming selected columns.

**Records removed or excluded:**

| Reason | Records |
|---|---:|
| Fully blank rows | 15 |
| Duplicate records | 495 |
| Invalid DiscountPct (1.5 / 150%) | 1,523 |
| Missing DiscountPct | 495 |
| Missing UnitPrice | 142 |
| Missing ShippingCost | 564 |
| **Total** | **3,234** |

Additional cleaning steps:

- Corrected 1,678 negative Quantity values (-1) to 1 based on an analytical assumption.
- Recalculated TotalAmount to correct existing calculation errors.
- Standardized date formats using Power Query.
- Standardized customer segment values.
- Handled selected missing values, including replacing missing PaymentMethod values with "Unknown".

**TotalAmount calculation:**

`TotalAmount = Quantity × UnitPrice × (1 − DiscountPct) + ShippingCost`

### Data Quality & Limitations

- Approximately 19% of the original records were removed or excluded during data cleaning.
- Records with invalid discount values or missing critical fields were excluded rather than filled with assumed values.
- Negative quantity values were treated as data-entry errors and changed to positive values. This is an analytical assumption, not a verified explanation from the original data source.
- The distribution of excluded records was not tested for randomness. Therefore, findings apply to the cleaned dataset and may not fully represent the original dataset.

### Exploratory Data Analysis

The analysis focused on:

- Revenue by country and customer segment.
- Product sales performance.
- Discount patterns across products.
- Payment method usage.
- Monthly revenue trends.
- Order status distribution and returned orders.

### Key Business Findings

**Revenue Overview**

| Metric | Amount |
|---|---:|
| Potential Revenue | 8,779,367 |
| Revenue from Active Orders | 5,492,470 |
| Lost Revenue (Cancelled, Returned & Refunded Orders) | 3,286,897 (37.4%) |

*Note: Revenue from Active Orders includes Delivered, Shipped, and Processing orders. Processing orders are included as an analytical assumption. Lost Revenue represents the value associated with cancelled, returned, and refunded orders; it does not necessarily represent a confirmed financial loss.*

**Revenue by Country**

The three highest-revenue countries accounted for 34.76% of Revenue from Active Orders.

| Country | Revenue | Revenue Share |
|---|---:|---:|
| Azerbaijan | 748,572 | 13.63% |
| United States | 604,797 | 11.01% |
| Turkey | 555,844 | 10.12% |
| **Total** | **1,909,213** | **34.76%** |

**Monthly Revenue**

- January recorded the highest monthly revenue at 513,658.
- April recorded the lowest monthly revenue at 398,012.

### Business Recommendations

- Investigate the reasons behind cancelled, returned, and refunded orders, which account for 37.4% of potential revenue.
- Continue monitoring revenue performance in Azerbaijan, the United States, and Turkey, which together contribute 34.76% of active-order revenue.
- Review monthly revenue trends to support sales planning and performance monitoring.

### Dashboard Preview

![Retail Sales Dashboard](images/dashboard.png)

### Tools & Technologies

- Microsoft Excel 2019
- Power Query
- Excel Formulas
- Pivot Tables
- Pivot Charts
- Slicers

### How to Use

1. Download the Excel workbook from this repository.
2. Open the workbook using Microsoft Excel 2019 or a compatible version.
3. Navigate to the Dashboard worksheet.
4. Use the available slicers to interact with the dashboard and explore the results.

### Conclusion

This project demonstrates practical Excel skills in data cleaning, exploratory data analysis, and interactive dashboard development. It transforms raw retail sales data into structured insights that can support business analysis and decision-making.
