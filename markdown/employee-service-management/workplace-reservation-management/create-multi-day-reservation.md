---
title: Create a multi-day reservation
description: Workplace users can now reserve a space covering multiple days. Employees can reserve a space that spans across multiple days.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 30
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a multi-day reservation

Workplace users can now reserve a space covering multiple days. Employees can reserve a space that spans across multiple days.

## Before you begin

Multi-day reservations can be made when **Max days for multi-day** Reservable Module property value is set in the Reservable module configuration. Default value of this property is set to 1. If the value for **Max days for multi-day** property is set to 1, then it will be considered a single day reservation and multi-day reservation will not be allowed. If the **Max days for multi-day** value is more than 1, the **All day** or single day reservation option is disabled on the reservation portal.

For more information, see [Configure a reservable module](config-reservable-module.md).

This property is dependent on the **Max days in future** value. If the value of **Max days for multi-day** is more than **Max days in future** Reservable Module property, application will show a validation error and will not create a multi-day reservation.

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Select any of the following context menu navigation options to make a multi-day.

<table id="choicetable_prt_yr3_smb"><thead><tr><th align="left" id="d503943e102">

Location

</th><th align="left" id="d503943e105">

Steps

</th></tr></thead><tbody><tr><td id="d503943e111">

**Application navigation filter**

</td><td>

Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

</td></tr><tr><td id="d503943e135">

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
3.  On the Make a reservation page, select any of the Reservable paths:

    The following reservation paths available for a selected Reservable Module.

    -   Browse all
    -   Browse near a person
    -   Browse by area
    -   Browse by neighborhood
    -   Browse all spaces
4.  Select **Browse all**.

    The **Browse all** reservable path is selected by default.

    1.  Search for a workplace item that you want to reserve using the following available criteria.

5.  Complete the following information.

    Fill in the form fields.

<table id="table_mn3_3gf_xdc"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Building

</td><td>

Name of the building for a selected campus. Select a building from the list. For example, Demo Campus.The building names and location names are alphabetically sorted or sorted according to the **Order** that you have configured on the Buildings and Regions tables. When a sort **Order** is configured for a building or region, the building names and locations are sorted accordingly. If the sorting **Order** value isn’t specified for an item, the items are listed on top of the list \(ascending order\), and sorted alphabetically. The building names and location names are alphabetically sorted based on the label name. For example Building A, Building B, and so on.

</td></tr><tr><td>

Floor

</td><td>

Floor of a building where you want to make a reservation.The floor names are either alphabetically sorted or the values are sorted based on the indicated sort order. You can configure the sort **Order** in the Floors table. If the sorting **Order** value is not specified for an item, then the items are listed on top of the list \(ascending order\), and then, sorted alphabetically. The Floor names are alphabetically sorted based on the names and labels.

</td></tr><tr><td>

From**Note:** The time directive fields \(From, time, To\) are also available on the MESP \(Mobile Employee Service Portal\) on the Now Mobile app.

</td><td>

Start date of your reservation.-   Employees can't select a date and create a reservation if the start date exceeds the Max days in future Reservable module value. Thisn’t value is configured on the Reservable module by your administrator. For more information, see [Configure a reservable module](config-reservable-module.md).

When the Max days in future value is configured by your administrator, you can’t select a date past the max allowed date. The dates in the calendar date picker are inactive for dates that are too far in future.

**Note:** If the Max days in future value isn’t configured, the date selection isn’t restricted. Date selection is based on the Max number of occurrences value. For more information, see [Configure a reservable module](config-reservable-module.md).

-   If you enter an invalid date which is greater than what is specified in the **Max days in future** value, the application resets the date to the current date.


</td></tr><tr><td>

Time

</td><td>

Start time when the reservation begins. Employees can select time using the drop-down list or by entering the time in the field. The time increment value depends on the value set by your administrator. Default reservation time duration available for selection is 30 minutes.The **time\_picker\_interval\_size** property for reservation start time and reservation end time is configured using the Service Portal Widget instances. The start time field increment value depends on the value set in the **time\_picker\_interval\_size**. Default reservation time increment value duration is 30 minutes.

**Note:** You can’t select a date that occurs in the past. The time for a selected location depends on the building time zone.

</td></tr><tr><td>

To

</td><td>

End date of your reservation. Select a number of days or dates on the calendar to make a multi-day reservation.Employees can't select a date and create a reservation when the End date exceeds the Max days in future value. The Max days in future value specifies the maximum number of the days in the future up to which the Reservable module can be reserved.

