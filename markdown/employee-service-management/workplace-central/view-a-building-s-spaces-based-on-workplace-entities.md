---
title: Edit or view a building's spaces based on workplace entities
description: View the spaces in a building based on their entity types. On the floor map, directly add an allocation or modify an allocation of space. Assign spaces to a workplace entity from the floor map.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 5
breadcrumb: [View or edit space allocations of a building, Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Edit or view a building's spaces based on workplace entities

View the spaces in a building based on their entity types. On the floor map, directly add an allocation or modify an allocation of space. Assign spaces to a workplace entity from the floor map.

## Before you begin

[View or edit space allocations of a building](view-or-edit-space-alloctions-of-a-building.md)

**Important:** You can view spaces based on their workplace entities only for a building. You cannot create or view a scenario based on workplace entities.

Role required: sn\_wsd\_spcmgmt.space\_planner, sn\_wsd\_spcmgmt.scenario\_reader \(read-only; to view a building\)

## About this task

You can view a building's spaces based on different entity types that you configured in the application. The stack plan enables you to view the number of spaces assigned to each entity. View the hierarchy of each entity that is, view the child and parent workplace entities.

From the floor map view of the building, directly assign a space to a workplace entity or change an existing allocation of a space.

You can also perform changes on a building using a floor map directly. Refer to [Edit a building's spaces using a map](edit-space-details-for-buildings.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  Select the **Space Optimization** icon \(![Space Optimization icon.](../images/space-optimization-icon.png)\).

    The Space optimization dashboard opens.

3.  In the All Buildings section, select the building for which you want to view the spaces.

    Select **View all** to view a list of buildings.

    The stack plan of the building opens.

4.  To view the spaces on each floor based on the workplace entities that are they are assigned to, do the following:

    1.  On the right panel, select the Stack plan settings icon \(![Stack plan settings icon.](../images/stack-plan-settings-icon.png)\) to open the settings.

    2.  In the **View by** field, select **Workplace Entity**.

    3.  In the **Workplace Entity Type** field, specify the entity type based on which you want to view the workplace entities.

        If you want to view all the workplace entities irrespective of their entity types, select **All levels**.

5.  To view the space details assigned to each workplace entity, do the following:

    1.  On the right panel, select the Space details icon \(![Space details icon.](../images/space-details-icon.png)\).

    2.  On the stack plan, select the bar of the workplace entity for which you want to view the space details.

        The details of the workplace entity such as the space count, capacity, user assignment details and the color legend associated with the entity is displayed on the right.

        Spaces that are not assigned to the selected workplace entity directly or indirectly \(to any lower hierarchy entity types that can be resolved to the selected workplace entity\) are assigned to the higher hierarchy of the workplace entity are displayed as **Others**.

6.  To view the hierarchy of the workplace entity, do the following:

    1.  Select the workplace entity for which you want to view the hierarchy.

        Select the bar on the floor.

    2.  In the Space details panel, go to the Workplace Entity section.

    3.  Select the hierarchy icon \(![Hierarchy icon.](../images/hierarchy-icon.png)\) next to the color legend of the workplace entity.

        The legend displays the color of the entity and the number of spaces assigned to that entity on the floor.

        A window opens displaying the details of the workplace entity and its hierarchy. The number of spaces assigned to each entity in the hierarchy is clearly detailed.

    4.  On the window, select the expand icon \(![Hierarchy expand icon.](../images/hierarchy-expand-icon.png)\) to view the list of below level entities and the number of spaces assigned to it.

        Point to the info icon \(![Info icon.](../../wsd-reservation-management/image/info-icon.png)\) to view the number of spaces directly assigned to that entity level out of the total assignments on it and its sublevels in the hierarchy.

7.  To allocate a space to a workplace entity or to change the allocation, do the following:

    1.  Select the **Floor map** tab.

    2.  Select the floor where the space is located using the drop-down on the top right of the map.

    3.  Select a space on the map directly to view the details of that space on the right panel.

        You can select a single or multiple spaces by drawing a circle around them or by using the Shift key on the keyboard. The details on the right panel are displayed based on your selection.

        The spaces are highlighted with different colors based on their allocation. The legend of colors is the displayed on the map. If a space is assigned to any user, an avatar icon is displayed with the number of users assigned to that space.

    4.  On the side panel, select **Edit Spaces**.

        A page opens displaying the list of selected spaces.

    5.  Select the spaces for which you want to change the allocation to a workplace entity.

    6.  Select the **Allocations** drop-down.

    7.  Depending on the allocation change that you want to make, select one of the following:

        -   **Change allocation**: To change the existing allocation to a workplace entity.
        -   **Add allocation**: To add the workplace entity allocation.
        -   **Remove allocation**: To remove the existing allocation.
    8.  On the window that opens, in the **Allocation type** field, select **Workplace entity**.

        You can also select other allocations depending on the requirement.

    9.  In the **Entity type** field, select the entity type to which the space belongs.

    10. In the **Workplace entity** field, select the workplace entity to which the space belongs.

    11. Select **Apply**.

    12. On the confirmation window, review the changes that are about to be implemented and select **Confirm**.

        The allocation changes are saved automatically.


**Parent Topic:**[View or edit space allocations of a building](view-or-edit-space-alloctions-of-a-building.md)

