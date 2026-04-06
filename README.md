# 🛒 Superstore Sales Analysis

## 📌 Project Overview
Analysis of retail sales data to identify business inefficiencies 
and provide actionable recommendations using SQL, Python, and Tableau.

## 🛠 Tools Used
- **SQL (SQLite3)** — data extraction and aggregation
- **Python (Pandas, Seaborn)** — data cleaning, EDA, visualization
- **Tableau** — interactive business dashboard

## 📁 Project Structure
superstore-analysis/
├── data/
│   ├── superstore.csv        ← Raw data
│   └── superstore.db         ← SQLite database
├── sql/
│   ├── exploration.sql       ← Column checks, previews
│   └── business_questions.sql← Business queries
├── notebooks/
│   ├── 01_setup_database.ipynb
│   ├── 02_sql_analysis.ipynb
│   └── 03_visualization.ipynb
├── report/
│   ├── recommendation.tex    ← LaTeX source
│   ├── recommendation.pdf    ← compiled output
│   └── chart*.png             ← charts embedded in the report
└── README.md

## 🔍 Key Findings
1. Central region has the lowest profit margin (7.92%) 
   despite being the 3rd highest in sales
2. Central's average discount (24%) is more than double 
   West's (11%), directly causing margin loss
3. Nearly 30% of Central's orders are discounted above 
   30% — a threshold that typically causes negative profit

## 💼 Business Recommendations

| # | Recommendation | Expected Impact |
|---|---------------|------------------|
| 1 | **Cap discounts at 15% in Central region** — discounts above 20% consistently produce negative profit | Margin improvement from 7.92% → 12%+ |
| 2 | **Eliminate deep discounts on Furniture** — Furnishings (40% avg discount) and Tables (26%) are top loss makers | Recover $7,000+ in lost profit from Furniture alone |
| 3 | **Review Binders pricing strategy** — $56K in sales but losing money due to 51% average discount | Turn $1,044 loss into potential profit |

**Bottom line:** The Central region has strong sales volume but is undermined by aggressive discounting. Capping discounts at 15% could realistically bring Central's margin from 7.92% to above 12%, approaching West's benchmark of 14.94%.

