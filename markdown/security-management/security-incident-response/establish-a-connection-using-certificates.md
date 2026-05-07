---
title: Establish a connection using certificates
description: Establish a connection between newly created Microsoft Teams graph application using certificates.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Certificates for authentication, Establish MS Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Establish a connection using certificates

Establish a connection between newly created Microsoft Teams graph application using certificates.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open **Microsoft Teams Spoke**.

3.  Modify the field value **Configuration Template: MSIM Microsoft Teams ConnectorAuthorization Code Template** and save the form.

    **Note:** This template contains the delegated API permission required for the MSTeams integration.

4.  From the Related Links section, select Create **New Connection &amp; Credential**.

<table id="choicetable_pnx_jpr_gwb"><thead><tr><th align="left" id="d272099e96">

 

</th><th align="left" id="d272099e98">

 

</th></tr></thead><tbody><tr><td id="d272099e103">

**Name**

</td><td>

Any unique Name.

</td></tr><tr><td id="d272099e112">

**Connection URL**

</td><td>

Connection URL. For example, https://graph.microsoft.com

</td></tr><tr><td id="d272099e121">

**API Version**

</td><td>

Version of the API. For example, v1.0

</td></tr><tr><td id="d272099e130">

**Authorization URL**

</td><td>

https://login.microsoftonline.com/&lt;&lt;tenant ID&gt;/oauth2/v2.0/authorize

</td></tr><tr><td id="d272099e140">

**Token URL**

</td><td>

https://login.microsoftonline.com/&lt;&lt;tenant ID&gt;/oauth2/v2.0/token

</td></tr><tr><td id="d272099e149">

**Token Revocation URL**

</td><td>

https://login.microsoftonline.com/&lt;&lt;tenant ID&gt;/oauth2/v2.0/revoke

</td></tr><tr><td id="d272099e158">

**OAuth Client ID**

</td><td>

Client ID.

</td></tr><tr><td id="d272099e167">

**OAuth Client Secret**

</td><td>

You can enter any value. **Note:** This is not important as you will be using the certificate-based authentication.

</td></tr></tbody>
</table>5.  Select **Create and Get Oauth Token**.

    An error message is displayed prompting 401- unauthorised.

6.  Reload the form and open the record in the Connections related list.

7.  Enter the Base64 encoded **Thumbprint** value in the **Encoded Certificate Thumbprint** attribute in the **Attributes** section.

    **Note:** The Thumbprint value is a hexadecimal value. You can use a Hexadecimal toBase64 \(Hex to Base64\) converter tool to encode the Thumbprint value to a Base64 value.

8.  Navigate to **System OAuth** &gt; **Application Registry**

9.  Open **MSIM Microsoft Teams Connector Authorization Code** record.

10. Modify the OAuth API Script: **OAuthUtilJWTMSTeamsConnector**.

11. Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

12. Open the record **MSIM Microsoft Teams Connector Credential**.

13. From Related Links, select **Get OAuth Token**.

    On success, the following API permissions are added to the Azure application.

    ![API Permissions - MS Teams](../image/api-permissions-msteams.png)


**Parent Topic:**[Using Certificates for authentication](using-certificates-for-authentication.md)

