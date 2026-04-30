---
title: Set up OAuth connection with Microsoft Exchange Online
description: Register your Microsoft Exchange Online with ServiceNow instance for OAuth authorization.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create a normal mode connection, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Set up OAuth connection with Microsoft Exchange Online

Register your Microsoft Exchange Online with ServiceNow instance for OAuth authorization.

## Before you begin

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope.](../image/application-scope-globe-icon.png)\) on the top-right corner of your Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

Ensure that you performed the following steps:

-   [Configure Microsoft Azure in normal mode](authenticate-mxexchange-with-azure.md)
-   Configured resources Microsoft Exchange Online in the calendar. For more information, refer to [https://learn.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-resource-mailboxes](https://learn.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-resource-mailboxes).
-   [Create a connection with Microsoft Exchange Online spoke](create-connection-with-msspoke.md)

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **Microsoft Exchange Online\_clientCredentials**

3.  On the form, fill in the fields with the specified details.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record, for example, Microsoft Exchange for Sync.|
    |Client ID|Client ID created during the app authentication in Microsoft Azure.|
    |Client Secret|The password you generated when creating the app in Microsoft Azure.|
    |Default Grant Type|Grant type used to establish the token. Select **Client Credentials**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/token`.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

4.  Right-click in the form header and select **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Microsoft Exchange Online default_profile`.


## Result

The OAuth registration is added for Microsoft Exchange Online.

## What to do next

Depending on whether you want to use the default alias or you want to create your own alias, do one of the following:

-   To use default alias: [Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections](create-connection-and-credential-alias-for-msexchange-.md).
-   To create your own alias: [Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md).

**Parent Topic:**[Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md)

**Related topics**  


[Configure Microsoft Azure in normal mode](authenticate-mxexchange-with-azure.md)

[Create a connection with Microsoft Exchange Online spoke](create-connection-with-msspoke.md)

[Configure Connection and credential alias for Microsoft Exchange Online using the default credentials and connections](create-connection-and-credential-alias-for-msexchange-.md)

[Create your own connection and credential alias for Microsoft Exchange Online](create-own-connection-and-credential-alias-normalmode.md)

[Configure Microsoft Exchange Online calendar provider](configure-xsex-calendar-provider-in-normal-mode.md)

