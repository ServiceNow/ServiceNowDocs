---
title: REST API Auth Scope
description: Use the REST API Auth Scope to provide access to a specific REST API
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [REST API access policies, API access policy, Authentication, Access Management]
---

# REST API Auth Scope

Use the REST API Auth Scope to provide access to a specific REST API

Earlier, the client without any scope have access to all APIs unless the API is protected by REST API Auth Scope or the client has `useraccount` scope.

After creating REST API Auth Scope record, to access this REST API you must associate the same Auth Scope to the OAuth Entity which should have access to this REST API. For a new OAuth Entity, the default Auth Scope is empty.

**Note:** Unless you have REST API Auth Scope record, the REST API can be accessed by any valid OAuth Entities.

You must manually link the Auth scope within the OAuth Entity. The `useraccount` is a special scope, if it’s associated with an OAuth Entity it can access any API even if you have created a REST API Auth Scope record with a different auth scope.

**Note:**

-   After the REST API Auth scope is enabled and added to the auth scope for the REST API, then all the existing OAuth token won’t able to access this API anymore unless admin adds this auth scope to the corresponded OAuth entity
-   The admin is responsible to making sure the oauth\_entity has the right auth scope after to link the auth scope with the REST API.
-   OAuth access tokens issued by ServiceNow supports the auth scope.
-   OIDC token that is not issued by ServiceNow is validated by ServiceNow.
-   OIDC token has its scope from IDP when you require an ID token. Here the auth scope is for ServiceNow instead of third party \(IdP\).

## Configurations for REST API Scope

To configure the REST API Scope, perform the following tasks:

-   Create an auth scope
-   Link auth scope with the REST API
-   Link auth scope with OAuth entity
-   Perform OAuth flow to get OAuth access token
-   Use the OAuth access token to make the API call

