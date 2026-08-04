# Milestone 3: Supplier Scorecard & Transportation Analytics

## 📊 Executive Summary
Milestone 3 expands the **Supply Chain Visibility & Optimization** platform by integrating supplier performance metrics and transportation cost efficiency analysis using Microsoft Power BI. The solution provides strategic dashboards for vendor evaluation, risk management, and logistics cost optimization.

---

## 🖼️ Dashboard Overview

### 1. Supplier Scorecard Generation
* **Key Metrics:** Total Suppliers, Average Quality Score, Average Reliability %, Average Lead Time (Days).
* **Core Visuals:**
  * **Lead Time vs. Reliability Scatter Plot:** Highlights vendor risk profiles across quality scores.
  * **Supplier Composite Score Ranking:** Ranks suppliers based on weighted performance.
  * **Tier Status Distribution:** Categorizes suppliers into Low, Medium, and High performance tiers.
  * **Quality Score Distribution:** Histogram binning supplier count by quality tiers.
  * **Vendor Detail Matrix:** Granular breakdown of lead times, quality scores, and product lines per vendor.

### 2. Transportation Analytics
* **Key Metrics:** Average Profit Per Order, Total Discount Given, Average Discount Rate %, Same Day Share %.
* **Core Visuals:**
  * **Discount Analysis by Shipping Mode:** Quantifies total discount allocation across shipping options.
  * **Late Delivery Rate by Shipping Mode:** Tracks late delivery risks per fulfillment type.
  * **Average Profitability by Shipping Mode:** Evaluates financial margins across shipping tiers.
  * **Order Volume by Shipping Mode:** Donut chart breakdown of fulfillment volume distribution.
  * **Regional Late Rate Heatmap:** Cross-evaluates market and region performance to spot delayed delivery bottlenecks.

---

## 📐 Methodologies & DAX Logic

### 1. Supplier Composite Score Calculation
* **Methodology:** Multi-criteria weighted decision analysis evaluating quality, reliability, and delivery speed.
* **Weights:** 40% Quality Score + 40% Reliability % + 20% Delivery Speed Index.
* **DAX Implementation:**
  ```dax
  Supplier Composite Score = 
  ([Avg Quality Score] * 0.4) + 
  ([Avg Reliability %] * 0.4) + 
  ((100 - [Avg Lead Time (Days)]) * 0.2)
