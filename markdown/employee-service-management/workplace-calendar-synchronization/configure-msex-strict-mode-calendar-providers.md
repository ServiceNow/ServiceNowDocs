---
title: Configure Microsoft Exchange Online calendar provider in strict mode
description: Configure Microsoft Exchange Online as a calendar provider in strict mode to synchronize reservations.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create a strict mode connection, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Exchange Online calendar provider in strict mode

Configure Microsoft Exchange Online as a calendar provider in strict mode to synchronize reservations.

## Before you begin

Ensure the following:

-   As a delegated user, you must have valid mailbox in the Microsoft Exchange Online. The user is identified by the email address. The same email address must be specified in the delegated user email address where it is necessary.
-   Configure strict mode Connection and Credential alias for Microsoft Exchange Online. If you want to use your own alias, then refer to [Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md).

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

**Note:** For calendars to synchronize successfully, you must have an email address that matches that of the provider.

Role required: admin

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

Name of the calendar service. For example, Microsoft Exchange Strict mode

</td></tr><tr><td>

Description

</td><td>

Description of the calendar service.

</td></tr><tr><td>

Active

</td><td>

Option to activate the calendar provider.

</td></tr><tr><td>

Calendar processor

</td><td>

Calendar processor for the synchronization. Select **Microsoft Graph**.

</td></tr><tr><td>

Override alias?

</td><td>

Option to enable selection of your own connection and credential alias from **Provider Configuration**. If the option is not enabled, then the default connection and credential alias is used.

</td></tr><tr><td>

Connection &amp; credential alias

</td><td>

Select the connection and credential alias that you created on your own for the calendar provider from **Provider Configuration**. This option appears only if you have selected the **Override alias?** option. If an alias is not specified, then the default connection and credential alias is used.

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

Select the option to synchronize all the past reservations from the specified **Sync start date time** to the **Sync end date time**.

</td></tr><tr><td>

Delegated user email

</td><td>

Delegated user email address that is used to create reservations and to receive reservation-related notifications. Employees are considered as invitees in the reservation.

</td></tr></tbody>
</table>    **Note:** The Strict mode field is deprecated and the user must set the Exchange Online Sync Integration Mode property to Strict, Personal, or Normal mode. Additionally, the strict mode email has been updated to Delegated user email.

4.  Select **Submit**.


## Result

The calendar provider is added.

**Warning:** Reservations that are created using calendar providers cannot be edited in the Workplace Reservation Management application.

## What to do next

Run Instance scan to check Microsoft Exchange Online synchronization configuration. For more information, see [Run Instance scan to check Microsoft Exchange Online synchronization configuration](run-instance-scan-on-your-workplace-cal-sync-configs.md).

**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](auth-mxex-with-azure-strict-mode.md)

[Create connection with Microsoft Exchange Online Spoke in strict mode](create-connection-with-msspoke-strict-mode.md)

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

[Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md)

[Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md)

