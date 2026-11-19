---
title: Shopfloor insights indicators and visualizations
description: Reference information for the indicators, charts, and visualizations displayed on the Insights Overview tab for IGT standards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/igt-shopfloor-insights-indicators.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [shopfloor insights, indicators, visualizations]
breadcrumb: [Industrial Guided Tasks, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Shopfloor insights indicators and visualizations

Reference information for the indicators, charts, and visualizations displayed on the Insights Overview tab for IGT standards.

The Insights Overview tab displays a collection of indicators and visualizations that provide execution analytics for an IGT standard. These dashboard insights are provided by the Industrial Analytics and Reporting application. Line leaders, operators, and equipment owners can use these metrics to analyze performance and identify improvement opportunities.

**Note:** If scoring is not enabled, the indicator displays "0".

## Mapping visualization and indicators

The following table maps the performance data collected by indicators and the visualization displayed on the dashboard:

<table id="table_drp_wnz_33c"><thead><tr><th>

Visualization

</th><th>

Indicator

</th><th>

Description

</th><th>

Calculation

</th></tr></thead><tbody><tr><td>

Completed tasks \(%\)

</td><td>

% IGTs completed \(Formula indicator\)

</td><td>

Displays the percentage of IGTs that were completed out of all IGTs opened within the selected time period. Helps identify task completion trends and potential bottlenecks.

</td><td>

Uses the following Automated indicators: `([[IGT tasks completed]/[IGT tasks opened]]*100)`

</td></tr><tr><td>

Average score

</td><td>

Average score \(Automated indicator\)

</td><td>

Displays the average score across all executed IGTs within the selected time period. Only visible when scoring is enabled on the standard. When scoring is not enabled or the score value is 0, the visualization also displays the value as 0.

</td><td>

Average of total scores for executed IGTs

</td></tr><tr><td>

Tasks planned per status

</td><td>

Industrial Guided Tasks - Planned start \(Automated indicator\)

 % IGTs completed in time \(Formula indicator\)

</td><td>

Displays the percentage of IGTs that were completed within their planned timeframe. Helps track on-time performance and identify scheduling or execution issues.

</td><td>

Industrial Guided Tasks - Planned start \(Automated indicator\)

 % IGTs completed in time uses the following automated indicators: `([[Completed in time]/ [Industrial Guided Tasks - Planned start]]*100)`

</td></tr><tr><td>

Opened deviations

</td><td>

Opened deviations \(Automated indicator\)

</td><td>

Displays all deviations for tasks related to this standard that were opened on the last date of the selected time period.

</td><td>

Number of deviations opened in the last day of the selected time period.

</td></tr><tr><td>

Opened actions

</td><td>

Opened actions \(Automated indicator\)

</td><td>

Displays all actions for tasks related to this standard that were opened on the last date of the selected time period.

</td><td>

Number of actions opened in the last day of the selected time period.

</td></tr><tr><td>

Average task duration

</td><td>

Average task duration \(Automated indicator\)

</td><td>

Displays the average time taken to complete the IGT tasks. Calculated from when the task was moved to work in progress and when it is submitted.

</td><td>

Average of actual execution time.

</td></tr></tbody>
</table>**Parent Topic:**[Industrial Guided Tasks reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/industrial-guided-tasks-reference.md)

