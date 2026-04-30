---
title: No request handling
description: Make a 'No request' call to test the configuration with the calendar provider.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# No request handling

Make a 'No request' call to test the configuration with the calendar provider.

## Before you begin

Role required: admin

## About this task

No request is a mechanism to validate the generated syntax of the payload of an event created for the calendar. But, instead of sending the event to the calendar provider, it is only created. The admin can validate the payload content of the event \(JSON\) to ensure that is generated as expected. 'No request' ensures that the application does not make any API calls to the calendar provider when you create, update, or cancel a reservation in the Workplace Reservation Management application.

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Reservable Sync Configuration**.

2.  Select the reservable sync record for which you want to enable 'No request.

3.  On the form, ensure that the **Active** option is enabled.

4.  Enable the **No request** option.

5.  Select **Update**.


**Parent Topic:**[Setup Workplace Calendar Synchronization](../concept/workplace-calendar-synchronization-setup.md)

**Related topics**  


[Set Workplace Calendar Synchronization properties](set-calendar-sync-properties.md)

[Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md)

[Google Calendar - Calendar synchronization](../reference/google-calendar-calendar-synchronization.md)

[Microsoft Exchange On-Premises - Calendar synchronization](../reference/ms-exchange-on-prem-calendar-synchronization.md)

[Add a Reservable Sync Configuration](add-reservable-sync-config.md)

[Synchronize past reservations](sync-past-reservation.md)

[Retrieve reservations](retrieve-reservations.md)

[Export reservations to the calendar provider](export-reservations-to-calendar-provider.md)

