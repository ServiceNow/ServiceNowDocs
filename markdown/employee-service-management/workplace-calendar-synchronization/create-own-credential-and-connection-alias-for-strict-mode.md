---
title: Create your own credential and connection alias for strict mode
description: Configure your own connection and credential alias if you do not want to use the default alias created during the strict mode application registration. You can configure your calendar to use the alias as an override alias.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a strict mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create your own credential and connection alias for strict mode

Configure your own connection and credential alias if you do not want to use the default alias created during the strict mode application registration. You can configure your calendar to use the alias as an override alias.

## Before you begin

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope icon.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

Role required: admin

## About this task

The application by default providers connection and credential. Perform this procedure if you want to create your own connection and credential alias instead of using the default alias. If you want to use the default alias then refer to [Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md).

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential aliases**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the connection and credential alias.|
    |ID|The field is automatically generated after you save the form based on the specified **Name**.|
    |Application|Ensure that the application is set as **Microsoft Exchange Online Spoke**|
    |Parent alias|Select **sn\_ex\_online\_spke.Microsoft\_Exchange\_Online**.|

4.  Select **Submit**.

    The Connection and Credential alias record is created. As the next step, you must create a OAuth 2.0 credential record.

5.  Create an OAuth 2.0 credential to use in the newly created connection and credential alias record.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **OAuth 2.0 Credentials**.

    4.  On the form, fill in the fields.

        |Field|Descriptions|
        |-----|------------|
        |Name|Name of the credential. Provide a unique name to differentiate from the default credentials provided by the application.|
        |Active|Option to activate the credential.|
        |OAuth Entity Profile|Select the default OAuth entity profile that was generated when you performed the strict mode app registry in [Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md).|
        |Applies to|Specify how you want to apply to the MID servers.|
        |Order|Order for the credential.|

    5.  Select **Submit**.

        The credential record is created.

    6.  Open the credential record that you created.

    7.  On the form, select **Get OAuth Token**.

        **Note:** If you are configuring strict mode, then you must perform this step.

        On the Microsoft window that opens, enter your credentials.

    8.  Select **Update**.

6.  Configure connection for the connection and credential alias.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential aliases**.

    2.  Select the connection and credential record that you created in the initial steps.

    3.  On the form, in the Connections related list, select **New**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the connection.|
        |Credential|Select the credential record that you created in Step 5.|
        |Connection alias|The field is automatically set with the connection and credential alias.|
        |Connection URL|Enter [https://graph.microsoft.com](https://graph.microsoft.com)|

    5.  Select **Submit**.


## Result

The connection and credential record is created with specified credentials and connections.

## What to do next

To use it for the calendar provider, see [Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md).

**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](auth-mxex-with-azure-strict-mode.md)

[Create connection with Microsoft Exchange Online Spoke in strict mode](create-connection-with-msspoke-strict-mode.md)

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

[Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md)

[Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md)

