# Vendor Performance Analysis 📊

A data-driven analysis of vendor and brand performance in the spirits/alcohol distribution sector.  
Using 10,692 transaction records, this project identifies top-performing vendors and brands, compares profit margins across segments, and proposes strategies for promotions, pricing, and portfolio optimization.

---
## 🛠️ Tools & Technologies

- **Language**: Python 3.x  
- **Data manipulation**: `pandas`, `numpy`  
- **Visualization**: `matplotlib`, `seaborn`  
- **Statistics**: `scipy.stats` (t‑tests, confidence intervals)  
- **Database**: `sqlite3` (reading from `inventory.db` / `vendorsalessummary` table)  
- **Notebook environment**: Jupyter Notebook (`Vendor-Performance-Analysis.ipynb`)  

## 🔍 Project Objectives

- Identify top-performing **vendors** and **brands** by sales.
- Evaluate **profitability** (gross profit, profit margin) across vendors.
- Understand the relationship between **sales volume** and **profit margin**.
- Find **high-margin, high-potential** brands for promotions / pricing changes.
- Provide **actionable recommendations** for vendor and pricing strategy.

---

## 🧾 Dataset Overview

The analysis is based on a consolidated vendor–sales summary table with:

- **Vendor information**: `VendorNumber`, `VendorName`
- **Product details**: `Brand`, `Description`, `volume`
- **Monetary features**: `PurchasePrice`, `ActualPrice`, `TotalPurchaseDollar`, `TotalSalesDollars`, `TotalSalesPrice`
- **Quantities**: `TotalPurchaseQuantity`, `TotalSalesQuantity`
- **Costs & taxes**: `TotalExciseTax`, `FreightCost`
- **Performance metrics**: `GrossProfit`, `ProfitMargin`, `StockTurnover`, `SalesPurchaseratio`

The notebook also includes basic data-quality checks and exploratory data analysis.

---

## 📈 Key Visuals


### 1. Vendor & Brand Frequency
<img width="905" height="373" alt="image" src="https://github.com/user-attachments/assets/f08bc2d4-c60e-4007-b2fd-99c621405f7b" />

Figure 1 – Count Plot of VendorName and Description

Shows which vendors and brands appear most frequently (e.g. MARTIGNETTI COMPANIES, DIAGEO NORTH AMERICA INC, Southern Comfort, etc.), helping to understand portfolio concentration.

---

### 2. Distributions of Numeric Features

<img width="905" height="602" alt="image" src="https://github.com/user-attachments/assets/1332ee96-05ef-4652-84bb-b71098b9cdf0" />

Figure 2 – Distribution of Key Numerical Features

Histograms for volume, purchase/sales dollars, gross profit, profit margin, freight, etc.  
Reveals heavy right-skew in monetary variables and a roughly bell-shaped distribution for profit margin.

---

### 3. Correlation Heatmap
<img width="905" height="710" alt="image" src="https://github.com/user-attachments/assets/284a629c-b788-4cc6-bccd-542290cca5cf" />

Figure 3 – Correlation Heatmap

Highlights strong positive correlations between quantities and dollar amounts (e.g. `TotalSalesQuantity` vs `TotalSalesDollars`) and shows that profit margin is mostly uncorrelated with sales volume.

---

### 4. Top Vendors & Brands by Sales

- Top 10 vendors contribute the majority of sales (e.g. DIAGEO NORTH AMERICA INC, MARTIGNETTI COMPANIES, PERNOD RICARD USA, etc.).
- Top brands include Jack Daniels No 7 Black, Tito’s Handmade Vodka, Grey Goose Vodka, Capt Morgan Spiced Rum, and Absolut 80 Proof.

---

### 5. Vendor Purchase Contribution
<img width="905" height="346" alt="image" src="https://github.com/user-attachments/assets/ff29a6a6-e3be-4c7e-8ed0-dacc8bde57fb" />

Figure 5 – Top 10 Vendors' Purchase Contribution

Donut chart showing that the **top 10 vendors account for ~66%** of total purchase dollars, with DIAGEO alone contributing a large share. This illustrates vendor concentration and portfolio risk.

---

### 6. Profit Margin Comparison (Top vs Low Vendors)

Compares profit margin distributions and 95% confidence intervals:

- Top vendors (by sales volume) have mean margin around **31%**.
- Low-volume vendors have mean margin around **42%**.
- A t‑test shows this difference is **statistically significant (p < 0.001)**.

---

### 7. Promotional / Pricing Targets

- High-margin, high-sales brands are ideal **candidates for premium positioning** (protect margin).
- Low-margin, high-sales brands are **candidates for price/discount review**.
- Low-sales, high-margin brands can be **premium niches** with selective promotion.
- Low-sales, low-margin brands are **discontinuation / repositioning candidates**.

---

## 🧠 Main Insights

- **Market concentration**: Top 10 vendors generate ~66% of purchases; the rest are fragmented.
- **Inverse sales–margin pattern**: High-volume vendors tend to have **lower margins**, while low-volume vendors operate at **higher margins**.
- **Statistically significant margin gap** (~10 percentage points) between top vs low vendors.
- **Brand-level opportunities**: Certain brands combine strong sales and very high margins and should be protected from over-discounting.
- **Operational efficiency**: Stock turnover is close to 1 on average, indicating reasonable inventory management.

---

## ✅ Recommendations (High Level)

- Negotiate better terms and logistics costs with the **largest vendors** to recover margin.
- Develop a **selective growth plan** for profitable, lower-volume vendors/brands.
- Use the sales–margin scatter to drive **promotion and discount decisions**.
- Rebalance the portfolio over time to reduce reliance on any single vendor while protecting total margin.

---


