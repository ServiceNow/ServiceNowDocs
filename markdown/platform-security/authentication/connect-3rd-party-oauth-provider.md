---
title: Connect to a third-party OAuth provider
description: Configure how the client ID and secret are sent to your OAuth provider.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [OAuth outbound, OAuth authentication, Authentication, Access Management]
---

# Connect to a third-party OAuth provider

Configure how the client ID and secret are sent to your OAuth provider.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and then click **New**.

2.  On the interceptor page, click **Connect to a third-party OAuth provider** and then fill in the form.

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

The client ID of application registered in the third-party OAuth server.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret of the application registered in the third-party OAuth server.

</td></tr><tr><td>

OAuth API Script

</td><td>

The script used to customize request and response to the external OAuth provider.

</td></tr><tr><td>

Logo URL

</td><td>

The OAuth application logo URL.

</td></tr><tr><td>

Default Grant type

</td><td>

The default grant type used to establish the token. Choices include:

-   **Authorization code**: The code that is granted to the client to obtain an access token, which is then used to obtain access to the resource. If you select this option, then you need an authorization URL \(the URL of the authorization server\).
-   **Resource owner password credentials**: The user name and password of the user that is trying to obtain access to the resource.
-   **Client Credentials**: The client ID and client secret, which are both used to get the access token. This method does not provide refresh tokens.
-   **JWT Bearer**: An authorization server validates a JWT token which enables identity and security information to be shared across security domains.
-   **SAML2 Bearer**: Generates the SAML2 assertion and then exchanges the assertion for the access tokens wit the provider.

**Note:** For outbound request to SuccessFactors use the **SAML2 Bearer** as the Default Grant Type.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 8,640,0000 seconds.

</td></tr><tr><td>

Public Client

</td><td>

Enables public clients to require PKCE for an authorization.**Note:** You can use only Authorization Code as the **Default Grant type** when PKCE is enabled.

</td></tr><tr><td>

Code challenge method

</td><td>

The code challenge method used in OAuth PCKE workflow. Choices include: -   S256 \[Default\]
-   Plain
-   None


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

The OAuth client populates the client credentials in the request: -   In Request Body \(Form URL-Encoded\)
-   Basic Authorization header
-   As Private Key JWT


</td></tr><tr><td>

Client Type

</td><td>

Choose the client type, based on the type of your client. Options:-   **Iframe Embedded**
-   **Integration as a User**
-   **Integration as a Service**
To know more, see [Configure client type for OAuth and SSO records](../../../integrate/authentication/concept/client-type.md).

</td></tr></tbody>
</table>    The system creates a record in the Application Registries \[oauth\_entity\] table with type OAuth Provider.

3.  Select OAuth Entity Profiles to validate a system-generated default profile for the new OAuth provider without any scope.

    You can change or add an OAuth provider profile including the name, grant type, and OAuth Scope.

4.  Select OAuth Entity Scopes to define all available OAuth scopes for this OAuth provider.

    You can select the scopes when you create or update a profile. Each OAuth scope contains a name and a scope that you must get from the provider's specification, such as a read scope or a write scope. Each scope must be defined separately.

5.  Select OAuth Entity Resources to define all OAuth resources this OAuth provider.

6.  Select **Submit**.


