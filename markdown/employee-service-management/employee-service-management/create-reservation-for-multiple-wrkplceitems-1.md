---
title: Create reservation for multiple workplace items
description: Reserve multiple workplace items for the same date and time in a single reservation.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
---

# Create reservation for multiple workplace items

Reserve multiple workplace items for the same date and time in a single reservation.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user

## About this task

Reserve multiple workplace items at the same time, either for yourself or on behalf of others.

Before booking a room or desk, check the availability of the selected item using the Schedule view. Review the standard services that are available with the workplace items.

**Note:** As an admin or reservation manager, you cannot edit a reservation opened manually using a URL.

## Procedure

1.  Navigate to the Make a Reservation page from any of the following starting points.

<table><thead><tr><th align="left" id="d323481e60">

Location

</th><th align="left" id="d323481e63">

Steps

</th></tr></thead><tbody><tr><td id="d323481e69">

**From application navigator**

</td><td>

Navigate to **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

</td></tr><tr><td id="d323481e90">

**From Employee Center Portal**

</td><td>

-   Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
-   On the Employee Center portal, select **Workplace Services** &gt; **Browse Workplace Services**.
-   Select the **New general reservation** card.

Make a reservation portal page opens for you to make workplace reservations.

</td></tr><tr><td id="d323481e137">

**From Workplace Service Portal**

</td><td>

1.  Navigate to **Workplace Core** &gt; **Workplace service portal** &gt; **Workplace Service Portal Home**.

**Note:** You can also raise a request from the Employee Center. On the home page, navigate to **Workplace** &gt; **Browse all Workplace** and select the workplace service.

2.  Open the reservation portal and do one of the following:
    -   Click **Reservations** &gt; **Make a reservation**.
    -   Select **Make a reservation** on the homepage directly.
    -   Select **New general reservation** from the Workplace services catalog.
        1.  Select **Catalog** &gt; **Browse by categories** &gt; **Workplace Services Catalog**.

**Note:** If there are multiple catalogs configured on the portal, go to the Catalogs list and select **Workplace Services Catalog**.

        2.  Select **Reservation Management** &gt; **New general reservation**.


</td></tr></tbody>
</table>    The Make a Reservation page opens in a new tab.

2.  Select a Reservable Module configuration such as **Desks**, **Meeting rooms** **Desks within an area** and so on.

    For more information how to configure a Reservable module, see [Configure a reservable module](config-reservable-module.md).

3.  Select **Search**.

    The available workplace items which match the search criteria appear.

    **Note:** While browsing near a person, if there are any private spaces, then they are not displayed in the search result.

    **Note:** You can switch between **Card view** tab and **Schedule view** tab to review the availability of workplace items. If your organization uses indoor map providers like Indoor Mapping or Mappedin, use the **Map view** to provide interactive locations and wayfinding to workplaces. Indoor Mapping is inbuilt map provider with WSD while Mappedin is a third-party map provider that is integrated with WSD. DXF maps are not supported.

4.  Sort the workplace items in alphabetical order or by using a filter with the **Show filter** option.

    You can also sort the workplace items to display your favorite locations first. To view the option, you must have access to the Employee Center and also have favorite locations. Your favorite locations are displayed first in an alphabetical order followed by the other locations that match the search criteria.

5.  Select the workplace item that you want to reserve using any of the following options.

    -   Click **Add**.
    -   If you have selected the **Schedule view** tab, click **Add**.
    -   If you have selected the **Map view** tab, select any space that is colored green and click **Add**.
6.  Select **Next**.

7.  On the form, fill in the fields.

<table id="table_rjr_5lp_zlb"><thead><tr><th>

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

Option to mark the subject of the reservation as private.

</td></tr><tr><td>

Reserve these items together for the same person

</td><td>

Select this option to reserve all the workplaces for the same user.

</td></tr><tr><td>

This reservation is for

</td><td>

If you are requesting a reservation on someone else's behalf, select the name of that person. Leave this field empty if you are requesting a reservation for yourself.

</td></tr><tr><td>

Number of attendees

</td><td>

Number of people expected to attend the meeting.

