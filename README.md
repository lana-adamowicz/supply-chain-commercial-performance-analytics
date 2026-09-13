# 📊 Supply Chain & Commercial Performance Analytics

> **Project Overview:** An end-to-end Business Intelligence solution built in Microsoft Excel to audit and optimize logistics and commercial performance. The system analyzes **5,000 transaction rows**, tracking **15 vendors, 6 regions, and 4 product categories** over a 12-month period (2025).

---

## 🛠️ Tech Stack & Key Skills
* **Advanced Excel:** Pivot Tables & Charts, Dynamic Array Functions, Conditional Formatting, Timelines, Cross-functional Slicers
* **Power Query:** Automated ETL pipelines, Data Cleansing, Feature Engineering
* **Business Analytics:** ABC/Pareto Analysis, Supply Chain KPIs (OTD, Fill Rate, Lead Time & Delays), Financial Metrics (Revenue, AOV, Average Revenue per Vendor)
* **Data Visualization & UX:** Minimalist dashboard design, corporate pastel styling, production-ready layouts

---

## 🎯 1. Business Objectives & Approach
The project was designed as a comprehensive data audit to evaluate the intersection of commercial performance and logistics efficiency across a 12-month period. The analytical workflow was structured into three sequential stages:

* **Commercial Segmentation:** Apply **Pareto (80/20) Analysis** to identify the key vendors which generate 80% of total revenue.
* **Operational Performance Mapping:** Evaluate network reliability across vendors by measuring core supply chain metrics, specifically **OTD**, **Lead Time**, **Fill Rate**.
* **Planning vs. Operations Audit:** Cross-reference actual physical delivery timelines with expected delivery dates to detect planning anomalies or baseline mismatches.

---

## 💻 2. Data Engineering & Power Query Pipeline (Back-end)
  To ensure high file performance and prevent Excel from freezing or slowing down, **all possible calculations were shifted to Power Query**:
  
* **Data Cleansing:** Standardized text fields, eliminated duplicates, and aligned date data types.
* **Feature Engineering:** Implemented business logic directly into Power Query to compute financial and logistical metrics (`Revenue`, `Lead Time`, `Delivery Delay`) and extracted `Month Names` to optimize data modeling.
* **Documentation:** Added clear comments and notes to key transformation steps for absolute process reproducibility.

---

## 📈 3. Analytical Frameworks & KPIs (Front-end)

* **Vendor Pareto Analysis:** Applied the 80/20 rule to segment the 15 vendors based on their annual revenue generation. This served as the diagnostic starting point, revealing that 11 out of 15 vendors form the core group driving the bulk of commercial operations.
* **Delivery Status:** Applied a Pivot operation to compare deliveries by `Early`, `On Time`, and `Late` statuses, enabling precise calculation of the OTD rate.
* **Commercial Metrics & Rankings:** Built dynamic pivot tables and charts to track monthly performance trends, identify regional volume distribution, and ranked **The Top 10 Vendors** by total annual revenue to evaluate their financial impact.

---

## 📌 4. Key Insights & Strategic Recommendations
**The Problem:** The critically low **13% On-Time Delivery (OTD) rate** is driven by unrealistic system deadlines rather than vendor operational failures. Actual delivery times remain highly consistent at **~7 days** across all 15 vendors.
**The Impact:** Overly aggressive system deadlines artificially drop the Order Fill Rate to **76.2%**, creating a phantom inventory shortage over a minor **0.5-day average delay**.

💡 **The Solution (Action Plan):** 
1. **Establish realistic expected delivery dates** by aligning system settings with historical lead time data. 
2. **Consolidate the vendor portfolio** around top-volume vendors to maximize commercial leverage and phase out unreliable bottom-tier suppliers after establishing new realistic deadlines.
3. **Optimize regional logistics:** to re-evaluate or suspend operations in regions with the sharpest revenue drops after considering the previous two points and recalculating KPI values.
   
---

## 📂 5. Workbook Structure
* **Data Layer (Back-end):** `Clean Data` (Standardized Excel Table), `Query Table` (Transformed Power Query dataset with engineered features).
* **Analytical Layer (Front-end):** Multi-page interactive dashboard structured into core analytical models: `Vendor Performance` (OTD/Late analysis), `Lead Time & Volume` (Early rates & Fill Rates), `Category Metrics` (Product trends & Monthly dynamics).
