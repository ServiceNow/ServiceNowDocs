---
title: Set a location as favorite using the Space details page
description: Mark your most reserved workplace location as favorite in the Workplace Service Portal. Once the location is set as favorite, it is displayed first whenever you search for locations to make a reservation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/set-a-location-as-favorite.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Set a location as favorite using the Space details page

Mark your most reserved workplace location as favorite in the Workplace Service Portal. Once the location is set as favorite, it is displayed first whenever you search for locations to make a reservation.

## Before you begin

**Important:** The favorite option appears only if you have access to the Employee Center and if your administrator has enabled the favorite option.

Role required: sn\_wsd\_core.workplace\_user

## About this task

You can set a location as favorite from any one of the following locations in the Workplace Service Portal:

-   **Quick Reservation widget**
-   **Make a reservation**

After you set a workplace location as your favorite, you can directly reserve that location from the My favorites page on the Employee Center.

**Note:** For more information about the derivation logic used by Workplace Reservation Management on the Space details page to assign reservable modules, see [Reservable module derivation logic for Space details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/reservation-logic-for-myfavorites-space-details.md).

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  From the top right menu, select the favorite icon \(\[Omitted image "favorite-icon.png"\] Alt text: Favorite icon.\).

    My favorites page is displayed.

3.  Select a space to view the space details page.

    For example: **Desk A1.0501**.

4.  On the **Check Availability** section, select the start date, time, and end date.

    \[Omitted image "wsd-emp-center-dates-new-changes-use.png"\] Alt text: Make reservations using the Employee Center space details page.

    If the **Max days for multi-day** Reservable Module property value is set and is greater than 1, employees can reserve a space for multiple days. Default value of **Max days for multi-day** property is 1. For example, if **Max days for multi-day** value is set to 10 days from the current date, then, only the next available 10 days are available for you to select and make a reservation. Other dates are disabled and are not available for selection.

5.  Select **Search**.

6.  In the **Card view**, **Schedule view** or **Map view** In the Card view, Schedule view or Map view, Mark a location as favorite by clicking the favorite icon \(\[Omitted image "favorite-icon.png"\] Alt text: Favorite icon to mark a location.\)

7.  The **Schedule view** in case of multi-day reservation displays available spaces in a day view.

    -   Clicking the chevron will take you to the next day and previous day.
    -   Three-hour blocks are used to show the time scale in a 24-hour format.
    -   In case of a single day reservation, one-hour blocks are used to show the time scale for a day.
8.  The calendar shows the available time lines when the reservable modules can be reserved.

9.  Map view shows the selected workplace spaces on a map, if maps are enabled by your organization.

    If employees have a permanent assignment in their workplace profile, the employee names are displayed on the map for a selected space. For more information, see [Display permanent seat assignments on floor maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/display-permanent-seats-on-maps.md).

10. Select **Reserve**.

11. Review the Reservation details page.

    For more information about Reservation details page, see [Create a reservation]()

12. Submit your Reservation.

13. Sort the workplace items to display your favorite locations using the **My favorites first** sort option.

    1.  By default, if you have favorite locations, the default sort option is set to **My favorites first**.

        The workplace items are then sorted and all your favorite locations are displayed first in an alphabetical order followed by the other workplace items that match the search criteria.

    2.  If you are browsing for a workplace location near a person, you can sort the workplace items to display your favorite locations first using the **My favorites first** sort option.

        The favorite locations are displayed based on the closest proximity with the person's location.

14. To remove a location from the favorites list, deselect the favorite icon in the location details.

15. On the Reservation Portal, you can view and perform the following actions after you set a location as favorite:

    1.  After your perform the search operation, you can sort the workplace items to display your favorite locations at first using the **My favorites first** sort option. By default, if you have favorite locations, the default sort option is set to **My favorites first**.

        The workplace items are then sorted and all your favorite locations are displayed first in an alphabetical order followed by the other workplace items that match the search criteria.

    2.  If you are browsing for a workplace location near a person, you can sort the workplace items to display your favorite locations first using the **My favorites first** sort option.

        The favorite locations are displayed based on the closest proximity with the person's location.

    3.  If you are creating a recurring reservation, you can see the recurring availability within the series of the space on the space details page.
16. To remove a location from the favorites list, deselect the favorite icon in the location details.

17. On the Reservation Portal, you can view and perform the following actions after you set a location as favorite:

    1.  After your perform the search operation, you can sort the workplace items to display your favorite locations at first using the My favorites first sort option.

        By default, if you have favorite locations, the default sort option is set to **My favorites first**. The workplace items are then sorted and all your favorite locations are displayed first in an alphabetical order followed by the other workplace items that match the search criteria.

    2.  If you are browsing for a workplace location near a person, you can sort the workplace items to display your favorite locations first using the My favorites first sort option.

        The favorite locations are displayed based on the closest proximity with the person's location.

18. In the Workplace Service Portal Quick Reservation widget, after you specify the search criteria, the most suitable location is displayed based on your favorite location.

    -   If there is any favorite location that best matches the search criteria, the Quick Reservation widget displays that location as the best match.
    -   You can also set a best match workplace location as favorite directly from the Quick Reservation widget.
19. If you want to reserve a space using a shared reservation, after you click **Reserve a space for me**, the application automatically reserves one of your favorite locations that has closest proximity with the space reserved in the shared reservation details.


## Result

The location is added to your favorites list.

**Parent Topic:**[Reserve workplace items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/reserve-workplace-items.md)

**Related topics**  


[Create a reservation]()

[Add invitees as collaborators and create a reservation]()

[Auto-resolve recurring reservations]()

[Reserve a space near your colleague]()

[Create a multi-day reservation]()

[Create multi-building reservations]()

[Create neighborhood reservations]()

[Create reservation for multiple workplace items]()

[Enable shift-based reservation]()

[Create a reservation along with a shared reservation]()

[Create a reservation including a virtual meeting link]()

[Create a shift reservation]()

[Create a group reservation]()

[Share, modify, or cancel a reservation]()

[Reserve a workplace using the Quick Reservation widget]()

[Download an iCalendar for a reservation]()

