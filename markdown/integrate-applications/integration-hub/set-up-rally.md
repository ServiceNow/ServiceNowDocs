---
title: Setting up the Rally spoke
description: Integrate the ServiceNow instance and Rally by using Rally credentials to authenticate ServiceNow requests.Register the Rally OAuth application to access the Rally API 2.0 and to receive a Client ID and Client secret.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Rally Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Setting up the Rally spoke

Integrate the ServiceNow instance and Rally by using Rally credentials to authenticate ServiceNow requests.

## Register a Rally OAuth application

Register the Rally OAuth application to access the Rally API 2.0 and to receive a Client ID and Client secret.

### Before you begin

-   The Rally Integration Hub spoke must be active. For more information, see [Rally Spoke](rally-spoke.md).
-   Role required: admin.

### Procedure

1.  Log in to [CA Agile Central](https://rally1.rallydev.com/login/accounts/index.html) by using your admin credentials.

2.  Select **OAUTH CLIENTS** &gt; **Create New Client**.

3.  In the Create Oauth Client dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Application Name|Provide a name for the application.|
    |Callback URL|Callback URL of the ServiceNow instance to which the application is to be integrated. For example, `https://<instance_url>/oauth_redirect.do`.|

4.  Select **Next**.

5.  Copy the Client ID and Client secret for later use.


