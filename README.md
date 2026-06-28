# Retail Executive Dashboard - Tableau

## Business Problem Summary

Retail leadership requires a centralized executive dashboard to monitor business performance across multiple dimensions, including sales, profitability, customer segments, regional performance, shipping efficiency, discount impact, and return patterns. The objective of this project is to transform raw transactional data into an interactive Tableau dashboard that enables leadership to identify business opportunities, operational risks, and areas for improvement through data-driven decision-making.

---

# Dataset Description

The dataset used in this project is:

**dashboard_sales_data.xlsx**

The dataset contains retail transaction records with information related to:

- Order Date
- Ship Date
- Sales
- Profit
- Discount
- Quantity
- Customer Segment
- Region
- State
- Category
- Sub-Category
- Ship Mode
- Campaign Channel
- Returned Orders
- Delivery Days

This dataset was imported into Tableau for data visualization and dashboard creation.

---

# Tableau Workbook Description

The Tableau packaged workbook is saved as:

```
tableau/executive_dashboard.twbx
```

The workbook contains:

- Individual worksheets for each business visualization
- KPI worksheets
- One interactive executive dashboard
- Interactive filters
- Dashboard action filter
- Calculated fields

The workbook is packaged (.twbx) to ensure that the data source is included.

---

# Calculated Fields Created

The following calculated fields were created in Tableau:

| Calculated Field | Formula / Logic |
|------------------|-----------------|
| Profit Margin | Profit / Sales |
| Cost | Sales - Profit |
| Average Order Value | Sales / COUNTD(Order ID) |
| Return Rate | Returned Orders / Total Orders |
| Shipping Delay Bucket | Categorizes delivery days into delay ranges |

These calculated fields support KPI reporting and business analysis.

---

# Dashboard Components

The executive dashboard includes:

### KPI Cards

- Total Sales
- Total Profit
- Profit Margin

### Visualizations

- Monthly Sales Trend (Line Chart)
- Regional Performance (Horizontal Bar Chart)
- Category Profitability (Horizontal Bar Chart)
- Customer Segment Performance (Stacked Bar Chart)
- Discount vs Profit Analysis (Scatter Plot)

---

# Filters and Interactions Used

## Interactive Filters

The dashboard includes the following interactive filters:

- Region
- Category
- Customer Segment
- Ship Mode

Each filter updates all relevant dashboard views and KPI cards.

## Dashboard Action Filter

An action filter has been implemented where selecting a region from the **Regional Performance** chart dynamically filters the remaining dashboard components, allowing users to perform focused regional analysis.

---

# Key Business Insights

Major insights obtained from the dashboard include:

- Monthly sales fluctuate throughout the year, indicating seasonal demand patterns.
- The South region generates the highest sales performance.
- Technology products contribute the highest profitability.
- Furniture products generate comparatively lower profits.
- Consumer and Home Office segments contribute strong sales performance.
- Higher discounts generally reduce profitability.
- Shipping performance varies across shipping modes.
- Return patterns indicate opportunities for product quality and process improvements.

Detailed insights are available in:

```
outputs/business_insights.md
```

---

# Dashboard Story Summary

The dashboard tells the overall business story by combining sales performance, profitability, customer behavior, regional analysis, operational performance, and pricing strategy into a single executive view.

It enables leadership to:

- Monitor business health
- Identify high-performing regions and categories
- Detect profitability risks
- Evaluate discount effectiveness
- Support strategic decision-making through interactive analysis

The complete dashboard story is available in:

```
outputs/dashboard_story.md
```

---

# Assumptions and Limitations

## Assumptions

- Dataset is complete and accurate.
- Sales and profit values are correctly recorded.
- Delivery Days accurately represent shipping performance.
- Returned order information is correctly captured.

## Limitations

- Analysis is based only on the provided historical dataset.
- External market conditions are not included.
- Customer demographics and competitor information are unavailable.
- Marketing expenditure and inventory data are outside the scope of this dashboard.

---

# Screenshots Included

The repository includes the following dashboard screenshots:

```
screenshots/
│── full_dashboard.png
│── sales_trend_view.png
│── regional_performance_view.png
│── category_profitability_view.png
│── filter_interaction_view.png
```

These screenshots provide evidence of dashboard functionality and interactivity.

---

# Repository Structure

```
part4_tableau_dashboard/
├── data/
│   └── dashboard_sales_data.xlsx
├── tableau/
│   └── executive_dashboard.twbx
├── outputs/
│   ├── dashboard_story.md
│   ├── business_insights.md
│   └── chart_selection_justification.md
├── screenshots/
│   ├── full_dashboard.png
│   ├── sales_trend_view.png
│   ├── regional_performance_view.png
│   ├── category_profitability_view.png
│   └── filter_interaction_view.png
└── README.md
```

---

# Project Deliverables

This repository contains all required deliverables:

- ✔ Dataset (`dashboard_sales_data.xlsx`)
- ✔ Tableau Packaged Workbook (`executive_dashboard.twbx`)
- ✔ Dashboard Story (`dashboard_story.md`)
- ✔ Business Insights (`business_insights.md`)
- ✔ Chart Selection Justification (`chart_selection_justification.md`)
- ✔ Dashboard Screenshots
- ✔ README Documentation

All required files are included and follow the prescribed folder structure and naming conventions.
