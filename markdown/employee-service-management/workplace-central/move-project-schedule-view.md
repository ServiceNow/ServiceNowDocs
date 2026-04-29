---
title: Move project views, actions, and states
description: As a move manager, create, track, and work on move projects to fulfill multiple move requests at a time. The move project enables you to work using a schedule view, which is faster than opening individual move requests.
locale: en-US
release: australia
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2026-03-25"
reading_time_minutes: 5
breadcrumb: [Move management key features and actions, Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Move project views, actions, and states

As a move manager, create, track, and work on move projects to fulfill multiple move requests at a time. The move project enables you to work using a schedule view, which is faster than opening individual move requests.

A Move project enables you to logically group move requests based on the specified conditions. You can view all the move requests under a single move project.

Using the Move project's Schedule view, you can:

-   Verify the user who raised the move request.
-   View the current state of that move request.
-   View and edit the expected start and due date by when the request must be fulfilled. The dates are displayed on a calendar.
-   Check the number of move requests to be fulfilled every day.
-   Schedule a move request to another date by simply dragging the bar of the request.

![Move scheduler view of a move project.](../images/move-scheduler.png "Move scheduler view of a move project")

## Move dates

The following process explains how the start and end dates of a move project are determined:

1.  An employee or a move manager raises a move request. They specify a date in the **Requested move date** field.
2.  When the move requests are collated in the Move Management workspace, they’re displayed with the **Requested move date**, **Expected start**, and **Due date**.
3.  The planned start and end date of the move project are set based on the minimum **Expected start** date and the maximum **Due date** from the move requests that are associated with the project.

## Move project views

When you select a move project to work, it’s opened in a separate tab. It’s opened in the schedule view by default. You can edit and view the move project details in different views.

-   **Schedule**

    The default view when you open a move project. The schedule view is an interactive calendar view with displayed according to your local time zone. You can also switch to a list view using the list options tab \(![List options.](../images/list-options.png)\).

    The view is categorized based on the following:

    -   **Move requests**: The first column displays the move request details such as the name of the requester, move request number, and its current state.
    -   **Calendar**: The main display of the view contains the event details in a calendar view sorted across a set of dates. The minimum planned start date is the first date of the calendar and the maximum planned end date is the end date of the calendar.
        -   Each calendar day is displayed with the number of move cases that are expected to be fulfilled.
        -   The calendar displays the move request as a bar on the calendar. To schedule the move request on a different day, drag the bar to the required date on the calendar.
        -   The calendar displays the dates based on your current local date. It displays the date and time based on your time zone.
        -   If a move request doesn’t have any **Expected start** or **Due date** specified, then the calendar doesn’t display any bar for the request.
        -   You can switch between a weekly view and a monthly view. By default, the calendar is displayed in a weekly view.
        -   When you select a move request bar on the calendar, a Case details panel is displayed. You can view case details like the **To location**, **Expected start**, **Due date**, **State**, and **Request for**.
    -   **List**: You can change your view from a calendar view to list view using the List options tab \( ![List options.](../images/list-options.png)\). View all the move requests under the move project as a list.
        -   You can view the details of the request like the request number, state, relevant dates, and the move project.
        -   You can remove a single or multiple move requests by selecting them from them list.
        -   You can also assign one or more move requests to yourself by using the **Edit** option.
-   **Move project details**

    The Move project details tab contains details such as the name of the project, the move manager who is assigned to the project and the state of the project.

    -   You can change the state of the project that is assigned to you.
    -   You can reassign the project to yourself by changing the **Assigned to** field.
    -   You can track the activities such as state changes and user assignment changes performed on the project in the Activity section.
    -   You can add work notes in the project using the Compose section. You can enter your names and select **Post Work notes \(Private\)**.
-   **Attachments**

    You can view any attachments in the **Attachments** section.


## Add move requests

At any time, you can add more move requests to a move project while the project is still in the Work in progress state. Select the **Add new requests** to add move requests. You can add multiple move requests to a project.

## Move project states

A move project goes through the following state changes:

-   **Initializing**

    When the move project is created while deploying a scenario, the state is set to **Initializing**. This state is set when a move project is created and the move requests are still being created under it.

-   **Ready**

    When a move project is ready with all the move requests that matched the conditions, the state of the project is set to **Ready**.

-   **Work in progress**

    When you start working on the project, you can set the state to **Work in progress**.

-   **Closed complete**

    After you fulfilled all the move requests of the move project, you can change the state to **Closed complete**. You can set it to **Closed complete** only if all the move requests that are assigned to the project are set as **Inactive**.

    A project that is in the **Closed complete** state can't be edited. You can only edit the **Assigned to** and the **State** fields.

-   **Closed incomplete**

    If you want to close a move project for some reasons irrespective of the status if the move requests assigned to it, you can change the state to **Closed incomplete**. Changing the state of the project doesn’t impact the state of the move requests assigned to the project.

    A project that is in the **Closed incomplete** state can't be edited. You can only edit the **Assigned to** and the **State** fields.

-   **Cancelled**

    You can cancel a move project at any time by changing the state to **Cancelled**. Changing the state of the project doesn't impact the state of the move requests assigned to the project.

    A project that is in the **Cancelled** state can't be edited. You can only edit the **Assigned to** and the **State** fields.


**Parent Topic:**[Move management key features and actions](move-mgmt-views-states-actions.md)

