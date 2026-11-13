# ecommerce-product-analytics

An end-to-end business and product analytics project that analyses e-commerce customer journeys and transaction data to understand conversion behaviour, identify funnel drop-offs, measure customer retention, and segment customers based on purchasing value.

Built using **SQL, Python, Pandas, NumPy, Matplotlib and SQLite**, this project transforms raw transactional and behavioural data into actionable business insights through analytical queries, visualisations and an interactive dashboard.

## Project Overview

Understanding customer behaviour is essential for improving e-commerce performance. However, sales figures alone do not explain why customers abandon purchases, which acquisition channels generate valuable customers, or what drives repeat purchases.

This project addresses these questions through five interconnected analytical workflows:

1. Conversion Funnel Analysis
2. Channel & Device Performance Analysis
3. Cohort-Based Customer Retention
4. RFM Customer Segmentation
5. Interactive Business Intelligence Dashboard

The objective is to translate customer and transaction data into measurable insights and actionable recommendations for improving conversion, retention and revenue performance.

## Business Questions

- At which stage of the purchasing journey do customers drop off?
- Which acquisition channels generate the highest conversion rates?
- Does device type influence purchasing behaviour?
- How effectively does the business retain existing customers?
- Which customer segments contribute most to overall revenue?
- Where should the business prioritise conversion and retention improvements?

## Technology Stack

| Category | Tools |
|---|---|
| Programming | Python |
| Data Analysis | Pandas, NumPy |
| Database | SQLite |
| Query Language | SQL |
| Visualisation | Matplotlib |
| Dashboard | Interactive HTML |
| Business Intelligence | Power BI (optional) |

## Project Structure

```text
ecommerce-funnel-retention/
│
├── data/
│   ├── users.csv
│   ├── events.csv
│   └── orders.csv
│
├── sql/
│   └── analysis.sql
│
├── src/
│   ├── generate_data.py
│   ├── run_analysis.py
│   ├── build_interactive_dashboard.py
│   └── prepare_powerbi.py
│
├── charts/
│
├── powerbi/
│   ├── processed_tables/
│   ├── dax_measures.txt
│   └── build_guide.md
│
├── interactive_dashboard.html
├── requirements.txt
└── README.md
```

## Analytical Methodology

### 1. Conversion Funnel Analysis

**Objective:** Identify friction points in the customer purchasing journey.

The analysis tracks distinct users across four stages:

`Product View → Add to Cart → Begin Checkout → Purchase`

Key metrics:
- Unique users at each funnel stage.
- Step-wise conversion rates.
- Customer drop-off rates.
- Identification of the weakest conversion stage.

**Key finding:** Approximately 41% of product viewers progressed to adding an item to their cart, highlighting product discovery and product-page engagement as potential areas for improvement.

**Business recommendation:** Prioritise product-page optimisation and experiment with product imagery, pricing presentation, product information and calls to action.

### 2. Channel & Device Performance Analysis

**Objective:** Evaluate acquisition channel effectiveness and identify device-level conversion differences.

The analysis compares purchasing behaviour across acquisition channels and devices.

Key metrics:
- Customer conversion rate by channel.
- Revenue contribution by acquisition source.
- Desktop versus mobile conversion.
- Customer acquisition performance.

**Key findings:**
- Email conversion: 23.7%.
- Paid Search conversion: 18.6%.
- Social conversion: 5.9%.
- Desktop conversion: 25.8%.
- Mobile conversion: 9.8%.

**Business recommendations:**
- Investigate the lower conversion performance of social traffic.
- Audit mobile navigation and checkout usability.
- Evaluate acquisition channel performance alongside customer value and acquisition costs before reallocating marketing budgets.

### 3. Cohort-Based Customer Retention Analysis

**Objective:** Understand repeat-purchase behaviour and identify customer retention trends.

Customers are grouped into monthly cohorts based on their first purchase date.

