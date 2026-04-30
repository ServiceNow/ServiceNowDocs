---
title: Manage Directions
description: Directions are used to compute routes from point A to point B on the map. Map administrators can manually draw lines on the floor map areas where people are allowed to walk within a building. This cannot be automated and has to be done manually.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Manage Directions

Directions are used to compute routes from point A to point B on the map. Map administrators can manually draw lines on the floor map areas where people are allowed to walk within a building. This cannot be automated and has to be done manually.

## Before you begin

Role required: map admin, map editor, map editor limited

## Procedure

1.  Two direction modes \(**Accessible** and **Default**\) are enabled by default in Indoor Mapping.

    -   **Accessible:** This mode is for users with reduced mobility and so by default, the stairs and escalators are inactive, while elevators and ramps are added.
    -   **Default**: Configured for general public and pedestrians.
2.  New direction modes require icons.

    For more information, see [Create Indoor Mapping icons and place types](place-icons-place-type.md)

3.  To create a new direction mode, navigate to **All** &gt; **Indoor Mapping** &gt; **Direction modes**.

    On the form, fill in the fields

<table id="table_knb_kl2_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Direction mode name.

</td></tr><tr><td>

Title

</td><td>

Direction mode title will be displayed on the map studio when you select the direction mode of a direction.

</td></tr><tr><td>

Icon

</td><td>

Select an icon from the list.

</td></tr><tr><td>

Average speed

</td><td>

Average speed for the type of transportation used.

</td></tr><tr><td>

Active

</td><td>

Option to activate the direction mode on the map.**Note:** Turning off the direction mode does not remove it's just made inactive on your map and the directions will not be shown on the map.

</td></tr></tbody>
</table>4.  Click **Submit**.

    The newly added direction mode is available in the list.

    **Note:** On the direction mode record, select **Route to direction mode associations** to find the list of campuses and buildings for which the direction mode is active.

5.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

6.  Select a campus.

7.  Go to **Manage Workplace**, select **Directions**.

    Alternatively, select **Manage Directions** from the Map Studio menu.

8.  Select a building and floors where you want to add the directions to edit.

9.  From the **Direction modes** drop-down list, select a direction mode from the available options:

    -   **All modes**
    -   **Accessible**
    -   **Default**
10. To draw directions from one point to another, select **Draw** and begin drawing routes along all the hallways for each floor.

    **Note:** Lines must be straight as they are used by the wayfinding application to display routes within a building.

    All segments created are by default set to Active, this state can be edited at any time on the Studio to reflect any changes \(incidents, renovation, and so on\). Change the state by selecting the toggle option **Active** or **Inactive**.

    ![Draw directions for wayfinding](../images/manage-directions.png)

11. To stop drawing, select **Select/Move** or press **esc** \(escape\) on the keyboard.

    All segments that are created are by default set to **Active**. The Active state can be edited any time on the Map Studio to reflect any changes \(incidents, renovations, etc.\).

12. To change the state, click the toggle option **Active** or **Inactive**.

    States help the wayfinding application to calculate a similar route without going through the inactive routes or segments.

13. Use the **All modes** option to use segment in both ways **Accessible** or **Default**.

    You can also change it to enable only one-way directions.

14. Select a way and define in which way the segment can be used.

15. Small arrows appear on the map.

    The route with the selected direction mode is highlighted on the map.

16. Each of the segments of the direction graph can be edited.

17. By default, both default and accessible modes are shown as active on each segment.

18. Once the direction graph is complete, make sure you clearly identify the connectors to link your floors together.

    For more information, see [Create a connector type](create-connectors.md).

19. Select the **Display settings** icon ![Manage directions toggle option](../images/manage-directions-new-toggle-icon.png)adjacent to the **Save** button.

20. Select **Connector links**.

21. Select the node that represents a connector and ensure that the correct building is selected.

    For more information, see [Create a connector type](create-connectors.md).

22. After creating the connectors, link additional floors of your building together.

23. Select the node and ensure that you link it with the same node you have created for the same connector.

24. After creating direction graphs for every floor in a building, repeat the process to add a graph on the campus.

25. Ensure you link two graphs by connecting the two end nodes.

26. Click **Save**.

27. To unlink a connector, select **Detach connector**.

28. Select **Place entrances** from Display settings to display the place entrances for a selected campus or building.

    This option displays on the map where the entrance is located and the point or points that are going to be used by graph directions as start points.

29. Select **System generated paths to entrances** from Display settings:

    This option is used to connect place entrances connect to a generated path. The paths marked in green show system generated paths. Users do not have draw manually. The application automatically computes paths from an entrance.

30. Click **Save**.

31. Click the other options icon \(![Other options icon](../../wsd-for-mobile/images/more-options-icon.png)\).

32. Select **Copy directions**.

    This option helps in mapping or copying directions where several floors have the same layout. You can also reuse directions defined for a previous floor. For more information, see [Copy direction graphs to multiple floors](copy-directions-multiple-floors.md).

33. Click **Save** to save all your changes.

34. After editing the directions, you must activate the direction mode in the map View Editor so that it is available for all map users.

35. Select **View Editor** on the Campus menu and click **Edit.**

36. After making the required changes, click **Save**.

37. If you want to remove a content, select it and click **Delete**.


-   **[Create a connector type](create-connectors.md)**  
Create connectors \(stairs, elevators, escalators, ramps\) and activate the connector type in the View editor. Connector Type contains the style \(icon\) and properties for each connector.
-   **[Copy direction graphs to multiple floors](copy-directions-multiple-floors.md)**  
Select a campus or building and copy floor direction graphs from a floor to a single floor or multiple floors in a building.

**Parent Topic:**[Manage map objects and data](../concept/using-indoor-mapping.md)

**Previous topic:**[Create Indoor Mapping icons and place types](place-icons-place-type.md)

**Next topic:**[Create a connector type](create-connectors.md)

