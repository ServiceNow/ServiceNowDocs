---
title: Close an alert
description: Close an alert by an event or a user action. Closing an alert also closes any related incident that is not already resolved or closed.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Close an alert

Close an alert by an event or a user action. Closing an alert also closes any related incident that is not already resolved or closed.

## Before you begin

Role required: evt\_mgmt\_admin or evt\_mgmt\_operator

## About this task

An alert can be closed manually, automatically by a close or clear event, or when a related incident is resolved. Whether the alert is closed when the incident is closed is determined by the **evt\_mgmt.incident\_closes\_alert** property.

When a Clear event is triggered for an open alert, the corresponding alert is set to the "Closed" state. Closing an alert also closes any related incident that is not already resolved or closed. This default behavior can be configured using the **evt\_mgmt.alert\_closes\_incident** property.

## Procedure

1.  Navigate to **Event Management** &gt; **All Alerts**.

2.  Select the alert you want to close.

3.  In the Alert Form, select **Close**.

    The alert closes without confirmation. If the alert has any resolved or closed incidents, a work note is added to the incident indicating that the related alert was closed.

    If an alert has an open incident that is not related to any other open alerts, the incident is either closed, resolved, or left unchanged based on the **evt\_mgmt.alert\_closes\_incident** property.


**Parent Topic:**[Manage and monitor alerts](../concept/c_EMAlert.md)

