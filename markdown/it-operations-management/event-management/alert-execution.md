---
title: Alert execution information
description: Alert execution information provides a reference to the actions that have been performed concerning the alert. Among the information presented is which alert management rules ran on the alert, incidents that were opened, and which remediation workflows ran.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [View alert information, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert execution information

Alert execution information provides a reference to the actions that have been performed concerning the alert. Among the information presented is which alert management rules ran on the alert, incidents that were opened, and which remediation workflows ran.

## Alert Executions

In an alert form, the Alert Execution tab shows key related records for the alert. For example, it shows which actions were performed and which alert management rules were run. If an incident was opened, the related tasks are shown.

![Alert execution details](../image/alert-execution.png "Alert Executions")

|Field|Description|
|-----|-----------|
|Alert|Reference to the alert that ran under this rule.|
|Action name|Indicates how the alert was resolved.|
|Link to execution|Link action that was taken to resolve the alert.|
|Related task|Link to the incident that was created when the alert was resolved.|
|Log|Link to the log that details the actions taken to resolve the alert|
|Automatic run|Indicates if the rule was automatic \(true\) or manual \(false\).|

## Action name

This indicates what occurred, for example, if an incident was created.

## Log

The log reveals which alert management rule initiated the action. It shows, for example, automatic execution 1 out 3, or manual execution, 2 out of 4.

**Parent Topic:**[View alert information](../task/t_EMViewAlert.md)

