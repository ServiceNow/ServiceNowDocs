---
title: Create a change schedule from the Change Schedules page
description: You can create a change schedule to view all scheduled changes, change tasks, blackout periods, and maintenance windows for any given date, week, month, or year.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/create-chng-sch-from-chng-sch-page.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Change schedules, Configure, Change Management, IT Service Management]
---

# Create a change schedule from the Change Schedules page

You can create a change schedule to view all scheduled changes, change tasks, blackout periods, and maintenance windows for any given date, week, month, or year.

## Before you begin

-   The Change Management - Change Schedule plugin \(com.snc.change\_management.soc\) must be active.
-   Role required: itil, sn\_chg\_soc.change\_soc\_admin, sn\_change\_role, sn\_change\_write, or admin

**Note:**

-   A user with the itil role can create a change schedule definition and view the change schedule definitions that they create.
-   An admin or a change schedule administrator can read or edit all change schedule definitions.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Schedules** &gt; **Change Schedules** and select **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the change schedule.|
    |Start date field|Field from the change request form that indicates the start date, for example, **Planned start date**.|
    |End date field|Field from the change request form that indicates the end date, for example, **Planned end date**.|
    |Condition|Conditions that determine which change requests display in the Change Schedule interface and the order in which those change requests are sorted.|

3.  Select **Submit**.

    The change schedule is displayed in the timeline view.


**Parent Topic:**[Change schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-schedule.md)

**Related topics**  


[Change schedules view]()

[Create a change schedule from the change schedule definition]()

[Add related tasks to a change schedule]()

[Style rules definition]()

