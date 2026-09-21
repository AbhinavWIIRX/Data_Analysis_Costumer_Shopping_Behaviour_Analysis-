# Customer Shopping Behavior Analysis

An end-to-end data analytics project analyzing **3,900 customer transactions** to uncover spending patterns, customer segments, product preferences, discount behavior, subscription patterns, and revenue trends.

The project combines **Python, Pandas, Microsoft SQL Server, SQL analysis, and Power BI** to transform raw shopping data into business insights.

## Project Overview

The objective of this project is to understand customer shopping behavior and identify patterns that can support:

- Customer segmentation
- Revenue analysis
- Product performance analysis
- Discount strategy
- Subscription analysis
- Shipping behavior analysis
- Age-group revenue analysis
- Customer loyalty analysis

The project covers **3,900 rows and 18 columns**, including demographics, purchase details, shopping behavior, shipping, and discount-related fields. fileciteturn0file0L8-L19

## Key Metrics

| Metric | Value |
|---|---:|
| Total Transactions | 3,900 |
| Average Purchase Amount | $59.76 |
| Average Review Rating | 3.75 |
| Subscribers | 1,053 (27%) |
| Non-Subscribers | 2,847 (73%) |
| Missing Review Ratings | 37 |

## Dataset

The project uses `customer_shopping_behavior.csv`.

### Main Columns

```text
Customer_ID
Age
Gender
Item_Purchased
Category
Purchase_Amount_USD
Location
Size
Color
Season
Review_Rating
Subscription_Status
Shipping_Type
Discount_Applied
Promo_Code_Used
Previous_Purchases
Payment_Method
Frequency_of_Purchases
```

## Data Preparation

The data preparation workflow includes:

1. Loading the CSV using Pandas.
2. Inspecting the dataset using `df.info()` and `df.describe()`.
3. Identifying missing values.
4. Imputing missing `Review_Rating` values using the category median.
5. Standardizing column names to `snake_case`.
6. Creating an `age_group` feature.
7. Creating `purchase_frequency_days`.
8. Removing the redundant `promo_code_used` field from the cleaned dataset.
9. Loading the cleaned data into Microsoft SQL Server.

These preparation steps are documented in the project report. fileciteturn0file0L22-L27

## SQL Server Analysis

The SQL analysis is implemented in **Microsoft SQL Server (T-SQL)**.

The project includes queries for:

1. Revenue by gender
2. High-spending customers who used discounts
3. Top products by average review rating
4. Average purchase amount by shipping type
5. Subscriber vs. non-subscriber spending
6. Products with the highest discount rate
7. Customer segmentation based on previous purchases
8. Top products within each category
9. Repeat buyers by subscription status
10. Revenue contribution by age group

Additional analysis covers payment methods, purchase frequency, promo-code usage, revenue by category, and revenue by season.

### SQL Table

```sql
dbo.customer_shopping_behavior
```

The SQL script is written for Microsoft SQL Server and can be executed using SQL Server Management Studio or the SQL Server extension in VS Code.

## Power BI Dashboard

The project includes a Power BI dashboard for interactive analysis.

### Dashboard KPIs

- Number of Customers: **3.9K**
- Average Purchase Amount: **$59.76**
- Average Review Rating: **3.75**
- Subscription Split: **27% Yes / 73% No** fileciteturn0file0L86-L92

The dashboard contains views for subscription status, revenue and sales by category, revenue and sales by age group, gender, shipping type, and category.

## Key Findings

### Revenue by Gender

The analysis reports:

- Male revenue: **$157,890**
- Female revenue: **$75,191** fileciteturn0file0L29-L38

### Shipping

Average purchase amount:

- Express: **$60.48**
- Standard: **$58.46** fileciteturn0file0L33-L35

### Subscription Behavior

| Subscription Status | Customers | Average Spend |
|---|---:|---:|
| No | 2,847 | $59.87 |
| Yes | 1,053 | $59.49 |

fileciteturn0file0L36-L38

### Product Ratings

The highest-rated products in the analysis are:

