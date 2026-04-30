---
title: Create a reservation
description: Create reservations across multiple buildings, campuses, neighborhoods, or sites. Create a reservation spanning across multiple days. Add attendees or visitors to a reservation. Synchronize reservation details and resolve conflicts when scheduling recurring reservation events. Add workplace services \(room configurations, catering, and so on\) to your reservation.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2026-03-05"
reading_time_minutes: 39
---

# Create a reservation

Create reservations across multiple buildings, campuses, neighborhoods, or sites. Create a reservation spanning across multiple days. Add attendees or visitors to a reservation. Synchronize reservation details and resolve conflicts when scheduling recurring reservation events. Add workplace services \(room configurations, catering, and so on\) to your reservation.

## Before you begin

Install and configure the following:

-   Workplace Core
-   Workplace Central
-   Workplace Space Management
-   Workplace Case Management
-   Workplace Indoor Mapping
-   Workplace Visitor Management
-   Workplace Maintenance Management

Role required: sn\_wsd\_core.workplace\_user

## About this task

Reserve a workplace space based on your office working hours.

Create a workplace reservation for a single day or for multiple days. Administrators can set the max days in future value in the **Reservable Module Configuration** tab. For more information, see [Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md).

Space and reservation planners \(sn\_wsd\_rsv.reservation\_planner\) with the dedicated role \(sn\_wsd\_rsv.bypass\_module\_validation\) can ignore or bypass certain settings in the Reservable module configuration. For more information, see [Allow Event planners to handle reservations with more flexibility](../../workplace-central/concept/event-planner-bypass-validation-rule-overview.md).

For example, reservation planners or space planners with the dedicated role \(sn\_wsd\_rsv.bypass\_module\_validation\) can ignore or bypass the following settings in the Reservable module:

-   Max days in the future
-   Max number of occurrence
-   Min and Max duration
-   Available in
-   All day

Role: sn\_wsd\_core.workplace\_user.

## Procedure

1.  Select any of the following context menu navigation options to make a workplace reservation.

<table id="choicetable_prt_yr3_smb"><thead><tr><th align="left" id="d491415e135">

Location

</th><th align="left" id="d491415e138">

Navigation path

</th></tr></thead><tbody><tr><td id="d491415e144">

**From Employee Center Portal**

</td><td>

-   Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
-   On the Employee Center portal, select **Workplace Services** &gt; **Browse Workplace Services**.
-   Select the **New general reservation** card.

Make a reservation portal page opens for you to make workplace reservations.

</td></tr></tbody>
</table>    The Make a Reservation page opens in a new tab.

    ![Make a reservation form page showing options to select location, date, and time. Make recurring or all day reservation as required.](../image/rsv-portal-page-map-use.png)

2.  From **Type**, select a Reservable Module configuration.

    For example, select any of the following Reservable Module configuraiton. For more information, see [Configure a reservable module](config-reservable-module.md).

    -   Desks
    -   Desks with an Area
    -   Meeting rooms require approval
    -   Meeting rooms
    -   Desks with a shift
3.  From **Where**, select any of the Reservable paths:

    The following reservation paths are available for a selected Reservable Module.

    -   Browse all
    -   Browse near a person
    -   Browse by area
    -   Browse by neighborhood
    -   Browse all spaces
4.  Select **Browse all**.

    The **Browse all** reservable path is selected by default.

    1.  Search for a workplace item that you want to reserve using the following available criteria.

5.  Complete the following information.

    On the form, fill in the fields.

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

Start date of your reservation. For a single day reservation, only the **From** field is shown and not the option to enter the end date.-   Employees can't select a date and create a reservation if the start date exceeds the Max days in future Reservable module value. Thisn’t value is configured on the Reservable module by your administrator. For more information, see [Configure a reservable module](config-reservable-module.md).

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

End date of your reservation.Employees can't select a date and create a reservation when the End date exceeds the Max days in future value. The Max days in future value specifies the maximum number of the days in the future up to which the Reservable module can be reserved.

**Note:** In the case of a single day reservation, option to enter the end date isn’t available.

If you enter an invalid date which is greater than what is specified in the **Max days in future** value, the application resets the date to the current date.

**Note:** If the **Max days in future** value isn’t enabled, then the date selection isn’t restricted and is based on the **Max number of occurrences** value configured in the Reservable module. For more information, see [Configure a reservable module](config-reservable-module.md).

</td></tr><tr><td>

Time

</td><td>