The analysis tracks:
- Monthly customer cohorts.
- Repeat purchase activity.
- Month-on-month retention.
- Customer retention trends.

A cohort retention heatmap visualises the percentage of customers who return to purchase in subsequent months.

**Business recommendation:** Identify cohorts with declining retention and develop targeted engagement, loyalty and repeat-purchase initiatives.

### 4. RFM Customer Segmentation

**Objective:** Identify valuable customer segments and understand revenue concentration.

RFM analysis evaluates customers across three dimensions:

- **Recency:** How recently a customer made a purchase.
- **Frequency:** How often a customer purchases.
- **Monetary:** How much a customer spends.

Customers receive quintile-based scores using SQL window functions and are classified into segments such as:

- Champions
- Loyal Customers
- Potential Loyalists
- At Risk
- Lost Customers

**Key finding:** The analysis identifies a concentration of approximately 83% of revenue among selected high-value and at-risk customer segments.

**Business recommendations:**
- Develop loyalty initiatives for Champions.
- Introduce targeted win-back campaigns for At-Risk customers.
- Create personalised engagement strategies for Lost customers.
- Prioritise retention investments based on customer value.

## Interactive Dashboard

The project includes a self-contained HTML dashboard that allows users to explore the analytical results.

Dashboard capabilities:

- Filter results by acquisition channel and device.
- View conversion funnel metrics.
- Switch between customer counts and conversion percentages.
- Explore customer retention through cohort analysis.
- Compare RFM segments by revenue and customer count.
- Interactively examine customer and business performance.

The project also includes Power BI-ready analytical tables, DAX measures and a dashboard implementation guide.

## SQL Concepts Demonstrated

- Aggregations and conditional calculations.
- `COUNT(DISTINCT ...)` for unique customer analysis.
- `LEFT JOIN` for combining customer and transaction data.
- Common Table Expressions (CTEs).
- Window functions using `NTILE(5)`.
- Customer segmentation using `CASE WHEN`.
- Date-based cohort calculations.
- Funnel and retention analysis.

## Key Business Insights

| Observation | Recommended Action |
|---|---|
| Low product-view-to-cart conversion | Optimise product pages and test alternative product experiences |
| Lower mobile conversion | Investigate mobile navigation and checkout friction |
| Differences in channel conversion | Evaluate acquisition efficiency and customer value |
| Declining cohort retention | Develop targeted repeat-purchase strategies |
| Revenue concentration among selected segments | Prioritise high-value customer retention and win-back initiatives |

## How to Run the Project

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd ecommerce-funnel-retention
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Generate the dataset

```bash
python src/generate_data.py
```

### 4. Run the analysis

```bash
python src/run_analysis.py
```

### 5. Generate the interactive dashboard

```bash
python src/build_interactive_dashboard.py
```

Open `interactive_dashboard.html` in your browser to explore the results.

## Dataset & Limitations

This project uses a **synthetically generated e-commerce dataset** consisting of customer, event and transaction records.

The dataset is designed to simulate customer purchasing journeys, conversion behaviour and repeat-purchase patterns.

The analytical methods can also be adapted to publicly available datasets such as:

- [Brazilian E-Commerce Public Dataset – Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- [Google Analytics 4 Sample Dataset](https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset)

**Important:** The numerical findings presented in this project are based on the generated dataset and should not be interpreted as actual industry benchmarks or real company performance.

## Skills Demonstrated

- Business Analytics
- Product Analytics
- Customer Behaviour Analysis
- Conversion Funnel Analysis
- Customer Retention & Cohort Analysis
- RFM Segmentation
- SQL Query Development
- Python-Based Data Analysis
- Data Visualisation
- Business Intelligence
- Data-Driven Decision Making
- Business Recommendation Development

## Project Objective

To demonstrate how customer behaviour and transactional data can be transformed into actionable business intelligence, supporting better decisions around product experience, customer acquisition, conversion optimisation and customer retention.
