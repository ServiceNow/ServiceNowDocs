---
title: Configure Microsoft OneDrive application for Knowledge Graph
description: Use Microsoft SharePoint for fetching user-specific external data, such as shared files, from external services through a Knowledge Graph API.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Configure Microsoft OneDrive application for Knowledge Graph

Use Microsoft SharePoint for fetching user-specific external data, such as shared files, from external services through a Knowledge Graph API.

## Before you begin

Knowledge Graph uses Microsoft OneDrive application for authentication of Microsoft SharePoint required to fetch external data such as shared files used for people citation in Virtual Agent. Use the below process to setup the necessary authentication, used for people citation in Virtual Agent.

To view the share files, configure the Microsoft OneDrive application with Knowledge Graph.

To complete the configuration, you must:

-   Create Microsoft OneDrive application.
-   Setup Knowledge Graph application on Microsoft OneDrive tenant.
-   Update Microsoft OneDrive permissions for delegated access.
-   Create a new client secret and complete the authentication process.

Role required: admin

## Procedure

1.  Go to portal.azure.com and select **view** to Manage Microsoft Entra ID.

2.  To register the app, do the following:

    -   Select **Manage** &gt; **App registration** and select **New Application**.
    -   Add a Name for the application
    -   Select **Accounts in this organizational directory only** single-tenant apps for use.
    -   Select Register.

        **Note:** Copy and save the Application ID and Tenant ID for future reference.

3.  Once the new application is registered, add the client credentials:

    -   Select **Add a certificate or secret**.
    -   Select **New client secret** and add Description and Expiry duration.
    -   Select **Add**.
    -   Ensure that you copy and save the New client secret value that is created.
4.  Select **Overview** from the left navigation pane to add the redirect URL.

    -   Select **Add a redirect URI**.
    -   Select **Add a platform** from the platform configurations section.
    -   Add `https://<instanceURL>/oauth_redirect.do` in **Redirect URIs** and **Front-channel logout URL** fields on the configure web page.

        **Note:** Replace the &lt;instanceURL&gt; with your instance path. Example:**abc.service-now.com**.

    -   Select both the Access token and ID tokens option from the **Select the token you would like to be issued for authorization endpoint** section.
    -   Select **Configure**.
5.  Select **Manage** &gt; **App permissions** from the left navigation pane, to add permissions.

    -   Select **Add a permission**.
    -   Select **Microsoft Graph**.
    -   Select **Delegated permission**.
    -   Add and select **offline.access** and **Sites.Read.All** in Select permissions section.
    -   Select **Add permissions**.
    -   Ensure that the **Admin consent required** field is set to Yes for the newly added Microsoft Graph.
6.  Go to your ServiceNow instance to change the Application registry settings:

    -   Select **All** &gt; **System OAuth** &gt; **Application registry**
    -   Select **KG MS OneDrive Delegated Connector**.
    -   Add the copied Application ID in the **Client ID** field.
    -   Add the Client secret in the **Client secret** field.
    -   Add the Tenant ID in the placeholder for \[tenantId\] in the Authorization URL and Token URL field.
    -   Ensure that the Redirect URL is correct.
    -   Select **Update**.

