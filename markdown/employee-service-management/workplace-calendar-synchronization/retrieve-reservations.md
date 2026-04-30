---
title: Retrieve reservations
description: Retrieves all the events for active reservable sync configurations from Microsoft Outlook to Workplace Service Delivery.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Retrieve reservations

Retrieves all the events for active reservable sync configurations from Microsoft Outlook to Workplace Service Delivery.

## Before you begin

Role required: sn\_wsd\_rsvsync admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Calendar Providers**.

2.  Select the calendar provider for which you want to retrieve reservations from the **Retrieve reservations**.

3.  On the Provider form, select **Retrieve reservations**.

    **Note:** The **sync start date time** is the current time and the **sync end date time** is the time taken to complete the synchronization.

4.  Select **Confirm**.

    **On demand sync execution** record for active **Reservable sync configurations** is generated.

    **Note:** **On demand sync execution** record is generated at provider level. You can click the active resource separately to generate an on demand sync record.

5.  Click the **On demand sync executions** record.

    It displays all the resources to be synced.

6.  Click **Sync execution for reservable sync configuration**, and check whether the **State** is turned to **Success**.


## Result

There is another table called Sync execution for **Reservable sync configuration spoke events** where all the events for the active **Reservable sync config** are displayed.

**Parent Topic:**[Setup Workplace Calendar Synchronization](../concept/workplace-calendar-synchronization-setup.md)

**Related topics**  


[Set Workplace Calendar Synchronization properties](set-calendar-sync-properties.md)

[Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md)

[Google Calendar - Calendar synchronization](../reference/google-calendar-calendar-synchronization.md)

[Microsoft Exchange On-Premises - Calendar synchronization](../reference/ms-exchange-on-prem-calendar-synchronization.md)

[Add a Reservable Sync Configuration](add-reservable-sync-config.md)

[No request handling](no-request-handling.md)

[Synchronize past reservations](sync-past-reservation.md)

[Export reservations to the calendar provider](export-reservations-to-calendar-provider.md)

