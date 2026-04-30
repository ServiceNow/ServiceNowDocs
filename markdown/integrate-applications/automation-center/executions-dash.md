---
title: Automation Center Executions dashboard
description: The Automation Center Executions dashboard helps you manage the health of automations in one central place. You can also​ import automation metrics and data from third-party providers regardless of the technology used.
locale: en-US
release: xanadu
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Automation Center Workspace, Exploring Automation Center, Automation Center, Creating integrations with applications]
---

# Automation Center Executions dashboard

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

The following information is available on the Executions page:

-   **Execution summary by state**

    This chart displays the execution status of automations in different states. This information helps in understanding the status of the automations.

-   **Automation incidents**

    This chart provides information about any incidents that have a direct impact on the automations. For example, if five automations are on hold, this chart lets you know about those five automations. This information enables you to manage the automations better.

-   **Automation changes**

    This chart focuses on any change that has a direct impact on the automations.

-   **Business application changes**

    This chart provides information about any change to the business applications that are associated with the automations.

-   **Execution state over time**

    This chart provides information about the state of the executions for a time period. There’s a date range filter for this chart. If you select a date range, the data is limited to the selected date range, or else the default date range is selected, which is last one week.

-   **Execution summary**

    This chart displays the number of executions and their respective states sorted by automation name.


## Insights panel

The Insights panel provides information about insights, which draw your attention to any issues within Automation Center. You can fix the issues or choose to ignore them. If you delay fixing issues, some automations might not behave as expected.



![Insights example](../images/insights-widget.jpg)

**Parent Topic:**[Automation Center Workspace](automation-center-workspace-ui.md)

