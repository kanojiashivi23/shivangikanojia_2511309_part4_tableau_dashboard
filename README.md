
## Task 1: Connect and Inspect Data

The dataset `dashboard_sales_data.xlsx` was loaded into Tableau. The fields were inspected and categorized to ensure accurate analysis:

### Field Classification
| Category | Fields |
| :--- | :--- |
| **Date Fields** | `order_date`, `ship_date` |
| **Geographic Fields** | `region`, `state`, `city` |
| **Categorical Fields** | `customer_segment`, `category`, `sub_category`, `product_name`, `ship_mode`, `campaign_channel` |
| **Numerical Measures** | `sales`, `quantity`, `discount`, `profit`, `delivery_days`, `customer_rating` |
| **Binary/Flag Fields** | `return_flag` |

### Data Assumptions & Quality Notes
* **Data Integrity**: Minor missing values were identified in `customer_rating` and `campaign_channel`. These records are included for total volume calculations but are excluded from average-based metrics.
* **Temporal Data**: `order_date` and `ship_date` were correctly interpreted by Tableau as Date/Time objects.
* **Return Logic**: The `return_flag` field uses `0` to represent a completed sale and `1` to represent a returned item.
* **Geographic Mapping**: State and city names are assumed to be standard; no custom geocoding was required for these locations.


## Calculated Fields Created
To enable deeper analysis, the following calculated fields were developed in Tableau:

1. **Profit Margin**: `SUM([Profit]) / SUM([Sales])` - Used to determine the percentage of revenue that remains as profit.
2. **Cost**: `SUM([Sales]) - SUM([Profit])` - Calculated to understand the total expenses incurred per transaction.
3. **Average Order Value**: `SUM([Sales]) / COUNTD([Order ID])` - Provides the average revenue generated per unique transaction.
4. **Return Rate**: `SUM([return_flag]) / COUNTD([Order ID])` - Measures the proportion of orders that are returned by customers.
5. **Shipping Delay Bucket**: `IF [delivery_days] <= 2 THEN 'On Time' ELSEIF [delivery_days] <= 5 THEN 'Minor Delay' ELSE 'Major Delay' END` - Categorizes delivery performance into three buckets to identify shipping inefficiencies.
