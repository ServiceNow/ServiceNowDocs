---
title: Configure a change request to monitor outside maintenance schedule conflicts
description: When a change request is configured to display the conflicts that are outside the maintenance schedule, conflict detection indicates whether the planned start and end dates occur outside the maintenance window or not. By reviewing the conflicts that are detected, you can modify the change schedule.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Configure a change request to monitor outside maintenance schedule conflicts

When a change request is configured to display the conflicts that are outside the maintenance schedule, conflict detection indicates whether the planned start and end dates occur outside the maintenance window or not. By reviewing the conflicts that are detected, you can modify the change schedule.

## Before you begin

Role required: personalize\_ui or admin

## About this task

The Outside maintenance schedule check box is informational and the instance sets this value and disregards any changes that you make to this check box. The check box is selected by default if either of the following actions occur.

-   The planned start and end dates in the change request with an associated configuration item \(CI\) are compared to the maintenance schedule and are determined to be outside the schedule.
-   Affected CIs associated with the change request are checked against their assigned maintenance schedules, if any.

**Note:** Only the maintenance window for the primary CI or affected CIs is checked; the upstream and downstream items are not checked.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open** and select an existing change request.

2.  If the **Outside maintenance schedule** field does not appear, add the field to the form.

    1.  Click the context menu icon and then click **Additional actions** &gt; **Configure** &gt; **Form Layout**.

    2.  Move **Outside maintenance schedule** to the Selected list.

    3.  Click **Save**.


## Result

When you save a change request that is outside the maintenance schedule, a warning appears for each item \(primary or affected\). This warning also displays the planned dates that fall outside the maintenance window.

**Parent Topic:**[Conflict detection](../concept/c_ConflictDetection.md)

**Related topics**  


[Detect change conflicts](configure-conflict-properties.md#)

[Create blackout and maintenance schedules in Change Management](t_CreateBlkoutMaintSched.md)

[Conflict calendar](../concept/change-conflict-calendar.md)

[Enable automatic change conflict detection](t_RunAutomatedConflictDetection.md)

[Detect conflicts manually and review conflict details](t_RunManualConflictDetection.md#)

