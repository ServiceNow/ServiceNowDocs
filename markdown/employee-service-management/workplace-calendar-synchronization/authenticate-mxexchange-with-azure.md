---
title: Configure Microsoft Azure in normal mode
description: Set up a normal mode authentication with Microsoft Azure to connect Microsoft Exchange Online with Workplace Calendar Synchronization.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a normal mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Azure in normal mode

Set up a normal mode authentication with Microsoft Azure to connect Microsoft Exchange Online with Workplace Calendar Synchronization.

## Before you begin

Role required: Exchange administrator

## About this task

Add normal mode permissions so that you can synchronize Workplace Calendar Synchronization with Microsoft Exchange Online via GraphAPI.

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  If you do not have an app registration, select **New registration**.

    1.  On the form, enter the **Name** of the registration.

    2.  Select the **Supported account types** of your choice.

    3.  Specify the **Redirect URL**.

        Specify the following details:

        1.  Select the platform as **Web**.
        2.  Enter the URL in the following format: https://&lt;instance-Name&gt;.service-now.com/oauth\_redirect.do
4.  If you already have an app registration, select the app registration.

    1.  Navigate to **Manage** &gt; **Authentication**.

    2.  Navigate to **Add a platform** &gt; **Web applications** &gt; **Web**.

    3.  On the Configure Web form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |Redirect URL|Enter a URL in the format: https://\[instance\].service-now.com/oauth\_redirect.do|
        |Implicit grant|Check **Access tokens**, and **ID tokens**|

    4.  Select **Configure**.

5.  Add a client secret.

    1.  Navigate to **Manage** &gt; **Certificates and secrets**.

    2.  In the **Description** field, enter a short description about the secret.

    3.  Under **Expires**, select an expiry.

    4.  Select **Add**.

    5.  After adding, in the Client secrets section, copy the value by selecting **Copy to clipboard**.

6.  Add a permission.

    1.  Navigate to **Manage** &gt; **API permissions**.

    2.  Select **Add a permission**.

    3.  Select **Microsoft Graph**.

    4.  Select **Application permissions**.

    5.  Under **Calendars**, select **Calendars.ReadWrite**.

    6.  Select **Add permissions**.

    7.  On the Configured permissions screen, select **Grant admin consent for ServiceNow**.


## Result

The Microsoft Exchange Online is set up with Microsoft Azure.

## What to do next

Configure resources Microsoft Exchange Online in the calendar. For more information, refer to [https://learn.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-resource-mailboxes](https://learn.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-resource-mailboxes).

**Parent Topic:**[Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md)

**Related topics**  


[Create a connection with Microsoft Exchange Online spoke](create-connection-with-msspoke.md)

[Set up OAuth connection with Microsoft Exchange Online](setup-connectivity-with-msexchange-for-calendar-sync.md)

[Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections](create-connection-and-credential-alias-for-msexchange-.md)

[Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md)

[Configure Microsoft Exchange Online calendar provider](configure-xsex-calendar-provider-in-normal-mode.md)

