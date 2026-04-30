---
title: Make a reservation using the Now Mobile app
description: Reserve a workplace location from anywhere and at any time using the Now Mobile app.
locale: en-US
release: zurich
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Use, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Make a reservation using the Now Mobile app

Reserve a workplace location from anywhere and at any time using the Now Mobile app.

## Before you begin

Ensure that you have the following applications installed:

-   Workplace Core \(sn\_wsd\_core\).

    For more information, see [Install Workplace Core](../../workplace-service-delivery/task/install-workplace-service-delivery.md).

-   Workplace Reservation Management \(sn\_wsd\_rsv\).

    For more information, see [Install Workplace Reservation Management](../../wsd-reservation-management/task/install-wsd-reservation-mgmt.md).

-   Workplace Service Delivery for Mobile

To view floor maps, you must have the following installed:

-   Workplace Space Mapping, Workplace Indoor Mapping, and Mappedin are installed
-   Ensure Map view is enabled. For more information, see [Enable map view to create reservations](enable-map-view-mobile-reservations.md).

**Note:** Creating reservations for shift-based modules aren’t supported on native mobile.

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  On your mobile device, open the Now Mobile app.

    ![Workplace Service Delivery Mobile Home Screen](../images/wsd-mobile-homepage.png)

    ![Mobile home screen showing the Make a reservation option.](../images/wsd-mobile-make-rsv-home-page.png)

2.  Tap **Make a reservation**.

3.  The Make a reservation section shows the Reservable Modules.

    For example: Select **Desks**.

    ![Make a reservation screen showing Reservable Modules.](../images/wsd-mobile-reservable-module-desks.png)

4.  In case, if you have set the Reservable Module property **Max days for multi-day** for two or more days, the **Make a reservation** screen shows the number of reservable days up to which a multi-day reservation can be made.

    The default value of **Max days for multi-day** is 1.

    If the **Max days for multi-day** value is set to 1, only single day reservations can be made and the **All day** option is enabled while making a reservation. If the **Max days for multi-day** value is set to 2 or higher value, the **All day** reservation option is disabled.

    ![Max days for multi-day value of 7 and Max days in future of 90 days shown on the Make a reservation screen.](../images/wsd-multi-day-rsv-mob-1.png)

    The **Max days in future** is configured on the Reservable module by your administrator, the number of days in the future up to which the reservation can be made is displayed on the card. The **Max days in future** value is 1 or higher. If an employee tries to select an invalid date range, search results for a reservation aren’t returned.

5.  To make a quick reservation for any workplace, under the Quickly reserve section, tap **Reserve this location**.

    If you have set any favorite locations in the Workplace Reservation Management Reservation portal, the Quick reserve section displays your favorite location in **My favorites**.

    **Note:** The workplace type that is available in the Quick reserve section depends on the configuration made by your organization.

6.  Select a reservable path.

    Multi-day reservation is available for all the reservable paths. For example: Select Browse all.

    -   Browse all
    -   Browse near a person
    -   Browse by area
    -   Browse by neighborhood
    ![Make a reservation screen showing the Reservation paths.](../images/wsd-mobile-browse-all.png)

7.  Add room or space requirements.

    1.  On the form, fill in the fields.

<table id="table_izv_mll_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Building

</td><td>

Building where you want to reserve the workplace.

</td></tr><tr><td>

Floor

</td><td>

Floor where you want to reserve the workplace.

</td></tr><tr><td>

Reservation start

</td><td>

Start time of the reservation.

</td></tr><tr><td>

All day

</td><td>

Option to enable the **All day** or a single day reservation.Time: All day depends on the start and end day reservation properties set by your administrator.

</td></tr><tr><td>

Start Date Time and End Date Time.

</td><td>

Option to select the Select the Start Date Time and End Date Time.**Note:** Reservable module property for multi-days **Max days for multi-day** is dependent on the Reservable Module **Max days in future** value. You can reserve a space for multi days only within the range \(number of days\) specified for the **Max days in future** value. If the reservation start date and end date range is more than the **Max days in future** value, the application shows a validation error and the End date and time is defaulted to the current date.

</td></tr><tr><td>

Reservation end

</td><td>

End time of the reservation. This field is automatically set to an hour after the start time.

</td></tr><tr><td>

Capacity

</td><td>

Capacity of the reservation.**Note:** If you’re using an iOS device, tap on **Done** after specifying the capacity.

</td></tr><tr><td>

Standard services

</td><td>

Option to select from available standard services based on which the locations must be filtered.**Note:** The field is visible only if you are using Workplace Service Delivery for Mobile version .

</td></tr><tr><td>

Reservable purposes

</td><td>