1. Gloves — 3.86
2. Sandals — 3.84
3. Boots — 3.82
4. Hat — 3.80
5. Skirt — 3.79

### Discount-Dependent Products

Products with high discount-purchase percentages include:

- Hat — 50.00%
- Sneakers — 49.66%
- Coat — 49.07%
- Sweater — 48.17%
- Pants — 47.37%

These results are reported in the project analysis. fileciteturn0file0L45-L58

### Customer Segmentation

The report identifies:

- Loyal: **3,116 customers**
- Returning: **701 customers**
- New: **83 customers** fileciteturn0file0L60-L70

### Revenue by Age Group

The report shows that the **56+ age group contributes approximately 28% of revenue**. fileciteturn0file0L74-L84

## Business Recommendations

The project report recommends:

### 1. Boost Subscriptions

Promote exclusive benefits and test incentives intended to increase subscriber share and customer lifetime value.

### 2. Strengthen Customer Loyalty

Use loyalty programs and rewards to retain repeat buyers.

### 3. Review Discount Strategy

Evaluate discount-dependent products while considering margin impact.

### 4. Improve Product Positioning

Highlight highly rated products and best-sellers.

### 5. Target High-Revenue Customer Groups

Use age-group and shopping-behavior insights for targeted campaigns.

### 6. Test Recommendations

A/B test subscription incentives and refine discount strategies based on measured margin impact. fileciteturn0file0L93-L106

## Tech Stack

- **Python**
- **Pandas**
- **NumPy**
- **Microsoft SQL Server**
- **T-SQL**
- **Power BI**
- **Jupyter Notebook / VS Code**
- **Git & GitHub**

## Recommended Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── data/
│   └── customer_shopping_behavior.csv
│
├── sql/
│   └── customer_shopping_behavior_MSSQL_exact_columns.sql
│
├── notebooks/
│   └── Customer_Shopping_Behavior_Analysis.ipynb
│
├── powerbi/
│   └── Customer_Behavior_Dashboard.pbix
│
├── reports/
│   └── Customer-Shopping-Behavior-Analysis.pdf
│
└── README.md
```

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Customer-Shopping-Behavior-Analysis.git
cd Customer-Shopping-Behavior-Analysis
```

### 2. Install Python Dependencies

```bash
pip install pandas numpy matplotlib jupyter
```

### 3. Run the Notebook

Open:

```text
notebooks/Customer_Shopping_Behavior_Analysis.ipynb
```

using VS Code or Jupyter Notebook.

### 4. Load the Dataset

Place:

```text
customer_shopping_behavior.csv
```

inside the `data/` directory.

### 5. Run SQL Analysis

Create/import the cleaned table in Microsoft SQL Server and execute:

```text
sql/customer_shopping_behavior_MSSQL_exact_columns.sql
```

The script can be run in **SSMS** or **VS Code with the SQL Server extension**.

### 6. Open Power BI

Open the `.pbix` dashboard in Power BI Desktop and refresh the data source if required.

## Skills Demonstrated

- Data cleaning
- Exploratory Data Analysis (EDA)
- Feature engineering
- Missing-value treatment
- SQL querying
- Aggregation and grouping
- Window functions
- Customer segmentation
- KPI analysis
- Data visualization
- Power BI dashboard development
- Business insight generation

## End-to-End Workflow

```text
Raw CSV
   ↓
Data Cleaning
   ↓
Feature Engineering
   ↓
Microsoft SQL Server
   ↓
SQL Analysis
   ↓
Power BI Dashboard
   ↓
Business Insights
   ↓
Recommendations
```

The project therefore demonstrates an end-to-end analytics workflow combining **Python-based preparation, SQL-based analysis, and Power BI visualization**. fileciteturn0file0L22-L27

## Author

**Abhinav Kaushik**

B.Tech — Computer Science & Engineering

GitHub: `https://github.com/YOUR-USERNAME`

LinkedIn: `https://www.linkedin.com/in/YOUR-LINKEDIN-USERNAME/`

## Disclaimer

This repository is intended for educational and portfolio purposes. Business recommendations are based on the analyzed dataset and should be validated against additional business, financial, and operational data before real-world use.
