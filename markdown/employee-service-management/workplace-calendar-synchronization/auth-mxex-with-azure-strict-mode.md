---
title: Configure Microsoft Azure
description: Set up a strict mode authentication with Microsoft Azure to connect Microsoft Exchange Online with Workplace Calendar Synchronization.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a strict mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Microsoft Azure

Set up a strict mode authentication with Microsoft Azure to connect Microsoft Exchange Online with Workplace Calendar Synchronization.

## Before you begin

As a delegated user, you must have a valid mailbox in the Microsoft Exchange Online. The user is identified by the email address. The same email address must be specified in the delegated user email address where it is necessary.

Role required: Exchange administrator

## About this task

Add strict mode permissions to synchronize Workplace Calendar Synchronization with Microsoft Exchange Online via GraphAPI in strict mode.

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

    4.  Select **Delegated permissions**.

    5.  Under **Calendars**, select **Calendars.ReadWrite**, **Calendars.ReadWrite.Shared** and **Offline\_access**.

    6.  Select **Add permissions**.

    7.  On the Configured permissions screen, select **Grant admin consent for ServiceNow**.


## What to do next

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md).

**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

**Related topics**  


[Create connection with Microsoft Exchange Online Spoke in strict mode](create-connection-with-msspoke-strict-mode.md)

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

[Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md)

[Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md)

[Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md)

