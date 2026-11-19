---
title: SQDC Analytics Overview dashboard indicators
description: Reference information for the indicators and visualizations displayed on the SQDC Analytics Overview dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/sqdc-overview-indicators.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-05-17"
reading_time_minutes: 1
keywords: [SQDC Analytics, Overview indicators, OEE, safety incidents, losses]
breadcrumb: [Industrial Analytics and Reporting, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# SQDC Analytics Overview dashboard indicators

Reference information for the indicators and visualizations displayed on the SQDC Analytics Overview dashboard.

The Overview dashboard displays a set of single-score indicators and time-based visualizations that summarize SQDC performance for the selected functional location. All values refresh when you change the period at the top of the dashboard.

## Single-score indicators

|Indicator|Description|Data source|Calculation|
|---------|-----------|-----------|-----------|
|OEE|Displays the current Overall Equipment Effectiveness percentage with a target of 70%. As a production manager, you can use OEE to monitor the combined effect of availability, performance, and quality.|`sn_icw_loss_process_metric_value` where the measurement definition is `OEE`|Manual measurement value in percent|
|Safety incidents|Displays the total number of safety incidents for the selected period and a trend indicator that shows the change since the start of the period.|Safety incident records|Total count of safety incidents in the selected period|
|Standard task completion|Displays the percentage of completed Industrial Guided Tasks and a trend indicator that shows the change since the start of the period.|`sn_icw_standard_task`|`(Standard tasks completed / Standard tasks created) * 100`|

## Production and loss visualizations

|Visualization|Description|Chart type|Data source|
|-------------|-----------|----------|-----------|
|Products Planned vs. Actual|Compares daily planned production, actual production, and the calculated loss between them. As a production manager, you can use this view to identify daily shortfalls and adjust resource allocation.|Time-based column chart|Measurement definitions for planned and actual production|
|Losses by category|Ranks loss categories in descending order by total loss. As an Operations manager, you can use this view to identify the highest-impact loss drivers and prioritize improvement initiatives.|Pareto chart|Loss events of type Losses and any measurement type marked as a loss|
|Losses by period|Displays total loss duration in minutes for the selected period, broken down by loss category. Includes minimum and maximum reference lines for context.|Stacked column time-series chart|Loss events of type Losses and any measurement type marked as a loss|

**Parent Topic:**[Reference for Industrial Analytics and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/reference-for-industrial-analytics-and-reporting.md)

