---
title: Determine the tasks to appear in the task panel
description: Define default filters to determine which tasks appear on the task panel in the Dispatcher Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Determine the tasks to appear in the task panel

Define default filters to determine which tasks appear on the task panel in the Dispatcher Workspace.

## Before you begin

Role required: admin, wm\_admin

## About this task

By default, dispatchers can filter work order tasks based on their states such as Pending Dispatch, Assigned tasks, P1 tasks, In-progress tasks, Maintenance, and Upcoming tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Task Panel Filters**.

2.  Click **New**.

3.  On the form, fill in the fields.

    **Note:** The **Category** and **Module** fields are read-only.

    |Name|Description|
    |----|-----------|
    |Title|Filter title|
    |Table|Table that contains the fields used to filter the list of work order tasks. The default table is **wm\_task**.|
    |Filter Query|Query to narrow down the fields that are displayed in the task panel.|
    |Order|Display order of the filters in the Dispatcher Workspace. Filters that have lower order numbers appear higher in the order.|
    |User|Name of the user to whom the filter applicable.|
    |Active|Option for enabling the filter in the Dispatcher Workspace.|

4.  Click **Submit**.


