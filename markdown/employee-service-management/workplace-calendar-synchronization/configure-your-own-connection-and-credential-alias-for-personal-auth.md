---
title: Configure your own connection and credential alias for personal authentication mode
description: Configure your own connection and credential alias if you don’t want to use the default alias created during the personal authentication mode application registration. You can configure your calendar to use the alias as an override alias.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a personal authentication mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure your own connection and credential alias for personal authentication mode

Configure your own connection and credential alias if you don’t want to use the default alias created during the personal authentication mode application registration. You can configure your calendar to use the alias as an override alias.

## Before you begin

**Note:** Configure your own connection and credential alias only when multiple delegated user emails are required. Ensure that the alias is specified on the calendar provider as well.

Confirm that the application scope is set to **Workplace Calendar Synchronization**.

Role required: admin

## About this task

The application by default provides a connection and credential. Perform this procedure if you want to create your own connection and credential alias instead of using the default alias. If you want to use the default alias, refer to [Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online](configure-personal-auth-mode-connection-and-credential-alias.md).

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the connection and credential alias.|
    |ID|The field is automatically generated after you save the form based on the specified **Name**.|
    |Application|Ensure that the application is set as **Workplace Calendar Synchronization**|
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
        |OAuth Entity Profile|Select the default OAuth entity profile that was generated when you performed the personal authentication mode app registry in [Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online](setup-personal-auth-mode-oauth-connectivity-with-msex.md).|
        |Applies to|Specify how you want to apply to the MID Servers.|
        |Order|Order for the credential.|

    5.  Select **Submit**.

        The credential record is created.

    6.  Open the credential record that you created.

    7.  On the form, select **Get OAuth Token**.

        **Note:** If you’re configuring a strict mode, then you must perform this step.

        On the Microsoft window that opens, enter your credentials.

    8.  Select **Update**.

6.  Configure the connection for the connection and credential alias.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential aliases**.

    2.  Select the connection and credential record that you created in the initial steps.

    3.  In the Connections related list, select **New**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the connection.|
        |Credential|Select the credential record that you created in Step 5.|
        |Connection alias|The field is automatically set with the connection and credential alias.|
        |Connection URL|Enter [https://graph.microsoft.com](https://graph.microsoft.com)|

    5.  Select **Submit**.


**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](configure-azure-personal-auth-mode.md)

[Configure resource rooms in Microsoft Exchange Online](configure-resource-rooms-in-msex.md)

[Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online](setup-personal-auth-mode-oauth-connectivity-with-msex.md)

[Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online](configure-personal-auth-mode-connection-and-credential-alias.md)

[Configure the Microsoft Exchange Online calendar provider in personal authentication mode](configure-calendar-provider-in-personal-auth-mode.md)

