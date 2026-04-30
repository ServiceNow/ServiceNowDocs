---
title: Display name of the person reserving a space
description: Display the name of a person who booked a space on the floor map.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-01-24"
reading_time_minutes: 4
breadcrumb: [Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Display name of the person reserving a space

Display the name of a person who booked a space on the floor map.

## Before you begin

On the floor map, when a space is booked, an option to display the name of the person who reserved the space is available.

Ensure that the following plugins are installed:

-   Workplace Core
-   Indoor Mapping
-   Workplace Reservation Management

Role required: admin

## Procedure

1.  In the navigation filter search context, enter **sys\_properties.list**.

    List of properties in the System Properties \[sys\_properties\] table appears.

2.  Search for **sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details** and set the Workplace Core property **sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details** to **true**.

3.  Make a reservation or check for an existing reservation in Workplace Reservation Management.

    For more information, see [Create a reservation](create-reservation-request-1.md).

4.  On the Map view, select the location, building, and a floor where you have made the reservation.

5.  Select **Show name of the person who booked the space**.

6.  Select **Apply**.

    Reserved or booked spaces show the name of person who booked the space.

7.  Select a reserved space to open the Space details page

    Name of the person who booked or reserved the space is shown.


**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management](install-wsd-reservation-mgmt.md)

[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

