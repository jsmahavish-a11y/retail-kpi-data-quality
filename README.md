# Retail Orders: KPI Dictionary & Data Quality Contract

Decision owner: Head of Sales & Operations (ed-tech business)

This project defines the key business metrics for a retail orders dataset and checks whether the data is trustworthy enough to report on.

## Files

- kpi_dictionary.xlsx: 10 KPIs with formula, grain, filters, owner and refresh cadence
- retail_data_quality_profile (2).ipynb: executable checks for completeness, uniqueness, validity, consistency and freshness, plus KPIs on the cleaned data
- data_quality_contract.md: failure thresholds and escalation actions for each check

## Key findings

- The raw file has 12 rows (11 unique orders) and fails every dimension checked.
- Issues found: missing date, city and discount; one duplicate order; invalid dates, quantities and discount; inconsistent text case; data last updated on 2026-01-18.
- KPIs are calculated only from rows that pass every rule.

## How to run

1. Open the notebook in Google Colab or Kaggle.
2. Upload retail-orders-raw.csv.
3. Run all cells.

## Assumptions

Owner names are role names, thresholds are proposed for this exercise, and missing discounts are not treated as zero without justification.
