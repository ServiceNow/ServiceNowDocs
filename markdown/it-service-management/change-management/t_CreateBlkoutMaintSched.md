---
title: Create blackout and maintenance schedules in Change Management
description: Use the Blackout and Maintenance windows to schedule a change. Blackout windows specify times during which normal change activity should not be scheduled. Maintenance windows specify times during which change requests should be scheduled. For example, create a blackout schedule for code freezes at the end of the year. blackout-maintenance-schedule
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/change-management/t\_CreateBlkoutMaintSched.html
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Create blackout and maintenance schedules in Change Management

Use the Blackout and Maintenance windows to schedule a change. Blackout windows specify times during which normal change activity should not be scheduled. Maintenance windows specify times during which change requests should be scheduled. For example, create a blackout schedule for code freezes at the end of the year. blackout-maintenance-schedule

## Before you begin

Role required: itil\_admin or admin

Ensure that the [Change Management - Collision Detector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/t_ActivateConflictDetection.md) \(com.snc.change.collision\) plugin is activated.

## About this task

Conflict detection uses blackout and maintenance schedules to find potential scheduling conflicts for the configuration items \(CIs\) associated with a change request. When conflict detection runs, either automatically or by manual request, conflict detection determines if either type of defined schedule applies to the change request. If a potential conflict is identified, a warning message appears and conflicts are listed within the Conflict form section. View conflicts in the [Conflict calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/change-conflict-calendar.md).

**Note:** To use the business service as the source for a blackout or maintenance schedule, the business service must be converted to an application service. For instructions, see [Convert business services to application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/convert-bus-to-app-svc-intro.md). For information about application services, see [Application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/application-services.md).

Conflict detection evaluates both the parent and child configuration items \(CIs\) of any CI in scope. A blackout or maintenance schedule applied to an upstream service, or CI also captures downstream child CIs that appear in change requests. For the full list of relationships that trigger a conflict, see [Conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/c_ConflictDetection.md).

## Procedure

1.  Create a blackout or maintenance schedule.

<table id="choicetable_p11_g2d_3t"><tbody><tr><td id="d340845e106">

**Create a blackout schedule**

</td><td>

1.  Navigate to **Change** &gt; **Schedules** &gt; **Blackout Schedules**.
2.  Click **New**.


</td></tr><tr><td id="d340845e139">

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

Source of the blackout or maintenance schedule. Select one of the following options to scope the schedule:-   **Service**: Applies the schedule to an application service. The business service must be converted to an application service to be available as a source.
-   **Change Request**: Applies the schedule to change requests that match the conditions you define.
-   **CI Class**: Applies the schedule to a configuration item \(CI\) class and its child classes. This option enables the **Applies to** field for selecting the CI class.
**Note:** When you select **Service** or **Change Request** from the Source list, the **Applies to** field does not appear. The **Applies to** field appears if you select **CI Class** as the Source, which in turn enables the selection of a **CI Class**.

</td></tr><tr><td class="sub-head" colspan="2">

**Choosing a Source**

</td></tr><tr><td>

When to use each source

</td><td>

Use **Service** when the schedule must cover every CI that supports a given application service.Use **Change Request** when the schedule applies to a defined set of change requests rather than to CIs.

Use **CI Class** when the schedule applies broadly to a class of CIs and its children.

The selected source determines which fields, such as **Applies to**, appear on the form, and how conflict detection evaluates the schedule. For details, see [Conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/c_ConflictDetection.md).

</td></tr><tr><td>

Applies to

</td><td>

CI classification that the conflict detection is filtered on. You can select a dynamic CI group so that all the configuration items in that dynamic CI group will be taken into account for blackout and maintenance when conflict detection is run.

 The dynamic CI group is seen as the parent CI to all the CIs that are within that group. If there are scheduling conflicts related to any of the CIs in the dynamic group, the conflict will be shown in the conflicts table of the dynamic CI group.

</td></tr><tr><td>

Condition

</td><td>

Conditions to specify the CIs that the schedule applies to.Use this field to scope a blackout against a set of CIs. For example, all CIs in a class that meet a chosen attribute.

This field does not appear when the **Applies to** field is set to **None**.

To exclude specific change

 **Note:** Related fields used in conditions are not evaluated for blackout or maintenance schedules.

</td></tr></tbody>
</table>3.  Open the form context menu and select **Save**.

    A blackout or maintenance schedule is created and the Schedule Entries, Child Schedules, and Referenced By related lists appear in the change.

    **Note:**

    The Blackout Schedule \[cmn\_schedule\_blackout\] table extends the Condition Schedule \[cmn\_schedule\_condition\] table, which in turn extends the Schedule \[cmn\_schedule\] table. The Blackout Schedule table inherits the domain properties from the Schedule table which has the Domain and Domain path columns.

    Because the Blackout schedule table uses the same Child Schedule and Schedule Entry tables as the Schedule table uses, the domain support is identical. The **domain\_master** attribute is used to derive the domain from a parent record. For more information, see [Domain support for schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/domain-support-for-schedules.md).

4.  Create one or more schedule entries by completing the following steps:

    1.  In the Schedule Entries related list of the new maintenance schedule, select **New**.

    2.  Enter a unique name and define the time during which you want to schedule the maintenance.

        For more information about the schedule entries field, see [Schedule entry fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_ScheduleEntryFields.md).

    **Note:** To delete the schedule created, select **Delete**. If you delete a schedule, the child schedules and schedule entries associated with the schedule would be deleted automatically.

5.  **Optional**: Add a child schedule to refine the blackout coverage.

    1.  In the child schedules related list, select **New**.

    2.  Define the child schedule for the specific set of CIs or time window you want to add under this blackout.

        A child schedule inherits from the parent blackout and lets you apply a more specific window to a subset of CIs.


## Result

A blackout or maintenance schedule is created.

**Important:** Conflict detection evaluates not only the CI explicitly named in a change request, but also its parent and child CIs by walking the relationships defined in the configuration management database \(CMDB\). As a result, a schedule you apply to an upstream business service or CI also covers the downstream CIs associated with that service or CI. For example, a blackout schedule on a payment service captures a change request that targets a database CI that supports that service, because the database is a child of the service.

To scope a schedule by CI class and its children, set **Source** to **CI Class** and select a class in the **Applies to** field. The schedule then applies to all CIs in that class and any child classes.

## What to do next

Associate the configuration item with the maintenance schedule that is used in the change request.

-   **[Assign a maintenance schedule to configuration items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/use-maintenance-schedule-management.md)**  
You can review and determine the conflicts in a change schedule by assigning the maintenance schedules to configuration items \(CI\). After you assign a maintenance schedules to the CI, add the CI to the change request.

**Parent Topic:**[Conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/c_ConflictDetection.md)

**Related topics**  


[Detect change conflicts]()

[Configure a change request to monitor outside maintenance schedule conflicts]()

[Conflict calendar]()

[Enable automatic change conflict detection]()

[Detect conflicts manually and review conflict details]()

[Define a schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_DefineASchedule.md)

[Schedule entry fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/r_ScheduleEntryFields.md)

[Parent and child schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/c_ParentAndChildSchedules.md)

