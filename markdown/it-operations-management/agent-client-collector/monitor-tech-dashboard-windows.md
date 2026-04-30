---
title: Monitoring Technology Dashboard for Windows
description: With the Windows Monitoring Technology Dashboard, you can monitor the health and performance of your Windows infrastructure. The dashboard enables you to identify the CIs and servers in your system with the highest resource consumption, and also the most recent active alerts.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Understanding the Monitoring Technology Dashboard, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Monitoring Technology Dashboard for Windows

With the Windows Monitoring Technology Dashboard, you can monitor the health and performance of your Windows infrastructure. The dashboard enables you to identify the CIs and servers in your system with the highest resource consumption, and also the most recent active alerts.

## Overview of the dashboard

The Monitoring Technology Dashboard for Windows shows the five CIs and servers with the highest metric readouts during the past six hours. The dashboard also shows the 50 most recent active alerts on your OS's servers.

To view the dashboard, navigate to **All** &gt; **AIOps Dashboards** &gt; **Monitoring Technology Dashboards** and select **Windows Server**.

## Using the Monitoring Technology Dashboard for Windows

Before using the Monitoring Technology Dashboard for Windows:

-   Ensure that you’re working in the Agent Client Collector Monitoring scope in your ServiceNow instance.
-   Ensure that the agent\_client\_collector\_admin and dashboard\_admin roles are enabled.
-   Enable Metric Intelligence on the MID Server.
-   Ensure that the **Windows OS Events** and **Windows OS Metrics** policies are enabled:

    Enabling these policies activates metric to CI mapping.

-   Ensure that the clotho plugin version 1.19.0.10 or above is enabled.
-   After upgrading from a previous version, follow the procedure described in the [ACC-M Dashboard Filters are not working when upgraded from Tokyo/Utah to Vancouver \[KB1438042\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1438042) article in the NOW Support Knowledge Base.

To view the dashboard, navigate to **All** &gt; **AIOps Dashboards** &gt; **Monitoring Technology Dashboards** and select **Windows Server**.

Point to the relevant widget to view a specific point of data and all of its details in a pop-up window. Select the Alerts tab to view the 50 most recent active alerts for CIs.

You can filter the dashboard data according to the following filters:

|Filter name|Description|
|-----------|-----------|
|Time range filter|The time range for which you want metric data to display on the dashboard.|
|Metrics by selected CI filter|The CIs for which you want metric data to display on the dashboard.|
|Metrics by selected OS filter|The OS for which you want metric data to display on the dashboard.|

On the right side of widgets displaying a single metric, you can select the More options icon \(![More options icon](../image/three-vertical-icon.png)\) and select **Change group by**. Select the category that you want to view the metric by: Host name, Class, Operating System, or OS Version.

## Windows server dashboard

![Windows Server dashboard](../image/monitor-tech-dash-windows.png)

The Metrics subtab displays the top five performing CIs and servers over the past six hours, according to the following metrics.

-   Processor Queue Length
-   CPU Load
-   System Uptime
-   CPU Core
-   RAM Usage
-   Network Bandwidth
-   Memory Distribution
-   Network Flow
-   Disk Usage
-   Disk Read/Write
-   Disk Distribution

You can customize the appearance of the individual widgets on the Windows Monitoring Technology Dashboard. For example, you could change the timeframe for which the alerts appear. You can also include customized widgets when you are creating a custom dashboard. For more information, see [Customize the Monitoring Technology Dashboard](../task/customize-dashboard-widgets.md).

