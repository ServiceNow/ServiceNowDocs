---
title: Make a reservation
description: The 'Make a reservation' form also referred to as the Reservation portal, is a central location for reserving workplace items, such as meeting rooms and desks. You can also view and manage your reservations. After a reservation request is confirmed, you're notified about the reservation details.
locale: en-US
release: zurich
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore Workplace Reservation, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Make a reservation

The 'Make a reservation' form also referred to as the Reservation portal, is a central location for reserving workplace items, such as meeting rooms and desks. You can also view and manage your reservations. After a reservation request is confirmed, you're notified about the reservation details.

You can reserve a workplace item for any period between 00:00 to 23:59 \(midnight to 11:59 p.m.\) on the same day. For example, you can make a reservation until anytime before 23:59. If the reservation continues to another day, you must create a separate reservation.

You can make a reservation from the Workplace Reservation Management application and the Workplace Service Portal.

-   To open the 'Make a reservation' form from the application, navigate to **Workplace Reservation Management** &gt; **New Reservation**.
-   To open the 'Make a reservation' form from the Workplace Service Portal, perform the following actions:
    1.  Select **Reservations** &gt; **Make a reservation**.
    2.  Select **Make a reservation** directly on the home page.
    3.  Select **New general reservation** from the Workplace services catalog.

The 'Make a reservation' form enables you to do the following:

-   View workplace items such as meeting rooms and desks for your location or for a different location.
-   View the availability of a meeting room or desk before making a reservation request.
-   Use workplace floor maps to find and reserve a space within Workplace Core. To view the maps in the Location directory and within Workplace Reservation Management, use Mappedin and Indoor Mapping. For more information on how to use floor maps, see [Workplace Space Mapping](../../workplace-space-mapping/concept/wsm-mappedin-admin.md).
-   Check for any standard services that are available with workplace items, such as whiteboards, seating capacity, and projector.
-   Reserve a workplace item for yourself or on behalf of someone else.
-   Reserve multiple buildings for a single reservation. For more information, see [Create multi-building reservations](../task/create-multi-building-reservation.md).
-   View the details of the reservations that you've created.
-   Modify or cancel the reservations that you've created.
-   Share reservation details with others.
-   Browse workplace locations near a person and make a reservation.
-   Reserve multiple workplace locations in a single reservation.
-   Make a group reservation for different users in a single reservation. You can manage the group reservation in the parent reservation.
-   Download an iCalendar of a reservation to add the reservation to your calendar.

You can also use the Virtual Agent chat support on the Workplace Service Portal to make a reservation and view your reservation details. The chat support enables you to do the following:

-   Create a reservation for a location.
-   View the reservations that you created on the current day.
-   See when your reservation will start or happen.
-   Cancel a reservation.

## Recurring reservations

When you reserve a workplace item for a recurring event, the reservation gets repeated for the indicated days of the specified period. You determine the applicable days when you create the request. The reservation that you initially created acts as the parent reservation record.

If a reservation occurrence conflicts with an existing reservation on a particular day, the reservation occurrence for that day is not confirmed and the state changes to **Conflicted**. The system tries to find an alternative space automatically for **Conflicted** states.

-   If a floor map is available, the Workplace Reservation Management application finds a space closest to the same capacity, then looks for one with more capacity, and lastly, for one with less capacity.
-   If no floor map is available, the application finds an alternative space in the same area or on the same floor.
-   The favorite spaces are prioritized over 'location' \(within the same area or proximity\).
-   The employee can find an alternative space easily if no alternative space was found.
-   The employee is notified when the application assigns an alternative space.

For more information about automatically resolving recurring conflicts, see [Configure a reservable module](../task/config-reservable-module.md) and [Create a reservation](../task/create-reservation-request-1.md).

If Workplace Reservation Management is unable to find a new workplace, date, and time, relevant messages are shown to the user so that the conflicted reservation can be manually resolved by selecting a different workplace item or by changing the time of the reservation.

For example, if you have reserved a workplace item for a meeting that occurs every Wednesday for one month. Four reservation records are created for each occurrence. But if another employee reserved that same room for the same time as one of your recurring reservations, then your reservation occurrence will conflict with the other employee's reservation. In such a case, you can modify your reservation for that day by selecting a different meeting room or time.

## Reservation states

After you make a reservation, the state of the reservation changes to **Confirmed**.

If the reservation requires approvals, its status changes depending on what your approver does. You receive email notifications of these changes. The possible changes are the following:

-   If your approver has not taken action on your reservation, the state of the request stays **Awaiting approval**.
-   If your approver approves your reservation and the availability is confirmed, the state of the reservation changes to **Confirmed**.
-   When the recurring reservations are automatically resolved, the **New Space** state is shown below the **Confirmed** state to indicate that Workplace Reservation Management has assigned a new workspace, date, or time.
-   If your approver rejects your reservation, the state of the reservation changes to **Rejected**.
-   If your approver approves your reservation but the workplace item is not available for the selected date and time, the state of the reservation changes to **Conflicted**.

    **Note:** If there are recurring conflicts, employees are expected to manually resolve the reservation conflicts by selecting a new workspace, time, and date. For more information, see [Create a reservation](../task/create-reservation-request-1.md).

-   If you're reserving a workplace item for recurring days, the reservation gets confirmed for the days and times when the item is available. For the remaining days and time, the state of the reservation remains as **Conflicted**.

    You can modify your reservation and follow up with your approver to resolve your conflicting reservation.

-   If you cancel your reservation, the state of the reservation changes to **Cancelled**.

