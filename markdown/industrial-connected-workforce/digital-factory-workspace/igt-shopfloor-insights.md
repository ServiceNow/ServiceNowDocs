---
title: Shopfloor insights for Industrial Guided Tasks
description: Shopfloor insights provide embedded execution analytics on Industrial Guided Tasks \(IGT\) standards to support continuous improvement of manufacturing processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/igt-shopfloor-insights.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [shopfloor insights, Industrial Guided Tasks, continuous improvement]
breadcrumb: [Industrial Guided Tasks, Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Shopfloor insights for Industrial Guided Tasks

Shopfloor insights provide embedded execution analytics on Industrial Guided Tasks \(IGT\) standards to support continuous improvement of manufacturing processes.

## Shopfloor insights overview

Shopfloor insights enable line leaders and operators to view execution analytics directly on each IGT standard record in the Digital Factory Workspace. By analyzing standard execution data, you can uncover performance gaps, develop strategies to prevent deviations, and gather insights to improve standards. This capability supports the continuous improvement of manufacturing standards and operational efficiency.

Shopfloor insights are displayed in an embedded overview tab on every IGT standard record in Workspace. Each indicator on the dashboard shows data related to the published standard, enabling you to see all execution results across versions.

The data is trended and aggregated based on the shift configuration of the linked functional location or their parent functional. The data is aggregated based on the following sequence:

1.  Data collection is performed on the first functional location
2.  If no shift configuration is available for the first functional location, it checks the parent functional location.
3.  If no shift configuration is available for the parent functional location, the system checks the next functional location. This process repeats until the system finds a shift configuration or reaches the end of the functional location sequence.

In case none of the functional locations of the standard has a shift configuration, data available from the selected time period on a standard calendar is automatically aggregated.

**Note:** The Insights Overview tab is not visible when the standard is in Draft or Review state. The dashboard displays the standard overview of the published standard.

## Data aggregation

Shopfloor insights aggregate data based on the time filter selection and the shift configuration of the functional location:

-   Month: Data is aggregated according to the default standard calendar.
-   Daily: Data is aggregated by shift according to the shift configuration for a functional location.

## Shopfloor insights benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Identify performance gaps in standards by analyzing execution data. Take action to prevent deviations and improve operational efficiency.|Continuous improvement|Line leader, Equipment owner|
|Compare IGT execution across shifts to analyze variance and take action accordingly. Shorten PDCA cycles for standard improvements.|Shift-based comparison|Line leader|
|Access embedded analytics without switching applications. Configure dashboards to show KPIs that matter most for your factory.|Embedded analytics|Line leader, Operator|
|Monitor follow-up tasks including actions and deviations to identify trends and take corrective action.|Follow-up tracking|Line leader, Equipment owner|

**Parent Topic:**[Exploring Industrial Guided Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/exploring-industrial-guided-tasks.md)

**Related topics**  


[Exploring Industrial Analytics and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/exploring-industrial-analytics-and-reporting.md)

