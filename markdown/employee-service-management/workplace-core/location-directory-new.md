---
title: Manage workplace activities and services with Location directory
description: Explore workplace campuses, sites, buildings, and neighborhoods using the Location directory. Get directions using map routes to a meeting room, building, or co-workers to collaborate effectively. Search for employees, locations, and neighborhood spaces. Reserve a space, request, or report a workplace service issue. Filter spaces by reservation states, occupancy states to get insights on space availability.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Request employee-related services, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Manage workplace activities and services with Location directory

Explore workplace campuses, sites, buildings, and neighborhoods using the Location directory. Get directions using map routes to a meeting room, building, or co-workers to collaborate effectively. Search for employees, locations, and neighborhood spaces. Reserve a space, request, or report a workplace service issue. Filter spaces by reservation states, occupancy states to get insights on space availability.

The location directory provides the Map view and the Card view to manage workplace activities and services. Indoor Mapping must be configured so that your locations can be viewed on a floor map. If a location doesn’t have a floor map, then only Card view is displayed.

## Reservation and occupancy status on the Location directory

Configure the Location directory to filter spaces by reservation and occupancy states.

**Note:** This is controlled through the **Show reservation and/or occupancy information on Location directory** map property and when it is set to true, you can view the reservation and occupancy status for a selected location on the floor map. The Workplace Reservation Management and Workplace Connectors must be installed and configured to show both reservation and occupancy statuses. Occupancy state for a location is displayed when an occupancy sensor provider is integrated with Workplace Connectors and occupancy sensor data is available for a selected location. For more information, see [Configure map properties for Location Directory](../task/configure-map-properties-location-directory.md).

Filter spaces by occupancy and reservation statuses for a selected space.

-   When only Workplace Reservation Management is configured and available for a selected location, filters for reservation status are available. Option to filter by occupancy status isn’t available on the Show filters panel.
-   When only Workplace Connectors with occupancy sensor data is configured, filters for Occupancy status are available. Option to filter by reservation status isn’t available on the Show filters panel.
-   When both Workplace Reservation Management and occupancy sensor plugins are configured and available. The Show filters panel shows both occupancy and reservation statuses.

Based on the occupancy and reservation status, the Location directory shows the following states for space availability on the Card and Map view.

-   **Available**: Status to indicate that a selected space is available for reservation.
-   **Currently booked**: Status to indicate that a space is booked or reserved for a meeting.
-   **Not available**: Status to indicate that the space isn’t available for reservation. This state is shown when Workplace Reservation Management is configured but the **Is Reservable** field on the Reservation portal is set to **false** \(**All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Workplace Spaces**\).
-   **Currently Occupied**: Status to indicate that a location has occupancy sensors. The occupancy state is shown as **Currently Occupied** on the floor map.
-   **Currently unoccupied**: Status to indicate that a location has occupancy sensors but the space isn’t occupied.
-   **Sensor not installed**: Status to indicate that occupancy sensor is not installed and configured for a location.
-   **Sensor not working**: Status to indicate that the occupancy sensor data is in an invalid state or it isn’t functional for a location.

## Map display settings

Configure map display setting options to show permanently assigned workplace locations on the map. If privacy is enabled, workspaces allocated for private users aren’t displayed on the map. For more information, see [Work with the Map view on the Location Directory](../task/wsd-map-view-loc-directiory.md).

## Auto-refresh reservation and occupancy states on Location directory

Configure Map properties to refresh automatically and get the latest reservation and occupancy status on the Location directory. Use filters on the Location directory to filter out and view either reservation or occupancy status or both reservation and occupancy status.

-   **[Configure map properties for Location Directory](../task/configure-map-properties-location-directory.md)**  
Configure map properties to enable reservation states, occupancy states, display permanent seat assignments, or auto-refresh time interval for showing the latest reservation and occupancy information on the map. Show or hide neighborhoods on the Location directory by using a map property.
-   **[Work with the Map view on the Location Directory](../task/wsd-map-view-loc-directiory.md)**  
Work with Map view to search for workplace users, locations, spaces, and neighborhoods. Get directions to a workplace location, meeting rooms, or an employee to collaborate quickly and effectively. Filter spaces based on reservation and occupancy states, space types, or neighborhoods.
-   **[Work with the Card view on the Location directory](../task/wsd-card-view-loc-directory.md)**  
Work with Card view to reserve a space or raise a workplace service request. Filter spaces based on reservation and occupancy data. View designated neighborhoods on the space card. Switch to Map view anytime when you want to locate a workplace location on the map or to get directions to a collaborator or location.

**Parent Topic:**[Request employee-related services](request-employee-services.md)

**Related topics**  


[Schedule your arrival time at a workplace location](../task/schedule-your-arrival-time-to-the-workplace-wsd.md)

[Making workplace reservations](making-workspace-reservations.md)

