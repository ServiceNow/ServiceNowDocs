---
title: Edit a building's spaces using a map
description: Space planners and administrators can update space attributes and allocation changes using interactive floor maps. Select and edit a single space or update bulk spaces via floor maps. Add, change, or remove space allocations as required. The updated space attributes and association changes are reflected in real-time on a floor map.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Map based space administration, Working with Space Optimization, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Edit a building's spaces using a map

Space planners and administrators can update space attributes and allocation changes using interactive floor maps. Select and edit a single space or update bulk spaces via floor maps. Add, change, or remove space allocations as required. The updated space attributes and association changes are reflected in real-time on a floor map.

## Before you begin

Role required: sn\_wsd\_spcmgmt.space\_planner

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Space Optimization** &gt; **All Buildings**.

2.  Select **View All** and select a building from the list of buildings.

3.  On the Stack plan, select the Stack plan settings icon \(![stack plan settings](../../workplace-space-mapping/images/gear-icon.png)\) from the right pane to display different view options.

4.  Select **View by** to select the view based on which the spaces on the floor must be categorized.

    The following view options are available:

    -   Department
    -   Cost center
    -   Neighborhood
    -   Workplace entity
    -   Space type
    -   Assignment type
    -   Space status
    -   Space function
    -   Occupancy status
    The spaces are displayed based on the selected view.

5.  To display the Space details for a selected stack bar, select the Space details icon \(![space details icon.](../images/space-details-icon.png)\) on the right pane.

6.  To view the space allocations on a map, select the **Floor Map** tab.

    The floor map of the selected floor on the stack plan is displayed. The spaces are highlighted based on the view option that you selected.

7.  To change the floors, use the **Floor** option.

8.  To view the space details of the spaces or any selected pane, on the right pane, go to the Space details section.

    Various space details such as the space counts, profiles assigned, department details and more are displayed.

9.  To change the view, on the right pane, select the Map Settings icon \(![map settings](../../workplace-space-mapping/images/gear-icon.png)\).

    In the Map Settings panel, you can perform the following actions:

    -   **Change the floor map view**: Select the **View by** option. The following view options are available:
        -   Department
        -   Cost center
        -   Neighborhood
        -   Workplace entity
        -   Space type
        -   Assignment type
        -   Space status
        -   Space function
        -   Occupancy status
    -   View spaces based on assignment: You can enable or disable the following settings:
        -   **Assigned to**: View the user to whom a space is assigned.
        -   **Assignment type**: View the assignment type of a space.
10. To zoom on the space on the map, use the zoom options displayed on the bottom right of the map.

11. To edit the space attributes or its allocation details, do the following:

    1.  Select either a single space or bulk spaces.

        To select multiple spaces, select and hold down the **Shift** key to draw a circle \(lasso\) or draw any freehand selection border around the spaces that you want to edit.

    2.  After the selection, to edit the spaces, on the right pane, select the **Edit Space** option under the **Space details** section.

        A new tab opens with a list view of the selected spaces. You can configure the columns based on which you want to view the spaces and also make edits and perform allocation changes. The updated changes are reflected in real time on a floor map.

    3.  Select the spaces that you want to edit using the check box.

        **Note:** Enable the system property **glide.lists.inline\_editing\_enabled** for making inline edits in the list pages.

        ![Real-time editing of multiple spaces using interactive floor map](../images/edit-multiple-spaces-floormap.png)

    4.  After selecting the required spaces, select **Edit**.

    5.  The right panel opens in the **Edit** mode.

    6.  After making the required space attributes and association changes, select **Update** to save the changes.

    7.  If there are spaces with similar names for a selected floor, a message is shown to change the space name.

    8.  Duplicate spaces are also shown so that they can be removed.

    9.  Take appropriate actions to change floor names and remove duplicate spaces.

    10. To update space allocation details, select required spaces from the list view and select the **Allocation** drop-down list to add, change, or remove space allocations.

<table id="table_hzw_plv_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Allocation

</td><td>

Select **Add allocation** from the drop-down list to add new space allocations.-   From the **Allocation type** drop-down list, select the allocation type.
-   Based on the **Allocation type** selection, select the required option.
-   Select **Apply**.


</td></tr><tr><td>

Change Allocation

</td><td>

Select **Change allocation** from the drop-down list to change or update space allocation.-   From the **Allocation type** drop-down list, select the allocation type.
-   Based on the **Allocation type** selection, select the required option.
-   Select **Apply**.


</td></tr><tr><td>

Remove Allocation

</td><td>

Select **Remove allocation** from the drop-down list to remove the selected space allocation.-   Select the allocation from the **Allocation type** drop-down list,
-   Select the required option, based on the **Allocation type** selection.
-   Select **Apply**.


</td></tr></tbody>
</table>    11. Additionally, select **Export** to export the bulk space record data to Excel, JSON, HTML, or CSV.

    12. Select the **Delivery type** list and select **Download** or **Email** to download or email the selected space record data.

    13. Select **New** to add a workplace location and update the required fields.

        For more information, see [Managing workplace locations](../../workplace-space-management/concept/Creating-workplace-location-records-using-spce-mgmt.md).

    14. After performing the changes, select **Save**.

12. Select **Back** to navigate back to **Floor Map**.

    Any changes that you make to space records are applied in real-time and available on the floor Map of the selected space.


**Parent Topic:**[Map based space administration](../concept/map-based-space-administration.md)

**Related topics**  


[Move employees on a floor or to a different floor using the map](move-employees-on-a-floor-or-to-a-different-floor-using-the-map.md)

