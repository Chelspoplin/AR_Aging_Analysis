# AR_Aging_Analysis
# AR Aging Query Overview

This query builds an Accounts Receivable (AR) aging dataset designed to support collections and executive reporting.

It combines invoice data, payment terms, and customer notes into a single, reporting-ready output.

## What This Query Does

- Pulls **open invoices only** (balance_due > 0)
- Filters to **active customer sites**
- Normalizes invoice dates for integration/special-case scenarios
- Calculates a **system-driven due date** based on payment terms
- Returns **two aging methods**:
  - Aging based on `reference_date` (system aging)
  - Aging based on calculated `system_due_date` (terms-based aging)
- Attaches the **most recent customer-level note**
- Attaches the **most recent invoice-specific note**

## Why It Matters

This structure allows:

- Collections teams to immediately see the latest customer activity
- Finance to evaluate delinquency both by system aging and by contractual due date
- BI dashboards to toggle between aging methods
- Leadership to analyze true overdue exposure

The result is a clean, enriched AR dataset that supports operational action and executive-level reporting.
