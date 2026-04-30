---
title: Using the Field Service Safety dashboard
description: Review the status of agents, tasks, and assets using the Field Service Management Covid19 map. Monitor the compliance reports of agents through the Field Service Safety dashboard.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting for Field Service Management, Field Service Management]
---

# Using the Field Service Safety dashboard

Review the status of agents, tasks, and assets using the Field Service Management Covid19 map. Monitor the compliance reports of agents through the Field Service Safety dashboard.

**Important:** Starting with the Xanadu release, the Field Service Safety dashboard is removed from the Emergency Exposure Management app. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Users with the wm\_manager role can use the Field Service Safety dashboard to monitor whether agents are compliant with the safety protocols of possible exposure to an infectious disease while performing tasks. The Covid19 map displays the impact of COVID-19 on the locations that are covered by the agents, tasks, and assets of an individual Field Service manager.

To see the FSM Covid19 map on your Field Service Safety dashboard, install the free COVID-19 Global Health Data Set application.

## COVID-19 Global Health Data Set

You can use the COVID-19 Global Health Data Set application to see the Field Service Management Covid19 map on your Field Service Safety dashboard. The application appears as an application in the instance navigation menu. It displays global COVID-19 information on request in the Field Service Safety dashboard. The **COVID-19 Data Feed - pre-sync** and **COVID-19 Data Feed - sync central instance, Daily Data Collection** scheduled jobs run every night to refresh the data.

## Using the Field Service Safety dashboard

Navigate to **Field Service** &gt; **Safety Dashboard**.

![Field Service Safety Map that displays COVID-19 alert locations by date range. A dashboard with task compliance by agents and the number of non-compliant agents, and working agents is displayed.](../../../use/dashboards/image/safety_dashboard.png "Field Service Safety Dashboard with COVID-19 data")

Locations with alerts are listed on the FSM Covid19 map. Use the map controls as follows:

-   To zoom in to a location and its alerts, click the location icon \(![COVID-19 alert location marker.](../image/marker-wot-unassigned-multiple-clear.svg) \).
-   To select a time period to review, use the Task Date Range at the top left.
-   To filter the information displayed on the map, click the layers icon \(![Layers icon to select filters.](../../../use/dashboards/image/layers-map.png)\) on the top right and select your filters.

Each icon displays the information in the following table.

<table id="table_sr2_ymm_1mb"><thead><tr><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task

</td><td>

Tasks for the locations that are covered by the logged-in field service manager. -   To display the task number and short description, click the task marker.
-   To review task details, click the task number.

</td></tr><tr><td>

Assets

</td><td>

The installed or available assets at the locations that are covered by the logged-in field service manager. -   To display the name and company name of the asset, click the asset marker.
-   To review asset details, click the asset name.

</td></tr><tr><td>

Agent

</td><td>

Managed by the logged-in field service manager. -   To display the agent's name and mobile number, click the agent marker.
-   To review agent details, click the agent name.

</td></tr></tbody>
</table>## Reports

Managers can view the task compliance result of their agents based on the date, such as tasks performed by the agents in the last 30 days and so on. Click any area of a chart to see the corresponding records.

|Chart|Description|
|-----|-----------|
|My Non-Compliant Agents|The number of agents who completed their tasks without following the safety protocols within the selected date range. Click the metrics to view the list of non-compliant tasks.|
|My Working Agents|The number of agents working on at least one task and reporting to the logged-in field service manager. Click the metrics to view the list of their compliant and non-compliant tasks.|
|Task Compliance by my Agents|The breakdown of compliant and non-compliant tasks by each agent within the selected date range. Click a section to view the list of tasks.|

**Parent Topic:**[Analytics and reporting for Field Service Management](analytics-reporting-fsm.md)

