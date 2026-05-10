---
title: Authorization code grant workflow
description: ServiceNow handles both authentication and API access by acting as the authorization and resource server. When single sign-on \(SSO\) is enabled, it redirects users to the configured IdP for authentication and issues tokens after successful login.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 5
breadcrumb: [OAuth Code Grant, Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Authorization code grant workflow

ServiceNow® handles both authentication and API access by acting as the authorization and resource server. When single sign-on \(SSO\) is enabled, it redirects users to the configured IdP for authentication and issues tokens after successful login.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## About this task

This topic collection provides information about how ServiceNow manages authentication and API access when acting as both the authorization server and the resource server. It describes the behavior when SSO is enabled, including redirection to the identity provider \(IdP\) for user authentication and the issuance of an authorization code by ServiceNow after successful authentication. The usage of authorization code ensures that ServiceNow retains control over token issuance and access to protected resources.

![Authorization Workflow](../../machine-identity/images/mic-authorization-flow.png "Authorization workflow")

## Procedure

1.  Log in from the client application.

    The user begins the login process from the client application interface.

2.  Initiate the authorization request.

    The client redirects the user to ServiceNow authorization endpoint to initiate the authorization request. The authorization request can be initiated either by including the `Client Secret` or `PKCE Code Challenge` in the request body, based on the client type- private or public. In the authorization request body, include `Client Secret` for private clients, and `PKCE Code Challenge` for public clients.

    -   **For Private clients**

        Include the `Client Secret` in the request body, while initiating the token request for private clients. Follow the procedure to initiate the authorization request using `Client Secret` for private clients.

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

Yes

</td><td>

A space-delimited list of requested scopes.Example: `incident_read incident_write`.

</td></tr><tr><td>

`state`

</td><td>

Yes

</td><td>

A client-generated value used to avoid Cross-Site Request Forgery \(CSRF\) attacks. The value is returned unchanged in the redirect URI, enabling the client to validate it

</td></tr></tbody>
</table>    -   **For Public clients**

        Include the `PKCE Code Challenge` in the request body, while initiating the token request for public clients. Follow the procedure to initiate the authorization request using `PKCE Code Challenge` for public clients.

        Perform a GET request to the authorization endpoint with the following parameters:

        ```
        Method: GET
        Endpoint: https://<servicenow_base_url>/oauth_auth.do
        ```

<table id="table_ez2_nsh_vfc"><thead><tr><th>

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

Yes

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

3.  Grant access consent to the client application.

    Access the ServiceNow login page \(or IdP, if SSO is enabled\), and grant access consent to the client application.

4.  ServiceNow \(or IdP, if SSO is enabled\) validates the credentials and ServiceNow returns an authorization code to the client.

    After the successful authentication, the browser is redirected to the `redirect_uri`, and the authorization code is included in the query string:

    ```
    https://yourapp.com/callback?code=AUTH_CODE&state=xyz123
    
    ```

5.  The client exchanges the authorization code for an access token \(and a refresh token, if it’s a private client\) by making a call to ServiceNow’s token endpoint.

    The authorization code for access token can be initiated either by including the `Client Secret` or `PKCE Code Challenge` in the request body, based on the client type- private or public. In the token request body, include `Client Secret` for private clients, and `PKCE Code Challenge` for public clients.

    -   **For Private clients**

        Include the `Client Secret` in the request body, while initiating the token request for private clients. Follow the procedure to initiate the token request using `Client Secret` for private clients.

        In case of private clients, the client sends a `POST` request to token endpoint with the following parameters:

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
</table>    -   **For Public clients**

        Include the `PKCE Code Challenge` in the request body, while initiating the token request for public clients. Follow the procedure to initiate the authorization request using `PKCE Code Challenge` for public clients.

        The client sends a POST request to token endpoint with the following parameters:

        ```
        
        Method: POST  
        Endpoint: https://<servicenow_base_url>/oauth_token.do  
        Headers: Content-Type: application/x-www-form-urlencoded
        ```

<table id="table_qzd_gk3_vfc"><thead><tr><th>

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


