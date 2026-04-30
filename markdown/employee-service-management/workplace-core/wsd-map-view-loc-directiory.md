---
title: Work with the Map view on the Location Directory
description: Work with Map view to search for workplace users, locations, spaces, and neighborhoods. Get directions to a workplace location, meeting rooms, or an employee to collaborate quickly and effectively. Filter spaces based on reservation and occupancy states, space types, or neighborhoods.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Location Directory, Request employee-related services, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Work with the Map view on the Location Directory

Work with Map view to search for workplace users, locations, spaces, and neighborhoods. Get directions to a workplace location, meeting rooms, or an employee to collaborate quickly and effectively. Filter spaces based on reservation and occupancy states, space types, or neighborhoods.

## Before you begin

Wayfinding using the Location directory 

-   Workplace Core
-   Workplace Reservation Management \(Optional\)

    Filter and display the reservation status for a selected location on the Location directory.

-   Workplace Connectors \(Optional\)

    Filter and display the occupancy status for a selected location on the Location directory.

-   Indoor Mapping
-   Workplace Space Mapping

**Note:** Confirm that the map properties for the Location directory are configured by your administrator. Map properties for the Location directory provide options to:

-   Filter spaces based on reservation and occupancy states
-   Automatically refresh reservation and occupancy data on the Location directory
-   Control the Map display setting options to display permanent and private workplace profile users.
-   Show or hide neighborhoods for a location.

For more information, see [Configure map properties for Location Directory](configure-map-properties-location-directory.md).

The latitude and longitude of your regions, sites, campuses, and buildings must be created. If the latitude and longitude aren’t specified, you can’t view a campus or its buildings on the map. Contact your administrator for more information.

While reserving or viewing a space, the employee can see if a space is part of a neighborhood. The neighborhood icon \(![Neighborhood icon.](../../wsd-for-mobile/images/neighborhood-icon.png)\) is displayed on the space card.

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Workplace Services**.

2.  From the **Workplace Services** list, select **Browse Workplace services**.

3.  From the **Support resources** section, select **Location directory**.

    By default, the Location directory home page opens on the World map.

    Your location is displayed with a location pin \(![Location pin that shows the selected location on the map.](../../wsd-for-mobile/images/wsd-location-pin-icon.png)\).

    .

4.  To select a campus on the map, enter the name of a campus or select a campus name from the **Select Campus** list.

    1.  Select a campus from the list or search for a campus in the search bar.

        If you search for a Neighborhood, all the campuses that contain the neighborhood are displayed on the map and the neighborhood card. You can copy the neighborhood URL from the context menu.

    2.  Additionally, use the zoom in \(![Zoom in control icon to focus on the map artifacts.](../../wsd-for-mobile/images/wsd-mobile-zoom-in-icon-new-loc-directory.jpeg)\) controls on the map to bring into focus your location or select the location pin marker icon \(![Location pin marker on map.](../../wsd-for-mobile/images/wsd-location-pin-icon.png)\).

        The campus when selected or zoomed into shows the buildings within a campus.

        The selected campus is displayed on the map.

        ![Map view showing selected campus tab.](../images/wsd-loc-directory-homepage-with-campus-selected-use.png)

5.  When you select a campus, the **Select Building** tab is enabled on the menu.

    If you search for a Neighborhood, all the buildings that contain the neighborhood are displayed on the neighborhood card. You can copy the neighborhood URL from the context menu.

6.  Select a building from the **Select Building** list option.

    For example: Building A

    You can also use the Zoom in controls on the map to select a building from a campus.

7.  When you select a building, the **Floor**, and **Neighborhood** menu options are enabled on the menu.

    If you search for a Neighborhood, all the floors that contain the neighborhood are displayed on the neighborhood card. You can copy the neighborhood URL from the context menu.

    The **Show filters** option is enabled when a floor is selected from the **Floor** tab.

    ![Location Directory home page displaying selected campus, building](../images/wsd-new-loc-directory-campus-buidling-menu.png)

    **Note:** The **Last updated &lt;time interval&gt;** label is shown on the map after selecting a building. For example,**Last updated 1 min ago**. The map is automatically refreshed if your administrator has enabled the map property \(**Auto Refresh time interval \(in mins\) for showing Reservation and/or Occupancy information on the Location directory**\). This property fetches the latest reservation and occupancy data on the map.

8.  Select a floor from the **Floor** list option.

    Floors that don't have Indoor Mapping maps are tagged as **Floor &lt;number&gt;- No map** in the Floor tab list. For example, **Floor 5 - No map**.

    **Note:** When a floor doesn’t have a map associated with it, you’re redirected to the Card view. If a location doesn’t have Indoor Mapping, the Card view is displayed by default.

