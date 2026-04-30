---
title: Detect conflicts manually and review conflict details
description: Run conflict detection manually for a change request and cancel conflict detection before it completes. Review the conflicts detected either automatically or manually and resolve them by changing the schedules.Cancel any conflict detection jobs that are actively running for a change request if you want to make any modifications to the schedules. After modifying the schedules, you can rerun the check conflicts action again to identify potential conflicts.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Detect conflicts manually and review conflict details

Run conflict detection manually for a change request and cancel conflict detection before it completes. Review the conflicts detected either automatically or manually and resolve them by changing the schedules.

## Before you begin

Before you can run conflict detection for a change request, the following fields must be completed in the change record.

-   **Configuration item**, except in advanced mode. In advanced mode, the **Affected CIs** field is required instead.
-   **Planned start date** of the change request.
-   **Planned end date** of the change request.

For more information about running conflict detection automatically, see [Enable automatic change conflict detection](t_RunAutomatedConflictDetection.md).

Prior to running conflict detection, consider the following scenarios unique to your organization.

-   **CMDB list size and relationship complexities**

    If you have a large organization with a large CMDB, conflict detection can take longer to complete.

-   **Inactive changes are not evaluated**

    Conflict detection does not evaluate inactive changes when determining conflicting changes.

-   **Advanced mode conflict checking is disabled by default**

    When you upgrade the application, advanced mode conflict checking is disabled by default and affected CIs are not considered during conflict detection. To evaluate all the CIs, set the mode to **Advanced**.


Role required: itil or sn\_change\_write

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  From the list of change requests, open the desired change request.

3.  Click the **Conflicts** tab or scroll to the bottom the form to find the **Conflicts** tab.

4.  Click **Check Conflicts**.

5.  When the conflict detection is completed, click **Close** in the pop-up window.

    Conflicts appear in the Conflicts Detected list on the **Conflicts** tab. The **Conflict status** and **Conflict last run** fields on the change request record are also updated.

6.  In the Conflicts Detected list, review the list of conflicts that appear.

<table id="table_inx_bpg_ys"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conflicting change

</td><td>

The change that is in conflict with the scheduled change, if any.

</td></tr><tr><td>

Affected CI

</td><td>

The affected CI associated with the change.

</td></tr><tr><td>

Last Checked

</td><td>

The last time the conflicts were checked. The **Last Checked** field is automatically updated.

</td></tr><tr><td>

Related CI

</td><td>

The parent CI or child CI of the current CI, if the CI has caused a conflict.

</td></tr><tr><td>

Schedule

</td><td>

The name of the maintenance window or blackout window that is causing the conflict, if any.

</td></tr><tr><td>

Type

</td><td>

The issue that caused the conflict.

-   **CI Already Scheduled**
-   **Parent CI Already Scheduled**
-   **Child CI Already Scheduled**
-   **Not in Maintenance Window**
-   **Parent Not In Maintenance Window**
-   **Child Not In Maintenance Window**
-   **Blackout**


</td></tr></tbody>
</table>
## Result

You can review the conflicts and the affected CIs in the Conflicts Detected list and reschedule the change to resolve the conflicts.

**Parent Topic:**[Conflict detection](../concept/c_ConflictDetection.md)

**Related topics**  


[Detect change conflicts](configure-conflict-properties.md#)

[Create blackout and maintenance schedules in Change Management](t_CreateBlkoutMaintSched.md)

[Configure a change request to monitor outside maintenance schedule conflicts](monitor-maintenance-schedule.md)

[Conflict calendar](../concept/change-conflict-calendar.md)

[Enable automatic change conflict detection](t_RunAutomatedConflictDetection.md)

## Cancel conflict detection manually

Cancel any conflict detection jobs that are actively running for a change request if you want to make any modifications to the schedules. After modifying the schedules, you can rerun the check conflicts action again to identify potential conflicts.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Open the change request that you want to cancel conflict checking for.

3.  Click the **Conflicts** tab.

4.  Click **Check Conflicts**.

    The Checking conflicts progress status pop-up window appears.

5.  To cancel conflict detection, click **Cancel**.

    The active conflict detection job is canceled and all conflicts displayed in the Conflicts section are cleared. The **Conflict Status** field displays a **Not Run** status.

    **Note:** If you set conflict detection to run automatically or on a scheduled basis, the future executions of conflict detection against the same change request record are not canceled.


