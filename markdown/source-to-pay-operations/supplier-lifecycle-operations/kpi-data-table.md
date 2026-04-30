---
title: KPI Data table
description: The KPI \[sn\_kpi\_data\] table stores the collected data for all the KPIs.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Primary data tables for SRPM, Supplier Relationship and Performance Management reference, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# KPI Data table

The KPI \[sn\_kpi\_data\] table stores the collected data for all the KPIs.

## KPI Data \[sn\_kpi\_data\] table

The KPI Data \[sn\_kpi\_data\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|KPI|Reference|KPI to which this data belongs to.|
|Collection start date|Date|Collection interval start date.|
|Collection end date|Date|Collection interval end date.|
|State|Choice|State of the data.|
|Last period data|Reference|Previous data collected for the KPI.|
|Threshold set|Reference|Set of thresholds created for this KPI.|
|Domain|Reference|Performance domain of the KPI.|
|Type|Choice|Indicates the type of the KPI.|
|Nature|Choice|Indicates whether the KPI is leading \(predicts future\), lagging \(measures past performance\), or current \(monitors ongoing activities\).|
|Collected from user|Reference|The person who provides the data.|
|Weight|Integer|Determines the importance of the KPI in the overall performance score when multiple KPIs are collected.|
|Variance|Decimal|Variance between current data and previous data of the KPI.|
|Original value|String|Original value collected through the collection task.|
|Latest value|String|Latest value of the data.|
|Kpi value unavailable|Boolean|True if the value isn’t available for this interval.|
|Override value|Boolean|Checked to override the submitted KPI data.|
|Is overridden|Boolean|Indicates whether the data is overridden.|
|Justification|String|Reason for overriding the data.|

**Parent Topic:**[Primary data tables for Supplier Relationship and Performance Management \(SRPM\)](primary-data-tables-srpm.md)

**Related topics**  


[Create KPIs without using KPI template](../task/create-kpis.md)

[Create KPIs by adding suppliers to a KPI template](../task/add-supplier-kpi-template.md)

