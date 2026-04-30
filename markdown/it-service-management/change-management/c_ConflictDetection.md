---
title: Conflict detection
description: Conflict detection identifies potential scheduling conflicts for a change request based on the configuration items \(CIs\), planned start date, and the planned end date in scope for the change. If a scheduling conflict exists, conflict detection also checks any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Conflict detection

Conflict detection identifies potential scheduling conflicts for a change request based on the configuration items \(CIs\), planned start date, and the planned end date in scope for the change. If a scheduling conflict exists, conflict detection also checks any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict.

Conflict detection identifies conflicts for any of the following reasons:

-   The CIs are already scheduled at the given date and time.
-   A parent of the CI is already scheduled at the given date and time.
-   A child of the CI is already scheduled at the given date and time.
-   The CI is not in the maintenance window.
-   A parent of the CI is not in the maintenance window.
-   A child of the CI is not in the maintenance window.
-   The CI is in a blackout window.
-   A parent of the CI is in a blackout window.
-   A child of the CI is in a blackout window.
-   The assigned to person is already scheduled at the given date and time.

If conflicts are identified, the **Conflict status** field is updated to reflect a conflict and an error message directs you to the Conflict form section of the Change request record to review conflicts. When you create a change request and provide a CI, planned start date, and planned end date, or update any of these values, conflict detection is executed automatically.

You can choose to show or hide the conflict error message by using the **Enable/Disable Scheduling Conflict Message** menu item from the context menu. As an admin, you can configure the message display setting using the **change.conflict.show\_conflict\_message** property. For more information on the property, see [Conflict analysis properties](../task/configure-conflict-properties.md#).

You can manually execute conflict detection. For more information, see [Detect conflicts manually and review conflict details](../task/t_RunManualConflictDetection.md#).

The Conflicts form section lists specific conflict details including the type of conflict, conflicting schedule, or conflicting change request. If a conflict must be resolved before requesting approval, modify the **Planned start date** and **Planned end date** fields in the Schedule form section.

## Conflict Calendar

You can also use the [Conflict calendar](change-conflict-calendar.md) to visually display any scheduling conflicts identified. To reschedule the change request, click the change request record or drag the change request to another time within the calender.

-   **[Configure conflict analysis properties](../task/configure-conflict-properties.md#)**  
Configure Change Management conflict analysis properties to detect change conflicts. Use the relevant information to calculate conflicts for change requests and review and modify the change to eliminate conflicts.
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

