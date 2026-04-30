---
title: Change the recipients of notifications for intraday schedule automation
description: You can change who receives notifications related to intraday schedule automation, so only the necessary recipients receive the notifications. For example, if an agent is late for a task, you can configure notifications to only be sent to the dispatcher.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Configuring Intraday schedule automation, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Change the recipients of notifications for intraday schedule automation

You can change who receives notifications related to intraday schedule automation, so only the necessary recipients receive the notifications. For example, if an agent is late for a task, you can configure notifications to only be sent to the dispatcher.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the flow that you want to change the notification recipients for.

3.  Select the subflow, and then the notification trigger.

4.  Select **Edit subflow**.

5.  Select the Data Pill Picker icon ![data pill picker](../image/data-pill-pick.png) for the field you want to change the recipients of intraday schedule automation notifications.

    |Action input|Description|
    |------------|-----------|
    |**Recipient user field**|Determine the recipient of the notification by choosing a sys\_user field.|
    |**Recipient group fields**|Choose a different group to receive notifications.|
    |**Scripted recipients**|Use a script to selectively determine who receives notifications.|

    **Note:** By default intraday schedule automation sends notifications to everyone in the dispatch group that the agent is a member of.

6.  Select **Publish**.


