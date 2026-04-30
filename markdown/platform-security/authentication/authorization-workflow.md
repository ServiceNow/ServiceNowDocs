---
title: Authorization code grant workflow
description: The OAuth authorization code grant is a secure and widely used flow for web, mobile, or desktop apps that access user data with user consent. It supports both private clients \(using a client secret\), and public clients \(using PKCE\).
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Authorization Code Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Authorization code grant workflow

The OAuth authorization code grant is a secure and widely used flow for web, mobile, or desktop apps that access user data with user consent. It supports both private clients \(using a client secret\), and public clients \(using PKCE\).

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

This topic collection provides information on how a client application can use the Authorization code grant flow to obtain a token from ServiceNow and make API calls with that token. Private clients use client secret, while public clients use PKCE code challenge.

![Authorization Workflow](../../machine-identity/images/mic-authorization-flow.png "Authorization workflow")

## Procedure

1.  Log in from the client application.

    The user begins the login process from the client application interface.

2.  Initiate the authorization request.

    The client redirects the user to the ServiceNow authorization endpoint. The method of initiating the authorization request depends on the type of client: Public or Private.

    -   **Public Clients**

        Public clients \(Example: Mobile or Single-page applications\) cannot securely store a client secret. Therefore, they must use **Proof Key for Code Exchange \(PKCE\)** to enhance security.

        -   In the authorization request, include the **PKCE code challenge** and specify the **code challenge method**.
        -   During the token request, the client must send the **code verifier** to validate the authorization code.
        Perform a GET request to the authorization endpoint with the following parameters:

        ```
        Method: GET
        Endpoint: https://<servicenow_base_url>/oauth_auth.do
        ```

<table id="table_oz1_lh2_lgc"><thead><tr><th>

Parameter

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`response_type`

</td><td>

Yes

</td><td>

Set the value to `code` to initiate the authorization code flow.

</td></tr><tr><td>

`client_id`

</td><td>

Yes

</td><td>

The unique identifier for your client application.Format: YOUR\_CLIENT\_ID

</td></tr><tr><td>

`redirect_uri`

</td><td>

Yes

</td><td>

The URI to which ServiceNow sends the authorization code.Example: https://yourapp.com/callback

</td></tr><tr><td>

`code_challenge`

</td><td>

Yes

</td><td>

A base64url-encoded SHA-256 hash of the code verifier. This is used as part of the PKCE flow.

</td></tr><tr><td>

`code_challenge_method`

</td><td>

Yes

</td><td>

Specifies the transformation method used for the code challenge. Set to `S256`.

</td></tr><tr><td>

`scope`

</td><td>

Optional

</td><td>

A space-delimited list of requested scopes.Example: `incident_read incident_write`.

</td></tr><tr><td>

`state`

</td><td>

Yes

</td><td>

A client-generated value used to avoid CSRF attacks. The value is returned unchanged in the redirect URI, enabling the client to validate it.

</td></tr></tbody>
</table>        **Note:** Starting with the Madrid release, the system property `glide.oauth.state.parameter.required` mandates the use of the `state` parameter in the OAuth requests. The `state` property is set to `true` by default in the new instances, and `optional` in upgraded instances. In case of missing `state` parameter, the authorization request fails and the following error is displayed: `Missing State parameter in request`.

    -   **Private Clients**

        Private clients \(Example: Server-side applications\) can securely store a client secret and do not require PKCE.

        -   The authorization request is initiated by redirecting the user to the authorization endpoint. **No client secret or PKCE code challenge is required** in this step.
        -   During the token request, the client includes the **client secret** along with the **authorization code** to obtain the access token.
        Perform a GET request to the authorization endpoint with the following parameters:

        ```
        Method: GET
        Endpoint: https://<servicenow_base_url>/oauth_auth.do
        ```

<table id="table_jg5_5rh_vfc"><thead><tr><th>

Parameter

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`response_type`

</td><td>

Yes

</td><td>

Set the value to `code` to initiate the authorization code flow.

</td></tr><tr><td>

`client_id`

</td><td>

Yes

</td><td>

The unique identifier for your client application.Format: YOUR\_CLIENT\_ID

</td></tr><tr><td>

`redirect_uri`

</td><td>

Yes

</td><td>

The URI to which ServiceNow sends the authorization code.Example: https://yourapp.com/callback

</td></tr><tr><td>

`scope`

</td><td>

Optional

</td><td>

A space-delimited list of requested scopes.Example: `incident_read incident_write`.

</td></tr><tr><td>

`state`

</td><td>

Yes

</td><td>

A client-generated value used to avoid Cross-Site Request Forgery \(CSRF\) attacks. The value is returned unchanged in the redirect URI, enabling the client to validate it.

