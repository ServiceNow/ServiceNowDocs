---
title: Configure Microsoft Exchange On-Premises as calendar provider in strict mode
description: Configure Microsoft Exchange On-Premises as calendar provider in strict mode to sync reservations. Specify your strict mode setting and the strict mode email address.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create a strict mode connection for Microsoft Exchange On-Premises, Microsoft Exchange On-Premises - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Exchange On-Premises as calendar provider in strict mode

Configure Microsoft Exchange On-Premises as calendar provider in strict mode to sync reservations. Specify your strict mode setting and the strict mode email address.

## Before you begin

[Create a strict mode Connection and credential alias for Microsoft Exchange On-Premises](create-connection-credential-alias-for-exchange-on-prem-in-strict-mode.md)

**Note:** For calendars to synchronize successfully, you must have an email address that matches that of the provider.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configurations** &gt; **Calendar Providers**.

2.  Select **New**.

3.  Fill in the form fields.

<table id="table_p1m_wdv_txb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the provider. For example: On Premises

</td></tr><tr><td>

Description

</td><td>

Enter a short description.

</td></tr><tr><td>

Active

</td><td>

Option to activate the On-premises calendar provider.

</td></tr><tr><td colspan="2">

**Provider Configuration**

</td></tr><tr><td>

Calendar processor

</td><td>

Calendar processor for the synchronization. Select **Microsoft EWS** as the processor.

</td></tr><tr><td>

Override alias?

</td><td>

Option to enable selection of your own connection and credential alias. If the option is not enabled, then the default connection and credential alias is used.

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Select the connection and credential alias that you created on your own for the calendar provider. This option appears only if you have selected the **Override alias?** option. If an alias is not specified, then the default connection and credential alias is used.

</td></tr><tr><td>

Page size

</td><td>

Page size of the calendar items. You can set the page size from 1 to 500.

</td></tr><tr><td>

Sync batch size

</td><td>

Size of batches during a synchronization. This field is automatically set to **500**, which means a sync batch handles 500 items at a time. If there are more than 500 items, the rest is displayed in the next sync batch.

</td></tr><tr><td>

Sync batch interval

</td><td>

Time interval between sync batches. This field is automatically set to **60** seconds.

</td></tr><tr><td>

Synchronize attendees

</td><td>

Enable this option to synchronize attendees as well while synchronizing reservations.

</td></tr><tr><td>

Sync start date time

</td><td>

The start date and time of the synchronization. The sync generates information from this date.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Sync end date time

</td><td>

End date and time of the synchronization. The sync generates information until this date. The recommended setting is at least 5 years from the **Sync start date time**.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Strict mode

</td><td>

Select the option to enable strict mode.If you enable this option, events are not directly created in the employee's calendar, instead, they are sent to a general email address. Employees are invited to the event. They can only make changes using the Workplace Reservation Management application.

</td></tr><tr><td>

Strict mode email

</td><td>

Strict mode email address used to create reservations and to receive reservation-related notifications. Employees are considered as invitees in the reservation.

</td></tr><tr><td>

Sync past reservations

</td><td>

Select the option to synchronize all the past reservations from the specified **Sync start date time** to **Sync end date time**.**Note:** Ensure that the reservations that you want to sync from the past are not above 1000 per room. If in cases the expected number of past events are more than 1000, it is recommended to modify the system property **sn\_wsd\_rsvsync.ewsPastSyncPeriodInMonths**. Specify the value in months keeping in mind the expected past reservations. A single sync syncs reservations from those many months. Ensure that the specified number of months do not have more than 1000 reservations.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The On-premises calendar provider is created.

5.  In the Reservable Sync Configurations related list, add the reservable sync configurations with which you want to synchronize reservations.

    To add a new one, refer to [Add a Reservable Sync Configuration](add-reservable-sync-config.md).


## What to do next

-   Set the scheduled job, **WSDRS Sync Calendar items** to **True**. The scheduled job is set to **False** by default and it must be enabled to start synchronizing. You can set the scheduled job time as you want. At any time, you can also manually execute it.
-   [Add a Reservable Sync Configuration](add-reservable-sync-config.md)

**Parent Topic:**[Create a strict mode connection for Microsoft Exchange On-Premises](../concept/create-a-strict-mode-connection-for-onprem.md)

**Previous topic:**[Create a strict mode Connection and credential alias for Microsoft Exchange On-Premises](create-connection-credential-alias-for-exchange-on-prem-in-strict-mode.md)

**Next topic:**[Create single or multiple providers with Microsoft Exchange On-Premises](create-multi-provider-connection-with-onprem.md)

