---
title: Working with schedule view
description: You can check any reservations created in your workplace and also make changes using the schedule view of the event planner.
locale: en-US
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Working with Event planner, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Working with schedule view

You can check any reservations created in your workplace and also make changes using the schedule view of the event planner.

## Before you begin

Ensure that you have installed the Calendar component \(sn\_calendar\) of version 23.2.0 or later.

**Important:** Reservations created using a calendar provider can only be managed using the calendar provider.

Role required: sn\_wsd\_rsv.reservation\_planner or sn\_wsd\_rsv.reservation\_viewer

## About this task

Using the Event planner Schedule view, do the following:

-   You can only manage reservations created using the Workplace Reservation Management applications.
-   Manage single and multi-day reservations.
-   You can manage or update a reservation only by opening a reservation on the reservation portal page and not using the Schedule view.

You can view reservations created in any campus, building, or floor of your organization using the schedule view. The schedule view provides a clear calendar-based view of the reservations and the reserved spaces. It displays all the reservations created on a space for a single day or a week \(multi-day\) depending on the reservation timeline.

-   You can filter reservations by space types and locations.
-   View reservations requested for present and past dates.
-   View current day's reservations requested for a selected building.
-   As a reservation or space planner, do the following:
    -   Drag a reservation to another space for a selected campus and building. Update date and time as required.
    -   Cancel a reservation.
    -   Open an existing reservation on the reservation portal. Update the reservation start date and end date, time, or location on the Workplace Reservation Management portal.

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  On the left pane, select the **Event planner** icon \(![Event planner icon.](../images/event-planner-icon.png)\).

    The Event Planner dashboard opens.

3.  Select **Open schedule view**.

    A schedule view opens displaying all the locations of your organization. If your had already applied a location filter on the schedule view in the past, the filter is retained and the locations are displayed accordingly.

4.  To search for a space directly, specify the space name in the **Search spaces** search bar on the top left.

5.  Select a date to view the reservation details.

6.  To view reservations for a date and time, do the following:

    The calendar displays the time based on the time zone of the selected campus.

    1.  Select the **Date**.

        The date field is displayed directly with the current date selection.

    2.  On the calendar, select the date that you want to view.

        You can change the month and year if necessary.

    3.  Select **OK**.

    The reservations created for a selected date are shown.

7.  Select a **Campus** from the Schedule view menu.

8.  Select a **Building** and **Floor**.

    By default, all the buildings and floors are displayed. From the building and floor drop-down list, deselect any buildings or floor that you don't require.

9.  To filter the spaces based on their reservable purpose, select the **Reservable puposes** option and make a selection.

    If a reservable purpose is not selected, then all the spaces including the ones that do not have any reservable purpose are displayed.

    The spaces that match the selected purpose are displayed.

10. To change the time line of the calendar, use the time line option.

    By default, the calendar is set to a 30-minute view, that is, the **Day view 30 minutes** option is selected.

11. To view reservation details, do the following:

    1.  Select a reservation.

        The reservation details \(start date and end date, time, reservation duration, type of reservation and current state is displayed.

    2.  To view and update the reservation details, select the Open side panel icon \(![Open side panel icon.](../images/evnt-plnnr-opensidepanelicon.png)\).

    3.  To open the reservation on the portal and view more details, select **Open reservation**.

12. Udpate a reservation to another date, time, or location.

    **Note:** You can perform this action only if you are a Reservation planner.

    1.  Select a reservation.

    2.  Drag the reservation to a desired time

        **Note:** You cannot move the reservation to another date. You can only change the timings.

        **Important:** Using the schedule view, you cannot edit a multi-child or a group-child reservation that is created using a calendar provider.

    3.  On the Confirm reservation changes window, review the changes to be implemented and select either **No, Cancel** or **Yes, Update**.

        **Note:** If there are any extra service requests with the reservation, you will have to request them again after you move the reservations. When you move a reservation, the extra services are not moved.

13. To move the reservation to another location on a building or floor, do the following:

    **Note:** You can perform this action only if you are a Reservation planner.

    1.  Select the reservation.

    2.  Drag the reservation to the desired location.

    3.  On the Confirm reservation changes window, read the changes that will be implemented and select either **No, Cancel** or **Yes, Update**.

        **Important:** If there are any extra service requests with the reservation, you will have to request them again after you move the reservations.

        -   After you move the reservation, you must request the extra services again. When you move a reservation, the extra services are not moved as the services vary for different locations.
        -   If you are moving a reservation requested by an employee, a notification is sent to the employee to confirm the action.
        -   To change the reservation and keep the services, edit the reservation first.
14. To create a reservation on the selected campus, select **Create new reservation**.

    For more information on how to make a reservation, refer to [Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).


-   **[Allow Event planners to handle reservations with more flexibility](../concept/event-planner-bypass-validation-rule-overview.md)**  
Reservation planners can bypass or overrule certain settings in the Reservable module while moving a reservation to another location in the Event planner Scheduled View.
-   **[Move reservations between Reservable modules using the Schedule view](evnt-planner-scheduled-view-move-rsv.md)**  
Reservation or space planners can move or update reservation between Reservable modules. Planners with sn\_wsd\_rsv.bypass\_module\_validation role can bypass the Reservable module configuration settings.

**Parent Topic:**[Working with Event planner](../concept/working-with-event-planner.md)

