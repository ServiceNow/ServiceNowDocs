---
title: Analyze log lines that surround an anomaly in Health Log Analytics
description: View the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Review logs that surround the anomaly, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Analyze log lines that surround an anomaly in Health Log Analytics

View the log lines around an anomaly to help you identify the root cause of a Log Analytics alert.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  In the Service Operations Workspace, open a Log Analytics alert.

2.  Select the **Surrounding logs** tab and review the information.

    The tab displays the list of log lines that were generated one minute before and one second after the Log Analytics alert. For an explanation of the information on the tab, see [Surrounding logs tab fields](../reference/hla-surrounding-logs-tab.md).

3.  View a different timespan of the log lines using one of the following methods:

    -   Update the time range relative to the alert to a predefined time range in the **Select range** list.
    -   Specify a **Start time** or **End time** using the time picker.
4.  View the anomalous log data graphically as a function of time by selecting **Log viewer**.

    For more information, see [Reviewing the logs for an alert on the Log Viewer in Health Log Analytics](../concept/hla-op-logs-log-viewer-concept-sow.md).


**Parent Topic:**[Analyzing the logs around an anomaly to help find the alert's root cause in Health Log Analytics](../concept/hla-op-surrounding-logs-view-concept-sow.md)

