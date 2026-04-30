---
title: View or edit space allocations of a building
description: The Space optimization also enables you to view space allocations and make any space-related changes on a building directly. You can view a building stack plan and floor map same as scenarios.
locale: en-US
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# View or edit space allocations of a building

The Space optimization also enables you to view space allocations and make any space-related changes on a building directly. You can view a building stack plan and floor map same as scenarios.

## Before you begin

Ensure that the following plugins are installed:

-   Workplace Central
-   Workplace Stack Plan
-   Workplace Service Delivery Components
-   Workplace Case Management
-   Workplace Space Management
-   For Floor map view, the floor maps must be created using Workplace Indoor Mapping Map studio.

Role required: sn\_wsd\_spcmgmt.space\_planner, sn\_wsd\_spcmgmt.scenario\_reader \(read-only; to view a building\)

## About this task

You can perform several actions on a building directly instead of working them through scenario planning. The building view enables you to perform the following:

-   View space allocations on each floor based on different view options. For more information on the different view by options that are available, refer to [Scenario and Building - Views, states, settings, and key features](../reference/scenario-planning-views-actions-keyfeatures-.md).
-   Get space details of each allocation on the stack plan same as in scenarios.
-   Perform map-based space administration. Such as, editing or updating user assignments to a neighborhood.
-   View space allocations based on the workplace entities. This view option is supported only in the building view. You can specify the entity type based on which you want to see the space allocations.
-   You can also perform changes on a building using a floor map directly. Refer to [Edit a building's spaces using a map](edit-space-details-for-buildings.md).

## Procedure

1.  Navigate to any one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  On the left pane, select **Space Optimization** icon \(![Space optimization icon.](../images/space-optimization-icon.png)\).

    The Space optimization dashboard opens.

3.  In the All Buildings section, select the building for which you want to view the spaces.

    Select **View all** to view a list of buildings.

    The stack plan of the building opens.

4.  To view the spaces on each floor based on their allocation that are they are assigned to, do the following:

    1.  On the right panel, select the **Stack plan settings** icon \(![Stack plan settings icon.](../images/stack-plan-settings-icon.png)\) to open the settings.

    2.  In the **View by** field, select an option.

        The following view options are available:

        -   **Department**
        -   **Cost center**
        -   **Neighborhood**
        -   **Workplace Entity**

            When you select **Workplace Entity**, an additional field, **Workplace Entity Type** is also displayed in which you can specify the entity type, based on which you want to view the spaces.

        -   **Space type**
        -   **Assignment type**
        -   **Space status**
        -   **Space function**
        -   **Occupancy status**
5.  To view the space details assigned to the allocation that you selected, do the following:

    1.  On the right panel, select the Space details icon \(![Space details icon.](../images/space-details-icon.png)\).

    2.  On the stack plan, select the bar for which you want to view the space details.

        The details such as the space count, capacity, user assignment details and the color legend associated with the allocation is displayed on the right.

6.  To allocate a space or to change the allocation, do the following:

    1.  Select the **Floor map** and the **Building** tab.

    2.  Select the floor and building where the space is located using the drop-down on the top right of the map.

    3.  Select a space on the map directly to view the details of that space on the right panel.

        You can select a single or multiple spaces by drawing a circle around them or by using the Shift key on the keyboard. The details on the right panel are displayed based on your selection.

        The spaces that are flexible, assigned, and unassigned spaces are highlighted with different color codes. The legend of these color codes is displayed on the map. If a space is assigned to any user, an avatar icon is displayed with the number of users assigned to that space.

    4.  On the side panel, select **Edit Spaces**.

        A page opens displaying the list of selected spaces.

    5.  Select the spaces for which you want to change the allocation.

    6.  Select the **Allocations** drop-down.

    7.  Depending on the allocation change that you want to make, select one of the following:

        -   **Change allocation**: To change the existing allocation.
        -   **Add allocation**: To add an allocation.
        -   **Remove allocation**: To remove the existing allocation.
    8.  On the window that opens, in the **Allocation type** field, select the allocation type.

        You can also select any allocations depending on the requirement.

    9.  Select **Apply**.

    10. On the confirmation window, review the changes that are about to be implemented and select **Confirm**.

        The allocation changes are saved automatically.


-   **[Edit or view a building's spaces based on workplace entities](view-a-building-s-spaces-based-on-workplace-entities.md)**  
View the spaces in a building based on their entity types. On the floor map, directly add an allocation or modify an allocation of space. Assign spaces to a workplace entity from the floor map.

**Parent Topic:**[Working with Space Optimization](../concept/working-with-space-optimization.md)

**Related topics**  


[Create a scenario](create-a-scenario.md)

[Viewing or editing a scenario](../concept/viewing-editing-scenario.md)

[Review a scenario](review-a-scenario.md)

[Publish a scenario](publish-a-scenario.md)

[Send a scenario for approval](send-a-scenario-for-approval.md)

[Change owner of a scenario](change-owner-of-a-scenario.md)

[Deploy a scenario](deploy-a-scenoria.md)

[View scenario change details](view-scenario-change-details.md)

[Create a copy of an existing scenario](create-copy-of-scenario.md)

[Work on a space assist request](work-on-space-assist-request.md)

[Map based space administration](../concept/map-based-space-administration.md)

