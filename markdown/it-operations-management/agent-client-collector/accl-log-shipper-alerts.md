---
title: View log shipper alerts
description: View all log shipper check alerts for Agent Client Collector Log Analytics \(ACC-L\) agents.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Log Analytics setup, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# View log shipper alerts

View all log shipper check alerts for Agent Client Collector Log Analytics \(ACC-L\) agents.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

In the ACC Alerts list, you can see at a glance if any issues are preventing the log shipper from collecting data. The list shows all log shipper-related alerts in one place and provides information to help you resolve the issues.

The ACC Alerts list only includes alerts about the success or failure of log shipper execution on a CI on a specific agent. These alerts are a subset of the alerts shown in the Event Management Alerts list, which includes alerts of all types. For more information about the Event Management Alerts list, see [View alert information](../../event-management/task/t_EMViewAlert.md).

Log shipper alerts are generated from log shipper events with a severity of Major or Critical. These alerts are typically related to log path issues or a lack of permissions.

**Note:** If an **OK** event on the log shipper is received on a CI where an open log shipper alert exists, the open log shipper alert on that CI is closed.

![Log shipper Alerts list.](../image/accl-log-shipper-alerts-list.png "Log shipper Alerts list")

## Procedure

1.  Navigate to **All** &gt; **ACC Log Analytics** &gt; **ACC Log Alerts**.

2.  Review the information provided in the Alerts list.

    For details and a description of the columns, see [Monitor incoming alerts](../../event-management/task/t_EMUseAlertConsole.md).


**Related topics**  


[View log shipper events](accl-log-shipper-events.md)

