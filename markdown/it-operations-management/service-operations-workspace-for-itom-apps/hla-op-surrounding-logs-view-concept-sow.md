---
title: Analyzing log lines to identify the root cause of an alert
description: When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you to identify the root cause of an alert.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Analyzing log lines to identify the root cause of an alert

When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you to identify the root cause of an alert.

The **Surrounding logs** tab lists the log lines that were generated one minute before and one second after the anomaly occurred. The log lines are related to the metric or pattern that created the alert. The list is filtered to the relevant component.

Logs that surround the anomaly are retained and available for 30 days after the creation of the alert. The system does not delete these logs when the global retention period of logs expires. When the retention period expires, the surrounding logs are available only on the **Surrounding logs** tab and not in the Log viewer.

<table id="table_mcw_ll1_gtb"><thead><tr><th>

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
</table>-   **[Analyze log lines that surround an anomaly](../task/hla-op-surrounding-logs-view-sow.md)**  
View the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.

**Parent Topic:**[Using Service Operations Workspace for ITOM Log Analytics](hla-op-binder-sow.md)

