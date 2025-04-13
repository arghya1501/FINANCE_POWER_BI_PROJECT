# 📊 Power BI Finance Dashboard by Arghyadip Pandey

This repository showcases an interactive **Finance Dashboard** created using Microsoft Power BI. The dashboard visualizes critical financial metrics, including total sales, discounts, shipping costs, and product base margins—broken down by region, city, customer segments, and product categories.

---

## 🧾 Project Structure

```
finance-dashboard/
├── Dashboard/
│   └── FINANCE_DASHBOARD by ARGHYADIP PANDEY.pbix
├── Presentation/
│   └── FINANCE_DASHBOARD_PPT ARGHYADIP PANDEY.pptx
└── README.txt
```

---

## 📌 Key Features

- Region-wise, city-wise financial performance
- KPI cards for Total Sales, Discount, Shipping Cost, and Product Base Margin
- Interactive filters for regional selection
- Drill-down capabilities and AI-powered Q&A
- Sub-dashboards for Sales, Discounts, Shipping Costs, and Product Margins

---

## 🔍 Dashboard Insights

### 📍 City and Region-wise Sales
- Sales distributed across Central, East, South, and West regions.
- Top cities: New York City, Los Angeles, Sanford.

### 💰 Profit by Region
- Pie chart shows profit breakdown:
  - West: 33.05%
  - Central: 24.27%
  - East: 22.22%
  - South: 20.45%

### 📈 Sales Trends
- Monthly analysis shows a decline from January (4.7K) to June (3.9K).

---

## 🧮 DAX Sample Queries

```dax
-- Total Sales
Total Sales = SUM('Sales'[Sales Amount])

-- Profit by Region
Profit by Region = 
SUMMARIZE(
    'Sales',
    'Sales'[Region],
    "Profit", SUM('Sales'[Profit])
)

-- Product Base Margin %
Product Base Margin = DIVIDE(SUM('Sales'[Profit]), SUM('Sales'[Sales Amount]))
```

---

## 🧹 Data Cleaning Process

- **Duplication**: Removed duplicate entries
- **Missing Values**: Handled gaps in sales and shipping data
- **Standardization**: Harmonized currency formats and product names
- **Data Integration**: Combined datasets using region codes and product IDs
- **Validation**: Cross-verified totals to ensure accuracy

---

## 📽️ PowerPoint Summary

The `Presentation/FINANCE_DASHBOARD_PPT ARGHYADIP PANDEY.pptx` includes:

- Dashboard Overview
- Data Profiling, Dictionary, and Lineage
- Sales, Discount, Shipping, and Margin Sub-Dashboards
- Visuals: Line Charts, Bar Graphs, Pie Charts, Donut Charts, Treemaps, and Gauges

---

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone https://github.com/arghya1501/finance-dashboard.git
```

2. Open the `.pbix` file in Power BI Desktop.

3. Refresh and explore the visuals interactively.

---


