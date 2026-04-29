---
title: Task SLA table
description: The Task SLA \[task\_sla\] table stores Task SLA records for the SLAs attached to particular tasks.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Task SLA table

The Task SLA \[task\_sla\] table stores Task SLA records for the SLAs attached to particular tasks.

For each task, attached SLAs are accessible in a related list on the Task's form.

![Task SLA table with two definitions](../image/TaskSLATable.png "Task SLA table")

The SLA form for a task shows further details:

![Task SLA form view](../image/TaskSLAForm.png "Task SLA form")

## Stage values

The following **Stage** values are defined:

-   **In progress**
-   **Cancelled**
-   **Paused**
-   **Completed**

**Note:** The **Breached** stage value is also available for systems either using the 2010 SLA engine, or running in compatibility mode.

## Timing information

The **Timings** fields on the Task SLA contain the crucial information powered by the SLA Engine:

<table id="tbl_TaskSLATime-BasedFields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start time

</td><td>

The time the SLA was started.

</td></tr><tr><td>

Stop time

</td><td>

The time the SLA ended.

</td></tr><tr><td>

Breach time

</td><td>

The time the SLA will breach, adjusted for business pause duration \(for task SLAs with a schedule specified\) or pause duration \(for task SLAs with no schedule\).**Note:** Breach time is the same as Planned end time.

</td></tr><tr><td>

Actual Elapsed Time

</td><td>

Time between start time and now \(minus pause duration\).

</td></tr><tr><td>

Actual Elapsed Percentage

</td><td>

Percentage of total SLA that has elapsed \(minus pause duration\).

</td></tr><tr><td>

Actual Time Left

</td><td>

Time remaining until SLA breach.

</td></tr><tr><td>

Business Elapsed Time

</td><td>

Time within the specified schedule between start time and now \(minus pause duration\).

</td></tr><tr><td>

Business Elapsed Percentage

</td><td>

Percentage of total SLA that has elapsed within the specified schedule \(minus pause duration\).

</td></tr><tr><td>

Business Time Left

</td><td>

Time within the schedule remaining until SLA breach.

</td></tr><tr><td>

Original breach time

</td><td>

The date/time the SLA would breach, as calculated when the SLA is first attached.**Note:** You may have to configure the form to see this field.

</td></tr></tbody>
</table>**Parent Topic:**[Service Level Management reference](../concept/service-level-management-reference.md)

