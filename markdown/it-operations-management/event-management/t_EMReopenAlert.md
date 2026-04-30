---
title: Reopen an alert
description: Additional events can cause reopening of alerts, or you can reopen an alert by changing its state. When an alert reopens, any associated incidents can also be updated or reopened according to the incident state and the evt\_mgmt.alert\_reopens\_incident property.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Reopen an alert

Additional events can cause reopening of alerts, or you can reopen an alert by changing its state. When an alert reopens, any associated incidents can also be updated or reopened according to the incident state and the **evt\_mgmt.alert\_reopens\_incident** property.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

When an alert is reopened, the related incident is processed as follows:

-   If the incident is not **Resolved** or **Closed**, a work note is added to indicate that the related alert was reopened.
-   If the incident is **Resolved** or **Closed**, the incident is reopened, a new incident is created, or nothing is done, depending on the **evt\_mgmt.alert\_reopens\_incident** property value.
    -   If the incident is reopened, work notes are added to the incident.
    -   If a new incident is created, any matching alert management rule, alert action rule, and task template applies to the incident. If there is no matching alert action rule or template, fields from the existing incident are copied to a new incident.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Search by alert number.

3.  In the **State** field, click **Reopen**.

4.  Click **Update**.


**Parent Topic:**[Manage and monitor alerts](../concept/c_EMAlert.md)

