---
title: Properties installed with Workplace Space Mapping
description: The following properties are installed with Workplace Space Mapping. Navigate to All Workplace Space Mapping Properties or enter sys\_properties.list in the context menu and search for Workplace Space Mapping properites.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Workplace Space Mapping reference, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Space Mapping

The following properties are installed with Workplace Space Mapping. Navigate to **All** &gt; **Workplace Space Mapping** &gt; **Properties** or enter sys\_properties.list in the context menu and search for Workplace Space Mapping properites.

<table id="table_hs1_nrx_bbc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_space\_map.mapping\_technology

</td><td>

Specifies the map provider that is used for workplace reservations and wayfinding.You can select Mappedin or Indoor Mapping as the map provider for your instance.

</td></tr><tr><td>

sn\_wsd\_space\_map.legend\_available\_text

</td><td>

Text that is displayed for the `Available` legend.

</td></tr><tr><td>

sn\_wsd\_space\_map.legend\_available\_color

</td><td>

Color that is used for available rooms. The value must be a valid CSS color. If this property is empty, the default color is used.

</td></tr><tr><td>

sn\_wsd\_space\_map.pattern\_available

</td><td>

Name of the image that you want to use for available space patterns.

</td></tr><tr><td>

sn\_wsd\_space\_map.selected\_item\_color

</td><td>

Color that is used for a selected item on the map. The value must be a valid CSS color. If this property is empty, the default color is used.

</td></tr><tr><td>

sn\_wsd\_space\_map.legend\_booked\_text

</td><td>

Text that is displayed for the `Booked` legend.

</td></tr><tr><td>

sn\_wsd\_space\_map.legend\_booked\_color

</td><td>

Color that is used for booked rooms. The value must be a valid CSS color. If this property is empty, the default color is used.

</td></tr><tr><td>

sn\_wsd\_space\_map.display\_seat\_assignment

</td><td>

Displays the permanent seat assignments on the location directory.

</td></tr><tr><td>

sn\_wsd\_space\_map.pattern\_booked

</td><td>

Name of the image that you want to use for reserved space patterns.

</td></tr><tr><td>

sn\_wsd\_space\_map.margin\_between\_labels

</td><td>

Adjusts the margin between labels measured in pixels. The range of values is between `1` and `50`. This property is specific to Mappedin.

</td></tr><tr><td>

sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir

</td><td>

Displays Reservation and Occupancy information on the location directory.

</td></tr><tr><td>

sn\_wsd\_space\_map.auto\_refresh\_show\_rsv\_occ\_data\_loc\_dir

</td><td>

Auto-refresh time interval in minutes to show reservation and occupancy information on location directory. Auto-refresh is turned off if this property is set to `0` or a negative number.Based on this value, the map is automatically updated to display the latest reservation and occupancy information for a selected location.

</td></tr><tr><td>

sn\_wsd\_space\_map.display\_neighborhood\_on\_the\_map

</td><td>

State of the neighborhood indicator on the location directory.You can select one of the following options:

-   **Available**: The employees can view and filter spaces by neighborhoods. You can select the **Neighborhood** check box on the location directory to view neighborhoods for a selected floor.
-   **Inactive**: The **Neighborhood** check box is inactive and not available on the location directory. Employees can’t view neighborhoods for a selected floor.
-   **Default**: The **Neighborhood** check box is available on the location directory and selected by default.
-   **User preference**: The **Neighborhood** check box is available on the location directory but not selected. If you select this option, your preference is stored in your next browser session. To disable neighborhoods on the location directory, you can clear the **Neighborhood** check box.

</td></tr><tr><td>

sn\_wsd\_space\_map.location\_directory\_filter\_persistence

</td><td>

Enables persistence of filters on the location directory.If this property is set to **true**, filters are retained across browser sessions and tabs. If you log out and log in to the location directory, the space availability filter is retained from your last browser session.

</td></tr><tr><td>

sn\_wsd\_space\_map.map\_default\_location