End time when you would stop using the workplace item. Employees can select the end time using the drop-down list or by entering the time in the field. The end time increment value depends on the value set by your administrator. Default reservation end time duration is 30 minutes. The **time\_picker\_interval\_size** property for reservation start time and reservation end time is configured using the Service Portal Widget instances. The start time and end time field increment value depends on the value set in the **time\_picker\_interval\_size**. Default reservation time increment value duration is 30 minutes.

**Note:** You can’t select a date that occurs in the past. For example, If the start time is 09:00, you can select an end time after this duration. You can’t select a time before 09:00 on the same day. The time for a selected location depends on the building time zone.

</td></tr><tr><td>

All day

</td><td>

Option to reserve the workplace item for an entire day or a single day. This option appears if your Workplace administrator has enabled the All day reservation setting on the selected **Type**. The start and end times of the reservation depend on the timings set by your organization. The **All day** option is also available on the Space details page. **Note:** The **All day** option's appearance depends on your administrator's configuration. If your admin has mandated all day reservation for a selected **Type**, the reservation is automatically made for the entire day. In case of All day you can only modify the Start date of the reservation.

</td></tr><tr><td>

Add another building

</td><td>

Reserve multiple workplace items spanning multiple buildings. The buildings time zones are different for a same date and time in a reservation.**Note:** This option is available if you have selected **Allow multiple reservations** check box on the **Reservable Module** &gt; **Reservable Module Configuration** tab. For more information, see [Create multi-building reservations](create-multi-building-reservation.md).

</td></tr></tbody>
</table>6.  Select Recurring to make a recurring reservation.

    When making a recurring reservation, select the most suitable recurring pattern \(Daily, Weekly, or Monthly\) based on the space availability within the recurring series.

    **Note:** Reservations in a recurring series cannot be updated in bulk. To update a reservation from a recurring series, select a reservation and edit it as required. The option to make a recurring reservation is configured by your administrator. The **Allow recurring reservations** Reservable Module configuration option should be enabled for making recurring reservations. This option is dependent on the **Max days in future** and **Max number of Occurrences** value. For more information, see [Configure a reservable module](config-reservable-module.md) Reservations with single occurrences are converted to a single-day reservation.

    Shift-based reservable module configuration is not supported for Recurring reservations.

    Calculate and set a recurring meeting pattern define the frequency and recurrence pattern in the Add Recurrence dialog box.

    1.  Set a start date, end date, and duration \(start time and end time\) for your reservation.

        For example:

        -   Start date: Select 25/02/2026 as your reservation start date.
        -   End date: Select 23/08/2026 as your reservation end date.
        -   From: Select a start time for your reservation.

            Duration or start time and end time depends on the selected building time zone.

        -   To: Select a time when you want to end your meeting or reservation.

            The end time is based on the standard working hours \(full day\) of your office.

            **Note:** The start date is reset if you select a different start and end date in the Add recurrence dialog box. For more information, see Step c. It's recommended that you select the start and end dates prior to setting the recurrence patterns in the Add recurrence dialog box.

    2.  Select Recurring list options as required:
        -   **Daily**: Option to set daily recurring series.
        -   **Weekly on Wednesday**. This option label changes as per the weekday that you have selected as your start day. For example, selecting Wednesday as your meeting weekday shows **Weekly on Wednesday**.
        -   **Monthly on fourth Wednesday**. This option label changes as per the selected weekday. For example, selecting Wednesday as your meeting start day shows Monthly on fourth Wednesday.
        -   **Every weekday \(Monday to Friday\)**
        -   **Custom**: Customize your recurring reservation options as required for Daily, Weekly, or Monthly recurrences.
    3.  Select any of the following recurring patterns to open the Add recurrence dialog box and select the required recurring pattern:

        1.  Daily:The meeting occurs every day. You can define a repeat interval of every X days.

            ![Daily Recurrence options showing reservation start and end date and recurrence pattern.](../image/add-recurrence-daily.png)

            1.  In the Add recurrence dialog box, confirm that the start and end dates are correct. Select the required recurrence pattern.

                Select the duration, repeat duration, and number of occurrences or date when you want to end the reservation. ![Select duration for daily recurrence meetings.](../image/add-recurrence-daily-end-date.png)

            2.  Select **Save**.

        2.  Weekly: The meeting takes place on the same weekday each week. You can define a repeat interval of every X weeks. For example, select the following recurrence Pattern for weekly or biweekly reservations.
            -   Weekly, Every 1 week on Wednesday. The meeting occurs every Wednesday starting Feb 25, 2026, ending on Aug 19, 2026 \(the last Wednesday before Aug 23\). Confirm that the start and end dates are correct. Select the required recurrence pattern.

                ![Select the weekly recurrence options and duration.](../image/add-recurrence-weekly-end-date.png)

            -   Bi-Weekly \(Every 2 Weeks\). Every 2 weeks on a selected weekday. For example, bi-weekly on Wednesday.
            -   Select **Save** after selecting the required weekly recurring pattern and duration.

                If the reservation time duration has only one occurrence in case of weekly recurring reservation, the single occurrences are converted to a single-day reservation. For example, consider a recurring reservation from 13-02-2026 to 18-02-2026 set to repeat weekly once on every Monday. Since, in this duration, there's a single Monday when the reservation is scheduled to repeat weekly, it is considered as a single-day reservation.

        3.  Monthly: Specific day of a month. For example, the last Wednesday of every 1 month. In the Add recurrence dialog box, confirm that the start and end dates are correct. Select the required recurrence pattern. You can define a repeat interval of every X Month. To select a day of the month, select **On**. Select from a date range, for example **29**, **30**, **31** or **Last day**

            Day 29,30, and 31: You can only select these days for a month, if the selected dates are available for a selected month. For example, February and April are skipped by the application if you select the date as **31**. If you set it to the **Last day** option, it selects the last day of a month automatically.

            .

            ![Select the required recurrence meeting pattern and duration for monthly meetings.](../image/add-recurrence-monthly-end-date.png)

        **Note:** If you select an invalid date range or number of occurrences for a recurring patter, the **Save** button is not available for selection. Reset the date range to save your changes.

    4.  Custom: Customize your recurring reservation options as required for Daily, Weekly, or Monthly recurrences.
    **Note:** If you change the start and end time duration for a reservation after setting a recurring reservation, it resets the duration for the reservation. You should add or update the recurring series and pattern again.

    **Note:** The option to set a recurring reservation pattern is also available on the My favorites page. Select a favorite space. On the Space details page, you can set a reservation to recurring.

    Consider the following when selecting a recurrence pattern. For example, select a recurring reservation from Feb 25, 2026 - August 23, 2026:

    -   Total Reservation Duration: The date range span covers approximately 179 days, which is about 25 weeks.
    -   Reservation End duration: If the pattern extends beyond the end date 23.08.26, application ends the reservation. You can choose to end the recurrence after a certain number of occurrences. The calendar doesn’t allow you to select a range beyond what is specified in the **Max number of occurrences** reservable module property configuration.
    -   If your workplace manager has enabled time-bound allocations, the workplace availability changes based on the start and end date of an allocation. For example, if you select five recurring days, and the workplace is allocated for 3 out of the five days, the availability of the workplace is 3/5. Only the first occurrence of the recurring reservation is checked for time-bound allocations.
    Upon confirming the required recurring reservation pattern and saving your changes, the Make a reservation portal page displays the recurring reservation duration selected by you.

    To update or edit recurring reservation series, select the edit option to edit your recurring reservation.

    **Note:** Recurring series cannot be edited. You can edit single reservation at a time and not the entire series.

