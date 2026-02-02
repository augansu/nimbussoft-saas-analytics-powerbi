# Semantic Model Specification

## Model Overview
The semantic model is designed as a **clean star schema** to ensure predictable filter behavior, performance, and analytical correctness across product usage and support domains.

The model supports cross-domain analysis, such as correlating product usage trends with support friction and customer risk.

---

## Fact Tables

### FactProductUsage
**Grain:** One row per product usage event per customer per date.

**Purpose:**
- Measure engagement intensity
- Track adoption and usage momentum
- Support rolling-window analytics

---

### FactSupportTickets
**Grain:** One row per support ticket.

**Purpose:**
- Measure support volume, backlog, and throughput
- Evaluate SLA compliance
- Analyze escalation and resolution patterns

---

## Dimensions

### DimCustomer
- Represents unique customers
- Used consistently across all fact tables
- Supports segmentation by tier and account type

---

### DimProductModule
- Represents functional areas or features of NimbusCore
- Enables feature-level adoption analysis

---

### DimSupportTeam
- Represents internal support teams
- Enables team-level performance analysis

---

### DimPriority
- Represents ticket priority levels
- Drives SLA targets and urgency analysis

---

### DimPlatform
- Represents product access platforms
- Enables usage pattern segmentation

---

## Date Table & Role-Playing Dates

### DimDate
- Single, marked Date table
- Drives all time intelligence

**Role-playing dates:**
- CreatedDate (active relationship)
- ResolvedDate (inactive relationship activated via USERELATIONSHIP)

This design avoids duplicate date tables while supporting lifecycle analysis.

---

## Relationship Design Principles
- One-to-many relationships from dimensions to facts
- Single-direction filtering
- No bidirectional relationships
- No snowflaking unless analytically required

These principles ensure predictable behavior and reduce ambiguity.
