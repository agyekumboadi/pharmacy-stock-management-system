# Pharmacy Stock Management System (Aronium POS) 🇬🇭

A practical, **pharmacy retail + inventory + reporting** setup built on **Aronium POS**, with real screenshots and sample exports that show how the system was configured to:

- manage **3,118 products** across **Pharmaceuticals** and **Non-pharmaceuticals**
- track **available stock value in Ghana Cedis (GHS)**
- run **sales**, accept **Cash & [Mobile Money](https://www.blackpenman.com/2026/01/complete-guide-to-mobile-money-in-ghana.html).**
- enforce **user access controls**
- generate **dashboards and reports**
- launch **health-driven promotions** ([Malaria](https://www.severemalaria.org/countries/ghana) medicines + [Condoms](https://www.who.int/teams/global-hiv-hepatitis-and-stis-programmes/stis/prevention/condoms)) during **Xmas & Easter**

> This repository is written as a **story + evidence pack**: it shows the system like a reader is “walking through the shop” - from checkout, to stock, to reporting, to security, to backups.

---

## The Story: Why this system exists

In many parts of Ghana (and across Africa), a pharmacy is more than a shop, it’s often the **closest, fastest healthcare touchpoint**.

But the day-to-day reality can be rough:
- customers queueing while staff search shelves manually
- stock levels remembered “in the head” or "shelf numbering"
- cashbook entries that don’t match the shelf
- difficulty knowing **what sells**, **what is expiring**, and **where money leaks**
- weak accountability when multiple staff use the same machine

This project documents how **PHAnford** moved from “manual guesswork” to a more structured, auditable setup using **Aronium POS** - without needing expensive enterprise software.

---

## What’s in this repo

### 1) Evidence screenshots (system walkthrough)
All key screenshots are in: **`assets/`**  
They show:
- POS interface (checkout flow)
- admin portal access
- product catalogue and stock valuation
- dashboards and sales reports
- payment method setup (Cash + Mobile Money)
- document search / audit by user
- user roles and access-level controls
- database backup configuration
- Xmas + Easter promotions setup for Malaria medicines & condoms

See: [`assets/README.md`](assets/README.md)

---

### 2) Sample data exports (products + stock valuation)
This repo includes two useful exports:
- **Products master list** (CSV)
- **Inventory/stock valuation report** (Excel)

See: [`data/README.md`](data/README.md)

> **Note:** Data is shared for portfolio and demonstration. Before public posting, always remove/blur any personal identifiers.

---

## Key Capabilities Demonstrated

### A. Fast checkout + clean sales flow
The POS interface supports:
- product search (by name/code/barcode)
- quantity/price display
- discount button (quick reduction where allowed)
- save sale / refund / transfer actions

Screenshots:
- `assets/Sales_Interface.png`
- `assets/Acessing_Admin_Portal.png`

---

### B. Stock management in Ghana Cedis (GHS)
This setup tracks:
- product quantities
- cost price and sales price
- stock value totals (useful for procurement & audit)
- visibility of **zero stock**, **non-zero stock**, and **negative stock** lines

From the screenshots (stock summaries):
- **Total products:** 3,118  
- **Pharmaceuticals:** 2,067  
- **Non-pharmaceuticals:** 616  
- **Negative quantity items:** 5 (system visibility helps catch errors fast)

Stock valuation snapshots (GHS):
- **Pharmaceuticals:** Total cost ≈ **111,892.89** | Total sale price ≈ **170,647.67**
- **Non-pharmaceuticals:** Total cost ≈ **50,994.38** | Total sale price ≈ **75,936.35**
- **All products:** Total cost ≈ **196,577.55** | Total sale price ≈ **298,918.40**

Screenshots:
- `assets/Pharmaceutical_Products_AvailableStock_inGhanaCedis.png`
- `assets/Non-Pharmaceutical_Products_AvailableStock_inGhanaCedis.png`
- `assets/Total_Products(Pharm&Non-Pharm)_AvailableStock_inGhanaCedis.png`

---

### C. Reporting: daily → monthly → annual performance
A pharmacy survives on **knowing what is moving** and **when**.

This repo demonstrates:
- sales dashboards by day
- annual/monthly charts
- top products
- hourly sales distributions
- top customers (where customer mapping is used)
- sales by product report (anonymised)

Screenshots:
- `assets/Sales_Dashboard_by_Day.png`
- `assets/Annual_Sales_Dashboard.png`
- `assets/Annual_Sales_Dashboard(contd).png`
- `assets/Sales_By_Products_Report(Anonymised).png`

---

### D. Payments: Cash + Mobile Money
Because Ghana retail reality is hybrid, the system supports:
- **Cash**
- **Mobile Money (MoMo)**

Screenshots:
- `assets/Payment_Options_for_Customers.png`
- `assets/Payment_Setup.png`

---

### E. Accountability: users, roles, and audit trails
When multiple staff sell on the same system, accountability matters.

This repo documents:
- user access levels
- permissions over actions like discounts, refunds, reports, and admin areas
- ability to **filter documents by user** to audit who did what

Screenshots:
- `assets/Users_&_AccessLevels_Summary.png`
- `assets/Users_Access&Security_Level_Setup.png`
- `assets/Users_Access&Security_Level_Setup(End).png`
- `assets/Finding_Sales_Document_By_User(Anonymised).png`

---

### F. Resilience: database backup setup
A pharmacy system must survive:
- power interruptions
- sudden restarts
- accidental data loss

This setup includes:
- manual backup
- auto backup options
- backup location configuration

Screenshots:
- `assets/Database_Setup.png`

---

## Promotions With Purpose: Xmas & Easter (Malaria + Condoms)

This repository highlights two targeted promotions:
- **Xmas Promo** (December window)
- **Easter Promo** (April window)

These promotions were configured on:
1) **Known malaria medicines**
2) **Condom brands**

Why this matters (health + business):
- Malaria remains a major cause of illness and death in many African contexts - price reductions during peak buying periods can encourage earlier treatment purchases (where appropriate).
- Condom promotions support prevention efforts for **STIs** such as:
  - **HIV**
  - **Gonorrhoea**
  - **Chlamydia**
  - **Syphilis**
  - **Trichomoniasis**
  - **Hepatitis B**
  - and reduced (not perfect) risk for infections like **HPV** and **Herpes**.

Business strategy side:
- promotions increase traffic
- improve turnover on key public-health products
- build trust and repeat customers

Screenshots:
- `assets/Xmas_Promo_Setup_for_KnownMalariaDrugs_InGhana_&_Condoms.png`
- `assets/Easter_Promo_Setup_for_KnownMalariaDrugs_InGhana_&_Condoms.png`
- `assets/Promos_Summary.png`

> **Medical note:** This is not medical advice. Discounts encourage access/uptake; they do not replace clinical guidance. Condoms reduce risk but do not eliminate risk completely.

---

## Suggested Repo Structure

```text
.
├── README.md
├── assets/
│   ├── README.md
│   └── (screenshots .png files)
└── data/
    ├── README.md
    ├── PHAnford_Products(Pharm&NonPharam).csv
    └── PHAnford_Stock(Pharm&NonPharam).xlsx
