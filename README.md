# 📦 Warehouse Performance Analysis — E-Commerce Fulfillment Center (2025)

---

## 1. Project Overview

This project analyzes the outbound operational performance of an **e-commerce fulfillment center (FC)** throughout the full year of 2025.

This project was built to answer key operational questions:

- How efficient is the fulfillment process across 12 months?
- Which days, hours, and shifts generate the highest order volume?
- Which sales channels and sellers drive the most business?
- Where are the operational bottlenecks hiding in the data?

The goal is to transform raw WMS export data into **actionable insights** using Python — demonstrating both technical skills and supply chain domain knowledge.

---

## 2. Data Description

| Attribute | Details |
|---|---|
| **Source** | WMS (Warehouse Management System) — Outbound export |
| **Coverage** | January 2025 – December 2025 |
| **Volume** | ~571,000 outbound orders |
| **Format** | CSV files (semicolon-separated), 1 file per month |

---

## 3. Tools & Libraries

- **Language:** Python

- **Libraries:** Pandas, Matplotlib, Seaborn

- **Environment:** Jupyter Notebook

---

## 4. Project Contents

The analysis is structured into 4 main sections:

### Section 1 — Load Data
- Read and merge 12 monthly CSV files into a single DataFrame

### Section 2 — Transform Data
- Drop irrelevant columns
- Rename and standardize column names
- Cast data types (datetime, category, numeric, string)
- Create derived columns (month, week_day, shift, hour)

### Section 3 — Clean Data
- Remove hidden tab characters (`\t`) from ID fields
- Standardize categorical values across 4 columns:
  - `delivery_method` → 10 carrier names → 9 standardized groups
  - `outbound_status` → multiple variants → 3 clean statuses
  - `sale_channel` → raw platform names → 9 clean channels
  - `final_status` → raw WMS codes → 3 clean statuses (Completed / Cancelled / Return)

### Section 4 — Analyze Data

| # | Analysis | Chart Type |
|---|---|---|
| 4.1 | Performance Overview (KPIs) | Text summary |
| 4.2 | Total Orders & Fulfill Rate by Month | Bar + Line chart |
| 4.3 | Orders by Weekday | Bar chart |
| 4.4 | Orders by Work Shift | Horizontal bar chart |
| 4.5 | Orders by Month & Weekday | Heatmap |
| 4.5 | Orders by Weekday & Hour | Heatmap |
| 4.6 | Orders by Sale Channel | Horizontal bar chart |
| 4.7 | Top 20 Sellers by Orders | Horizontal bar chart |

---

## 5. Key Insights

### 📈 Fulfillment Performance
- **Fulfill Rate: ~88%** across 571,000+ orders
- **Cancel Rate: ~11%** — concentrated in specific channels
- **Return Rate: ~0.2%** — low but consistent throughout the year
- February had the lowest Fulfill Rate (~64%) — indicating early-year operational challenges

### 📅 Time Patterns
- **Peak month: November** (116,000+ orders) — driven by 11.11 campaign
- **Lowest month: January** (5,600 orders) — post-Tet slowdown
- **Peak weekday: Friday** — highest order volume across all months
- **Peak hour: 21:00** — customers shop after dinner
- **Q4 (Oct–Dec)** dominates order volume — requires additional staffing

### 🛒 Channel Analysis
- **Shopee (43.2%) + TikTok Shop (41.6%) = 84.8%** of total orders — Big 2 dominate
- Kiot (8.7%) is the 3rd largest channel — significant offline/POS volume
- Remaining 5 channels collectively account for only ~6%

### 🏪 Seller Analysis
- **Top 6 sellers out of 20** account for **80% of total orders**
- VIFON alone contributes ~17% of total volume
- Clear concentration risk — heavy dependency on top 2 sellers

---

## 6. Summary

This project demonstrates an end-to-end data analysis workflow applied to a real e-commerce fulfillment center dataset:

> **Raw WMS data → Clean & Structured → Analyzed → Visualized → Insights**

From a business perspective, the analysis reveals that the FC operates with a strong but improvable fulfillment rate, faces significant demand concentration in Q4 and on Fridays/evenings, and relies heavily on THREE sellers (VIFON, SKIN UNIVERSE and INDOMIE).

These findings provide a data-driven foundation for **workforce planning, carrier optimization, and seller relationship management** — directly applicable to Planning & Analytics roles in supply chain and e-commerce operations.

---

## 📁 File Structure

```
warehouse-performance/
├── Warehouse_Performance_Analysis.ipynb   # Script
├── OB_Data_2025_S.csv                     # Dataset (not included in repo)
└── README.md                 
```

---

*Built with Python | Data from WMS | Period: Jan–Dec 2025*
