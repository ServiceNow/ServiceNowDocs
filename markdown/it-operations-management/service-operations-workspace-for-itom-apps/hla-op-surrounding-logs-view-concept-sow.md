---
title: Analyzing log lines to identify the root cause of an alert
description: When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you narrow down the root cause of an alert.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Analyzing log lines to identify the root cause of an alert

When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you narrow down the root cause of an alert.

While viewing a Log Analytics alert, the **Surrounding logs** tab lists the log lines that were generated one minute before and one second after the anomaly occurred. The log lines are related to the metric or pattern that triggered the alert. The list is filtered to the relevant component.

Logs generated immediately before the anomaly might point to warning signs or conditions that led to the issue. By reviewing these logs, you can trace the sequence of events that led to the anomaly, helping you understand what went wrong. Logs created right after the anomaly can help you evaluate the impact of the event by analyzing how the system responded and whether other components were affected. The timeline of the logs around the anomaly can help clarify what might have caused the issue, for example a configuration change or a software update.

You can modify the time range of the displayed log lines, for example to investigate logs from more than one minute before the anomaly, or more than a second afterward.

**Note:** Logs that surround the anomaly are retained and available for 30 days after the creation of the alert. The system does not delete these logs when the global retention period of logs expires. When the retention period expires, the surrounding logs are available only on the **Surrounding logs** tab and not in the Log viewer.

Health Log Analytics enables you to view the anomalous log data graphically on the Log viewer, accessed from the Service Operations Workspace. The Log viewer displays a chart of the frequency of anomalous log lines during one minute before and one minute after the Log Analytics alert and lists the associated log lines. It automatically shows the query that relates to the anomaly, the selected component, and the appropriate time filter. For more information, see [Reviewing the logs for an alert on the Log viewer](hla-op-logs-log-viewer-concept.md).

-   **[Analyze log lines that surround an anomaly](../task/hla-op-surrounding-logs-view-sow.md)**  
View the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.

**Parent Topic:**[Using Service Operations Workspace for ITOM Log Analytics](hla-op-binder-sow.md)

**Related topics**  


[Analyze log lines that surround an anomaly](../task/hla-op-surrounding-logs-view-sow.md)

