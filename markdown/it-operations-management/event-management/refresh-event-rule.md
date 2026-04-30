---
title: Refresh event rules
description: Manually update event rules to reflect current event information because once an event rule is created, the Event Additional info and Event Raw info fields are not automatically updated.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Refresh event rules

Manually update event rules to reflect current event information because once an event rule is created, the **Event Additional info** and **Event Raw info** fields are not automatically updated.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Events**.

2.  Select the event.

3.  Select **Refresh Event Rule**.

4.  Select the event rules to refresh.

5.  Select **Refresh Selected**.

    If you selected multiple event rules, then the last selected item in the list opens in the Event Rule Designer.

    **Note:** If the current event rule regex expressions do not match the selected event after the refresh, the update fails and an error message appears specifying the problematic fields. This safeguard ensures that your previously defined event rule regex expressions are not broken due to the refresh.


**Parent Topic:**[Event rules](../concept/create-event-rules.md)

