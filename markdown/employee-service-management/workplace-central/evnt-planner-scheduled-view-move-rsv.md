---
title: Move reservations between Reservable modules using the Schedule view
description: Reservation or space planners can move or update reservation between Reservable modules. Planners with sn\_wsd\_rsv.bypass\_module\_validation role can bypass the Reservable module configuration settings.
locale: en-US
release: xanadu
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2024-12-20"
reading_time_minutes: 7
breadcrumb: [Working with schedule view, Working with Event planner, Use Workplace Central, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Move reservations between Reservable modules using the Schedule view

Reservation or space planners can move or update reservation between Reservable modules. Planners with sn\_wsd\_rsv.bypass\_module\_validation role can bypass the Reservable module configuration settings.

## Before you begin

Make sure that you have installed the following applications:

-   Workplace Core
-   Workplace Central
-   Workplace Reservation Management
-   Workplace Case Management

Role required: sn\_wsd\_rsv.reservation\_planner

## About this task

As a reservation or space planner, you can perform the following actions:

-   Create a reservation from the Event Planner Scheduled view page.
-   Drag and move a reservation to another location, date, and time.
-   Change or update the reservation location, start and end dates, and time.
-   Open a reservation from the Scheduled view page to update a reservation on the Workplace Reservation Management reservation portal page and add services to it.

## Procedure

1.  Navigate to **All** &gt; **Workplace central** &gt; **Workplace Central**.

    You can also open Workplace Central from Employee Center directly. Navigate to **All** &gt; **Self-service** &gt; **Employee Center** &gt; **Workspaces** &gt; **Workplace Central**.

2.  Select the Event Planner icon \(![Event planner icon to open the Event planner home page.](../images/event-planner-icon.png)\).

3.  Select **Open Scheduled view**.

    Schedule view page opens. If you have already applied a location filter on the schedule view in the past, the filter is retained and the locations are displayed accordingly.

4.  To search for reservations requested for a campus, building, or a floor, do the following:

    1.  Select a **Campus** from the menu.

        The **Building** and **Floor** fields are automatically populated. By default, all the buildings and floors are displayed. The spaces in a campus are displayed based on the building and floor where it’s located. Select a building, floor as required. You can clear or uncheck the buildings and floors that are selected by default in the drop-down list.

        Space or reservation planners can change the Reservable module to a different Reservable module while moving or updating a reservation. Planners can search for spaces and select a new location.

    2.  To view a reservation for a specific date, do the following:

        ![Scheduled view page showing Date picker to select date to verify reservations.](../images/wsd-event-planner-scheduled-view-page.png)

    1.  Select the date from the Date picker for which you want to view a reservation.

        For example, December 24, 2024.

    2.  Change the month or year as required.

    3.  Select **OK**.

    The reservations available for a selected date are displayed.

5.  Select **Space type** to filter reservable locations based on space types.

    For example, Gym, elevator, Meeting rooms, Desks/Meeting rooms, and so on.

    Scheduled view displays only spaces of the selected type.

6.  To create a reservation, select the **Create new Reservation** button from the Scheduled view menu.

    The Make a reservation page opens on the reservation portal.

    **Note:** Adding multiple spaces to a reservation isn’t supported in Event Planner. Select only a single space while creating a reservation.

    For more information, see [Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).

    While creating a reservation, space or reservation planners can bypass the start date or end date restrictions configured in the Reservable module:

    -   Max days in the future

        For multi-day reservations, planners can select a time span exceeding the Reservable module configuration. For example, If Max days in future vale is 90, space planners can make a reservation exceeding the 90-day limit.

        **Note:** When synchronizing a reservation with the Microsoft Exchange Server, reservation dates too far in the future are rejected.

    -   Recurring

        For recurring reservation, planners can select a date past the **Max number of occurrences** value set in the Reservable module configuration.

7.  To move the reservation from one Reservable module to another or within the same Reservable module, do the following:

    **Note:** Only one space or location can be selected while moving or updating a reservation from one location to another.

    1.  Select the reservation that you want to update.

    2.  Drag and move or drop the reservation to the desired location or space.

        For example: Select a reservation in Demo campus, First floor from Room B1-02 and move it to Room B2-02.

        **Note:** You can move a reservation from one location to another locations within the same Reservable module or it can be moved to a space or location with a different Reservable module. Workplace services added to a reservation remains intact when the services are available on the new space.

    3.  The confirm reservation changes dialog box opens.

        ![The Confirmation reservation changes dialog box showing options to select Reservable modules.](../images/wsd-move-rsv-confirmation-window.png)

    4.  Select the Reservable module to where you want to move your reservation.

        The list displays all the available Reservable modules to which the selected space or location belongs.

        While updating the reservation certain roles and limitations are ignored or bypassed for reservation or space planners \(sn\_wsd\_rsv.reservation\_planner\) having the \(sn\_wsd\_rsv.bypass\_module\_validation\) role.

        -   If a selected location or space is available in multiple Reservable modules, reservation or space planners can select the Reservable module from while updating a reservation. If a space is part of multiple Reservable modules, available Reservable modules are displayed in the list for selection. The Reservable modules are sorted alphabetically.

            **Note:** If the space is part of multiple Reservable modules, one of the eligible Reservable modules is preselected based on the space details algorithm. For example, if space Dublin is part of Reservable Module Desks and you want to move it to space Eureka which is also part of the same Reservable module \(Desks\), then Desks is preselected based on the space details logic. If you’re moving a space to a location which is part of two different reservable modules then one of the Reservable modules is preselected based on the space details algorithm. For example, if you’re moving Eureka to B1.003, and B1.003 is part of two Reservable modules \(**Desks** and **Desks within an area**\), one of these Reservable module is preselected based on the space details algorithm.

        -   If the space is part of multiple Reservable modules including the current module from which the event planner is moving a reservation to a different location, the current module is preselected. The reservation or space planner can select a new module from the list of presented modules as required.

        -   If a space is part of a single Reservable module, only that Reservable module is available for selection while updating a reservation from one location to another. The confirm Reservation changes dialog box doesn't show the drop-down list with multiple reservable modules and only one reservable module is shown for selection.
        **Note:** If the selected space has no Reservable module, moving or updating a reservation to a new location isn’t allowed. A message is displayed, "The target space has no module associated.”

    5.  Select **Yes, update** to confirm your selection.

8.  Select an existing shift-based reservation from the Scheduled view.

    1.  Select a reservation from a location and move or drag it to a desired location.

        The confirm reservation changes dialog box opens.

        ![Confirm reservation changes dialog box showing a shift-based Reservable module.](../images/wsd-moving-shift-based-rsv.png)

    2.  Select a Reservable module to which you want to move the selected reservation and space.

        While moving a shift-based reservation, the shift-based Reservable module of which the space is part of is preselected.

        **Note:** You can move a location within the same shift-based reservation and not to a different shift-based reservation. Two different shifts aren’t available for selection in the confirm reservation changes dialog box when you try to move a reservation. Space planners can move a shift-based reservation to a non-shift Reservable module \(Desks, meeting rooms, and so on\). For example: **Desks within a Shift** Reservable module can be moved to **Desks** Reservable Module. For more information, see [Allow Event planners to handle reservations with more flexibility](../concept/event-planner-bypass-validation-rule-overview.md).

9.  Select the Show reservation details icon \(![Reservation details icon.](../images/wsd-show-reservation-details-icon.png)\) to open the Reservation details side-panel context window.

    ![Reservation details window showing a selected reservation details.](../images/wsd-evnt-planner-update-rsv-window.png)

    1.  Select and select a reservation to open the reservation details information window.

        1.  Select **Open Reservation**. Your reservation opens in a new browser tab on the Employee Central portal page.
        2.  Select the **Actions** tab and select **Change Reservation details** to update the reservation.

    2.  Select an existing reservation on the Scheduled view to open and update the reservation using the contextual side panel.

        Update the following field information:

        ![Update reservation contextual side-panel window to modify location, date, and time for a reservation.](../images/wsd-scheduled-page-view.png)

        -   Floor
        -   Building
        -   Location
        -   Start Date
        -   End Date
        -   Requested for
        -   Reservation subject
        -   Additional message
        For more information, see [Create a reservation](../../wsd-reservation-management/task/create-reservation-request-1.md).

    3.  After making the required changes, select **Update reservation**.

        The **Update reservation** button is activated when you edit or update changes in the Reservation details contextual-side panel.

        Follow Step 7 to Step 8 as required.


**Parent Topic:**[Working with schedule view](working-with-schedule-view.md)

