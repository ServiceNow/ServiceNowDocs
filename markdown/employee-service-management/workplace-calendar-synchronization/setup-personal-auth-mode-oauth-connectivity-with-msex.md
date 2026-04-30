---
title: Setup personal authentication mode OAuth connectivity with Microsoft Exchange Online
description: Create a personal authentication mode application registry for Microsoft Exchange Online with ServiceNow instance for OAuth authorization.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-11-28"
reading_time_minutes: 1
breadcrumb: [Create a personal authentication mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Setup personal authentication mode OAuth connectivity with Microsoft Exchange Online

Create a personal authentication mode application registry for Microsoft Exchange Online with ServiceNow instance for OAuth authorization.

## Before you begin

[Configure Microsoft Azure](configure-azure-personal-auth-mode.md)

Ensure that the application scope is set to **Workplace Calendar Synchronization**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope to set the scope of your application.](../image/application-scope-globe-icon.png)\) on the Employee Center home page.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Workplace Calendar Synchronization**.
4.  Refresh the page.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **Microsoft Exchange Online\_personalAuth** OAuth provider created for personal authentication.

3.  On the form, specify the OAuth provider details as described in the following table:

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the OAuth provider. For example, Microsoft Exchange Online\_personalAuth.|
    |Client ID|Client ID created during the app creation in Microsoft Azure.|
    |Client Secret|The password you generated when creating the app in Microsoft Azure.|
    |Default Grant Type|Grant type used to establish the token. Select **Authorization Code**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/token >`.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

4.  Right-click in the form header and select **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, Microsoft Exchange Online\_personalAuth default profile.

5.  Select the OAuth Entity Scopes list and verify that the following OAuth scopes are already defined for the OAuth provider profile:

    1.  Calendars.ReadWrite

    2.  Calendars.ReadWrite.Shared

    3.  Offline\_access

6.  Select **Update**.


## Result

The OAuth registration is added for Microsoft Exchange Online with personal authentication mode OAuth entity profiles and OAuth entity scopes.

**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

