---
title: Agent Health dashboard
description: The Agent Health dashboard provides visibility into the status and distribution of agents installed in your system. It allows you to quickly assess the number of deployed agents and their distribution, helping you prioritize your work more efficiently.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [AIOps Dashboards in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Agent Health dashboard

The Agent Health dashboard provides visibility into the status and distribution of agents installed in your system. It allows you to quickly assess the number of deployed agents and their distribution, helping you prioritize your work more efficiently.

The following example shows the agents in your system that are currently up, which agents are configured to collect data, and which agents have stopped data collection due to having reached their CPU threshold \(Silent/Off\). It also displays the agents according to their version, OS, and connected MID Server.

![Agent Health Dashboard](../image/agent-health-dashboard.png)

## Prerequisites

The Agent Client Collector application must be installed.

## Required ServiceNow AI Platform roles

A user must have the agent\_client\_collector\_admin role to see all the widgets in the dashboard.

## Access the Events and alerts dashboard

To open the dashboard, use one of the following methods:

-   Navigate to **All** &gt; **AIOps Dashboards** &gt; **AIOps Operational** &gt; **Agent Health**.
-   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the AIOps Dashboards icon \(![AIOps Dashboards icon.](../../health-log-analytics-admin/image/aiops-operational-icon.png)\) and then select the **Agent Health** tab.
-   After upgrading to Discovery Admin Workspace version 1.3.1 \(August 2024 Store\), you can navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** and use the enhanced dashboard.


## Use case

For examples of how different people in your organization would use this dashboard, see the use case in the following table.

|User|Dashboard use|
|----|-------------|
|admin|Visibility into the status of the agents.|

## Breakdowns

Breakdowns available in the Agent Health are:

-   Agent status: The status of the agents currently deployed in your system.
-   Agent distribution: The distribution of the agents by the agent version number, the MID Server that the agent is assigned to, and the OS that the agent is working on.

## Reports

<table id="table_yyl_b4z_xxb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent status breakdown

</td><td>

Pie chart

</td><td>

Agents deployed in your system that are up and down. Select the relevant color in the widget to display a list of up or down agents.

</td></tr><tr><td>

Agent by data collection status

</td><td>

Pie chart

</td><td>

Agents deployed in your system with data collection turned on and off. Select the relevant color in the widget to display a list of agents with data collection on or off.

</td></tr><tr><td>

Silent/Off \(auto\) agents

</td><td>

Line graph

</td><td>

Agents that automatically stopped collecting data after crossing the CPU usage threshold. The CPU usage threshold is configurable in the `acc.yml` configuration file.

 For more information on the `acc.yml` configuration file, see [Configuration file options](../../agent-client-collector/reference/acc-yml-options.md).

</td></tr><tr><td>

Agent by version

</td><td>

Bar chart

</td><td>

Breakdown of your deployed agents by their version numbers.

</td></tr><tr><td>

Agent by MID Server

</td><td>

Bar chart

</td><td>

Breakdown of the deployed agents according to the MID Server they're assigned to.

</td></tr><tr><td>

Agent by OS

</td><td>

Bar chart

</td><td>

Breakdown of your deployed agents according to the operating systems they are working on.

</td></tr></tbody>
</table>