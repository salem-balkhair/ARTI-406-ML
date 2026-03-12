# Assignment 2: Data Quality Assessment & Preprocessing

**Course:** ARTI406 - Machine Learning  
**Dataset:** Global Superstore Sales  
**Source:** https://www.kaggle.com/datasets/fatihilhan/global-superstore-dataset  
**Size:** ~51,000 rows × 24 columns

---

## Dataset Description

The Global Superstore dataset contains retail sales transactions from a global superstore
spanning multiple countries, product categories, and customer segments.

| Column | Type | Description |
|--------|------|-------------|
| Order ID | String | Unique order identifier |
| Order Date | Date | Date the order was placed |
| Ship Date | Date | Date the order was shipped |
| Ship Mode | Categorical | Shipping method |
| Customer ID | String | Unique customer identifier |
| Customer Name | String | Customer full name |
| Segment | Categorical | Consumer / Corporate / Home Office |
| Country | Categorical | Country of order |
| City | Categorical | City of order |
| State | Categorical | State of order |
| Postal Code | Mixed | Postal code (can be missing for some countries) |
| Region | Categorical | Geographic region |
| Product ID | String | Unique product identifier |
| Category | Categorical | Furniture / Office Supplies / Technology |
| Sub-Category | Categorical | Product sub-category |
| Product Name | String | Product name |
| Sales | Numeric | Revenue from order |
| Quantity | Numeric | Units ordered |
| Discount | Numeric | Discount applied (0.0 - 1.0) |
| Profit | Numeric | Profit from order (can be negative) |

---

## Data Quality Issues Found

1. **Data Type Issues** - `Order Date`, `Ship Date` as strings; `Postal Code` as float
2. **Missing Values** - `Postal Code` has missing values for international orders
3. **Duplicate Rows** - Some duplicate order records
4. **Outliers** - High-value corporate orders in `Sales` and `Profit`

---

## Tasks Performed

| Task | Method |
|------|--------|
| Task 1: Quality Assessment | dtype check, isnull, duplicated, boxplots |
| Task 2: Missing Value Handling | Median (numeric) + Mode (categorical) |
| Task 3: Outlier Detection & Handling | IQR + Capping (5th-95th percentile) |
| Task 4: Normalization | Min-Max Scaling + Z-Score Standardization |
| Task 5: Dimensionality Reduction | PCA + explained variance analysis |

---

## Requirements

```bash
pip install kagglehub pandas numpy matplotlib seaborn scikit-learn jupyter
```

## Usage

```bash
jupyter notebook Assignment2_GlobalSuperstore.ipynb
```

> **Note:** The notebook downloads the dataset automatically via `kagglehub`.  
> You need a Kaggle account and API token configured at `~/.kaggle/kaggle.json`.

## Files

```
.
|-- Assignment2_GlobalSuperstore.ipynb   # Main notebook (all 5 tasks)
|-- README.md                            # This file
```
