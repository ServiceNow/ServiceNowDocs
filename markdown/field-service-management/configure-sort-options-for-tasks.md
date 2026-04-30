---
title: Configure sort options for task panel
description: Configure options for dispatchers to sort work order tasks in Dispatcher Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Dispatcher Workspace, Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Configure sort options for task panel

Configure options for dispatchers to sort work order tasks in Dispatcher Workspace.

## Before you begin

Role required: wm\_admin, admin

## About this task

By default, dispatchers can sort tasks based on only the following options:

-   Scheduled Start Date - Earliest
-   Scheduled Start Date - Latest
-   Priority - Highest
-   Window End - Earliest
-   Window End - Latest
-   Window Start - Earliest
-   Window Start - Latest

## Procedure

1.  Navigate to **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Task Panel Sorting**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Name|Description|
    |----|-----------|
    |Name|Unique name for the sort option.|
    |Display Name|Labels for the fields that appear as the sort option in Dispatcher Workspace.|
    |Table|Table that contains the fields that are used to sort the list of work order tasks. This field is automatically set to the wm\_task table.|
    |Field|Field used for sorting the list of tasks.|
    |Active|Option for displaying the field for sorting tasks in Dispatcher Workspace.|
    |Sort order|Sort order for the sort field labels. The default value is ascending. To use a descending order, select **z-a**.|
    |Order|The display order of the sort options in Dispatcher Workspace. Sort options that have a lower order number appear higher in the order.|

4.  Click **Submit**.


