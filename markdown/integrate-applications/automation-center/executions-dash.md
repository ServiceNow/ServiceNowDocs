---
title: Automation Center Executions dashboarb
description: The Automation Center Executions dashboard helps you manage the health of automations in one central place. You can also​ import automation metrics and data from third-party providers regardless of the technology used.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workspace, Explore, Automation Center, Workflow Data Fabric]
---

# Automation Center Executions dashboarb

The Automation Center Executions dashboard helps you manage the health of automations in one central place. You can also​ import automation metrics and data from third-party providers regardless of the technology used.

Executions refer to the times each automation runs.

You can access the Executions dashboard in either of two ways:

-   By navigating to **All** &gt; **Automation Center** &gt; **Automation Center Home** and then selecting the **Executions** tab.
-   By navigating to **Workspaces** &gt; **Automation Center Workspace** &gt; **Executions**.

## Executions dashboard details

The Executions dashboard provides the details about the automation executions in the form of charts and tables. These charts give an overview of the entire execution process.

You can filter all data that is displayed on this page using the four filters available:

-   Department
-   Automation
-   Source
-   Application

If you don’t specify any filter, then all available data is displayed.

**Note:** To view the Automation incidents, Automation changes, and Business application changes widgets, in addition to the Automation Center roles you need to have the itil or sn\_incident\_read and sn\_change\_read roles.

<table id="id_ojr_yyl_c2c"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution summary by state

</td><td>

This chart displays the execution status of automations in different states. This information helps in understanding the status of the automations.![Execution summary by state](../images/exe-summ-1.png)

</td></tr><tr><td>

Automation incidents

</td><td>

This chart provides information about any incidents that have a direct impact on the automations. For example, if five automations are on hold, this chart lets you know about those five automations. This information enables you to manage the automations better.![Automation incidents](../images/exe-summ-2.png)

</td></tr><tr><td>

Automation changes

</td><td>

This chart focuses on any change that has a direct impact on the automations.![Automation changes](../images/exe-summ-3.png)

</td></tr><tr><td>

Business application changes

</td><td>

This chart provides information about any change to the business applications that are associated with the automations.![Business application changes](../images/exe-summ-4.png)

</td></tr><tr><td>

Execution state over time

</td><td>

This chart provides information about the state of the executions for a time period. There’s a date range filter for this chart. If you select a date range, the data is limited to the selected date range, or else the default date range is selected, which is last one week.![Execution state over time](../images/exe-summ-5.png)

</td></tr><tr><td>

Execution summary

</td><td>

This chart displays the number of executions and their respective states sorted by automation name.![Execution summary](../images/exe-summ-6.png)

</td></tr></tbody>
</table>## Transaction summary

The Transaction summary section displays execution details of the spokes for the last 24 hours.

|Section|Description|
|-------|-----------|
|Active applications|Displays the number of active applications running in your instance for the last 24 hours.![Active applications](../images/exe-summ-tran-1.png)|
|Actions in use|Displays the number of actions that are used in your instance in the last 24 hours.![Actions in use](../images/exe-summ-tran-2.png)|
|Total transactions|Displays the total number of transactions in your instance in the last 24 hours.![Total transactions](../images/exe-summ-tran-3.png)|
|In progress and failed transactions by flow|Displays all the in progress and failed transactions by flow in your instance in the last 24 hours.![In progress and failed transactions by flow](../images/exe-summ-tran-4.png)|
|Flow execution status trends|Displays the flow execution trend for all states in your instance in the last 24 hours.![Flow execution status trends](../images/exe-summ-tran-5.png)|

## Insights panel

The Insights panel provides information about insights, which draw your attention to any issues within Automation Center. You can fix the issues or choose to ignore them. If you delay fixing issues, some automations might not behave as expected.



![Insights example](../images/insights-widget.jpg)

**Parent Topic:**[Automation Center Workspace](automation-center-workspace-ui.md)

