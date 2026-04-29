---
title: Configure Microsoft Azure
description: Set up a personal mode of authentication with Microsoft Azure to connect Microsoft Exchange Online with Workplace Calendar Synchronization.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a personal authentication mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Azure

Set up a personal mode of authentication with Microsoft Azure to connect Microsoft Exchange Online with Workplace Calendar Synchronization.

## Before you begin

In Personal Authentication mode, a valid delegated user account with an associated email address on Microsoft Exchange Online is required. The user's identity is determined by their email address, which must also be specified in the delegated user email field, where applicable.

Role required: Exchange administrator

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Navigate to **Azure Services** &gt; **App registrations**.

3.  If you don’t have an app registration, select **New registration**.

    1.  On the form, enter the **Name** of the registration.

    2.  Select the **Supported account types** of your choice.

    3.  Specify the **Redirect URL**.

        Specify the following details:

        1.  Select the platform as **Web**.
        2.  Enter the URL in the following format:`https://<instance-Name>.service-now.com/oauth_redirect.do`
4.  If you already have an app registration, select the app registration.

    1.  Navigate to **Manage** &gt; **Authentication**.

    2.  Navigate to **Add a platform** &gt; **Web applications** &gt; **Web**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Redirect URL|Enter a URL in the format: `https://[instance].service-now.com/oauth_redirect.do`|
        |Implicit grant|Select the **Access tokens** and **ID tokens** options.|

    4.  Select **Configure**.

5.  Add a client secret.

    1.  Navigate to **Manage** &gt; **Certificates and secrets**.

    2.  In the **Description** field, enter a short description about the secret.

    3.  In the **Expires** field, select an expiry.

    4.  Select **Add**.

    5.  After adding client secret details, in the Client secrets section, copy the value by selecting **Copy to clipboard**.

6.  Add a permission.

    1.  Navigate to **Manage** &gt; **API permissions**.

    2.  Select **Add a permission**.

    3.  Select **Microsoft Graph**.

    4.  Select **Delegated permissions**.

    5.  In the **Calendars** Permission section, select **Calendars.ReadWrite**, **Calendars.ReadWrite.Shared**, and **Offline\_access**.

    6.  Select **Add permissions**.

    7.  On the Configured permissions screen, select **Grant admin consent for ServiceNow**.


## Result

Microsoft Exchange Online is set up with Microsoft Azure.

## What to do next

Configure resource room and specify the delegated user email details. For more information, see [Configure resource rooms in Microsoft Exchange Online](configure-resource-rooms-in-msex.md).

**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

**Related topics**  


[Configure resource rooms in Microsoft Exchange Online](configure-resource-rooms-in-msex.md)

[Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online](setup-personal-auth-mode-oauth-connectivity-with-msex.md)

[Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online](configure-personal-auth-mode-connection-and-credential-alias.md)

[Configure your own connection and credential alias for personal authentication mode](configure-your-own-connection-and-credential-alias-for-personal-auth.md)

[Configure the Microsoft Exchange Online calendar provider in personal authentication mode](configure-calendar-provider-in-personal-auth-mode.md)

