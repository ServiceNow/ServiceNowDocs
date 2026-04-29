---
title: Create a group reservation
description: Reserve multiple spaces for different users in a single group reservation.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a group reservation

Reserve multiple spaces for different users in a single group reservation.

## Before you begin

**Note:** Workplace users can make a group reservation only if the Reservable Module configuration property **Allow group reservation** is set by your workplace administrator. Make sure that the **Allow invitees** property is unchecked in the Reservation Widget Configuration. You cannot add or invite attendees to a group reservation. For more information, see [Configure a reservable module](config-reservable-module.md).

Role required: sn\_wsd\_core.workplace\_user

## About this task

Reserve multiple spaces at a time for different employees in a single group reservation. After you submit the reservation, the reservations are created individually for each employee along with a parent reservation. You can view all the individual reservations in a single parent reservation and modify any details if required.

For example, if you are reserving four workplaces for four different employees. After you submit the reservation, a total of five reservations are created. The fifth reservation is the parent reservation where you can see all the child reservation details and update these reservations as required.

## Procedure

1.  Navigate to the Make a Reservation page from any of the following starting points.

<table id="choicetable_ewc_11d_vrb"><thead><tr><th align="left" id="d525327e73">

Location

</th><th align="left" id="d525327e76">

Steps

</th></tr></thead><tbody><tr><td id="d525327e82">

**From application navigator search context menu**

</td><td>

Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

</td></tr><tr><td id="d525327e106">

**Employee Center**

</td><td>

1.  Navigate to Employee Center \(**All** &gt; **Self-service** &gt; **Employee Center\)**\). On the home page, navigate to **Workplace Services** &gt; **Browse all Workplace Services**.
2.  Select **New general Reservation**.


</td></tr></tbody>
</table>    The Make a Reservation page opens in a new tab.

2.  Select a Reservable module.

    By default, the **Desks** reservable module is selected.

3.  Select a Reservable Path.

    By default, **Browse All** Reservable path is selected.

    -   **Campus**: Option to select a campus.
    -   **Building**: Option to select a building where you want to make the reservation.
    -   **Start date**: Option to enter the start date for your reservation.
    -   Time: Option to select the start time for your reservation. The time is displayed based on the selected building's time zone.
    -   **End date**: Option to enter the end date for your reservation.
    -   Time: Option to select the end time for your reservation.
    -   All day: Option to create an all day reservation.
    -   **Recurring**: Option to create a recurring reservation on a recurring basis. Select this field and specify the number of days and the number of times that you want to repeat the reservation. For weekly reservations, select the days of the week for reservation.
4.  Select **Search**.

    The available workplace items that match the search criteria appear.

    **Note:** You can select a space using **Card view**, **Map view** or **Schedule view**.

    Map view displays workspace on a floor map. Make sure that you have configured Indoor Mapping as your map provider.

5.  Select the workplace item that you want to reserve using any of the following options.

    -   Select **Add**.

        Select multiple spaces as required for the group reservation. For example, if there's a group with five workspace users, you can add five spaces for a selected campus or location.

6.  Select **Next** to reserve the selected spaces.

7.  On the form, specify the reservation details.

    1.  In the **Reservation subject**, the reservation name or subject is auto-populated.

        Change or modify the reservation subject, as required.

    2.  To enable privacy for a selected workspace, check the **Mark space details private** check box.

    3.  Clear the **Reserve these items together for the same person** option.

        **Note:** When the **Reserve these items together for the same person** is unchecked, the **This reservation is for** option is not displayed on the Reservation details page since this is a group reservation. The space cannot be reserved for a single workplace user.

    Selected spaces in a campus are displayed.

8.  From a campus, select a workplace user from **This reservation is for** drop-down list.

    Provide a workplace user name for whom you are creating this reservation. Repeat this step for all the spaces displayed for a campus.

9.  Click **Submit reservation**.


## Result

The group reservation is created. You can view the reservation details on the Reservation summary page.

-   Individual reservations are created for each user. Users can view the reservation details in their own My reservations page. They cannot edit or cancel the reservation.

    **Note:** You cannot share the details of a group reservation from the parent reservation directly. Instead, you can share the individual reservations that are created from the group reservation.

-   To edit a reservation, open the parent reservation and click **Actions** &gt; **Change reservation details**. After making the changes, click **Update reservation details**.

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

[Create a reservation including a virtual meeting link](Create-reservation-with-virtual-meeting.md)

[Create a shift reservation](create-a-shift-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

