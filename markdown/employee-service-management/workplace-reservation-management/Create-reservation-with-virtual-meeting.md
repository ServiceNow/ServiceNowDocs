---
title: Create a reservation including a virtual meeting link
description: Enable employees who are located outside the office to join a reservation by using a virtual meeting link. A virtual meeting link is created for an employee selected in "On behalf of".
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a reservation including a virtual meeting link

Enable employees who are located outside the office to join a reservation by using a virtual meeting link. A virtual meeting link is created for an employee selected in "On behalf of".

## Before you begin

**Note:** You can create a virtual meeting link only if your administrator has enabled the virtual meeting configuration. For more information, see [Configure a reservable purpose](configure-reservable-purpose.md) and [Create a reservation](create-reservation-request-1.md).

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Navigate to the Make a Reservation page from any of the following starting points.

<table id="choicetable_oxk_tfj_zsb"><thead><tr><th align="left" id="d172693e68">

Location

</th><th align="left" id="d172693e71">

Steps

</th></tr></thead><tbody><tr><td id="d172693e77">

**From application navigator**

</td><td>

Navigate to **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

</td></tr><tr><td id="d172693e98">

**Employee Center**

</td><td>

1.  Navigate to the Employee Center \(**All** &gt; **Self-service** &gt; **Employee Center\)**\). On the home page, navigate to **Workplace** &gt; **Browse all Workplace** and select the workplace service.
2.  Open the reservation portal and do one of the following:
    -   Click **Reservations** &gt; **Make a reservation**.
    -   On the homepage, select **Make a reservation** directly.
    -   From the Workplace services catalog, select **New general reservation**.
        1.  Select **Catalog** &gt; **Browse by categories** &gt; **Workplace Services Catalog**.

**Note:** If there are multiple catalogs configured on the portal, go to the Catalogs list and select **Workplace Services Catalog**.

        2.  Select **Reservation Management** &gt; **New general reservation**.


</td></tr></tbody>
</table>    The Make a Reservation page opens in a new tab.

2.  Select the type of workplace item that you want to reserve.

    The types are displayed as tabs, such as a meeting room or desk.

3.  Select **Browse all**.

    The **Browse all** reservable path is selected by default.

    1.  Search for a workplace item that you want to reserve using the following available criteria.

4.  Click **Search**.

    The workplace items which match the search criteria and which are available for reservation are displayed.

    **Note:** While browsing near a person, if there are any private spaces, then they are not displayed in the search result.

    **Note:** You can switch between the **Card view** tab and **Schedule view** tab to review the availability of workplace items. If your company uploads floor maps, view the maps using Mappedin or Indoor Mapping. For more information on how to use floor maps, refer to [Workplace Space Mapping](../../workplace-space-mapping/concept/wsm-mappedin-admin.md).

5.  Sort the workplace items in alphabetical order or by using a filter with the **Show filter** option.

    You can also sort the workplace items to display your favorite locations first. To view the option, you must have access to the Employee Center and also have favorite locations. Your favorite locations are displayed first in an alphabetical order followed by the other locations that match the search criteria.

    **Note:** You cannot sort workplace items in alphabetical order or by your favorite locations if you are browsing spaces near a person. The spaces near a person are searched based on proximity.

6.  Select the workplace item that you want to reserve using any of the following options:

    -   Click **Add**.
    -   In the **Schedule view** tab, click **Add**.
    -   In the **Map view**, select any space that is colored green and then select **Add**.
7.  Select **Next**.

8.  On the form, fill in the fields.

<table id="table_bzj_mgj_zsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reservation subject

</td><td>

Subject of your meeting.

</td></tr><tr><td>

Make subject private

</td><td>

Option to make reservation subject as private.

</td></tr><tr><td>

Make subject private

</td><td>

Option to mark the reservation as private and to hide the reservation subject.

</td></tr><tr><td>

Add a virtual meeting link

</td><td>

Option to generate a virtual meeting link so that remote employees can join the reservation.**Note:**

-   If a virtual link is not created successfully, the reservation details page doesn't display a meeting link and this option is cleared in the reservation record. To generate a meeting link again, select this option and submit the record.
-   If you add a meeting link for Microsoft Teams, the application retrieves meeting details while synchronizing the event with a calendar provider.


