---
title: Customize the map properties
description: Customize how your map renders in the Workplace Service Portal by configuring Workplace Space Mapping properties.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting up Workplace Space Mapping, Configure, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Customize the map properties

Customize how your map renders in the Workplace Service Portal by configuring Workplace Space Mapping properties.

## Before you begin

Role required: admin

## About this task

Indoor maps properties are specific to ServiceNow AI Platform capabilities. Map properties are customizable and define and determine the appearance of the legend, labels, or text that is displayed on an indoor map. Select Indoor Mapping or Mappedin as your map provider. Indoor Mapping is an inbuilt map provider with Workplace Service Delivery.

**Note:** The map legend is available only on the map view in **Workplace Core** &gt; **Workplace services portal** &gt; **Make a reservation**.

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

Option in the map legend for spaces that can be booked or reserved. Select Available, Free, or Open.

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

Option in the map legend to indicate spaces that are already booked or reserved. Select Booked, Reserved, or Taken.

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

Displays permanent seat assignments on a map. The employee names are also displayed if the employee names are part of a workplace profile. Select Yes.A Toggle button is available on the floor map to enable or disable this option. For more information, see [Display permanent seat assignments on floor maps](../../wsd-reservation-management/task/display-permanent-seats-on-maps.md).

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

Auto Refresh time interval \(in minutes\) for showing Reservation and/or Occupancy information on Location Directory \[sn\_wsd-space\_map.auto\_refresh\_show\_rsv\_occ\_data\_loc\_dir\].

</td><td>

Option to automatically refresh the map to fetch the reservation and occupancy states on the Location directory portal. Default value is 2. **Note:** This property is only valid if the **Show Reservation and/or Occupancy information on Location Directory** property is set to true.

The auto refresh feature is only available at the floor or space level and is not supported at the campus or building level. Reservation and Occupancy states are shown only on **Map view** and not available on the **Card view** on the Location directory.

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Setting up Workplace Space Mapping](../concept/set-up-workplace-service-mapping.md)

