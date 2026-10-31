# Retail Orders: KPI Dictionary & Data Quality Contract

**Decision owner:** Head of Sales & Operations (ed-tech business)

Defines the key business metrics for a retail orders dataset and checks whether the data is trustworthy enough to report on.

## Files

| File | What it contains |
|---|---|
| `kpi_dictionary.xlsx` | 10 KPIs with formula, grain, filters, owner and refresh cadence |
| `retail_data_quality_profile.ipynb` | Executable checks for completeness, uniqueness, validity, consistency and freshness, plus KPIs on the cleaned data |
| `data_quality_contract.md` | Failure thresholds and escalation actions for each check |

## Key findings

- The raw file has 12 rows (11 unique orders) and fails every dimension checked.
- Issues found: missing date, city and discount; one duplicate order; invalid dates, quantities and discount; inconsistent text case; data last updated 2026-01-18.
- KPIs are calculated only from rows that pass every rule.

## How to run

1. Open `retail_data_quality_profile.ipynb` in Google Colab or Kaggle.
2. Upload `retail-orders-raw.csv` to the notebook.
3. Run all cells.

## Assumptions

Owner names are role names, thresholds are proposed for this exercise, and missing discounts are not treated as zero without justification.
