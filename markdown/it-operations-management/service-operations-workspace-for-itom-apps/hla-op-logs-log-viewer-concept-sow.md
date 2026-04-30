---
title: Viewing the logs for an alert on the Log viewer
description: The Log viewer in the Service Operations Workspace enables you to browse the logs by timestamp or time range, to search for particular log text, and to visualize the frequency of anomaly occurrences in a particular time period. If you discover an important metric in the log data, you can use it to define a Log Analytics alert rule.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Viewing the logs for an alert on the Log viewer

The **Log viewer** in the Service Operations Workspace enables you to browse the logs by timestamp or time range, to search for particular log text, and to visualize the frequency of anomaly occurrences in a particular time period. If you discover an important metric in the log data, you can use it to define a Log Analytics alert rule.

The Log viewer displays a chart of the frequency of anomalous log lines during one minute before and one minute after the Log Analytics alert. In addition, the viewer lists the associated log lines.

<table id="table_dzq_kr2_ftb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time

</td><td>

Timestamp of the log line in the format that the source uses. If no value appears, then check the source type structure of the raw data.

</td></tr><tr><td>

Application service

</td><td>

Application service in which the metric was found.

</td></tr><tr><td>

Component

</td><td>

Logical component of the service instance that generated the event. Multiple CIs can sometimes perform the same function.

</td></tr><tr><td>

Message

</td><td>

Inner message of the raw log line that contains the text of the system-generated log message regarding the nature of the occurrence.

</td></tr><tr><td>

Level

</td><td>

Type of event. The available values, in order of importance, are:-   **Emergency**
-   **Alert**
-   **Critical**
-   **Error**
-   **Warning**
-   **Notice**
-   **Informational**
-   **Debug**

</td></tr><tr><td>

Host

</td><td>

Host identifier from the log line that consists of the hostname or IP address of the endpoint.

</td></tr><tr><td>

Log message

</td><td>

The raw log message without the header.

</td></tr></tbody>
</table>**Note:** By default, the Raw message column does not appear in the Log viewer table. You can display this column by selecting it from the **Filters** pane. For more information, see [Customize the Log viewer table](../task/hla-op-log-viewer-table.md).

You can personalize the displayed data on the Log viewer:

-   [Filter search results on the Log viewer](../task/hla-op-log-viewer-filter-sow.md) to show only the data you want to view.
-   [Customize the Log viewer table](../task/hla-op-log-viewer-table-sow.md) by adding or removing columns.

**Note:** These features are supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

As you analyze the logs for an alert, you can modify the search query to fine-tune the search, and save useful searches. For more information, see [Define, save, and share a search of log data](../task/hla-op-search-queries-manage-sow.md).

If you discover important relationships in the log data, you can define the type of alert that the data should trigger. For more information, see [Add a Log Analytics alert rule](../task/hla-op-alert-rule-add-sow.md).

-   **[View log data for an alert](../task/hla-op-logs-log-viewer-sow.md)**  
View a chart of the frequency of anomalous log lines and the associated log data on the Log viewer.
-   **[Define, save, and share a search of log data](../task/hla-op-search-queries-manage-sow.md)**  
Define, save, and share searches of log data to help determine the causes of Log Analytics alerts.
-   **[Use or modify a saved search](../task/hla-op-search-queries-saved-sow.md)**  
Use a saved search of log data to better understand the causes of an alert. As the owner of a saved search, you can modify the search values and save your changes.
-   **[Filter search results on the Log viewer](../task/hla-op-log-viewer-filter-sow.md)**  
Apply filters on the **Log viewer** to show only your desired data.
-   **[Customize the Log viewer table](../task/hla-op-log-viewer-table-sow.md)**  
Add or remove columns in the **Log viewer** table to show only the data you want to view.

**Parent Topic:**[Using Service Operations Workspace for ITOM Log Analytics](hla-op-binder-sow.md)

