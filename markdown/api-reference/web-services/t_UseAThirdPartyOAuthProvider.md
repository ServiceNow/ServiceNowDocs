---
title: Use a third-party OAuth provider
description: Each client application must register with the instance to participate in OAuth authorization.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure a message with OAuth, Outbound REST authentication, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Use a third-party OAuth provider

Each client application must register with the instance to participate in OAuth authorization.

## Before you begin

Role required: admin

## About this task

**Note:** ServiceNow only supports third-party OAuth providers to authorize requests from ServiceNow to third-party APIs.

For example, you might want to integrate with a third-party Calendar service which requires OAuth 2.0 access tokens to read a user's scheduled events and create events. Configure the Calendar service as a third-party OAuth provider. This configuration allows you to get an access token from the Calendar service and then use the token to make requests against the service from ServiceNow.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry** and then click **New**.

2.  On the interceptor page, click **Connect to a third party OAuth Provider** and then fill in the form.

<table id="table_sgc_qqv_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name that identifies the application to access.

</td></tr><tr><td>

Client ID

</td><td>

The unique ID of the application. The instance uses the client ID when requesting an access token. You must get the client ID from the authorization server.

</td></tr><tr><td>

Client Secret

</td><td>

\[Required\] The shared secret string that the instance and the application use to authorize communications with one another. If you do not enter the correct client secret, tokens are not issued.

</td></tr><tr><td>

OAuth API Script

</td><td>

This option enables you to reference an amended OAuthUtil script include. Copy and rename the default OAuthUtil script include file, and then amend this version for specific requests and responses to match your 3rd party OAuth provider. The amended script name must have the prefix **OAuth**. See [OAuthUtil](../../../app-store/dev_portal/API_reference/OAuthUtil/concept/c_OAuthUtilScriptInclude.md#) to add the required body parameter in the proper method.

</td></tr><tr><td>

Logo URL

</td><td>

The URL that contains an image to use as the application logo.

</td></tr><tr><td>

Default Grant Type

</td><td>

The type of grant:-   **Authorization code**: The code that is granted to the client to obtain an access token, which is then used to obtain access to the resource. If you select this option, then you need an authorization URL \(the URL of the authorization server\).
-   **Resource owner password credentials**: The user name and password of the user that is trying to obtain access to the resource.
-   **Client Credentials**: The client ID and client secret, which are both used to get the access token. This method does not provide refresh tokens.
-   **JWT Bearer**: An authorization server validates a JWT token which enables identity and security information to be shared across security domains.
-   **SAML2 Bearer**: Generates the SAML2 assertion and then exchanges the assertion for the access tokens wit the provider.

**Note:** For outbound request to SuccessFactors use the **SAML2 Bearer** as the Default Grant Type.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

The refresh token lifespan in seconds.

</td></tr><tr><td>

Accessible from

</td><td>

The application scope that this registry is accessible from.

</td></tr><tr><td>

Active

</td><td>

A check box that indicates that the application registry is active.

</td></tr><tr><td>

Authorization URL

</td><td>

If you are using the authorization code grant type, the URL of the endpoint to authorize the user. If you are accessing another ServiceNow instance, append `/oauth_auth.do` to the URL.

</td></tr><tr><td>

Token URL

</td><td>

The location of the token endpoint that the instance uses to retrieve and refresh tokens. If you are accessing another ServiceNow instance, append `/oauth_token.do` to the URL.

</td></tr><tr><td>

Redirect URL

</td><td>

The application endpoint that receives the authorization code. Leave the field empty to have the instance auto-generate the URL. If you are accessing another ServiceNow instance, append `/oauth_redirect.do` to the URL.

</td></tr><tr><td>

Token Revocation URL

</td><td>

The location of the endpoint that the instance uses to revoke the token. If you are accessing another instance, append `/oauth_revoke.do` to the URL.

</td></tr><tr><td>

Comments

</td><td>

Additional information to associate with the application.

</td></tr><tr><td class="sub-head" colspan="2">

Embedded lists

</td></tr><tr><td>

OAuth Entity Profiles

</td><td>

The profiles that are associated with the OAuth provider. The profile includes the grant type. Click the profile name to go to [the OAuth Entity Profile form](t_SpecifyAnOAuthProfile.md).

</td></tr><tr><td>

OAuth Entity Scopes

</td><td>

The entity scopes associated with the OAuth provider. The scope identifies the services the application has access to. Click the scope name to go to [the OAuth Entity Scope form](t_SpecifyAnOAuthScope.md).

</td></tr></tbody>
</table>3.  Click **Submit**. The record is saved in the Application Registries \[oauth\_entity\] table.

    The system creates a record in the Application Registries \[oauth\_entity\] table of type OAuth Provider. The instance also auto-generates a default profile using the specified grant type, but without any scopes.


## What to do next

You can [create additional profiles](t_SpecifyAnOAuthProfile.md), each with scopes.

-   **[OAuth profiles and scopes](../concept/c_OAuthProviderAndScope.md)**  
In the OAuth provider scenario, profiles and scopes specify the grant type, authorization type, and level of access.

**Parent Topic:**[Configure a REST message with OAuth](../../../integrate/outbound-rest/task/t_ConfigureARESTMessageWithOAuth.md)

