---
title: Analyze log lines that surround an anomaly in Health Log Analytics
description: Review the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [surrounding logs, anomaly analysis, log timeline analysis, root cause analysis, health log analytics, log anomaly investigation, log viewer, anomaly timeline, log investigation, alert investigation, log data analysis, anomaly root cause, troubleshooting logs, system fault diagnosis]
breadcrumb: [Review logs surrounding the anomaly, Analyzing and resolving alerts, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Analyze log lines that surround an anomaly in Health Log Analytics

Review the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.

## Before you begin

For background information, see [Review logs surrounding the anomaly to help find the root cause in Health Log Analytics](../concept/hla-op-surrounding-logs-view-concept.md).

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  In the Service Operations Workspace, open a Log Analytics alert.

2.  Select the **Surrounding logs** tab and review the information.

    The tab displays the list of log lines that were generated one minute before and one second after the Log Analytics alert. For an explanation of the information on the tab, see [Surrounding logs tab fields](../reference/hla-surrounding-logs-tab.md).

3.  View a different time span of the log lines using one of the following methods:

    -   Update the time range relative to the alert to a predefined time range in the **Select range** list.
    -   Specify a **Start time** or **End time** using the time picker.
4.  View the anomalous log data graphically as a function of time by selecting **Log viewer**.


