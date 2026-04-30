---
title: Configure CyberArk
description: Configure the CyberArk vault to store OAuth 2.0 credentials and respond to requests for OAuth 2.0 credentials from the MID Server.
locale: en-US
release: xanadu
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [OAuth 2.0 authentication via MID Server using external credential storage, External credential storage, Getting started with credentials, Connections and Credentials, Access Management]
---

# Configure CyberArk

Configure the CyberArk vault to store OAuth 2.0 credentials and respond to requests for OAuth 2.0 credentials from the MID Server.

## Before you begin

Confirm that you have subscribed to the ServiceNow IntegrationHub Standard Pack Installer. For more information, see [https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

Role required: agent\_admin or admin

## Procedure

1.  [Configure the CyberArk vault and install the AIM API](t_InstallCyberArkAIMAPI.md).

2.  [Import the CyberArk JAR file](t_ImportTheCyberArkJARFile.md).

3.  [Configure OAuth 2.0 credentials on CyberArk](configure-oauth-2-0-credentials-on-cyberark.md).

4.  [Configure a connection to send OAuth request via the MID Server using external vault](configure-oauth-2-0-authentication.md).


-   **[Configure OAuth 2.0 credentials on CyberArk](configure-oauth-2-0-credentials-on-cyberark.md)**  
Configure your CyberArk vault with OAuth 2.0 credentials that the ServiceNow instance requests.

**Parent Topic:**[OAuth 2.0 authentication via MID Server using external credential storage](../concept/oauth-2-0-support-in-external-credential.md)

