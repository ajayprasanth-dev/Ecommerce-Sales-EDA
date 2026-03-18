# Ecommerce Sales & Profit Analysis — Python EDA Project

##  Project Overview

This project performs a complete **Exploratory Data Analysis (EDA)**
on an Ecommerce Sales Dataset covering the period of 2024-2025.
The goal is to analyze sales performance, profit trends, customer
behavior and regional patterns to derive meaningful business insights.

---

##  Dataset Information

- **Dataset Name:** Ecommerce Sales Data 2024-2025
- **Source:** Downloaded from Kaggle
- **Total Records:** 5000 rows
- **Total Features:** 14 columns
- **Time Period:** 2024 - 2025

###  Dataset Columns

| Column | Description |
|---|---|
| Order ID | Unique identifier for each order |
| Order Date | Date when order was placed |
| Customer Name | Name of the customer |
| Region | Geographic region of order |
| City | City of the order |
| Category | Product category |
| Sub-Category | Product sub-category |
| Product Name | Name of the product |
| Quantity | Number of items ordered |
| Unit Price | Price per item |
| Discount | Discount applied (%) |
| Sales | Total sales amount |
| Profit | Profit earned |
| Payment Mode | Mode of payment used |

---

##  Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation & analysis |
| NumPy | Numerical operations |
| Matplotlib | Base plotting library |
| Seaborn | Statistical data visualization |
| Jupyter Notebook | Development environment |

---

##  Project Structure
```
Ecommerce-Sales-EDA/
│
├── 📁 Project_Files/
│   ├── Ecommerce_EDA.ipynb
│   └── Ecommerce_Sales_Data_2024_2025.csv
│
├── 📁 Images/
│   └── (All chart screenshots)
│
├── 📁 Videos/
│   └── (Project walkthrough video)
│
├── 📁 Insights/
│   └── key_insights.md
│
└── 📄 README.md
```

---

##  EDA Process & Steps Followed

###  Step 1 — Environment Setup
- Imported all necessary libraries
- Pandas, NumPy, Matplotlib, Seaborn
- Set plot styling and display settings

###  Step 2 — Load Dataset
- Loaded CSV file using pd.read_csv()
- Verified data loaded correctly using df.head()

###  Step 3 — Data Overview
- Checked dataset shape → 5000 rows × 14 columns
- Reviewed column names and data types using df.info()
- Generated statistical summary using df.describe()

###  Step 4 — Data Cleaning
- Checked missing values → df.isnull().sum()
  → Result: No missing values found 
- Checked duplicate rows → df.duplicated().sum()
  → Result: No duplicates found 
- Fixed Order Date column data type
  → Converted from object to datetime64 format

###  Step 5 — Univariate Analysis
Analyzed each column individually:
- Category Distribution → Countplot
- Region Distribution → Countplot
- Payment Mode Distribution → Countplot
- Sales Distribution → Histogram
- Quantity Distribution → Histogram

###  Step 6 — Bivariate Analysis
Analyzed relationships between two columns:
- Category vs Sales → Barplot
- Region vs Profit → Barplot
- Category vs Profit → Barplot
- Discount vs Sales → Scatterplot

###  Step 7 — Correlation & Heatmap
- Generated correlation matrix using df.corr()
- Visualized using sns.heatmap()
- Identified strong and weak relationships between columns

###  Step 8 — Feature Engineering
Created 3 new columns from existing data:
- Revenue_per_Item = Unit Price × Quantity
- Profit_Margin = (Profit / Sales) × 100
- Order_Month = Extracted month from Order Date

###  Step 9 — Insights & Conclusion
- Documented top 8 key insights
- Provided 7 business recommendations
- Written final conclusion

---

##  Key Insights Found

1. **Sales & Profit are strongly related (0.85)**
   → When sales increase profit increases proportionally

2. **Unit Price drives both Sales & Profit**
   → Unit Price vs Sales correlation = 0.72
   → Unit Price vs Profit correlation = 0.61

3. **Discount has NO significant impact on Sales**
   → Discount vs Sales correlation = only -0.10
   → Discounts are not boosting sales performance

4. **North region is the best performing region**
   → Highest orders → ~1275 orders
   → Highest average profit → ~16,500

5. **Electronics is the most profitable category**
   → Average profit → ~17,000
   → Outperforms Kitchen by ~2,100 in profit

6. **Most customers make small value purchases**
   → Sales data is right skewed
   → Majority of orders fall between 0 - 50,000

7. **All payment modes equally preferred**
   → Each payment mode has ~1000 orders
   → No single payment method dominates

8. **Quantity is uniformly distributed**
   → Each quantity level (1-5) has ~1000 orders
   → No bulk ordering pattern observed

---

##  Business Recommendations

1. **Re-evaluate Discount Strategy**
   → Discounts show negative correlation with sales
   → Reducing discounts can protect profit margins

2. **Focus on Electronics & Home Decor**
   → Highest profit generating categories
   → Increase inventory & marketing for these

3. **Expand in North Region**
   → Best performing region in orders & profit
   → Invest more in North region operations

4. **Introduce Premium High Price Products**
   → Unit price strongly drives sales & profit
   → Premium products can boost revenue significantly

5. **Improve Kitchen Category Performance**
   → Lowest profit category (~14,900)
   → Review pricing strategy for Kitchen products

6. **Target South Region for Growth**
   → Lowest orders & profit among all regions
   → Run targeted marketing campaigns in South

7. **Maintain All 5 Payment Modes**
   → All payment modes equally used
   → Removing any option may impact orders negatively

---

##  Final Conclusion

This Exploratory Data Analysis was performed on 5000 ecommerce
orders from 2024-2025 covering 10 product categories across
4 regions with 5 payment modes.

The most important finding is that Unit Price has the strongest
impact on both Sales (0.72) and Profit (0.61), while Discount
strategy shows minimal impact (-0.10) on driving sales.
North region and Electronics category consistently outperform
all others in both orders and profit generation.

The dataset shows a balanced distribution across regions,
payment modes and quantities suggesting a well diversified
customer base. However the right skewed sales distribution
indicates majority of revenue comes from small value orders
which presents a strong opportunity to introduce and promote
higher value premium products.

Overall this project successfully uncovered key business
patterns and provided actionable recommendations that can
help improve sales strategy, regional focus and category
performance for the ecommerce business.

---