**Note:** In the case of a single day reservation, option to enter the end date isn’t available.

If you enter an invalid date which is greater than what is specified in the **Max days in future** value, the application resets the date to the current date.

**Note:** If the **Max days in future** value isn’t enabled, then the date selection isn’t restricted and is based on the **Max number of occurrences** value configured in the Reservable module. For more information, see [Configure a reservable module](config-reservable-module.md).

</td></tr><tr><td>

Time

</td><td>

End time when you would stop using the workplace item. Employees can select the end time using the drop-down list or by entering the time in the field. The end time increment value depends on the value set by your administrator. Default reservation end time duration is 30 minutes. The **time\_picker\_interval\_size** property for reservation start time and reservation end time is configured using the Service Portal Widget instances. The start time and end time field increment value depends on the value set in the **time\_picker\_interval\_size**. Default reservation time increment value duration is 30 minutes.

**Note:** You can’t select a date that occurs in the past. For example, If the start time is 09:00, you can select an end time after this duration. You can’t select a time before 09:00 on the same day. The time for a selected location depends on the building time zone.

</td></tr><tr><td>

Recurring

</td><td>

Option to reserve the workplace items on a recurring basis. Specify the number of days and the number of times that you want to repeat the reservation in a recurring series.For weekly reservations, select the days of the week for the reservation. The Recurring option is displayed based on the configuration that your admin has set. Also, if there are any recurring reservation conflicts, they’re auto-resolved if your admin has configured the same.

Auto-resolve recurring conflicts&lt;/uicontrol&gt; option is enabled on the Reservable module form. The application tries to auto-resolve recurring reservation conflicts. For more information, see [Auto-resolve recurring reservations](recurring-reservations.md).

**Note:** Adding extra services option isn’t available for Recurring reservations.

</td></tr><tr><td>

All day

</td><td>

Option to reserve the workplace item for an entire day or a single day. This option appears if your Workplace administrator has enabled the All day reservation setting on the selected **Type**. The start and end times of the reservation depend on the timings set by your organization. The **All day** option is also available on the Space details page. **Note:** The **All day** option's appearance depends on your administrator's configuration. If your admin has mandated all day reservation for a selected **Type**, the reservation is automatically made for the entire day. In case of All day you can only modify the Start date of the reservation.

</td></tr><tr><td>

Add another building

</td><td>

Reserve multiple workplace items spanning multiple buildings. The buildings time zones are different for a same date and time in a reservation.**Note:** This option is available if you have selected **Allow multiple reservations** check box on the **Reservable Module** &gt; **Reservable Module Configuration** tab. For more information, see [Create multi-building reservations](create-multi-building-reservation.md).

</td></tr></tbody>
</table>6.  Select **Add another building**.

    Reserve multiple workplace items across multiple locations and buildings belonging to the same neighborhood.

    The buildings can belong to different time zones for the same date and time in a single reservation.

    **Note:** This option is available if you've selected **Allow multiple reservations** check box on the Reservable Module Configuration.

    For more information, see [Create multi-building reservations](create-multi-building-reservation.md).

7.  Click **Search**.

    The workplace items that match the search criteria and which are available for reservations are displayed. By default when you click **Search**, the first building card is shown as selected and the available spaces in that building are shown.

    **Note:** While browsing near a person, if there are any private spaces, then they are not displayed in the search result.

8.  The card view shows all the available spaces.

    **Note:** You can switch between the **Card view** tab and the **Schedule view** tab to review the reservation timelines and the availability of workplace items.

    \(Optional\) To mark a location as favorite, click the **Card view** or **Schedule view** click the favorite icon \(Favorite icon.\)

9.  Click **Map view**, select a space and then select **Add** to add the space.

    The map view shows available and booked spaces.

    -   If your organization is using floor maps, view the floor maps using Mappedin or Indoor Mapping as your map provider.

        .

        -   Select a Campus on the Map view.
        -   Select a Floor from the drop-down list.
        -   Zoom in to select a building and location

            The building names are alphabetically sorted or sorted as per the **Order** that you have configured in the Buildings table.

10. For a multi day reservation search, the **Schedule view** shows available spaces in a day view.

    The schedule view shows available as well as unavailable spaces.

    ![Scheduled view showing available and unavailable spaces.](../image/wsd-scheduled-view-12hr.png)

    -   Clicking the chevron will take you to the next day and previous day.
    -   In case of a single day reservation, one-hour blocks are used to show the time scale for a day.
