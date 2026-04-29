---
title: Workplace Central Event planner
description: The Workplace Central Event planner is a one-stop workspace where you can check all the reservations requested in your organization at a time.
locale: en-US
release: australia
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2026-03-25"
reading_time_minutes: 12
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Workplace Central Event planner

The Workplace Central Event planner is a one-stop workspace where you can check all the reservations requested in your organization at a time.

## Event planner capabilities

You can view all the reservations of your organization in this single workspace, and monitor how many workplace locations are engaged by employees. Using the planner, you can perform the following actions:

-   Access the event planner as a Reservation planner and a Reservation viewer.
-   Set the start and end time displaying on the calendar in the schedule view.
-   View various reservations such as single, recurring occurrences, multi-child, group, and more.
-   Check the available and unavailable spaces at any time.
-   Directly view or edit reservations requested in any campus, building, or a floor when required.
-   Open and View Location directory using Event planner.
-   View the planner in a Scheduled view. Open Location directory from the Scheduled view.
-   Change a reservation to an earlier or later date or time.
-   View detailed information of each reservation requested either in the past, on the current day or that are upcoming.
-   View details such as the requester, the current state of the reservation, the check-in and check-out status, the invitees, the number of people attending and more.
-   Create a reservation.
-   As a reservation planner, you can perform the following actions:
    -   Drag a reservation to another date and time to reschedule.
    -   Drag and drop a reservation with service items to another time or another location. The service items can't be modified but the quantity of the service items can be modified.

        **Note:** If the new location or time does not have one or more added services, then a message is displayed informing ''This change will result in the loss of one or more services for this reservation''.

    -   Change the reservation timings.
    -   Change the location of the reservation.
    -   Cancel a reservation.

        **Note:** Only selected reservation occurrence is deleted when a recurring reservation is cancelled, and not the complete recurrence series. You can cancel the complete recurring reservation from the portal.

    -   Open a reservation and make advanced changes and also add services.
    -   Edit the reservation from the contextual side panel of the calendar. This functionality is available only for single and recurring reservations.

        **Note:** When you modify a building value in an existing reservation, because the previous location is not available in the updated building, selecting it throws an error. You can select a different location.

-   As a reservation planner, you can manage single or occurrence reservation details. You can also edit reservation details such as the reservable purpose, number of attendees and cost center from the details reservation details pages directly.

    **Note:** You can manage a multi-location or a group reservation only by opening the reservation details and not with the schedule view.


**Important:** Reservations created using a calendar provider can only be managed using the calendar provider.

## Landing page

The Event planner landing page consists of the following sections:

-   **Reservations**

    The metrics of the reservations are displayed in the section. The metrics of the current day's planned reservation, requested extra services, canceled reservations, and pending approval reservations.

-   **Active reservations**

    This section displays the detailed list of all the reservations requested in the organization and the reservations requested by you. You can also view the reservations in a schedule view using the **Open schedule view** option.


## Reservation metrics

On the Event planner landing page, you can view the reservation metrics in the **Reservations** section. The following metric cards are displayed. You can select the metric card to view the respective reservations in a list.

-   **Planned reservations for today**

    Number of reservations scheduled for the current day \(today\).

-   **Reservations with extra services for today**

    Number of reservations that have extra service requests for the current day \(today\).

-   **Canceled reservations of today**

    Number of reservations that have been canceled for the current day \(today\).

-   **Pending approval reservations**

    Number of reservations that are awaiting approval.


## Reservations list view

The **Active reservations** section on the landing page displays a list of reservations. You can view all the reservations and reservations requested by you. The **Active reservations** section displays the following:

-   **All Reservations**

    The **All Reservations** section displays the list of reservations created in throughout your organization. The list displays ten reservations at a time. Select the **View all** option to view all the reservations. You can view the following details:

    -   The reservations requester.
    -   The location on which the reservation is created.
    -   The building and campus where the location resides.
    -   The reservation purpose.
    -   The reservation types such as single, occurrence, multi-child, group, and others.
    -   The start and end time of the reservation.
    -   The current state of the reservation.
    You can refresh the list whenever required. You can also edit the columns of the list based on how you want to view the list.

