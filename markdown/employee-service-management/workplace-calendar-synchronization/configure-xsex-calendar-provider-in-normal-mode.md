---
title: Configure Microsoft Exchange Online calendar provider
description: Configure Microsoft Exchange Online as a calendar provider in normal mode to synchronize reservations.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create a normal mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Exchange Online calendar provider

Configure Microsoft Exchange Online as a calendar provider in normal mode to synchronize reservations.

## Before you begin

**Important:** If you do not want to use the default alias provided by the application for the calendar provider, you can create your own connection and credential alias. Refer to [Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md).

[Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections](create-connection-and-credential-alias-for-msexchange-.md). If you do not want to use the default alias then create your own alias. Refer to [Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md).

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

Strict mode

</td><td>

Don't select the option.If you enable this option, events are not directly created in the employee's calendar, instead, they are sent to a general email address. Employees are invited to the event. They can only make changes using the Workplace Reservation Management application.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The calendar provider is added.

**Warning:** Reservations that are created using calendar providers cannot be edited in the Workplace Reservation Management application.

**Parent Topic:**[Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md)

**Previous topic:**[Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md)

**Next topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

