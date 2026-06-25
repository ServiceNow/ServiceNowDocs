---
title: MPN Formula Engine processing
description: The Formula Engine processes raw KPI formulas and stores the result in the Formatted KPI Formula field when a record is inserted or updated in the MPN Formulas \[sn\_tsom\_em\_conns\_kpi\_definitions\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formula-engine.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Performance management: Metric collection, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# MPN Formula Engine processing

The Formula Engine processes raw KPI formulas and stores the result in the **Formatted KPI Formula** field when a record is inserted or updated in the MPN Formulas \[sn\_tsom\_em\_conns\_kpi\_definitions\] table.

When a record is inserted or updated in the MPN Formulas table, a business rule named Transform KPI Formula to Script fires automatically. It invokes the `NokiaMpnFormulaEngineSEP` extension point to process the raw formula before it is stored in the **Formatted KPI Formula** field.

The processing runs in two steps:

1.  Cleanup: The raw value in **KPI Formula** is normalized into a JavaScript-evaluable expression:
    -   Whitespace and line breaks are collapsed to a single space.
    -   `Sum()` wrappers are removed; `Max()` and `Min()` are converted to `Math.max()` and `Math.min()`.
    -   `**` exponentiation notation is converted to `Math.pow()` for compatibility with the MID Server JavaScript engine.
2.  Validation — The processed formula is checked for balanced parentheses. If the parentheses are unbalanced, the raw value is still stored but a warning is logged. Records with unbalanced parentheses are skipped during metric collection at runtime.

The resulting value is written to the **Formatted KPI Formula** field and is the expression that the metric calculation engine references at runtime.

**Note:** If no `NokiaMpnFormulaEngineSEP` implementation is registered, the raw value in the **KPI Formula** value is stored unchanged and a warning is logged.

**Related topics**  


[MPN Formulas table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formulas-table.md)

