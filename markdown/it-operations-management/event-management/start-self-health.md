---
title: Start or stop self-health monitoring
description: You can control the starting or stopping of the self-health monitor feature by configuring the self-health monitoring property. The first time that the self-health monitoring property is enabled, it automatically creates the ServiceNow Event Management application services.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Self-health monitors for Event Management, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Start or stop self-health monitoring

You can control the starting or stopping of the self-health monitor feature by configuring the self-health monitoring property. The first time that the self-health monitoring property is enabled, it automatically creates the ServiceNow Event Management application services.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Configure the self-health monitoring property to monitor and track application services and Event Management.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Event Management Properties**.

2.  Locate the **Enable Event Management self-health monitoring** \(**evt\_mgmt.self\_health\_active**\) property.

    Select one of these values:

    |Field|Description|
    |-----|-----------|
    |Enabled|The ServiceNow Event Management application services is created and set to monitor self-health. Events are received and alerts are generated.|
    |Alerts Only|The ServiceNow Event Management application services and the CIs related to it are not created. Alerts are created but are not bound to a CI.|
    |Disabled|The ServiceNow Event Management application services is not operational. Events are not received, and alerts are not generated.|

3.  Click **Save**.


## Result

The ServiceNow Event Management application services is set according to the value selected for the **evt\_mgmt.self\_health\_active** property.

**Parent Topic:**[Self-health monitors for Event Management](../concept/self-monitoring.md)

