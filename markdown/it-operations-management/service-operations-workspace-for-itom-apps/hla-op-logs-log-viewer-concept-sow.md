---
title: Reviewing the logs for an alert on the Log Viewer in Health Log Analytics
description: The Log Viewer tab lets you browse the logs for an alert by timestamp or time range, and visualize anomaly frequency within a specific time period. Customizing the displayed data and adjusting time filters enables you to better understand the framework in which the anomaly occurred, helping you find the root cause faster.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Reviewing the logs for an alert on the Log Viewer in Health Log Analytics

The **Log Viewer** tab lets you browse the logs for an alert by timestamp or time range, and visualize anomaly frequency within a specific time period. Customizing the displayed data and adjusting time filters enables you to better understand the framework in which the anomaly occurred, helping you find the root cause faster.

The Log Viewer presents all data connected with the Log Analytics alert. It shows the query that relates to the anomaly, the selected component, and the appropriate time filter. You can personalize the displayed data, and manually adjust the time range without affecting the other settings. The applied filters appear in the **Filters** pane. You can add or remove filters as needed to show only the data you want to view.

The **Log Viewer** displays a chart of the frequency of anomalous log lines during one minute before and one minute after the Log Analytics alert and lists the associated log data. This information helps you identify trends leading up to and following the event, providing context for root cause analysis.

As you analyze the logs for an alert on the **Log Viewer**, you can modify the query to fine-tune the search, save useful searches, and share them with others. For a description of the information displayed in the **Log Viewer** table, see [Log Viewer table fields](../reference/hla-op-log-viewer-table-ref.md).

You can perform the following tasks on the **Log Viewer**:

-   [View log data for an alert in Health Log Analytics](../task/hla-op-logs-log-viewer-sow.md)

    View a chart of the frequency of anomalous log lines and the associated log data.

-   [Define, save, and share a search of log data in Health Log Analytics](../task/hla-op-search-queries-manage-sow.md)

    Fine-tune the search query to help determine the causes of the issue, and save and share useful searches.

-   [Use or modify a saved log data search in Health Log Analytics](../task/hla-op-search-queries-saved-sow.md)

    Use a saved search. As the owner of a saved search, you can modify the search values and save your changes.

-   [Filter search results on the Log Viewer in Health Log Analytics](../task/hla-op-log-viewer-filter-sow.md)

    Apply filters to show only the data you want to view.

-   [Customize the Log Viewer table in Health Log Analytics](../task/hla-op-log-viewer-table-sow.md)

    Add or remove columns in the table to show only the data you want to view.


If you discover an important metric in the log data, you can use it to define a new Log Analytics alert rule. For more information, see [Define a Log Analytics alert rule in Health Log Analytics](../task/hla-op-alert-rule-add-sow.md).

-   **[View log data for an alert in Health Log Analytics](../task/hla-op-logs-log-viewer-sow.md)**  
View a chart of the frequency of anomalous log lines and the associated log data on the Log Viewer.
-   **[Define, save, and share a search of log data in Health Log Analytics](../task/hla-op-search-queries-manage-sow.md)**  
Define, save, and share searches of log data to help determine the causes of Log Analytics alerts.
-   **[Use or modify a saved log data search in Health Log Analytics](../task/hla-op-search-queries-saved-sow.md)**  
Use a saved search of log data to better understand the causes of an alert. As the owner of a saved search, you can modify the search values and save your changes.
-   **[Filter search results on the Log Viewer in Health Log Analytics](../task/hla-op-log-viewer-filter-sow.md)**  
Apply filters on the **Log Viewer** to show only your desired data.
-   **[Customize the Log Viewer table in Health Log Analytics](../task/hla-op-log-viewer-table-sow.md)**  
Add or remove columns in the **Log viewer** table to show only the data you want to view.

**Parent Topic:**[Log Analytics in Service Operations Workspace for ITOM](hla-op-binder-sow.md)

**Related topics**  


[Analyzing the logs around an anomaly to help find the alert's root cause in Health Log Analytics](hla-op-surrounding-logs-view-concept-sow.md)

