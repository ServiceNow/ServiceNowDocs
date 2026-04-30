---
title: Configure Application Registry on the ServiceNow instance
description: Register the application with the instance to use OAuth authorization.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setup Splunk environment, Splunk integration setup, ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Application Registry on the ServiceNow instance

Register the application with the instance to use OAuth authorization.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

3.  Click **Create an OAuth API endpoint for external clients**.

4.  On the form, fill in the fields.

<table id="choicetable_ecw_c4x_gwb"><thead><tr><th align="left" id="d270448e94">

Field

</th><th align="left" id="d270448e97">

Description

</th></tr></thead><tbody><tr><td id="d270448e103">

**Name**

</td><td>

A unique name that identifies the application that you require OAuth access for.

</td></tr><tr><td id="d270448e112">

**Client ID**

</td><td>

\(Read-Only\) The auto-generated unique ID of the application. The instance uses the client ID when requesting an access token.

</td></tr><tr><td id="d270448e121">

**Client Secret**

</td><td>

The shared secret string that both the instance and the client application or website use to authorize communications with one another. The instance uses the client secret when requesting an access token. Leave this field blank to have the instance auto-generate a client secret. To display existing client secrets, click the lock icon.

</td></tr><tr><td id="d270448e130">

**Redirect URL**

</td><td>

The callback URL that the authorization server redirects to. Enter as many URLs as needed for all possible token consumers. The instance matches the URL of the incoming request to one of the redirect URLs. If no match is made, the instance uses the first redirect URL.

</td></tr><tr><td id="d270448e140">

**Logo URL**

</td><td>

The URL that contains an image to use as the application logo. The logo appears on the approval page when the user receives a request to grant a client application access to a restricted resource on the instance.

</td></tr><tr><td id="d270448e149">

**Application**

</td><td>

The name of the application.

</td></tr><tr><td id="d270448e158">

**Accessible from**

</td><td>

Define the application scope. Select one of the following:-   **All application scopes**
-   **This application scope only**


</td></tr><tr><td id="d270448e178">

**Active**

</td><td>

Select the check box to make the application registry active.

</td></tr><tr><td id="d270448e187">

**Refresh Token Lifespan**

</td><td>

The number of seconds that a refresh token is valid. The instance uses the lifespan value when requesting a refresh token. By default, refresh tokens expire in 100 days \(8640000 seconds\).

</td></tr><tr><td id="d270448e196">

**Access Token Lifespan**

</td><td>

The number of seconds that an access token is valid. The instance uses the lifespan value when requesting an access token. By default, access tokens expire in 30 minutes \(1800 seconds\).

</td></tr><tr><td id="d270448e206">

**Comments**

</td><td>

Additional information to associate with the application.

</td></tr></tbody>
</table>    ![Configure Application Registry on the ServiceNow instance](../image/splunk-addon-config.gif)

5.  Right-click on the form header, and click **Save**.

6.  Click **Submit**.


