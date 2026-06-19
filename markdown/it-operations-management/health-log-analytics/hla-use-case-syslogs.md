---
title: Use Case: Proactive monitoring of your ServiceNow instance in Health Log Analytics
description: Use Health Log Analytics to detect and resolve emerging issues in your organization's ServiceNow instance before they negatively impact users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-use-case-syslogs.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, system logs, instance, monitoring, use case, data input, MID Server, System Logs Retriever]
breadcrumb: [Analyzing and resolving alerts, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Use Case: Proactive monitoring of your ServiceNow instance in Health Log Analytics

Use Health Log Analytics to detect and resolve emerging issues in your organization's ServiceNow instance before they negatively impact users.

## Using the ServiceNow System Logs Retriever integration to detect platform issues automatically

Starting with version 35.0.26 of Health Log Analytics, you can use the [ServiceNow System Logs Retriever integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-glide-syslog.md) to automatically detect errors and anomalies in your ServiceNow instance's system logs. As an operator you can view, manage, and respond to the generated alerts in the [Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/t_EMUseAlertConsole.md). Filter the list to show only alerts for the impacted service. Then, use Now Assist to get an in-depth analysis of the alert and potential resolutions in straightforward, human-readable language. This AI-driven tool demonstrates a deep understanding of the Glide system and offers actionable insights.

Combining HLA's anomaly detection with Now Assist's GenAI capabilities provides a comprehensive toolkit for identifying and resolving platform system issues more effectively. This collaboration enables Health Log Analytics to help prevent system issues from impacting your platform users.

## Using the MID Server and System Logs Retriever data inputs together to monitor your instance

You can also stay ahead of disruptions to your ServiceNow environment by using the [MID Server data input](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-mid-server.md) and the [ServiceNow System Logs Retriever data input](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-glide-syslog.md) together.

As an admin, you select a MID Server from the MID Servers list. Under Related Links, choose **Create MID Server Data Input using HLA** to create a data input specific to the selected MID Server. Then activate the System Logs Retriever data input and configure it to collect your ServiceNow instance's system logs.

As an operator, you navigate to the [Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/t_EMUseAlertConsole.md) and select an alert from the Alerts list. Review the alert details, including duration and impacted services, and analyze the logs that surround the anomaly. Use Now Assist to get an in-depth analysis of the alert and potential resolutions in straightforward, human-readable language. If needed, for further investigation, you can navigate to the [Reviewing the logs for an alert on the Log Viewer in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-op-logs-log-viewer-concept-sow.md) for a visual presentation of the system logs. Select System Logs Retriever from the components drop-down list to view all the errors that have occurred in the ServiceNow instance. You can customize the visualization by using filters.

By drilling down into the alert and MID Server logs, you can quickly identify the issue and resolve it before it affects your platform users.

