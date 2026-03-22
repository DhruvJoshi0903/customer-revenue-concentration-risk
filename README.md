# Customer Revenue & Concentration Risk Analysis

## Project Overview

This project analyses transactional retail data to identify revenue concentration risks across customers and geographies. The analysis is structured around three business questions that are directly relevant to risk, strategy, and account management teams:

- Is revenue growth driven by acquiring more customers, or by existing customers spending more?
- How dependent is the business on a small number of high-value accounts?
- Does geographic concentration in one market create systemic business risk?

This is the kind of analysis a Data or Risk Analyst would be asked to produce when a business wants to understand the stability and resilience of its revenue base.

---

## Dataset

**Source:** [Online Retail Dataset — Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset)

**Description:** Transactional sales data from a UK-based online retailer. Each row represents one line item in a customer invoice.

| Column | Description |
|---|---|
| Invoice | Unique invoice number |
| StockCode | Product identifier |
| Description | Product name |
| Quantity | Units sold (negative values = returns/cancellations) |
| InvoiceDate | Date and time of transaction |
| Price | Unit price in GBP (£) |
| Customer ID | Unique customer identifier |
| Country | Customer's country |

---

## Key Findings

### 1. High Customer Concentration Risk 🔴
> **Top 10 customers generate 68.8% of total revenue. The top 5 alone account for 45.3%.**

A business this concentrated is highly vulnerable. Losing a single large account could remove 10–17% of revenue overnight. The analysis identifies which accounts carry this risk and quantifies the exposure.

### 2. Extreme Geographic Dependency 🔴
> **The United Kingdom contributes 87.8% of total revenue.**

Revenue is almost entirely dependent on a single market. Any economic shock, regulatory change, or logistics disruption in the UK directly threatens the majority of the business. EIRE (Ireland) was identified as the most attractive near-term expansion market — it has the highest Average Revenue Per Customer (£734) of any non-UK market.

### 3. Revenue Growth is Volume-Driven, Not Value-Driven 🟡
> **Revenue spikes align with increases in active customer count — ARPC does not grow independently.**

This means the business grows by acquiring new buyers, not by increasing spend from existing ones. Volume-driven growth is more expensive to sustain and signals limited pricing power or low customer loyalty.

### 4. Returns Represent Measurable Revenue Leakage 🟡
> **33 return/cancellation transactions reduce gross revenue by £424.**

Returns were separated from valid sales and quantified. Tracking return rate monthly by product category is recommended to identify quality or fit issues before they escalate.

---

## Project Structure

```
customer-revenue-concentration-risk/
│
├── Customer_Revenue_Concentration_Risk_Analysis.ipynb   # Main analysis notebook
├── README.md                                            # This file
└── data/
    └── online_retail_II.csv                             # Source dataset (download from Kaggle)
```

---

## How to Run This Project

**Prerequisites:** Python 3.8+ with the following libraries installed:
```
pandas
numpy
matplotlib
```

Install them in one command if needed:
```bash
pip install pandas numpy matplotlib
```

**Steps:**
1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset) and place it in a `data/` folder inside the project directory
2. Open `Customer_Revenue_Concentration_Risk_Analysis.ipynb` in Jupyter Notebook or JupyterLab
3. Run all cells from top to bottom (`Kernel → Restart & Run All`)

---

## Notebook Structure

The notebook follows a structured analytical flow:

| Section | What It Covers |
|---|---|
| 1. Setup & Imports | Libraries, global chart styling |
| 2. Data Loading | Dataset overview, column descriptions |
| 3. Data Quality Assessment | Missing values, duplicates, anomalies |
| 4. Data Cleaning & Feature Engineering | Returns separation, Revenue column, date features |
| 5. Returns Analysis | Gross vs. net revenue, cancellation impact |
| 6. Monthly Business Performance | Revenue trends, active customers, ARPC, MoM growth |
| 7. Customer Concentration Risk | Top customer rankings, concentration curve, headline metrics |
| 8. Geographic Concentration Risk | Country revenue breakdown, ARPC by market, expansion opportunities |
| 9. Key Findings & Recommendations | All findings in Problem → Analysis → Finding → Recommendation format |
| 10. Conclusion | Summary and skills demonstrated |

---

## Skills Demonstrated

- **Data Cleaning** — handling nulls, removing duplicates, separating returns from valid sales
- **Feature Engineering** — creating Revenue, ARPC, Month-over-Month growth rate
- **Exploratory Data Analysis** — customer segmentation, geographic breakdown, trend analysis
- **Concentration Risk Analysis** — cumulative revenue curves, customer dependency quantification
- **Business Insight Framing** — every finding is tied to a business risk and a recommendation
- **Data Visualisation** — dual-axis charts, horizontal bar charts, concentration curves using Matplotlib
- **Python & Pandas** — groupby aggregations, merges, sorting, percentage calculations

---

## Tools Used

| Tool | Purpose |
|---|---|
| Python 3 | Core analysis language |
| Pandas | Data manipulation and aggregation |
| NumPy | Numerical operations |
| Matplotlib | Data visualisation |
| Jupyter Notebook | Interactive analysis environment |

---

## About

**Dhruv Joshi**  
Data & Risk Analyst — ANZ (Australia and New Zealand Banking Group), Bangalore  

This project reflects the kind of risk-focused data analysis I work with professionally — specifically the practice of identifying revenue concentration and dependency risks that inform strategic and operational decisions.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/dhruvjoshi09/)
