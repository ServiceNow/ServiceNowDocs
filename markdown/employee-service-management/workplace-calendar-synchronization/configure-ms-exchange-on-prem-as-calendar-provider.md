---
title: Configure Microsoft Exchange On-Premises as calendar provider
description: Set Microsoft Exchange On-Premises as calendar provider to sync reservations. Specify the calendar processor, the sync-related settings, and strict mode preference.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create a normal mode connection, Microsoft Exchange On-Premises - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Exchange On-Premises as calendar provider

Set Microsoft Exchange On-Premises as calendar provider to sync reservations. Specify the calendar processor, the sync-related settings, and strict mode preference.

## Before you begin

**Note:** For calendars to synchronize successfully, you must have an email address that matches that of the provider.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configurations** &gt; **Calendar Providers**.

2.  Select **New**.

3.  On the form fill in the fields.

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

</td></tr><tr><td>

Calendar processor

</td><td>

Calendar processor for the synchronization. Select **Microsoft EWS** as the processor in **Provider Configuration**.

</td></tr><tr><td>

Override alias?

</td><td>

Option to enable selection of your own connection and credential alias in **Provider Configuration**. If the option is not enabled, the default connection and credential alias is used.

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Fro **Provider Configuration**, select the connection and credential alias that you created on your own for the calendar provider. This option appears only if you have selected the **Override alias?** option. If an alias is not specified, then the default connection and credential alias is used.

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

Sync past reservations

</td><td>

Select the option to synchronize all the past reservations from the specified **Sync start date time** to the **Sync end date time**.**Note:** Ensure that the reservations that you want to sync from the past are not above 1000 per room. If in cases the expected number of past events are more than 1000, it is recommended to modify the system property **sn\_wsd\_rsvsync.ewsPastSyncPeriodInMonths**. Specify the value in months keeping in mind the expected past reservations. A single sync syncs reservations from those many months. Ensure that the specified number of months do not have more than 1000 reservations per room.

</td></tr><tr><td>

Delegated user email

</td><td>

Delegated user email address that is used to create reservations and to receive updates on room calendars as notifications.**Note:** If multiple delegated users manage multiple rooms, a separate calendar provider record must be created for each user to manage their respective rooms. This requires retrieving individual tokens for each user, creating separate connections and credential aliases, and mapping them to the respective calendar provider.

</td></tr></tbody>
</table>    **Note:** The Strict mode field is deprecated and the user must set the Exchange Online Sync Integration Mode property to Strict, Personal, or Normal mode. Additionally, the strict mode email has been updated to Delegated user email.

4.  Select **Submit**.

    The On-premises calendar provider is created.

5.  In the Reservable Sync Configurations related list, add the reservable sync configurations with which you want to synchronize reservations.

    To add a new one, refer to [Add multiple Reservable Sync Configurations](add-reservable-sync-config.md).


## What to do next

-   Set the scheduled job, **WSDRS Sync Calendar items** to **True**. The scheduled job is set to **False** by default and it must be enabled to start synchronizing. You can set the scheduled job time as you want. At any time, you can also manually execute it.
-   [Add multiple Reservable Sync Configurations](add-reservable-sync-config.md)

