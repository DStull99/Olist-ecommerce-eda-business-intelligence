# Olist Brazilian E-Commerce: Business Intelligence Report

An end-to-end exploratory data analysis of the [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), covering ~100,000 orders placed across multiple Brazilian online marketplaces between 2016 and 2018.

The goal of this project was to extract business-relevant insights across four analytical pillars and synthesize them into a polished report suitable for executive presentation.

---

## Key Findings

- **Order volume grew rapidly through 2017**, peaking at 7,544 orders in November 2017 (Black Friday), before stabilizing at 6,000–7,000 orders/month in 2018. Revenue tracked volume closely, with average order value remaining flat at R$137–163 throughout — confirming growth was driven by volume, not price inflation.

- **Late delivery is the single strongest driver of customer dissatisfaction.** On-time orders averaged 4.29 stars; late orders averaged just 2.57 — a 1.72-point gap on a 5-point scale across nearly 100,000 orders.

- **A severe geographic disparity exists.** Customers in northern states wait up to 29 days for delivery (vs. 9 days in São Paulo) and pay nearly 3× more for freight — directly causing the lowest review scores in the dataset (RR: 3.61 avg).

- **Revenue is highly seller-concentrated.** The top 10% of ~3,100 sellers generate 67.6% of all product revenue, creating meaningful platform concentration risk.

- **Only 3.12% of customers made a repeat purchase**, revealing that growth during 2016–2018 was almost entirely acquisition-driven rather than retention-driven.

---

## Project Structure

```
olist-ecommerce-eda/
├── README.md
├── notebooks/
│   └── Olist_E-Commerce_Dataset_--_EDA.ipynb   # Full analysis notebook
├── report/
│   └── olist_bi_report.docx                    # Polished BI report (12 pages)
└── data/
    └── README.md                                # Link to Kaggle dataset
```

---

## Analysis Structure

The analysis is organized around four business pillars:

### 1. Business Growth
- Monthly order volume and revenue trends (2016–2018)
- Average order value stability
- Top 10 product categories by revenue and market share

### 2. Customer Experience
- Review score distribution across all orders
- Impact of delivery timing on customer satisfaction
- Payment method breakdown and installment behavior
- Repeat purchase rate and customer retention

### 3. Seller & Operational Performance
- Revenue concentration among top sellers
- Seller geographic distribution
- New seller onboarding trends over time

### 4. Customer Geography
- Revenue by customer state
- Delivery time and freight cost by state
- Seller vs. customer geographic mismatch and its operational consequences

---

## Strategic Recommendations

1. **Prioritize delivery reliability** — reducing the 7.9% late delivery rate is the highest-leverage action to improve customer satisfaction
2. **Expand seller presence in the North and Northeast** — to close the geographic gap driving long delivery times and high freight costs
3. **Build a key account program for top sellers** — protecting the ~310 sellers that generate 67.6% of revenue
4. **Invest in customer retention** — moving from 3.12% to even 6% repeat rate would have significant revenue impact
5. **Develop category-specific quality programs** for the three sub-4.0 review score categories (bed_bath_table, computers_accessories, furniture_decor)

---

## Tech Stack

- **Python** — pandas, matplotlib
- **Jupyter Notebook**
- **Dataset** — [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle)

## Requirements

- Python 3.12.3
- pandas 2.2.3
- matplotlib 3.10.6
- jupyter

---

## Dataset

This project uses the Olist Brazilian E-Commerce Public Dataset, available on Kaggle. The dataset is not included in this repository — download it directly from Kaggle and place the CSV files in a `data/` folder before running the notebook.

**Files required:**
- `olist_orders_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_order_payments_dataset.csv`
- `olist_order_reviews_dataset.csv`
- `olist_customers_dataset.csv`
- `olist_sellers_dataset.csv`
- `olist_products_dataset.csv`
- `product_category_name_translation.csv`
