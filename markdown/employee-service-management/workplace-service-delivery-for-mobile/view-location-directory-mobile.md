---
title: Work with Location Directory for Now Mobile app
description: Work with Map view and Card view on the Location directory. Search for employees, locations, and neighborhoods. Filter spaces based on reservation status, occupancy status, and space types. Get directions to a workplace location or collaborators or a workplace profile user using floor maps. Reserve a space or raise a workplace service request or an issue for a location.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/workplace-service-delivery-for-mobile/view-location-directory-mobile.html
release: zurich
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Use, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Work with Location Directory for Now Mobile app

Work with Map view and Card view on the Location directory. Search for employees, locations, and neighborhoods. Filter spaces based on reservation status, occupancy status, and space types. Get directions to a workplace location or collaborators or a workplace profile user using floor maps. Reserve a space or raise a workplace service request or an issue for a location.

## Before you begin

Make sure that the following applications are configured:

-   Workplace Core
-   Indoor Mapping
-   Workplace Reservation Management \(Optional\)

    Filter and display reservation status for a selected location on the Location directory.

-   Workplace Connectors \(Optional\)

    Filter and display occupancy status for a selected location on the Location directory.

-   Workplace Space Mapping

**Note:** Confirm that the map properties for the Location directory are configured by your administrator. Map properties for the Location directory provide options to:

-   Filter spaces based on the reservation and occupancy states.
-   Automatically refresh reservation and occupancy data on the Location directory.
-   Control the Map display setting options to display permanent and private workplace profile users.
-   Show or hide neighborhoods for a location.

For more information, see [Configure map properties for Location directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-service-delivery-for-mobile/wsd-mobile-map-config-properties-loc-directory.md)

Role required: sn\_wsd\_core.workplace\_user \(workplace\_user\)

## Procedure

1.  Log in to the Now Mobile app and select the add \(+\) option on the home page.

    \[Omitted image "wsd-mobile-homepage.png"\] Alt text: Workplace Service Delivery Mobile Home Screen

2.  Tap to select **View Location directory**.

    \[Omitted image "wsd-mob-showing-view-location-directory-button.png"\] Alt text: Option to select and open the View Location directory on Now Mobile app.

    By default, the Map view is displayed. The Location directory home page is displayed on the World map.

    **Note:** If a location doesn’t have indoor Maps, the Location directory opens in the Card view.

3.  Tap to select the **Select Campus** tab.

    \[Omitted image "wsd-mobile-location-directory-homepage.png"\] Alt text: Now Mobile showing the option to select a campus on the Location Directory home page.

    You can also search for a campus or zoom in to select a campus or location.

    1.  On the search bar, search for a campus or location.

    2.  Use the zoom in \(\[Omitted image "wsd-mobile-zoom-in-icon-new-loc-directory.jpeg"\] Alt text: Zoom in control icon to focus on the map artifacts.\) controls on the map to bring into focus the location pin marker icon \(\[Omitted image "wsd-location-pin-icon.png"\] Alt text: Location pin marker on map.\) to select a campus.

    3.  Employees can also pinch to zoom in the location.

        You can also swipe your mobile screen and move around the map to select a location.

4.  When you select a campus, the **Select Building** tab is enabled and the buildings in a campus are displayed.

    For example, Demo campus with Building A and Building B.

    \[Omitted image "wsd-mobile-new-loc-directory-home-page.png"\] Alt text: Location Directory campus showing buildings in a campus on Now Mobile.

5.  Tap on the **Select Building** tab and select a building.

    When you select a building, the **Select Floor** and the **Filters** menu options are enabled.

    **Note:** The **Last updated &lt;time interval&gt;** label is shown on the map after selecting a building. For example, **Last updated 1 min ago**. The map is automatically refreshed if your administrator has enabled the map property \(**Auto Refresh time interval \(in mins\) for showing Reservation and/or Occupancy information on the Location directory**\). This property fetches the latest reservation and occupancy data on the map.

    \[Omitted image "wsd-mobile-last-updated-time-new-loc-directory.jpeg"\] Alt text: Last updated time interval label to show the time when the latest occupancy and reservation data is fetched.