11. Click **Add**.

12. Select a Space or Spaces.

13. Select **Next**.

14. On the form, fill in the fields.

<table id="table_rjr_5lp_zlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reservation subject

</td><td>

Subject of your meeting.

</td></tr><tr id="make-all-space-private"><td>

Make all space details private

</td><td>

Option to make all the selected spaces as private.**Note:** The option is displayed based on the location privacy setup of the selected space\(s\).

 If you have selected multiple spaces, you can also specify your privacy preference for each space individually, using the **Mark space details private** below each space on the form.

</td></tr><tr id="make-space-detail-private"><td>

Make space details private

</td><td>

Option to set the space details of the space as private.**Note:** The option is displayed based on the privacy setup of the space.

</td></tr><tr><td>

Make subject private

</td><td>

Option to mark the subject of the reservation as private.

</td></tr><tr><td>

Reserve these items together for the same person

</td><td>

Option to reserve all the workplaces for the same user. This option appears if you've selected multiple workplace items for reservation.

</td></tr><tr><td>

Add a virtual meeting link

</td><td>

Option to generate a virtual meeting link so that remote employees can join the reservation. **Note:** \(Only applicable for Microsoft Teams\) As of the May Store 2023 release, when adding a meeting link, the application will retrieve the meeting details while synchronizing the event with a calendar provider.

</td></tr><tr><td>

This reservation is for

</td><td>

If you're requesting a reservation on behalf of someone else, select the name of that person. Leave this field empty if you're requesting a reservation for yourself.

</td></tr><tr><td>

Number of attendees

</td><td>

Number of people expected to attend the meeting.

</td></tr><tr><td>

Add notes

</td><td>

Option to add the meeting note to a reservation using the rich text editor. The notes can be shared with the meeting invitees. Users can also copy and paste text to the editor. The message can contain a maximum of 65,000 characters.Note is saved on the reservation record. Employees can update the note when required. The invitees receive a notification when note is added or updated. The reservation summary page shows the summary of the meeting note.

This option is available only if you have selected the **Allow reservation message** option on the Reservation widget configuration. For more information, see [Configure a reservable module](config-reservable-module.md).

</td></tr><tr><td>

**Add invitees to this reservation** section

</td><td>

**Note:** This section appears only if your administrator has enabled the configuration to invite attendees to this workplace location. This option will not appear if the **Number of attendees** option is displayed for the workplace location.

</td></tr><tr><td>

Invite coworkers

</td><td>

Employees whom you want to invite to the reservation.

</td></tr><tr><td>

Invite external visitor

</td><td>

Option to invite external visitor.**Note:** This option appears only if you have the Workplace Visitor Management application installed. The visitor details are automatically logged in the Workplace Visitor Management application for the reception staff to perform visitor-related tasks.

 -   If you've already registered the visitor, do the following:
    1.  Select **Previous visitor**.
    2.  In the **Select a prior visitor** field, select the visitor.

You can also preview the visitor details and modify any details if required. The details are updated automatically in all the visitor-related records and registration records.

-   If you're registering the visitor for the first time, do the following:
    1.  Select **Add new visitor**.
    2.  Select the **Visitor type**.
    3.  If the guest is a special guest, enable **VIP**.
    4.  Enter the **First name** of the visitor.
    5.  Enter the **Last name** of the visitor.
    6.  Specify the **Email Address** of the visitor to send registration details and communications.
    7.  Enter the **Phone number** of the visitor.
    8.  Enter the **Organization** details of the visitor.
    9.  Enter the **Title** of the visitor.
    10. In the Private notes section, specify any private information.
    11. In the **Visitor preferences** and **Notification preferences** fields, select the visitor's preferences.
    12. Add the visitor by clicking **Save and add**.


</td></tr><tr><td>

Add extra services

</td><td>

Click the **Add extra services**drop-down list to select a service that you want to add to your current reservation.**Note:** The **Add extra services** option is not available for recurring reservation.

When the employees select multi-building locations, new services are shown for the selected spaces so that they can add the services.

For example: In case if you have selected space arrangements as an extra service, then select the following items:

-   On the **Add Space Arrangement** dialog box, select a service from the drop-down list. For example, select **Chair layout**.
-   Select the Chair layout options:
    -   Classroom style
    -   Banquet rounds
    -   Theater style
