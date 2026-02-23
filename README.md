# NSP_MENE_GLOBAL
A high-impact Power BI dashboard designed for real-time monitoring of offshore assets. This "Command Center" visualizes critical KPIs including Total Revenue, Fleet Utilization, and Avg. Daily Rates across global ROV and Vessel operations, it provides executive-level insights into asset health and geospatial deployment.
![WhatsApp Image 2026-02-23 at 2 30 39 PM](https://github.com/user-attachments/assets/cc3debe3-1a97-4e9c-9e54-72f8a07c0f5b)
power-bi, data-analytics, dax, offshore-operations, dashboard-design.
Uploaded .pbix file, cleaned datasets, and high-contrast
UI assets. Integrated DAX measures for Revenue and Utilization tracking.
# 🌊 NSP Mene Global | Offshore Operations Command Center

![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge&logo=powerbi&logoColor=white&color=orange)
![Data](https://img.shields.io/badge/Industry-Offshore_Energy-blue?style=for-the-badge)

## 📌 Project Overview
This project involves the development of a high-fidelity **Command Center Dashboard** for **NSP Mene Global**. The solution transforms complex offshore operational data into actionable intelligence, allowing for real-time monitoring of high-value assets (ROVs and Vessels).

---

## 👔 Stakeholder Executive Summary

### 🚩 The Challenge
Managing offshore assets involves high daily operational costs. Without centralized visibility, leadership faces delayed insights into fleet utilization, revenue leakage, and disconnected geospatial deployment data.

### ✅ The Strategic Solution
This dashboard acts as a "Single Source of Truth," enabling stakeholders to:
* **Maximize Revenue:** Identify top-earning assets and optimize standby equipment.
* **Enhance Logistics:** Use the Geospatial Map for real-time deployment tracking.
* **Control Costs:** Monitor Average Daily Rates (ADR) to maintain market competitiveness.

---

## 🛠️ Technical Implementation & DAX Measures
To achieve the "Exactly like the reference" look, the following custom DAX measures were implemented:

#### 1. Total Fleet Revenue
```dax
Total Revenue = SUM('Fleet_Data'[Daily_Rate_NGN])

Avg Daily Rate = AVERAGE('Fleet_Data'[Daily_Rate_NGN])

Utilization % = 
DIVIDE(
    CALCULATE(COUNT('Fleet_Data'[Asset_ID]), 'Fleet_Data'[Status] = "Active"),
    COUNT('Fleet_Data'[Asset_ID]),
    0
)

