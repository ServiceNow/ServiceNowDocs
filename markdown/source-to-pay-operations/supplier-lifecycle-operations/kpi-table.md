---
title: KPI table
description: The KPI \[sn\_kpi\_kpi\] table stores the important information about the KPIs created.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Primary data tables for SRPM, Supplier Relationship and Performance Management reference, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# KPI table

The KPI \[sn\_kpi\_kpi\] table stores the important information about the KPIs created.

## KPI \[sn\_kpi\_kpi\] table

The KPI \[sn\_kpi\_kpi\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Name|String|Name of the KPI.|
|Description|String|Brief description of the KPI.|
|Active|Boolean|Status of the KPI.|
|KPI Template|Reference|KPI Template used to create the KPI.|
|Supplier|Reference|Supplier for which this KPI is created.|
|Threshold set|Reference|Set of thresholds created for this KPI.|
|Domain|Reference|Performance domain of the KPI.|
|Type|Choice|Indicates the type of the KPI.|
|Nature|Choice|Indicates whether the KPI is leading \(predicts future\), lagging \(measures past performance\), or current \(monitors ongoing activities\).|
|Collected from user|Reference|The person who provides the data.|
|Weight|Integer|Determines the importance of the KPI in the overall performance score when multiple KPIs are collected.|
|Direction|Choice|Indicates whether the KPI should be minimized or maximised to show the ideal trend of the values.|
|Precision|Integer|Specifies the number of decimal points to be used for data collection to ensure accuracy and consistency.|
|Collection source type|Choice|The user persona that provides the data.|
|Unit|Reference|Measurement unit used to quantify the KPI.|
|Collection frequency|String|The frequency for collecting the KPI data.|
|Instructions|Translated html|Populated in KPI collection tasks to give more context to the user providing the KPI data.|
|Next run date|Date|Next scheduled run date of the KPI to collect the data.|
|Last collected date|Date|Latest date on which KPI data is collected.|
|Last period data|Reference|Latest KPI data.|
|Entity table|Table name|Table in which the entity belongs.|
|Entity Sys ID|Document ID|Sys ID of the entity.|

**Parent Topic:**[Primary data tables for Supplier Relationship and Performance Management \(SRPM\)](primary-data-tables-srpm.md)

**Related topics**  


[Create KPIs without using KPI template](../task/create-kpis.md)

[Create KPIs by adding suppliers to a KPI template](../task/add-supplier-kpi-template.md)

