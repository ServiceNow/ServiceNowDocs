---
title: Working with schedule view
description: You can check any reservations created in your workplace and also make changes using the schedule view of the event planner.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Working with Event planner, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Working with schedule view

You can check any reservations created in your workplace and also make changes using the schedule view of the event planner.

## Before you begin

Ensure that you have installed the Calendar component \(sn\_calendar\) of version 23.2.0 or later.

**Important:** Reservations created using a calendar provider can only be managed using the calendar provider.

Role required: sn\_wsd\_rsv.reservation\_planner or sn\_wsd\_rsv.reservation\_viewer

## About this task

Using the Event planner schedule view, you can perform various actions on reservation. However, note the following:

-   You can only manage reservations that are created using Workplace Core applications.
-   You can manage single and occurrence reservations.
-   You can manage a multi-location or a group reservation only by opening the reservation details and not with the schedule view.

You can view reservations created in any campus, building, or floor of your organization using the schedule view. The schedule view provides a clear calendar-based view of the reservations and the reserved room. The calendar displays all the reservations created on a space for the entire day or week depending on the time-line that you selected.

-   You can filter the locations based on their reservable purposes and check the reservations requested on them.
-   View reservations requested on any date, including past dates.
-   View the status of reservations. The statuses are displayed in different based on their state.
-   View the time line based on 30-minutes interval, hourly interval or a weekly view.
-   View reservation details.
-   View current day's reservations requested on the selected building.
-   Search for spaces based by the space's title, reservation host, and subject of the reservation.
-   As a planner, you can perform the following actions:
    -   Drag a reservation to another date and time to reschedule.
    -   Change the reservation timings,
    -   Change the location of the reservation.
    -   Cancel a reservation
    -   Open a reservation and make advanced changes and also add services

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  On the left pane, select the **Event planner** icon \(![Event planner icon.](../images/event-planner-icon.png)\).

    The Event Planner dashboard opens.

3.  Select **Open schedule view**.

    A schedule view opens displaying all the locations of your organization. If your had already applied a location filter on the schedule view in the past, the filter is retained and the locations are displayed accordingly.

4.  To search for a space directly, specify the space name in the **Search spaces** search bar on the top left.

5.  To search for reservations requested on a campus, building, or a floor, do the following:

    1.  On the top-right corner, select the **Campus** drop-down and select the campus.

        The **Building** and **Floor** fields are automatically populated. By default, all the buildings and floors are displayed.

        The spaces of the campus are displayed based on the building and floor where it’s located.

    2.  To exclude any building or floor, you can expand the drop-down and deselect.

    The spaces are displayed based on your selection. You can scroll to the right to view the timeline and scroll downwards to view the locations.

6.  To filter the spaces based on their reservable purpose, select the **Reservable puposes** option and make a selection.

    If a reservable purpose is not selected, then all the spaces including the ones that do not have any reservable purpose are displayed.

    The spaces that match the selected purpose are displayed.

7.  To view reservations requested on a different date, do the following:

    The calendar displays the time based on the time zone of the selected campus.

    1.  Select the date drop-down.

        The date field is displayed directly with the current date selection.

    2.  On the calendar, select the date that you want to view.

        You can change the month and year if necessary.

    3.  Select **OK**.

    The reservations created on the selected date are displayed.

8.  To change the time line of the calendar, use the time line option.

    By default, the calendar is set to a 30-minute view, that is, the **Day view 30 minutes** option is selected.

9.  To understand the status of the reservation, that is, to know the state of the reservation by its color, select the **Legends** \(![Legends icon.](../images/evnt-plnnr-legend-icon.png)\) option.

10. To view the details of the reservation, do the following:

    1.  Select the reservation.

        The reservation details such as the start and end time, total duration, type of reservation and current state is displayed.

    2.  To view the reservation details on the side panel, select the Open side panel icon \(![Open side panel icon.](../images/evnt-plnnr-opensidepanelicon.png)\).

    3.  To open the reservation on the portal and view more details, select **Open reservation**.

11. To move the reservation to another time, do the following:

    **Note:** You can perform this action only if you are a Reservation planner.

    1.  Select the reservation.

    2.  Drag the reservation to the desired time.

        **Note:** You cannot move the reservation to another date. You can only change the timings.

        **Important:** Using the schedule view, you cannot edit a multi-child or a group-child reservation that is created using a calendar provider.

    3.  On the Confirm reservation changes window, review the changes to be implemented and select either **No, Cancel** or **Yes, Update**.

        **Note:** If there are any extra service requests with the reservation, you will have to request them again after you move the reservations. When you move a reservation, the extra services are not moved.

12. To move the reservation to another location on the building, do the following:

    **Note:** You can perform this action only if you are a Reservation planner.

    1.  Select the reservation.

    2.  Drag the reservation to the desired location.

    3.  On the Confirm reservation changes window, read the changes that will be implemented and select either **No, Cancel** or **Yes, Update**.

        **Important:** If there are any extra service requests with the reservation, you will have to request them again after you move the reservations.

        -   After you move the reservation, you must request the extra services again. When you move a reservation, the extra services are not moved as the services vary for different locations.
        -   If you are moving a reservation requested by an employee, a notification is sent to the employee to confirm the action.
        -   To change the reservation and keep the services, edit the reservation first.
13. To create a reservation on the selected campus, select **Create new reservation**.

    For more information on how to make a reservation, refer to [Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).


-   **[Allow Event planners to handle reservations with more flexibility](../concept/event-planner-bypass-validation-rule-overview.md)**  
Reservation planners can bypass or overrule certain settings in the Reservable module while moving a reservation to another location in the Event planner Scheduled View.
-   **[Move reservations between Reservable modules using the Schedule view](evnt-planner-scheduled-view-move-rsv.md)**  
Reservation or space planners can move or update reservation between Reservable modules. Planners with sn\_wsd\_rsv.bypass\_module\_validation role can bypass the Reservable module configuration settings.

**Parent Topic:**[Working with Event planner](../concept/working-with-event-planner.md)

