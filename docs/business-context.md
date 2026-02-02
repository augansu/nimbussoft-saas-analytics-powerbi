# Business Context & Analytical Framing

## Project Objective
The objective of this analytics platform is to support executive and operational decision-making for a mid-market B2B SaaS company, NimbusSoft, and its core product, NimbusCore.

The platform is designed to answer **business-critical questions** across product adoption, support operations, and customer health, with a focus on early risk detection and proactive intervention rather than retrospective reporting.

This phase intentionally avoided tools and visuals and focused on defining *what problems analytics must solve* before any modeling or KPI design occurred.

---

## Stakeholders & Decisions Supported

### VP of Product
**Primary concerns:**
- Is the product being actively used as designed?
- Which features drive adoption versus disengagement?
- Are there early signals of declining engagement?

**Decisions supported:**
- Feature investment and prioritization
- Product roadmap adjustments
- Adoption improvement initiatives

---

### Head of Customer Support
**Primary concerns:**
- Are SLAs consistently met?
- Where are bottlenecks forming?
- How efficiently are teams handling workload?

**Decisions supported:**
- Staffing and capacity planning
- Process improvements
- Escalation management

---

### Director of Customer Success
**Primary concerns:**
- Which customers are at risk?
- How does product usage relate to support demand?
- Which accounts require high-touch engagement?

**Decisions supported:**
- Customer outreach prioritization
- Retention strategies
- Account segmentation

---

### Executive Leadership (CEO / COO)
**Primary concerns:**
- Is customer experience improving or degrading?
- Where should leadership intervene proactively?
- Are operational risks increasing?

**Decisions supported:**
- Strategic investments
- Cross-functional alignment
- Risk mitigation

---

## Business Concerns → Analytical Questions

### Product Usage & Adoption
- What percentage of customers generate usage events weekly and monthly?
- How does usage trend over time?
- Which features are most and least used?
- How does usage vary by customer tier?

---

### Support Operations & SLA
- What percentage of tickets meet SLA targets?
- How does SLA performance change over time?
- Which priorities and teams drive backlog risk?

---

### Customer Health & Retention Risk
- Which customers show declining usage?
- Are low-usage customers generating more support demand?
- Which customers show combined risk signals?

---

## Key Assumptions
- Customers are segmented into tiers (SMB, Mid-Market, Enterprise)
- Product usage events represent meaningful engagement
- SLA targets vary by ticket priority
- A ticket is considered resolved when a resolution timestamp is populated

These assumptions are explicitly documented to prevent downstream KPI disputes.
