---
title: Analyzing log lines to identify the root cause of an alert
description: When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you to identify the root cause of an alert.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Analyzing log lines to identify the root cause of an alert

When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you to identify the root cause of an alert.

While viewing a Log Analytics alert in the Operator Workspace, the **Surrounding logs** tab lists the log lines that were generated one minute before and one second after the anomaly occurred. The log lines are related to the metric or pattern that created the alert. The list is filtered to the relevant component.

<table id="table_oj2_3gw_zpb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time

</td><td>

Timestamp of the log line in the format that the source uses. If no value appears, then check the source type structure of the raw data.

</td></tr><tr><td>

Service instance

</td><td>

Service instance in which the metric was found.

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
</table>You can modify the time range of the displayed log lines, for example to investigate logs from more than one minute before the anomaly, or more than a second afterwards.

Health Log Analytics enables you to view the anomalous log data graphically on the Log viewer, accessed from the Service Operations Workspace.

The Log viewer presents all data connected with the Log Analytics alert. It automatically shows the query that relates to the anomaly, the selected component, and the appropriate time filter. Manually adjusting the time range does not affect any of the other settings. The applied filters appear in the **Filters** pane, where you can add or remove filters as needed. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **[Analyze log lines that surround an anomaly](../task/hla-op-surrounding-logs-view.md)**  
View the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.

**Parent Topic:**[Using Health Log Analytics](../reference/hla-op-guide-binder.md)

**Related topics**  


[Viewing the logs for an alert on the Log viewer](hla-op-logs-log-viewer-concept-sow.md)

