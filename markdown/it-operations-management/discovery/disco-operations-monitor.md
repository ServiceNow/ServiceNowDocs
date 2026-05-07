---
title: Discovery Operations Monitor dashboard
description: The Discovery Operations Monitor dashboard displays performance metrics for your Discovery environment. Use this dashboard to monitor discovery health and identify issues across your IT landscape.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Operations Monitor dashboard

The Discovery Operations Monitor dashboard displays performance metrics for your Discovery environment. Use this dashboard to monitor discovery health and identify issues across your IT landscape.

To access the dashboard, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Discovery Operations Monitor**. You can also access this dashboard from the Discovery Admin Workspace Home page.

![Discovery Operations Monitor dashboard](../image/disco-op-monitor.png)

## Required ServiceNow AI Platform roles

-   discovery\_admin
-   admin

## Prerequisites

-   **Verify that you have the required setup**
    -   Discovery.
    -   Discovery Admin Workspace 1.15.0.

## Key features

The Discovery Operations Monitor dashboard displays visuals for discovery performance data.

**Note:** Metrics are collected for the most recently completed 15-minute window. Data may not reflect activity from the current interval until collection has run. For more information, see [Configure the time interval for a Discovery Operations Monitor visualization](../task/config-interval-disco-op-mon.md).

Select the info icon \(![](../image/daw-info-icon.png)\) to view dashboard details, such as the owner and usage. Select the **More options** icon \(![](../../health-log-analytics-admin/image/more-options.png)\) to duplicate, share, export, schedule, or print the dashboard. Select **Edit** to access editing mode, where you can update the data source and visualization settings. For more information about editing dashboards, see [Common dashboard tasks in the in-line editor](https://www.servicenow.com/docs/access?context=common-dashboard-tasks&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\) on a visualization to export it in CSV, JPEG, PNG, or Excel format.

|Report title|Type|Description|
|------------|----|-----------|
|Transaction Duration|Line chart|Displays discovery transaction duration compared to overall system transaction duration over time. Use this chart to identify discovery-specific spikes or anomalies relative to system activity. Select a record to view the related transactions.|
|Sensor Jobs by Schedule|Bar chart|Displays the count of discovery sensor jobs over time, stacked by schedule. Use this chart to identify which schedules contribute most to sensor job load.|
|MID Server Queue Load|Line chart|Displays ECC queue volume over time for MID Servers associated with discovery. Metrics are tracked separately for each MID Server. Select a record to view the ECC queue records.|
|MID Server Average Probe Time|Line chart|Displays the average ECC probe processing time in seconds over time. Select a record to view the related ECC queue records.|
|Discovery Event Load|Bar chart|Displays the volume of discovery events over time. The chart tracks four event types: discovery.error, discovery.device.complete, discovery.complete, and discovery.canceled. Select a record to view related events.|

**Note:** The dashboard displays data from the last 7 days by default. Data is retained for 30 days. For more information, see [Configure the date range for a Discovery Operations Monitor visualization](../task/config-time-frame-disco-op-mon.md).

