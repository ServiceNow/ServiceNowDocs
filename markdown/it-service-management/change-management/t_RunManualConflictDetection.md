---
title: Detect conflicts manually and review conflict details
description: Run conflict detection manually for a change request. Review the conflicts detected either automatically or manually and resolve them by changing the schedules.Cancel any conflict detection jobs that are actively running for a change request if you want to make any modifications to the schedules. After modifying the schedules, you can rerun the check conflicts action again to identify potential conflicts.Exclude change records from being displayed as a potential conflict in the conflict detection process.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Detect conflicts manually and review conflict details

Run conflict detection manually for a change request. Review the conflicts detected either automatically or manually and resolve them by changing the schedules.

## Before you begin

Before you can run conflict detection for a change request, the following information must be provided in the change record:

-   The configuration item in either the **Configuration item** field or in advanced mode the **Affected CIs** field.
-   The planned start date, provided in the **Planned start date** field.
-   The planned end date, in the **Planned end date** field.

**Note:** The conflict detection feature is unavailable if the **Exclude from conflict detection** check box in the Change Request form is selected. For more information, see [.](t_RunManualConflictDetection.md#)

For information about running conflict detection automatically, see [Enable automatic change conflict detection](t_RunAutomatedConflictDetection.md).

Prior to running conflict detection, consider the following scenarios:

-   **CMDB list size and relationship complexities**

    If you have a large organization with a large CMDB, conflict detection can take longer to complete.

-   **Inactive changes are not evaluated**

    Conflict detection does not evaluate inactive changes when determining conflicting changes.

-   **Advanced mode conflict checking is disabled by default**

    When you upgrade the application, advanced mode conflict checking is disabled by default and affected CIs are not considered during conflict detection. To evaluate all CIs, set the mode to **Advanced**.


Role required: itil or sn\_change\_write

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Select the change request.

3.  Select the **Conflicts** tab.

4.  Select **Check Conflicts**.

5.  When the conflict detection pop-up window is displayed, click **Close**.

    Conflicts appear in the Conflicts Detected list on the **Conflicts** tab. The **Conflict status** and **Conflict last run** fields on the change request record are also updated.

6.  In the Conflicts Detected list, review the list of conflicts.

<table id="table_inx_bpg_ys"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Conflicting change

</td><td>

Change that is in conflict with the scheduled change, if any.

</td></tr><tr><td>

Affected CI

</td><td>

Affected CI associated with the change.

</td></tr><tr><td>

Last Checked

</td><td>

The last time the conflicts were checked. The **Last Checked** field is automatically updated.

</td></tr><tr><td>

Related CI

</td><td>

Parent CI or child CI of a current CIthat has caused a conflict.

</td></tr><tr><td>

Schedule

</td><td>

Maintenance window or blackout window causing the conflict, if any.

</td></tr><tr><td>

Type

</td><td>

Issue that caused the conflict. The available types are:

-   CI Already Scheduled
-   Parent CI Already Scheduled
-   Child CI Already Scheduled
-   Not in Maintenance Window
-   Parent Not In Maintenance Window
-   Child Not In Maintenance Window
-   Blackout


</td></tr></tbody>
</table>
## What to do next

Resolve any conflicts and reschedule the change.

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


## Exclude change requests from conflict detection

Exclude change records from being displayed as a potential conflict in the conflict detection process.

### Before you begin

Role required: change\_manager

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Select an existing change request.

3.  In the form context menu, select **Configure** &gt; **** &gt; **Form layout**.

4.  Add the **Exclude from conflict detection** field to the change request form.

    For information on the procedure to add a new field to a form, see Configuring the form layout.


### Result

The **Exclude from conflict detection** check box is added to the Change Request form. When the check box is selected in the change request form, the **Check conflicts** option is inactive, and the change request is excluded from the conflict detection process. The change request is also excluded from being displayed as a conflict when conflict detection is run on other change records.