9.  Select the **Neighborhood** check box to show designated neighborhoods for a selected location.

    Neighborhoods are color-coded based on the assigned department, cost center, or workplace entity. For more information, see Step 17.

    ![Map view showing neighborhoods for a selected location.](../images/wsd-neighborhoods-map-new-loc-directory.png).

10. Select the **Refresh view** icon on the map \(![Refresh view icon to manually refresh the map and fetch reservation and occupancy status.](../images/wsd-refresh-icon-loc-directory.png)\) to refresh the map.

    When you manually refresh the map, the application fetches the latest reservation and occupancy status for a selected location.

11. Select **Show Filters** to filter spaces on the map by reservation states, occupancy states, and space types \(rooms, gym, elevator, and so on\).

    **Note:** The **Show filters** button is displayed on the map when **Show Reservation and/or Occupancy information on the Location directory** \[sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir\] map property is set to **Yes** by your administrator. Filters can be applied at a floor or space level. When this property is set to **No**, only space type filters are available for you to select.

    ![All filters panel showing space availability filters based on reservation status, occupancy status, and spaces space types.](../images/wsd-show-filters-panel-items-new-loc-dir.png)

    ![All filters panel showing space availability filters.](../images/wsd-new-all-filters-items-loc-directory.png)

    Select and filter any of the following available options in the All filters dialog box:

    -   View space availability and reservation status on the map, select the **Reservation status** check box.

        The map displays reservation status and spaces are shown with color-coded icons for different reservation states on the map. For more information, see Legends in Step 17.

    -   Filter spaces on the map with only reservation status. Select any of the following options:
        -   Booked
        -   Available
        -   Not Reservable
        -   Currently booked
    -   Selecting the **Select All** option enables all reservation statuses \(Booked, Available, Not Reservable, and so on\) on the map.
    -   Select the **Occupancy status** check box to view only occupancy sensor data icons on the map.

        The map displays reservation status and spaces are shown with color-coded icons for different reservation states on the map. For more information, see Legends in Step 17.

    -   Select any of the following occupancy states and filter spaces on the map with occupancy data.
        -   Occupied
        -   Not Occupied
        -   Sensor not installed
        -   Sensor not working
    -   Selecting the **Select All** option to filter all occupancy states on the map.
    **Note:** Occupancy states are only shown on the map if Workplace Connectors is installed and configured for a selected location. Your administrator must also configure the map property **Show Reservation and/or Occupancy information on Location directory \[sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir\]**.

    Spaces on the map with matching the filter conditions are highlighted. Spaces that don’t fulfill the filter conditions or that don’t have a filter applied are shown in white \(polygon color\).

    -   When both reservation and occupancy filters are applied, then maps shows both reservation and occupancy states for a selected floor.
    -   When only reservation or occupancy filters are applied, then only reservation or occupancy states are displayed.
    -   Select the **Spaces** check box to filter selected space types on the map. For example, the following space types can be selected:
        -   Rooms
        -   Gym
        -   Cafe
        -   Phone booth
        -   Workspace/Desk
        -   Restroom-Men
        -   Restroom-Women
        -   Miscellaneous
        -   Elevator
    -   Select the **Select All** option to select all the space types available for a location.

        **Note:** Indoor Mapping place types are displayed as space types on the Location directory.

12. Select **Apply**.

    The selected filters are applied and the **Filter by label** on the map shows filtered items as pills on the map. For example: Booked, Available, and so on. Select **Clear All** to remove the filter pills from the map.

    ![Filter by label showing the filter pills with filtered items.](../images/wsd-filter-pills-new-loc-directory.png)

13. Select a space on the map to view the Space card details.

    You can view the following information on the space card:

    -   Labels for space occupancy and reservation status are displayed on the space card panel. For example, **Available**, **Currently booked**, **Booked**, **Blocked**, and so on.

    -   Check if a space is being used by an employee or a team member.
    -   View the spaces surrounding your desk or workplace location.
    -   View employee avatar or workplace profile initials on the space card details.
    -   View your team and collaborators.
    -   Private spaces are hidden when the profile or space is indicated as private. The employee name isn’t displayed.
    -   View permanent seat assignment. Permanently assigned spaces are displayed with workplace profile names.
    -   View standard workplace services for a selected space.
    -   View a designated neighborhood, The neighborhood icon \(![Space card with neighborhood icon showing number of spaces with neighborhood.](../../wsd-for-mobile/images/wsd-neighborhood-icon-new-loc-directory.png)\) is displayed along with the number of seats.
    1.  Select the More actions icon \(![More options icon](../images/wsd-more-options-icon-loc-directory.png)\) and use any of the following options as required:

        -   Copy URL: Option to copy a space location link. The Copy URL link, when selected, copies the location URL link to a clipboard. The location URL link can be shared with your team members and colleagues.
        -   Raise an issue: Option to raise a workplace service request or a workplace service issue. For example, catering, cleaning, furniture, and so on
        ![Space card panel showing Copy URL and Raise an issue options.](../images/wsd-space-copy-url-raise-issue-reserve.png)

        ![Space card panel showing currently booked reservation state label.](../images/wsd-space-card-new-loc-currently-booked.png)

    2.  Select **Reserve** to reserve an available space.

        The employee can see the availability of the space and see if it’s reserved. A tag is added to indicate the space is occupied and used when a space is already reserved. If the reservation status label on the space card panel is **Currently booked**, the **Reserve** button isn’t available for selection and is inactive.

    3.  Select **Get Directions** for wayfinding and navigating to a meeting room or to where your co-worker is seated.

        You can find directions with the same floor or the same building or to a different floor or a different building.

