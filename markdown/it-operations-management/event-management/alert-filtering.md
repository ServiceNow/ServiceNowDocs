---
title: Configure filters for automatic alert groups
description: Filter alerts and alert groups to reduce alert noise. Only alerts that match the filter are included in the group of the selected group type \(Automated, CMDB, or Text\).
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scheduled jobs and parameters for alert grouping, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure filters for automatic alert groups

Filter alerts and alert groups to reduce alert noise. Only alerts that match the filter are included in the group of the selected group type \(Automated, CMDB, or Text\).

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

If your filter specifies alerts whose configuration item class is not Linux, then only alerts with non-Linux configuration items are included in the group of the selected group type.

**Note:** After the filter is created, it will only apply to new alerts.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Automatic Group Filter**.

2.  On the Automatic Group Filters page, either select an existing group filter or create a new filter.

3.  If you are creating a new filter:

    1.  Select **New**.

    2.  Enter a name for the filter in the **Name** field.

    3.  Select the alert group type:

        -   Automated
        -   Test
        -   CMDB
        You can assign more than one group type with a single filter condition.

        Each group type can have only one active filter.

4.  In the **Alert Filter** section, create conditions for the alert to meet to be included in the group.

5.  Save the alert group filter.

    -   For an existing alert group filter, select **Submit**.
    -   For a new alert group filter, select **Update**.

## Result

The filter condition appears on the SA Grouped Alert Filters page in the **Alert filter** column.

