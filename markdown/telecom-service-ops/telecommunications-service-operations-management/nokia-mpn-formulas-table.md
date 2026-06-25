---
title: MPN Formulas table
description: Reference for the MPN Formulas \[sn\_tsom\_em\_conns\_kpi\_definitions\] table and the automatic processing that occurs when a record is inserted or updated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formulas-table.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# MPN Formulas table

Reference for the MPN Formulas \[sn\_tsom\_em\_conns\_kpi\_definitions\] table and the automatic processing that occurs when a record is inserted or updated.

## MPN Formulas table columns

|Column|Description|
|------|-----------|
|Release|Release version|
|Vendor|Vendor name|
|Technology|Radio technology type \(for example, NR, LTE\)|
|KPI Formula|Raw formula string|
|Index|Elasticsearch index pattern to query \(for example, `radio-pm*`\)|
|Labels Up Down|Indicates the direction of the KPI metric. The available values are up and down.|
|Labels Vendor KPI ID|Unique KPI identifier assigned by the vendor|
|Labels KPI Standard Name|Standardized name for the KPI|
|Labels KPI Node|Node-level label associated with the KPI. The available values are RAN, Core, or Latency Collector.|
|Unit|Unit of measurement for the KPI value, for example, %, Mbps|
|Source Time Interval|Data collection time interval from the source system|
|Aggregation Type|How the KPI value is aggregated, for example, AVG, SUM|
|CI Label|Path in the Elasticsearch document used to extract the CI identifier|
|CI Class|ServiceNow CI class the KPI is mapped to|
|Component Aggregation|Aggregation method applied at the component level. The available values are flat, hierarchy, or flat+hierarchy.|
|MPC Description|Full description of the KPI from the MPC specification|
|MPC UX Name|Display name for the KPI as shown in the MPC UI|
|MPC KPI Group|Top-level KPI grouping as defined in the MPC|
|MPC KPI Sub Group|Sub-grouping of the KPI within the MPC group|
|Formatted KPI Formula|Auto-populated. Do not enter a value manually.|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[MPN Formula Engine processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formula-engine.md)

