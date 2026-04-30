---
title: KPI Template table
description: The KPI Template \[sn\_kpi\_template\] table stores the configurations required to create KPIs.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Primary data tables for Supplier Relationship and Performance Management \(SRPM\), Supplier Relationship and Performance Management reference, Supplier Lifecycle Operations reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# KPI Template table

The KPI Template \[sn\_kpi\_template\] table stores the configurations required to create KPIs.

## KPI Template \[sn\_kpi\_template\] table

The KPI Template \[sn\_kpi\_template\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Name|String|Name of the KPI template.|
|Description|String|Brief description of the KPI template.|
|Active|Boolean|Status of the KPI template.|
|Threshold set|Reference|Set of thresholds created for this template.|
|Domain|Reference|Performance domain of the template.|
|Type|Choice|Indicates the type of the KPI template.|
|Nature|Choice|Indicates whether the KPI is leading \(predicts future\), lagging \(measures past performance\), or current \(monitors ongoing activities\).|
|Collected from user|Reference|The person who provides the data.|
|Recommended weight|Integer|Determines the importance of the KPI in the overall performance score when multiple KPIs are collected.|
|Supplier count|Integer|Total number of suppliers added to the KPI template.|
|Direction|Choice|Indicates whether the KPI should be minimized or maximised to show the ideal trend of the values.|
|Precision|Integer|Specifies the number of decimal points to be used for data collection to ensure accuracy and consistency.|
|Template owner|Reference|The person who owns the KPI template.|
|Collection source type|Choice|The user persona that provides the data.|
|Unit|Reference|Measurement unit used to quantify the KPI.|
|Collection frequency|String|The frequency for collecting the KPI data.|
|Instructions|Translated html|Populated in KPI collection tasks to give more context to the user providing the KPI data.|

**Parent Topic:**[Primary data tables for Supplier Relationship and Performance Management \(SRPM\)](primary-data-tables-srpm.md)

**Related topics**  


[Create manual KPI templates](../task/create-kpi-template-slo.md)

