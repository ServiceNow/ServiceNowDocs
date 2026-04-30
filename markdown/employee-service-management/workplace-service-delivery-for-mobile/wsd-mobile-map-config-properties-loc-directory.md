---
title: Configure map properties for Location directory
description: Configure map properties to enable reservation states, occupancy states, display permanent seat assignments, or auto-refresh time interval for showing the latest reservation and occupancy information on the map. Show or hide neighborhoods on the Location directory.
locale: en-US
release: zurich
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Configure map properties for Location directory

Configure map properties to enable reservation states, occupancy states, display permanent seat assignments, or auto-refresh time interval for showing the latest reservation and occupancy information on the map. Show or hide neighborhoods on the Location directory.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Space mapping** &gt; **Map properties**.

2.  Configure the following map properties for Location directory:

<table id="table_v2n_pj4_vcc"><thead><tr><th>

Map property

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Show Reservation and/or Occupancy information on Location directory \[sn\_wsd\_space\_map.show\_rsv\_occ\_data\_loc\_dir\]

</td><td>

Option to show the reservation and occupancy states on the Location directory. Set the map property to **Yes** to display reservation and occupancy status on the location directory.

</td></tr><tr><td>

Auto Refresh time interval \(in mins\) for showing Reservation and/or Occupancy information on the Location directory.

</td><td>

Option to auto-refresh reservation and occupancy information on the Location directory.Enter the map property value in minutes. Default value is `2` minutes. Based on this value, the map is updated and refreshed automatically every 2 minutes with the latest reservation and occupancy information for a selected location. You can change the default value as appropriate. Zero or negative integer value deactivates this property. Decimal values are not supported.

**Note:** Make sure that you have enabled the map property Show Reservation and/or Occupancy information on Location directory. Auto-refresh time interval is displayed on the Location directory only when the Show Reservation and/or Occupancy information on Location Directory map property is enabled. If the Show Reservation and/or Occupancy information on Location Directory is set to **No**, the auto-refresh of reservation and occupancy information is not shown on the Location directory.

</td></tr><tr><td>

Configure the default state for the neighborhood indicator on the location directory \[sn\_wsd\_space\_map.display\_neighborhood\_on\_the\_map\]

</td><td>

Map property to display the neighborhood on the Location directory. Select any of the following available list option as required: -   Available: The **Neighborhood** toggle button is available on the Location Directory but is not selected. Select the check box to view neighborhoods for a selected floor.
-   Disabled: The **Neighborhood** toggle button is disabled and not available on the Location Directory. Employees cannot view neighborhoods for a selected floor.
-   Default: By default, the **Neighborhood** toggle button is available and enabled on the Location directory.
-   User preference: By default, the **Neighborhood** toggle button on the Location directory is not enabled. If you select this option, your preference is stored in your next browser session. To disable neighborhoods on the Location directory, you can deselect the Neighborhood check box.


</td></tr><tr><td>

Enable persistence of filters on the location directory \[sn\_wsd\_space\_map.location\_directory\_filter\_persistence\]

</td><td>

Select **Yes** to enable persistence of space availability filters for browser sessions and tabs on the location directory.By default, this property is set to true.

The filters are retained or persist across browser sessions and tabs. Applied filter information is retained from your last browser session.

</td></tr></tbody>
</table>3.  Select **Save**.

    The updated map configuration properties are available on the Location directory.


**Parent Topic:**[Configure Workplace Service Delivery for Mobile](../concept/configure-wsd-mobile.md)

**Previous topic:**[Configure AI search for Workplace Service Delivery for Mobile](configure-ai-search-mobile.md)

**Next topic:**[Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../concept/workplace-preference-schedule.md)

