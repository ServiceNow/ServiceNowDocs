---
title: FDIH Dashboard
description: Use a single dashboard to view usage, execution, and debug information for Workflow Studio and Integration Hub transactions. Open links to related Workflow Studio properties, logs, events, and editors.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Flow administration, Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# FDIH Dashboard

Use a single dashboard to view usage, execution, and debug information for Workflow Studio and Integration Hub transactions. Open links to related Workflow Studio properties, logs, events, and editors.

With the FDIH Dashboard, you can manage and see the status of Workflow Studio and Integration Hub transactions. Access to the dashboard is role-based.

The dashboard is divided into six sections.

-   **FDIH Dashboard header**

    View the state of flow reporting and the log level being replicated to the flow logs. Use links to open the system properties table, the system logs, the outbound HTTP logs, Workflow Studio propertgies, and flow settings.

-   **Flow Usage**

    View the number of flows run and their state over various time periods. For example, you can view the flow executions in the complete state over the last 14 days. Use links to Workflow Studio, system properties, event handlers, and flow settings to manage how flows are run.

-   **IH Usage**

    View Integration Hub transactions and features used over the last month. For example, you can view the top spokes used over the last month.

-   **Flow Executions**

    View a list of flow executions by creation date. View information about flow, its runtime duration, state, calling source, and associated application. For example, you can filter flows by calling source to see which ones have been tested recently.

-   **MID Executions**

    View Integration Hub probes that ran on a MID Server. View information about the agent, source, topic, queue, state, and processing state. For example, you can filter probes run by source of queue. Use links to see MID Server queues sorted by source and available MID Servers.

-   **Debug**

    View a list of flow jobs in the ready state that are waiting to run. Identify flows that need manual intervention or redesign to complete. For example, use the list of waiting flows to identify a performance issue.


There's no specific order in which you must view the reports, set filters, or customize the columns in the report tables.

The following example shows how the dashboard data is organized into sections, charts, filters, and graphs. The filters enable you to drill beyond a chart or a graph to view more detailed data.

![Sample data of top 10 flow runs.](../images/fdih-dashboard-flow-usage-example.png "FDIH Dashboard showing sample flow usage")

-   **[Get insights from the FDIH Dashboard](../task/get-insights-fdih-dashboard.md)**  
Use the FDIH Dashboard to get insights on flow executions and historical performance.

**Parent Topic:**[Flow administration](flow-administration.md)

