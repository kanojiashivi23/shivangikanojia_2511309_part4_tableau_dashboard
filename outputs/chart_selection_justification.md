# Chart Selection Justification

## Objective

The dashboard was designed to provide retail executives with a clear overview of business performance by highlighting sales trends, profitability, customer behavior, regional performance, and the impact of discounts. Each visualization was selected to answer a specific business question while following Tableau visualization best practices.

---

# 1. Monthly Sales Trend

**Chart Type:** Line Chart

### Business Question
How have sales changed over time?

### Why this chart?
A line chart is the most appropriate visualization for displaying trends over time because it clearly shows increases, decreases, and seasonal patterns in monthly sales.

### Fields Used
- **Columns:** Month(Order Date)
- **Rows:** SUM(Sales)

### Design Principles Applied
- Chronological order maintained.
- Minimal clutter by avoiding unnecessary visual elements.
- Readable title and axis labels.
- Consistent formatting.

### Mistakes Avoided
- Did not use a bar chart for time-series data.
- Avoided misleading scales by starting the axis at zero.

---

# 2. Regional Sales & Profit Performance

**Chart Type:** Horizontal Bar Chart

### Business Question
Which regions generate the highest sales and profit?

### Why this chart?
A horizontal bar chart makes it easy to compare performance across regions and quickly identify the best and worst performing areas.

### Fields Used
- **Rows:** Region
- **Columns:** SUM(Sales)
- **Color:** SUM(Profit)

### Design Principles Applied
- Regions sorted by sales in descending order.
- Color intensity represents profit performance.
- Labels improve readability.

### Mistakes Avoided
- Avoided pie charts, which make regional comparisons difficult.
- Used consistent color encoding for profit.

---

# 3. Category & Sub-Category Profitability

**Chart Type:** Horizontal Bar Chart

### Business Question
Which product categories and sub-categories contribute the most profit?

### Why this chart?
Horizontal bars effectively compare profitability across multiple categories and sub-categories while accommodating long category names.

### Fields Used
- **Rows:** Category, Sub-Category
- **Columns:** SUM(Profit)

### Design Principles Applied
- Descending sorting highlights the most profitable products first.
- Consistent color scheme across categories.
- Clear labels improve interpretation.

### Mistakes Avoided
- Avoided stacked charts that could hide individual profitability.
- Maintained consistent sorting for easy comparison.

---

# 4. Sales by Customer Segment

**Chart Type:** Stacked Bar Chart

### Business Question
How does sales performance vary across customer segments and product categories?

### Why this chart?
A stacked bar chart allows comparison of total sales by customer segment while also showing each category's contribution within the segment.

### Fields Used
- **Columns:** Customer Segment
- **Rows:** SUM(Sales)
- **Color:** Category

### Design Principles Applied
- Consistent category colors.
- Clear segment comparison.
- Data labels added for readability.

### Mistakes Avoided
- Avoided pie charts because comparing multiple segments is easier with stacked bars.
- Prevented unnecessary visual clutter.

---

# 5. Discount vs Profit

**Chart Type:** Scatter Plot

### Business Question
How do discounts influence profitability?

### Why this chart?
A scatter plot is the most appropriate visualization for identifying relationships, trends, clusters, and outliers between two numerical variables.

### Fields Used
- **Columns:** Discount
- **Rows:** Profit
- **Detail:** Order ID
- **Color:** Category
- **Size:** Sales

### Design Principles Applied
- Trend line added to identify overall relationship.
- Zero-profit reference line highlights loss-making orders.
- Different colors distinguish product categories.

### Mistakes Avoided
- Avoided bar charts because they cannot effectively display relationships between two continuous variables.
- Prevented misleading interpretation by displaying individual orders instead of aggregated values.

---

# Dashboard Design Principles

The executive dashboard follows key visualization best practices:

- Appropriate chart types selected for each business question.
- Clear visual hierarchy with KPI cards positioned at the top.
- Consistent color usage throughout the dashboard.
- Minimal clutter by avoiding unnecessary decorations.
- Readable chart titles and labels.
- Logical sorting of categories and regions.
- Interactive filters (Region, Category, Customer Segment, Ship Mode) support focused analysis.
- Action filter enables dynamic exploration by allowing users to click on a region and update the entire dashboard.
- Consistent scales and formatting improve readability and prevent misleading interpretations.
- Dashboard emphasizes business insights and decision-making rather than displaying raw data.

---

# Summary

The selected visualizations were chosen to answer specific business questions while ensuring clarity, readability, and ease of interpretation. Together, the charts provide leadership with a comprehensive view of sales performance, profitability, customer behavior, regional performance, and discount effectiveness, enabling informed business decisions.