</td><td>

Default location that is zoomed into when you open the location directory.You can select one of the following values:

-   **World map**: The location directory opens in the world map view and doesn’t zoom into any location.
-   **Workplace Profile**: The location directory opens and zooms into your workplace profile location.
-   **User preference**: The location directory zooms into the location that you select.

</td></tr><tr><td>

sn\_wsd\_space\_map.default\_label\_on\_map

</td><td>

Default value that is used for the labels on the map.Select one of the following options:

-   **Space name**: Only the space name or space ID is displayed on the map.
-   **Space and user names**: The space name and the assigned user's name are displayed on the map. If a space doesn't have an assigned user, only the space name or space ID is displayed.
-   **User preference**: Your last session details are cached in the Map settings. Selecting the map displays these options on your next login. For example, if in your previous login session, you selected **Space Name**, the application caches this information and the Space name option for a space is displayed when you login next

The map label shows personalized option based on the employee's selection from their previous login session.


</td></tr><tr><td>

sn\_wsd\_space\_map.default\_label\_on\_map\_reservation

</td><td>

Default value used to display labels on map on the reservation portal search page.**Note:** This property is displayed only when any of the following properties are enabled in Workplace Space Mapping and Workplace Core respectively:

-   sn\_wsd\_space\_map.display\_seat\_assignment: Displays the permanent seat assignments on the location directory. For more information, see [Properties installed with Workplace Space Mapping](wsd-space-mapping-properties.md)
-   sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details:Determines whether reservation details appear when users point to booked spaces on the floor plan in Workplace Service Portal. For more information, see [Properties installed with Workplace Core](../../workplace-service-delivery/reference/properties-installed-with-workplace-service-delivery.md).
    -   Type: true\|false
    -   Default value: false

Employees can select one of following options in \(sn\_wsd\_space\_map.default\_label\_on\_map\_reservation\):

-   **Space name**: The space name or space ID is displayed on the map. Default value is set to Space name.

After enabling this property, navigate to the reservation portal search page and select the Map view option. Spaces on the map shows space IDs or names. Example: A1.0501, A1.0502. Select map settings and notice that the **Don’t show employee names** option is enabled. The map shows only space identifiers or space names and doesn't show employee names.

-   **Assigned user**: The assigned employee name or permanent seats for employees with a workplace profile are displayed on the map. For this property to work, make sure that you have enabled the **Enable Display of permanent seat assignments on map** property in Workplace Space Mapping.

After enabling **Enable Display of permanent seat assignments on map**, navigate to the Reservation portal search page and select the Map view option.

**Note:** If a space doesn't have an permanent seat assignment or workplace profile assigned to it, only the space name or space IDs are displayed. Enabling the **Enable Display of permanent seat assignments on map** property shows only permanent seating of employees on the map and it doesn't show temporary reservations.

-   **Reserved User**: The reserved user's name is displayed on the name along with the space name.

**Note:** Make sure to enable sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details property on Workplace Core.

After enabling the **sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details** Workplace Core property, navigate to the reservation portal search page and select the Map view option. For reserved spaces, the map shows the name of the person who reserved it. For example, if Abel Tuter reserved a space, the map shows Abel Tuter.

-   **User preference**: Your last session details are cached in the Map settings on the reservation portal search page. Selecting the map displays these options on your next login. For example, if in your previous login session, you selected Reserved User, the application caches this information and the **Reserved User** option for a space is displayed when you login next.

For example, if an employee selects the following:

    -   Space name: Map shows the space IDs or space names.
    -   Assigned user: Map shows permanent seating names.
    -   Reserved user: Map shows reservation owner names.
The map label shows personalized option based on the employee's selection from their previous login session.


</td></tr></tbody>
</table>**Parent Topic:**[Workplace Space Mapping reference](../concept/wsm-reference.md)

**Related topics**  


[Components installed with Workplace Space Mapping](wsm-mappedin-components.md)

