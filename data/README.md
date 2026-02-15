# Data (Exports Used in This Repository)

This folder contains **two exports** that align with the screenshots in `/assets` and demonstrate how PHAnford organised:

1) a full **product master list**
2) an **inventory stock/valuation** report (quantities + value in Ghana Cedis)

These files are useful for:
- audit and reconciliation
- stock valuation reporting
- procurement planning (what to reorder)
- analytics (top products, pricing, margins, and category breakdown)

---

## Files in this folder

### 1) `PHAnford_Products(Pharm&NonPharam).csv`
A **product catalogue export** containing roughly **3,118 rows** (one row per product).

Typical fields you may see:
- **Name** — product name as entered in Aronium
- **ProductGroup** — e.g. *Pharmaceuticals*, *Non-pharmaceuticals* (some rows may be blank)
- **SKU / Barcode** — identifiers for search and scanning
- **MeasurementUnit** — unit type (tabs, bottle, pack, etc.)
- **Cost / Price** — purchase cost vs sale price
- **Markup** — margin configuration (where applicable)
- **Tax** — tax mapping
- **IsActive** — whether product is active for sale
- **Description** — often contains notes like expiry info (where used)

Why this matters:
- this file represents the “source of truth” for what the pharmacy sells
- it helps ensure consistent naming, pricing, and category organisation

---

### 2) `PHAnford_Stock(Pharm&NonPharam).xlsx`
An **inventory/valuation report** that reflects current stock quantities and value.

Common columns:
- **Name** — product name
- **Product group** — Pharmaceuticals / Non-pharmaceuticals / (none)
- **Qty.** — available quantity (can include **zeros** or **negative values** depending on adjustments/errors)
- **Cost price** — unit cost
- **Cost bef. tax / Cost incl. tax** — total cost valuation for that product line
- **Price** — unit selling price
- **Total before tax / Total** — total selling valuation for that product line

Why this matters:
- gives you “what is on the shelf” and its value (GHS)
- supports procurement and financial reporting
- highlights stock issues like **negative quantity** and **out-of-stock** items

---

## How the data matches the screenshots

The `/assets` stock screenshots show summary totals like:
- product counts (pharmaceuticals vs non-pharmaceuticals)
- totals for cost and selling value
- counts of negative / non-zero / zero items

This Excel export is the “data behind the view on Aronium.”

---

## Quick analysis
If you want to analyse these exports with any programming language, e.g. Python:

```python
import pandas as pd

products = pd.read_csv("data/PHAnford_Products(Pharm&NonPharam).csv")
stock = pd.read_excel("data/PHAnford_Stock(Pharm&NonPharam).xlsx")

# Product group counts
print(products["ProductGroup"].value_counts(dropna=False))

# Stock valuation by group (cost vs selling value)
group_totals = stock.groupby("Product group")[["Cost incl. tax", "Total"]].sum()
print(group_totals.sort_values("Total", ascending=False))