Option to select from available reservable purposes based on which the locations must be filtered. The field is visible only if you are using Workplace Service Delivery for Mobile version .If you specified both **Standard services** and **Reservable purposes**, the search returns only those locations that have met both the specified criteria.

</td></tr><tr><td>

Toggle Map view

</td><td>

View the available reservations using a floor map view instead of a list view. The option to view a map is available only if the map property is set by your administrator for a selected space or room. For more information, see [Configure the Toggle map view property](configure-toggle-map-view.md).

</td></tr></tbody>
</table>        **Note:** Reservation uses the workplace profile's building, floor, start and end date and time details, in case if no user preferences are set. If the selected space isn’t mapped to any area, then the building and floor details are auto-populated or pre-filled in **Browse all spaces**. If a space is mapped to an area, building and floor details are pre-filled in **Browse by area**. If both user preference and a workplace profile exists, user preference takes precedence, and space mapping is done by user preference. The **Browse by area** field is auto-populated based on user preferences and not by workplace profile.

8.  Click **Next**.

9.  Select the locations that you are reserving.

    Locations that are set as favorite on the Reservation portal are prioritized and displayed in an alphabetical order followed by other workplace locations.

    Tap Building to show the floor level information, and select a floor.

    -   On the list view, you can select one or more locations.

        To search for a location, enter the exact location name in the search box.

        **Note:** If you’re browsing a space near a user, only the five most suitable spaces are listed.

    -   On the map view, you can zoom in on the map to select one or more locations.

        Use the **All floors** drop-down list to switch between floors.

        Click the **Selected** button to review your selections, or select **All** to navigate back to the map view. You can also select rooms on different floors.

        **Note:** Map view is available only if it’s enabled by your administrator.

10. Click **Next**.

11. To browse all the available spaces, select **Browse all spaces**.

12. To search for reservable spaces in the context of a neighborhood, select the **Browse by Neighborhood** option.

    **Note:** **Browse by Neighborhood** option is only available if **Enable browse by neighborhood** option is configured by your administrator.

    1.  Specify the following details to search for the most suitable space in an area.

        -   **Neighborhood**: Name of the neighborhood.
        -   **Building**: Name of the building available in a neighborhood. For example: NBH2
        -   \(Optional\) **Floor**: Floor of the building where you want to make a reservation. The reservation admin can indicate in the Reservable Module if an employee can use a floor in the search.
        -   **Start date and time**: Date and time when you would start using the workplace item. The time is displayed based on the selected building's time zone.
        -   **End date and time**: Date and time when you would stop using the workplace item. The time is displayed based on the selected building's time zone.
13. To reserve a space from your favorite space, tap **Browse favorites**.

    The spaces that you have set as favorite using the Workplace Reservation Management Reservation portal are displayed with the favorite icon \(![Favorite space icon.](../../wsd-reservation-management/image/favorite-icon.png)\). If you want to set any location as favorite, refer to [Set a location as favorite using the Space details page](../../wsd-reservation-management/task/set-a-location-as-favorite.md).

    **Note:** The favorite option appears only if you have Employee Center 25.0.0 and if your administrator has configured the settings.

14. To reserve an available space near a person, tap **Browse near a person**.

    1.  Select the user near whom you want to reserve a space in the **Look for spaces near this colleague**.

        **Note:** If there are any private reserved spaces near the person, then they aren’t displayed in the search result.

    2.  Select a reservation made by the user in the **Choose colleague's reservation**.

    3.  Select **Toggle Map view** to review the available reservations using a map view instead of a list view.

        This option is available only if activated by your administrator.

15. To reserve an available space in a particular area, tap **Browse by area**.

    1.  Select the **Building** of the area where you want to make a reservation.

    2.  Select the **Area** where you want to make a reservation.

    3.  Select a start date and time in the **Start date and time**.

    4.  Select an end date and time in the **End date and time**.

    5.  Select **Toggle Map view** to review the available reservations using a map view instead of a list view.

        The available favorite space is highlighted on the map.

        **Note:** This toggle is available only if activated by your administrator.

    6.  Select a floor from the **Floor** drop-down list on the Map view.

        For example: Floor 1.

    7.  Available spaces belonging to a neighborhood for a building are shown.

16. Tap **Next**.

17. On the Map view, select **Get Directions** for wayfinding and indoor navigation.

    For more information, see [Work with Location Directory for Now Mobile app](view-location-directory-mobile.md).

18. Click **Submit**.

    In personal authentication mode, to reserve a sync-enabled room, you must check your email and click the link to log in to Microsoft Exchange. After logging in and obtaining the token through the redirect link, you can return to the reservation screen and submit the reservation.