-   Select the Number of seats.
-   Add additional comments for the service item.
-   Click **Add**.
-   A new case is created when a reservation or services are updated. A reference is added to the old and new service.
-   Application tries to retain the services. In case while updating a reservation, the space or location is not changed, then the services are visible and employees can update the reservation after changing the date and time.
-   In case, if space or location is changed while updating a reservation, then the application tries to propose the available services and applicable for a new location. Employees must select the suggested services and add it to their reservation while updating it.
-   In case if you are adding a space while updating a reservation, then you must add the services manually.
**Note:** In case, if you add a service item, a new case is created. If you update the reservation date, time, or location and update services by retaining or discarding them, then a reference is added to the new service \(replacement case for\) on the new case record and also a reference is added to the old service. A summary is added to the new case for items that are added, updated, or removed. For more information, see [View and track workplace cases](../../workplace-case-mgmt/task/view-workplace-cases.md).

</td></tr><tr><td>

Edit &lt;services name&gt;

</td><td>

Click **Edit** to update the services.-   The Update &lt;services name&gt; dialog box is shown.
-   Click **Update** to update the services.


</td></tr><tr><td>

Remove &lt;services name&gt;

</td><td>

Click **Remove** to remove the services from a reservation. A confirmation message is shown to confirm whether you want to remove the services from a reservation.

</td></tr></tbody>
</table>15. After verifying the services, employees can select a new date, time, and space to update the reservation details.

    On the **Reservation Details** page, select **Change date, time, or location** to update a reservation.

    On the Update meeting room reservation page, modify the **Start date and time** and **End date and time**. For more information about how to modify a reservation, see [Share, modify, or cancel a reservation](modify-cancel-res-request.md). If the item doesn't require any approval, the selected workplace item is reserved. The reservation details are displayed on the Reservation summary page. The state of the request is updated to **Confirmed**.

16. When you update a reservation, the Reservation details page shows the **Retain extra services** option to retain the services from the previous location and reservation.

    For more information about how to retain services, see [Create a reservation](create-reservation-request-1.md).

17. Click **Submit reservation**.

18. Click **Reservation Summary** to navigate to the Reservation Summary page.

    In case of multi-day reservation, the Reservation Summary page will show the reservation end duration.

    ![Reservation summary page.](../image/wsd-multi-dayr-rsv-summary-page.png)

19. Click **My Reservation** to navigate to the My Reservations page.

20. View and track the progress of your reservation status using the My Reservations page.

    ![My Reservations page showing the reservation details and reservation end duration for multi-day reservation.](../image/wsd-multi-dayr-rsv-summary-page.png)

    -   **Confirmed**: State to indicate that the reservation for the selected building is confirmed.

        **Note:** The **New space** state indicates that a new space is assigned due to a conflicted reservation.

    -   **Conflicted**: State to indicate that the application was not able to resolve the recurring reservation. Employees must manually find an alternate space, date, and time. Use the **Actions** field on the Reservation Summary page to **Change reservation occurrence**, **Cancel occurrence**. **Cancel series**, or **Share reservation**.

        **Note:** When a conflicting recurring reservation gets auto-resolved with the auto-resolution feature, it's status in **Reservation subtype** column is shown as **Exception** on the Workplace Reservations table.

        For more information, see [Auto-resolve recurring reservations](recurring-reservations.md).

21. The Reservation Summary page shows reserved spaces and it's status along with the duration for the reservation in case of multi-day reservation.

    Employees are informed in the case if they are viewing a multi-day reservation.

22. The **Actions** tab on the Reservation Summary page shows the following options:

    -   Share Reservation: Perform the following steps to share a reservation:
        1.  Select **Actions** &gt; **Share reservation**.
        2.  In the **Send reservation details to** field, select the users that you want to share the reservation with.
        3.  In the **Include a note**, enter a note if required.
        4.  Click **Send**.

            The reservation details are shared after the state of the reservation is **Confirmed**. If you edit the reservation details after sharing, the application will prompt you asking whether you want to send an email update to the users that you shared the reservation details with earlier.

    -   Update Reservation details
    -   Cancel Reservation: To edit or cancel your reservations, see [Share, modify, or cancel a reservation](modify-cancel-res-request.md).
23. Click **Check in** to check in a reservation, if the workplace item that you've reserved requires check-in and check-out.

    In the case an employee checks in their reservation, the complete reservation is checked in. The admin can indicate if a check in is allowed when there is still an active reservation happening on that space.

    **Note:** You must check in within 30 minutes before the reservation start time. If the reservation is not checked in within 30 minutes before the reservation start time, then the reservation is canceled. You will receive an email about the cancellation. The Check in option is also available on the My Reservations page.

