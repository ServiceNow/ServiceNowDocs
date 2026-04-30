---
title: Monitoring Technology Dashboard for HTTP
description: With the HTTP Monitoring Technology Dashboard you can monitor the response time of your http and https URLs. By using the dashboard, you can identify the URLs with the highest metric readouts in your system's infrastructure, and view the most recent active alerts on those URLs.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Understanding the Monitoring Technology Dashboard, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Monitoring Technology Dashboard for HTTP

With the HTTP Monitoring Technology Dashboard you can monitor the response time of your `http` and `https` URLs. By using the dashboard, you can identify the URLs with the highest metric readouts in your system's infrastructure, and view the most recent active alerts on those URLs.

## Monitoring Technology Dashboard for HTTP overview

The HTTP Monitoring Technology Dashboard shows the five URLs with the highest metric readouts during the past six hours. The dashboard also shows the 50 most recent active alerts on those URLs.

To view the dashboard, navigate to **All** &gt; **AIOps Dashboards** &gt; **Monitoring Technology Dashboards** and select **HTTP**.

## Using the Monitoring Technology Dashboard for HTTP

Before using the Monitoring Technology Dashboard for HTTP:

-   Ensure that you’re working in the Agent Client Collector Monitoring scope in your ServiceNow instance.
-   Ensure that the agent\_client\_collector\_admin and dashboard\_admin roles are enabled.
-   Enable Metric Intelligence on the MID Server.
-   Ensure that the **HTTP Entry Points Events** and **HTTP Entry Points Metrics** policies are enabled.

    Enabling these policies activates metric to CI mapping.

-   Ensure that the clotho plugin version 1.19.0.10 or above is enabled.
-   After upgrading from a previous version, follow the procedure described in the [ACC-M Dashboard Filters are not working when upgraded from Tokyo/Utah to Vancouver \[KB1438042\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1438042) article in the NOW Support Knowledge Base.

The Azure Monitoring Technology Dashboard contains the tabs that are listed in the following table.

|Tab|Description|
|---|-----------|
|Metrics|Displays the top 5 performing metrics that are associated with the URLs in your system.|
|Alerts|Displays the 50 most recent alerts that are associated with the URLs in your system. Alerts help you to remediate your system by providing information on problematic behavior.|

On the right side of widgets displaying a single metric, you can select the More options icon \(![More options icon](../image/three-vertical-icon.png)\) and select **Change group by**. Select the category you want to view the metric by: Host name, Class, Operating System, or OS Version.

Point to the relevant widget to view a specific datapoint and all of its details in a pop-up window.

Use the **Time range filter** to filter the time range for which you want metric data to display on the dashboard.

You can customize the appearance of the individual widgets on the HTTP Monitoring Technology Dashboard. For example, you could change the data parameters that display for the Response Time metric, like the time range that the response time is displayed. You can also include the customized widgets when you’re creating a custom dashboard. For more information, see [Customize the Monitoring Technology Dashboard](../task/customize-dashboard-widgets.md).

