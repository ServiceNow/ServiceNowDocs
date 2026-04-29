---
title: Set up the Microsoft 365 Excel spoke
description: Integrate the ServiceNow instance and Microsoft 365 Excel by using the OAuth credentials to authenticate ServiceNow requests.Create a credential record for the Microsoft Azure Portal Specify whether record is for a host, instance, server, custom application, or account: account. The Microsoft 365 Excel Spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft 365 Excel Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft 365 Excel spoke

Integrate the ServiceNow instance and Microsoft 365 Excel by using the OAuth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft 365 Excel spoke.
-   Role required: admin.

## Create a credential record for the Microsoft 365 Excel spoke

Create a credential record for the Microsoft Azure Portal account. The Microsoft 365 Excel Spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

-   Register your ServiceNow instance in [Microsoft Azure Portal](https://portal.azure.com) and record the client ID and client secret. Also, add the offline\_access, Files.ReadWrite.All, and Files.ReadWrite scopes in the API permissions for the application. For more information, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app).

    **Note:** Ensure that the Redirect URI of the instance is in the `https://<instance>.service-now.com/oauth_redirect.do` format.

-   Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection and Credential Aliases**.

2.  Open the **Microsoft\_365\_Excel** record.

3.  Click the **Create New Connection &amp; Credential** related link.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection. This field is automatically set to `Microsoft 365 Excel Spoke Connection` Cred.|
    |Connection URL|The URL used for connecting to Microsoft Office 365 Excel. This field is automatically set to `https://graph.microsoft.com/v1.0`|
    |Credential Name|Name of the credential. This field is automatically set to `Microsoft 365 Excel Spoke Credential`|
    |OAuth Entity Name|Name of the OAuth entity profile. This field is automatically set to `Microsoft 365 Excel Spoke OAuth`|
    |OAuth Client ID|Client ID of the Microsoft Office 365 Excel application you registered in Azure Portal.|
    |OAuth Client Secret|Client Secret that you request for the registered application in Azure Portal.|
    |OAuth Redirect URL|The redirect URL. The format of the URL is `https://<instance>.service-now.com/oauth_redirect.do`|

5.  Click **Create and Get OAuth Token**.


