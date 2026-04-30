---
title: Set Workplace Calendar Synchronization properties
description: Configure the properties for the Workplace Calendar Synchronization to set the Exchange Online Sync Integration Mode to Strict, Personal Authentication, or Normal mode to synchronize reservations.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-11-28"
reading_time_minutes: 2
breadcrumb: [Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Set Workplace Calendar Synchronization properties

Configure the properties for the Workplace Calendar Synchronization to set the Exchange Online Sync Integration Mode to Strict, Personal Authentication, or Normal mode to synchronize reservations.

## Before you begin

Role required: sn\_wsd\_rsvsync.admin

**Note:** The Exchange Online Sync Integration Mode property isn’t supported for Google Calendar.

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Properties**.

2.  Set the Exchange Online Sync Integration Mode property value to any of the following:

<table id="table_ww2_t1m_sdc"><thead><tr><th>

Mode

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Strict

</td><td>

To use strict mode user to manage all reservations in Outlook using an authorization code, set up Strict mode authentication to connect Microsoft Exchange Online with Workplace Calendar Synchronization.

</td></tr><tr><td>

Personal

</td><td>

To manage a user's own reservations in Outlook using their personal token, configure the connections and settings with Microsoft Exchange Online in Personal Authentication mode. This process ensures synchronization of reservations and restricts unauthorized access to the user's calendar.**Note:** This property isn’t supported for Google Calendar and Microsoft Exchange On-Premises.

</td></tr><tr><td>

Normal

</td><td>

To manage all reservations in Outlook using admin client credentials, set up a Normal mode authentication to connect Microsoft Exchange Online with Workplace Calendar Synchronization.

</td></tr></tbody>
</table>3.  Select **Save**.


**Parent Topic:**[Setup Workplace Calendar Synchronization](../concept/workplace-calendar-synchronization-setup.md)

**Related topics**  


[Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md)

[Google Calendar - Calendar synchronization](../reference/google-calendar-calendar-synchronization.md)

[Microsoft Exchange On-Premises - Calendar synchronization](../reference/ms-exchange-on-prem-calendar-synchronization.md)

[Add a Reservable Sync Configuration](add-reservable-sync-config.md)

[No request handling](no-request-handling.md)

[Synchronize past reservations](sync-past-reservation.md)

[Retrieve reservations](retrieve-reservations.md)

[Export reservations to the calendar provider](export-reservations-to-calendar-provider.md)

