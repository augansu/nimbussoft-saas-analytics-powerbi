# SaaS Product & Support Analytics Platform (Power BI)

**NimbusSoft — Executive, Product, and Customer Risk Analytics**

---

## How to Review This Project (2-Minute Lens)

This repository is **not a dashboard gallery**.

It demonstrates how a senior analytics practitioner designs a **governed, production-style Power BI solution** that supports executive decision-making in a SaaS environment.

When reviewing, focus on:

* **Why** specific KPIs exist (not just what they show)
* How product usage, support operations, and customer risk are **connected**
* The **architecture, governance, and tradeoffs**, not visual polish alone

---

## 1 Project Overview

This project simulates a **production-grade SaaS analytics platform** for a fictional mid-market B2B company, **NimbusSoft**, and its core product **NimbusCore**. It is designed using **patterns, architectures, and governance approaches I have implemented in a real SaaS organization**, adapted here using synthetic data for portfolio demonstration.


The objective was **not** to build dashboards, but to design a **governed analytics system** that enables leadership to:

* Understand product adoption and usage momentum
* Monitor support performance and SLA risk
* Identify early customer disengagement and churn risk
* Decide **where to intervene proactively**

Although the data is synthetic, the **modeling approach, DAX patterns, governance decisions, and performance tradeoffs** mirror real-world SaaS analytics implementations.

---

## 2 Business Context & Stakeholders

**Primary stakeholders supported by this solution:**

* **VP of Product** — feature adoption, engagement trends
* **Head of Customer Support** — SLA compliance, backlog risk
* **Director of Customer Success** — customer health and retention risk
* **Executive Leadership** — cross-functional intervention signals

Each KPI and dashboard in this project traces back to **explicit stakeholder questions and decisions**, not generic reporting.

---

## 3 Solution Architecture (High Level)

### Data Sources

* Product usage events
* Support ticket data
  *(simulated to reflect realistic SaaS patterns)*

### Semantic Model

* Clean **star schema**
* Two fact tables at different grains:

  * **Product Usage** (event grain)
  * **Support Tickets** (ticket grain)
* Conformed dimensions:

  * Date, Customer, Product Module, Priority, Support Team, Platform
* Single marked Date table with **role-playing dates** for ticket lifecycle analysis

### Analytics Layer

* Canonical KPI definitions
* Centralized measure catalog
* Defensive DAX patterns
* Rolling time intelligence and trend comparisons

---

## 4 Key Analytics & KPIs

### Product & Adoption

* Active customers (rolling)
* Usage intensity (events per active customer)
* Adoption breadth across modules
* Usage trends and momentum

### Support Operations

* Ticket throughput and backlog
* SLA compliance and breach rate
* Escalation trends
* Team performance diagnostics

### Customer Health & Risk

* Customers at Risk (percentile-based low usage + usage decline)
* Composite Customer Risk Score (0–100)
* Early churn proxy indicators

These KPIs are designed to surface **signals**, not just historical counts.

---

## 5 Dashboards (What They Enable)

The solution includes five executive and operational views plus one detailed customer 360 drillthrough page:


1. **Executive Overview** — rolling KPIs and trends
   ![Executive Overview Dashboard](images/01_executive-overview.png)
   
   
2. **Support Operations** — SLA, backlog, throughput
   ![Support Operations Dashboard](images/02_support-operations.png)
   

3. **Product Adoption & Usage** — engagement and feature usage
   ![Product Adoption & Usage Dashboard](images/03_product-adoption-usage.png)
   

4. **Customer Health & Risk** — early churn signals
   ![Customer Health & Risk Dashboard](images/04_customer-health-risk.png)
   

5. **Executive Insights & Action Framework** — diagnostic matrix for intervention
    ![Executive Insights & Action Dashboard](images/05_executive-insights-action.png)

6. **Customer 360 Drill-through Page** - A dedicated Customer 360 drill-through page enables contextual investigation of customer health, combining rolling usage metrics, SLA performance, and ticket-level detail. The page is intentionally hidden from primary navigation and accessed via drill-through to preserve executive dashboard clarity while supporting deep operational analysis.



Dashboards are intentionally **diagnostic and action-oriented**, not exploratory demos.

> Representative screenshots are provided in the `/images` folder for context only.

---

## 6 Performance & Governance

* Dataset implemented as a **governed semantic model**
* Fact tables and technical keys hidden from report authors
* Canonical KPIs exposed through a curated measure catalog
* Deprecated logic archived rather than deleted
* Performance profiled using **Power Query Diagnostics** and **Performance Analyzer**
* Analytically expensive metrics (e.g., percentile-based risk) explicitly documented and justified


This approach supports **trusted self-service analytics** at scale.

### Semantic Model Overview

![Star Schema Semantic Model](images/semantic-model-star-schema.png)



---

## 7️⃣ What This Project Demonstrates

* Business-first analytics design
* Strong data modeling fundamentals
* Advanced DAX with explainable tradeoffs
* Governance and metric discipline
* Executive-focused storytelling
* Realistic SaaS analytics patterns

---

## 8️⃣ Notes & Disclaimer

All data used in this project is **synthetic and fictional**, created solely for portfolio demonstration purposes.
However, the **analytics patterns, data modeling decisions, DAX techniques, governance structures, and performance considerations** reflect approaches I have **designed and implemented in real SaaS analytics environments.**

NimbusSoft and NimbusCore are not real companies or products.

---

## 📁 Repository Navigation

* `/images` — dashboard screenshots (context only)
* `/docs` — supporting documentation (model, KPIs, governance)
* `/assets` — diagrams and supporting visuals
* `/pbix` — Power BI report files (included only if appropriate for public sharing)
  - `/pbix` — Power BI report files (available upon request or during interviews)


> *Additional architecture, governance, and performance documentation is available in the `/docs` folder for reviewers who want a deeper technical dive.*