</td></tr><tr><td>

This reservation is for

</td><td>

If you are requesting a reservation on someone else's behalf, select the name of that person. Leave the field empty if you are requesting a reservation for yourself.

</td></tr><tr><td>

**Add invitees to this reservation** section

</td><td>

**Note:** This section appears only if your administrator has enabled the configuration to invite attendees to this workplace location.

</td></tr><tr><td>

Invite coworkers

</td><td>

Select the employees whom you want to invite to the reservation.

</td></tr><tr><td>

Invite external visitor

</td><td>

Option to invite an external visitor.**Note:** This option appears only if you have the Workplace Visitor Management application installed.

 -   If you have already registered the visitor before, do the following:
    1.  Select **Previous visitor**.
    2.  In the **Select a prior visitor** field, select the visitor.

You can also preview the visitor details and modify if required. The details are updated automatically in all the visitor-related records and registration records.

-   If you are registering the visitor for the first time, do the following:
    1.  Select **Add new visitor**.
    2.  Select the **Visitor type**.
    3.  If the visitor is a special guest, enable **VIP**.
    4.  Enter the **First name** of the visitor.
    5.  Enter the **Last name** of the visitor.
    6.  Specify the **Email Address** of the visitor to send registration details and communications.
    7.  Enter the **Phone number** of the visitor.
    8.  Enter the **Organization** details of the visitor.
    9.  Enter the **Title** of the visitor.
    10. In the **Private notes** section, specify any private information.
    11. In the **Visitor preferences** and **Notification preferences** fields, select the visitor's preferences.
    12. Click **Save and add** to add the visitor.


</td></tr><tr><td>

Add extra services

</td><td>

Extra services available with the reservation.

</td></tr></tbody>
</table>9.  Click **Submit reservation**.


## Result

The reservation is created with a virtual meeting link. If you have invited attendees to the reservation, the meeting link is provided to them along with the reservation details.

To view the reservation recording, go to Reservation summary of the reservation and select **Additional details**. If passcode is configured for virtual meeting provider, then, in the **Additional details**, you can also view the relevant passcode. Only the organizer and the user specified in the **This reservation is for** field can view the passcode.

-   Zoom: If a Zoom meeting link is added, the link appears in the **Location** field of the email containing the meeting invite.
-   Microsoft Teams: When a reservation is created with a virtual meeting link, the application retrieves the meeting link and the joining-related details. When this reservation is synchronized with Microsoft Outlook calendar, the meeting link and the joining-related details are added to the body of the calendar event. Similarly, when a reservation is created in the Microsoft Outlook calendar using the **Teams meeting** toggle button, the meeting link is retrieved and saved as a virtual meeting link.

    **Note:** As the meeting link appears in the body of the email, in any case, if you want to update or change the meeting details, you must do it only using the Workplace Reservation Management. Because when a reservation synchronization is performed, the details \(in this case, the meeting link and details\) are synchronized only in one way, that is, from Workplace Reservation Management to the calendar provider\(in this case Microsoft Teams\). If you already made any changes to the meeting details or the notes from the calendar provider, it is overwritten by Workplace Reservation Management when a synchronization is performed.

-   **Any other virtual meeting providers**: The meeting link is added in the **Location** field of the email containing the meeting invite.

**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Create a reservation](create-reservation-request-1.md)

[Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md)

[Auto-resolve recurring reservations](recurring-reservations.md)

[Set a location as favorite using the Space details page](set-a-location-as-favorite.md)

[Reserve a space near your colleague](browse-near-person-rsv.md)

[Create a multi-day reservation](create-multi-day-reservation.md)

[Create multi-building reservations](create-multi-building-reservation.md)

[Create neighborhood reservations](create-neighborhood-reservations.md)

[Create reservation for multiple workplace items](create-reservation-for-multiple-wrkplceitems-1.md)

[Enable shift-based reservation](enable-shift-based-reservation.md)

[Create a reservation along with a shared reservation](create-rsv-along-with-shared-rsv.md)

[Create a shift reservation](create-a-shift-reservation.md)

[Create a group reservation](create-group-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

