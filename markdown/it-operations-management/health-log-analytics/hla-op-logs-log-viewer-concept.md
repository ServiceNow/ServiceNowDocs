---
title: Reviewing the logs for an alert on the Log viewer
description: The Log viewer tab lets you browse the logs for an alert by timestamp or time range, and visualize anomaly frequency within a specific time period. Customizing the displayed data and adjusting time filters enables you to better understand the framework in which the anomaly occurred, helping you find the root cause faster.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Reviewing the logs for an alert on the Log viewer

The **Log viewer** tab lets you browse the logs for an alert by timestamp or time range, and visualize anomaly frequency within a specific time period. Customizing the displayed data and adjusting time filters enables you to better understand the framework in which the anomaly occurred, helping you find the root cause faster.

The Log viewer presents all data connected with the Log Analytics alert. It shows the query that relates to the anomaly, the selected component, and the appropriate time filter. You can personalize the displayed data, and manually adjust the time range without affecting the other settings. The applied filters appear in the **Filters** pane. You can add or remove filters as needed to show only the data you want to view.

The **Log viewer** displays a chart of the frequency of anomalous log lines during one minute before and one minute after the Log Analytics alert and lists the associated log data. This information helps you identify trends leading up to and following the event, providing context for root cause analysis.

As you analyze the logs for an alert on the **Log viewer**, you can modify the query to fine-tune the search, save useful searches, and share them with others. For a description of the information displayed in the **Log viewer** table, see [Log viewer table fields](../reference/hla-op-log-viewer-table-ref.md).

You can perform the following tasks on the **Log viewer**:

-   [View log data for an alert](../task/hla-op-logs-log-viewer-sow.md)

    View a chart of the frequency of anomalous log lines and the associated log data.

-   [Define, save, and share a search of log data](../task/hla-op-search-queries-manage-sow.md)

    Fine-tune the search query to help determine the causes of the issue, and save and share useful searches.

-   [Use or modify a saved search](../task/hla-op-search-queries-saved-sow.md)

    Use a saved search. As the owner of a saved search, you can modify the search values and save your changes.

-   [Filter search results on the Log viewer](../task/hla-op-log-viewer-filter-sow.md)

    Apply filters to show only the data you want to view.

-   [Customize the Log viewer table](../task/hla-op-log-viewer-table-sow.md)

    Add or remove columns in the table to show only the data you want to view.


If you discover an important metric in the log data, you can use it to define a new Log Analytics alert rule. For more information, see [Add a Log Analytics alert rule](../task/hla-op-alert-rule-add-sow.md).

**Related topics**  


[Analyzing the logs that surround the anomaly](hla-op-surrounding-logs-view-concept.md)

