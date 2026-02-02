# Performance & Tradeoffs Notes

## Performance Profiling Approach
Performance was evaluated using:
- Power Query Diagnostics (refresh behavior)
- Performance Analyzer (visual rendering)

---

## Known Expensive Patterns
- Rolling time windows evaluated at fine grain
- Customer-level iteration
- Percentile-based calculations

These patterns are analytically necessary in SaaS risk detection.

---

## Resolved Issues
- Corrected time-axis grain for executive visuals
- Standardized month-level aggregation where appropriate
- Eliminated redundant evaluations

---

## Accepted Tradeoffs
Some metrics remain computationally expensive by design.  
Simplifying them would reduce analytical value and risk detection accuracy.

---

## Scalability Considerations
- Incremental refresh can be introduced if data volume grows
- Aggregation tables may be added for high-level trends
- Core logic is designed to scale without rework
