---
title: Customize the map properties
description: Customize how buildings, floors, and spaces appear on the map by configuring Workplace Space Mapping properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/wsm-configure-map-properties.html
release: brazil
topic_type: task
last_updated: "2026-11-11"
reading_time_minutes: 2
breadcrumb: [Setting up Workplace Space Mapping, Configure, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Customize the map properties

Customize how buildings, floors, and spaces appear on the map by configuring Workplace Space Mapping properties.

## Before you begin

Role required: admin

Before you customize the map, make sure that:

-   Your location and workplace data is imported from Indoor Mapping and synchronized with Workplace Service Delivery. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/indoor-mapping/synchronize-ind-mapping-wsd.md).
-   The latitude and longitude of your campuses and buildings are set. Without them, employees can't see a campus or its buildings on the map.

## About this task

Map properties are customizable. They control the appearance of the legend, labels, or text that is displayed on an indoor map. Select Indoor Mapping as your map provider. Indoor Mapping is a built-in map provider with Workplace Service Delivery.

The map is what employees see when they browse locations on the Location directory or select **Map view** while reserving a space. The map is built from your location hierarchy and your map data:

-   The floor map shows the spaces for a selected floor.
-   The map draws buildings, floors, and spaces from the Indoor Mapping map data that you synchronized with Workplace Service Delivery.
-   A floor without an Indoor Mapping map is tagged as **No map**, and employees see the Card view instead.
-   Spaces are color-coded to show reservation status when Workplace Reservation Management is installed, and occupancy status when Workplace Connectors is configured. Map properties set the colors, patterns, and legend text.

Use map properties to control:

-   The colors, patterns, and legend text for available and booked spaces, and the color of a selected space.
-   Whether permanent seat assignments and neighborhoods are displayed, and which location the map opens on.
-   Whether the map automatically refreshes reservation and occupancy information.

## Procedure

1.  Navigate to **Space Mapping** &gt; **Map properties**.

2.  Set the map properties based on your preference.

    For more information about the map properties, see [Properties installed with Workplace Space Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/wsd-space-mapping-properties.md).

3.  Select **Save**.

4.  Preview the changes on the map.

    Open the Location directory, or select **Map view** from Workplace Reservation Management while making a reservation, and select a building and floor. For more information, see [Work with the Map view on the Location Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-core/wsd-map-view-loc-directiory.md) and [Create a reservation]().


## Result

Employees see the updated colors, labels, and legend when they browse buildings and floors on a map while reserving a space.

To show the map in reservations on the mobile app, see [Enable map view to create reservations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/workplace-service-delivery-for-mobile/enable-map-view-mobile-reservations.md).

**Parent Topic:**[Setting up Workplace Space Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/set-up-workplace-service-mapping.md)

