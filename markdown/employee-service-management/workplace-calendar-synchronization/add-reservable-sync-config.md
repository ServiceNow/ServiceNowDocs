---
title: Add a Reservable Sync Configuration
description: Add workplace-workspace/desk \(or\) rooms that must be synchronized with the calendar provider whenever an employee makes a reservation.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Add a Reservable Sync Configuration

Add workplace-workspace/desk \(or\) rooms that must be synchronized with the calendar provider whenever an employee makes a reservation.

## Before you begin

Refer to [Explore Workplace Calendar Synchronization](../concept/workplace-calendar-synchronization-overview.md).

Role required: sn\_wsd\_rsvsync.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Reservable Sync Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_el5_gnj_vnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Location

</td><td>

Workplace item that you want to synchronize with the calendar provider whenever an employee makes a reservation. For example, this field can be the location of a meeting room, conference room, or board room.

</td></tr><tr><td>

Reservable module

</td><td>

The reservable module, which contains the workplace item.

</td></tr><tr><td>

Email

</td><td>

The email address of the workplace room/space, such as for a meeting room or conference room. The email address is used to check calendar statuses and events. **Important:** The **Email** field will not be auto-populated with the email address that is specified in the room/space configuration form.

 After you specify the email address and save the form, the following actions are performed:

-   If there is no email address specified on the room/space configuration form, then the **Email** field of the room/space configuration form is auto-filled with the email address that you specified here.
-   If an email address is specified on the room/space configuration form, and it does not match the email address that you specified here, an error is displayed.


</td></tr><tr><td>

Active

</td><td>

Option to activate the workplace item for synchronization.**Important:** The **Active** field is read-only and inactive if you are adding the reservable sync config record to the Microsoft Exchange Online or Microsoft Exchange On-Premises calendar provider. To activate the reservable sync config record, you must select the **Activate** option after you save the form.

</td></tr><tr><td colspan="2">

**Provider Configuration**

</td></tr><tr><td>

Provider

</td><td>

Calendar provider that you want to synchronize with the workplace item.

</td></tr><tr><td>

No request

</td><td>

Option to test synchronization. Select this option to test if a reservation is synchronized or not when the workplace item is active. Validate the configuration and events to ensure that everything is set up correctly. Selecting this option will only generate events and not send them to the calendar service.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The workplace item is added.

**Important:** If you are adding the reservable sync config record to the Microsoft Exchange Online calendar provider, the reservable sync config record will be de-activate after creation. To activate the reservable sync record, you must select the **Activate** option on that reservable sync config record form.

**Note:** When a Reservable Sync configuration is changed or updated, the synchronization deltas \(Sync delta\) are cleared from the application.

-   **[Activate or deactivate a Reservable sync configuration](activate-or-deactivate-a-reservable-sync-configuration.md)**  
You can activate or deactivate a reservable sync configuration if it is not required at any time.

**Parent Topic:**[Setup Workplace Calendar Synchronization](../concept/workplace-calendar-synchronization-setup.md)

**Related topics**  


[Set Workplace Calendar Synchronization properties](set-calendar-sync-properties.md)

[Microsoft Exchange Online - Calendar synchronization](../reference/ms-exchange-reservation-synchronization.md)

[Google Calendar - Calendar synchronization](../reference/google-calendar-calendar-synchronization.md)

[Microsoft Exchange On-Premises - Calendar synchronization](../reference/ms-exchange-on-prem-calendar-synchronization.md)

[No request handling](no-request-handling.md)

[Synchronize past reservations](sync-past-reservation.md)

[Retrieve reservations](retrieve-reservations.md)

[Export reservations to the calendar provider](export-reservations-to-calendar-provider.md)

