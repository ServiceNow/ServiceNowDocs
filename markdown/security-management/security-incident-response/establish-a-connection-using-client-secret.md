---
title: Establish a connection using client secret
description: Establish a connection between newly created Microsoft Teams graph application with ServiceNow AI Platform instance.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Client Secret value, Establish MS Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Establish a connection using client secret

Establish a connection between newly created Microsoft Teams graph application with ServiceNow AI Platform instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open **Microsoft Teams Spoke**.

3.  Modify the field value **Configuration Template: MSIM Microsoft Teams ConnectorAuthorization Code Template** and save the form.

    **Note:** This template contains the delegated API permission required for the MSTeams integration.

4.  From the Related Links section, click Create **New Connection &amp; Credential**.

    | | |
    |---|---|
    |**Name**|Any unique Name.|
    |**Connection URL**|Connection URL. For example, https://graph.microsoft.com|
    |**API Version**|Version of the API. For example, v1.0|
    |**Authorization URL**|https://login.microsoftonline.com/&lt;&lt;tenant ID&gt;/oauth2/v2.0/authorize|
    |**Token URL**|https://login.microsoftonline.com/&lt;&lt;tenant ID&gt;/oauth2/v2.0/token|
    |**Token Revocation URL**|https://login.microsoftonline.com/&lt;&lt;tenant ID&gt;/oauth2/v2.0/revoke|
    |**OAuth Client ID**|Client ID.|
    |**OAuth Client Secret**|Client secret.|

5.  Click **Create and Get Oauth Token**.

    On success, the following API permissions are added to the Azure application.

    ![API Permissions - MS Teams](../../secops-integration-major-security-incident-management/image/api-permissions-msteams.png)


**Parent Topic:**[Using Client Secret value](using-client-secret-value.md)

