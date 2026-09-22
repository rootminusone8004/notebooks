# Course Datasets (`data_files/`)

This directory houses the structured tabular datasets (both **CSV** and **Excel `.xlsx`** files) used across the Machine Learning curriculum notebooks.

---

## Dataset Catalog

| File Name | Format | Dimensions | Description & Features | Primary Notebook Modules |
|---|---|---|---|---|
| **`telecom_churn.csv`** | CSV | 10 rows $\times$ 6 cols | Customer telecommunication churn dataset (`customer_id`, `churn`, `monthly_charges`, `total_charges`, `contract_type`, `tenure_months`). | `02_pandas` (Notebooks 01, 02) |
| **`housing_market.csv`** | CSV | 50 rows $\times$ 5 cols | Real estate pricing data (`House_ID`, `SquareFeet`, `Bedrooms`, `Location`, `Price`). Used for regression and EDA. | `02_pandas`, `03_matplotlib`, `05_scikit_learn` |
| **`sensor_telemetry.csv`** | CSV | 100 rows $\times$ 5 cols | Continuous numeric IoT sensor measurements (`timestamp_sec`, `temperature_c`, `humidity_pct`, `pressure_kpa`, `vibration_index`). | `01_numpy` (Notebook 01), `02_pandas` |
| **`business_metrics.xlsx`** | Excel (`.xlsx`) | 3 Sheets | Multi-sheet corporate workbook: <br>• **`Customers`**: Churn & billing profiles <br>• **`Subscription_Plans`**: Tier pricing & user limits <br>• **`Regional_Targets`**: Q1/Q2 revenue ARR targets & sales leads. | `02_pandas` (Notebook 01) |
| **`ecommerce_orders.xlsx`** | Excel (`.xlsx`) | 2 Sheets | Multi-sheet retail transactions: <br>• **`Orders`**: Order IDs, customer IDs, spend amounts, and promo tags <br>• **`Promotions`**: Active discount codes and spend thresholds. | `02_pandas` (Notebooks 04, 05) |

---

## How to Load in Notebooks

To ensure code runs reliably whether executed from the module subfolder or the repository root:

```python
import os
import pandas as pd

# Detect data_files directory path
data_dir = "data_files" if os.path.exists("data_files") else "../data_files"

# 1. Read CSV
df_churn = pd.read_csv(os.path.join(data_dir, "telecom_churn.csv"))

# 2. Read specific Excel Sheet
df_plans = pd.read_excel(os.path.join(data_dir, "business_metrics.xlsx"), sheet_name="Subscription_Plans")

# 3. Read All Sheets from an Excel Workbook
all_sheets = pd.read_excel(os.path.join(data_dir, "business_metrics.xlsx"), sheet_name=None)
```
