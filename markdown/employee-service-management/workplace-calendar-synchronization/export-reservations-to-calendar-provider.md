---
title: Export reservations to the calendar provider
description: As a one time procedure, export all your confirmed reservations to your calendar provider for synchronization.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Export reservations to the calendar provider

As a one time procedure, export all your confirmed reservations to your calendar provider for synchronization.

## Before you begin

You must have the Workplace Reservation Management application installed.

Role required: admin

## About this task

If you have installed Workplace Calendar Synchronization after using Workplace Reservation Management for a long time, run the export scheduled job to export all your confirmed present and future reservations to your calendar provider. During the export, for every 45 seconds, the scheduled job exports 10 reservations to the calendar.

The export runs based on the following conditions:

-   The reservations made on the past date are not exported. Only the reservations that are on the current date and future dates are exported.
-   Only the reservations that are in confirmed state are exported.
-   Only the reservations made on spaces and rooms that have Reservable sync configuration are exported. For more information on how to add a Reservable sync configuration for a room or a space, refer to [Add multiple Reservable Sync Configurations](add-reservable-sync-config.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Scheduled jobs**.

2.  Select **Export reservations to calendar** scheduled job.

3.  Select the **Active** field to activate the scheduled job.

4.  Click **Update**.

    The export process is initiated.


## Result

The export process runs in the background. For every 45 seconds, 10 reservations are exported to the calendar.

**Note:** The application will not send any notification when the export process is complete and if any reservation is not exported.

