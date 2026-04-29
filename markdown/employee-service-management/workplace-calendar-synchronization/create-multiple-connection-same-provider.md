---
title: Create single or multiple calendar providers with Microsoft Exchange Online
description: For the Microsoft Exchange Online provider, configure single or multiple calendar providers.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create single or multiple calendar providers with Microsoft Exchange Online

For the Microsoft Exchange Online provider, configure single or multiple calendar providers.

## Before you begin

You must have Microsoft Exchange Online spoke version 3.2.4 or later installed.

**Important:** Multi-provider is not supported or is not the same as Exchange hybrid configurations.

**For strict mode:**

-   Ensure that every delegated user \(in the calendar provider\) has a different connection &amp; credential alias, connection, and credential records. However, you can reuse the same OAuth Entity profile in all the credential records.
-   While performing the **Get OAuth token** action for each credential, you must be prompted for credential. When asked, specify the delegated user email credentials.

    **Note:** If you are not prompted for the credential, it may use the credential of the logged-in user on the same browser, which is incorrect. You must close the browser and refresh to be prompted about the credentials.


Role required: admin

## Procedure

1.  For normal mode user:

    1.  [Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections](create-connection-and-credential-alias-for-msexchange-.md) or [Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md).

    2.  Create multiple calendar providers and specify the alias. [Configure Microsoft Exchange Online calendar provider](configure-xsex-calendar-provider-in-normal-mode.md)

2.  For delegated user:

    -   If there is a single delegated user, do the following:
        -   [Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md) or [Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md).
        -   Create a calendar provider. Refer to [Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md).
    -   For multiple delegated users:
        -   Create connection and credential record for each delegated user. Refer to [Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md) or [Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md).
        -   Create calendar providers for each user and specify the alias. Refer to [Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md).

## Result

Multiple providers are created for a single provider.

