---
title: Enable automatic change conflict detection
description: Automate conflict detection to run at specific intervals or when a change request is updated to immediately review the conflicts when the schedule dates are updated.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Enable automatic change conflict detection

Automate conflict detection to run at specific intervals or when a change request is updated to immediately review the conflicts when the schedule dates are updated.

## Before you begin

Prior to running conflict detection, consider the following scenarios:

-   **CMDB list size and relationship complexities**

    If you have a large organization with a large CMDB, conflict detection can take longer to complete.

-   **Inactive changes are not evaluated**

    Conflict detection does not evaluate inactive changes when determining conflicting changes.

-   **Advanced mode conflict checking is disabled by default**

    When you upgrade the application, advanced mode conflict checking is disabled by default and affected CIs are not considered during conflict detection. To evaluate all CIs, set the mode to **Advanced**.


Role required: change\_manager or admin

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Conflict Properties**.

2.  Select one of the following options.

<table id="choicetable_kz3_j3d_3t"><tbody><tr><td id="d71782e112">

**Run conflict detection automatically after changes to Configuration item, Planned start date, Planned end date, or State when a change request is updated**

</td><td>

When selected, runs conflict detection automatically when a change to one or more of the following fields on the change request record is saved.-   **Configuration item**
-   **Planned start date**
-   **Planned end date**
-   **State**


</td></tr><tr><td id="d71782e140">

**Enable the scheduled change conflict checker**

</td><td>

When selected, runs the following conflict detection scheduled jobs at these intervals: **Change Conflict Detection &lt; 1 Week Away** is scheduled every day.

 **Change Conflict Detection &lt; 1 Month Away** is scheduled every two days.

 **Change Conflict Detection &gt;=1 Month Away** is scheduled every seven days.

</td></tr></tbody>
</table>3.  Click **Save**.

    You can view the conflicts on the **Conflicts** tab on the change request record.


**Parent Topic:**[Conflict detection](../concept/c_ConflictDetection.md)

**Related topics**  


[Detect change conflicts](configure-conflict-properties.md#)

[Create blackout and maintenance schedules in Change Management](t_CreateBlkoutMaintSched.md)

[Configure a change request to monitor outside maintenance schedule conflicts](monitor-maintenance-schedule.md)

[Conflict calendar](../concept/change-conflict-calendar.md)

[Detect conflicts manually and review conflict details](t_RunManualConflictDetection.md#)

