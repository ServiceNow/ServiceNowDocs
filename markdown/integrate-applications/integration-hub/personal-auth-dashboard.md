---
title: Using the Personal Authentication dashboard
description: Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage connections, Integration Hub, Workflow Data Fabric]
---

# Using the Personal Authentication dashboard

Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.

The Personal Authentication dashboard provides a streamlined way to manage your personal authentication integrations. With personal authentication, multiple users can use Integration Hub without needing to share superuser credentials. It also enhances security by removing the need to manage ACLs for third-party systems.

This feature requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Dashboard overview

The Personal Authentication dashboard has two main sections.

-   The My Integrations section at the top of the page, which shows your authenticated integrations.
-   The Integrations I can use section at the bottom of the page, which shows the integrations available to you.

![The Personal Authentication dashboard with two sections: The My Integrations section, and the Integrations I can use section.](../images/personal-auth-dashboard.png "Personal Authentication dashboard")

-   **My Integrations section**

    Displays authenticated integrations. Each integration has its own card. From the card, you can **Revoke** or **Renew** the authentication.

    When you revoke an authentication, you revoke any relevant access or refresh tokens for the personal authentication credential associated with the integration. Revoking invalidates the existing authentication. You can reauthenticate later to reestablish the connection. Once the authentication is revoked, the integration card moves to the Integrations I can use section of the dashboard.

    Renewing an authentication renews the associated token and updates the expiration date. To renew, select the **Renew** button on the integrations card. This button opens a pop-up window where you can reauthenticate the credential. The contents of the pop-up window depend on the integration.

    -   For ServiceNow integrations, the pop-up window has fields where you can enter the **Username** and **Password** for the credential, then select **Get OAuth Token**.
    -   For all other integrations, the pop-up window displays your OAuth credential page for that application.
-   **Integrations I can use section**

    Displays the integrations that are available but not authenticated. To authenticate, select the **Authenticate** button on the integration card. Authenticating opens the same pop-up window that opens when you **Renew** an integration: For ServiceNow integrations, the pop-up window has the **Username**, **Password**, and **Get OAuth Token** buttons. For all other integrations, the pop-up window displays your OAuth credential page for that application.

    Once the credential is authenticated, the integration card moves to the My Integrations section at the top of the dashboard.


## Required dashboard setup

If you're already using the personal authentication credential type, you can upgrade to the dashboard by installing the Personal Authentication \[com.snc.sn\_ihub\_personal\_auth\] plugin. After installing the plugin, navigate to **All** &gt; **IntegrationHub** &gt; **Personal Authentication** &gt; **Personal Integrations** to see the dashboard.

The integrations on the dashboard all come from the Connection &amp; Credential Aliases \[sys\_alias\] table. Any alias where the credential has a personal integration type is displayed on the dashboard, according to the following guidelines.

-   If the credential currently has a valid token, it's listed in the My Integrations section of the dashboard.
-   If the credential doesn't currently have a valid token, it's listed in the Integrations I can use section of the dashboard.

If you're not already using the personal authentication credential type, you can configure one by creating a Connection &amp; Credential Alias that uses an OAuth 2.0 credential with the **Integration Type** of **Personal**. For more details and instructions, see Create a Connection &amp; Credential alias.

## Token revocation URL

Revoking an authentication revokes all the related active tokens stored in the instance for the user that initiated the session. You can also enable token revocation on the OAuth Server by providing the server's token revocation endpoint in the **Token Revocation URL** field.

To enable authentication revocation at the OAuth Server, fill in the **Token Revocation URL** field in the Application Registries form for the integration's OAuth Provider. To fill in this field, follow these steps.

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.
2.  Select the form for the appropriate OAuth Provider from the Application Registries \[oauth\_entity\] table.
3.  In the **Token Revocation URL** field, enter the OAuth Server's token revocation endpoint.

## Roles

The Personal Authentication dashboard requires the sn\_personal\_auth.personal\_auth\_user role.

