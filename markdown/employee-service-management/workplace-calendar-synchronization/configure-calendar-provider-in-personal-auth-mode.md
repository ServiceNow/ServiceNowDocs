---
title: Configure Microsoft Exchange Online calendar provider in personal authentication mode
description: Enhance your workplace reservation experience with the Workplace Calendar Synchronization application to synchronize reservations with your calendar provider. Configure Microsoft Exchange Online to synchronize reservations with your calendar provider using personal authentication mode. The Workplace Calendar Synchronization application uses the calendar provider as the primary source, ensuring events are updated and confirmed for room bookings through the Workplace Reservation Management portal.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-11-29"
reading_time_minutes: 3
breadcrumb: [Create a personal authentication mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Exchange Online calendar provider in personal authentication mode

Enhance your workplace reservation experience with the Workplace Calendar Synchronization application to synchronize reservations with your calendar provider. Configure Microsoft Exchange Online to synchronize reservations with your calendar provider using personal authentication mode. The Workplace Calendar Synchronization application uses the calendar provider as the primary source, ensuring events are updated and confirmed for room bookings through the Workplace Reservation Management portal.

## Before you begin

Ensure the following:

-   As a personal authentication mode user, you must have a valid mailbox in the Microsoft Exchange Online. The user is identified by the email address. The same email address must be specified in the delegated user email address where it’s necessary.

Ensure that the application scope is set to **Workplace Calendar Synchronization**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center home page.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Workplace Calendar Synchronization**.
4.  Refresh the page.

**Note:** For calendars to synchronize successfully, you must have an email address that matches that of the provider.

Role required: sn\_wsd\_rsvsync.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Calendar Providers**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_o1q_frp_5nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the calendar provider.

</td></tr><tr><td>

Description

</td><td>

Description of the calendar provider.

</td></tr><tr><td>

Active

</td><td>

Option to activate the calendar provider.

</td></tr><tr><td colspan="2">

**Provider Configuration**

</td></tr><tr><td>

Calendar processor

</td><td>

Calendar processor for the synchronization. Select **Microsoft Graph**.

</td></tr><tr><td>

Override alias?

</td><td>

Option to enable selection of your own connection and credential alias. If the option isn’t enabled, then the default connection and credential alias are used.

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Select the connection and credential alias that you created on your own for the calendar provider. This option appears only if you have selected the **Override alias?** option. If an alias isn’t specified, then the default connection and credential alias are used.

</td></tr><tr><td>

Sync start date time

</td><td>

The start date and time of the synchronization. The synchronization generates information from this date. Specify the **Sync start date time** manually from the subscription record of the reservable sync record for which you’re syncing the past reservations.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Sync end date time

</td><td>

End date and time of the synchronization. The sync generates information until this date. The recommended setting is at least 5 years from the **Sync start date time**.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Delegated user email

</td><td>

Delegated user email address that is used to create reservations and to receive updates on room calendars as notifications.**Note:** If multiple delegated users manage multiple rooms, a separate calendar provider record must be created for each user to manage their respective rooms. This process requires retrieving individual tokens for each user, creating separate connections and credential aliases, and mapping them to the respective calendar provider.

</td></tr></tbody>
</table>    **Note:** The Strict mode field is deprecated and you must set the Exchange Online Sync Integration Mode property to Strict, Personal, or Normal mode. Additionally, the strict mode email has been updated to Delegated user email.

4.  Select **Submit**.


## What to do next

To access resource calendars and generate a subscription ID, you must add a Reservable Sync Configuration. For more information, see [Add a Reservable Sync Configuration](add-reservable-sync-config.md).

**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

**Related topics**  


[Run Instance scan to check Microsoft Exchange Online synchronization configuration](run-instance-scan-on-your-workplace-cal-sync-configs.md)

