---
title: OAuth Inbound
description: OAuth Inbound authentication allows trusted external applications to securely access ServiceNow APIs, ensuring controlled and authorized connections.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [OAuth authentication, Authentication, Access Management]
---

# OAuth Inbound

OAuth Inbound authentication allows trusted external applications to securely access ServiceNow APIs, ensuring controlled and authorized connections.

You must have one of the following roles to configure or manage OAuth integrations in the system:

-   `oauth_admin`
-   `mi_admin`
-   `admin`

Inbound authentication enables external applications such as third-party systems or other ServiceNow® instances to connect securely to ServiceNow APIs. Inbound authentication confirms that only trusted clients can access your ServiceNow instance in a controlled and secure manner. ServiceNow supports several OAuth 2.0 grant types, each designed for specific integration scenarios. Use the following information to choose the grant type that best fits your use case:

## Authorization Code Grant

<table id="table_bs4_2jj_wfc"><thead><tr><th>

Ideal usage scenario

</th><th>

Functionality

</th></tr></thead><tbody><tr><td>

Applications that must access user data on behalf of user with the user’s consent.Example: Web, mobile, or desktop applications acting on behalf of a user.

</td><td>

The user initiates the login process from the client application, which redirects them to a ServiceNow login page. After the user logs in and grants consent, the client application receives an authorization code. The client application exchanges the authorization code with the ServiceNow instance for an access token. Authorization code grant is the most secure and widely used workflow for user-facing integrations. It supports both confidential clients \(with a client secret\) and public clients using Proof Key for Code Exchange \(PKCE\).

</td></tr></tbody>
</table>For more information about Authorization code grant workflow and configuration, see 

## Client Credentials Grant

|Ideal Usage Scenario|Functionality|
|--------------------|-------------|
|Client applications such as back-end services or automated system integrations that must access ServiceNow APIs without user involvement.|The client application authenticates directly with the ServiceNow instance using its own credentials \(client ID and secret\). Once authenticated, the application receives an access token to access the ServiceNow APIs.|

For more information about Client credentials grant workflow and configuration, see .

## Third party ID Token Flow

|Ideal Usage Scenario|Functionality|
|--------------------|-------------|
|Federated authentication scenarios where ServiceNow trusts identity tokens issued by external identity providers such as Azure AD or Okta.|The client application obtains an ID or access token from a trusted third-party identity provider, and includes it in the authorization header when making API requests to the ServiceNow instance. ServiceNow validates the token and, if trusted, grants access based on the identity it asserts. This enables seamless single sign-on \(SSO\) and federated authentication across systems.|

For more information about Third party token flow and configuration, see.

## JWT Bearer Grant

<table id="table_vn1_zjj_wfc"><thead><tr><th>

Ideal Usage Scenario

</th><th>

Functionality

</th></tr></thead><tbody><tr><td>

Client applications that need secure access to ServiceNow resources, either on behalf of a user or as themselves, without requiring user interaction or storing a shared secret.The client application creates a signed JSON Web Token \(JWT\) that includes identity-related claims, such as the user or system it represents. It then presents it to the ServiceNow instance to request for access token.

</td><td>

-   **When acting on behalf of a user:**

The token represents a previously authenticated user. This enables secure, seamless access without prompting the user for credentials or consent again. The signed token asserts the user’s identity, enabling ServiceNow to trust the request without requiring real-time user interaction.

-   **When acting as itself:**

The token identifies and authenticates the client application directly. Instead of using a shared secret, the client signs the token with a private key, making it a more secure alternative to the client credentials grant.


</td></tr></tbody>
</table>For more information about JWT bearer grant workflow and configuration, see .

## Resource Owner Password Credentials Grant

|Ideal Usage Scenario|Functionality|
|--------------------|-------------|
|Highly trusted internal client applications in controlled environments where the app collects the user’s credentials directly.|The client application collects the user’s user name and password, and redirects them to the ServiceNow instance to obtain an access token. The workflow bypasses redirection and consent screens, but exposes user credentials to the client application. ServiceNow recommends that you implement the Resource owner password credentials grant only in legacy or controlled environments.|

For more information about Resource owner password credentials grant workflow and configuration, see .

## Implicit Grants

<table id="table_wmj_2lt_xfc"><thead><tr><th>

Ideal Usage Scenario

</th><th>

Functionality

</th></tr></thead><tbody><tr><td>

Legacy Single-page applications \(SPAs\) or browser-based apps that can’t securely store a client secret, and require a lightweight, client-side authentication flow.

</td><td>

The user logs in through a browser. The client application receives the access token directly in the URL after login, bypassing the intermediate authorization code step. This flow was originally designed for public clients that run entirely in the browser, where securely storing secrets isn’t possible. While it simplifies implementation, it exposes tokens in the browser, increasing the risk of interception. For stronger security, ServiceNow recommends implementing an authorization code grant with PKCE.

</td></tr></tbody>
</table>For more information about Implicit grant workflow and configuration, see [OAuth implicit grants](../../../administer/security/concept/c_OAuthImplicitGrants.md).

## OAuth Scopes

You can scope the OAuth authentication scope support for REST API. OAuth Scope provides access to only the particular REST APIs. For more information, see [REST API Auth Scope](../../../administer/security/concept/rest-api-auth-scope.md).

