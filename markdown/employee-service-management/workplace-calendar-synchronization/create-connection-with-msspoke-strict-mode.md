---
title: Create connection with Microsoft Exchange Online Spoke in strict mode
description: Configure a strict mode connection with the Microsoft Exchange Online spoke.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a strict mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create connection with Microsoft Exchange Online Spoke in strict mode

Configure a strict mode connection with the Microsoft Exchange Online spoke.

## Before you begin

Ensure the following:

1.  Install Microsoft Exchange Online spoke from the ServiceNow Store. For more information, refer to [Microsoft Exchange Online spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/ms-exch-online-spoke.md).

    **Important:** After installing Microsoft Exchange Online spoke, check that the **Data Stream action** field of the Data source **Exchange Online Calendar** is not set to empty. Otherwise, repair the Microsoft Exchange Online spoke plugin.

2.  After installing Microsoft Exchange Online spoke, depending on what type of customer you are, perform the following actions:
    -   If you are a new customer, to install the applications, refer to [Install Workplace Calendar Synchronization](install-workplace-calendar-synchronization.md).
    -   If you are an existing customer, upgrade to the latest versions of the following applications:
        -   Workplace Reservation Management.
        -   Workplace Calendar Synchronization.
3.  Repair the Microsoft Exchange Online spoke. Perform the following repair if you never had an internal dependency on the **com.glide.hub.action\_type.datastream** plugin.
    1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.
    2.  Search and select Microsoft Exchange Online Spoke.
    3.  **Repair** the plugin.

Role required: admin

## About this task

Synchronize reservations using a connection with the Microsoft Exchange Online spoke.

## Procedure

1.  Ensure that the Microsoft Exchange Online spoke is installed.

    Refer to the **Before you begin** section.

2.  [Set up Microsoft Exchange Online spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-ms-exch-ol.md).

    If you are a new customer, in the **Create Connection records for the Microsoft Exchange Online spoke** procedure, perform the following actions:

    -   For **Microsoft\_Exchange\_Online** Connection and Credential alias, in the Connection related list, select **MS Graph 1** and make the changes.

        Do not change the **Name** and **Credential**. In the OAuth Entity Profile form of the **MS Graph 1** credential, ensure that the **Grant type** field is selected as **Client Credentials**.

    -   For **Microsoft\_Exchange\_Online\_clientCred** Connection and Credential alias, in the Connection related list, select **MS Graph 2** and make the changes.

        Do not change the **Name** and **Credential**. In the OAuth Entity Profile form of the **MS Graph 2** credential, ensure that the **Grant type** field is selected as **Client Credentials**.

    -   Get OAuth token.
        1.  Select the credentials \(**MS Graph 1** and **MS Graph 2**\) that you created previously.
        2.  In the Related links section, select **Get OAuth Token**.
        3.  In the Microsoft Exchange Online login page that appears, login with the strict mode user's email credentials.

## What to do next

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](auth-mxex-with-azure-strict-mode.md)

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

[Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md)

[Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md)

[Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md)

