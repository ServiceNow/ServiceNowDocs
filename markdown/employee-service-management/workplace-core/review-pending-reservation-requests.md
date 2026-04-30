---
title: Review pending workspace reservation requests
description: Review pending workplace reservation requests from employees in Workplace Core and assign available workplaces to complete these requests.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing workplace reservations for employees, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Review pending workspace reservation requests

Review pending workplace reservation requests from employees in Workplace Core and assign available workplaces to complete these requests.

## Before you begin

Role required: sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Safety Management** &gt; **Workplace Requests** &gt; **Pending**.

2.  Open a pending request that you want to address.

3.  Open the related reservation record, which is the parent reservation:

    1.  Select the information \(![Info icon](../../wsd-reservation-management/image/info-icon.png)\) icon next to the **Reservation** field.

    2.  Select **Open Record** for the desired request.

4.  On the reservation form, review the reservation details such as the workplace location being requested, the start and end dates, and the number of reservations confirmed for that period.

    From these details, you can review the number of days, with their dates, that are missing a reservation for the employee for the requested location.

5.  If any dates are missing a reservation for the requested location, adjust the pending request to assign a workplace for all the missing desired dates.

    -   Change the workplace location in the parent reservation to a workplace available for all dates, which will also update the location for all applicable future child reservations.
        1.  Select a different location from the **Workplace location** field.
        2.  Select **Update**.
    -   Create a child reservation for a new workplace location for this employee for specific dates that are missing a reservation.
        1.  In the Reservations related list, select **New**.
        2.  Select the start and end dates in the **Start** and **End** fields.
        3.  Select a location from the **Workplace location** field.

            The list of spaces displays the locations that are available for the requested dates.

        4.  Select **Submit**.
6.  After all the days that were missing a reservation are addressed, update the status of the pending workplace task to **Closed complete**.

7.  Repeat this process for all pending workplace requests that you want to address.


## Result

Once the status of workplace request is updated to **Closed complete**, the reservation information is populated in the **Notes** field of the workplace request.

**Parent Topic:**[Managing workplace reservations for employees](../concept/managing-workplace-reservations-wsd.md)

