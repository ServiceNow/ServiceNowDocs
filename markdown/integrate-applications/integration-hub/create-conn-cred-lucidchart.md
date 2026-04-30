---
title: Create a connection and credential alias for the Lucidchart Diagramming spoke
description: Create a connection and credential record for the Lucidchart application. The Lucidchart connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Lucidchart Diagramming Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a connection and credential alias for the Lucidchart Diagramming spoke

Create a connection and credential record for the Lucidchart application. The Lucidchart connection and credential alias uses these credentials to authorize actions.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Lucidchart spoke.
-   Register your application using Lucid API console and record the client ID and client secret. For more information, see [Create OAuth 2.0 Client in Lucidchart](set-up-lucidchart.md).
-   Role required: ServiceNow admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the Lucidchart record.

3.  Under Related Links section, click **Create New Connection &amp; Credential**.

4.  On the pop-up window, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection. This field is automatically set to **Lucid Spoke Connection**.|
    |Connection URL|The URL used for connecting to Lucid APIs. This field is automatically set to `https://api.lucid.co`.|
    | | |
    |OAuth Entity Name|Name of the OAuth entity profile. This field is automatically set to **Lucid Credentials**.|
    |OAuth Client ID|Client ID generated when you created the OAuth client application in the Lucid API Console.|
    |OAuth Client Secret|Client Secret generated when you created the OAuth client application in the Lucid API Console.|
    |OAuth Authorization URL|Lucid authorization URL. This field is automatically set to [https://lucid.app/oauth2/authorizeUser](https://lucid.app/oauth2/authorizeUser).|
    |OAuth Token URL|Lucid token URL. This field is automatically set to [https://api.lucid.co/oauth2/token](https://api.lucid.co/oauth2/token).|
    |OAuth Redirect URL|The redirect URL. This field is an auto-generated value. You must copy this URL and paste in the Lucid OAuth Client for the integration. The format of the URL is `https://<your-instance>.service-now.com/oauth_redirect.do`.|

5.  Click **Create and Get OAuth Token**.


## Result

An Application Registry, Connection Record, and Credential record is created in the ServiceNow instance.

