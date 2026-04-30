---
title: Create multi-building reservations
description: Reserve multiple spaces spanning across multiple buildings in different timezone. Create multi-building reservations for the same date and time in a single reservation.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create multi-building reservations

Reserve multiple spaces spanning across multiple buildings in different timezone. Create multi-building reservations for the same date and time in a single reservation.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user

## About this task

Reserve multiple spaces belonging to different buildings in a single reservation using the **Add another building** option on the Make a reservation page. For example, if you want to have a meeting where your colleagues are joining from different locations, you can create a single reservation with multiple locations from different time zones. Some of your colleagues may join from California while others may join from Amsterdam, and so on. Workplace Reservation Management automatically takes care of the timezone conversion based on the buildings selected and their associated timezones.

The **Allow multiple building reservations** option should be configured by your administrator to make a multi-building reservation. For more information, see [Configure a reservable module](config-reservable-module.md).

Make a multi-building reservation. 

## Procedure

1.  Navigate to **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

    Select the type of spaces that you want to reserve. The types are displayed as tabs, such as Desks, Meeting rooms, or Parking.

    You cannot make a multi-building reservation when using shifts.

2.  Provide the name of the primary or first building and the floor of the building where you want to make a reservation along with date and time.

    You must select a space for the primary building when making a multi-building reservation using the web portal.

3.  Select the **Add another building** option to add multiple buildings and spaces within a single reservation and provide the required details like Building name, floor, start date and time.

    The selected buildings can belong to different regions or locations and different time zones. The application automatically adjusts the time zones variations accordingly.

    The first building that you select is considered the primary building and the other buildings that you add after the first building are the secondary buildings. The application uses the date and time from the primary building to convert the applicable time zones for the secondary buildings.

4.  Click **Search**.

    By default, the search results first shows the primary building with spaces available in that building. Building card shows details like the building name, the campus that a building belongs to, and the number of spaces selected in a building.

    If auto-search is enabled, the search results are automatically displayed. For more information, see [Create a reservation](create-reservation-request-1.md).

5.  Switch between the **Card view** and **Schedule view** tabs to review and select the available spaces.

    In the schedule view, for a selected building, you can see the date and time as applicable.

    The bottom pane will show the number of items that you've selected from the search results.

6.  If your organization has uploaded floor maps, view the **Floor maps** using Mappedin or Indoor Mapping map providers.

7.  To revisit and update the search criteria, click **Edit search**.

    Click the remove building icon \( ![Remove building icon.](../image/remove-building-icon.png)\) to remove a building. If you remove a secondary building, the spaces associated with the building are also removed.

8.  Click **Next**.

    If you missed adding a space to a building, the application alerts to add a space. A space must always be added to a primary building. Select a building card and click **Add** to add selected spaces from the search results.

    After adding a space or room to a building, you're taken to the Reservation details page.

9.  Click **Add Services** to add room configurations or catering for selected spaces.

10. Review the reservation summary details.

11. Click **Submit Reservation**.

    **Note:** When you create a multi-building reservation using the Workplace Reservation Management application and synchronize it with the Workplace Calendar Synchronization service and later on, if you update this reservation in calendar service by removing all spaces from a primary building, then, the primary building will continue to remain as a primary building with no reserved spaces.

    This behavior is different when compared to multi-building reservations created using the Workplace Reservation Management application, as it does not allow you to proceed with the reservation if you have not selected a space in the primary building.


**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Create a reservation](create-reservation-request-1.md)

[Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md)

[Auto-resolve recurring reservations](recurring-reservations.md)

[Reserve a space near your colleague](browse-near-person-rsv.md)

[Create a multi-day reservation](create-multi-day-reservation.md)

[Create neighborhood reservations](create-neighborhood-reservations.md)

[Create reservation for multiple workplace items](create-reservation-for-multiple-wrkplceitems-1.md)

[Create a group reservation](create-group-reservation.md)

[Enable shift-based reservation](enable-shift-based-reservation.md)

[Set a location as favorite using the Space details page](set-a-location-as-favorite.md)

[Create a reservation along with a shared reservation](create-rsv-along-with-shared-rsv.md)

[Create a reservation including a virtual meeting link](Create-reservation-with-virtual-meeting.md)

[Create a shift reservation](create-a-shift-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