6.  Tap **Select Floor** to select a floor.

    You can also search and select floor from the list.

    \[Omitted image "wsd-mobile-new-search-floors-loc-dir.png"\] Alt text: Search for a floor from the Floor list option.

7.  Select **Filters**.

    Filter spaces or locations on the map by reservation states, occupancy states, and space types \(rooms, gym, elevator, and so on\).

    \[Omitted image "wsd-mobile-filters-new-rsv-occ-status-loc-dir.png"\] Alt text: Filter space availability by reservation status and occupancy status.

    Spaces are filtered and the ones that match the filter conditions are displayed on the map. Spaces that don’t fulfill the filter conditions or that don’t have a filter applied are shown in white \(map polygon color\).

    -   When both reservation and occupancy filters are applied then spaces fulfilling both these conditions are shown.
    -   When only reservation or occupancy filters are applied then only reservation or occupancy states are displayed.
    **Note:** The option to show **Filters** option is configured by your administrator using a map property \[sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir\]. Filters can be applied at a floor or space level for both Card view and Map view.

    1.  Tap to select the **Reservation status** check box to display reservation status and icons on the map.

        For more information about Legends, see Step 12.

    2.  Select and filter spaces based on reservation states.

        For example, you can select any of the following reservation states to display only the selected filter conditions on the map:

        -   Booked
        -   Available
        -   Not Reservable
        -   Currently booked
    1.  Tap to select the **Occupancy status** check box.

        \[Omitted image "wsd-mobile-filters-occupancy-spaces-new-loc-dir.png"\] Alt text: Filter space availability by occupancy status or spaces.

        Occupancy status and related icons are displayed on the map. For more information about Legends, see Step 12.

    2.  Filter spaces by occupancy states.

        For example, select any of the following occupancy states to display on the map:

        -   Occupied
        -   Not Occupied
        -   Sensor not installed
        -   Sensor not working
    -   Tap to select **Spaces** &gt; **Show all space types**.
    -   Filter selected space types on the map. For example, the following space types can be selected:

        -   Rooms
        -   Gym
        -   Cafe
        -   Phone booth
        -   Workspace/Desk
        -   Restroom-Men
        -   Restroom-Women
        -   Miscellaneous
        -   Elevator
        **Note:** Indoor Mapping places types are shown as Spaces types on the Location directory.

    -   Select **Apply** to apply your changes on the map.
    -   Tap and select **Clear** to remove filters.
8.  Tap to select a space on the map to view the space card details panel.

    \[Omitted image "wsd-mobile-new-reservation-states-loc-dir.png"\] Alt text: Select space on the map showing space card details panel on Now Mobile Location directory .

    Space card details show labels or tags for space occupancy and reservation states. For example, **Available**, **currently booked**, or **Sensor not working**.

    1.  Select **Reserve** to reserve an available space.

        For example, tags for reservation and occupancy status are shown in the space card details panel \(**Available \| Sensor not working**\).

        \[Omitted image "wsd-mobile-space-card-details-use-new-loc-directory.png"\] Alt text: Space card details panel on the Location Directory showing both reservation and occupancy status tag.

        \[Omitted image "wsd-mobile-space-card-details-available-use-new-loc-directory.png"\] Alt text: Space card details panel showing reservation status as Available.

    2.  Select **Get Directions** for wayfinding.

        This option enables employees to navigate to a meeting room or to a co-worker's desk and collaborate effectively.

        You can find directions from a selected space to another space in the same building or to another building or to a different floor in another building.

        \[Omitted image "wsd-mob-get-directions-default-path-loc-directory.png"\] Alt text: Get directions panel showing Default and accessible routes for navigation.

    1.  Tap and enter the starting route for wayfinding in the **Select start point**.

        You can enter a workplace profile name, location, desk, or meeting room.

        **Note:** When you select a location, workplace profile or desk that is not configured by your administrator for you to use, a message is displayed `Sorry this location isn’t configured to be shown on the map`.

    2.  Tap and enter the destination for the wayfinding route in **Select End Point**.

        The location is selected by default. You can change it as required to another building, space, or to a workplace profile.

    3.  Select **Default**or **Accessible**.

        Accessible routes or pathways are near or adjacent to an elevator.

        The directions are displayed on the map. You can define directions from one building or floor to another building or floor. For example, get directions from Building A to Building B.

        \[Omitted image "wsd-get-directions-new-loc-dir-wayfinding-buildings.png"\] Alt text: Get directions from one building to another.

        \[Omitted image "wsd-get-directions-collaborator-new-loc-dir.jpeg"\] Alt text: Get directions to a workplace user or collaborator.

        If you try to provide a route or location that is not configured by your administrator, an error message is shown `Sorry! This location is not configured to be shown on the map`.

        \[Omitted image "wsd-mobile-get-directions-error-use-new-loc-directory.png"\] Alt text: Location directory Get directions pathways showing error for locations that are not configured.

        \[Omitted image "wsd-mobile-get-directions-error-use-new-loc-directory.png"\] Alt text: Location for get directions not configured error message.