24. Click **Check out** to check out a reservation.

    In the case an employee checks out their reservation, the end date and time is updated and the space is made available again.

    Check out within 30 minutes after the reservation end time. If the reservation is not checked out within 30 minutes after the reservation end time, you receive an email reminder to check out the reservation. The Check out option is also available on the My Reservations page.

25. An email notification is sent with the details of your reservation and the reservation is updated with your changes.

    In case of multi-day, reservation, the email notification contains the multi-day reservation details along with the number of days and hours a space is reserved for. For more information, about sharing a reservation, see [Create a reservation](create-reservation-request-1.md).

    ![Email notification for multi-day reservation showing the number of days a space has been reserved for.](../image/wsd-email-notification-multi-day.png)


## Result

## What to do next

Review your reservation details on the Reservation summary page.

1.  On the Reservation summary page, select **Actions** &gt; **Share reservation**.
2.  In the **Send reservation details to** field, select the users that you want to share the reservation with.
3.  In the **Include a note**, enter a note if required.
4.  Click **Send**
5.  When you share a reservation, invitees will receive an email notification.

    ![Shared email notification for a reservation with Browse all spaces and Reserve a space for me clickable link options.](../image/wsd-shared-email-options.png)

    You can perform the following from a shared reservation email:

    -   Login as System Administrator.
    -   Navigate to **All** &gt; **Emails** &gt; **Open shared reservation**.
    -   Two clickable links **Browse all spaces** and **Reserve a space for me** are shown:
        -   **Browse all spaces**: Click the **Browse all spaces** link to open the Reservation portal search page.

            If the shared reservation start date \(current date\) is within the number of days specified in the **Max number of days for browse near a person** Reservable Module property, then the **Browse all spaces** clickable link from a shared email notification will show pre-filled dates for a selected team member or colleague on the reservation portal search page.

            ![Browse all Spaces clickable link from shared email showing pre-filled dates on the reservation portal.](../image/wsd-shared-email-browse-all-spaces.png)

            -   On the Reservation portal search page, the **Browse near a person** is selected by default.

                If this path is not available, then, the **Browse all** path is used.

            -   All the fields are pre-filled for a selected team member or colleague.
            -   In case of multi-day reservation, the first day of a multi-day reservation is pre-filled. If the first day is in the past but the current date is still within the reservation time, the current date is selected. In case of multi-day reservation, consider the following:

                -   Start date and time: The first day of the multi-day reservation is shown. Start time is the start time of the reservation.
                -   End date and time: The End date and time of the reservation is pre-filled.
                For more information about multi-day reservation, see [Create a multi-day reservation](create-multi-day-reservation.md).

            **Note:** If the start day \(current date\) of a shared reservation is past the value set in the **Max number of days for browse near a person** Reservable module property, the **Browse all spaces** clickable link will not show pre-filled dates on the Make a reservation search page. Application shows a validation error message "**Reservation date for the selected user has changed. Select a date**'. In this case, employees must manually, select the **Start date and time** and **End date and time**.

        -   **Reserve a space for me**: When an employee clicks open the **Reserve a space for me** link from an email, the space reserved for a colleague or team member is selected by default. The system will create a reservation with the same start and end date and time. If the start date of the reservation falls prior to the current date, then the current date will be taken as the start date of the reservation. For example, if the start date is October 15, 2023 and the current date is October 17, 2023, the system will use the current date \(October 17, 2023\).

            **Note:** When making a reservation directly by using the **Reserve a space for me** clickable link option, application ignores the value set in the **Max number of days for browse near a person** Reservable module property and creates a reservation.

            ![Reservation a space.](../image/wsd-shared-email-rsv-space-for-me.png)


-   1.  On the Reservation summary page, select **Actions** &gt; **Share reservation**.
2.  In the **Send reservation details to** field, select the users that you want to share the reservation with.
3.  In the **Include a note**, enter a note if required.
4.  Click **Send**
5.  When you share a reservation, invitees will receive an email notification.

    ![Shared email notification for a reservation with Browse all spaces and Reserve a space for me clickable link options.](../image/wsd-shared-email-options.png)

