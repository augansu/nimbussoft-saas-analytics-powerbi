# Customer 360 Drill-through Page

## Purpose
The Customer 360 drill-through page provides an investigative view of a single customer’s engagement, support demand, and risk profile. It is designed to support Customer Success, Support Leadership, and Product stakeholders in understanding *why* a customer is healthy or at risk and what intervention may be required.

This page is intentionally not accessible via primary navigation and is only reached through drill-through from customer-level visuals. This preserves dashboard clarity while enabling deep contextual analysis.

---

## Analytical Structure

The page follows a structured investigation flow:

1. **Current State (KPI Strip)**  
   - Customer Risk Score (0–100)  
   - At-Risk Status (R30D)  
   - Usage Events (R30D)  
   - Usage Drop % (R30D vs Prior R30D)  
   - Tickets Created (R30D)  
   - SLA Breach Rate % (R30D)

   These KPIs answer:  
   *“What is the customer’s current health and support status?”*

2. **Trends (Momentum & Quality Over Time)**  
   - Monthly Usage Trend  
   - Ticket Volume vs SLA Breach Trend (with SLA target reference)

   These visuals answer:  
   *“Is performance improving or deteriorating?”*

3. **Drivers (Root Cause Analysis)**  
   - Top Product Modules by Usage (R30D)  
   - Tickets by Priority (R30D)

   These answer:  
   *“What is driving engagement or friction?”*

4. **Operational Detail (Action Layer)**  
   - Ticket-level detail table including priority, SLA compliance, and resolution time

   This enables immediate intervention.

---

## Design & Governance Principles

- Drill-through is configured using `DimCustomer[CustomerName]`
- "Keep all filters" is enabled to preserve time and segment context
- The page is hidden from main navigation
- Only canonical, documented KPIs are used
- Visual hierarchy follows enterprise SaaS analytics standards
- Composition visuals (donut chart) are used sparingly and only for limited categorical breakdowns

---

## Business Value

The Customer 360 page transforms high-level risk indicators into actionable diagnostics. It bridges product usage behavior, support performance, and retention risk in a single contextual view, enabling proactive customer management rather than reactive reporting.
