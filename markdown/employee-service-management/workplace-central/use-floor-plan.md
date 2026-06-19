---
title: Use Floor Plan
description: Use the floor plan to manage space and user assignments in your workplace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-central/use-floor-plan.html
release: zurich
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Working with Space Planning, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Use Floor Plan

Use the floor plan to manage space and user assignments in your workplace.

## Before you begin

Make sure that you have installed Workplace Core. For more information, see [Install Workplace Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-core/install-workplace-service-delivery.md)

For the Floor plan, make sure that you have configured the map in Indoor Mapping. For more information about configuring an indoor map, see [Configure Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/configure-ind-mapping.md).

Role required: sn\_wsd\_core.workplace\_manager or sn\_wsd\_spcmgmt.space\_planner

**Note:** The sn\_wsd\_core.scenario\_reader role has access to view the map, space allocations, and user assignments.

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

2.  On the side navigation, select the **Space Planning** module.

    The Space Planning workspace opens with the **Floor plan** tab selected by default.

3.  Select a campus, building, and floor to view the map.

4.  View the KPIs on the details panel.

    The following KPIs are displayed based on your selection on the map.

    -   `Space count`: Number of spaces on the floor or in the selection.
    -   `Total effective capacity`: Capacity of the number of spaces multiplied by their capacity ratio.

        For example: If 20 spaces have a capacity ratio of 1.5, and 10 spaces have a capacity ratio of 1, the space count is 30 and total effective capacity is 40.

    -   `Profiles assigned`: Number of workplace profiles assigned to the floor or selected spaces. If a user is assigned to multiple spaces, they are considered to have multiple profiles. The KPI includes both location assignments and neighborhood assignments.

        For example, if a user is assigned to 2 spaces, and another user is assigned to 3 spaces, the number of assigned profiles is 5.

    -   `Unassigned spaces`: Number of spaces that do not have any assignments.
    -   `Assignment ratio`: Ratio of the assigned profiles to the total effective capacity.
    If you have installed Workplace Space Management, space admins can configure custom KPIs to be displayed on the details panel. For more information about configuring KPIs, see [Create a KPI Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-space-management/create-kpi-configuration.md).

5.  Select a **View by** option to group spaces on the map.

    The default view by option is set to **None**. If Workplace Space Management is installed, the option with the lowest order is selected by default.

    Based on the view by option, the details panel displays information about Neighborhoods or Space Types. If the view by option is **None**, the details panel displays both Neighborhoods and Space Types. With Workplace Space Management, the details panel displays spaces allocated to all neighborhoods, departments, cost centers, and workplace entities.

    If you have installed Workplace Space Management, space admins can configure custom view-by configurations to group spaces. For more information about configuring the view by options, see [Create a view-by configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-space-management/create-view-by-config.md).

    1.  For workplace entities, select the entity level that you want to use to view the map.

        For example, select Project to view project-level allocations.

        The map displays all entity levels by default.

    2.  For workplace entities, view the hierarchy by selecting the tree icon \[Omitted image "wsd-central-tree-icon.png"\] Alt text: on the legend.

6.  Perform any of the following actions based on your requirement.

<table id="choicetable_y3x_khj_3vb"><thead><tr><th align="left" id="d155684e252">

Action

</th><th align="left" id="d155684e255">

Steps

</th></tr></thead><tbody><tr><td id="d155684e261">

**Zoom in or out on the map**

</td><td>

Use the zoom options \[Omitted image "zoom-options.png"\] Alt text: on the map.

</td></tr><tr><td id="d155684e275">

**Change the map to a different floor and building**

</td><td>

Select a building and floor from the **Building** and **Floor** list options.

</td></tr><tr><td id="d155684e290">

**Search for a user or space**

</td><td>

1.  In the search bar, search for a user or a space.

The search is global; you can search for a user's first name or the space name from any location.

2.  Select a search result based on your preference.
3.  After selecting a user or a space, you can edit their assignments and allocations.

For more information, see either of the following topics:

    -   [Edit user assignments on the floor plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/edit-user-assignments-floor-plan.md)
    -   [Edit space allocations on the floor plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/edit-space-allocations-floor-plan.md)


