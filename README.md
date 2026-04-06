# 💳 Credit Card Data - Exploratory Data Analysis (EDA)

A end-to-end EDA project on credit card transaction data for PSPD Bank, covering data cleaning, aggregation, visualization, and user-defined functions in Python.

---

## 📁 Project Structure

```
├── Credit Card analysis.ipynb       # Main analysis notebook
├── Credit Card Data.xlsx            # Raw data (Customer, Spend, Repayment sheets)
├── Customer Acquisition.csv         # Customer details
├── spend.csv                        # Transaction data
├── Repayment.csv                    # Repayment data
└── README.md
```

---

## 📊 Dataset Description

| Table | Description |
|---|---|
| **Customer Acquisition** | Customer details at time of card issuing (Age, City, Product, Limit, Segment) |
| **Spend** | Credit card transaction data per customer |
| **Repayment** | Credit card payment data per customer |

---

## 🧹 Data Cleaning

- Replaced age values below 18 with the mean age
- Replaced spend amounts exceeding the per-transaction limit with 50% of that limit
- Capped repayment amounts at the customer's limit

---

## 📝 Analysis Summary

### Descriptive Stats
- Total distinct customers
- Total distinct spend categories
- Average monthly spend per customer
- Average monthly repayment per customer
- Monthly bank profit at 2.9% interest rate (interest earned only on positive monthly profits)

### Top Insights
- Top 5 product types by spend
- City with maximum spend
- Age group with highest spending
- Top 10 customers by repayment amount

---

## 📈 Visualizations

- **City-wise yearly spend by product** — Grouped bar charts (one per year)
- **Monthly city-wise spend comparison** — Multi-line chart
- **Yearly spend on Air Tickets** — Bar chart
- **Monthly spend by product** — Line chart with seasonality analysis

---

## ⚙️ User Defined Function

```python
func1(product, time_period)
```

Finds **top 10 customers per city** based on repayment amount, filtered by:
- `product` → `"Gold"`, `"Silver"`, or `"Platimum"`
- `time_period` → year (e.g. `2004`) or month number (e.g. `6` for June)

**Example usage:**
```python
func1("Gold", 2004)   # Top 10 per city for Gold customers in 2004
func1("Silver", 6)    # Top 10 per city for Silver customers in June
```

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| Python | Core analysis |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualizations |
| Jupyter Notebook | Development environment |
