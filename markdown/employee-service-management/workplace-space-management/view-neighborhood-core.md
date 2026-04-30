---
title: View neighborhoods in Workplace Core
description: View existing neighborhoods with assigned spaces and user allocation.
locale: en-US
release: yokohama
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2026-01-09"
reading_time_minutes: 4
breadcrumb: [Managing Neighborhoods, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# View neighborhoods in Workplace Core

View existing neighborhoods with assigned spaces and user allocation.

## Before you begin

Role required: admin

## Procedure

1.  To view existing neighborhoods with assigned spaces and user allocation, navigate to **All** &gt; **Workplace Core** &gt; **Neighborhood** &gt; **All**.

2.  Select a neighborhood, then add spaces from a group, cost center, or department, by selecting **Assign spaces**.

3.  On the form, fill in the fields.

<table id="table_inj_wgg_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Neighborhood

</td><td>

Neighborhood name that the spaces are assigned to.

</td></tr><tr><td>

Table

</td><td>

By default, the following tables are available. -   Cost Center/Department \[sn\_wsd\_spcmgmt\_location\_cc\_dept\_map\]
-   Room \[sn\_wsd\_core\_room\]
-   Room \[sn\_wsd\_core\_room\]


</td></tr><tr><td>

Filter

</td><td>

Filter to show the number of matching records that match the conditions in the condition builder.The space planner can assign spaces in a neighborhood based on department, business unit, cost center, or group.

For more information about filters, see [Filter condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

State

</td><td>

The space assignment request state moves from **Open** to **Work in progress** and then when spaces are assigned, the state moves to **closed**.

</td></tr><tr><td>

Workplace task sub type

</td><td>

-   **Append**: Add this space to an existing list of spaces in a neighborhood.
-   **Remove all and replace**: Available spaces are removed \(already available spaces on the **Spaces** tab\) from a neighborhood. Add new spaces that match the filter condition builder.


</td></tr></tbody>
</table>4.  Select **Submit**.

    The **Space Assignment Tasks** related list shows the newly assigned space.

5.  To edit, select a space, change the required details, and select **Update**.

6.  After making the required changes, select **Save**.

7.  Assign users to spaces by selecting the **User Assignment Rules** tab.

    You can also select **All** &gt; **Neighborhood** &gt; **Assign Employees** to assign a workplace user to a department, group, or cost center.

8.  Create a new user assignment task by selecting **New**.

    On the form, fill in the fields.

<table id="table_tll_rhg_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the user assignment rule.

</td></tr><tr><td>

Neighborhood

</td><td>

Neighborhood field. Select a neighborhood using the lookup list icon \(![Lookup list icon](../../workplace-case-mgmt/image/search-icon.png)\) to search for available neighborhoods.

</td></tr><tr><td>

Building

</td><td>

Building that the user is assigned to in a neighborhood. Only buildings that are part of a selected neighborhood can be selected.

</td></tr><tr><td>

Floor

</td><td>

Floors in a selected building.

</td></tr><tr><td>

Table

</td><td>

By default, the **sys\_user** table is selected.User criteria reference various user fields \(from the User \[sys\_user\] table\), such as department, cost center, and group.

</td></tr><tr><td>

Filter

</td><td>

Add filter conditions using the condition builder to assign users to a cost center or department. For example: **Cost center is Finance**.

</td></tr><tr><td>

Active

</td><td>

Option to make users active in a neighborhood.

</td></tr></tbody>
</table>9.  Select **Submit**.

    The employee is added \(auto-assigned\) to a selected neighborhood. Employees belonging to an indicated hierarchy \(auto-assigned\), or employees that are added manually \(on demand\) can interact with a neighborhood.

10. Select the **Execute User Assignments** tab to trigger all assignment rules \(users to added or removed space allocation\) to this neighborhood directly.

    ![Neighborhood with assigned users and spaces](../images/neighborhood-auto-assigned.png "Neighborhood showing allocated spaces and users")

    **Note:** Neighborhood assignments are applicable if **Neighborhood** is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.

    By default, the **Execute User Assignment** scheduled job runs daily or weekly on an instance. You may want to run it for the first time directly. When you run the scheduled job for each user, a workplace profile record is created \(if it's not in your instance already\), and the neighborhood is assigned to that workplace profile.

    -   When an employee is assigned to a neighborhood, a workplace profile is created.
    -   Neighborhoods are assigned to a workplace profile, even if an employee has multiple workplace profiles. All neighborhood assignments are done only on one workplace profile.
    -   An employee can be assigned to multiple neighborhoods. Each assignment is a separate record in the Workplace Profile Location Assignment Related list on the workplace profile form.
    -   The changes are captured in the execution details table and the changes are mentioned as type **Allocation**.
    -   If new spaces are assigned to a neighborhood, the spaces are updated in the neighborhood record.
    -   If spaces are removed from a neighborhood, the neighborhood record is updated when you run the execute user assignment task.

        Workplace Profile records are updated, added, or removed. A move task is initiated for employees who have a new space allocation and who are moved from one floor to another.

11. To create and manage a neighborhood in Workplace Central for a scenario, see [Create a scenario](../../workplace-central/task/create-a-scenario.md).

12. To view and reserve spaces in a neighborhood using the Reservation Management portal, see [Create neighborhood reservations](../../wsd-reservation-management/task/create-neighborhood-reservations.md).

13. To add a user to the neighborhood, refer to [Add a user to the neighborhood](add-a-user-to-neighbourhood.md).


