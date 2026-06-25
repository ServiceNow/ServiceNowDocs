---
title: Display name of the person reserving a space
description: Display the name of a person who booked a space on the floor map.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/displayname-person-booking-rsv.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Display name of the person reserving a space

Display the name of a person who booked a space on the floor map.

## Before you begin

On the floor map, when a space is booked, an option to display the name of the person who reserved the space is available.

Verify that the following plugins are installed:

-   Workplace Core
-   Indoor Mapping
-   Workplace Reservation Management

Role required: admin

## Procedure

1.  In the navigation filter search context, enter **sys\_properties.list**.

    The System Properties \[sys\_properties\] table displays a list of properties.

2.  Search for **sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details** and set the Workplace Core property **sn\_wsd\_core.floor\_plan.portal.show\_reservation\_details** to **true**.

3.  Make a reservation or check for an existing reservation in Workplace Reservation Management.

    For more information, see [Create a reservation]().

4.  On the Map view, select the location, building, and a floor where you have made the reservation.

5.  Select the map gear icon \(\[Omitted image "wsd-gear-settings-icon.png"\] Alt text: Floor map gear settings icon.\) to view Display options.

6.  Select **Show name of the person who booked the space**.

7.  Select **Apply**.

    Reserved or booked spaces show the name of person who booked the space.

8.  Select a reserved space to open the Space details page.

    The name of the person who booked or reserved the space is shown.


**Parent Topic:**[Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management]()

[Add a workplace space for reservation]()

[Add a workplace room for reservation]()

[Configure a reservable module]()

[Assign spaces to an area]()

[Create a standard service]()

[Create a flexible service]()

[Create a workplace service to provide an extra service for a reservation]()

[Create a reservable view]()

[Create a user criteria record]()

[Configure a reservable purpose]()

[Create a quick reservation time slot]()

[Configure virtual meeting providers]()

[Configure Microsoft Teams as virtual meeting provider]()

[Connect Workplace Reservation Management with Microsoft Teams]()

[Connect Workplace Reservation Management with Zoom]()

[Display permanent seat assignments on floor maps]()

[Manage check-in and check-out reservations]()

[Configure automatic check-in for reserved spaces]()

[Configure reservation multi-day settings in Reservable Module]()

