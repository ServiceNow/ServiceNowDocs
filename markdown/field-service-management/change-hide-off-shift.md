---
title: Change the number of days that dispatchers can hide off shift agents
description: Increase the amount of time that the hide off-shift agent shows on the calendar in Dispatcher Workspace so dispatchers can plan around agent schedules farther in advance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Change the number of days that dispatchers can hide off shift agents

Increase the amount of time that the hide off-shift agent shows on the calendar in Dispatcher Workspace so dispatchers can plan around agent schedules farther in advance.

## Before you begin

Change the number of days that dispatchers can hide off shift agents 

Role required: admin

## About this task

By default dispatchers can use the hide off shift agents button up to seven days in the future. If a dispatcher navigates on the calendar in Dispatcher Workspace farther than seven days in the future, then the hide off shift agents button is disabled. You can change the number of days that the hide off shift agents button shows.

For more information on hiding off shift agents, see [Show or hide off shift agents from the calendar in Dispatcher Workspace](hide-off-shift-agents.md).

**Warning:** Extending the number of days in the future that the hide off shift agents button is available causes the nightly processing of the Populate Agents Daily Schedule Table to take longer. Don't extend the number of days that the hide off shift agents button is available past 15 days.

## Procedure

1.  Navigate to **All**, type `sys_properties.list` in the filter field, and press enter on your keyboard.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Name|Description|
    |----|-----------|
    |**Name**|glide.sg.offline.scheduled\_download.no\_of\_days\_data|
    |**Type**|Integer|
    |**Value**|Enter the number of days that the Show or hide off shift agents icon should be present in the calendar in Dispatcher Workspace.|

4.  Select **Submit**.


**Related topics**  


[Run the Populate Agents Daily Schedule Table](run-agent-schedule.md)

[Show or hide off shift agents from the calendar in Dispatcher Workspace](hide-off-shift-agents.md)

