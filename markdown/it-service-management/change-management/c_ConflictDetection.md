---
title: Conflict detection
description: Conflict detection identifies potential scheduling conflicts for a change request based on the configuration items, and planned start and end date or the change. If a scheduling conflict exists, conflict detection also checks any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Conflict detection

Conflict detection identifies potential scheduling conflicts for a change request based on the configuration items, and planned start and end date or the change. If a scheduling conflict exists, conflict detection also checks any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict.

Conflict detection identifies conflicts for any of the following reasons:

-   The configuration items \(CIs\) are already scheduled at the given date and time.
-   A parent or child of the CI is already scheduled at the given date and time.
-   The CI is not in the maintenance window.
-   A parent or child of the CI is not in the maintenance window.
-   The CI is in a blackout window.
-   A parent or child of the CI is in a blackout window.
-   The CI is assigned to a person already scheduled at the given date and time.

Using the **change.conflict.useprogressworker** system property, the conflict detection process can now be managed in two ways. By default, the value of this property is set as false, and conflict detection is executed using the Change Management Worker table and the Change - Conflict Detection flow.

If you set the value of this property as true, conflict detection uses Progress Workers instead, as it used previously.

You can also manually execute conflict detection. For more information, see [Detect conflicts manually and review conflict details](../task/t_RunManualConflictDetection.md#).

## Conflict detection process

Conflict detection can run automatically when you provide values for the Configuration item, planned start and end date fields. It can also run when the values in any one of these fields are updated, or when values for these fields are available and the state of the change request is updated.

When the value in the **change.conflict.useprogressworker** system property is set to false, the Change Management Worker \(chg\_mgt\_worker\) table can be used to track the execution of conflict detection for a change request. You can view the associated Change - Conflict Detection flow by selecting Show Flows on the change form.

When Conflicts are identified, the conflict status and conflict last run fields are updated to reflect the outcome. Conflicts can be reviewed in the Conflict section of the change request form.

## Conflict Calendar

You can choose to display a conflict calendar to view identified scheduling conflicts. For more information, see [Conflict calendar](change-conflict-calendar.md)

-   **[Detect change conflicts](../task/configure-conflict-properties.md#)**  
Detect change conflicts by setting Change Management conflict analysis properties. Use the resulting information to calculate conflicts for change requests and review and modify the change to eliminate conflicts.
-   **[Create blackout and maintenance schedules in Change Management](../task/t_CreateBlkoutMaintSched.md)**  
Use the Blackout and Maintenance windows to schedule a change. Blackout windows specify times during which normal change activity should not be scheduled. Maintenance windows specify times during which change requests should be scheduled. For example, create a blackout schedule for code freezes at the end of the year. blackout-maintenance-schedule
-   **[Configure a change request to monitor outside maintenance schedule conflicts](../task/monitor-maintenance-schedule.md)**  
When a change request is configured to display the conflicts that are outside the maintenance schedule, conflict detection indicates whether the planned start and end dates occur outside the maintenance window or not. By reviewing the conflicts that are detected, you can modify the change schedule.
-   **[Conflict calendar](change-conflict-calendar.md)**  
The conflict calendar graphically represents the potential scheduling conflicts for a change request. Conflicts are identified as active change requests, blackout schedules, and changes scheduled outside maintenance schedules. Use the **Scheduling Assistant** to resolve any schedule conflicts.
-   **[Enable automatic change conflict detection](../task/t_RunAutomatedConflictDetection.md)**  
Automate conflict detection to run at specific intervals or when a change request is updated to immediately review the conflicts when the schedule dates are updated.
-   **[Detect conflicts manually and review conflict details](../task/t_RunManualConflictDetection.md#)**  
Run conflict detection manually for a change request and cancel conflict detection before it completes. Review the conflicts detected either automatically or manually and resolve them by changing the schedules.

**Parent Topic:**[Configuring Change Management](configure-change-management.md)