7.  Select Add Invitees.

    This option is available when your administrator has enabled the Reservable Module property configuration **Allow attendees based search** on the Reservation Widget Configuration. This option allows employees to add attendees to a reservation and search for their availability on the Make a reservation portal page. For more information, see [Configure a reservable module](config-reservable-module.md) and [Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md).

8.  Select **Search**.

    Available spaces for reservations are displayed automatically. The first building card is selected by default in the search result.

9.  The application performs auto-search for reservable items when the reservation property \(**sn\_wsd\_rsv.enable\_auto\_search**\) is enabled by your administrator.

    If an auto-search reservation property is configured by your administrator, the **Search** button is hidden on the reservation portal. The application searches for reservable locations and items automatically while creating a reservation. An auto- search is triggered when any of the following is changed or updated:

    -   Reservable module.
    -   Reservable paths.
    -   Building.
    -   Floor.
    -   Start Date.
    -   End Date.
    -   All day.
    -   Recurring \(Daily/Weekly/Monthly\)
10. Select **Refresh the results** manually to refresh the search results on the advanced reservation portal page while making a reservation.

    When the auto-search property is enabled, the reservation portal search page shows a message to refresh the page when an employee stays too long on a page or when the search results are outdated. Select **Refresh the results** manually to fetch the latest reservation search results data.

11. Select the toggle option **Show Filters** to filter by:

    -   Minimum Capacity: Filter by space capacity.
    -   Services: Filter by Workplace Services
    -   Purposes: Filter by Location purposes.
    -   Floors: Filter by Floors for a selected building.
    Select **Apply** to apply the selected filter option.

