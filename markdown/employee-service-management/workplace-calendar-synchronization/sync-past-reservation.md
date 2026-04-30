---
title: Synchronize past reservations
description: Sync reservations made in the past, that is, before configuring the reservation synchronization setup.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Synchronize past reservations

Sync reservations made in the past, that is, before configuring the reservation synchronization setup.

## Before you begin

Ensure that the calendar provider is active.

**Note:** In case of Microsoft Exchange On-Premises, ensure that the reservations that you want to sync from the past are not above 1000 per room/resource. If in cases the expected number of past events are more than 1000, it is recommended to modify the system property **sn\_wsd\_rsvsync.ewsPastSyncPeriodInMonths**. Specify the value in months keeping in mind the expected past reservations. A single sync syncs reservations from those many months. Ensure that the specified number of months do not have more than 1000 reservations per room/resource.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Calendar Providers**.

2.  Select the calendar provider for which you want to synchronize past reservations.

3.  On the Provider form, ensure that the **Active** option is enabled.

4.  Enable the **Sync past reservations** field.

5.  In the **Sync start time**, specify the start time from the past from when you want to synchronize reservations.

    **Note:** For Microsoft Exchange Online calendar provider, specify the **Sync start time** manually from the subscription record of the reservable sync record for which you are synchronizing the past reservations.

6.  In the **Sync end time**, specify the end time from the past until when you want to synchronize reservations.

    **Important:** The past sync duration must not exceed 1825 days.

7.  Select **Update**.


## Result

The past reservations are synchronized.

**Parent Topic:**[Setup Workplace Calendar Synchronization](../concept/workplace-calendar-synchronization-setup.md)

**Related topics**  


[Set Workplace Calendar Synchronization properties](set-calendar-sync-properties.md)

[Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md)

[Google Calendar - Calendar synchronization](../reference/google-calendar-calendar-synchronization.md)

[Microsoft Exchange On-Premises - Calendar synchronization](../reference/ms-exchange-on-prem-calendar-synchronization.md)

[Add a Reservable Sync Configuration](add-reservable-sync-config.md)

[No request handling](no-request-handling.md)

[Retrieve reservations](retrieve-reservations.md)

[Export reservations to the calendar provider](export-reservations-to-calendar-provider.md)

