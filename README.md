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

* **Commercial Segmentation:** Applying **Pareto (80/20) Analysis** to identify the key vendors which generate 80% of total revenue.
* **Operational Performance Mapping:** Evaluating network reliability across vendors by measuring core supply chain metrics, specifically **OTD**, **Lead Time**, **Fill Rate**.
* **Planning vs. Operations Audit:** Cross-referencing actual physical delivery timelines with expected delivery dates to detect planning anomalies or baseline mismatches.

---

## 💻 2. Data Engineering & Power Query Pipeline (Back-end)
  To ensure high file performance and prevent Excel from freezing or slowing down, **all possible calculations were shifted to Power Query**:
  
* **Data Cleansing:** Standardized text fields, eliminated duplicates, and aligned data types.
* **Feature Engineering:** Implemented business logic directly into Power Query, computed financial and logistical metrics (`Revenue`, `Lead Time`, `Delivery Delay`) and extracted `Month Names` to optimize data modeling.
* **Documentation:** Added clear comments and notes to key transformation steps for absolute process reproducibility.

---

## 📈 3. Analytical Frameworks & KPIs (Front-end)

* **Vendor Pareto Analysis:** Applied the 80/20 rule to segment the 15 vendors based on their annual revenue generation. This served as the diagnostic starting point, revealing that 11 out of 15 vendors form the core group driving the bulk of commercial operations.
* **Delivery Status:** Applied a Pivot operation to compare deliveries by `Early`, `On Time`, and `Late` statuses, enabling precise calculation of the OTD rate.
* **Commercial Metrics & Rankings:** Built dynamic pivot tables and charts to track monthly performance trends, identify regional volume distribution, and ranked **the Top 10 Vendors** by total annual revenue to evaluate their financial impact.

---

## 📌 4. Key Insights & Strategic Recommendations
**The Problem:** The critically low **13% On-Time Delivery (OTD) rate** is driven by unrealistic system deadlines rather than vendor operational failures. Actual delivery times remain highly consistent at **~7 days** across all 15 vendors.
**The Impact:** Overly aggressive system deadlines artificially drop the Order Fill Rate to **76.2%**, creating a phantom inventory shortage due to a **0.5-day average delay**.

💡 **The Solution (Action Plan):** 
1. **Establish realistic expected delivery dates** by aligning system settings with historical lead time data. 
2. **Consolidate the vendor portfolio** around top-volume vendors to maximize commercial leverage and phase out unreliable bottom-tier vendors after establishing new realistic deadlines.
3. **Optimize regional logistics:** re-evaluate or suspend operations in regions with the sharpest revenue drops after considering the previous two points and recalculating KPI values.
  <img width="1135" height="393" alt="Delivery_Analysis" src="https://github.com/user-attachments/assets/b394205f-30db-4e95-875f-04f43ff9ba32" />
    
---

## 📂 5. Workbook Structure
* **Data Layer (Back-end):** `Clean Data` (Standardized Excel Table), `Query Table` (Transformed Power Query dataset with engineered features).
* **Analytical Layer (Front-end):** Multi-page interactive dashboard structured into core analytical models: `Vendor Performance` (OTD/Late analysis), `Lead Time & Volume` (Early rates & Fill Rates), `Category Metrics` (Product trends & Monthly dynamics).


<details>
  <summary>🔍 Expand Cleaned query_table Structure (For Team Lead)</summary>
  <br>
  
  > **Note for reviewer:** The first 6 rows of the final dataset are presented below to demonstrate the comprehensive 19-column data structure, custom calculated metrics, and how the ETL logic handles Cancelled, In Transit, and Delivered orders.

  | Order_ID | Vendor_ID | Product_Category | Order_Date | Expected_Delivery_Date | Actual_Delivery_Date | Status | Quantity | Price_Per_Unit | Region | Revenue | Month_Name | Lead_Time | Delivery_Delay | Non_Delivered | Late | On_Time | Early | Delivered_Qty |
  | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
  | ORD-0001 | VND-007 | Furniture | 01/01/2025 | 10/01/2025 | | Cancelled | 2 | 9500 | Central | 19000 | January | | | 1 | 0 | 0 | 0 | 0 |
  | ORD-0002 | VND-004 | Apparel | 01/01/2025 | 09/01/2025 | | Cancelled | 18 | 75 | International | 13500 | January | | | 1 | 0 | 0 | 0 | 0 |
  | ORD-0003 | VND-013 | Office Supplies | 01/01/2025 | 07/01/2025 | 08/01/2025 | Delivered | 55 | 12 | South | 660 | January | 7 | 1 | 0 | 1 | 0 | 0 | 55 |
  | ORD-0004 | VND-015 | Apparel | 01/01/2025 | 09/01/2025 | | In Transit | 48 | 75 | South | 3600 | January | | | 1 | 0 | 0 | 0 | 0 |
  | ORD-0005 | VND-011 | Office Supplies | 01/01/2025 | 05/01/2025 | 05/01/2025 | Delivered | 71 | 18 | West | 1278 | January | 4 | 0 | 0 | 0 | 1 | 0 | 71 |
  | ORD-0006 | VND-008 | Furniture | 01/01/2025 | 07/01/2025 | 10/01/2025 | Delivered | 1 | 12000 | East | 12000 | January | 9 | 3 | 0 | 1 | 0 | 0 | 1 |

  *...5,000 rows in total.*

  👉 **[View Full Cleaned Dataset (CSV)](./Query_Table.csv)**

</details>
