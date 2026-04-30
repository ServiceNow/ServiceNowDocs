---
title: Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online
description: Establish a personal authentication mode connection and credential alias for Microsoft Exchange Online. Confirm that the values for the connection and credentials alias are set as specified.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a personal authentication mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online

Establish a personal authentication mode connection and credential alias for Microsoft Exchange Online. Confirm that the values for the connection and credentials alias are set as specified.

## Before you begin

Confirm that the application scope is set to **Workplace Calendar Synchronization**.

Role required: admin

## About this task

Configure the default connection and credential alias to use the default entity profile created during the personal authentication mode application registry.

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select Microsoft\_Exchange\_Online\_PersonalAuth connection and credential child alias type created for personal authentication.

3.  Perform the following to check the HTTP Connection details:

    1.  On the Connection &amp; Credential Aliases form, under the **Connections** tab, select the connection name.

    2.  In the **Connection alias** field, verify that the child alias inherits the properties from the parent alias.

    3.  Verify that the Connection URL is set to [https://graph.microsoft.com](https://graph.microsoft.com)https://graph.microsoft.com.

    4.  Select **Update**.

4.  Perform the following to check the OAuth Credentials details:

    1.  On the Connection &amp; Credential Aliases form, under the **Connections** tab, select the credential name.

    2.  On the OAuth 2.0 Credentials form, verify that the **OAuth Entity Profile** is set with the default OAuth entity profile that was created when creating the personal authentication mode app registry.

5.  Perform the following to request a new OAuth access token using the configured OAuth entity profile created for personal authentication:

    1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Credentials**.

    2.  Select **Ms Graph 1**.

    3.  Set the OAuth Entity Profile to the default personal authentication OAuth entity profile that was generated when you performed the personal authentication mode application registry.

    4.  Select **Get OAuth Token**.

        In the Microsoft Exchange login page that appears, log in with the delegated user email credentials.

6.  Perform the following to request a new OAuth access token using the configured OAuth entity profile created for personal authentication:

    1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Credentials**.

    2.  Select **Ms Graph 2**.

    3.  Set the OAuth Entity Profile to the default personal authentication OAuth entity profile that was generated when you performed the personal authentication mode application registry.

    4.  Select **Get OAuth Token**.

        In the Microsoft Exchange login page that appears, log in with the delegated user email credentials.


## Result

The Connection and credential alias is set.

**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](configure-azure-personal-auth-mode.md)

[Configure resource rooms in Microsoft Exchange Online](configure-resource-rooms-in-msex.md)

[Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online](setup-personal-auth-mode-oauth-connectivity-with-msex.md)

[Configure your own connection and credential alias for personal authentication mode](configure-your-own-connection-and-credential-alias-for-personal-auth.md)

[Configure the Microsoft Exchange Online calendar provider in personal authentication mode](configure-calendar-provider-in-personal-auth-mode.md)