-   **My reservations**

    The **My reservations** section displays the list of reservations that you have created either for yourself or for others. The list displays 10 reservations at a time. Select the **View all** option to view all the reservations.

    You can refresh the list whenever required. You can also edit the columns of the list based on how you want to view the list. You can configure to display up to 10 columns at a time.


## Reservations schedule view

The event planner enables you to view all the reservations in a schedule view using the **Open schedule view**.

The schedule view opens a time-line view displaying all the workplace locations of your organization such as campuses, buildings, floors, and spaces on that floor. The schedule view has the following capabilities:

-   **Campus selection**

    On the top right of the schedule view, you can specify the campus for which you want to view the reservations using the **Campus** option. After you specify the campus, the **Buildings** and **Floors** filters are automatically generated. You can specify the building and the flood that you want to view respectively. As an admin, you can configure the number of campuses that must be displayed in the drop-down selection. You can specify the number in the **Maximum number of items that can appear in filter drop down of campus, buildings and floors in Event Planner Experience.** property.

    After you specify your campus, the selection is retained and is displayed by default when you open the schedule view next time.

-   **Reservable purpose**

    You can use the **Reservable purpose** option to filter the spaces of the campus based on the reservable purposes configured in your organization.

-   **Date**

    You can view the reservations of any date by selecting a date on the calendar. You can select **Today** to view the current day on the calendar.

-   **Timezone**

    The schedule view time line is set based on the time zone of the selected location.

-   **Time frame**

    You can specify the time frame of the schedule view using the drop-down location on the top-right corner of the view. By default, the time frame is set as **Day view 30 minutes**. You can choose to view the time in a one hour window or a week view.

-   **Event Planner Schedule**

    You can set the start and end time that displays on the calendar in the schedule view from the system properties**Start time Event Planner Schedule**,and **End time Event Planner Schedule**.

-   **Snap duration**

    When you drag and drop a reservation, you select and move the reservation by some duration and the duration is called Snap Duration.

    The default snap duration for a 30-minute and 60-minute view of the event planner schedule view is 5 and 15 minutes, respectively. The minimum and maximum values to set a snap duration for a 30-minute view is 1 and 30, and for a 60-minute view is 1 and 60. You can modify the default values using the system properties **Snap duration for 30 min view of Workplace Event Planner Schedule View** and **Snap duration for 60 min view of Workplace Event Planner Schedule View**.

-   **Schedule view properties**

    Configure the **sn\_wsd\_rsv.row\_title\_fields\_event\_planner\_schedule** system property to specify comma separated field names from space table to display in Row title in Schedule view.

    Configure the **sn\_wsd\_rsv.event\_body\_fields\_event\_planner\_schedule** system property to specify comma separated field names from reservation table to display on Reservation event in Schedule view.

    Configure the **sn\_wsd\_rsv.additional\_space\_details\_fields** system property to specify comma separated field names from space table to display on Space details side panel in Schedule view.

-   **Refresh**

    You can refresh the view at any time by selecting the Refresh option.

-   **Legend**

    You can view the color legend based on which the reservations are displayed. The legend displays the colors associated with each state. As an admin, you can modify the colors associated with each state in Workplace Reservation Management properties. Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Properties** to modify the properties. You can edit the following properties and specify your colors:

    -   Color for Draft reservations in Event Planner Experience
    -   Color for In progress reservations in Event Planner Experience.
    -   Color for Awaiting confirmation reservations in Event Planner Experience.
    -   Color for Confirmed reservations in Event Planner Experience.
    -   Color for Completed reservations in Event Planner Experience.
    -   Color for Awaiting approval reservations in Event Planner Experience.
    -   Color for Approved reservations in Event Planner Experience.
    -   Color for Rejected reservations in Event Planner Experience.
    -   Color for Conflicted reservations in Event Planner Experience.
    -   Color for Read only reservations in Event Planner Experience.
    Specify the hex code for the color.

-   **Search spaces**

    You can directly search for a space using the **Search spaces** option.

