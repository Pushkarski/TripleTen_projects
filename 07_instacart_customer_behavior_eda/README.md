# Instacart Customer Behavior - EDA (Beginner Project)

Beginner-level exploratory data analysis (EDA) project completed as part of the TripleTen Data Analysis Bootcamp.  
The goal is to clean a multi-table Instacart dataset and explore basic customer shopping behavior.

> This is an **introductory training project** focused on core pandas EDA, not advanced analytics or modeling.

---

## 🔍 Project Overview

**Business context:** Instacart is a grocery delivery platform.  
**Objective:** Understand how customers shop:

- When they place orders (by hour and day of week)
- How often they reorder
- How many items they typically buy
- Which products are most popular and most frequently reordered

---

## 📊 Dataset

Multiple related tables (simplified Instacart dataset):

- `instacart_orders.csv` — orders (`order_id`, `user_id`, `order_dow`, `order_hour_of_day`, `days_since_prior_order`)
- `products.csv` — product catalog (`product_id`, `product_name`, `aisle_id`, `department_id`)
- `order_products.csv` — products within each order (`order_id`, `product_id`, `add_to_cart_order`, `reordered`)
- `aisles.csv` — aisle metadata
- `departments.csv` — department metadata

---

## 🛠️ Tech Stack

- **Python**
- **pandas** — data cleaning & aggregation
- **NumPy**
- **matplotlib** — basic visualizations
- **Jupyter Notebook**

---

## ✅ What I Did

**Data preparation**

- Loaded 5 related CSV files with non-standard separators
- Checked structure, data types, missing values, and duplicates
- Removed exact duplicate orders
- Handled missing values:
  - Filled missing `product_name` as `"Unknown"` for items in a special “missing” aisle/department
  - Kept expected missing values (e.g., `days_since_prior_order` for first orders)
  - Converted `add_to_cart_order` to nullable integer (`Int64`) while preserving `NaN`

**Exploratory analysis**

- Verified value ranges:
  - `order_hour_of_day ∈ [0, 23]`
  - `order_dow ∈ [0, 6]`
- Analyzed:
  - Orders by hour of day and day of week
  - Time between orders (`days_since_prior_order`)
  - Distribution of number of orders per customer
  - Distribution of items per order
- Identified:
  - Top 20 most frequently ordered products
  - Top 20 most frequently reordered products
  - Reorder rate per product (share of orders that are reorders)

---

## 📌 Key Findings (High Level)

- Customers most often place orders **in late morning / early afternoon**, with a peak around **10–11 AM**.
- Order volume is highest on a couple of **“weekend-like” days** and slightly lower on others.
- Typical basket size is **around 5–7 items**; very large orders are rare.
- A small group of products (mostly **fresh & organic produce**, e.g. bananas, berries, spinach) dominate both:
  - total orders and  
  - reorders  
- Many products are purchased only once, while a smaller subset has **very high reorder rates**, indicating core staple items.

---

## 📁 Repository Structure

```text
07_instacart_customer_behavior_eda/
├── README.md                # Project summary (this file)
└── instacart_eda.ipynb      # Full analysis notebook
