---
title: Create an information schedule
description: Create an information schedule to record events such as holidays or organizational events that change teams should be aware of. Conflict detection doesn't create conflict records for information schedules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/create-information-schedule.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-10-14"
reading_time_minutes: 2
keywords: [information schedule, create information schedule, schedule category]
breadcrumb: [Schedule types in conflict detection, Conflict detection, Configure, Change Management, IT Service Management]
---

# Create an information schedule

Create an information schedule to record events such as holidays or organizational events that change teams should be aware of. Conflict detection doesn't create conflict records for information schedules.

## Before you begin

Role required: itil\_admin or admin

The [Change Management - Collision Detector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ActivateConflictDetection.md) plugin \(com.snc.change.collision\) must be active.

## About this task

The Information Schedule \[cmn\_schedule\_information\] table extends the Condition Schedule \[cmn\_schedule\_condition\] table, the same as blackout and maintenance schedules. Information schedules use the same fields as blackout and maintenance schedules.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Schedules** &gt; **Information Schedules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For the **Name**, **Description**, **Time zone**, **Source**, **Applies to**, and **Condition** fields, see [Create blackout and maintenance schedules in Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_CreateBlkoutMaintSched.md).

<table id="table-information-schedule-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Type of event that the schedule records. The available options are:-   Holiday
-   Global event
-   Organisational event
This field is empty by default. The category is stored only after you select a value and save the schedule.

</td></tr><tr><td>

Assignment group

</td><td>

Group that owns the schedule.

</td></tr><tr><td>

Assigned to

</td><td>

User who owns the schedule. This field depends on the **Assignment group** field.

</td></tr></tbody>
</table>4.  Open the form context menu and select **Save**.

5.  Create one or more schedule entries.

    1.  In the Schedule Entries related list, select **New**.

    2.  Enter a unique name and define the time of the event.

        For more information about schedule entry fields, see [Schedule entry fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_ScheduleEntryFields.md).


## Result

The information schedule is created. Conflict detection doesn't create conflict records for this schedule.

**Parent Topic:**[Schedule types in conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/schedule-types-conflict-detection.md)

**Related topics**  


[Schedule types in conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/schedule-types-conflict-detection.md)

[Schedule categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/schedule-categories-reference.md)

[Create blackout and maintenance schedules in Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_CreateBlkoutMaintSched.md)