19. The Reservation Information screen shows the **Details** tab with reservation details.

    In the case of multi-day reservation, the Reservation Information screen shows the number of days in a series for which a space is reserved \(start date time and end date time\).

<table id="table_bf3_11v_xwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Give your reservation a name

</td><td>

Option to provide a subject or name for your reservation.

</td></tr><tr><td>

This reservation is for

</td><td>

User name. For example: Abel Tuter.

</td></tr><tr><td>

Start Date and time

</td><td>

Reservation start date and time.

</td></tr><tr><td>

End Date and time

</td><td>

Reservation end date and time.

</td></tr><tr><td>

Virtual Meeting link

</td><td>

Option to generate a virtual meeting link so that remote employees can join the reservation.

</td></tr><tr><td>

Additional message

</td><td>

Users can view the meeting note for a reservation on the mobile app. Employees can’t add or update the meeting note on the mobile app. They can only view it. The meeting notes can be added on the advanced reservation web portal.

</td></tr><tr><td>

Workplace location

</td><td>

Workplace reservation location.

</td></tr><tr><td>

Floor

</td><td>

Floor name.

</td></tr><tr><td>

Building

</td><td>

Building name.

</td></tr><tr><td>

Sensitivity

</td><td>

Subject appears on your calendar and is viewable by everyone except when the reservation sensitivity is set to private.

</td></tr><tr><td>

Make all Space details private

</td><td>

Specify your privacy preferences.**Note:** This option is displayed based on the privacy setup made on the selected space.

You have the following options to set your reservation to:

-   None
-   Normal
-   Private
-   Confidential


</td></tr><tr><td>

Check-in-state

</td><td>

Awaiting check-in.When workplace spaces are having occupancy sensor and if the state of the space is unoccupied or Invalid, application sends push notification "Your reservation for Reservation for &lt;space-name&gt; has started. Either Check in to confirm your attendance or Release Booking to Cancel the space reservation".

For more information, see [Configure automatic check-in for reserved spaces](../../wsd-reservation-management/concept/configure-rsv-check-in.md).

</td></tr><tr><td>

Created

</td><td>

Reservation created date and time.

</td></tr><tr><td>

Updated

</td><td>

Reservation details updated date and time.

</td></tr></tbody>
</table>    The **Related reserved items** will show the related workplace service items for a reservation.

20. Tap the additional information icon \(![More information icon.](../../legal-mobile/image/action-icon.png) \) to perform the following:

    -   Edit reservation: \(Optional\) If required, enter the following information:
        -   Set the **Reservation subject** field.
        -   Set the **On behalf of** field to the user for whom you want to make the reservation.
    -   Share reservation
    -   Cancel reservation
21. Tap **Submit**.

22. Click **Check in** to check in a reservation, if the workplace item that you've reserved requires check-in and check out.

    **Note:** You must check in within 30 minutes before the reservation start time. If the reservation isn’t checked in within 30 minutes before the reservation start time, then the reservation is canceled. You receive an email about the cancellation. The Check in option is also available on the My Reservations page.

    In case, if you have occupancy sensors installed in your workplace location, your reserved spaces are automatically checked in. You also receive a push notifications on Workplace Service Delivery for Mobile app when your reserved spaces are checked in automatically. If the workplace location or space state is Occupied, then, application automatically checks in the reservation. The reservation state moves to In progress state. A push notification is sent to Workplace Service Delivery for Mobile "Your reservation has started. You are automatically checked in based on the presence detected at the space. No further action is required." If the state of the space is Unoccupied or Invalid, application sends push notification "Your reservation for Reservation for &lt;space-name&gt; has started. Either Check in to confirm your attendance or Release Booking to Cancel the space reservation". For more information, see [Configure automatic check-in for reserved spaces](../../wsd-reservation-management/concept/configure-rsv-check-in.md).


## Result

The workplace reservation is confirmed.

## What to do next

View your reservation status in the My reservations section. For more information, see [Edit or cancel a reservation on Now Mobile app](edit-rsv-on-mobile.md).

In the case of multi-day reservation, My reservations show the status of the reservation along with the number of days the multi-day reservation is spanning across.

If the workplace item that you've reserved requires check-in and check out, see [Check in or check out a reservation](check-in-out-rsv-on-mobile.md).

To reserve a space using the QR code scanning option, see [Scan the QR code to reserve a space](scan-qr-code.md).

**Parent Topic:**[Using Workplace Service Delivery for Mobile](../concept/using-wsd-mobile.md)

**Previous topic:**[Search for a campus, building and a space using AI Search](ai-search-buildings-floors.md)

**Next topic:**[Get directions to a workplace](get-directions-to-a-workplace.md)

