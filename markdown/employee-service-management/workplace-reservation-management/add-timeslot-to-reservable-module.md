---
title: Add a time slot to a reservable module
description: After you create a time slot, assign the time slot to a reservable module that is configured for reservation on the Quick Reservation widget. When an employee wants to reserve a workplace item of this reservable module, the employee can select a time slot for reservation.
locale: en-US
release: xanadu
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a quick reservation time slot, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Add a time slot to a reservable module

After you create a time slot, assign the time slot to a reservable module that is configured for reservation on the Quick Reservation widget. When an employee wants to reserve a workplace item of this reservable module, the employee can select a time slot for reservation.

## Before you begin

[Create a quick reservation time slot](add-reservable-time-slots.md).

Role required: sn\_wsd\_rsv.admin

## About this task

After you create a time slot, you must assign the time slot to the reservable module to make it available for reservation.

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Module**.

2.  Select the reservable module to which you want to add a time slot.

3.  On the form, scroll down to the Time Slots related list.

4.  Click **Edit...**.

5.  On the Edit members form, set the filter option **Active** to **True**.

6.  Select the time slot by doing the following:

    1.  Select the time slot from the **Collection** column on the left.

    2.  Move the selection to the **Time Slots List** column on the right.

        To move the time slot, use the add/remove icon \(![Add remove time slot icon](../image/add-remove-icon.png)\).

    3.  Click **Save**.


## Result

The time slot is added to the reservable module. When an employee uses the Quick Reservation widget to reserve a workplace item of this reservable module, the time slot is displayed.

**Important:** When the reservable module is configured, the minimum and maximum duration set to 4 and 8 hours are not validated it impacts quick reservation.

**Parent Topic:**[Create a quick reservation time slot](add-reservable-time-slots.md)

