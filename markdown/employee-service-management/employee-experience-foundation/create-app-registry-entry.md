---
title: Create a Microsoft Teams application registry entry to connect the created app to ServiceNow instance
description: Register your Microsoft Teams application with your ServiceNow instance for OAuth authorization.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Create a Microsoft Teams application registry entry to connect the created app to ServiceNow instance

Register your Microsoft Teams application with your ServiceNow instance for OAuth authorization.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

3.  Select **New**.

4.  Select **Connect to a third-party OAuth Provider**.

5.  On the form, fill in the fields.

    -   Name: Name to uniquely identify the record, for example, Microsoft Teams for Notify Self-configured app.
    -   Client ID: Application \(client\) ID or Bot ID created and copied during the app creation in Microsoft Teams.

        Copy the Application \(client\) ID from the Microsoft Azure portal. Bot ID created in the Microsoft Teams Developer portal and Application \(client\) ID in the Microsoft Azure portal are the same. For the Application \(client\) ID or Bot ID information, see [Create an app in Microsoft Teams to enable making calls](create-app-ms-teams.md).

        Do not copy the App ID of the Microsoft Teams app created on the Microsoft Teams Developer Portal.

    -   Client Secret: The password you generated when creating the bot in the Microsoft Teams Developer Portal \(step 3h\).

        For the Client Secret information on the Microsoft Azure portal, see [Create an app in Microsoft Teams to enable making calls](create-app-ms-teams.md).

    -   Default Grant Type: `Client Credentials`.
    -   Token URL: Token endpoint URL that includes the Directory ID of your app with the structure `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`, where `<Directory ID>` is the tenant ID created during the app/bot creation in Microsoft Teams Developer Portal. For the tenant ID information in the Microsoft Azure portal, see [Create an app in Microsoft Teams to enable making calls](create-app-ms-teams.md).

        Or follow this procedure.

        1.  Log in to the [Microsoft Azure portal](https://portal.azure.com/).
        2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.
        3.  Search and open the new bot created for Notify connector by name or by Application \(client\) ID.
        4.  Copy the Directory \(tenant\) ID value.
        5.  Go to **Endpoints** &gt; **Get the OAuth 2.0 token endpoint \(v2\)**.
        6.  Replace `common` with the copied Directory \(tenant\) ID value.
6.  Select **OAuth Entity Scopes** in related list and add a record with the values `Default` in **Name** and `.default` in **OAuthscope**.

7.  Set OAuth Entity Profile values.

    **Note:** By default, an OAuth Entity Profile record is created. If it is not available, then you can create one by following these sub-steps.

    -   Select **OAuth Entity Profiles** in related list.
    -   Open the created `<>default_profile`record.
    -   Select **OAuth Entity Profile Scopes** in related list.
    -   Add a record with the values `Default` in **OAuth Entity Scope** and `<>default_profile` in **OAuth Entity Profile**.
    -   Select **Update** to save the changes.

## Result

The Microsoft Teams app is now registered with an OAuth profile authorization.

## What to do next

[Create a Connection &amp; Credentials alias for Microsoft Teams](create-connection-credential-aliases.md)

**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md)

