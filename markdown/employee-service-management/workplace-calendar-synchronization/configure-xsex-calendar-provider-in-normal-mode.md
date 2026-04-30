---
title: Configure Microsoft Exchange Online calendar provider
description: Configure Microsoft Exchange Online as a calendar provider in normal mode to synchronize reservations.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Create a normal mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Exchange Online calendar provider

Configure Microsoft Exchange Online as a calendar provider in normal mode to synchronize reservations.

## Before you begin

**Important:** If you do not want to use the default alias provided by the application for the calendar provider, you can create your own connection and credential alias. Refer to [Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md).

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

**Note:** For calendars to synchronize successfully, you must have an email address that matches that of the provider.

Role required: admin

## About this task

Configure Microsoft Exchange Online as calendar provider. If you want to specify your own alias, then enable the **Override alias** option. To create your own alias, refer to [Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md).

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

Name of the calendar provider. For example, Microsoft Exchange.

</td></tr><tr><td>

Description

</td><td>

Description of the calendar service.

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

Option to enable selection of your own connection and credential alias. If the option is not enabled, then the default connection and credential alias is used.

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Select the connection and credential alias that you created on your own for the calendar provider. This option appears only if you have selected the **Override alias?** option. If an alias is not specified, then the default connection and credential alias is used.

</td></tr><tr><td>

Sync start date time

</td><td>

The start date and time of the synchronization. The sync generates information from this date. Specify the **Sync start date time** manually from the subscription record of the reservable sync record for which you are syncing the past reservations.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Sync end date time

</td><td>

End date and time of the synchronization. The sync generates information until this date. The recommended setting is at least 5 years from the **Sync start date time**.**Important:** The past sync duration must not exceed 1825 days.

</td></tr><tr><td>

Sync past reservations

</td><td>

Select the option to synchronize all the past reservations from the specified **Sync start date time** to the **Sync end date time**. You can configure the setting using the **Synchronize past reservations**.

</td></tr><tr><td>

Delegated user email

</td><td>

Delegated user email address that is used to create reservations and to receive updates on room calendars as notifications.**Note:** If multiple delegated users manage multiple rooms, a separate calendar provider record must be created for each user to manage their respective rooms. This requires retrieving individual tokens for each user, creating separate connections and credential aliases, and mapping them to the respective calendar provider.

</td></tr></tbody>
</table>    **Note:** The Strict mode field is deprecated and the user must set the Exchange Online Sync Integration Mode property to Strict, Personal, or Normal mode. Additionally, the strict mode email has been updated to Delegated user email.

4.  Select **Submit**.


## Result

The calendar provider is added.

**Warning:** Reservations that are created using calendar providers cannot be edited in the Workplace Reservation Management application.

## What to do next

Run Instance scan to check Microsoft Exchange Online synchronization configuration. For more information, see [Run Instance scan to check Microsoft Exchange Online synchronization configuration](run-instance-scan-on-your-workplace-cal-sync-configs.md).

**Parent Topic:**[Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md)

**Related topics**  


[Configure Microsoft Azure in normal mode](authenticate-mxexchange-with-azure.md)

[Create a connection with Microsoft Exchange Online spoke](create-connection-with-msspoke.md)

[Set up OAuth connection with Microsoft Exchange Online](setup-connectivity-with-msexchange-for-calendar-sync.md)

[Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections](create-connection-and-credential-alias-for-msexchange-.md)

[Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md)