14. To get directions from one space to another, perform the following actions on the map.

    **Important:** When privacy is enabled for an employee, using the Get directions option doesn't display the employee or colleague's workplace location.

    1.  Select a space and on the space card details panel, select **Get directions**.

    2.  Enter the start and end points for navigation and wayfinding.

        Complete the following:

        -   Select start point: Option to enter the starting point from where you want your direction or wayfinding route to start. For example, select a floor in a building from the list. You can also select a different building. For example, Starting point as Building A or Building B. You can enter a collaborator or colleague's name to find directions to their desk or location on the map.
        -   Select end point: The End point is selected by default for a selected building and floor. You can change it to another building or to a location or workplace profile user of your choice.
    3.  Select direction modes as **Default** or **Accessible**.

        **Note:** Accessible wayfinding paths are placed near or adjacent to an elevator.

    4.  Change the distance measurement units by selecting the distance value.

        You can select either meters or feet based on your preference. The default unit is set based on your location.

    5.  Enable step-by-step directions on the directions card.

        The system displays directions from the start point to the end point. The distance is displayed in feet or in meters based on your selection.

15. Select the Map display settings icon \(![Map display settings icon.](../images/wsd-gear-settings-icon-loc-directorr.png)\) to open the Display options panel.

    -   Show names for permanent assigned seating: Option to show users with permanently assigned seats on the map. Select the check box if you want to display permanent workplace user profiles on the map.
    -   Don't show employee names: Option To hide private workplace users profile names on the map. Select the check box to hide private users on the map.
    -   Select **Apply**.
    ![Map settings display options.](../images/wsd-new-display-settings-loc-dir.png)

    1.  To show layers on the map, select all the available layers for a location or select layers as required.

        **Note:** The Layers that you have defined in Indoor Mapping are shown on the map.

    2.  Select **Apply**.

    ![Map settings display options with Layers selected.](../images/wsd-new-display-options-layers-selected-loc-dir.png)

16. To reset the map to north, select the **Reset North** icon \(![Reset north icon on the map.](../images/wsd-reset-north-icon-loc-directory.png)\) on the map.

17. Select a **Legend** list to view and interpret the colors and symbols or icons available on the map.

    **Legend** shows the following options.

    -   Amenities: Option to view map legend assigned for Spaces types. For example, Room, lounge, desk, and so on.

        ![Map legends for Amenities or space types on the map.](../images/wsd-legend-amenities-new-loc-dir.png)

    -   Space Availability: Option to view map legends for space availability based on reservation states and occupancy states. For example: Available, currently booked, Occupied, and so on.

        ![Map showing space availability legend based on reservation status.](../images/wsd-legend-space-availability--new-loc-dir.png)

    -   Neighborhood: If you have selected the **Neighborhood** check box, the map legend shows a toggle option to show or hide neighborhoods on the map. If the Neighborhood check box isn’t selected on the map menu \(See step 17\), you don't see the option to show or hide the neighborhood on the Legend.

        **Note:** Option to show or hide a neighborhood for a location is dependent on a map property configuration \[sn\_wsd\_space\_map.display\_neighborhood\_on\_the\_map\]. This property is set by your administrator.

        .

        ![Map showing legend available for a neighborhood.](../images/wsd-legend-neighborhood-new-loc-dir.png)

        -   Select the Neighborhood toggle on and toggle off button to show or hide the neighborhoods on the map.
        -   Neighborhoods are color-coded based on the department, cost center, or workplace entity.
        -   Selected locations or workspaces with a neighborhood are filled with neighborhood-assigned colors.
        -   The **Select all** and **Deselect all** options are available on the Legend to select or deselect neighborhoods.
        -   If a space belongs to more than one Neighborhood, it’s represented with a unique color on the map and the Neighborhood is displayed on the map legend with "&amp;."
18. To switch to the Card view, select the toggle button \(![Toggle button to switch to the Map view.](../images/wsd-map-card-view-toggle-button.png)\).


**Parent Topic:**[Manage workplace activities and services with Location directory](../concept/location-directory.md)

**Related topics**  


[Configure map properties for Location Directory](configure-map-properties-location-directory.md)

[Work with the Card view on the Location directory](wsd-card-view-loc-directory.md)

