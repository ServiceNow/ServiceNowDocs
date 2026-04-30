---
title: Explore Workplace Calendar Synchronization
description: Enhance your workplace reservation experience. Synchronize your reservations with your calendar provider by using the ServiceNow Workplace Calendar Synchronization application. Enable your employees to make reservations with ServiceNow Workplace Reservation Management or with your organization's calendar service providers, such as Microsoft Exchange Online.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2025-09-08"
reading_time_minutes: 3
breadcrumb: [Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Explore Workplace Calendar Synchronization

Enhance your workplace reservation experience. Synchronize your reservations with your calendar provider by using the ServiceNow® Workplace Calendar Synchronization application. Enable your employees to make reservations with ServiceNow® Workplace Reservation Management or with your organization's calendar service providers, such as Microsoft Exchange Online.

The Workplace Calendar Synchronization application synchronizes reservation-related information based on the configuration made on the requested workplace room. When you synchronize with a calendar provider, the reservations are directly added to the calendars of your employees.

**Note:** Workplace Calendar Synchronization Guided setup is available for system administrators and is provided out of the box with the application. The Guided setup can be accessed from **All** &gt; **Workplace Calendar Synchronization** &gt; **Administration** &gt; **Guided setup**.

![Workplace Calendar Synchronization Guided Setup configuration steps.](../image/wsd-guided-tour-landing-page.png "Workplace Calendar Synchronization Guided Setup")

The Workplace Calendar Synchronization application supports the following calendar services:

-   Microsoft Exchange Online
-   Google Calendar
-   Microsoft Exchange On - Premises

    **Note:** Workplace Calendar Synchronization does not support hybrid Microsoft Exchange environments.


The Workplace Calendar Synchronization application uses the calendar service as the primary source. However, the availability for a workplace room can be checked either using the calendar provider or the Reservation portal separately. Events are sent and received from the calendar provider for updates. The calendar provider confirms reservations on rooms created using the Workplace Reservation Management Reservation portal.

## Specify your connection and synchronization settings

As an admin, you can do the following:

-   Configure connections with a calendar service.
-   Configure workplace items that require synchronization when they’re reserved.
-   Monitor events and calendar events that are created in the applications. For information about how events work, refer to [Events in Workplace Calendar Synchronization](../reference/events-in-workplace-calendar-synchronization.md).
-   For Google Calendar and Microsoft Exchange, receive calendar updates via synchronization deltas \(Sync deltas\). A Sync delta contains a token using which the application retrieves only the changes that happened since the last interval instead of displaying the complete calendar history of the workplace item.

    **Note:** If you’re using Microsoft Exchange Online, you cannot view synchronization deltas.

-   For Microsoft Exchange Online, receive calendar updates through subscriptions and callback events. A callback event triggers the application to retrieve the calendar information.
-   For Google Calendar and Microsoft Exchange On Premises, receive calendar updates via synchronization deltas \(Sync deltas\). A Sync delta contains a token using which the application retrieves only the changes that happened since the last interval instead of displaying the complete calendar history of the workplace item.

You can create a connection with your calendar service by using the following configuration form:

![Configuration form for the calendar provider.](../image/calendar-service-confg-form.png)

## Create or update reservations

As an employee, you can do the following:

-   Make a reservation for a workplace item in both the Workplace Reservation Management application and synchronize it with your calendar service.
-   Update a reservation or cancel a reservation using the calendar provider or the Workplace Reservation Management application. View the reservation details, add attendees, change location or more.

    **Warning:** Reservations that are created using calendar providers cannot be edited in the Workplace Reservation Management application

-   Check the availability of workplace items using both Workplace Reservation Management and your calendar service.
-   Using the calendar provider, plan meetings, add a location, invite attendees and more. The meeting is synchronized to Workplace Reservation Management as a reservation.​
-   See all your workplace reservations in a single place.

    **Note:** Only rooms added in the Rooms \[sn\_wsd\_core\_room\] table are synchronized using the calendar provider. To synchronize spaces, that spaces must be added as rooms in the Rooms \[sn\_wsd\_core\_room\] table.


## Synchronized information

When you synchronize your calendar provider and Workplace Reservation Management, whenever a reservation is created or updated, the following information is synchronized:

-   Details of the reserved location
-   Subject​ of the reservation
-   Start and end time​s of the reservation
-   Privacy of the reservation
-   Invitees of the reservation

**Parent Topic:**[Workplace Calendar Synchronization](workplace-calendar-sync-feat.md)

