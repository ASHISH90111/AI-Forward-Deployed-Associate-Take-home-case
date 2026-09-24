
# BrightChamps AI Forward Deployed Associate Case Study

## 📌 Project Overview
This repository contains the complete data-driven analysis, financial leak quantification, and an automated agent prototype for the **BrightChamps Sales Funnel Optimization Study**.

The primary goal of this study is to identify top-of-funnel conversion leaks, isolate the operational root cause, quantify the total financial impact, and provide a low-overhead automated mitigation strategy.

---

## 📊 Core Data Findings & Metrics

An analysis of **5,000 top-of-funnel leads** across a 2-month period ($N=2,500\text{ leads/month}$) revealed a major bottleneck between **Stage 2 (Demos Scheduled)** and **Stage 3 (Demos Joined)**.

* **Funnel Baseline Join Rate:** 63.8% (2,060 joined out of 3,229 scheduled demos)
* **Monthly Demo No-Shows:** 584.5 leads / month
* **Financial Leak Impact:**
  * **Unrealized Revenue Leak:** **₹61.63 Lakhs/month** ($\approx \text{₹}6,162,786$)
  * **Sunk Marketing CAC Lost:** **₹5.26 Lakhs/month** ($\approx \text{₹}526,050$ at ₹900 CAC/lead)
  * **Total Monthly Financial Leak:** **₹66.89 Lakhs/month**

---

## 🔍 Root Cause Analysis
Cross-referencing lead metadata against representative scheduling data indicates that **71.0% of all scheduled no-shows** (830 out of 1,169) stem directly from a **Parent Timezone vs. Sales Rep Shift Misalignment**. 

Leads in non-IST timezones (e.g., Singapore, Ho Chi Minh, Sydney) were frequently assigned to representatives working default IST shifts, leading to delayed touchpoints, off-peak outreach, and dropped demo appointments.

---

## 🚀 The Proposed Solution ("The Lever")
Instead of increasing ad spend or scaling manual sales headcount, we deploy a **Smart Timezone Alignment Engine & WhatsApp Automated Dispatcher**:

1. **Dynamic Shift Re-routing:** Detects parent timezone upon lead creation (`parent_timezone`) and dynamically routes the lead to a regional representative shift (`US_SHIFT`, `SEA_SHIFT`, `EMEA_SHIFT`).
2. **Automated WhatsApp Engagement:** Dispatches instant localized calendar confirmation messages with quick-reply triggers (Reply 1 to Confirm, 2 to Reschedule).

### Target Impact Model:
* **Target Join Rate:** $63.8\% \rightarrow 75.0\%$ (+11.2% improvement)
* **Recovered Monthly Joined Demos:** +181 joined demos / month
* **Recovered Revenue Value:** **+₹19.08 Lakhs / month** (+₹2.29 Crore / year)

---

## 🛠️ Repository Structure & Python Code

### Prerequisites
Ensure you have the following Python libraries installed:
```bash
pip install pandas numpy
