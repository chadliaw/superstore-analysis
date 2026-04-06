# Superstore Sales Analysis

## Summary
Statistical analysis across 45 US states confirms that aggressive discounting
is the primary driver of Central region's profit underperformance
(7.92% vs West's 14.94%, r = −0.905, p < 0.0001).

Further investigation reveals two distinct problems requiring different solutions:
a Central-specific discount policy failure, and a company-wide structural
pricing issue affecting all regions.

## Key Findings

1. **Central has the lowest profit margin** — 7.92% vs West's 14.94%,
   despite being 3rd highest in sales volume ($501K)
2. **Central over-discounts** — 24% average vs West's 11%;
   27.7% of Central's orders exceed the 20% breakeven threshold
3. **7 sub-categories lose money in Central** — combined loss of $15,294
4. **Discounting is statistically validated** — Pearson r = −0.905 (p < 0.0001, n = 45 states);
   consistent across Furniture (r = −0.757), Office Supplies (r = −0.919),
   and Technology (r = −0.669) independently
5. **Two root causes identified:**
   - Group A (Central-specific): Appliances, Furnishings, Binders —
     other regions sell these profitably at <10% discount
   - Group B (Company-wide): Tables, Machines, Bookcases —
     all regions discount at similar levels, pointing to a cost structure issue

## Recommendations

**For Central Regional Management**
| # | Recommendation | Expected Impact |
|---|----------------|-----------------|
| 1 | Cap discount authorisation at 20% for Appliances and Furnishings | Eliminate $6,545 combined loss |
| 2 | Align Binders discount with company average (50.9% → ~34%) | Recover portion of $1,044 loss |
| 3 | Pilot discount cap for one quarter and track margin outcomes | Empirically validate causal effect |

**For Company Leadership**
| # | Recommendation | Expected Impact |
|---|----------------|-----------------|
| 4 | Review cost structure and list pricing for Tables, Machines, Bookcases | Address $9,045 structural loss across all regions |
| 5 | Evaluate whether current discount programme generates sufficient volume uplift to justify losses | Evidence-based repricing decision |

## Tools
SQL (SQLite3) · Python (Pandas, Matplotlib, Seaborn, SciPy) · LaTeX

## Project Structure
```
superstore-analysis/
├── data/
│   ├── superstore.csv
│   └── superstore.db
├── notebooks/
│   ├── 01_setup_database.ipynb
│   ├── 02_sql_analysis.ipynb
│   └── 03_visualization.ipynb
├── report/
│   ├── recommendation.tex
│   ├── recommendation.pdf
│   └── chart*.png
├── requirements.txt
└── README.md
```

## Setup
```bash
pip install -r requirements.txt
```
Run notebooks in order: 01 → 02 → 03