</td></tr><tr><td colspan="2">

**Add invitees to this reservation** **Note:** This section appears only if your administrator has enabled the configuration to invite attendees to this workplace location. This option will not appear if the **Number of attendees** option is displayed.

</td></tr><tr><td>

Invite coworkers

</td><td>

Select the employees whom you want to invite to the reservation.

</td></tr><tr><td>

Invite external visitor

</td><td>

Option to invite external visitor.**Note:** This option appears only if you have Workplace Visitor Management application installed.

 -   If you have already registered the visitor before, do the following:
    1.  Select **Previous visitor**.
    2.  In the **Select a prior visitor** field, select the visitor.

You can also preview the visitor details and modify any details if required. The details are updated automatically in all the visitor-related records and registration records.

-   If you are registering the visitor for the first time, do the following:
    1.  Select **Add new visitor**.
    2.  Select the **Visitor type**.
    3.  If the is a special guest, enable **VIP**.
    4.  Enter the **First name** of the visitor.
    5.  Enter the **Last name** of the visitor.
    6.  Specify the **Email Address** of the visitor to send registration details and communications.
    7.  Enter the **Phone number** of the visitor.
    8.  Enter the **Organization** details of the visitor.
    9.  Enter the **Title** of the visitor.
    10. Specify any private information in the **Private notes** section.
    11. Select their preferences in the **Visitor preferences** and **Notification preferences**.
    12. Click **Save and add** to add the visitor.


</td></tr><tr><td>

Sensitivity

</td><td>

Nature of your meeting. Select **Private** if you want to hold a confidential meeting.**Note:** When you mark a meeting as **Private**, the **Reservation subject** becomes hidden for other people and is displayed as **\*\* private \*\***. Only you or the person for whom you have requested this meeting can see the subject.

</td></tr></tbody>
</table>8.  Click **Submit reservation**.


## Result

If the items do not require any approval, the selected workplace items are reserved. The status of the request is updated to Confirmed.

If any of the items needs approval, then your request is submitted to the approver. The status of the request is updated to Awaiting approval.

## What to do next

-   To view, edit or cancel your reservations, see [Share, modify, or cancel a reservation](modify-cancel-res-request.md).
-   To view, add or remove any invitees from the reservation, do the following:
    1.  On the Reservation summary page, select the **Invitees** tab.
    2.  To change the location of any invitees, do the following:
        1.  Select the check box next to the invitee.
        2.  Select **Actions** &gt; **Assign to**.

            You can also select the actions icon \(![Action icon](../image/actions-invitees-icon.png)\) next to the invitee details.

        3.  In the **New location assignment** field, select the location where you want to move the invitee.
        4.  Click **Send update**.

            An email is sent to the invitees about the reservation changes.

    3.  To add or remove an invitee, do the following:

        1.  On the Reservation summary page, select **Actions** &gt; **Change reservation details**.
        2.  In the Reservation details page, go to the **Add invitees to this reservation** section.
        3.  To add an invitee, select the invitee name from the search list.
        4.  To remove an invitee, click the remove icon \(![Remove icon](../image/remove-invitee-icon.png)\) near the invitee name.
        5.  Click **Update reservation details**.
        If you have added an invitee, an email is sent to the invitee with the reservation details. If you have removed an invitee, an email is sent that the reservation is canceled.


**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Create a reservation](create-reservation-request-1.md)

[Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md)

[Auto-resolve recurring reservations](recurring-reservations.md)

[Reserve a space near your colleague](browse-near-person-rsv.md)

[Create neighborhood reservations](create-neighborhood-reservations.md)

[Create multi-building reservations](create-multi-building-reservation.md)

[Create a multi-day reservation](create-multi-day-reservation.md)

[Create a reservation along with a shared reservation](create-rsv-along-with-shared-rsv.md)

[Set a location as favorite using the Space details page](set-a-location-as-favorite.md)

[Create a reservation including a virtual meeting link](Create-reservation-with-virtual-meeting.md)

[Create a shift reservation](create-a-shift-reservation.md)

[Create a group reservation](create-group-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

