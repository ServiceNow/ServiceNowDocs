---
title: Customize the map properties
description: Customize how your map renders in the Workplace Service Portal by configuring Workplace Space Mapping properties.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up Workplace Space Mapping, Configure Workplace Space Mapping, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Customize the map properties

Customize how your map renders in the Workplace Service Portal by configuring Workplace Space Mapping properties.

## Before you begin

Role required: admin

## About this task

Indoor maps properties are specific to ServiceNow AI Platform capabilities. Map properties are customizable and define and determine the appearance of the legend, labels, or text that is displayed on an indoor map. Select Indoor Mapping or Mappedin as your map provider. Indoor Mapping is an inbuilt map provider with Workplace Service Delivery.

## Procedure

1.  Navigate to **Space Mapping** &gt; **Map properties**.

2.  Set the following property values.

<table id="table_gqj_5pg_rrb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Define whether the Mappedin or Indoor Mapping map provider is used for reservations and wayfinding.\[sn\_wsd\_space\_map.mapping\_technology\]

</td><td>

Select **Indoor Mapping** or **Mappedin** as your map provider. **Note:** Indoor Mapping is a part of the Workplace Service Delivery suite. Mappedin is a third-party map provider and requires a separate installation license.

</td></tr><tr><td>

Text to display for 'Available' legend.\[sn\_wsd\_space\_map.legend\_available\_text\]

</td><td>

Option in the map legend for spaces that can be booked or reserved. Select **Available**, **Free**, or **Open**.

</td></tr><tr><td>

Color to use for 'available' rooms \(must be a valid CSS color\), leave empty to use the default color.\[sn\_wsd\_space\_map.legend\_available\_color\]

</td><td>

Option to indicate the CSS color or color name for spaces that can be reserved. If the color is not a valid CSS or if the property is empty, the indoor map uses the default color.

</td></tr><tr><td>

Write the name of the image you want to use for available spaces pattern

 \[sn\_wsd\_space\_map.pattern\_available\]

</td><td>

Image pattern to show available spaces on a floor map. For example: pattern-available.svg

</td></tr><tr><td>

Text to display for 'Booked' legend.\[sn\_wsd\_space\_map.legend\_booked\_text\]

</td><td>

Option in the map legend to indicate spaces that are already booked or reserved. Select **Booked**, **Reserved**, or **Taken**.

</td></tr><tr><td>

Color to use for 'booked' rooms \(must be a valid css color\), leave empty to use the default color.\[sn\_wsd\_space\_map.legend\_booked\_color\]

</td><td>

The CSS color or color name to indicate spaces that are already booked or reserved. If the color is not a valid CSS color or if the property is empty, the indoor map uses the default color.

</td></tr><tr><td>

Color to use for a selected item on the map \(must be a valid css color\), leave empty to use the default color.\[sn\_wsd\_space\_map.selected\_item\_color\]

</td><td>

The CSS color or color name to indicate space that is selected. If the color is not a valid CSS color or the property is empty, the map will use the default color.

</td></tr><tr><td>

Write the name of the image you want to use for reserved space patterns.

 \[sn\_wsd\_space\_map.patter\_booked\]

</td><td>

Image pattern to show reserved spaces on a floor map. For example: pattern-booked.svg.

</td></tr><tr><td>

Enable display of permanent seat assignments on map.\[sn\_wsd\_space\_display\_seat\_assignment\]

</td><td>

Displays permanent seat assignments on a map. The employee names are also displayed if the employee names are part of a workplace profile. Select **Yes**.A Toggle button is available on the floor map to enable or disable this option. For more information, see [Display permanent seat assignments on floor maps](../../wsd-reservation-management/task/display-permanent-seats-on-maps.md).

**Note:** This property is available when you have Indoor Mapping maps.

</td></tr><tr><td>

\(Mappedin specific\) Adjust the margin between labels measured in pixels \(1-50\)\[sn\_wsd\_space\_map.margin\_between\_labels\]

</td><td>

Sets the space between labels and determines how many labels are visible at once. A lower value results in more labels while a higher value results in fewer labels. This property is available only for Mappedin indoor maps.

</td></tr><tr><td>

Show Reservation and/or Occupancy information on Location Directory \[sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir\]

</td><td>

Displays Reservation and Occupancy states on the Location directory portal. Set the value to **Yes** to see the occupancy and reservations states on the map.

</td></tr><tr><td>

Configure the default state for the neighborhood indicator on the location directory \[sn\_wsd\_space\_map.display\_neighborhood\_on\_the\_map\]

</td><td>

Map property to display the neighborhood on the Location directory. Select any of the following available list options as required: -   Available: The employees can view and filter spaces by neighborhoods. The **Neighborhood** check box is not selected by default. Select the check box to view neighborhoods for a selected floor.
-   Inactive: The **Neighborhood** check box is inactive and not available on the Location Directory. Employees can’t view neighborhoods for a selected floor.
-   Default: By default, the **Neighborhood** check box is available and enabled on the Location directory.
-   User preference: By default, the **Neighborhood** check box on the Location directory isn’t enabled. If you select this option, your preference is stored in your next browser session. To disable neighborhoods on the Location directory, you can deselect the Neighborhood check box.


</td></tr><tr><td>

Enable persistence of filters on the location directory \[sn\_wsd\_space\_map.location\_directory\_filter\_persistence\]

</td><td>

Select **Yes** to enable persistence of space availability filters for browser sessions and tabs on the location directory.By default, this property is set to true.

The filters are retained or persist across browser sessions and tabs. If you log out and log in to the Location directory, space availability filter information is retained from your last browser session.

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Setting up Workplace Space Mapping](../concept/set-up-workplace-service-mapping.md)

