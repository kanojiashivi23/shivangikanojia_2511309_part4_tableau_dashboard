
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
