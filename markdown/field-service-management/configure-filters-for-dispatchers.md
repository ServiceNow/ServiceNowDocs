---
title: Configure filters for dispatchers
description: Create filters for dispatchers to filter work order tasks in Dispatcher Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure filters for dispatchers

Create filters for dispatchers to filter work order tasks in Dispatcher Workspace.

## Before you begin

Role required: wm\_admin, admin

## About this task

By default, dispatchers can filter tasks based on work order task states. You can also create your own filters for the tasks.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Task Panel Dispatcher Filters**.

    **Note:** Select any filter from the Application Filter Configurations list to see what it filters from the task panel in Dispatcher Workspace.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Name|Description|
    |----|-----------|
    |Title|Filter title|
    |Table|Table that contains the fields used to filter the list of work order tasks. This field is automatically set to the wm\_task table.|
    |Filter Query|Query to narrow down the fields that are displayed in the task panel.|
    |Order|The display order of the filters in Dispatcher Workspace. Filters that have a lower order number appear higher in the order.|
    |Active|Option for enabling the filter in Dispatcher Workspace.|

4.  Click **Submit**.

    ![application filter configuration form](../image/application-filter.png)


