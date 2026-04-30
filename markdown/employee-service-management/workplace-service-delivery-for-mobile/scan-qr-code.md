---
title: Scan the QR code to reserve a space
description: Scan the QR code of a workplace and quickly reserve a space using the Now Mobile app.
locale: en-US
release: zurich
product: Workplace Service Delivery for Mobile
classification: workplace-service-delivery-for-mobile
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, Workplace Service Delivery for Mobile, Workplace Service Delivery, Employee Service Management]
---

# Scan the QR code to reserve a space

Scan the QR code of a workplace and quickly reserve a space using the Now Mobile app.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Log in to the ServiceNow® mobile app.

    The Mobile home page is displayed.

2.  You can also select a space from **My favorites** and reserve a space.

3.  Select a space.

4.  Tap **See my reservations** to see your existing reservations for a selected space.

    Select a space from the list of spaces to view the Reservation Information screen. For more information about the Reservation Information screen, see [Make a reservation using the Now Mobile app](make-a-reservation-on-mobile.md).

5.  Tap **Reserve** to reserve a location for a selected space.

6.  Space details screen is displayed with the quick reservation option for a day.

7.  Perform the following steps:

    1.  Reserve available time slot: Select a time slot for your reservation.

        -   Suggestion for available reservation time slots is displayed in horizontal blocks with a scroll bar.
        -   To view the time slots in a vertical list, select **View all**.

            The time slot duration is dependent on the **Max duration**and **Min duration** values configured by your administrator in the Reservable Module configuration. For more information, see [Configure a reservable module](../../wsd-reservation-management/task/config-reservable-module.md).

            The time displayed in the time slot considers the Start time of the working day \(sn\_wsd\_rsv.day\_start\) and End time of the working day \(sn\_wsd\_rsv.day\_end\) properties set by your administrator. If office hours are from 9 AM to 5 PM, then all the available reservation slots between 9 to 5 are divided into 2-hour intervals \(based on the values that you’ve provided for Max and Min duration\). However, if there are any existing reservations, then these aren’t displayed. Only available time slots for a reservation are displayed. If the available slot for a reservation is from 9 AM to 12 PM, and the maximum duration for a meeting is two hours, then 9–11 is the first time slot and 11–12 is the next time slot.

            For example, If the Max duration is two hours and the Min duration is 30 minutes. The office timings are from 9 AM to 5 PM, and a space \(Building A, Floor 3, Meeting room 1\) has two existing reservations. The first reservation is from 9 AM to 1.45 PM and another reservation is from 2 PM to 3 PM. Then, 3 PM to 5 PM can be the next time slot.

        **Note:** QR code reservation is not supported for **All day** reservation. Multi-day and recurring reservation is also not supported for QR code reservations.

    2.  Check availability: Manually select a Start date and time and End date and time for your reservation. If you try to select a past date or select any future dates, tThe time is reset to the current date. Time durations can be changed.
    3.  The Schedule view shows the time slot in vertical bars. Select the chevron icon \( ![chevron icon to move forward in the scheduled view calendar](../../../reuse/icons/product-icons/chevron-right-outline-24.svg)\) to move forward or select the icon \(![Chevron icon to move backward in the scheduled view calendar](../../../reuse/icons/product-icons/chevron-left-outline-24.svg)\) to go back and check the reservation time slot availability for a day.

        The selected time slot \(Step 9a\) is highlighted in green on the scheduled view. Existing reservations and unavailable time slots show shaded blocks. Vertical lines indicate a 1-hour duration while the dotted lines indicate a 30-minute duration.

    4.  If the selected time slot isn’t available or if the selected space is not available, a validation message is shown. Users can use the **Nearby spaces** option to check for available spaces or check for next available time slot. **Nearby spaces** section shows list of spaces that are nearby the scanned space and are available for reservation.
    5.  Select **View details** to see the space details.
8.  Tap **Reserve** to make your reservation.

    Check in your reservation by the start time and check-out the reservation after it ends. Open your reservation to check in directly using the My Reservations option on the home page.

9.  Review the reservation summary details.

10. Tap **Check in** to check in your reservation.

    For more information, see [Check in or check out a reservation](check-in-out-rsv-on-mobile.md).

11. Select the **Actions** drop-down options to:

    -   Change reservation details
    -   Cancel reservation
    -   Share reservation
12. To submit a general inquiry or raise a complaint request, select **Submit a request**.

    **Note:** This option appears only if the Workplace Case Management plugin is installed.

    1.  In the **What can we help you with?** field, enter your inquiry details.

    2.  Tap **Submit**.

        A case is submitted for the inquiry.

    3.  After reviewing the inquiry details, tap **Close**.

13. To view and change your reservation details, select **See my reservation**.

    This option appears only if you have a reservation on this space.

    1.  Select the more options icon.

        \(\)

        The availability of the icon depends on the type of device that you’re using.

    2.  To edit the reservation, tap **Edit reservation**.


**Parent Topic:**[Using Workplace Service Delivery for Mobile](../concept/using-wsd-mobile.md)

**Previous topic:**[Share your reservation details with other users](share-rsv-details.md)

**Next topic:**[Work with Location Directory for Now Mobile app](view-location-directory-mobile.md)

