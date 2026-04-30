---
title: Configure the alert active interval
description: The active interval property \(evt\_mgmt.active\_interval\) determines how Event Management handles a new event that is similar to events that appear on an existing closed alert. Based on the active interval, event, and existing closed alert information, the alert is reopened and the event information is added to the existing alert or a new alert is created.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Alert lifecycle configuration, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure the alert active interval

The active interval property \(**evt\_mgmt.active\_interval**\) determines how Event Management handles a new event that is similar to events that appear on an existing closed alert. Based on the active interval, event, and existing closed alert information, the alert is reopened and the event information is added to the existing alert or a new alert is created.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When the new event is received and the alert is already closed, Event Management compares the time since the last alert update \(**sys\_updated\_on**\) and the active interval property value. Then, the system either updates the existing alert or creates a new alert \(if the original alert is closed\), as explained in the following table. If the alert is open, Event Management automatically updates it without checking the active interval property value.

|Scenario|Result|
|--------|------|
|The new event occurs before the active interval elapses for the existing closed alert.|The event is identified as a recurrence of an existing issue. The alert is updated with the event information and the alert is reopened.|
|The new event occurs after the active interval elapses for the existing closed alert.|A new alert is created because the event is identified as a new issue. The event information is added to the new alert.|

Change the active interval by editing the **Active interval \(in seconds\), within which a new event reopens a closed alert** property value.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Event Management Properties**.

2.  Change the number of seconds for the **Active interval \(in seconds\), within which a new event reopens a closed alert** property.

3.  Click **Save**.


**Parent Topic:**[Alert lifecycle configuration](../concept/c_EMAlertRule.md)

