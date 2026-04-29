---
title: OAuth client APIs
description: The OAuth client API provides methods to request and revoke OAuth tokens.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# OAuth client APIs

The OAuth client API provides methods to request and revoke OAuth tokens.

The OAuth client provides these classes:

-   [GlideOAuthClient](https://www.servicenow.com/docs/access?context=c_GlideOAuthClient&version=australia&pubname=australia-api-reference&ft:locale=en-US): Methods for requesting and revoking the refresh and access tokens.
-   [GlideOAuthClientRequest](https://www.servicenow.com/docs/access?context=c_GlideOAuthClientRequest&version=australia&pubname=australia-api-reference&ft:locale=en-US): Methods for handling client requests.
-   [GlideOAuthClientResponse](https://www.servicenow.com/docs/access?context=c_GlideOAuthClientResponse&version=australia&pubname=australia-api-reference&ft:locale=en-US): Methods for handling client responses.
-   [GlideOAuthToken](https://www.servicenow.com/docs/access?context=c_GlideOAuthToken&version=australia&pubname=australia-api-reference&ft:locale=en-US): Methods for retrieving the access token and information about the access token.

You can also customize the OAuthUtil script include to intercept the request parameters and also parse the responses from external OAuth providers.

When using OAuth classes in a scoped script, use the `sn_auth` namespace identifier.

