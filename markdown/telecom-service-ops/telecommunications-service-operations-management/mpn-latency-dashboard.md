---
title: MPN Latency Dashboard
description: Monitor UE-to-switch latency and related KPIs across MPN-connected devices, with combined and per-KPI trend views, an instance summary table, and a last-recorded-value panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/mpn-latency-dashboard.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 2
keywords: [Nokia MPN]
breadcrumb: [Fault Management: Events and alerts, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# MPN Latency Dashboard

Monitor UE-to-switch latency and related KPIs across MPN-connected devices, with combined and per-KPI trend views, an instance summary table, and a last-recorded-value panel.

## Access the MPN Latency Dashboard

Access the MPN Latency Dashboard by navigating to **All** &gt; **Platform Analytics &gt; Dashboards** and searching for or selecting MPN Latency Dashboard.

## Average Latency for All KPIs

The **Average Latency for All KPIs** panel is a combined time-series chart showing all three latency KPIs together, in 30-second buckets. Filter the chart by Assurance ID, Instance, or DNN.

|Title|Type|Description|
|-----|----|-----------|
|Average Latency for All KPIs|Combined time-series chart|The average value of all three latency KPIs \(`collector2ue`, `collector2sw`, `ue2sw`\) over time, in 30-second buckets, filterable by Assurance ID, Instance, or DNN|

## Per-KPI trend views

Three separate panels, one per latency KPI, each showing the trend in 2-minute buckets with legends by DNN and Instance.

|Title|Type|Description|
|-----|----|-----------|
|Collector-to-UE latency|Time-series chart|Trend of the `collector2ue` KPI, in 2-minute buckets, with legends by DNN and Instance|
|Collector-to-switch latency|Time-series chart|Trend of the `collector2sw` KPI, in 2-minute buckets, with legends by DNN and Instance|
|UE-to-switch latency|Time-series chart|Trend of the derived `ue2sw` KPI, in 2-minute buckets, with legends by DNN and Instance|

## Additional Info

The **Additional Info** table lists latency data by instance, sorted by Instance.

|Column|Description|
|------|-----------|
|Instance|The instance identifier|
|Customer|The customer associated with the instance|
|opCo|The operating company associated with the instance|
|Assurance ID|The assurance identifier for the instance|
|DNN|The data network name associated with the instance|
|Product|The product associated with the instance|
|Vendor|The vendor associated with the instance|
|Last value of Latency|The most recently recorded latency value for the instance|
|KPI|The latency KPI the row's value belongs to|

## Instances with Latency \(Last Recorded Value\)

The **Instances with Latency \(Last Recorded Value\)** panel shows the most recently recorded latency value for each instance.

## Understanding data gaps

TSOM flags or logs a latency metric as stale when the latest published value for a CI is older than expected, rather than silently displaying it as current. If a switch-side record is missing for a DNN during a collection cycle, the `ue2sw` calculation is skipped for that cycle. This may appear as a gap in the dashboard panels before rather than a repeated or estimated value.

**Related topics**  


[MPN latency KPIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-latency-kpis.md)

[SD-WAN Alerts Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/sd-wan-alerts-dashboard.md)

