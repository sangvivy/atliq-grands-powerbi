# AtliQ Grands — Hospitality Revenue Analysis (Power BI)

An end-to-end data analytics project analyzing revenue, occupancy, and 
cancellation trends for AtliQ Grands, a five-star hotel chain in India 
operating across 4 cities with 7 properties.

## 🎯 Business Problem

AtliQ Grands has been losing market share and revenue due to increasing 
competition and ineffective decision-making. The management wanted to 
leverage data intelligence to regain their position. This project delivers 
an interactive Power BI dashboard to support data-driven decisions.

## 🧰 Tools & Technologies

- **Power BI Desktop** — Dashboard development
- **Power Query** — Data cleaning and transformation
- **DAX** — 24 custom measures including time intelligence and WoW % changes
- **Data Modeling** — Star schema with fact and dimension tables

## 📊 Dataset

- 5 tables: `dim_date`, `dim_hotels`, `dim_rooms`, `fact_bookings`, `fact_aggregated_bookings`
- ~135,000 bookings across May–July 2022
- Source: [Codebasics Hospitality Challenge](https://codebasics.io/resources/end-to-end-data-analyst-project)

## 🏗️ Approach

1. **Data Loading** — Imported 5 CSVs via Power Query
2. **Data Transformation** — Cleaned data types, removed errors, fixed date fields
3. **Data Modeling** — Built a star schema with `fact_bookings` at the center
4. **DAX Measures** — Created 24 measures including:
   - Base: Total Bookings, Total Capacity, Daily Sellable Room Nights
   - KPI: ADR, RevPAR, Occupancy %, Realisation %, Cancellation %
   - WoW: RevPAR WoW %, ADR WoW %, Occupancy WoW %, Realisation WoW %
5. **Visualization** — Built a 3-page interactive dashboard

## 📈 Dashboard Pages

### 1. Executive Summary
High-level KPIs with week-over-week changes, revenue trends, and 
booking distribution by room class and platform.

![Executive Summary](images/01_executive_summary.png)

### 2. Revenue & KPI Trends
Weekly WoW performance comparison across ADR, RevPAR, Occupancy, DSRN, 
and Realisation. Property-level KPI breakdown.

![Revenue & KPI Trends](images/02_revenue_trends.png)

### 3. Operations & Guest Behavior
Cancellation and no-show analysis by platform and room class, plus a 
property operational scorecard.

![Operations](images/03_operations.png)

## 🔍 Key Insights

1. **Cancellation rate is 24.83%** across all booking platforms — 
   consistent across channels, indicating a systemic issue rather than 
   a platform-specific one.
2. **No-show rate is only 5.02%** — most guests cancel well before 
   check-in, giving the hotel time to resell rooms.
3. **Occupancy averages 57.87%**, leaving significant headroom to grow 
   revenue through targeted promotions.
4. **RevPAR and Occupancy move together** — occupancy is the primary 
   driver of revenue at current pricing.
5. **ADR is stable (~₹18,100)** with minimal week-to-week variation, 
   suggesting price elasticity isn't being tested.
6. **Realisation % is 85.12%** — about 15% of potential revenue is lost 
   to cancellations and no-shows.
7. **Weekend occupancy spikes** create predictable demand patterns that 
   dynamic pricing could exploit.

## 💡 Recommendations

- Introduce **flexible cancellation policies** to reduce the high cancellation rate
- Launch **direct booking incentives** to reduce OTA commission dependency
- Apply **dynamic weekend/holiday pricing** to capture peak demand
- Target **low-occupancy weeks (W21, W26, W30)** with marketing campaigns
- Investigate properties with the **highest cancellation rates** for 
  targeted operational fixes

## 📂 Project Files

- `AtliQ_Grands_Dashboard.pbix` — Full Power BI project file
- `data/` — Source CSV files
- `images/` — Dashboard screenshots

---

*Project completed as part of the Codebasics End-to-End Data Analyst 
Portfolio Challenge.*
