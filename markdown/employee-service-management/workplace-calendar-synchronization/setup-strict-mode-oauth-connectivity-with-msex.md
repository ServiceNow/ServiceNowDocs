---
title: Setup strict mode OAuth connectivity with Microsoft Exchange Online
description: Create a strict mode app registry for Microsoft Exchange Online with ServiceNow instance for OAuth authorization.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create a strict mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Setup strict mode OAuth connectivity with Microsoft Exchange Online

Create a strict mode app registry for Microsoft Exchange Online with ServiceNow instance for OAuth authorization.

## Before you begin

[Configure Microsoft Azure](auth-mxex-with-azure-strict-mode.md)

[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

Ensure that the application scope is set to **Microsoft Exchange Online Spoke**. Otherwise, do the following:

1.  Select the Application scope icon \(![Application scope to set the scope of your application.](../image/application-scope-globe-icon.png)\) on the Employee Center homepage.
2.  In the drop- down, select the option consisting **Application scope:**.
3.  In the filter navigator, search and select **Microsoft Exchange Online Spoke**.
4.  Refresh the page.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  Select **Connect to a third party OAuth Provider**

4.  On the form, fill in the fields with the specified details.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record as a strict mode record, for example, MsExchange strict mode.|
    |Client ID|Client ID created during the app creation in Microsoft Azure.|
    |Client Secret|The password you generated when creating the app in Microsoft Azure.|
    |Default Grant Type|Grant type used to establish the token. Select **Authorization Code**.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/token >`.|
    |Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|

5.  Right-click in the form header and select **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, MsExchange Strict mode default profile.

6.  Create a OAuth Entity Scope.

    1.  In the OAuth Entity Scopes related list, select **Insert a new row...**

    2.  Enter the name as `Calendars.ReadWrite` for the scope.

    3.  Enter the OAuth scope as `Calendars.ReadWrite`.

    4.  Select the Save icon.

    5.  Right-click the Application Registry form header and select Save.

        The system creates the scope record. Similarly, create the following entity scopes:

        -   **Name**: Calendars.ReadWrite.Shared

            **OAuth scope**: Calendars.ReadWrite.Shared

        -   **Name**: offline\_access

            **OAuth Scope**: offline\_access

7.  Select **Update**.

8.  On the Application registry form, select the **OAuth Entity Profiles** related list.

    In the following steps, you add the OAuth Entity Scopes that you created in Step 6 to the default profile.

    1.  Select the default entity profile, for example, MsExchange Strict mode default profile.

    2.  On the OAuth Entity Profile form, do the following:

        1.  In the OAuth Entity Profiles Scopes section, double-click **Insert a new row**.
        2.  Select the Lookup icon \(![Lookup icon.](../../../common/image/List_SearchIcon.png)\).
        3.  Select `Calendars.ReadWrite` that is assigned to the OAuth provider that you created in Step 6.
        4.  Repeat the previous steps and also add the following OAuth Entity Profiles Scopes created in Step 6:
            -   `Calendars.ReadWrite.Shared`
            -   `offline_access`
9.  Select **Update**.


## Result

The strict mode OAuth registration is added for Microsoft Exchange Online with strict mode OAuth entity profiles and OAuth entity scopes.

## What to do next

Configure the connection and credential alias. You can configure the default alias ore create your own alias.

To configure the default alias, refer to [Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md).

**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

**Previous topic:**[Create a strict mode configuration in Microsoft Exchange Online](strict-mode-configuration-in-msex.md)

**Next topic:**[Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md)

