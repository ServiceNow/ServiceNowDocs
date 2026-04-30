---
title: Create a neighborhood for workplace users
description: Create a neighborhood and assign users to available spaces in a neighborhood. Add or remove users in bulk and allocate available neighborhood spaces to users in a department, cost center, or group.
locale: en-US
release: xanadu
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Managing Neighborhoods, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Create a neighborhood for workplace users

Create a neighborhood and assign users to available spaces in a neighborhood. Add or remove users in bulk and allocate available neighborhood spaces to users in a department, cost center, or group.

## Before you begin

**Note:** Verify that Workplace Core is installed to set up and manage neighborhoods.

**Important:** If you’re using Workplace Space Management version1.11.1 or later, to add a user to the neighborhood, refer to [Add or edit a neighborhood assignment of a workplace profile](add-a-user-to-the-neighbourhood-from-the-workplace-profile.md).

**Important:** From Workplace Space Management version 1.11.1, the **Neighbourhood User Assignments** table is no longer available. Instead, the user assignment can be performed on a workplace profile directly using the **Workplace Profile Location Assignment** table \(displayed a related list on the form\) in the Workplace Core application. The **Workplace Profile Location Assignment** in the Workplace Core is now configured with additional fields such as **Profile type**, **Neighborhood**, and **Source** where all the data is saved. This table helps a space manager to perform scenario planning and save any user assignment-related changes performed on a neighborhood directly on the workplace profile.

On a neighborhood, when you configure a user assignment rule, the neighborhood assignment changes on the workplace profile are automatically saved on the user's workplace profile. On the user's workplace profile, you can check the type of assignment from the **Profile type** field.

If you’re an existing customer, upon upgrading, the entities in the **Neighbourhood User assignments** table are automatically migrated to the **Workplace Profile Location Assignment** of the user's workplace profile.

Role required: sn\_wsd\_spcmgmt.admin, sn\_wsd\_spcmgmt.space\_planner

## About this task

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Neighborhood** &gt; **Create New**.

    You can also create a neighborhood or update an existing neighborhood by navigating to **All** &gt; **Workplace Core** &gt; **Neighborhood.**

2.  On the form, fill in the fields.

<table id="table_zvh_pgg_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the neighborhood.

</td></tr><tr><td>

Active

</td><td>

Status of the neighborhood workplace location.The availability of a workplace location for any workplace-related activities is determined based on the status that is set. For more information, see [Change the status of a workplace location](change-active-status-of-workplace-location.md).

</td></tr><tr><td>

Restricted

</td><td>

A private or restricted neighborhood.If an employee is assigned to the neighborhood by user assignment rule or is added manually \(on-demand basis\), the employee can reserve a space in the neighborhood. Otherwise, employees won’t see the neighborhoods. see [Location privacy settings and impact](../../wsd-reservation-management/reference/location-privacy-settings-and-impact.md).

</td></tr></tbody>
</table>3.  Select **Submit**.

    A neighborhood is created.

4.  To view existing neighborhoods with assigned spaces and user allocation, navigate to **All** &gt; **Workplace Core** &gt; **Neighborhood** &gt; **All**.

5.  Select a neighborhood, then add spaces from a group, cost center, or department, by selecting **Assign spaces**.

6.  On the form, fill in the fields.

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

For more information about filters, see [Filter condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

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
</table>7.  Select **Submit**.

    The **Space Assignment Tasks** related list shows the newly assigned space.

8.  To edit, select a space, change the required details, and select **Update**.

9.  After making the required changes, select **Save**.

10. Assign users to spaces by selecting the **User Assignment Rules** tab.

    You can also select **All** &gt; **Neighborhood** &gt; **Assign Employees** to assign a workplace user to a department, group, or cost center.

11. Create a new user assignment task by selecting **New**.

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
</table>12. Select **Submit**.

    The employee is added \(auto-assigned\) to a selected neighborhood. Employees belonging to an indicated hierarchy \(auto-assigned\), or employees that are added manually \(on demand\) can interact with a neighborhood.

13. Select the **Execute User Assignments** tab to trigger all assignment rules \(users to added or removed space allocation\) to this neighborhood directly.

    ![Neighborhood with assigned users and spaces](../images/neighborhood-auto-assigned.png "Neighborhood showing allocated spaces and users")

    **Note:** Neighborhood assignments are applicable if Neighborhood is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.

    By default, the **Execute User Assignment** scheduled job runs daily or weekly on an instance. You may want to run it for the first time directly. When you run the scheduled job for each user, a workplace profile record is created \(if it's not in your instance already\), and the neighborhood is assigned to that workplace profile.

    -   When an employee is assigned to a neighborhood, a workplace profile is created.
    -   Neighborhoods are assigned to a workplace profile, even if an employee has multiple workplace profiles. All neighborhood assignments are done only on one workplace profile.
    -   An employee can be assigned to multiple neighborhoods. Each assignment is a separate record in the Workplace Profile Location Assignment Related list on the workplace profile form.
    -   The changes are captured in the execution details table and the changes are mentioned as type **Allocation**.
    -   If new spaces are assigned to a neighborhood, the spaces are updated in the neighborhood record.
    -   If spaces are removed from a neighborhood, the neighborhood record is updated when you run the execute user assignment task.

        Workplace Profile records are updated, added, or removed. A move task is initiated for employees who have a new space allocation and who are moved from one floor to another.

14. To create and manage a neighborhood in Workplace Central for a scenario, see [Create a scenario](../../workplace-central/task/create-a-scenario.md).

15. To view and reserve spaces in a neighborhood using the Reservation Management portal, see [Create neighborhood reservations](../../wsd-reservation-management/task/create-neighborhood-reservations.md).

16. To add a user to the neighborhood, refer to [Add a user to the neighborhood](add-a-user-to-neighbourhood.md).


