---
title: Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections
description: Establish connection and credential alias for Microsoft Exchange Online so that you can synchronize reservations. Configure the default credentials and connections. Ensure that the values for the connection and credentials alias are set as specified.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a normal mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections

Establish connection and credential alias for Microsoft Exchange Online so that you can synchronize reservations. Configure the default credentials and connections. Ensure that the values for the connection and credentials alias are set as specified.

## Before you begin

-   [Configure Microsoft Azure in normal mode](authenticate-mxexchange-with-azure.md)
-   [Set up OAuth connection with Microsoft Exchange Online](setup-connectivity-with-msexchange-for-calendar-sync.md).

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

**Note:** Starting from Workplace Calendar Synchronization version 2.0.1, to synchronize the reservations automatically with Microsoft Exchange Online, create a connection with Microsoft Exchange Online spoke version 3.2.1. If you have upgraded to Workplace Calendar Synchronization version 2.0.1, then the following procedure is no longer required. For more information on how to install Microsoft Exchange Online spoke and to set up a connection, refer to [Create a connection with Microsoft Exchange Online spoke](create-connection-with-msspoke.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Credentials**.

    Perform the following actions individually:

    1.  Select **MS Graph 1**.

        On the form, check if the **OAuth Entity Profile** is set as **Microsoft Exchange Online\_clientCredentials default\_profile**. If it is not set, then set the profile as specified.

    2.  Go back to the **Credentials** list.

    3.  Select **MS Graph 2**.

        On the form, check if the **OAuth Entity Profile** is set as **Microsoft Exchange Online\_clientCredentials default\_profile**. If it is not set, then set the profile as specified.

2.  Navigate to **All** &gt; **Connection &amp; Credentials** &gt; **Connections**.

    Perform the following actions individually:

    1.  Select **MS Graph 1**.

        Check if the fields are set as follows:

        -   **Connection alias**: **sn\_ex\_online\_spke.Microsoft\_Exchange\_Online**
        -   **Credential**: **MS Graph 1**
        -   **Connection URL**: [https://graph.microsoft.com](https://graph.microsoft.com)
    2.  Go back to the **Connections** list.

    3.  Select **MS Graph 2**.

        Check if the fields are set as follows:

        -   **Connection alias**: **sn\_ex\_online\_spke.Microsoft\_Exchange\_Online\_clientCred**
        -   **Credential**: **MS Graph 2**
        -   **Connection URL**: [https://graph.microsoft.com](https://graph.microsoft.com)

## Result

The Connection and credential alias is set.

-   Configure new rooms\(resources\) in Microsoft Exchange Online to synchronize reservations.
-   After synchronization, ensure that the meeting subject is unchanged. If the meeting subject is changed, use Microsoft PowerShell to make changes.

## What to do next

[Configure Microsoft Exchange Online calendar provider](configure-xsex-calendar-provider-in-normal-mode.md)

**Parent Topic:**[Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md)

**Previous topic:**[Set up OAuth connection with Microsoft Exchange Online](setup-connectivity-with-msexchange-for-calendar-sync.md)

**Next topic:**[Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md)