9.  From the Space details card panel, tap and select the More actions icon \(\[Omitted image "wsd-more-options-icon-loc-directory.png"\] Alt text: More options icon\) and select any of the following options as required:

    -   Copy URL: Option to copy the space browser link. The Copy URL link, when selected, copies the URL link to the clipboard. The space location link can be shared with your team members and colleagues.
    -   Raise an issue: Option to raise a workplace service request.
10. Select the Map display settings icon \(\[Omitted image "wsd-gear-settings-icon-loc-directorr.png"\] Alt text: Map display settings to show layers, private users, and permanent seating on the map.\) to enable or disable the following on the map:.

    -   Don't display employee names: Option to hide employee workplace profile names on the map.
    -   Display permanent seating assignment: Option to show workplace profile users with a permanent seat allocation.
    -   Layers: Option to select and display layers on the map for a selected location. Tap and select **Show all layers** to show all available layers on the map.
    -   Select **Apply** to apply the changes made to map display settings.
11. Tap and select the swipeable drawer on the navigation bar.

    \[Omitted image "wsd-mobile-nav-scalable-drawer-new-loc-dir.jpeg"\] Alt text: Mobile navigation bar displaying swipeable drawer to open and view map legends and neighborhoods.

    Swipe horizontally or sideways to view map legends for workplace amenities, space availability, and neighborhood.

    -   Amenities: Option to view the available space types for a selected location.

        \[Omitted image "wsd-mobile-nav-drawer-amenities-new-loc-directory.png"\] Alt text: Mobile navigation bar displaying workplace amenities.

    -   Space Availability: Option to view the map legends for space occupancy and reservation status.

        \[Omitted image "wsd-mobile-nav-drawer-space-availability-new-loc-dir.png"\] Alt text: Map Legend for Space availability based on reservation and Occupancy status.

    -   Neighborhood: Option to enable and view designated neighborhoods for a selected location.

        **Note:** Option to show or hide a neighborhood for a location is dependent on a map property configuration \[sn\_wsd\_space\_map.display\_neighborhood\_on\_the\_map\] set by your administrator. For more information, see [Configure map properties for Location directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-service-delivery-for-mobile/wsd-mobile-map-config-properties-loc-directory.md).

    \[Omitted image "wsd-nav-drawer-mobile-neighborhood-enabled-new-loc-dir.jpeg"\] Alt text: Navigation bar showing option to enable neighborhood on Now Mobile.

    Select the Neighborhood toggle on and toggle off button to show or hide the neighborhoods on the map.

    -   Neighborhoods are color-coded based on an assigned department, cost-center, or workplace entity.
    -   Spaces with an assigned neighborhood are filled with neighborhood color on the map.
    -   The **Select all** and **Deselect all** options can be used to select or deselect neighborhoods.
    -   Spaces belonging to more than one Neighborhood are represented with a unique color and the neighborhood is displayed in the map legend with "&amp;".
