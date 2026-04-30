---
title: Edit a scenario using the floor map
description: Edit a scenario using the floor map to add or remove allocations, or to assign users to spaces in your organization.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-03-25"
reading_time_minutes: 5
breadcrumb: [Viewing or editing a scenario, Working with Space Optimization, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Edit a scenario using the floor map

Edit a scenario using the floor map to add or remove allocations, or to assign users to spaces in your organization.

## Before you begin

Ensure that you have created a scenario, and it is in the Draft state. For more information, see [Create a scenario](create-a-scenario.md).

Ensure that you have selected Indoor Mapping as your map provider to view maps.

-   For more information about selecting a map provider, see [Customize the map properties](../../workplace-space-mapping/task/wsm-configure-map-properties.md).
-   For more information about indoor mapping, see [Indoor Mapping](../../wsd-indoor-mapping/reference/Indoor-mapping.md).

Role required: sn\_wsd\_spcmgmt.space\_planner, sn\_wsd\_spcmgmt.scenario\_reader \(read only; to view a scenario\)

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
    You can also open Workplace Central from the Employee Center. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  From the All scenarios list, select the scenario that you want to edit.

    By default, the scenario opens in the **Stack plan** tab.

3.  Select the **Floor map** tab.

4.  On the Space details pane, on the View options card, select **Edit scenario**.

    The **Group by** option is automatically filled based on the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property.

5.  Edit the scenario by using the floor map.

<table id="choicetable_y3x_khj_3vb"><thead><tr><th align="left" id="d629533e199">

Action

</th><th align="left" id="d629533e202">

Description

</th></tr></thead><tbody><tr><td id="d629533e208">

**Zoom in or out on the map**

</td><td>

Use the zoom options \(![Zoom options.](../images/zoom-options.png)\) on the map.

</td></tr><tr><td id="d629533e223">

**Change the map to a different floor and building**

</td><td>

Select a building and floor from the **Building** and **Floor** list options.

</td></tr><tr><td id="d629533e238">

**View the details of a space**

</td><td>

Select one or more spaces on the map.You can select multiple spaces by holding the Shift key. You can also hold the Shift key and draw a circle to select spaces on the map.

The details of the selected spaces are displayed on the Space details panel section.

</td></tr><tr><td id="d629533e252">

**Edit the allocation of a space**

</td><td>

1.  Select the spaces that you want to edit.

You can select multiple spaces by holding the Shift key. You can also hold the Shift key and draw a circle to select spaces on the map.

2.  On the Space details panel, from the **Actions** drop-down list, select **Allocation**.
3.  In the **Allocation** field, select any one of the following options:
    -   **Change allocation**: Select this option to change the allocation.
    -   **Add allocation**: Select this option to add an allocation.
    -   **Remove allocation**: Select this option to remove allocation.
4.  In the **Allocation type** field, select the allocation that you want to make.

**Note:** This field appears only if you select **Change allocation** or **Add allocation**. The name of the field depends on the **Group by** field of the scenario.

5.  Select **Apply**, then save the scenario.
 **Note:** For Workplace Entities, if you add a parent and child entity as allocations, only the child entity is displayed on the map legend.

</td></tr><tr><td id="d629533e334">

**Edit the assignment type of a space**

</td><td>

1.  Select the spaces for which you want to change the assignment.

You can select multiple spaces by holding the Shift key. You can also hold the Shift key and draw a circle to select spaces on the map.

2.  On the Space details panel, from the **Actions** drop-down list, select **Assignment type**.
3.  In the **Assignment type** field, select the type of assignment that you want to make.
4.  Select **Apply**, then save the scenario.


</td></tr><tr><td id="d629533e372">

**Assign a user to a space**

</td><td>

1.  Select the space that you want to edit.

You can select only a single space to assign a user.

2.  On the Space details panel, from the **Actions** drop-down list, select **User assignment**.
3.  In the **User assignment** field, select the user that you want to assign to the space.

You can also select multiple users.

4.  Select **Apply**, then save the scenario.


</td></tr><tr><td id="d629533e412">

**Remove a user assigned to a space**

</td><td>

1.  Select the space that you want to edit.

You can select only a single space to remove a user.

2.  On the Space details panel, on the **Assignment** card, remove a user by selecting the remove assignment icon \(![Remove assignment icon.](../images/remove-assignment.png)\).


</td></tr><tr><td id="d629533e441">

**Edit the display of user assignment and assignment type on the map**

</td><td>

1.  On the Space details panel, select the Map settings icon \(![Map settings icon.](../images/map-settings-icon.png)\).
2.  Based on what changes you want to make, enable, or disable any of the following options:
    -   **Assigned to**: Option to display the number of users assigned to a space.
    -   **Assignment type**: Option to display the type of assignment, that is, flexible or permanent.


</td></tr><tr><td id="d629533e480">

**Change the opacity of colored spaces**

</td><td>

You can change the opacity of the spaces that are colored based on the group by or view by options. Changing the opacity is helpful if some elements on the map are hidden due to the color.1.  On the Space details panel, select the Map settings icon \(![Map settings icon.](../images/map-settings-icon.png)\).
2.  In the **Opacity** field, enter the percentage value that you want for the highlighted spaces.
3.  Select **Apply**.

The specified opacity value is set for the colored spaces.

</td></tr></tbody>
</table>    **Important:** Neighborhood assignments are applicable if Neighborhood is selected as the group by or view by option in a scenario or building overview. Location assignments are applicable for all other options.


**Parent Topic:**[Viewing or editing a scenario](../concept/viewing-editing-scenario.md)

**Related topics**  


[Edit a scenario using the stack plan](edit-scenario-stack-plan.md)

[Edit user assignments of a neighborhood](add-or-edit-user-assignments-of-a-neighbourhood.md)

