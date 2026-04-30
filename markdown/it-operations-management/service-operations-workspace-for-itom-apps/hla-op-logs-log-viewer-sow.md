---
title: View log data for an alert
description: View a chart of the frequency of anomalous log lines and the associated log data on the Log viewer.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reviewing the logs for an alert on the Log viewer, Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View log data for an alert

View a chart of the frequency of anomalous log lines and the associated log data on the Log viewer.

## Before you begin

Role required: evt\_mgmt\_operator, or evt\_mgmt\_admin

## Procedure

1.  Open the **Log viewer** tab using one of the following methods:

    -   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the Log Viewer icon \(![Log viewer icon.](../image/icon-log-viewer-sow.png)\).
    -   While viewing log entries for an alert on the **Surrounding logs** tab, select **Log viewer**.
2.  Personalize the displayed data and how it is presented on the Log viewer.

    -   [Filter search results on the Log viewer](hla-op-log-viewer-filter-sow.md) to show only the data you want to view.
    -   [Customize the Log viewer table](hla-op-log-viewer-table-sow.md) by adding or removing columns.
    These features are supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

3.  Analyze log-based anomalies and added context to help you achieve faster mean time to repair \(MTTR\).

    For example, say you find a log line with errors found in a configuration file. On the **Anomaly** card, a sudden spike on the chart indicates where the configuration file is generating the errors. You can view additional key-value pairs extracted from the logs on the **Meaningful log properties** card and find the affected application services and their related service offerings on the **Impacted services** card. For greater context, you may want to [investigate the logs that surround the anomaly](../concept/hla-op-surrounding-logs-view-concept-sow.md), locate the configuration file, and find the time frame where the issues occurred.


## What to do next

Use additional features on the Log viewer to refine your search or define alerts.

-   Modify the search query to fine-tune the search and save useful searches. See [Define, save, and share a search of log data](hla-op-search-queries-manage-sow.md).
-   If you discover important relationships in the log data, select **Define alert** to define the kind of alert that should be triggered by the data. See [Add a Log Analytics alert rule](hla-op-alert-rule-add-sow.md) for instructions.

**Parent Topic:**[Reviewing the logs for an alert on the Log viewer](../concept/hla-op-logs-log-viewer-concept-sow.md)

**Related topics**  


[Reviewing the logs for an alert on the Log viewer](../concept/hla-op-logs-log-viewer-concept-sow.md)

