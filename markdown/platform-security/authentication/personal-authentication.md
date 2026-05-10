---
title: Personal Authentication
description: Personal authentication enables you to securely connect and manage your OAuth-based integrations like Microsoft OneDrive or Google Drive.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Access Management]
---

# Personal Authentication

Personal authentication enables you to securely connect and manage your OAuth-based integrations like Microsoft OneDrive or Google Drive.

## OAuth 2.0 Credentials

The OAuth 2.0 Credentials module in ServiceNow `(oauth_2_0_credentials)`enables you to configure and manage access tokens used to connect with external OAuth 2.0-compliant systems. Use the Personal integration type when each user must authenticate with their own identity to an external system.

Use the Credential form to configure OAuth 2.0 credentials with `integration_type = Personal`. For more information, see [OAuth 2.0 credentials](../../../product/credentials/reference/oauth-2-credentials.md).

Personal authentication is supported only for the following OAuth 2.0 grant types:

-   Authorization Code
-   Resource Owner Password Credentials \(ROPC\)

Grant types such as Client Credentials, and JWT Bearer Grant aren’t supported with `integration_type = Personal`.

**Note:** Personal authentication is also supported via a MID Server for the Authorization Code and ROPC grant types. For more information, see [OAuth token fetching via MID](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1645211).

## Personal Authentication dashboard

Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface. For more information, see [Using the Personal Authentication dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/personal-auth-dashboard.md).

**Note:** The personal authentication dashboard can only be accessed by users who are assigned to the role: `sn_personal_auth.personal_auth_user`

