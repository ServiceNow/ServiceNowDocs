---
title: Edit user assignments of a neighborhood
description: Add a user to a neighborhood or edit the existing user assignments of a neighborhood in a building.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 3
breadcrumb: [Viewing or editing a scenario, Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Edit user assignments of a neighborhood

Add a user to a neighborhood or edit the existing user assignments of a neighborhood in a building.

## Before you begin

Make sure that you have created a scenario that is based on neighborhoods. For more information about creating neighborhoods and scenarios, see the following topics.

**Important:** If allocation changes in your instance impact the scenario, the system displays a warning on the Space Details panel. You must review the changes, edit the scenario accordingly, then select **Move to valid** before continuing. For more information about allocation changes, see [Reviewing allocation changes](../../workplace-space-management/concept/reviewing-allocation-changes.md).

-   [Managing Neighborhoods](../../workplace-space-management/concept/neighborhoods.md)
-   [Create a scenario](create-a-scenario.md).

**Important:** You can add a user assignment or edit a user assignment of a neighborhood only in a building view.

Role required: sn\_wsd\_spcmgmt.space\_planner

## About this task

You can add or remove user assignments of a neighborhood in a building or a scenario. A workplace user can only have one location in a neighborhood. If a user is assigned multiple locations in the same neighborhood, the latest added location is set as active and others are deleted.

**Note:** On a building, you can only make user assignment-related changes only for a neighborhood that is already created. You can’t add a new neighborhood.

## Procedure

1.  Navigate to any one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  Select the **Space Optimization** icon \(![Space optimization.](../images/space-optimization-icon.png)\).

    The Space optimization dashboard opens.

3.  In the All Buildings section, select the building that you want to modify the neighborhood user assignments for.

    Select **View all** to view a list of buildings.

    The stack plan of the building opens.

4.  View the neighborhoods on each floor of the building.

    1.  Select the Stack plan settings icon \(![Stack plan settings.](../images/stack-plan-settings-icon.png)\) to open the settings.

    2.  In the **View by** field, select **Neighborhood**.

        The stack plan displays the neighborhoods in the building.

5.  Edit the user assignments of a neighborhood in the stack plan.

    1.  Select the neighborhood on the floor that you want to edit the user assignments on.

    2.  On the Space details panel, in the Assignment section, select **Edit user assignments**.

        A page opens displaying the list of users assigned to the neighborhood.

    3.  Use the filter, sort, or refresh options to modify the list.

    4.  Add or remove users from the neighborhood.

<table id="choicetable_ebx_gdx_rfc"><thead><tr><th align="left" id="d190984e257">

Choice

</th><th align="left" id="d190984e260">

Steps

</th></tr></thead><tbody><tr><td id="d190984e266">

**Add users to the neighborhood**

</td><td>

1.  Select **Add**.
2.  In the Add user profile window, select the users whom you want to add.

Use the filter option to filter the users list. You can add up to 1000 users to the neighborhood.

3.  Select **Add**.
 The users are added to the neighborhood. A new Workplace Profile Location Assignment is added to the user's workplace profile with the neighborhood assignment. The **Source** field of the user assignment is set as manual.

</td></tr><tr><td id="d190984e304">

**Remove users from the neighborhood**

</td><td>

1.  Select the users who you want to remove from the neighborhood.
2.  Select **Remove**.
3.  On the deletion confirmation window, select **Delete All**.
 The users are removed from the neighborhood. The Workplace Profile Location Assignment is removed from the user's workplace profile with the neighborhood assignment.

</td></tr></tbody>
</table>    Neighborhood assignments are applicable if **Neighborhood** is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.


**Parent Topic:**[Viewing or editing a scenario](../concept/viewing-editing-scenario.md)

**Related topics**  


[Edit a scenario using the stack plan](edit-scenario-stack-plan.md)

[Edit a scenario using the floor map](edit-scenario-floor-map.md)