</td></tr><tr><td id="d155684e333">

**Select spaces**

</td><td>

1.  On the details panel, select **Select spaces**.

The Select spaces pop-up opens. You can select spaces on the current floor.

2.  Add conditions to filter the spaces.

For example, `Department is Finance`. For more information about conditions, see  and .

3.  Select the spaces from the list.
 Alternatively, you can select multiple spaces on the map by holding the Shift key. You can also hold the Shift key and draw a circle to select spaces on the map.

 The details panel displays information about the selected spaces and their assigned users.

</td></tr><tr><td id="d155684e377">

**Select a neighborhood**

</td><td>

1.  From the View by list, select **Neighborhoods**.
2.  On the details panel, select **Select neighborhoods**.

The Select neighborhood pop-up opens.

3.  Select a neighborhood from the list, then select **Confirm**.

All spaces on the floor that are allocated to the neighborhood are selected.

 Alternatively, for a single neighborhood, you can select the neighborhood from the legend.

</td></tr><tr><td id="d155684e414">

**Select Users**

</td><td>

1.  On the details panel, select **Select users**.

The Select users pop-up opens. You can select users on the current floor.

2.  Add conditions to filter the users.

For example, `Workplace profile is Active`. For more information about conditions, see .

3.  Select the users from the list.
 The details panel displays information about the selected users and their assigned spaces.

</td></tr><tr><td id="d155684e451">

**Print the map**

</td><td>

1.  On the Floor Map tab, select the map print icon.
2.  On the map printing page, fill in the fields based on your preference.

For more information about map printing and its options, see [Print a map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/print-map.md).

 To print a map, you need the `sn_map_core.map_printer` role.

</td></tr><tr><td id="d155684e484">

**Edit space details**

</td><td>

1.  Select the spaces that you want to edit.
2.  On the details panel, select **View/edit details**.
3.  On the Spaces list, edit the details based on your requirement.


</td></tr><tr><td id="d155684e508">

**Review move information for a space**

</td><td>

**Important:** You must have Workplace Move Management installed to view move-related information.

 1.  On the floor map, select a space that has a move icon.
2.  On the details panel, review the user cards for the move information.
    -   A card tagged as **Outgoing** indicates that the user is moving out of the selected space.
    -   A card displayed under **Incoming moves** indicates that the user is moving into the selected space.
3.  On the user card, select the info icon to view the source and destination of the move request.
4.  On the user card, select the link icon to view the details of the move case.


</td></tr><tr><td id="d155684e552">

**Display user assignments on the map**

</td><td>

1.  On the map, select the settings icon \[Omitted image "map-settings-icon.png"\] Alt text:.
2.  Turn on the **Assigned to** option to display user assignments on the map.

This option is switched on by default.

3.  Select any of the following options based on your requirement:
    -   **Location assignments**
    -   **Neighborhood assignments**
4.  Select **Apply**.


</td></tr><tr><td id="d155684e603">

**View the map as defined in the Map Studio**

</td><td>

1.  On the map, select the settings icon \[Omitted image "map-settings-icon.png"\] Alt text:.
2.  Turn on the **Show base map** option, then select **Apply**.

The map displays spaces as defined in the Map Studio.

</td></tr></tbody>
</table>    **Important:**

    If **Neighborhood** is selected as the group by option, only assignments that have the **Neighborhood assignment** type are applicable. For any other group by option, assignments that have the **Location assignment** type are applicable.


## What to do next

-   [Edit space allocations on the floor plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/edit-space-allocations-floor-plan.md)
-   [Edit user assignments on the floor plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/edit-user-assignments-floor-plan.md)

-   **[Edit user assignments on the floor plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/edit-user-assignments-floor-plan.md)**  
Use the floor plan to edit location or neighborhood assignments for the users.
-   **[Edit space allocations on the floor plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/edit-space-allocations-floor-plan.md)**  
Use the floor plan to edit space or neighborhood allocations.

**Parent Topic:**[Working with Space Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/working-with-space-planning.md)