12. Select **Alphabetically A-z** list option to sort the workplace items in an alphabetical order \(Z-A or A-Z\)

    The **My favorites First** sort option is automatically selected if you have favorite locations. Your favorite locations are displayed first in an alphabetical order followed by the other locations that match the search criteria.You can view and perform the following actions after you set a space as favorite:

    1.  When searching for a space, you can sort the workplace items to display your favorite locations at first using the **My favorites first** sort option. By default, if you have favorite locations, the default sort option is set to **My favorites first**.

        The workplace items are sorted and all your favorite locations are displayed first in an alphabetical order.

    2.  If you're browsing for a workplace location near a person, you can sort the workplace items to display your favorite locations first using the **My favorites first** sort option.

        The favorite locations are displayed based on the proximity closest to the person's location.

    **Note:** You can’t sort workplace items in alphabetical order or by your favorite locations if you're browsing spaces near a person. The spaces near a person are searched based on proximity.

13. Select a location or locations from Search Results.

14. View search results using the **Card**, **Schedule**, or **Map** tab.

    ![Schedule view showing locations for reservations.](../image/rsv-schedule-view.png)

15. Select the workplace item that you want to reserve using any of the following options:

    -   Select the **Card**, **Schedule**, or **Map** tab.
        -   Select a Campus on the Map.

            ![Map view showing spaces on a floor map.](../image/rsv-map-view.png)

        -   Select a Floor from the drop-down list.

            The floor names are alphabetically sorted or sorted based on the sorting **Order**. The values are sorted based on the indicated sort order, if it’s available. You can indicate the sort order in the Floors table. If the sorting Order value isn’t specified for an item, then the items are listed on top of the list \(ascending order\), and then, sorted alphabetically. The Floor names are alphabetically sorted based on the label names. For example Floor A, Floor B, and so on. For more information about sorting order, see [Add a floor using Workplace Space Management](../../workplace-space-management/task/add-a-floor-1.md).

            **Note:** If the **Order** is null for all available buildings in a selected campus, then floor names are alphabetically sorted based on floor name label. For example Floor A, Floor B, and so on.

        -   Zoom in to select a building and location

            The building names are alphabetically sorted or sorted according to the **Order** that you have configured in the Buildings table.

    -   Select a space and then, select **Add** to add a space.

        While reserving or viewing a space, the employee can see if a space is part of a neighborhood. The neighborhood icon \(![Neighborhood icon.](../../wsd-for-mobile/images/neighborhood-icon.png)\) is displayed on the space card.

        If your organization is using floor maps, you can view the floor maps for a location using Indoor Mapping as your map provider.

        .

        If you have selected the **Browse by neighborhood** option in Step 6, the reservation portal shows spaces for a neighborhood.

        When you browse by neighborhood, all spaces belonging to a neighborhood are displayed but you can only select available spaces within a neighborhood.

16. To show or hide spaces or layers on the Map, do the following:

    -   Select a building or a floor on the Map.
    -   Select the Filter out layers and places icon \(![Filter out layers and places.](../image/filter-place-layers-icon.png)\) to filter out spaces and layers on the map.
    -   From the **Display Options** list, select **Spaces** or **Layers** and clear to remove the selected spaces or layers from the Map View.
    -   Select **Apply**.
    By default, all the spaces and layers are selected or checked.

    **Note:** The spaces and layers that are displayed on the floor map are based on the Layer types and Place types table configuration settings in Indoor Mapping. Navigate to **All** &gt; **Indoor Mapping** &gt; **Place types** or **All** &gt; **Indoor Mapping** &gt; **Layer types** to open the Places or Layer types page respectively. Set the Filter out layers and places **Filter out layers and places** column to **true** to display the places \(spaces\) or layers that you want to display on the floor map.

17. Select a space and mark a location as favorite by selecting the favorite icon \(![Favorite icon.](../image/favorite-icon.png)\) on the space card.

18. Select **Next** to add spaces and make a reservation.

    ![Card view showing available spaces on the reservation portal.](../image/rsv-add-space-select-next.png)

    When you create a reservation in a sync-enabled space or location using Personal Authentication mode, a valid OAuth token is required to access your Microsoft Outlook or Google Calendar account.

    **Note:** If you have activated Personal Authentication mode in Workplace Calendar Synchronization and attempt to reserve a sync-enabled space or location without a token, a pop-up notification is displayed informing you that the token is unavailable. To retrieve the token, log in using the respective email credentials: Microsoft Exchange Server credentials for Microsoft Outlook or Google Calendar credentials for Google Calendar.

    Selected space is added to reservable items. The Reservation Details page opens.

