---
title: Configure map properties for Location Directory
description: Configure map properties to enable reservation states, occupancy states, display permanent seat assignments, or auto-refresh time interval for showing the latest reservation and occupancy information on the map. Show or hide neighborhoods on the Location directory by using a map property.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Location Directory, Request employee-related services, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configure map properties for Location Directory

Configure map properties to enable reservation states, occupancy states, display permanent seat assignments, or auto-refresh time interval for showing the latest reservation and occupancy information on the map. Show or hide neighborhoods on the Location directory by using a map property.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Space mapping** &gt; **Map properties**.

2.  Configure the map properties for the Location directory.

    For more information about the map properties, see [Properties installed with Workplace Space Mapping](../../workplace-space-mapping/reference/wsd-space-mapping-properties.md).

3.  Select **Save**.

    The updated map configuration properties are available on the Location directory.

4.  Display the name of a person reserving a space on the map by following these steps.

    1.  In the filter navigator, enter `sys_properties.list`.

    2.  Select the **sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details** property.

    3.  Set the value of the property to **true** and save the record.


**Parent Topic:**[Manage workplace activities and services with Location directory](../concept/location-directory.md)

**Related topics**  


[Work with the Map view on the Location Directory](wsd-map-view-loc-directiory.md)

[Work with the Card view on the Location directory](wsd-card-view-loc-directory.md)