6.  You can perform the following from a shared reservation email:
    -   Login as System Administrator.
    -   Navigate to **All** &gt; **Emails** &gt; **Open shared reservation**.
    -   Two clickable links **Browse all spaces** and **Reserve a space for me** are shown:
        -   **Browse all spaces**: Click the **Browse all spaces** link to open the Reservation portal search page.

            If the shared reservation start date \(current date\) is within the number of days specified in the **Max number of days for browse near a person** Reservable Module property, then the **Browse all spaces** clickable link from a shared email notification will show pre-filled dates for a selected team member or colleague on the reservation portal search page.

            -   On the Reservation portal search page, the **Browse near a person** is selected by default.

                If this path is not available, then, the **Browse all** path is used.

            -   All the fields are pre-filled for a selected team member or colleague.
            -   In case of multi-day reservation, the first day of a multi-day reservation is pre-filled. If the first day is in the past but the current date is still within the reservation time, the current date is selected. In case of multi-day reservation, consider the following:

                -   Start date and time: The first day of the multi-day reservation is shown. Start time is the start time of the reservation.
                -   End date and time: The End date and time of the reservation is pre-filled.
                For more information about multi-day reservation, see [Create a multi-day reservation](create-multi-day-reservation.md).

            **Note:** If the start day \(current date\) of a shared reservation is past the value set in the **Max number of days for browse near a person** Reservable module property, the **Browse all spaces** clickable link will not show pre-filled dates on the Make a reservation search page. Application shows a validation error message "**Reservation date for the selected user has changed. Select a date**'. In this case, employees must manually, select the **Start date and time** and **End date and time**.

        -   **Reserve a space for me**: When an employee clicks open the **Reserve a space for me** link from an email, the space reserved for a colleague or team member is selected by default. The system will create a reservation with the same start and end date and time. If the start date of the reservation falls prior to the current date, then the current date will be taken as the start date of the reservation. For example, if the start date is October 15, 2023 and the current date is October 17, 2023, the system will use the current date \(October 17, 2023\).

            **Note:** When making a reservation directly by using the **Reserve a space for me** clickable link option, application ignores the value set in the **Max number of days for browse near a person** Reservable module property and creates a reservation.

            ![Reserve a space.](../image/wsd-shared-email-rsv-space-for-me.png)

    The reservation details are shared after the state of the reservation is **Confirmed**. If you edit the reservation details after sharing, the application will prompt you asking whether you want to send an email update to the users that you shared the reservation details with earlier.

-   To edit or cancel your reservations, see [Share, modify, or cancel a reservation](modify-cancel-res-request.md).
-   To download an iCalendar, see [Download an iCalendar for a reservation](generate-ical.md).
-   To view, add, or remove any invitees from the reservation, do the following:

    1.  On the Reservation summary page, select the **Invitees** tab.

        The details of the invitee their name, email, assigned location, and invite acceptance states are displayed.

    2.  If you've selected multiple workplace items and you want to reassign the invitees to a different location, do the following:
        1.  Select the check box next to the invitee.
        2.  Select **Actions** &gt; **Assign to**.

            You can also select the Actions icon \(![Action icon.](../image/actions-invitees-icon.png)\) next to the invitee details.

        3.  In the **New location assignment** field, select the location where you want to move the invitee.
        4.  Click **Send update**.
    3.  Add or remove an invitee.
        1.  On the Reservation summary page, select **Actions** &gt; **Change reservation details**.
        2.  On the Reservation details page, go to the **Add invitees to this reservation** section.
        3.  Add an invitee by selecting the invitee name from the search list.
        4.  Remove an invitee by clicking the remove icon \(![Remove icon.](../image/remove-invitee-icon.png)\) near the invitee name.
        5.  Click **Update reservation details** tab.
    Invitees and visitors receive email notifications for the following actions:

    -   When a reservation is created, they will receive an email notification that they are invited to the reservation.
    -   When a reservation is cancelled or updated.
    -   When an invitee or visitor is removed from the reservation, they will receive an email notification that the invite has been canceled for them.
    **Note:** If push notifications are enabled in your organization and you have the Workplace Service Delivery for Mobile application, you will receive notifications for your reservation on your mobile device. For more information on reservation-related push notifications, see [Mobile push notifications for workplace reservations](../reference/reservation-push-notifications.md).

    For more information about making multi-day reservation using the Space Details page, see [Set a location as favorite using the Space details page](set-a-location-as-favorite.md).


**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Create a reservation](create-reservation-request-1.md)

[Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md)

[Auto-resolve recurring reservations](recurring-reservations.md)

[Set a location as favorite using the Space details page](set-a-location-as-favorite.md)

[Reserve a space near your colleague](browse-near-person-rsv.md)

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