19. On the Reservation Details form, fill in the fields.

    ![Reservation details form showing options to add the Reservation subject, add invitees to your reservation, and invite external visitors.](../image/rsv-summary-page-add-invitees.png)

    ![Add new visitor form on the Reservation Details page.](../image/rsv-add-new-visitor-form.png)

    ![Add or remove workplace services from a reservation.](../image/rsv-remove-service-message.png)

<table id="table_rjr_5lp_zlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reservation subject

</td><td>

Subject of your meeting. For example, Status meeting.

</td></tr><tr id="make-all-space-private"><td>

Make subject private

</td><td>

Option to make reservation subject as private.

</td></tr><tr id="make-space-detail-private"><td>

Make space details private

</td><td>

Option to set the space details of the space as private.**Note:** The option is displayed based on the privacy setup of the space.

If you have selected multiple spaces while adding a reservation, you can specify your privacy preference for each workspace individually by using the **Make space details private**.

</td></tr><tr><td>

Reserve these items together for the same person

</td><td>

Option to reserve all the workplaces for the same user. This option appears if you have selected multiple workplace items for reservation.

</td></tr><tr><td>

Add a virtual meeting link

</td><td>

Option to generate a virtual meeting link so that remote employees can join the reservation. **Note:** \(Only applicable for Microsoft Teams\) As of the May Store 2023 release, when adding a meeting link, the application retrieves the meeting details while synchronizing the event with a calendar provider.

</td></tr><tr><td>

This reservation is for

</td><td>

If you're requesting a reservation on behalf of your team member, select the name of that person. Leave this field empty if you're requesting a reservation for yourself.

</td></tr><tr><td>

Number of attendees

</td><td>

Number of people expected to attend the meeting.

</td></tr><tr><td>

Add notes

</td><td>

Option to add the meeting note to a reservation using the rich text editor. The notes can be shared with the meeting invitees. Users can also copy and paste text to the editor. The message can contain a maximum of 65,000 characters.Note is saved on the reservation record. You can update the note as required. The invitees receive a notification when note is added or updated. The reservation summary page shows the summary of the meeting note.

This option is available only if your administrator has configured the **Allow reservation message** option on the Reservation module. For more information, see [Configure a reservable module](config-reservable-module.md).

\\

</td></tr><tr><td>

**Add invitees to this reservation** section

</td><td>

**Note:** This section appears only if your administrator has enabled the configuration to invite attendees to this workplace location on the Reservable module. This option doesn't appear if the **Number of attendees** option is available for a selected location.

</td></tr><tr><td>

Invite coworkers

</td><td>

Coworkers or team members are added to the meeting invite and are notified when this option is selected.

</td></tr><tr><td>

Invite external visitor

</td><td>

Option to invite an external visitor.**Note:** This option appears only when Workplace Visitor Management is installed and configured. The visitor details are automatically logged in the Workplace Visitor Management for the reception staff to perform visitor-related tasks.

 -   If you have already registered a visitor, do the following:
    1.  Select **Previous visitor**.
    2.  In the **Select a prior visitor** field, select the visitor.

You can also preview the visitor details and modify any details if necessary. The details are updated automatically in all the visitor-related records and registration records.

-   If you're registering a visitor for the first time, do the following:
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
    12. Add the visitor by selecting **Save and add**.


</td></tr><tr><td>

Add extra services

</td><td>

Select **Add extra services** to select a service from the list to add a workplace service to your current reservation.**Note:** The **Add extra services** option is not available for recurring reservation.

When you select multiple buildings while adding a reservation, new services are shown for selected locations. You can add these services as required to your reservation.

From the list options, select Space arrangement as an extra service. Select the following options:

-   On the **Add Space Arrangement** dialog box, select a service from the list. For example, select **Chair layout**.
-   Select the Chair layout options:
    -   Classroom style
    -   Banquet rounds
    -   Theater style
-   Select the Number of seats.
-   Add additional comments for the service item.
-   Select **Add**.
-   A new case is created when a reservation or services are updated. A reference is added to the old and new service.
-   Application tries to retain the services when you update a location.

When updating a reservation, if the location isn’t updated, the services are visible and you can update the reservation after changing the date and time.

-   In case, if space or location is changed while updating a reservation, the application tries to propose available services for a new location. Select the required services and add it to your reservation while updating or modifying a reservation.
-   If you’re adding a new space while updating a reservation, you must add the services manually.
**Note:** If a workplace service is added to a reservation, a workplace case is created. If you update the reservation date, time, or location and update services by retaining or removing the services, a reference is added to the updated workplace service. The **replacement case for** option is displayed on the new case record form and also a reference is added to the old service. A summary is added to a workplace case record for items that are added, updated, or removed. For more information, see [View and track workplace cases](../../workplace-case-mgmt/task/view-workplace-cases.md).

