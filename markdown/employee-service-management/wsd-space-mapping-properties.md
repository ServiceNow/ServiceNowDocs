---
title: Properties installed with Workplace Space Mapping
description: The following properties are installed with Workplace Space Mapping.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/wsd-space-mapping-properties.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Properties installed with Workplace Space Mapping

The following properties are installed with Workplace Space Mapping.

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

Default value that is used for the labels on the map.You can select one of the following options:

-   **Space names**: Only the space name is displayed on the map.
-   **Space and user names**: The space name and the assigned user's name are displayed on the map. If a space doesn't have an assigned user, only the space name is displayed.
-   **User preference**: You can select whether only space names or space and user names are displayed on the map.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Space Mapping reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/wsm-reference.md)

**Related topics**  


[Components installed with Workplace Space Mapping]()

