# PH Anford Pharmacy – Stock Management System (Spreadsheet-based)

This repository documents a practical **pharmacy stock management system** implemented using a structured spreadsheet workflow.  
It supports stock visibility, simple auditing, and basic analytics for day-to-day pharmacy operations.

The system focuses on:
- consistent product catalogue structure
- stock-in / stock-out tracking
- automatic totals, low-stock alerts, and valuation fields
- pivot tables/dashboards for management insight

> **Commercial sensitivity:** If your workbook contains real pricing, supplier details, or profit margins, upload an anonymised copy (mask sensitive columns).

---

## What this shows (portfolio value)

- Spreadsheet **data modelling** (clean tables, consistent columns, validation)
- **Operational analytics** (pivots, summaries, low-stock reports)
- **Process design** (how staff update stock and how reviews happen)
- Documentation skills (non-technical users can follow the workflow)

---

## Repository layout

- `data/` – workbook(s) and optional sample exports
- `docs/` – usage guide, data dictionary, rules, and safeguards
- `screenshots/` – visuals of key tabs and dashboard/pivots
- `templates/` – reusable blank templates (recommended)
- `reports/` – exported summaries (PDF/CSV), anonymised

---

## Quick verification

1. Open `data/` and review the workbook structure.
2. Read `docs/how-to-use.md` for the daily workflow.
3. Check `screenshots/` for proof of:
   - product master table
   - stock movements (in/out)
   - current stock summary + reorder flags
   - pivot tables and dashboard outputs
4. If included, open `templates/` to see reusable versions.

---

## Recommended workbook design (tabs)

A reliable structure often includes:

- **Products** (master): SKU, Name, Category, Supplier, Unit Cost, Unit Price, Reorder Level
- **Stock Movements**: Date, SKU, Movement Type (IN/OUT/ADJUST), Qty, Reason, Staff
- **Current Stock** (calculated): SKU, On-hand Qty, Stock Value, Reorder Flag
- **Suppliers** (optional): Supplier, Contact, Lead time
- **Dashboard**: KPIs + charts (low-stock count, valuation, fast movers)

---

## Data quality & safety

- use dropdown validation for categories and movement types
- protect formula columns to avoid accidental edits
- add a visible instruction panel (inside the workbook)
- create weekly backups (export a dated copy)

---

## Suggested releases

- `v1.0-workbook-baseline` – initial workbook + documentation
- `v1.1-dashboard-pivots` – pivot tables and dashboard improvements
- `v1.2-validation-hardening` – additional validation + protected ranges

---

## Contact

Samuel Boadi Agyekum  
GitHub: https://github.com/agyekumboadi  
LinkedIn: https://www.linkedin.com/in/samuel-agyekum-388a82150/  
Email: agyekumowuraku@outlook.com

_Last updated: 2026-02-15_
