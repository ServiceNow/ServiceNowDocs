---
title: Reserve a space near your colleague
description: Make a workplace reservation and reserve a space near your team member or a colleague.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Reserve a space near your colleague

Make a workplace reservation and reserve a space near your team member or a colleague.

## Before you begin

Role required: admin

## Procedure

1.  Select any of the following context menu navigation options to make a workplace reservation and reserve a space near your preferred colleague or a team member.

<table id="choicetable_prt_yr3_smb"><thead><tr><th align="left" id="d728917e59">

Location

</th><th align="left" id="d728917e62">

Steps

</th></tr></thead><tbody><tr><td id="d728917e68">

**Application navigation filter**

</td><td>

Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

</td></tr><tr><td id="d728917e92">

**From Employee Center Portal**

</td><td>

-   Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
-   On the Employee Center portal, select **Workplace Services** &gt; **Browse Workplace Services**.
-   Select the **New general reservation** card.

Make a reservation portal page opens for you to make workplace reservations.

-   Another way to make reservation is to use chat icon. On the home page, select the chat icon \(![Chat icon.](../image/chat-icon.png)\). To make a reservation, enter your question or select **Show Me Everything** to select from the list of available options.

</td></tr></tbody>
</table>    The Make a Reservation page opens in a new tab.

2.  Select a Reservable Module configuration.

    For example, select any of the following Reservable Module configuraiton. For more information, see [Configure a reservable module](config-reservable-module.md).

    -   Desks
    -   Desks with an Area
    -   Meeting rooms require approval
    -   Meeting rooms
    -   Desks with a shift
3.  Select **Browse near a person** to search for available spaces near a colleague or team member.

    **Note:** This option appears only if the **Enable browse near a person** Reservable Module property is enabled. For more information, see [Configure a reservable module](config-reservable-module.md).

    The **Max number of days for browse near a person** Reservable Module property can be configured to reserve a space near a colleague for a maximum number of days. The default value of this property is 7. The **Browse near a person** is displayed only when the **Enable browse near a person** option is selected on the Reservable Module. The system counts **Max number of days for browse near a person** from the current date \(day 1\). Here, seven days includes current date \(day 1\) and the next six available calendar days.

    **Note:** When browsing near a person, if there are any private spaces, the private spaces aren’t displayed in the reservation search result.

    If a cost center or department is enabled for a user profile's location, only those spaces or desks that have the same cost center or department as profile locations are displayed. Only spaces or desks that are assigned as flexible or none are displayed. The search results doesn't display permanent spaces or desks.

    All required fields must be filled in on the form when you’re creating a reservation and when the auto-search option is enabled by your administrator. The auto-search option doesn't work if the required field inputs are missing on the reservation page.

    ![Browse near a person reservable path selected with inputs provided in the Browse near a person form fields.](../image/wsd-browse-near-a-person-rsv.png)

    1.  **Who would you like to sit near?**: Select the user or colleague that you want to reserve a space nearby.

    2.  Specify the following details to search for the most suitable space near a colleague or team member.

        **Note:** You can’t create a Recurring reservation if you're making a reservation near a team member or colleague.

        -   **Select one of their reservation dates**: Reservation dates to make a reservation.

            **Note:** In case, if your colleague has a workplace profile, all dates \(date range\) specified in the **Max number of days for browse near a person** are displayed. In case, if there’s no workplace profile, only the available reservation dates, if applicable, are shown for a colleague or team member. After selecting the dates, you can reserve available spaces. Spaces with privacy enabled \(Private\) spaces aren’t available for selection.

            The dates are visible, based on the following considerations:

            -   Maximum days specified in the **Max number of days for browse near a person** Reservable Module property. For more information, see [Configure a reservable module](config-reservable-module.md).
            -   Start date and End date: If a multi-day reservation is enabled, you can select a date in the range of a colleague's multi day reservation when making a reservation.

                For example, if **Max days for multi-day** is 10 and you try to make a reservation for 15 days, the application shows a validation error. You’re only allowed to make a reservation for the next 10 days from the current date.

                For more information, see [Create a multi-day reservation](create-multi-day-reservation.md)

        -   **Select one of their reserved spaces**: Option to show dedicated spaces and reserved spaces that aren’t marked as private for a colleague or team member with a workplace profile. In case, if the selected user or colleague doesn’t have a workplace profile, only the available reserved spaces \(if applicable\) are displayed.

            **Note:** If a colleague has a permanently assigned space and has also had a reservation for the same day or has multiple reservations, you can select either of these spaces to make a reservation near their colleague.

        -   **From**: Reservation start date. The time is displayed based on the selected building's time zone.
        -   **To**: Reservation end date. The time is displayed based on the selected building's time zone.
        -   **All day**: Select this option to reserve the workplace item for an entire day. The start date and time of the reservation depends on the date and time set by your organization. This option appears if your Workplace administrator has enabled the **All day** reservation setting for a selected workplace location.
        -   For a multi-day reservation, the **From** and **To** fields show the date range specified for a multi-day reservation.

4.  Select **Search** to select available spaces from the Card View, Map View, or Scheduled view.

    **Note:** You can’t sort workplace items in alphabetical order or by your favorite locations if you're browsing spaces near a person. The spaces near a person are searched based on proximity.

5.  Select Add to add a space.

6.  Select **Next** to proceed with reserving the selected space.

7.  Review the Reservation details.

8.  Add workplace services as required.

9.  Select **Submit Reservation**.


**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Create a reservation](create-reservation-request-1.md)

[Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md)

[Auto-resolve recurring reservations](recurring-reservations.md)

[Set a location as favorite using the Space details page](set-a-location-as-favorite.md)

[Create a multi-day reservation](create-multi-day-reservation.md)

[Create multi-building reservations](create-multi-building-reservation.md)

[Create neighborhood reservations](create-neighborhood-reservations.md)

[Create reservation for multiple workplace items](create-reservation-for-multiple-wrkplceitems-1.md)

[Enable shift-based reservation](enable-shift-based-reservation.md)

[Create a reservation along with a shared reservation](create-rsv-along-with-shared-rsv.md)

[Create a reservation including a virtual meeting link](Create-reservation-with-virtual-meeting.md)

[Create a shift reservation](create-a-shift-reservation.md)

[Create a group reservation](create-group-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

