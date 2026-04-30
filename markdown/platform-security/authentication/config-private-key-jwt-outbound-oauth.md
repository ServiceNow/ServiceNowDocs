---
title: Configure Private Key JWT for Outbound OAuth
description: Configure Private Key JWT for outbound OAuth integrations.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Private Key JWT Support for OAuth 2.0 Client Authentication, OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# Configure Private Key JWT for Outbound OAuth

Configure Private Key JWT for outbound OAuth integrations.

## Before you begin

Role required: admin

Before configuring Private Key JWT for outbound OAuth integrations, you must perform the following tasks:

-   [Upload Java Key Store certificate](../../../administer/security/task/JWT-Bearer-token-support.md#): Attach a JKS certificate to your instance to use to enable the JWT client authentication.
-   [Configure a JWT signing key](../../../administer/security/task/JWT-Bearer-token-support.md#): Create a JWT signing key to assign to your Java KeyStore \(JKS\) certificate.

    **Note:** If you want to add **X.509 Certificate SHA-1 Thumbprint int \(x5t\)** to the header as part of the JWT Key, you must configure the form and add the **X.509 Certificate SHA-1 Thumbprint int \(x5t\)** field.

-   [Create a JWT provider with a JWT signing key](../../../administer/security/task/JWT-Bearer-token-support.md#): Add a JWT provider to your ServiceNow instance.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and then click **New**.

2.  On the interceptor page, click **Connect to a third-party OAuth provider** and then fill in the form.

    **Note:** You must add **Send Credentials** and **JWT Provider** fields to the form to use the Private Key JWT for Outbound OAuth authentication requests.

<table id="table_sgc_qqv_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the third-party OAuth connection.

</td></tr><tr><td>

Client ID

</td><td>

The client ID of the application registered in the third-party OAuth server.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret of the application registered in the third-party OAuth server.

</td></tr><tr><td>

OAuth API Script

</td><td>

The script used to customize requests and responses to the external OAuth provider.

</td></tr><tr><td>

Logo URL

</td><td>

The OAuth application logo URL.

</td></tr><tr><td>

Default Grant type

</td><td>

Choose: **Client Credentials**: The client ID and client secret, which are both used to get the access token. This method does not provide refresh tokens.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 8,640,000 seconds.

</td></tr><tr><td>

Public Client

</td><td>

Enables public clients to require PKCE for an authorization.**Note:** You can use only Authorization Code as the **Default Grant type** when PKCE is enabled.

</td></tr><tr><td>

Comments

</td><td>

Add any comments regarding the OAuth app.

</td></tr><tr><td>

Application

</td><td>

Application and scope that contain this record.

</td></tr><tr><td>

Accessible from

</td><td>

Make this app accessible from all application scopes or from this scope only.

</td></tr><tr><td>

Active

</td><td>

Select the check box to make the app active.

</td></tr><tr><td>

Authorization URL

</td><td>

The OAuth authorization code endpoint.

</td></tr><tr><td>

Token URL

</td><td>

The OAuth server token endpoint.

</td></tr><tr><td>

Token Revocation URL

</td><td>

The OAuth server token revocation endpoint.

</td></tr><tr><td>

Redirect URL

</td><td>

The OAuth callback endpoint. If blank, the instance auto-generates an entry.

</td></tr><tr><td>

Use mutual authentication

</td><td>

Check the box to use mutual authentication for token request and revocation. This feature requires a mutual authentication profile to be specified.

</td></tr><tr><td>

Send Credentials

</td><td>

Choose: **As Private Key JWT**

</td></tr><tr><td>

JWT Provider

</td><td>

JWT Provider details. You can use the lookup to select the JWT provider.

</td></tr></tbody>
</table>    The system creates a record in the Application Registries \[oauth\_entity\] table with type OAuth Provider that can be used for Private JWT Key authentication.


