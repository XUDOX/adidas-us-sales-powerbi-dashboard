# 👟 Adidas US Sales Performance Dashboard

An interactive Power BI dashboard analyzing ~$900M in Adidas US retail sales across 
2020–2021, built as an end-to-end portfolio project — from data modeling to 
DAX-driven KPIs to a fully interactive 4-page report.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data%20Modeling-blue)

## 📌 Overview

This project explores Adidas's US sales performance across retailers, regions, and 
product categories using a real-world retail dataset. The goal was to build a 
dashboard that doesn't just visualize data, but supports real analytical questions — 
who are the most profitable retail partners, which regions and channels drive margin 
vs. volume, and how do product categories perform seasonally.

**Dataset:** [Adidas US Sales Dataset (Kaggle)](https://www.kaggle.com/datasets/heemalichaudhari/adidas-sales-dataset)  
9,648 transactions | 6 retailers | 50 states | 6 product categories | Jan 2020 – Dec 2021

## 📊 Dashboard Pages

| Page | Description |
|---|---|
| **Executive Overview** | KPI cards, YoY revenue trend, revenue by state (map), sales channel split |
| **Regional Performance** | Region → State → City drill-down, decomposition tree, region/date slicers |
| **Retailer Profitability** | Revenue vs. profit comparison, margin-vs-volume scatter plot, ranked table |
| **Product Category Deep Dive** | Seasonal trends by category (small multiples), treemap, gender breakdown |
| **Retailer Detail** *(drill-through)* | Region → City → Retailer → Sales Method breakdown |

## 🔍 Key Insights

- **Online sales carry the highest average margin (~39%)** despite being the smallest 
  channel by revenue — In-store leads on volume but trails on margin (~36%)
- **West Gear** is the top-performing retailer by revenue (~$243M), narrowly ahead of 
  Foot Locker (~$220M)
- The **West region** outpaces every other region at ~$270M — nearly double the 
  Midwest's ~$136M

## 🛠️ Built With

- **Power BI Desktop** — report design & data modeling
- **Power Query** — data cleaning and transformation
- **DAX** — custom measures including YoY time intelligence, ranking, and margin calculations
- **Star-schema date dimension** for proper time intelligence

## ⚙️ Features

- Drill-down hierarchies (Region → State → City, Gender → Type → Product)
- Cross-page synced slicers (Date, Region)
- Drill-through detail page
- Custom report-page tooltips
- Bookmark-driven view toggles
- Conditional formatting (data bars) on profitability tables

## 📐 Key DAX Measures

\`\`\`DAX
Total Revenue = SUM('Sales'[Total Sales])
Revenue PY = CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Date'[Date]))
Revenue YoY % = DIVIDE([Total Revenue]-[Revenue PY],[Revenue PY])
Revenue per Retailer Rank = RANKX(ALL('Sales'[Retailer]),[Total Revenue])
\`\`\`

## 📁 Repository Structure

\`\`\`
├── Adidas_US_Sales_Dashboard.pbix     # Power BI report file
├── data/
│   └── Adidas_US_Sales_Datasets.xlsx  # Source dataset
├── screenshots/
│   ├── 01_executive_overview.png
│   ├── 02_regional_performance.png
│   ├── 03_retailer_profitability.png
│   └── 04_product_deep_dive.png
└── README.md
\`\`\`

## 🖼️ Preview

<img width="869" height="494" alt="1" src="https://github.com/user-attachments/assets/9ae75462-b605-4c3e-9c94-9679d865460c" />

<img width="876" height="495" alt="2" src="https://github.com/user-attachments/assets/8abace63-54d7-4f87-9f1c-459c35e434d3" />

<img width="872" height="491" alt="3" src="https://github.com/user-attachments/assets/7d252dba-723e-4aa8-9874-67b18dd4a749" />

<img width="875" height="490" alt="4" src="https://github.com/user-attachments/assets/bd5971b6-8952-4f29-b85d-d70c1c8b39a6" />

<img width="880" height="494" alt="5" src="https://github.com/user-attachments/assets/31e6807e-e1f2-40cf-8778-aaf5db846b81" />


## 👤 Author

**Muhammad Yaseen Khan**  
Data Science Graduate | Incoming MSc Data Analytics, CCT College Dublin  
[LinkedIn](#) | [Portfolio](#)
