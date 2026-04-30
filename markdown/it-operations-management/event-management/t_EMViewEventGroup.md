---
title: View patterns for event group creation
description: Event groups are sets of events that do not have a matching event rule. You can view the patterns in a group of events to learn the impact of creating a rule based on the event source and description patterns.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View patterns for event group creation

Event groups are sets of events that do not have a matching event rule. You can view the patterns in a group of events to learn the impact of creating a rule based on the event source and description patterns.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

Events are grouped according to their source and description.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Wait for the group calculation to complete and then click the created link.

    If there are not enough events, the calculation will not create groups.

3.  In the list of events, select an event.

4.  To change the pattern of an event, double-click the pattern, make your changes, and then click **Update**.

    ![Event Groups](../image/EventManagementGroups.png)


**Parent Topic:**[Event rules](../concept/create-event-rules.md)

