---
title: Make workplace reservations on the kiosk
description: Workplace visitors and guests with kiosk viewer role can make workplace reservations. They can search and select a space on the Kiosk Map to reserve a space.
locale: en-US
release: xanadu
product: Workplace Services Kiosk
classification: workplace-services-kiosk
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 6
breadcrumb: [Use Workplace Services Kiosk, Workplace Services Kiosk, Workplace Service Delivery, Employee Service Management]
---

# Make workplace reservations on the kiosk

Workplace visitors and guests with kiosk viewer role can make workplace reservations. They can search and select a space on the Kiosk Map to reserve a space.

## Before you begin

Install and configure the following from the ServiceNow Store.

-   Workplace Reservation Management
-   Workplace Services Kiosk
-   Workplace Central
-   Workplace Indoor Mapping
-   Workplace Core
-   Workplace Space Management

Make sure that your device is set up on a kiosk to enable workplace reservations. For more information, see [Setup a kiosk on a physical device for reservations](kiosk-setup-rsv-space.md).

You can’t add workplace services to a reservation in kiosk. Recurring, neighborhood, and browse near a person reservations aren’t supported for kiosk reservation.

Role required: sn\_wsd\_kiosk.viewer, sn\_wsd.core\_workplace\_user

**Note:** The sn\_wsd.core\_workplace\_user \(workplace user\) role is part of the kiosk viewer role. Employees can log in with the sn\_wsd.core\_workplace\_user role to view, search for spaces on a floor map and make a reservation. For more information, see [Components installed with Workplace Services Kiosk](../reference/components-workplace-services-kiosk.md).

Role: sn\_wsd\_kiosk.viewer.

## Procedure

1.  Log in to your instance with the kiosk viewer role.

    ![The welcome page shows the Explore Map option for workplace kiosk viewers to search and select a space for reservation.](../images/kiosk-welcome-page-kiosk-viewer-4.png)

2.  Select **Explore Map**.

    The Explore Workplace page opens and displays workplace locations on the map.

    ![Search for a space to make a reservation on the kiosk map.](../images/kiosk-map-explore-workplace-page-5.png)

3.  From the menu, select **Building** and **Floor** to select a building and a floor.

4.  Zoom in and select a space on the map to make a reservation.

5.  Space details card for the selected space shows the **Get directions** and **Reserve** button.

    ![Space Details card with option to Reserve displayed on map for a selected space.](../images/kiosk-map-space-details-card.png)

    If the selected space is already reserved, it shows the **Raise an issue** tab. Raise an issue tab is also shown if the space type configuration in the Reservable Module configuration for the kiosk doesn't match the space type configuration of a selected space.

    -   Select the ellipsis icon \(![](../images/kiosk-raise-an-issue-icon.png)\) and select **Raise an issue**.

        The Raise an Issue form opens.

        ![Raise an issue form with options to raise a request for maintenance or workplace issues.](../images/kiosk-raise-an-issue-form.png)

    -   On the form, fill in the field information.

<table id="table_wff_nkg_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

What can we help you with?

</td><td>

Option to provide the workplace issue for which you want to raise a case.

</td></tr><tr><td>

Urgency

</td><td>

Option to prioritize the urgency of the case. Select any of the following options: -   Today
-   This week
-   Next week


</td></tr><tr><td>

Requested for

</td><td>

Search and select a user for whom you are raising the workplace issue.

</td></tr></tbody>
</table>6.  Select **Reserve** to create a workplace reservation.

    **Note:** Space types configured for you by your administrator are displayed on the map. For example, Meeting rooms or Desks/Spaces. If your administrator has set the space type configuration as Desks/Spaces in the Kiosk Reservable module, the floor map shows only desks or space. If the space type configuration is meeting rooms, the map shows meeting rooms for reservations. For more information, see [Configure Reservable Module for kiosk reservation](config-rsv-module-kiosk.md).

7.  Select **Get Directions**.

    ![Options to get directions on the map using the Accessible or Default options.](../images/kiosk-get-directions-map.png)

    Select your current position on the map, and select the location on the map for getting directions on the map.

    Select **Accessible** or **Default** for getting directions to a workplace on the map.

8.  The Reserve a space page opens and the selected space is shown on a schedule view calendar.

    ![Reserve a space showing reservation start date, start time, and end time along with the Reservation subject.](../images/kiosk-rsv-2.png)

    On the form, fill in the information.

<table id="table_inf_jvg_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reserve for

</td><td>

Option to select a date. If **All day** Reservable module configuration is set to **Disabled**, the current date is selected and the **Reserve for** option is read-only. If Max days in future value is set to more than 1, the **Reserve for** option shows options to select calendar dates.

</td></tr><tr><td>

From

</td><td>

Option to select the start time of the reservation.

</td></tr><tr><td>

To

</td><td>

Option to select the end time of the reservation.

</td></tr><tr><td>

Reservation subject

</td><td>

Option to provide the Reservation subject details. For example, Reservation for AI workflows. If the **Require Subject** check box is selected in the **Reservation Widget Configuration** tab, you’re required to enter the Reservation Subject label while submitting the reservation. For more information, see [Configure Reservable Module for kiosk reservation](config-rsv-module-kiosk.md)

</td></tr></tbody>
</table>    When All day **Reservable Module** setting is set to **Default** on the Reservable module configuration, you see the actual time when you’re making a reservation. For example, if you’re making the reservation at 11.24 am, reservation start time shows **11.24**. Start and end time for a reservation are based on the building time zone and reservation properties for setting office hours. For more information, see [Properties installed with Workplace Reservation Management](../../wsd-reservation-management/reference/properties-installed-with-wsd-reservation-mgmt.md).

    ![All day check box is selected and shows office hours as 9 am to 5 pm.](../images/kiosk-all-day-default-settings-map-view.png)

    If **All day** Reservable configuration is set to **Enabled**, the reservation start and end timings are rounded off. For example, 11.30 am to 12.30. The All day check box isn’t selected with office timing shown from 9 am to 5 am. The timing shown depends on your office start time and end time.

    ![All day check box is inactive and shows office hours as 9 am to 5 pm.](../images/kiosk-all-day-enabled-unchecked-onmap.png)

    If **All day** Reservable module configuration is set to **Required**, the **All day** check box shown in read-only mode and you can’t change the start time and end time. The building's current time is shown based on the building time zone.

    ![All day check box is selected and inactive. Office hours are shown as 9 am to 5 pm.](../images/kiosk-all-day-required-readonly-onmap.png)

    **Note:** If you’re trying to book a space beyond the time specified in the Min or Max duration, application displays an error message. The **All day**, **Min duration** and **Max day duration** values are set by your administrator. For more information, see [Configure Reservable Module for kiosk reservation](config-rsv-module-kiosk.md).

9.  Select **Submit Reservation**.

    If a reservation can’t be created for a space that is already reserved, a message is displayed informing the employee that the space isn’t available anymore. The schedule view is refreshed with the latest search results. The **Submit reservation** button is inactive. The employee can change the date or time to find a new, available slot.

    **Note:** After your reservation is confirmed in the kiosk, email notifications aren’t sent to workplace users.


**Parent Topic:**[Use Workplace Services Kiosk](../concept/use-workplace-services-kiosk.md)

