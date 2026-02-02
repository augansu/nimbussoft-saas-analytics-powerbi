# Governance Framework

## What a Governed Dataset Means
A governed dataset exposes only **approved, canonical metrics** while hiding raw facts and technical columns.  
This prevents metric drift and ensures consistent interpretation.

---

## Canonical KPI Policy
- Each KPI has a documented definition and intent
- Only canonical KPIs are exposed to report authors
- Ad hoc measures are discouraged

---

## Hidden Facts & Technical Columns
- Fact tables are hidden from report view
- Surrogate keys and helper columns are hidden
- Users interact only with business-friendly dimensions and measures

---

## Archived / Deprecated Logic
- Deprecated KPIs are hidden, not deleted
- Archived logic is retained for lineage and reference
- Canonical replacements are documented

---

## KPI Change Management
- KPI changes require documentation
- Historical results are not silently overwritten
- Changes are version-aware and defensible

Governance exists to preserve **trust**, not restrict flexibility.
