---
title: Work with the Card view on the Location directory
description: Work with Card view to reserve a space or raise a workplace service request. Filter spaces based on reservation and occupancy data. View designated neighborhoods on the space card. Switch to Map view anytime when you want to locate a workplace location on the map or to get directions to a collaborator or location.
locale: en-US
release: xanadu
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2024-09-23"
reading_time_minutes: 7
breadcrumb: [Manage workplace activities and services with Location directory, Request employee-related services, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Work with the Card view on the Location directory

Work with Card view to reserve a space or raise a workplace service request. Filter spaces based on reservation and occupancy data. View designated neighborhoods on the space card. Switch to Map view anytime when you want to locate a workplace location on the map or to get directions to a collaborator or location.

## Before you begin

Make sure to activate and configure the following plugins:

-   Workplace Core
-   Workplace Reservation Management
-   Workplace Connectors
-   Indoor Mapping
-   Workplace Space Mapping

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center** &gt; **Workplace Services**.

2.  From the **Workplace Services** list, select **Browse Workplaces** &gt; **Support resources** &gt; **Location Directory**.

    Location directory home page is displayed. By default, the Location directory opens in the Map view. If there are no maps available for a location, the Card view is opened by default.

    .

3.  If you are on the Map view, select the Card view icon \(![Card view icon on the Location directory to switch to Card view.](../images/wsd-card-view-icon.png)\) to switch to the Card view.

    The Card view home page is displayed with a list of all campuses.

    ![Card view home page showing list of campus. Select or search for a campus.](../images/wsd-card-view-new-loc-dir-homepage.png)

4.  Select a campus from the **Select campus** tab.

    You can also search for a campus using the search field option on the Card view.

    To sort locations alphabetically, select **Alphabetically** and sort as required \(A to Z or Z to A\).

5.  When you select a campus, the **Select Building** tab is enabled.

    ![Location directory card view showing the Select Building option.](../images/wsd-card-view-building-tab-new-loc-directory.png).

6.  Select a building from the **Select Building** list option.

    For example, Building A.

    When you select a building, the **Floor** tab is enabled on the Card view. After selecting a floor, the **Show Filters** option is enabled.

7.  After selecting a building, select **See Spaces** to view the number of allocated workspaces for a building.

    The All spaces page for a selected building is displayed. All spaces in a building are displayed as individual cards.

    **Note:** Space card doesn't show the Show on map option when there’s no map available for a building. The toggle button icon \(![Toggle button to switch to the Map view.](../../wsd-for-mobile/images/wsd-map-card-view-toggle-button.png)\) to switch to Map view is also grayed out on the Card view.

    ![All Spaces showing spaces in a selected building with option to reserve a space or raise an workplace service](../images/wsd-card-view-spaces-new-loc-dir.png)

    Labels or tags available on a space card show Reservation and Occupancy status, number of seats available in that space, and designated neighborhoods. The space card also provides the following information:

    -   Option to mark a space as favorite \( ![Favorite icon to mark a space as favorite.](../../wsd-reservation-management/image/favorite-icon.png)\)
    -   Space name
    -   The employee avatar or workplace profile initials are displayed as image on the space card details.
    -   Occupancy status
    -   Reservation status
    -   Space image
    -   Floor, building, and campus name and details
    -   Space Capacity
    -   Standard workplace services
    -   Neighborhood
8.  On the space card, select the More actions icon \(![More actions icon to select copy URL and raise an issue options.](../../wsd-for-mobile/images/wsd-more-options-icon-loc-directory.png)\).

    ![Card view showing the Copy URL and Raise an Issue options for a space.](../images/wsd-card-view-new-copy-url-loc-directory.png)

    Select the following options as required:

    -   Copy URL: Option to share the space location browser link and share it with your team members.
    -   Raise an Issue: Option to raise a workplace service request. This option is available in the More actions option only for a space that can be booked or reserved. In case if a space is already reserved or not available, then the Raise an issue option is available as a button in the space card.
9.  Select **Reserve** to reserve a space.

    The selected space opens in a browser tab. The space card details page shows options to select reservation **Start date and time** and **End date and time**. The selected space is also shown on the map \(if floor map is available\). Complete the reservation process on the Reservation details page.

    ![Space Card details showing option to reserve a space.](../images/wsd-reserve-spac-card-view-loc-dir.png)

10. Navigate back to the All spaces page on the Card view and select **Show on map**.

    The space card details panel opens on the map and shows option to raise a request or reserve a space, and get directions to a location for wayfinding. For more information, see [Work with the Map view on the Location Directory](wsd-map-view-loc-directiory.md).

11. Select **Raise an issue** to request a workplace service or raise a workplace service issue.

    You’re redirected to the General Request page on the Employee center.

12. Select **Show filters** to filter spaces based on reservation states, occupancy states, and space types.

    **Note:** The **Show filters** button is displayed on the map when **Show Reservation and/or Occupancy information on the Location directory** \[sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir\] map property is set to **Yes** by your administrator. Filters can be applied at a floor or space level. When this property is set to **No**, only space type filters are available for you to select.

    ![Card view showing the filter options for space availability based on reservation status, occupancy status, and space types.](../images/wsd-card-view-show-filters-new-loc-dir.png).

    Select and filter any of the following options as required:

    1.  Select the **Reservation status** check box filter to view space availability on the map.

    2.  Select the required reservation status to filter spaces based on reservation data for a selected location.

        For example, the following reservation states are displayed on the map for a selected space.

        -   Booked
        -   Available
        -   Not Reservable
        -   Currently booked
    1.  Select the **Occupancy status** check box to view the occupancy status for a selected space or a location on the map.

        **Note:** Occupancy states are only shown on the map if Workplace Connectors is configured for a selected location. Your administrator must also configure the map property **Show Reservation and/or Occupancy information on Location directory \[sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir\]**. For more information, see [Configure map properties for Location Directory](configure-map-properties-location-directory.md).

    2.  Select the following options as required:

        -   Occupied
        -   Not Occupied
        -   Sensor not installed
        -   Sensor not working
        -   When both reservation and occupancy filters are applied, then spaces fulfilling both these conditions are shown.
        -   When only reservation or occupancy filters are applied then only reservation or occupancy states are displayed.
        -   Spaces on the map that are matching the filter conditions are highlighted.
        -   Spaces that don’t fulfill the filter conditions or that don’t have a filter applied are shown in white \(polygon color\).
    1.  Select the **Spaces** check box to filter selected space types on the Card view.

        **Note:** Indoor Mapping place types are available as space types on the Location directory.

    2.  Select the required spaces.

        For example, the following space types can be selected:

        -   Rooms
        -   Gym
        -   Cafe
        -   Phone booth
        -   Workspace/Desk
        -   Restroom-Men
        -   Restroom-Women
        -   Miscellaneous
        -   Elevator
13. Select **Apply** to apply the filters.

    The selected filters are applied and the **Filter by label** shows filtered items as pills. For example: Booked, Available, and so on. Select **Clear All** to remove the filters.

14. To switch to Map view, select the toggle button \(![Toggle button icon to switch to Map view from card view.](../../wsd-for-mobile/images/wsd-map-card-view-toggle-button.png)\).

    For more information, see [Work with the Map view on the Location Directory](wsd-map-view-loc-directiory.md).


**Parent Topic:**[Manage workplace activities and services with Location directory](../concept/location-directory.md)

**Previous topic:**[Work with the Map view on the Location Directory](wsd-map-view-loc-directiory.md)

**Next topic:**[Publish Now Assist in Virtual Agent topics for Workplace Service Delivery](publish-now-assist-va-topics.md)

