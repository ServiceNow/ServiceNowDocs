---
title: Create blackout and maintenance schedules in Change Management
description: Use the Blackout and Maintenance windows to schedule a change. Blackout windows specify times during which normal change activity should not be scheduled. Maintenance windows specify times during which change requests should be scheduled. For example, create a blackout schedule for code freezes at the end of the year. blackout-maintenance-schedule
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Create blackout and maintenance schedules in Change Management

Use the Blackout and Maintenance windows to schedule a change. Blackout windows specify times during which normal change activity should not be scheduled. Maintenance windows specify times during which change requests should be scheduled. For example, create a blackout schedule for code freezes at the end of the year. blackout-maintenance-schedule

## Before you begin

Role required: itil\_admin or admin

Ensure that the [Change Management - Collision Detector](t_ActivateConflictDetection.md) \(com.snc.change.collision\) plugin is activated.

## About this task

Conflict detection uses blackout and maintenance schedules to find potential scheduling conflicts for the configuration items \(CIs\) associated with a change request. When conflict detection runs, either automatically or by manual request, conflict detection determines if either type of defined schedule applies to the change request. If a potential conflict is identified, a warning message appears and conflicts are listed within the Conflict form section. View conflicts in the [Conflict calendar](../concept/change-conflict-calendar.md).

**Note:** To use the business service as the source for a blackout or maintenance schedule, the business service must be converted to an application service. For instructions, see [Convert business services to application services](https://www.servicenow.com/docs/access?context=convert-bus-to-app-svc-intro&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). For information about application services, see [Application services](https://www.servicenow.com/docs/access?context=application-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Create a blackout or maintenance schedule.

<table id="choicetable_p11_g2d_3t"><tbody><tr><td id="d332183e97">

**Create a blackout schedule**

</td><td>

1.  Navigate to **Change** &gt; **Schedules** &gt; **Blackout Schedules**.
2.  Click **New**.


</td></tr><tr><td id="d332183e130">

**Create a maintenance schedule**

</td><td>

1.  Navigate to **Change** &gt; **Schedules** &gt; **Maintenance Schedules**.
2.  Click **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_avy_xxk_xs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the schedule.

</td></tr><tr><td>

Description

</td><td>

Short description about the schedule.

</td></tr><tr><td>

Time zone

</td><td>

Time zone for the schedule.Select **Floating** to evaluate planned start and end dates on the Change Request form for the logged-in user.

</td></tr><tr><td>

Source

</td><td>

Source of the blackout or maintenance schedule. The available options are **Service**, **Change Request**, and **CI Class**.**Note:** When you select **Service** or **Change Request** from the Source list, the **Applies to** field does not appear. The **Applies to** field appears if you select **CI Class** as the Source, which in turn enables the selection of a **CI Class**.

</td></tr><tr><td>

Applies to

</td><td>

The class of CI that this schedule applies to.Specifying CI \[cmdb\_ci\] indicates that this schedule is applicable to all CIs in this class and any children of this class.

Conflict detection evaluates whether the schedule applies to a given change request, service, or CI, and the condition defined on the schedule.

</td></tr><tr><td>

Condition

</td><td>

Conditions to specify the CIs that the schedule applies to.This field does not appear when the **Applies to** field is set to **None**.

 **Note:** Related fields used in conditions are not evaluated for blackout or maintenance schedules. Condition on the schedule can only apply to one table at a time.

</td></tr></tbody>
</table>3.  Open the form context menu and click **Save**.

    A blackout or maintenance schedule is created and the Schedule Entries, Child Schedules, and Referenced By related lists appear in the change.

    **Note:**

    The Blackout Schedule \[cmn\_schedule\_blackout\] table extends the Condition Schedule \[cmn\_schedule\_condition\] table, which in turn extends the Schedule \[cmn\_schedule\] table. The Blackout Schedule table inherits the domain properties from the Schedule table which has the Domain and Domain path columns.

    Because the Blackout schedule table uses the same Child Schedule and Schedule Entry tables as the Schedule table uses, the domain support is identical. The **domain\_master** attribute is used to derive the domain from a parent record. For more information, see [Domain support for schedules](https://www.servicenow.com/docs/access?context=domain-support-for-schedules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) .

4.  Create one or more schedule entries by completing the following steps:

    1.  In the Schedule Entries related list of the new maintenance schedule, click **New**.

    2.  Enter a unique name and define the time during which you want to schedule the maintenance.

        For more information about the schedule entries field, see [Schedule entry fields](https://www.servicenow.com/docs/access?context=r_ScheduleEntryFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    **Note:** To delete the schedule created, select **Delete**. If you delete a schedule, the child schedules and schedule entries associated with the schedule would be deleted automatically.


## Result

A blackout or maintenance schedule is created.

## What to do next

Associate the configuration item with the maintenance schedule that is used in the change request.

-   **[Assign a maintenance schedule to configuration items](use-maintenance-schedule-management.md)**  
You can review and determine the conflicts in a change schedule by assigning the maintenance schedules to configuration items \(CI\). After you assign a maintenance schedules to the CI, add the CI to the change request.

**Parent Topic:**[Conflict detection](../concept/c_ConflictDetection.md)

**Related topics**  


[Configure conflict analysis properties](configure-conflict-properties.md#)

[Configure a change request to monitor outside maintenance schedule conflicts](monitor-maintenance-schedule.md)

[Conflict calendar](../concept/change-conflict-calendar.md)

[Enable automatic change conflict detection](t_RunAutomatedConflictDetection.md)

[Detect conflicts manually and review conflict details](t_RunManualConflictDetection.md#)

[Define a schedule](https://www.servicenow.com/docs/access?context=t_DefineASchedule&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Schedule entry fields](https://www.servicenow.com/docs/access?context=r_ScheduleEntryFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

[Parent and child schedules](https://www.servicenow.com/docs/access?context=c_ParentAndChildSchedules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

