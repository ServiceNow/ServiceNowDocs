---
title: OAuth 2.0
description: OAuth 2.0 lets users access instance resources through external clients by obtaining a token rather than by entering login credentials with each resource request.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [servicenow OAuth, Servicenow OAuth, ServiceNow OAuth, OAuth authentication, inbound authentication, outbound authentication, OAuth 2.0, OAuth provider, OAuth client, token endpoint, authorization server, resource server, OAuth scope, OAuth grant types]
breadcrumb: [OAuth authentication, Authentication, Access Management]
---

# OAuth 2.0

OAuth 2.0 lets users access instance resources through external clients by obtaining a token rather than by entering login credentials with each resource request.

You must have the security\_admin role to manage the OAuth integration. Configure OAuth 2.0 for the following scenarios:

-   **OAuth external client scenario** \(Inbound\): Your instance provides an endpoint for third-party clients to pull data from the instance.
-   **OAuth provider scenario** \(Outbound\): Your instance pulls data from a third-party provider.

**Note:** You must user authenticate for the first time to fetch the token post which, you don't need to authenticate using a user account before the token expiry.

Both, simple security and high security frameworks support OAuth 2.0. High Security is recommended. See for information about which versions have high security already active and how to activate high security.

## Key concepts of the OAuth 2.0 implementation

<table id="table_jlt_dmv_yq"><thead><tr><th>

Concept

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource Owner

</td><td>

An entity capable of granting access to a protected resource. A resource owner who is a person is called an end user. The resource owner is always a user account.

</td></tr><tr><td>

Client

</td><td>

An application that, with the authorization of the resource owner, makes requests for protected resources on behalf of the resource owner.

</td></tr><tr><td>

Resource Server

</td><td>

The server that hosts the protected resources, capable of accepting and responding to requests for protected resources.

</td></tr><tr><td>

Authorization Server

</td><td>

The server that issues access tokens to the client after successfully authenticating the resource owner and obtaining authorization.

</td></tr><tr><td>

Authorization Request

</td><td>

The permission that a client requires to access a protected resource. The authorization request is always an HTTP POST message that contains the ID of the client that is acting on behalf of the resource owner and credentials that authorize the request.

</td></tr><tr><td>

Authorization Grant

</td><td>

A credential that represents the authorization from the resource owner to access a resource. The authorization grant is either user login credentials or a refresh token.

</td></tr><tr><td>

Access Token

</td><td>

A secure string that a client uses to access protected resources. An instance issues access tokens to clients that have a valid authorization grant. Each access token has a specific scope, lifespan, and other attributes. By default, an instance issues access tokens with a 30-minute lifespan in the scenario where the instance is the OAuth provider. For third-party tokens, 30 days.

</td></tr><tr><td>

Refresh Token

</td><td>

A credential that a client uses to obtain new access tokens without requiring additional user authorization. An instance issues a refresh token to a client when it is first authorized to have an access token. By default, an instance issues refresh tokens with a 100-day lifespan in the scenario where the instance is the OAuth provider. For third-party tokens, 365 days.

</td></tr><tr><td>

Self-signed certificates

</td><td>

The ServiceNow AI Platform does not support self-signed certificates. The OAuth client does not utilize the certificate trust store or allow connection to OAuth endpoints that incorporate a self-signed certificate.

</td></tr><tr><td>

User agent

</td><td>

The user who delegates access rights to a client application, which is often a website. The access rights permit the client application or website to access data in the instance that the user has access rights to. The user agent is used in the scenario.

</td></tr></tbody>
</table>## OAuth grant types

A grant type is the way that the client obtains the access token. The following grant types are supported:

-   **Authorization code**: The consumer first gets an authorization code and then uses it to get an access token. You can [Specify an OAuth profile](https://www.servicenow.com/docs/access?context=t_SpecifyAnOAuthProfile&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) and specify this grant type. The process that uses the authorization code is also referred to as auth code flow or authorization code flow.
-   **Resource owner password credentials**: The consumer of the resource already has the user credentials to get the access token. This process is also referred to as password flow.
-   **Client credentials**: The consumer of the resource uses the client ID and client secret that is already configured in the application registry.

## Storage of authentication credentials

The OAuth client secret is stored as a **password2** type field, which is encrypted with KMF. User passwords, which are used to check incoming endpoint requests, are stored as a hash value in the User table in a **password** type field \(SHA 256\). For details on this encryption, see [Password2 encryption with KMF](../../key-management-framework/concept/password-2way-encrypted-fields.md)

