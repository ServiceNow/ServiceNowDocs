---
title: KPI Threshold table
description: The KPI Threshold \[sn\_kpi\_threshold\] table stores the information about threshold values or value ranges configured for KPIs or KPI templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/kpi-threshold-table.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Primary data tables for SRPM, Supplier Relationship and Performance Management reference, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# KPI Threshold table

The KPI Threshold \[sn\_kpi\_threshold\] table stores the information about threshold values or value ranges configured for KPIs or KPI templates.

## KPI Threshold \[sn\_kpi\_threshold\] table

The KPI Threshold \[sn\_kpi\_threshold\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Name|String|Name of the KPI threshold.|
|Label|String|Label for the KPI threshold.|
|Description|String|Brief description of the KPI threshold.|
|Active|Boolean|Option that indicates the threshold is active for use.|
|Low Value|Integer|Represents the low value in the KPI threshold value range.|
|High Value|Integer|Represents the high value in the KPI threshold value range.|
|Normalized value|Integer|Indicates a value that has been calculated from its original figure to fit a specific scale for easy comparison with other values. For example, a scale of 1–5.|
|Color|String|Color for the threshold.|

**Parent Topic:**[Primary data tables for Supplier Relationship and Performance Management \(SRPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/primary-data-tables-srpm.md)

**Related topics**  


[Create KPI thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-kpi-threshold.md)

