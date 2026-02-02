# KPI Dictionary

This document defines canonical KPIs used across the analytics platform.  
Each KPI is documented with business intent to prevent misinterpretation.

---

## Active Customers (Rolling 30 Days)
**Business Definition:**  
Distinct customers generating usage events in the last 30 days.

**Grain:** Customer

**Time Context:** Rolling 30 days

**Intended Decision Use:**  
Monitor engagement base and adoption trends.

**Notes:**  
Used as denominator for usage intensity metrics.

---

## Usage Intensity (Events per Active Customer)
**Business Definition:**  
Average number of usage events per active customer in the rolling window.

**Grain:** Aggregate

**Time Context:** Rolling 30 days

**Intended Decision Use:**  
Assess depth of engagement, not just breadth.

**Notes:**  
Sensitive to rolling window grain.

---

## SLA Compliance Rate
**Business Definition:**  
Percentage of resolved tickets meeting SLA targets.

**Grain:** Ticket

**Time Context:** Selected period

**Intended Decision Use:**  
Evaluate support effectiveness and operational risk.

---

## Customers At Risk (Rolling 30 Days)
**Business Definition:**  
Customers showing low usage or significant usage decline relative to peers.

**Grain:** Customer

**Time Context:** Rolling 30 days vs prior rolling period

**Intended Decision Use:**  
Early identification of churn and disengagement risk.

**Notes:**  
Uses percentile-based thresholds to avoid arbitrary cutoffs.

---

## Customer Risk Score (0–100)
**Business Definition:**  
Composite score combining usage drop, low usage, SLA breaches, and escalations.

**Grain:** Customer

**Time Context:** Rolling 30 days

**Intended Decision Use:**  
Prioritize outreach and intervention.

**Notes:**  
Score is capped between 0 and 100 to maintain interpretability.