</td></tr><tr><td>

Edit &lt;services name&gt;

</td><td>

Select **Edit** to update the services.-   The Update &lt;services name&gt; dialog box is shown.
-   Select **Update** to update the services.


</td></tr><tr><td>

Remove &lt;services name&gt;

</td><td>

Select **Remove** to remove the services from a reservation. A confirmation message is shown to confirm whether you want to remove the services from a reservation.

</td></tr></tbody>
</table>20. Select **Submit reservation**.

    The Reservation Summary page opens.

    ![Rservation page showing reservation as confirmed, the room details, date, time, number of invitees, workplace services, and so on.](../image/rsv-summary-confirmed-rsv.png)

    If the workplace item doesn't require any approval, the selected item is reserved. The reservation details are displayed on the Reservation summary page. The state of the request is updated to **Confirmed**. If your request requires approval, it’s submitted to a workplace approver. The state of the request is updated to **Awaiting approval**. For more information, see [Approve a reservation](approve-res-req.md).

    An email notification is sent regarding the reservation confirmation along with the details to the organizer and the user is added to the reservation. If you have invited attendees or any visitors, they receive a notification for the reservation invite. You receive email notifications when reservable synchronization is configured for Workplace Calendar Synchronization. You receive notifications for your reservation on your mobile device when push notification is enabled.

21. Review the reservation summary page.

    **Note:** For multi-day reservation, the reservation summary shows reservation end time duration. For a single day, reservation, only the start date and time are shown.

    While reserving or viewing a space, the employee can see if a space is part of a neighborhood.

    1.  Select **Check in** to check in a reservation, if the workplace item that you have reserved requires check-in and check out.

        **Note:** You must check in within 30 minutes before the reservation start time. If the reservation isn’t checked in within 30 minutes before the reservation start time, your reservation is canceled. An email notification is sent for the canceled reservation. The Check-in option is also available on the My Reservations page.

        In case, if you have occupancy sensors installed in your workplace location, your reserved spaces are automatically checked in. You also receive a push notification on the Workplace Service Delivery for Mobile app when your reserved spaces are checked in automatically. If the workplace location or space state is Occupied, the application automatically checks in the reservation. The reservation state moves to In progress state. A push notification is sent to Workplace Service Delivery for Mobile "Your reservation has started. You’re automatically checked in based on the presence detected at the space. No further action is required." If the state of the space is Unoccupied or Invalid, the application sends a push notification "Your reservation for Reservation for &lt;space-name&gt; has started. Either Check in to confirm your attendance or Release Booking to Cancel the space reservation". For more information, see [Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md).

    2.  Select **Check out** to check out a reservation.

        Check out within 30 minutes after the reservation end time. If the reservation isn’t checked out within 30 minutes after the reservation end time, you receive an email reminder to check out the reservation. The Check out option is also available on the My Reservations page.

    3.  Select the **Invitees** tab to view, add, or remove any invitees from the Reservation Summary page.

        The details of the invitee such as their name, email, assigned location, and invite acceptance states are displayed.

    4.  If you have selected multiple workplace items and you want to reassign the invitees to a different location, do the following:

        -   Select the Invitees check box.
        -   Select **Actions** &gt; **Assign to**.
        -   In the **New location assignment** field, select the location to be assigned to an invitee.
        -   Select **Send update**
    5.  To add or remove an invitee, do the following:

    1.  On the Reservation summary page, select **Actions** &gt; **Change reservation details**.

        ![Change or modify reservation details.](../image/rsv-update-rsv-details.png)

    2.  On the Reservation details page, scroll to view Add Invitees to this reservation section.

    3.  Add a new invitee or remove an existing invitee by selecting the invitee name from the search option.

    4.  Select the **Update reservation details** tab.

        Invitees and visitors receive email notifications for the following actions:

        -   When a reservation is created.
        -   When a reservation is canceled or updated.
        -   When an invitee or visitor is removed from the reservation, a cancellation mail is sent.
22. If your administrator has configured the **Default reservation path when editing a reservation** value on the Reservable Module, the following reservable paths are shown while editing or updating a reservation:

    For more information see, [Configure a reservable module](config-reservable-module.md)

    **Note:** This option isn’t available on the Now Mobile app.

<table id="table_rps_3tt_1xb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Based on reservation