12. Tap to select the Map controls or symbols that are available on the map.

    -   Reset north: Option to select the Reset north icon \(\[Omitted image "wsd-reset-north-icon-loc-directory.png"\] Alt text: Reset north icon.\).
    -   Refresh view: To refresh the map manually, select the Refreshed view icon \[Omitted image "wsd-refresh-icon-loc-directory.png"\] Alt text: Refresh view icon..
    -   Map display settings: Select the Map setting icon \(\[Omitted image "wsd-gear-settings-icon-loc-directorr.png"\] Alt text: Map display settings icon.\) to open the display options:
    -   Zoom controls: Option to zoom in and zoom out on the map. The Zoom in control icon \(\[Omitted image "wsd-mobile-zoom-in-icon-new-loc-directory.jpeg"\] Alt text: Zoom in control icon to focus on the map artifacts.\) and zoom out control icon \(\[Omitted image "wsd-mobile-zoom-out-icon-new-loc-directory.png"\] Alt text: Zoom out map control icon.\) can be used to change the zoom level of the map.
13. To switch to Card view, select the **Card view** tab.

    \[Omitted image "wsd-card-view-tab-mob-loc-directory.png"\] Alt text: Card view tab.

14. Select a campus from the All campuses screen.

    \[Omitted image "wsd-mobile-card-view-all-campuses-new-loc-dir.png"\] Alt text: All campuses screen showing the Select Campus tab.

    The **Select building** tab is enabled when you select a campus.

15. Tap to select a building.

    \[Omitted image "wsd-mobile-card-view-all-buildings-page-loc-dir.png"\] Alt text: All buildings screen with the Select Building tab.

    The **Floor** and **Filter** menu options are activated when you select a building.

16. Tap to select a floor from the **Floor** list options.

    The All Spaces screen appears for a selected floor. Spaces in a building are displayed as individual cards.

17. Tap to select a space from the All Spaces page.

    The space card provides the following information:

    -   Option to mark a space as favorite \(\[Omitted image "favorite-icon.png"\] Alt text: Favorite icon to mark a space as favorite.\)
    -   Space name
    -   Occupancy status
    -   Reservation status
    -   Space image
    -   Floor, building, and campus name and details
    -   Space Capacity
    -   Standard workplace services
    -   Neighborhood
    \[Omitted image "wsd-mob-card-view-loc-directory.png"\] Alt text: Card view location directory.

18. Select **Show on map** to show the selected space on the map.

    The selected space opens in the Map view and displays the space card panel.

    **Note:** The Show on the map is inactive or grayed out when there’s no floor map available for a space.

19. Select **Reserve** to reserve a space.

    Complete your reservation using the Reservation details screen.

20. On the Space card panel, select **Get directions** for wayfinding and visual representation of the routes on a map to navigate to a workplace location or a team member.

    On selecting **Get directions**, you’re redirected to the Map view.

21. Select **Raise an issue** to request a workplace service or raise a workplace service issue.

22. Select a space and select the More actions icon \(\[Omitted image "wsd-more-options-icon-loc-directory.png"\] Alt text: More actions icon to select on a space.\).

    -   Copy URL: Option to share the space location URL link and share it with your team members.
    -   Raise an Issue: Option to raise a workplace service request. This option is available in the More actions option only for a space that can be booked or reserved. In case if a space is already reserved or not available, then the Raise an issue option is available as a button in the space card.

**Parent Topic:**[Using Workplace Service Delivery for Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-service-delivery-for-mobile/using-wsd-mobile.md)

**Previous topic:**[Scan the QR code to reserve a space](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-service-delivery-for-mobile/scan-qr-code.md)

**Next topic:**[Workplace Service Delivery for Mobile references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-service-delivery-for-mobile/wsd-mobile-references.md)

