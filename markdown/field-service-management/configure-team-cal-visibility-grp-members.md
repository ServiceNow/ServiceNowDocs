---
title: Configure team calendar visibility for group members
description: Increase Team calendar visibility to enable teams to better coordinate meetings, events, and tasks.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Workforce, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Configure team calendar visibility for group members

Increase Team calendar visibility to enable teams to better coordinate meetings, events, and tasks.

## Before you begin

The **team\_calendar.enable\_for\_grpmember** system property must be enabled.

Role required: wm\_admin

## About this task

The Team calendar includes a list of the members in an assignment group and their current schedules. You have the ability to expand the visibility of team members' schedules, making it accessible to both their own group and other groups. Complete the following task to enable group visibility.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  Select the **Type** field on the group record where you want to add calendar visibility.

    If you don't see the **Type** field, click the gear icon to configure the form and add this field.

3.  Add the group type.

    |To|Do This|
    |---|-------|
    |**Make all members in the group visible to other members in the group.**|Select **schedule\_visible\_internally**.|
    |**Make all members in the group visible to all groups.**|Select **schedule\_visible\_externally**.|

    The "sn\_shift\_planning.agent" role is required for an agent's schedule to be visible in the Team calendar in Workforce.

4.  Select **Save**.


**Related topics**  


[Workforce system properties](../concept/workforce-system-properties.md)

[Managing agents and tasks from Workforce](../concept/using-manager-workforce.md)