</td><td>

You can search locations in the context of a Reservable Path that was used while creating a reservation as shown in Step 2. For example; **Browse all**, **Browse by area**, **Browse by neighborhood**.

</td></tr><tr><td>

Browse all

</td><td>

If you have selected this option on the Reservable module, then while editing a reservation, the context \(Reservable Path\) is defaulted to **Browse all**. You can change or update the selected space, date, or time of the reservation.

</td></tr></tbody>
</table>23. After reviewing the workplace services added to a reservation, you can select a new date, time, and location to update the reservation details.

24. On the Reservation Details page, select**Change date, time, or location** to update a reservation.

25. On the Update meeting room reservation page, modify the date, time, and location as required.

26. When you update a reservation, the Reservation details page shows the **Retain extra services** option to retain the services from the previous location and reservation.

    When you update or change a location, a message is shown to indicate that certain services are going to be removed. This happens when workplace services for an updated location are not available. Users are notified if the services are available for a location. The Reservation details page shows services that are available on the new location and also shows the services that aren’t available on the new location.

    Workplace Services are automatically retained when the date or time changes for a reservation. But if a location is changed, or if a new location or space is added, you must select to **Retain** your existing workplace services. You can retain, review, or discard the proposed services. When this action is performed, the services are considered **Resolved** for that location. When all location workplace services are resolved, confirm the changes. If location workplace services aren’t resolved, a pop-up message is displayed to confirm the action.

    **Note:** In this case, if the **Allow only single service item selection** option is selected on the Workplace services page, the **Retain Services** option isn’t shown on the Reservation details page and the existing services are removed after updating the reservation details for a space \(location\). You can add new services using the **Add extra services** option as shown in step 11. For more information, see [Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md).

    On the form, fill in the fields.

<table id="table_akf_pyk_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Retain extra services

</td><td>

URL link to the workplace location to view the list of services that are retained after updating the reservation details. Select the location link to review services to be retained or removed.

</td></tr><tr><td>

Discard

</td><td>

Option to remove services for a location.

</td></tr><tr><td>

Retain

</td><td>

Option to retain services after updating the reservation details.Workplace services are automatically retained when date and time are updated for a reservation. Select **Retain**, when a location is changed or when a new location is added to a reservation. You can retain or remove the proposed workplace services. The workplace services are resolved for a location when you update a reservation.

**Note:** If workplace services are retained, the quantity is reset to 1. Review the retained workplace service. Workplace services such as space configurations and space layouts aren’t retained for a reservation.

</td></tr></tbody>
</table>    -   Services are canceled if they aren’t available or applicable for a location.
    -   While updating a multi-location reservation, employees are notified after matching the workplace services from previous workplace locations.
    -   When you change an existing service or services for a reservation, existing workplace case is canceled. A new workplace case is created as a replacement for an existing case and the workplace services are updated.
    -   A state is added to the changed service. A note is added on the new service case with the changes to the ordered services \(added, updated, removed, no changes\). For more information, see [View and track workplace cases](../../workplace-case-mgmt/task/view-workplace-cases.md).
    -   The costs of services are shown based on the case or requested item fields.
    -   The cost is updated when a workplace service is updated.

        **Note:** Cost of service items are updated if an employee updates existing service offerings. For example, if you have not changed your extra service item but have changed the time for a reservation record, the cost of the service item is updated based on the latest pricing of the service item. In case, if you remove a space \(location\) and the service item is also removed from a reservation record, suggested services in the **Retain Services** option show the latest pricing or cost in the reservation record.


## Result

-   Select **Reservations** &gt; **My Reservations** to view and track your reservation on the Reservation portal home page or on the Reservation summary page.
-   **Confirmed**: Reservation State to indicate that the reservation for the selected building is confirmed.

    **Note:** The **New space** state indicates that a new space is assigned due to a conflicted reservation.

-   **Conflicted**: Reservation State on the Reservation summary page. This state shows that the application was not able to resolve the recurring reservation. You must manually find an alternate space, date, and time. Use the **Actions** tab on the Reservation Summary page to select the **Change reservation occurrence**, **Cancel series**, or **Share reservation**.

    An email notification is sent and the reservation is updated with your changes.

    **Note:** When a conflicting recurring reservation gets auto-resolved with the auto-resolution feature, its status in the **Reservation subtype** column is shown as **Exception** on the Workplace Reservations table.

    For more information, see [Auto-resolve recurring reservations](recurring-reservations.md).


## What to do next

Review your reservation details on the Reservation Summary page.

