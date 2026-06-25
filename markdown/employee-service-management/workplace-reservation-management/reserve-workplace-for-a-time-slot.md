---
title: Reserve a workplace using the Quick Reservation widget
description: Reserve a workplace quickly by using the Quick Reservation widget in the Workplace Service Portal. The widget enables you to select from a list of available time slots instead of specifying the start and end times.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/reserve-workplace-for-a-time-slot.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Reserve a workplace using the Quick Reservation widget

Reserve a workplace quickly by using the Quick Reservation widget in the Workplace Service Portal. The widget enables you to select from a list of available time slots instead of specifying the start and end times.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user

## About this task

With the Quick Reservation widget, you can directly make a quick reservation from the Workplace Service Portal home page. Specify the type of space that you are looking for, the date, the time slot, and the building in which you want to reserve a space. Depending on your specifications, the workplace that best matches your specifications is displayed. You can either make a reservation directly using the Quick reservation widget or use the Reservation portal to search for more suitable workplaces. Select **Advanced reservations** to open the Reservation portal.

**Note:** It is not possible to make a shift-based reservation using the Reservation widget.

\[Omitted image "wsd-rsv-home-page-quick-rsv.png"\] Alt text: Quick Reservation widget.

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Portal** &gt; **New Reservation**.

2.  Select the Quick Reservation widget on the home page.

3.  In the Quick Reservation widget, specify the details to make a reservation.

    1.  In the **Reserve a** field, select the type of workplace that you want to reserve.

    2.  To select the date of reservation, click the calendar icon \( \[Omitted image "calendar-icon.png"\] Alt text: Calendar icon.\)

    3.  In the **Time slot** field, select a time slot for which you want to make a reservation.

        **Note:** Employees are not allowed to create a reservation too far in the future if they have enabled **Max days in future** value on the Reservable module. A warning message is shown in case if an employee tries to enter a date that is greater than the **Max days in future** value. For example, if the **Max days in future** value is 90 days, and if you try to select a date beyond 90 days, a warning message is displayed. For more information, see [Create a reservation]() and [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

        If the**Max days in future** value is not enabled, users can select a date as per the **Max number of occurrences** on the Reservable module.

    4.  In the **Location** field, click the location selection icon to select the building where you want to make a reservation.

        \[Omitted image "location-selection-icon.png"\] Alt text: Location selection icon.

    5.  In the **Floor** field, select the floor on which you want to make a reservation.

    6.  If you want to change the privacy of the space, select or deselect the **Mark space details private** option.

    The space that best matches the reservation criteria is displayed. If you have set favorite locations, then those locations are prioritized first for the best match.

4.  To set the space as favorite, click on the Favorite icon.

    \[Omitted image "favorite-icon.png"\] Alt text: Favorite icon

    **Note:** The Favorite icon will appear only if you have access to the Employee Center.

5.  To make the reservation, select **Reserve this desk**.

    If a space is part of a neighborhood, employees can see the neighborhood information on the space details card.

6.  To apply more filter criteria or to view all the spaces that match the specified criteria on the Reservation portal, select **Advanced reservations**.

    For more information on how to make a reservation on the Reservation portal, see [Create a reservation]().


## Result

The workplace is reserved for the selected time slot.

To view the details of the reservation, click **View details**. To cancel the reservation, click **Release space**.

**Parent Topic:**[Reserve workplace items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/reserve-workplace-items.md)

**Related topics**  


[Create a reservation]()

[Add invitees as collaborators and create a reservation]()

[Auto-resolve recurring reservations]()

[Set a location as favorite using the Space details page]()

[Reserve a space near your colleague]()

[Create a multi-day reservation]()

[Create multi-building reservations]()

[Create neighborhood reservations]()

[Create reservation for multiple workplace items]()

[Enable shift-based reservation]()

[Create a reservation along with a shared reservation]()

[Create a reservation including a virtual meeting link]()

[Create a shift reservation]()

[Create a group reservation]()

[Share, modify, or cancel a reservation]()

[Download an iCalendar for a reservation]()

