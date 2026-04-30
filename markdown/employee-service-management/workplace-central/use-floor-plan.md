---
title: Use Floor Plan
description: Use the floor plan to manage space and user assignments in your workplace.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-02-02"
reading_time_minutes: 4
breadcrumb: [Working with Space Planning, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Use Floor Plan

Use the floor plan to manage space and user assignments in your workplace.

## Before you begin

Make sure that you have installed Workplace Core. For more information, see [Install Workplace Core](../../workplace-service-delivery/task/install-workplace-service-delivery.md)

For the Floor plan, make sure that you have configured the map in Indoor Mapping. For more information about configuring an indoor map, see [Configure Indoor Mapping](../../wsd-indoor-mapping/concept/configure-ind-mapping.md).

Role required: sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Central**.

2.  Select the **Space Planning** module.

    The Floor Plan tab opens by default.

3.  Select a campus, building, and floor to view the map.

4.  View the KPIs on the details panel.

    The following KPIs are displayed based on your selection on the map.

    -   `Space count`: Number of spaces on the floor or in the selection.
    -   `Total effective capacity`: Capacity of the number of spaces multiplied by their capacity ratio.

        For example: If 20 spaces have a capacity ratio of 1.5, and 10 spaces have a capacity ratio of 1, the space count is 30 and total effective capacity is 40.

    -   `Profiles assigned`: Number of workplace profiles assigned to the floor or selected spaces. If a user is assigned to multiple spaces, they are considered to have multiple profiles.

        For example, if a user is assigned to 2 spaces, and another user is assigned to 3 spaces, the number of assigned profiles is 5.

    -   `Unassigned spaces`: Number of spaces that do not have any assignments.
    -   `Assignment ratio`: Ratio of the assigned profiles to the total effective capacity.
5.  Select a **View by** option to group spaces on the map.

    The default view by option is set to **None**.

    Based on the view by option, the details panel displays information about Neighborhoods or Space Types. If the view by option is **None**, the details panel displays both Neighborhoods and Space Types.

6.  Perform any of the following actions based on your requirement.

<table id="choicetable_y3x_khj_3vb"><thead><tr><th align="left" id="d471398e183">

Action

</th><th align="left" id="d471398e186">

Steps

</th></tr></thead><tbody><tr><td id="d471398e192">

**Zoom in or out on the map**

</td><td>

Use the zoom options \(![Zoom options.](../images/zoom-options.png)\) on the map.

</td></tr><tr><td id="d471398e207">

**Change the map to a different floor and building**

</td><td>

Select a building and floor from the **Building** and **Floor** list options.

</td></tr><tr><td id="d471398e222">

**Search for a user or space**

</td><td>

1.  Search for a user or a space in the search bar, then select one of the search results based on your preference.
2.  After selecting a user or a space, you can edit their assignments and allocations.

For more information, see either of the following topics:

    -   [Edit user assignments on the floor plan](edit-user-assignments-floor-plan.md)
    -   [Edit space allocations on the floor plan](edit-space-allocations-floor-plan.md)


</td></tr><tr><td id="d471398e260">

**Select spaces**

</td><td>

1.  On the details panel, select **Select spaces**.

The Select spaces pop-up opens.

2.  Add conditions to filter the spaces.

For example, `Department is Finance`. For more information about conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

3.  Select the spaces from the list.
 Alternatively, you can select multiple spaces on the map by holding the Shift key. You can also hold the Shift key and draw a circle to select spaces on the map.

 The details panel displays information about the selected spaces and their assigned users.

</td></tr><tr><td id="d471398e302">

**Select a neighborhood**

</td><td>

1.  From the View by list, select **Neighborhoods**.
2.  On the details panel, select **Select neighborhoods**.

The Select neighborhood pop-up opens.

3.  Select a neighborhood from the list, then select **Confirm**.

All spaces on the floor that are allocated to the neighborhood are selected.

</td></tr><tr><td id="d471398e336">

**Select Users**

</td><td>

1.  On the details panel, select **Select users**.

The Select users pop-up opens.

2.  Add conditions to filter the users.

For example, `Workplace profile is Active`. For more information about conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

3.  Select the users from the list.
 The details panel displays information about the selected users and their assigned spaces.

</td></tr><tr><td id="d471398e374">

**Edit space details**

</td><td>

1.  Select the spaces that you want to edit.
2.  On the details panel, select **View/edit details**.
3.  On the Spaces list, edit the details based on your requirement.


</td></tr><tr><td id="d471398e398">

**Display user assignments on the map**

</td><td>

1.  On the map, select the settings icon \(![Map settings icon.](../images/map-settings-icon.png)\).
2.  Turn on the **Assigned to** option to display user assignments on the map.

This option is switched on by default.

3.  Select any of the following options based on your requirement:
    -   **Location assignments**
    -   **Neighborhood assignments**
4.  Select **Apply**.


</td></tr><tr><td id="d471398e449">

**View the map as defined in the Map Studio**

</td><td>

1.  On the map, select the settings icon \(![Map settings icon.](../images/map-settings-icon.png)\).
2.  Turn on the **Show base map** option, then select **Apply**.

The map displays spaces as defined in the Map Studio.

</td></tr></tbody>
</table>    **Important:**

    If **Neighborhood** is selected as the group by option, only assignments that have the **Neighborhood assignment** type are applicable. For any other group by option, assignments that have the **Location assignment** type are applicable.


## What to do next

-   [Edit space allocations on the floor plan](edit-space-allocations-floor-plan.md)
-   [Edit user assignments on the floor plan](edit-user-assignments-floor-plan.md)

-   **[Edit user assignments on the floor plan](edit-user-assignments-floor-plan.md)**  
Use the floor plan to edit location or neighborhood assignments for the users.
-   **[Edit space allocations on the floor plan](edit-space-allocations-floor-plan.md)**  
Use the floor plan to edit space or neighborhood allocations.

**Parent Topic:**[Working with Space Planning](../concept/working-with-space-planning.md)