-   **Reservations**

    The reservations created on a space are displayed as a bar expanded between start and end time. The reservations are displayed in colors based on their current state. You can view the color legend to know the state.

    You can select the reservation to view details such as the reservation start and end time, duration, subtype, status, and services requested if there are any.

    -   You can also view further details of the reservations on the side panel by selecting the Open side panel icon \(![Open side panel icon.](../images/evnt-plnnr-opensidepanelicon.png)\).
    -   To open the reservation and view it on the portal, you can select the **Open reservation** option. The reservation is displayed in Employee Center by default. If you want the reservation to open on a custom portal instead of Employee Center, you must perform the following actions:
        1.  Navigate to **System Definitions** &gt; **Script includes**.
        2.  Search and open **WPCoreUtils**.
        3.  In the **Script** field, override `getCommonPortalSuffix` function to get the common portal suffix.
        4.  Click **Update**.
    -   You can also select the Show \(![Show icon.](../images/evnt-plnnr-showrsvdetails-icon.png)\) icon to get a detailed view of the reservation. The side panel displays the reservation-related details such as the location, start and end time, current state, synchronization state, reservation subject and services requested. As a reservation planner, you can also cancel the reservation using the **Cancel reservation** option.
    -   You can also move the reservation to another time or to another location by dragging the bar of the reservation.
-   **Last updated sub source**
    -   When a reservation is updated from the Contextual side panel, the last updated sub source is updated as **Workplace Event Planner**.
    -   When a reservation is updated from the portal, then the last updated sub source is updated as **Workplace Service Delivery**.

## Reservation details view

When you select a reservation in the event planner, the reservation opens in a new tab displaying all the reservation-related details. The page displays the requester details, the current state, and the campus where the reservation is requested on the top-level view.

The reservation details are displayed in the following tabs:

-   **Details**

    The **Details** tab displays the reservation details specified by the requester on the reservation form while making the reservation. As a reservation planner, you can edit the **Number of attendees**, **Reservable purpose** and the **Cost center** field.

-   **Blocker Reservations**

    The tab displays blocker reservations created along with the reservation. Blocker reservations are created for cleanup and preparation if any extra services are requested with the reservation.

-   **Cases**

    The tab displays the workplace cases created to fulfill the extra services requested with the reservation. If there are any workplace tasks created, a **Tasks** tab appears.

-   **Requested Service Items**

    The tab displays the service items requested with the reservation.

-   **Approvers**

    The tab displays the details of the approvers of the reservation.

-   **Invitees**

    The tab displays the details of the invitees invited to the reservation.

-   **Reservation Recordings**

    The tab displays the recording details if the reservation includes a virtual meeting link.


From the reservation details page, you can also open the reservation to view it in the Employee Center portal using the **Open reservation** option. If you want the reservation to open on a custom portal instead of Employee Center, you must perform the following actions:

1.  Navigate to **System Definitions** &gt; **Script includes**.
2.  Search and open **WPCoreUtils**.
3.  In the **Script** field, override `getCommonPortalSuffix` function to get the common portal suffix.
4.  Click **Update**.

As a reservation planner, you can cancel a reservation if necessary using the **Cancel reservation** option.

**Parent Topic:**[Workplace Central reference](../concept/workplace-central-references.md)

**Related topics**  


[Components installed with Workplace Central](components-installed-with-workplace-central.md)

[Space Optimization - Key features and actions](space-optmization-features-and-actions-.md)

[Scenario and Building - Views, states, settings, and key features](scenario-planning-views-actions-keyfeatures-.md)

[Space request approvals, states, actions, and key features](space-request-states-and-view.md)

[Move management key features and actions](move-mgmt-views-states-actions.md)

[Case Management - Key features, Actions &amp; Case details](case-management-key-features-actions-case-details.md)

[Schedule Plan details form](schedule-plan-details-form.md)

[Scenario details form](scenario-details-form.md)

[Space Deployment Plan](space-deployment-plan.md)

[User Deployment Plan](user-deployment-plan.md)

[Excel column lengths for move projects](move-excel-char-limit.md)

[Move conflicts for projects created via Excel upload](excel-upload-conflicts.md)

[Workplace Central troubleshooting](workplace-central-troubleshooting.md)

[Workplace Task form - Space Assignment task](workplace-task-space-assignment.md)

[Neighborhood User Assignment Rule form](user-assignment-rule-form.md)

[User Workplace Profile form](user-workplace-profile-form.md)

