---
title: SQDC Analytics Delivery dashboard indicators
description: Reference information for the indicators and visualizations displayed on the SQDC Analytics Delivery dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/sqdc-delivery-indicators.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-05-17"
reading_time_minutes: 2
keywords: [SQDC Analytics, Delivery indicators, IGT completion, CIL, deviations, RCA aging]
breadcrumb: [Industrial Analytics and Reporting, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# SQDC Analytics Delivery dashboard indicators

Reference information for the indicators and visualizations displayed on the SQDC Analytics Delivery dashboard.

The Delivery dashboard displays single-score indicators and visualizations that summarize delivery performance for the selected functional location. All values refresh when you change the period at the top of the dashboard.

## Single-score indicators

|Indicator|Description|Data source|Calculation|
|---------|-----------|-----------|-----------|
|IGT completion|Displays the percentage of Industrial Guided Tasks completed against the total created in the selected period. Refreshes when task status changes.|`sn_icw_standard_task` with a breakdown on `task_type=IGT`.|`(Completed IGTs / Total created IGTs) * 100`|
|CIL completion|Displays the percentage of Cleaning, Inspection, and Lubrication \(CIL\) tasks completed on time and verified within the selected period.|`sn_icw_standard_task` with a breakdown on `task_type=IGT` and standard category `CIL`.|`(Completed CILs / Total required CILs) * 100`|
|Action completion SLA|Displays the average time to close actions within the selected period. Only closed or completed actions are included.|`sn_icw_action`|Average of the duration field across closed actions|
|Planned vs. Actual production|Displays the current production performance as a percentage of actual production against the planned target.|`sn_icw_measurement_record` with definitions for planned and actual production.|`(Actual production / Planned production) * 100`|
|Root cause analysis aging|Displays the average age of open root cause analysis \(RCA\) records in days. Plant managers and quality leads use this view to identify RCAs that need attention.|`sn_icw_rca` where type is not Breakdown and the record is not yet closed or verified.|Average age of open RCAs in days|
|Breakdown analysis aging|Displays the average age of open breakdown analysis records in hours.|`sn_icw_rca` where type is Breakdown and the record is not yet closed or complete.|Average age of open breakdown analysis in hours.|

## Deviation, loss, and waste visualizations

|Visualization|Description|Chart type|Data source|
|-------------|-----------|----------|-----------|
|Deviations|Displays deviation volume and aging trends. Bars show found, scheduled, fixed, and closed deviations. Lines show the average age of open deviations and the average age of fixed deviations.|Multi-axis time-series chart|`sn_icw_deviation`|
|Loss by period|Displays daily loss duration in minutes, broken down by loss category. The X-axis is the date and the Y-axis is duration in minutes.|Stacked column chart|`sn_icw_loss_industrial_loss` grouped by category|
|Unplanned downtime|Displays daily unplanned downtime duration in minutes, broken down by subcategory. Includes minimum and maximum reference lines.|Stacked column time-series chart|`sn_icw_loss_industrial_loss` where category is Unplanned downtime, grouped by subcategory|
|Breakdown by state|Displays the total number of breakdowns and the distribution across lifecycle states Open, Scheduled, Fixed, and Closed.|Donut chart|`sn_icw_deviation` where `task_classification=breakdown`|
|Total waste and scrap|Displays waste and scrap quantities in kilograms as stacked columns and the corresponding cost impact as a line on the secondary axis. Plant managers use this view to monitor material losses.|Combo chart \(stacked columns and line\)|`sn_icw_loss_process_metric_value` for Scrap, Startup scrap, Waste, and Rework required definitions with cost impact from `sn_icw_loss_industrial_loss`|
|Average RCA aging per state|Displays the average RCA aging in hours, broken down by RCA state over time.|Multi-line time-series chart|`sn_icw_rca` grouped by state|

**Parent Topic:**[Reference for Industrial Analytics and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/reference-for-industrial-analytics-and-reporting.md)

