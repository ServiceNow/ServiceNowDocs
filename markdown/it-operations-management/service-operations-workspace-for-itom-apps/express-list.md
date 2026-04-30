---
title: Express List in the Service Operations Workspace for ITOM
description: The ServiceNow Event Management Express List feature helps you identify health issues across the datacenter on the Service Operations Workspace. It provides a list of quick information on alerts so you can more efficiently monitor systems and services,​ resolve alerts, evaluate the alert impact,​ track issues, and report incidents.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Express List in the Service Operations Workspace for ITOM

The ServiceNow Event Management Express List feature helps you identify health issues across the datacenter on the Service Operations Workspace. It provides a list of quick information on alerts so you can more efficiently monitor systems and services,​ resolve alerts, evaluate the alert impact,​ track issues, and report incidents.

Introduction to the Event Management Express List

## Overview of Express List

The Express List pane sortable alert list reduces the number of clicks necessary to access alert information. Selecting the check box of an alert opens a preview panel where you can view data that helps for prioritization, impact realization, and root cause analysis. You can easily modify the Express List pane to narrow down the display by using a provided fields list, displaying additional alert information, and filtering out or showing matching alerts. You can also modify the displayed time range.

The following image shows a sample Express List pane.![Express List display](../../event-management/image/express-list-main-page.png)

## Express List benefits

The Express List pane enables operators to more efficiently perform the following actions:

-   **Monitoring systems or application services**. Monitoring the performance and capability of computer systems to see any discrepancies​.
-   **Resolving alerts**. Working on discrepancies to troubleshoot issues and promote the efficient functioning of IT infrastructure.​
-   **Tracking issues**. Tracking and documenting defects and resolutions in detail and reporting incidents.
-   **Reporting incidents**. Escalating complex issues to management, other IT resources, third parties or vendors​.

## Alert information displayed in the Express List preview panel

The Express List preview panel displays additional alert information on the Express List pane. This information enables you to conduct an assessment that helps in resolving incidents without having to open multiple alert forms.

The **Info** tab on the preview panel displays the following information for a selected alert:

-   Alert number \(link\)
-   Status
-   Duration
-   Configuration items \(with links\)
-   Metric name
-   Node
-   Resource
-   Source
-   Assigned to
-   Assignment group
-   Last Updated
-   Impacted services

    For more information, see [View data on impacted services on the preview panel in Express List](../task/el-impacted-services-data.md).

-   Additional info
-   Custom field

You can view additional alert information by selecting any of the linked items.

The **Alerts in group** tab on the preview panel displays alert information for a selected alert group. Information for each alert is displayed in a tile with additional options for each alert in the group.

Each tile displays the following alert information:

-   Alert number \(link\)
-   Status
-   Severity
-   Configuration items
-   Duration
-   Metric name

## Customizing the alert display time range

You can determine the time range of the displayed alerts. The default time range is the last 24 hours. The list continues to update with new alerts until you select the pause icon \(![Pause icon.](../image/pause-el.png)\). Selecting the current range setting in the upper right displays a dialog box with date and time range options:

-   All time - The last 90 days
-   Last 24 hours
-   Last week
-   Last 12 hours
-   Last hour
-   Last 15 minutes
-   Custom - Enables you to select a date and time range from the pop-up calendar.

**Related topics**  


[Roles used by Express List](../reference/roles-used-by-express-list.md)

