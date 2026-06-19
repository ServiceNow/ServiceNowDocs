---
title: Configure an OAuth client in SAP
description: Register and configure an OAuth 2.0 client in SAP using the system user created for OAuth authentication, to enable secure data exchange with your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/configure-oauth-client-sap.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
keywords: [OAuth client, SOAUTH2, SAP OAuth configuration, OAuth scopes]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Configure an OAuth client in SAP

Register and configure an OAuth 2.0 client in SAP using the system user created for OAuth authentication, to enable secure data exchange with your ServiceNow instance.

## Before you begin

A system user for OAuth authentication must exist in SAP before configuring the OAuth client. For details, see [Create a system user for OAuth authentication in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-system-user-oauth-sap.md).

SAP Role required: SAP Basis administrator

## About this task

Use transaction code **SOAUTH2** to register the OAuth client and define the grant types, redirect URI, and scopes required for the integration.

## Procedure

1.  Open transaction code **SOAUTH2** in your SAP system and select **Create**.

2.  In the **Client ID** field, select the system user created for OAuth authentication.

    For example, `OAUTH_USER`. For information on creating a system user, see [Create a system user for OAuth authentication in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/create-system-user-oauth-sap.md).

3.  Enter a description for the OAuth client, then select **Next**.

4.  On the Grant Types screen, fill in the fields.

    |Field|Value|
    |-----|-----|
    |SAML 2.0 Bearer|Clear this option.|
    |Authorization Code|Select this option.|
    |Redirect URI|The redirect URI for your ServiceNow instance.|
    |Refresh Allowed|Select this option to enable refresh.|

5.  Select **Next**.

6.  Define the following scopes for the OAuth client.

    -   `/NOW/ODATA_VALIDATE_REFRESH_SRV_0001`
    -   `/NOW/ODATA_PULL_DATA_SRV_0001`
    \[Omitted image "sap-config-oauth-client.png"\] Alt text: OAuth 2.0 configuration page on SAP portal

7.  Select **Finish** and then select **Save**.


## What to do next

Configure roles and authorizations for the OAuth user. For details, see [Configure roles and authorizations for the OAuth user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/configure-roles-auth-oauth-user.md).

