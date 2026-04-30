---
title: Proximity calculation when browsing near a person
description: When an employee searches for a space near a person using the Browse near a person option, the workplace locations are displayed based on the closest proximity.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Proximity calculation when browsing near a person

When an employee searches for a space near a person using the **Browse near a person** option, the workplace locations are displayed based on the closest proximity.

## Proximity calculation flow

The factors that influence the proximity based search are explained below:

1.  **Floor plan**: After the employee specifies the colleague near whom they want to reserve a space, the application checks if the colleague's location has a floor plan defined.
    -   If there is a floor plan, then the floor map coordinates are used to find the nearest space.
    -   If there is no floor plan, then the next step is performed.
2.  **Area**: If there are no floor plans defined for the colleague's location, then the application checks if the location is part of an area.
    -   If the location is part of an area, then the available spaces are displayed based on the area configuration.
    -   Only available spaces on the floor where the employee is located are displayed.
    -   If the location is not part of any area, then the next step is performed.
3.  **Tag**: If the location is not part of any area, then the application checks if the colleague's location has any tags.
    -   If the location has a tag, then all the available spaces with the same tag value are displayed.
    -   Only available spaces on the floor where the employee is located are displayed.
    -   If the location does not have a tag, then all the available spaces of the floor where the colleague is located are displayed.

-   For proximity based search that involves area and tag, only the available spaces on the floor where the employee is located are displayed.
-   If there are is no area or tag defined, then the available spaces of that floor are displayed. If there are no available spaces on that, then a message is displayed that there no matching spaces found.
-   By default the **My favorites first** sort option is selected when an employee searches for spaces using the **Browse all** or **Browse by area** option.
-   If an employee searches for a space using the **Browse near a person** option, then the spaces are displayed based on the closest proximity. If the employee selects the **My favorites first** sort option, then the favorite spaces of that employee which have the closest proximity are displayed first.

By default, all the available spaces are displayed based on the above proximity calculations. In case the employee has set favorite locations and has selected the **My favorites first** sort option, then the favorite locations are displayed at first.

**Parent Topic:**[Workplace Reservation Management references](../concept/rsv-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Reservation Management](components-installed-with-wsd-reservation-mgmt.md)

[Properties installed with Workplace Reservation Management](properties-installed-with-wsd-reservation-mgmt.md)

[Workplace Reservation Management - Field descriptions](../concept/workplace-reservation-management-field-descriptions.md)

[Reservable module derivation logic for Space details](../concept/reservation-logic-for-myfavorites-space-details.md)

[Mobile push notifications for workplace reservations](reservation-push-notifications.md)

[Location privacy settings and impact](location-privacy-settings-and-impact.md)

[Additional details record producer - Mapping Variable types and limitations](custom-fields-record-producer-mapping-variable-type-conditions.md)

