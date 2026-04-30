---
title: Enable shift-based reservation
description: As an admin, enable employees to reserve a workplace item for a shift. Configure the spaces that can be reserved for a shift. Specify the users who can make shift-based reservation.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create neighborhood reservations, Reserve workplace items, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Enable shift-based reservation

As an admin, enable employees to reserve a workplace item for a shift. Configure the spaces that can be reserved for a shift. Specify the users who can make shift-based reservation.

## Before you begin

To enable shift-based reservation, select the **Apply to shift** field on the reservable module form of the workplace item.

Ensure you have the following information:

-   Appropriate shift schedules.
-   Data of the employees who would operate from the office in this shift.
-   Data of the workplace spaces to be made available for this shift.

Ensure that the **Building** field on the Shift form has a value.

Role required: sn\_wsd\_core.workplace\_manager

## Procedure

1.  Navigate to **Workplace Core** &gt; **Shift Management** &gt; **All**.

2.  Select the shift to which you want to assign spaces and users.

3.  To assign users to the shift, scroll down and click **Edit** in the Users related list.

    Only the assigned users can make reservations for this shift on the Reservation portal.

4.  On the Edit members form, add users to the shift by doing the following.

    1.  Select the users from the **Collection** column on the left.

    2.  To move the selection to the **Users List** column on the right, use the add-remove icon.

        ![Add-remove icon.](../image/add-remove-icon.png)

    3.  Click **Save**.

5.  To assign spaces to the shift, scroll down and click **Edit** in the Locations related list.

    Only the assigned spaces are displayed for shift-based reservation on the Reservation portal.

6.  On the Edit members form, add spaces to the shift by doing the following.

    1.  Select the spaces from the **Collection** column on the left.

    2.  To move the selection to the **Locations List** column on the right, use the add-remove icon.

        ![Add-remove icon.](../image/add-remove-icon.png)

    3.  Click **Save**.

7.  Click **Update**.


## Result

The users and spaces are assigned to the shift. When an employee wants to make a shift reservation, the Reservation portal displays the following information:

-   The shifts for which the employee can make a reservation.
-   The spaces that are available for reservation in the selected shift.

**Parent Topic:**[Create neighborhood reservations](create-neighborhood-reservations.md)

