# Chart Selection Justification

## Overview

The Executive Dashboard was designed to provide retail leadership with a concise, interactive view of business performance. Each visualization was selected based on the business question it answers, following data visualization best practices to ensure clarity, accuracy, and effective decision-making.

---

# 1. Monthly Sales Trend

**Chart Type:** Line Chart

### Business Question
How has monthly sales performance changed over time?

### Why This Chart?
A line chart is the most suitable visualization for time-series data because it clearly shows trends, growth patterns, and seasonal fluctuations across months.

### Fields Used
- **Columns:** Order Date (Month)
- **Rows:** SUM(Sales)
- **Label:** Monthly Sales
- **Filters:** Region, Category, Customer Segment, Ship Mode

### Design Principle Applied
- Used chronological ordering to preserve the time sequence.
- Maintained a clean layout with minimal visual clutter.
- Added a clear title and formatted axes for readability.

### Mistake Avoided
Avoided using a bar chart or pie chart, which would make it difficult to identify sales trends over time.

---

# 2. Regional Performance

**Chart Type:** Horizontal Bar Chart

### Business Question
Which regions generate the highest sales?

### Why This Chart?
A horizontal bar chart allows easy comparison between regions and accommodates region names without reducing readability.

### Fields Used
- **Rows:** Region
- **Columns:** SUM(Sales)
- **Color:** Profit
- **Label:** Sales Value
- **Filters:** Category, Customer Segment, Ship Mode

### Design Principle Applied
- Sorted regions in descending order of sales.
- Used color to represent profit, adding another layer of insight without increasing clutter.
- Displayed labels for quick comparison.

### Mistake Avoided
Avoided pie charts because comparing multiple regions is much easier with aligned bar lengths.

---

# 3. Category Profitability

**Chart Type:** Horizontal Bar Chart

### Business Question
Which product categories and sub-categories contribute the most profit?

### Why This Chart?
A horizontal bar chart is ideal for comparing profitability across many categories and sub-categories while keeping long labels readable.

### Fields Used
- **Rows:** Category and Sub-Category
- **Columns:** SUM(Profit)
- **Color:** Category
- **Label:** Profit
- **Filters:** Region, Customer Segment, Ship Mode

### Design Principle Applied
- Sorted bars by profit to highlight top-performing products.
- Applied consistent category colors throughout the dashboard.
- Used clear labels to improve readability.

### Mistake Avoided
Avoided stacked charts that could hide differences in individual category profitability.

---

# 4. Customer Segment Performance

**Chart Type:** Stacked Bar Chart

### Business Question
How is sales distributed across customer segments and product categories?

### Why This Chart?
A stacked bar chart compares total sales across customer segments while also showing each product category's contribution within the segment.

### Fields Used
- **Columns:** Customer Segment
- **Rows:** SUM(Sales)
- **Color:** Category
- **Label:** Sales
- **Filters:** Region, Ship Mode

### Design Principle Applied
- Used consistent category colors across the dashboard.
- Displayed category contribution without sacrificing total comparison.
- Maintained clear labels and readable titles.

### Mistake Avoided
Avoided multiple separate bar charts, which would make segment comparisons less efficient.

---

# 5. Discount vs Profit

**Chart Type:** Scatter Plot

### Business Question
How do discounts affect profitability?

### Why This Chart?
A scatter plot is the most effective chart for identifying relationships, trends, clusters, and outliers between two continuous variables.

### Fields Used
- **Columns:** Discount
- **Rows:** Profit
- **Color:** Category
- **Size:** Sales
- **Detail:** Order ID
- **Trend Line:** Linear Trend
- **Filters:** Region, Customer Segment, Ship Mode

### Design Principle Applied
- Added a trend line to show the overall relationship between discount and profit.
- Used color to distinguish product categories.
- Included individual marks to reveal outliers.

### Mistake Avoided
Avoided aggregating the data into bars, which would hide the relationship between individual orders, discounts, and profits.

---

# Dashboard Design Principles

The dashboard follows key visualization best practices:

- Appropriate chart types selected for each business question.
- Clear visual hierarchy with KPI cards placed at the top.
- Consistent color usage across visualizations.
- Minimal clutter to improve readability.
- Clear titles, labels, and formatted values.
- Logical sorting for easier comparison.
- Interactive filters (Region, Category, Customer Segment, and Ship Mode) support focused analysis.
- Action filter enables users to click on a region and dynamically update the remaining dashboard views.
- Consistent scales and formatting prevent misleading interpretation.
- Dashboard emphasizes business insights and decision-making rather than displaying raw data.

---

# Conclusion

Each chart was selected to answer a specific business question while following visualization best practices. Together, the dashboard enables leadership to monitor sales performance, identify profitable regions and product categories, understand customer behavior, evaluate discount strategies, and make informed business decisions through an interactive and easy-to-understand interface.