While reserving or viewing a space, the employee can see if a space is part of a neighborhood. The neighborhood icon \(![Neighborhood icon.](../../wsd-for-mobile/images/neighborhood-icon.png)\) is displayed on the space card.

-   To share the reservation details with others, perform the following actions:

    1.  On the Reservation summary page, select **Actions** &gt; **Share reservation**.

        Sh![Share reservation details form showing options to add recipients for sharing the reservation.](../image/rsv-share-reservation-form.png)

    2.  In the **Send reservation details to** field, select the users that you want to share the reservation with.
    3.  In the **Include a note**, enter a note if necessary.
    4.  Select **Send**
    5.  When you share a reservation, invitees receive an email notification.

        ![Shared email notification for a reservation with Browse all spaces and Reserve a space for me navigational link options.](../image/wsd-shared-email-options.png)

    6.  You can perform the following from a shared reservation email:
        -   Log in as an administrator.
        -   Navigate to **All** &gt; **Emails** &gt; **Open shared reservation**.
        -   Two navigational links **Browse all spaces** and **Reserve a space for me** are shown:
            -   **Browse all spaces**: Select the **Browse all spaces** link to open the reservation portal page.

                If the shared reservation start date \(current date\) is within the number of days specified in the Max number of days for browse near a person, the **Browse all spaces** clickable link. The clickable links are shown from a shared email notification with pre-filled dates for a selected team member.

                -   The **Browse near a person** reservable path is selected by default. If it path isn’t available, the **Browse all** path is used.
                -   All the fields are pre-filled for a selected team member or a colleague.
                -   For multi-day reservation, the first day of a multi-day reservation is prefilled. If the first day is in the past but the current date is still within the reservation time, the current date is selected. In case of multi-day reservation, consider the following:

                    -   From: The start date of your reservation.
                    -   Time: Select the start time for your reservation from the drop-down list.
                    -   To: End date of your reservation.
                    -   Time: Select the end time for your reservation from the drop-down list.
                    For more information about multi-day reservation, see [Create a multi-day reservation](create-multi-day-reservation.md).

                **Note:** If the start day \(current date\) of a shared reservation is past the value set in the **Max number of days for browse near a person** Reservable module property, the **Browse all spaces** link doesn't show prefilled dates on the Make a reservation page. The application shows a validation error message "**Reservation date for the selected user has changed. Select a date**. You must manually, select the start date and time and end date and time for a reservation.

            -   **Reserve a space for me**: When you select the **Reserve a space for me** URL link from an email, the space reserved for a colleague or team member is selected by default on the reservation portal. A reservation is created with the same start and end date and time from your previous reservation. If the start date of the reservation falls prior to the current date, the current date is taken as the start date of the reservation. For example, if the start date of your previous reservation is October 15, 2023 and the current date is October 17, 2023, the application uses the current date \(October 17, 2023\).

                **Note:** When making a reservation directly by using the **Reserve a space for me** navigational link option, the application ignores the value set in the **Max number of days for browse near a person** Reservable module configuration and creates a reservation.

    The reservation details are shared when a reservation is **Confirmed**. If you edit the reservation details after sharing, you’re prompted to send an email update to reservation invitees.

-   To edit or cancel your reservations, see [Share, modify, or cancel a reservation](modify-cancel-res-request.md).
-   To download an iCalendar, see [Download an iCalendar for a reservation](generate-ical.md).
-   -   If you want to reserve a space using a shared reservation, after you select **Reserve a space for me**, the application automatically reserves one of your favorite locations that has the closest proximity to the space reserved in the shared reservation details.
-   Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Reservation Overview** &gt; **All Reservations** to view all workplace reservations.
-   Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Reservation Overview** &gt; **My Reservations** to view all reservations made by you.

**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md)

[Auto-resolve recurring reservations](recurring-reservations.md)

[Reserve a space near your colleague](browse-near-person-rsv.md)

[Create multi-building reservations](create-multi-building-reservation.md)

[Create a multi-day reservation](create-multi-day-reservation.md)

[Create neighborhood reservations](create-neighborhood-reservations.md)

[Create reservation for multiple workplace items](create-reservation-for-multiple-wrkplceitems-1.md)

[Create a group reservation](create-group-reservation.md)

[Enable shift-based reservation](enable-shift-based-reservation.md)

[Set a location as favorite using the Space details page](set-a-location-as-favorite.md)

[Create a reservation along with a shared reservation](create-rsv-along-with-shared-rsv.md)

[Create a reservation including a virtual meeting link](Create-reservation-with-virtual-meeting.md)

[Create a shift reservation](create-a-shift-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

