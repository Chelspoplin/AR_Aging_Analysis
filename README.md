# AR_Aging_Analysis

# AR Aging Dashboard – Tableau Overview

This Tableau dashboard provides a comprehensive view of Accounts Receivable performance, designed to support Collections, Finance, and Leadership teams.

The report combines aging analysis, payment term performance, customer risk exposure, and trend monitoring into a single interactive view.

---

## Dashboard Highlights

### 🔹 Executive KPIs
The top section displays high-level AR metrics:
- **Total AR**
- **% Payment Collected**
- **% Over 30 Days**

This provides immediate visibility into overall receivable health and delinquency exposure.

---

### 🔹 Aging by Branch
A dynamic aging matrix shows balances segmented by:
- 1–60 Days
- 61–90 Days
- 91–120 Days
- 121–180 Days
- 181–210 Days
- Over 210 Days

Users can switch the aging basis using the **“Age By” parameter**, allowing comparison between:
- Invoice Due Date
- Alternate aging logic (system/reference date)

This enables more accurate delinquency evaluation based on business context.

---

### 🔹 % Collected by Payment Terms
A bar chart visualizes collection performance by payment term.

This helps identify:
- Which terms perform well
- Which terms correlate with higher delinquency
- Whether extended terms are impacting cash flow

The chart supports click-to-filter functionality to dynamically update the rest of the dashboard.

---

### 🔹 Amount & Payment by Month
A dual-axis trend shows:
- Monthly invoice amounts
- Monthly payment activity

This allows users to assess:
- Billing vs collection velocity
- Seasonal AR growth
- Collection lag trends

---

### 🔹 Top Customers Overdue
A ranked table displays:
- Customer ID
- Count of open invoices
- Net Due balance

This section supports immediate collector prioritization and risk identification.

---

## Interactive Features

- **Age By parameter** to toggle aging methodology
- Clickable charts to filter by branch or payment term
- Invoice date filtering (e.g., previous year)
- Invoice type filtering

These features allow users to move from high-level AR health to actionable customer-level detail quickly.

---

## Purpose

This dashboard was designed to:

- Improve AR visibility across business units
- Support faster collector action
- Identify delinquency drivers by payment term
- Provide leadership with a clear, executive-level AR snapshot
- Enable flexible aging analysis based on operational needs

The result is an interactive AR monitoring tool that connects invoice-level detail to strategic financial insight.

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
