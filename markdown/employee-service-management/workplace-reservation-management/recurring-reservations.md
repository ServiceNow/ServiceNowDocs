---
title: Auto-resolve recurring reservations
description: While making a recurring reservation, only the availability of the first occurrence is checked. It’s possible that a future occurrence of the meeting may run into conflicts. To avoid such conflicts, while scheduling a recurring reservation, the Workplace Reservation Management application tries to auto-resolve any recurring conflicts.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Auto-resolve recurring reservations

While making a recurring reservation, only the availability of the first occurrence is checked. It’s possible that a future occurrence of the meeting may run into conflicts. To avoid such conflicts, while scheduling a recurring reservation, the Workplace Reservation Management application tries to auto-resolve any recurring conflicts.

## Before you begin

Administrators can choose to auto-resolve recurring reservation conflicts at the Reservable module level.

**Note:** Ensure that you have enabled **Allow recurring reservations** and **Auto-resolve recurring conflicts** options on the Reservable Module form. For more information, see [Configure a reservable module](config-reservable-module.md).

If you’re upgrading from a previous version of Workplace Reservation Management and if you've updated the form layout before, you must edit the form view again to display the **Auto-resolve recurring conflicts** field.

**Note:** Reservations in a recurring series cannot be updated in bulk. To update a reservation, select a reservation and edit it as required.

The application tries to find an alternative space automatically for conflicted occurrences based on the following logic:

-   When floor maps are available, the application tries to find a space closest to the same capacity, then looks for one with more capacity, and lastly, for one with less capacity.
-   When no floor map is available, the application finds an alternative space in the same area or on the same floor.
-   Favorite spaces are prioritized over 'location' \(within the same area or within proximity\).
-   Application searches for a space of the same type.
-   Application searches for a space with similar standard services.
-   Employee is notified through the Reservation Summary page and via email when the application assigns an alternative space.

**Note:** Adding extra services option isn’t available for Recurring reservations.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Module**.

2.  Navigate to **Workplace Core** &gt; **Workplace service portal** &gt; **Workplace Service Portal Home** &gt; **Make a Reservation**.

3.  Create a reservation.

    For more information about how to create a reservation, see [Create a reservation](create-reservation-request-1.md).

    For example, two workplace users, Abel Tutor and Abel L create reservations. Abel L creates a reservation for Tuesday 11/22 10.00 AM to 12.00 PM in Room A1-02-01.

4.  Select **Recurring** to make a recurring reservation.

5.  Make the required changes and submit the reservation.

6.  Another workplace user \(Abel Tutor\) makes a recurring reservation.

    Abel Tutor makes the reservation for the week 11/21 to 11/25 from 09:00 to 3 PM for the same space \(Room A1-02-01\). For more information, see step 3.

7.  After submitting the reservation, notice that the user \(Abel Tutor\) is now assigned a different space for Tuesday since it was already booked by Abel L in Step 3.

    The new space is visible on the reservation summary page. When the conflicting reservation occurrences are resolved, the application tries to assign a new workplace, date, and time within the same module or an alternative space is assigned for the existing date and time. You’re also notified via email.

    The **New space** state indicates that a new space is assigned due to a conflicted reservation.

    **Note:** When a conflicting recurring reservation gets auto-resolved, its status is shown in the Reservation table, and the **Reservation subtype** column is set to **Exception**.

8.  If the **Auto-resolve recurring conflicts** property is set to false or not enabled in the Reservable module, and you try to make a reservation \(see Step 3\), conflicting reservations occur if the same space is booked by another workplace user.

    In such cases, the employee is expected to resolve the reservation conflicts manually by finding an alternative space, date, and time.

9.  When viewing the details of a conflicting reservation, the employee can find an alternative space and time using the **Recurrences** option on the Reservation Summary page.

    ![Reservation summary page showing conflicts in reservation and option to find another available space.](../image/wsd-conflicting-recurring-reservation.png)

10. Select the required options from the **Actions** drop-down list on the Reservation Summary page:

    -   Change reservation occurrence
    -   Cancel occurrence
    -   Cancel series
    -   Share reservation
11. From the email notifications that you receive, select the **View reservation series** option to update space and time for a conflicted reservation.

12. Find an available space or time and create a reservation.

13. Submit the reservation.

    If the **Auto-resolve recurring conflicts** option is enabled, the conflicting recurring reservation in a series is resolved and the user is assigned an available space. When this option isn’t enabled, workplace users must manually update the time and space for a given reservation.


**Parent Topic:**[Reserve workplace items](../concept/reserve-workplace-items.md)

**Related topics**  


[Create a reservation](create-reservation-request-1.md)

[Add invitees as collaborators and create a reservation](add-colleagues-rsv-search.md)

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

[Create a group reservation](create-group-reservation.md)

[Share, modify, or cancel a reservation](modify-cancel-res-request.md)

[Reserve a workplace using the Quick Reservation widget](reserve-workplace-for-a-time-slot.md)

[Download an iCalendar for a reservation](generate-ical.md)

