---
title: Enable resource time indicators
description: Resource time indicators allow dispatchers to see all the Field Service technicians' time zones on the calendar in Dispatcher Workspace at a glance. It takes away the math needed to calculate time zones differences between technicians.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Time Zones, Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Enable resource time indicators

Resource time indicators allow dispatchers to see all the Field Service technicians' time zones on the calendar in Dispatcher Workspace at a glance. It takes away the math needed to calculate time zones differences between technicians.

## Before you begin

Role required: wm\_admin

## About this task

When the `work.management.enable.resource.time.indicator` property is enabled, a date and time field showing the task’s time zone is added to all the forms that have a date and time field with populated data throughout Dispatcher Workspace and the ServiceNow AI Platform.

For example, if a dispatcher is in Pacific time, and they open the form of a work order task scheduled in Mountain time, then they see a blue box below the date and time fields of the task that shows the time for the task in Mountain time. If the date and time field is empty, then the added field doesn’t show.

Once the resource time indicators property is enabled, dispatchers can turn on resource time indicators in the settings in Dispatcher Workspace. For more information, see [Enable Dispatcher Workspace settings](dispatcher-wrkspc-settings.md).

## Procedure

1.  Navigate to **All** and enter `sys_properties.list` and press Enter or Return on your keyboard.

2.  Search for and select the system property `work.management.enable.resource.time.indicator`.

3.  Select the **Value** field and enter `True`.

4.  Select **Update**.


