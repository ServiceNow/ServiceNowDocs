---
title: Add invitees as collaborators and create a reservation
description: Employee can add their colleagues as collaborators while making a reservation. Employees can view availability of their colleagues on the reservation portal search page while making a reservation to find an available space.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Add invitees as collaborators and create a reservation

Employee can add their colleagues as collaborators while making a reservation. Employees can view availability of their colleagues on the reservation portal search page while making a reservation to find an available space.

## Before you begin

The option to add invitees or colleagues as collaborator is available on the Make a reservation portal page. The option to add guests is available on the Reservation details page once you have selected an available space for reservation.

Workplace Reservation Management should be integrated with Microsoft Exchange Online. The **Find Meeting Times** Spoke and **Lookup Schedules** Spoke action in Microsoft Exchange Online is used to view the availability of invitees. The application retrieves free, busy, out of office, and other availability status for selected attendees. Application suggests alternative meeting times and available spaces when there's a conflict or when the selected employees are unavailable.

For more information about setting up Microsoft Azure portal configuration, see [Set up Microsoft Exchange](https://www.servicenow.com/docs/r/yokohama/integrate-applications/integration-hub/setup-ms-exch-ol.html?contentId=R1EDI02PGW_yQSiS3EQ1ow). To set up the Find Meeting Times and Lookup Schedules spoke actions for Microsoft Exchange Online, see [Microsoft Exchange Online Spoke Action](https://www.servicenow.com/docs/r/xanadu/integrate-applications/integration-hub/ms-exch-online-spoke.html).

-   Microsoft Exchange Online integration is enabled with Workplace Reservation Management with availability of Spoke action 'Find Meeting Times'.
-   Ensure the Reservable Module property **Allow attendees-based search** option is enabled by your administrator. This property is available when you've installed and configured Workplace Calendar Synchronization. For more information, see [Configure Workplace Calendar Synchronization](../../workplace-calendar-synchronization/concept/configure-rsv-sync.md)
-   The sys\_user table must be populated with valid user data. Employees can select attendees for their event from the sys\_user table.
-   Valid user email Id should be configured in Microsoft Exchange Online. When email Id is missing or not configured, the status of an employee is shown as unknown in the add attendee list.
-   Workplace Calendar Synchronization should be installed and configured.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Self-service** &gt; **Employee Center** &gt; **Workplace Services** &gt; **Browse Workplace Services** &gt; **New General Reservation**.

2.  Reserve a workplace location and add attendees as collaborators.

    On the form, fill in the fields.

    ![Make a reservation form.](../image/make-reservation-page-add-invitees.png)

<table id="table_nxh_43v_j3c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select a Reservable Module \(Example, Desks, Meeting rooms, and so on\)**Note:** Allow attendee-based search is not supported for shift-based Reservable Module configuration. For more information, see [Configure a reservable module](config-reservable-module.md).

Google Calendar and Microsoft On premises are not supported for you to add colleagues as collaborators in a reservation.

</td></tr><tr><td>

Where

</td><td>

Select a reservable path \(Example: Browse all, Browse near a person, and so on\).

</td></tr><tr><td>

Building

</td><td>

Select a building where you want to make the reservation.

</td></tr><tr><td>

Floor

</td><td>

Select a floor.

</td></tr><tr><td>

When

</td><td>

Select the meeting duration. The meeting duration is shown based on your building time zone. For example, Europe/Amsterdam timezone.The start date and end date is dependent on the on Max days in future value. If Max days in future module configuration value is 6, you cannot reserve a location beyond this duration. /Max number of occurrences. Employees cannot select a date beyond the range specified in these Reservable Module configuration. For more information, see [Configure a reservable module](config-reservable-module.md).

</td></tr><tr><td>

From

</td><td>

Select the start date and time.

</td></tr><tr><td>

To

</td><td>

Select the end date and time.

</td></tr><tr><td>

Recurring

</td><td>

Select the required recurring event option from the drop-down list. For example, Daily, Weekly, Monthly, Custom and so on. For more information, see [Create a reservation](create-reservation-request-1.md).**Note:** Recurring event scheduling is dependent on the **Max number of Occurrences** and **Max days in future** Reservable Module property value. You cannot select recurring occurrences beyond the value specified in the **Max number of Occurrences** Reservable module property value.

In case of recurring reservations \(Daily, Weekly, Monthly, or Custom\), time suggestions for selected attendees are shown only for a single day \(24-hour\) duration. For Weekly, time suggestion for the first occurrence in a series is shown. For Daily and monthly recurring reservations, time suggestion for the first occurrence is shown.

</td></tr></tbody>
</table>3.  Select **Add invitees**.

    In the The Add invitees and find availability dialog box appears. It shows the host calendar availability at first. If you are making a reservation and adding invitees, you are shown as the host. You can search for attendees that you want to add to your meeting for collaboration. You can search by your colleagues name or email address to find their availability. You can add as many invitees to your meeting as your collaborators. The attendees list is fetched from Microsoft Exchange Online based on the collaborator or invitees calendar events. When you search for attendees, the attendees availability is also shown as Suggestions.

    **Note:** Application supports adding guests to reservations on the Reservation Details page after you have selected a space for reserving. For guests, application doesn't retrieve the colleagues' availability for them on the reservation portal search page.

    An attendee's availability on the Add Attendees dialog box is shown using Microsoft Exchange Online calendar events color scheme. Out of office calendar event displays purple or white dot against the selected employee name. A new date and time is suggested by the application for a duration when the attendee is available in office. Employees can view suggested reservation options and select any one. If attendees user mail ID is not configured with Microsoft Exchange Online, unknown user \(null or no color\) is shown against their availability status.

    When creating or viewing an event, the "Show As" setting in Microsoft Exchange Online determines how your time appears to others:

    -   Busy \(Solid Bar/Color\): You are unavailable; others cannot book this time.
    -   Tentative \(Diagonal Striped Bar\): You have a tentative appointment, but might be free.
    -   Free \(White/Transparent Bar\): You are available, even if a calendar item is present.
    -   Away \(purple or yellow/Specific Indicator\): You are away from your desk.
    -   Working Elsewhere \(Dashed/Different Color\): You are working, but not in your usual location.
    -   Solid Green Dot: Available.
    -   Solid Red Dot: Busy, in a call, or in a meeting.
    -   Red Dot with Horizontal Line: Do not disturb.
    -   Yellow Dot with Clock: Away or Be right back.
    -   White, pink dot or arrow in Purple: Often appears for Out of Office events or shared calendar items.
    **Note:** These colors and icons may vary slightly between classic Microsoft Outlook, New Microsoft Outlook, and Microsoft Outlook on the web, but "Show As" meanings \(Busy/Free/Tentative\) remain consistent.

    ![Unknown user shown by a null or empty color in the Add Availability dialog box.](../image/add-invitees-unknown-user-email-not-config.png)

4.  In the Add invitees and find availability dialog box, select attendees or collaborators that you want to add to your meeting.

    ![Add invitees and find availability dialog box.](../image/add-invitees-dialog-box-select.png)

    The application adds attendees to your meeting and syncs the attendees calendar event to your calendar.

    When the application is unable to fetch attendees availability, it shows a message. “Unable to load availability. Availability cannot be loaded. You can continue with your reservation”.

    ![Add invitees dialog box showing unavailability of selected attendees.](../image/add-invitees-message-availability-cannot-be-loaded.png)

    **Note:** If you change the start and end date, the list is refreshed.

    Employees can select event attendees, and the application checks their availability for a selected date and time.

    -   Employees can view the availability of attendees or an attendee. Application recommends available spaces based on attendee’s availability.
    -   If there are conflicts, application suggests a space with optimal availability. Application suggests alternative meeting options based on selected attendees’ availability for a date and time duration.
    -   Adding guests to reservations is supported but the application doesn't retrieve availability for them on the reservation portal search page.
5.  From Suggestions panel, select a date and time of your choice.

    Suggestions are displayed based on your selected start date and end time and the duration of your meeting. For example, if you select 2 hours as the duration of your meeting, suggestions are displayed based on two-hour time duration. For example, if you select your meeting start time as 12 pm, suggestions are displayed from 12 pm onwards.

    If you add multiple attendees or invitees, the users are displayed in horizontal sequence or series. At a time, five attendees names are displayed. If there are more than five attendees, expand the plus option to view additional attendees.

    ![Add multiple invitees to your meeting for collaboration. Remove attendees as required.](../image/rsv-add-invitees-plus-number.png)

    You can remove an attendee by selecting the remove option icon \(![Remove icon.](../image/remove-invitee-icon.png)\).

    **Note:** Availability for selected attendees is shown for 24-hour duration only. If you select a duration beyond this, the application shows "Availability is checked for the first 24-hours only". Suggestions are shown only for 24-hour duration for attendees availability. Microsoft Exchange Online's **Find Meeting Times** spoke action doesn't return attendees' availability for more than 24-hours.

    For recurring reservations, application shows availability based on the first occurrence, and doesn't calculate the availability based on all occurrences or a sub-set of it. For Weekly, time suggestion for the first occurrence in a series is shown. For Daily and monthly recurring reservations, time suggestion for the first occurrence is shown.

    ![Availability for attendees in the Suggestions panel are shown only for 24-hour duration.](../image/rsv-attendees-availability-24hrs-only.png)

    Select **More Suggestions** to load additional suggestions. At a time, the maximum number of suggestions up to 7 days are displayed or shown at a time. This is dependent on the **Max days in future** Reservable Module configuration property. If your Max days in future value is 5, you get suggestions for 5 days only.

    ![Message showing max number of suggestions that can be loaded at a time.](../image/rsv-attendees-max-number-suggestions-message.png)

6.  Select **Confirm**.

    Upon confirmation, application adds the attendees as invitees before synchronizing the event to the calendar. The **Manage Invitees** option appears on the reservation page after you confirm and add invitees to your meeting.

    If the application is unable to load invitee’s availability, it shows **Continue** instead of **Confirm**. Select **Continue** to move forward with your reservation.

    The invitees or attendees are added to your meeting. You can add additional invitees to your meeting using the **Manage Invitees** option. You can also remove invitees as required.

7.  Select **Search**.

    Search results page shows available spaces for selected location, date, and time.

8.  Select **Add** to add space or spaces to your reservation.

9.  Select **Next**.

    The Reservation details page appears. On the Reservation details page, you can add visitors or guests.

10. Complete the required information on the Reservation details page.

    For more information, see [Create a reservation](create-reservation-request-1.md).

11. Select Invite Attendees to add external visitors or guests.

    Review the number attendees or invitees added to your reservation.

12. Add or remove workplace services as required.

13. Edit or update your reservation or workplace services as required.

    For more information, see [View or update reservations](view-reservations.md)

14. Select **Submit** to create a reservation and add invitees as collaborators to your reservation.

15. Review the Reservation summary page.

    ![Reservation summary page showing internal and external attendees that are added to a reservation.](../image/rsv-summary-page-showing-attendees-added.png)

    The Reservation summary page displays the invitees or attendees that are added to your reservation. The internal invitees \(attendees\) column that you've added shows Microsoft Exchange Online user mail IDs. External visitors' column show their personal mail IDs.


**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Create a reservation](create-reservation-request-1.md)

[Auto-resolve recurring reservations](recurring-reservations.md)

[Reserve a space near your colleague](browse-near-person-rsv.md)

[Create neighborhood reservations](create-neighborhood-reservations.md)

[Create multi-building reservations](create-multi-building-reservation.md)

[Create a multi-day reservation](create-multi-day-reservation.md)

[Create reservation for multiple workplace items](create-reservation-for-multiple-wrkplceitems-1.md)

[Create a reservation along with a shared reservation](create-rsv-along-with-shared-rsv.md)

[Set a location as favorite using the Space details page](set-a-location-as-favorite.md)

[Create a reservation including a virtual meeting link](Create-reservation-with-virtual-meeting.md)

[Create a shift reservation](create-a-shift-reservation.md)

[Create a group reservation](create-group-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

