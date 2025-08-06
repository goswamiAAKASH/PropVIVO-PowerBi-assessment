# ** PropVivo Sales Dashboard & Case Study **

This repository contains my submission for the **PropVivo Power BI Assessment**, covering:
- A fully interactive **Sales Performance Dashboard** (Part 1)
- A conceptual **Business Strategy & BI Design Case Study** (Part 2)

---

## Problem Statement:

PropVivo, a rapidly growing retail company, wants to improve its business decision-making and operational visibility. You are tasked with:

- Building an insightful Power BI dashboard using a raw sales dataset
- Providing analytical and business insights for better decision making
- Designing a BI solution for the expansion of **Urban Threads**, a new business segment

---

## Part 1: Sales Performance Dashboard

### Objectives:
- Monitor revenue, orders, and customer trends
- Identify top-performing products and regions
- Enable slicing by Region, Product, Month, and Category

### Key KPIs:
- Total Revenue
- Total Orders
- Average Order Value (AOV)
- Total Customers

### Visuals:
- KPI Cards (4 cards at top)
- Line Chart: Monthly Revenue Trend
- Bar Chart: Top 10 Products by Revenue
- Donut Chart: Revenue by Region
- Matrix: Region × Category with Conditional Formatting
- Slicers: Region, Product Name, MonthYear, Category

### Time Intelligence:
DAX
* MonthYear = FORMAT(Sales[Date], "MMM-YYYY")

### DAX Measures Used:
* Total Revenue = SUM(Sales[UnitPrice] * Sales[Quantity])
* Total Orders = DISTINCTCOUNT(Sales[TransactionID])
* Average Order Value = [Total Revenue] / [Total Orders]
* Total Customers = DISTINCTCOUNT(Sales[CustomerID])

### Page Layout:
* Page 1: Sales Overview
- 4 KPI Cards
- Monthly Revenue Line Chart

* Page 2: Product & Region Insights
- Bar Chart (Top Products)
- Donut Chart (Revenue by Region)
- Matrix (Region × Category)
- 4 Slicers grouped with heading

### Folder / File Structure:
```
PropVIVO-PowerBi-assessment/
├── Power Bi Project 1.docx
├── README.md
├── DashBoard_summary_and_Dashboard(PBI)/
│   ├── PropVivo_Dashboard_Summary.docx
│   ├── PropVivo_Dashboard_Summary.pdf
│   ├── propVIVO.pbix
├── PowerBI_Case_Study_Assessment/
│   ├── PowerBI_Case_Study_Assessment.docx
│   ├── UrbanThreads_CaseStudy.docx
│   ├── UrbanThreads_CaseStudy_ANS.pdf
├── cleaning_dataset_using_PY/
│   ├── clean_the_dataset.ipynb
│   ├── PowerBI_Cleaned_Dataset.xlsx
├── uncleaned dataset/
│   ├── PowerBI_Uncleaned_Dataset-Project1.xlsx
├── screenshots of dashboards/
│   ├── overview.png
│   ├── Product & Regional Insights.png
```


## Part 2: Case Study – Urban Threads Expansion
----
### Objective:
- Design a scalable Power BI strategy for a new business unit (Urban Threads) entering Tier 2 & Tier 3 cities.

### Summary of Case Study Answers:
* Suggested KPIs:
- Sales Growth %, Customer Retention Rate, Regional Revenue

* Dashboard Design:
- Multi-page dashboard with city-level drilldowns

*Data Model: 
- Star schema with fact (Sales) and dimension tables (Product, Region, Customer)

* Audience: 
- Management, Sales Head, Regional Manager, CXOs

* Insights:
- Underperforming regions, high shipping costs, low coupon usage

### Screenshots:

- (Inside the screenshots of dashboards folder)
- Dashboard Page 1 (Sales Overview)
- Dashboard Page 2 (Product & Region Insights)

### DAX code view:
- Data Model (3-table star schema)
- Business Insights Highlighted
- Revenue concentrated in a few cities
- Top 10 products account for ~65% of revenue
- Shipping cost affects Tier 2/3 order completion
- High correlation between coupon usage and repeat orders


### Tools Used: 
* Power BI
* Excel
* Python (for Data cleaning)

### Author
~ Akash Goswami
- B.Tech CSE | Data Analyst | Power BI Developer
