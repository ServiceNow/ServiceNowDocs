---
title: Review logs surrounding an anomaly
description: When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you narrow down the root cause of an alert.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/hla-op-surrounding-logs-view-concept.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analyzing and resolving alerts, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Review logs surrounding an anomaly

When Health Log Analytics identifies an anomaly, viewing the logs that surround the anomaly provides clues about the state of faulting systems. This information can help you narrow down the root cause of an alert.

While viewing a Log Analytics alert, the **Surrounding logs** tab lists the log lines that were generated one minute before and one second after the anomaly occurred. The log lines are related to the metric or pattern that triggered the alert. The list is filtered to the relevant component.

Logs generated immediately before the anomaly might point to warning signs or conditions that led to the issue. By reviewing these logs, you can trace the sequence of events that led to the anomaly, helping you understand what went wrong. Logs created right after the anomaly can help you evaluate the impact of the event by analyzing how the system responded and whether other components were affected. The timeline of the logs around the anomaly can help clarify what might have caused the issue, for example a configuration change or a software update.

You can modify the time range of the displayed log lines, for example to investigate logs from more than one minute before the anomaly, or more than a second afterward.

**Note:** Logs that surround the anomaly are retained and available for 30 days after the creation of the alert. The system does not delete these logs when the global retention period of logs expires. When the retention period expires, the surrounding logs are available only on the **Surrounding logs** tab and not in the Log viewer.

Health Log Analytics enables you to view the anomalous log data graphically on the Log viewer, accessed from the Service Operations Workspace. The Log viewer displays a chart of the frequency of anomalous log lines during one minute before and one minute after the Log Analytics alert and lists the associated log lines. It automatically shows the query that relates to the anomaly, the selected component, and the appropriate time filter. For more information, see [Review alert-related logs on the Log Viewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-logs-log-viewer-concept.md).

-   **[Analyze log lines surrounding an anomaly](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-op-surrounding-logs-view.md)**  
View the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.

**Parent Topic:**[Analyzing and resolving Log Analytics alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-analyzing-resolving-hla-alert.md)

**Related topics**  


[Analyze log lines that surround an anomaly in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-surrounding-logs-view-sow.md)

