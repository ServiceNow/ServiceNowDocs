---
title: OAuth authorization code grant flow
description: Authorization code grant flow allows a user to access a resource by authenticating directly with an OAuth server that trusts the resource, in contrast with authenticating with username/password credentials.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Old Inbound integrations experience, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# OAuth authorization code grant flow

Authorization code grant flow allows a user to access a resource by authenticating directly with an OAuth server that trusts the resource, in contrast with authenticating with username/password credentials.

This implementation of OAuth authorization code flow allows access to a resource via REST. The authorization code framework gets the access token through the authorized URL that the user configures rather than requiring the user to enter a username/password. The username/password are never exposed to the client that is requesting access to the resource.

## A ServiceNow instance as the authorization server

The OAuth server is typically a third-party authorization server. You can also specify a ServiceNow instance as the authorization server that issues the tokens for authorization code flow.

The user who owns the restricted resource must authorize access. The user can also revoke the issued access token at any time to terminate access.

## Authorization code grant flow process

The Authorization code grant flow process consists of these three steps:

![Authorization code grant flow process](../../../product/discovery/image/AuthCodeGrantFlow1.png)

In step one, the client application or website initiates a REST API call in the form of a GET request to the instance via the user agent. Typically, the REST call is initiated when the end user clicks a button or a link on the client application or website to request an access token. In the client application, the end user also has to specify the authorization URL, token URL, client ID, and client secret. For an explanation of these items, see the field descriptions in this topic: [Use a third-party OAuth provider](https://www.servicenow.com/docs/access?context=t_UseAThirdPartyOAuthProvider&version=australia&pubname=australia-api-reference&ft:locale=en-US). If the client asks for a grant type, the end user must select **Authorization Code**.

Example GET request from the client application to the instance:

```
https://myinstance.service-now.com/oauth_auth.do?response_type=code&redirect_uri={the_redirect_url}&client_id={the_client_identifier}
```

**Note:** The **response\_type** must be **code** to use the standard OAuth code grant flow.

The end user must manually allow access to the restricted resource on the instance. In the ServiceNow implementation, the end user must be logged into the instance. The instance prompts the end user with a UI page that has **Allow** and **Deny** buttons.

The item that the client application is actually requesting the token from is the OAuth provider application registry record that you created, also known as the authorization endpoint \(see [Use a third-party OAuth provider](https://www.servicenow.com/docs/access?context=t_UseAThirdPartyOAuthProvider&version=australia&pubname=australia-api-reference&ft:locale=en-US)\). The auth code is sent from the authorization endpoint to the client. It does not go to the client directly but to the **Redirect URL** that you specify on the authorization endpoint form. This URL is also known as a callback URL. You can obtain this URL from the client application or website.

Example response from the instance to the client application, providing an authorization code:

```
https/http://{callbackURL}?code={the actual auth code}
```

![Client application sends auth code to ServiceNow instance, which in turn sends a token](../../../product/discovery/image/AuthCodeGrantFlow2.png)

Now that the client application has the authorization code, the client uses the code to request the access token. The authorization code proves that the user has consented in step 1.

Example POST request from the client application to the ServiceNow instance that provides the auth code and requests the access token:

```
https://myinstance.service-now.com/oauth_token.do?grant_type=authorization_code&code={the auth code}&redirect_uri={the_same_redirect_url}&client_id={the_same_client_identifier}&client_secret={client_secret_value}
```

The endpoint on the instance returns an access token and a refresh token. The refresh token can be used to request additional access tokens.

You can manage the tokens, including revoking the token, in the instance. See [Manage OAuth tokens](../task/t_ManageTokens.md).

![Client application sends a token to ServiceNow instance, which then sends a JSON payload of data](../../../product/discovery/image/AuthCodeGrantFlow3.png)

The client application uses the access token to authenticate to the REST API. After authenticating the client application, the REST API returns the requested data in a JSON payload.

Example GET request for the JSON payload of data for the Incident \[incident\] table:

```
https://myinstance.service-now.com/api/now/table/incident?access_token={the_token}
```

**Note:** The system also supports [OAuth implicit grants](c_OAuthImplicitGrants.md), also known as implicit grant code flow.

## Integration support

Authorization code flow supports the following integrations on the instance:

-   Multi-SSO
-   SAML 2.0 Update 1
-   Multifactor authentication

The mobile interface is also supported.

