---
title: Reservation Waitlist data model
description: The Reservation Waitlist data model describes the tables and configuration options that support waitlist requests, space allocation, and reservation fulfillment for employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-reservation-management/waitlist-configuration.html
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 4
breadcrumb: [Manage and configure reservation waitlist, Manage employee reservations, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Reservation Waitlist data model

The Reservation Waitlist data model describes the tables and configuration options that support waitlist requests, space allocation, and reservation fulfillment for employees.

## Reservation Waiting Lists

The Reservation Waiting Lists table \(sn\_wsd\_rsv\_waitlist\) is updated with **Neighborhood**, **Reservable Module**, and **Fulfilled by** columns for manual event planner fulfillment. Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Reservation Overview** &gt; **My Waiting List**.

\[Omitted image "waitlist-list-reservable-module-record.png"\] Alt text: Reservation waiting list table showing the Reservable module configuration, status, and priority.

Status: The waitlist **Status** column is updated with the following values:

-   Queued: When an employee submits a waitlist request, the system creates a record in the Reservation Waitlist \[sn\_wsd\_rsv\_waitlist\] table with the status set to **Queued**
-   Confirmed: The queued waitlist request is approved or fulfilled, a space is assigned for reservation, and the status changes from **Queued** to **Confirmed**.
-   Expired: Stale or past waitlist records are removed by the nightly **Waitlist Expiration** scheduled job. The scheduled job identifies waitlist records in **Queued** state. The scheduled job detects past or stale timestamps for waitlist records. Waitlist records with a past start time are set to **Expired**. Expired records are retained for 30 days before being permanently purged.

    For more information, see [Create a schedule job for waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/schedule-job-waitlist.md).

-   Canceled: An employee or the Reservation Event Planner cancels a Queued waitlist record. The status changes from **Queued** to **Canceled**.

## Workplace Reservation

The Workplace Reservation Table \(sn\_wsd\_rsv\_reservation\) is updated with Waitlist origin column. By default, the value in this column is set to **False**. When a Queued waitlist record is fulfilled and confirmed, a space is assigned and a reservation is created. When a reservation record is created, the Waitlist origin column value changes to **True**. This column shows how many waitlist records are fulfilled, supporting waitlist management.

\[Omitted image "waitlist-origin-table-configuration.png"\] Alt text: Workplace Reservations table showing the Waitlist origin column.

-   Reservable Module Record: Workplace users can join a waitlist only for a reservable module — for example, desks or meeting rooms. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).
-   Neighborhood: Workplace users can also waitlist on a neighborhood so that preferred neighborhood space allocation is done when the space is free and available for reservation.
-   Weight \(Priority\): Only event planners can update the weight of a queued waitlist record. Records with the highest weight move to the top of the queue and are allocated a space first. For more information, see [Manage reservation waitlist records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/rsv-planner-subscribe-waitlist.md).
-   Created: If no weight value is set, space allocation follows first-in, first-out \(FIFO\) logic based on the date and time the waitlist record was created. Records with an earlier start time are prioritized.
-   Fulfilled by: The **Fulfilled by** column value is updated only when a Workplace Reservation Event Planner manually assigns a space to an employee whose waitlist is in a Queued state. For more information, see [Manage reservation waitlist records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/rsv-planner-subscribe-waitlist.md).

## Reservable Module Configuration

The following configuration options must be enabled in the Reservable Module Configuration for employees to join a waitlist. For more information, see [Configure a reservable module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/config-reservable-module.md).

-   Enable Waitlist: When selected, enables employees to join a waitlist.
-   Enable browse by Neighborhood: When selected, enables employees to join a waitlist for a neighborhood space and have a preferred neighborhood space assigned when one is available.

    For more information, see [Create a reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-rsv-waitlist.md).


**Parent Topic:**[Manage and configure reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/subscribe-waitlist-overview.md)

**Previous topic:**[Manage and configure reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/subscribe-waitlist-overview.md)

**Next topic:**[Create a reservation waitlist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-reservation-management/create-rsv-waitlist.md)

