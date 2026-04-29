---
title: Configure strict mode Connection and Credential alias for Microsoft Exchange Online
description: Establish a strict mode connection and credential alias for Microsoft Exchange Online. Ensure that the values for the connection and credentials alias are set as specified.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 4
breadcrumb: [Create a strict mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure strict mode Connection and Credential alias for Microsoft Exchange Online

Establish a strict mode connection and credential alias for Microsoft Exchange Online. Ensure that the values for the connection and credentials alias are set as specified.

## Before you begin

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

**Note:** Starting from Workplace Calendar Synchronization version 2.0.1, to synchronize the reservations automatically with Microsoft Exchange Online, create a connection with Microsoft Exchange Online spoke version 3.2.1. If you have upgraded to Workplace Calendar Synchronization version 2.0.1, then the following procedure is no longer required. For more information on how to install Microsoft Exchange Online spoke and to set up a connection, refer to [Create a connection with Microsoft Exchange Online spoke](create-connection-with-msspoke.md).

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

Role required: admin

## About this task

Configure the default connection and credential alias to use the default entity profile created during the strict mode application registry \(in [Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)\). You can also create your own connection and credential alias, if you do not want to use the default alias. To create your own alias, refer to [Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md).

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Credentials**.

2.  Check if the OAuth entity profile is set as follows:

    Perform the following actions individually:

    1.  Select **MS Graph 1**.

        On the form, check if the **OAuth Entity Profile** is set with the OAuth entity profile that was created when they created the strict mode app registry \(performed in [Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)\). If it is not set, then set the profile as specified.

    2.  To generate the OAuth token, select the **Get OAuth Token** related link.

        In the Microsoft Exchange login page that appears, login with the delegated user email credentials. You must be prompted for credential. When asked, specify the strict mode email credentials.

        **Warning:** If you are not prompted for the credential, it may use the credential of the logged-in user on the same browser, which is incorrect. You must close the browser and refresh to be prompted about the credential.

    3.  Go back to the **Credentials** list.

    4.  Select **MS Graph 2**.

        On the form, check if the **OAuth Entity Profile** is set with the OAuth entity profile that was created when they created the strict mode app registry \(performed in [Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)\). If it is not set, then set the profile as specified.

        **Warning:** If you are not prompted for the credential, it may use the credential of the logged-in user on the same browser, which is incorrect. You must close the browser and refresh to be prompted about the credential.


## Result

The Connection and credential alias is set.

-   Configure new rooms\(resources\) in Microsoft Exchange Online to synchronize reservations.
-   After synchronization, ensure that the meeting subject is unchanged. If the meeting subject is changed, use Microsoft PowerShell to make changes

## What to do next

[Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md)

**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](auth-mxex-with-azure-strict-mode.md)

[Create connection with Microsoft Exchange Online Spoke in strict mode](create-connection-with-msspoke-strict-mode.md)

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

[Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md)

[Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md)

