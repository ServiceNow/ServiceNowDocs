---
title: MPN latency KPIs
description: Reference for the latency KPIs collected by the MPN Pull Connector and the derived UE-to-switch latency metric.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-latency-kpis.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 1
keywords: [Nokia MPN]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# MPN latency KPIs

Reference for the latency KPIs collected by the MPN Pull Connector and the derived UE-to-switch latency metric.

## Source KPIs

The MPN Pull Connector collects the following latency KPIs from the `e2e-latency-collector-{env}` Elasticsearch index, filtered to round-trip-time samples \(`phase=rtt`\).

|KPI|Description|
|---|-----------|
|`collector2ue`|Latency between the collector and the user equipment \(UE\).|
|`collector2sw`|Latency between the collector and the switch.|

## Derived KPI

TSOM calculates one additional KPI from the source KPIs. This value is not reported directly by the vendor; it is computed after both source KPIs are collected.

|KPI|Description|
|---|-----------|
|`ue2sw`|User-equipment-to-switch latency, calculated as `collector2sw` minus `collector2ue`. If a switch-side record is missing for a given DNN in a collection cycle, the calculation is skipped for that cycle.|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[MPN Formulas table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formulas-table.md)

[MPN Formula Engine processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formula-engine.md)

[MPN Latency Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/mpn-latency-dashboard.md)

