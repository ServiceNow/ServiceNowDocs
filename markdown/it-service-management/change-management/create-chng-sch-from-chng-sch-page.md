---
title: Create a change schedule from the Change Schedules page
description: You can create a change schedule to view all scheduled changes, change tasks, blackout periods, maintenance windows for any given date, week, month, or year.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Create a change schedule from the Change Schedules page

You can create a change schedule to view all scheduled changes, change tasks, blackout periods, maintenance windows for any given date, week, month, or year.

## Before you begin

-   You have activated Change Management - Change Schedule plugin \(com.snc.change\_management.soc\).
-   Role required: itil, sn\_chg\_soc.change\_soc\_admin, sn\_change\_role, sn\_change\_write roles, sn\_change\_write, or admin

**Note:**

-   A user with an ITIL role can create a Change Schedule definition and view the schedule definition that they have created.
-   An admin or a change schedule administrator can read or edit all Change Schedule definitions.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Schedules** &gt; **Change Schedules** and click **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the change schedule.|
    |Start date field|Field from the change request form that indicates the start date as an example planned start date.|
    |End date field|Field from the change request form that indicates the end date as an example planned end date.|
    |Condition|Conditions that determine which change requests display in the Change Schedule interface and the order in which those change requests are sorted.|

3.  Click **Submit**.

    The change schedule is displayed in the timeline view.


**Parent Topic:**[Change schedules](../concept/change-schedule.md)

**Related topics**  


[Change schedules view](../concept/change-schedules-view.md)

[Create a change schedule from the change schedule definition](create-chng-sch-from-chng-sch-def.md)

[Add related tasks to a change schedule](add-related-tasks-to-chng-schedule.md)

[Style rules definition](../concept/style-rules-definition.md)

