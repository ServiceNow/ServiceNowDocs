---
title: Use the Workflow Operations Dashboard
description: On the Workflow Operations Dashboard, view and add widgets to help you monitor workflows. Review the performance of workflows and determine which workflows must be improved.Multiple gauges are available to help you review the performance of workflows. You can add these gauges to the Workflow Operations Dashboard or custom homepages.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use the Workflow Operations Dashboard

On the Workflow Operations Dashboard, view and add widgets to help you monitor workflows. Review the performance of workflows and determine which workflows must be improved.

## Before you begin

Role required: workflow\_admin

The different levels of access are:

-   **View**: View the dashboard and refresh report widgets.
-   **Customize**: Refresh, add, delete, and rearrange widgets.

## About this task

**Important:** As of the Zurich release, new customers no longer receive the legacy workflows created and published by ServiceNow, Inc.. All legacy workflow functionality has been replaced by Workflow Studio content. Only customers who upgraded from prior versions retain the ability to use and edit existing legacy workflows. While all customers retain the ability to create legacy workflows, you are strongly encouraged to instead use Workflow Studio to create process automation content. Only Workflow Studio will receive new features and enhancements.

On the Workflow Operations Dashboard, you can click widget elements to view the records they represent. You can also add new report widgets that are not displayed by default.

## Procedure

1.  View the Workflow Operations Dashboard by navigating to **Workflow** &gt; **Operations** &gt; **Workflow Operations Dashboard**.

    The default reports on the dashboard include:

    -   Workflow contexts providing run time metrics
    -   Active workflows started during a specified time period
    -   Workflows run between yesterday and today
    -   Workflows by state for the current month
    -   Aged workflow contexts for the past month
2.  Find and add more widgets by selecting the add content icon \(![Add Content icon.](../../../use/homepages/image/AddContent.png)\) in the corner of the dashboard.


## What to do next

If a workflow consistently appears as an outlier and there is no error causing the run time values, you can use its historical run time values to calculate a new estimated run time value. Then update the estimated run time in the workflow properties.

## Workflow gauges

Multiple gauges are available to help you review the performance of workflows. You can add these gauges to the Workflow Operations Dashboard or custom homepages.

**Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Overview dashboards take over homepage functionality.

Use the [Homepage deprecation help tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/homepage-deprecation-help-tool.md) to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   [Dashboards in the Analytics Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-dashboards.md).
-   [Working with responsive dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_ResponsiveDashboards.md).

|Content|Description|
|-------|-----------|
|**ERT Dashboard Controls** &gt; ****|
|Outlier Finished Workflows for ERT \(Percentage Outlier\)|Identifies workflows that finished, but did not finish within estimated runtime \(ERT\) values. Enter an outlier percentage to see workflows that ran outside the specified runtime range.|
|Outlier Long Running Workflows for ERT \(Percentage Outlier\)|Displays workflows running longer than the configured runtime threshold.|
|**Workflow Dashboard** &gt; ****|
|Workflows Without Current Record|Displays workflow contexts that do not have an associated current record.|
|**Gauges** &gt; **Workflow Context**|
|Number of Active Workflows Started Hourly Over Time \(Yesterday\)|Displays the total number of running workflows per hour over a given time period. By default, it displays the number of workflows that ran per hour over the previous day \(yesterday\).|
|Outlier Finished Workflows Not Cumulated to ERT|Displays workflow contexts that are finished outside the estimated runtime outlier value and not cumulated to estimated run time value.|
|Running Workflow Contexts|Displays the total number of running workflows.|
|Successfully Finished Workflows Cumulated to ERT|Displays the total number of successfully completed workflows whose running duration is cumulated to the estimated run time value.|
|Workflows by State \(This Month\)|Displays the total number of workflows run in a month grouped by the current state.|
|Aged Workflow Contexts \(Running Since Last Month\)|Displays the total number of workflow contexts running for a given period of time by workflow name. By default, it displays the total number of workflow contexts running over the last month.|
|Workflows Run Between Yesterday and Today \(by Table\)|Displays workflows that have run in the last day grouped by table name.|

