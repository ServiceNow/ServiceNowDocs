---
title: Create a schedule plan
description: Create a schedule plan to assign employees, spaces, and employee-space mappings for your projects.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2024-09-11"
reading_time_minutes: 3
breadcrumb: [Working with Schedule Planning, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Create a schedule plan

Create a schedule plan to assign employees, spaces, and employee-space mappings for your projects.

## Before you begin

**Important:** The admin must set a value for the **sn\_wsd\_core.ALLOCATION\_TYPE** property to enable schedule planning.

You can create schedule plans for projects that are assigned to you. Projects can be assigned to a user from the following fields:

-   **Primary contact** field of the department
-   **Manager** field of the cost center
-   **Managed by group** or **Managed by** field of the workplace entity

Only one of the fields is considered for the project list based on the **sn\_wsd\_core.ALLOCATION\_TYPE** property. For example, if the allocation type is Department, the project list only displays the departments that you are the primary contact for.

Role required: sn\_wsd\_spcmgmt.project\_owner

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center by navigating to **Workspaces** &gt; **Workplace Central**.

2.  Select the **Schedule Planner** icon \(![Schedule Planner icon.](../images/schedule-plan-icon.png)\).

3.  On the Schedule Plans list, select **Create schedule plan**.

4.  On the details page, fill in the fields, then select **Next**.

    For a description of the field values, see [Schedule Plan details form](../reference/schedule-plan-details-form.md).

    A schedule plan record is created in the **Draft** state.

5.  On the User selection page, select the users that you want to include in the schedule plan, then select **Next**.

    The user selection limit is based on the value of the **WSMConstants.SCHEDULE\_PLAN.USER\_SELECTION\_LIMIT** constant. The default selection limit is 1000.

    **Note:** If the **sn\_wsd\_core.ALLOCATION\_TYPE** property is set to Department or Cost Center, the users are displayed from the Users \[sys\_user\] table. If the property is set to Workplace Entity, the users are displayed from the User Workplace Profile \[sn\_wsd\_core\_workplace\_profile\] table.

6.  On the Space selection page, select the workspaces that you want to include in the schedule plan, then select **Next**.

    The space selection limit is based on the value of the **WSMConstants.SCHEDULE\_PLAN.SPACE\_SELECTION\_LIMIT** constant. The default selection limit is 1000.

    **Note:** The spaces are displayed from the Allocation \[sn\_wsd\_spcmgmt\_location\_cc\_dept\_map\] table.

7.  After the system creates a mapping for the users and workspaces, select **Validate**.

    **Note:** The mapping for users and spaces is generated randomly. You can modify the mapping by editing the user and workspace columns.

    Based on the selected workspaces and users, the system may prompt you to resolve warnings and errors. The schedule plan can be created with warnings. However, you must fix the errors to create the schedule plan.

    You can view the error or warning in the **Validation Issues** column.

<table id="table_a11_zhs_xcc"><thead><tr><th>

Validation issue

</th><th>

Issue type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Not Found

</td><td>

Error

</td><td>

The user field mapped to the space is empty.Map a user to the space to resolve the error.

</td></tr><tr><td>

Space Not Found

</td><td>

Error

</td><td>

The space field mapped to the user is empty.Map a space to the user to resolve the error.

</td></tr><tr><td>

User Entry Duplicated

</td><td>

Warning

</td><td>

The user is mapped to multiple spaces.

</td></tr><tr><td>

Space Entry Duplicated

</td><td>

Warning

</td><td>

The space is mapped to multiple users.

</td></tr></tbody>
</table>8.  Resolve the errors and warnings, then select **Create plan**.


## Result

The schedule plan record is moved to the **In Progress** state. The system takes some time to assign the workspaces to the workplace profile of the users. You can view the progress in the Assignments tab.

If a user has an existing Workplace Profile Location Assignment, the schedule plan creates a non-primary location assignment. If a user does not have a workplace profile, the system creates a workplace profile and a primary location assignment.

After a schedule plan is published, the selected users receive an email with details about their workspace assignment and the start and end date of the schedule.

**Parent Topic:**[Working with Schedule Planning](../concept/working-with-schedule-planning.md)