</td></tr></tbody>
</table>3.  Log in and grant access consent to the client application.

    Log in to ServiceNow \(or IdP, if SSO is enabled\), and grant access consent to the client application.

4.  ServiceNow \(or IdP, if SSO is enabled\) validates the credentials and ServiceNow returns an authorization code to the client.

    After the successful authentication, the browser is redirected to the `redirect_uri`, and the authorization code is included in the query string:

    ```
    https://yourapp.com/callback?code=AUTH_CODE&state=xyz123
    
    ```

5.  Initiate the authorization request.

    The client redirects the user to the ServiceNow authorization endpoint for an access token. The method of initiating the authorization request depends on the type of client: Public or Private.

    -   **Public Clients**

        Public clients \(Example: Mobile or Single-page applications\) cannot securely store a client secret. Therefore, they must use **Proof Key for Code Exchange \(PKCE\)** to enhance security.

        -   In the authorization request, include the **PKCE code challenge** and specify the **code challenge method**.
        -   During the token request, the client must send the **code verifier** to validate the authorization code.
        The client sends a POST request to token endpoint with the following parameters:

        ```
        
        Method: POST  
        Endpoint: https://<servicenow_base_url>/oauth_token.do  
        Headers: Content-Type: application/x-www-form-urlencoded
        ```

<table id="table_ztk_z32_lgc"><thead><tr><th>

Parameter

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grant_type`

</td><td>

Yes

</td><td>

Set the value to `authorization_code` to exchange the code for a token.

</td></tr><tr><td>

`code`

</td><td>

Yes

</td><td>

The authorization code received from the authorization endpoint.

</td></tr><tr><td>

`redirect_uri`

</td><td>

Yes

</td><td>

The URI used in the initial authorization request.Example: https://yourapp.com/callback

</td></tr><tr><td>

`client_id`

</td><td>

Yes

</td><td>

The unique identifier for your client application.

</td></tr><tr><td>

`code_verifier`

</td><td>

Yes

</td><td>

The original string used to generate the PKCE `code_challenge`.

</td></tr><tr><td>

`state`

</td><td>

Yes

</td><td>

A client-generated value used to help prevent CSRF attacks. The value is returned unchanged in the redirect URI, enabling the client to validate it.

</td></tr></tbody>
</table>    -   **Private Clients**

        Private clients \(Example: Server-side applications\) can securely store a client secret and do not require PKCE.

        -   The authorization request is initiated by redirecting the user to the authorization endpoint. **No client secret or PKCE code challenge is required** in this step.
        -   During the token request, the client includes the **client secret** along with the **authorization code** to obtain the access token.
        Perform a POST request to the authorization endpoint with the following parameters:

        ```
        
        Method: POST 
        Endpoint: https://<servicenow_base_url>/oauth_token.do   
        Headers: Content-Type: application/x-www-form-urlencoded
        ```

<table id="table_xlf_y33_vfc"><thead><tr><th>

Parameter

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grant_type`

</td><td>

Yes

</td><td>

Set the value to `authorization_code` to exchange the code for a token.

</td></tr><tr><td>

`code`

</td><td>

Yes

</td><td>

The authorization code received from the authorization endpoint.

</td></tr><tr><td>

`redirect_uri`

</td><td>

Yes

</td><td>

The URI used in the initial authorization request.Example: https://yourapp.com/callback

</td></tr><tr><td>

`client_id`

</td><td>

Yes

</td><td>

The unique identifier for your client application.

</td></tr><tr><td>

`client_secret`

</td><td>

Yes

</td><td>

The client’s secret used to authenticate with the token endpoint.

</td></tr><tr><td>

`state`

</td><td>

Yes

</td><td>

A client-generated value used to help prevent CSRF attacks. The value is returned unchanged in the redirect URI, enabling the client to validate it.

</td></tr></tbody>
</table>6.  Access the ServiceNow APIs with the access token.

    -   **Example:**

        Make a GET request to the APIs using the access token. Include the access token in the `Authorization` header.

    ```
    Method: GET
    End Point: https://<servicenow_base_url>/api/now/incident  
    Authorization: Bearer YOUR_ACCESS_TOKEN
    ```

7.  Renew the access token if it has expired.

    Make a POST request to refresh the access token \(private clients only\) with the following parameters:

    ```
    
    Method: POST  
    Endpoint: https://<servicenow_base_url>/oauth_token.do  
    Headers: Content-Type: application/x-www-form-urlencoded
    ```

    |Parameter|Required|Description|
    |---------|--------|-----------|
    |`grant_type`|Yes|Set the value to `refresh_token` to request a new access token.|
    |`refresh_token`|Yes|The refresh token previously issued by the token endpoint.|
    |`client_id`|Yes|The unique identifier for your client application.|
    |`client_secret`|Yes|The client secret used to authenticate with the token endpoint.|


