---
title: Create a quick reservation time slot
description: Create a time slot for the reservable module that is available in the Quick Reservation widget on the reservation portal. When an employee wants to reserve a workplace item of that reservable module, the employee can select a suitable time slot instead of specifying a start and end times for the reservation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/add-reservable-time-slots.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Create a quick reservation time slot

Create a time slot for the reservable module that is available in the Quick Reservation widget on the reservation portal. When an employee wants to reserve a workplace item of that reservable module, the employee can select a suitable time slot instead of specifying a start and end times for the reservation.

## Before you begin

Role required: sn\_wsd\_rsv.admin

## About this task

Create a time slot for reservation. You can specify the order of appearance of the time slot in the selection list for reservations.

**Note:** You can add a time slot only to the reservable module that is configured as available on the Quick Reservation widget.

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Time Slots**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the time slot.|
    |Short description|Short description about the time slot.|
    |Start time|Start time of the time slot.|
    |End time|End time of the time slot.|
    |Active|Option to activate the time slot.|
    |Order|Order in which the time slot is displayed in the selection list.|

4.  Click **Submit**.


## Result

The time slot is created.

## What to do next

Add the time slot to the reservable module. The time slot will be displayed in the selection list when an employee wants to reserve a workplace item from the reservable module that has this time slot. For more information, see [Add a time slot to a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/add-timeslot-to-reservable-module.md).

-   **[Add a time slot to a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/add-timeslot-to-reservable-module.md)**  
After you create a time slot, assign the time slot to a reservable module that is configured for reservation on the Quick Reservation widget. When an employee wants to reserve a workplace item of this reservable module, the employee can select a time slot for reservation.

**Parent Topic:**[Configure Workplace Reservation Management portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/wsd-reservation-setup.md)

**Related topics**  


[Install Workplace Reservation Management]()

[Add a workplace space for reservation]()

[Add a workplace room for reservation]()

[Configure a reservable module]()

[Assign spaces to an area]()

[Create a standard service]()

[Create a flexible service]()

[Create a workplace service to provide an extra service for a reservation]()

[Create a reservable view]()

[Create a user criteria record]()

[Configure a reservable purpose]()

[Configure virtual meeting providers]()

[Configure Microsoft Teams as virtual meeting provider]()

[Connect Workplace Reservation Management with Microsoft Teams]()

[Connect Workplace Reservation Management with Zoom]()

[Display permanent seat assignments on floor maps]()

[Display name of the person reserving a space]()

[Manage check-in and check-out reservations]()

[Configure automatic check-in for reserved spaces]()

[Configure reservation multi-day settings in Reservable Module]()

