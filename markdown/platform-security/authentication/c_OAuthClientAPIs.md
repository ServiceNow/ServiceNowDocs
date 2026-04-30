---
title: OAuth client APIs
description: The OAuth client API provides methods to request and revoke OAuth tokens.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth outbound, OAuth authentication, Authentication, Access Management]
---

# OAuth client APIs

The OAuth client API provides methods to request and revoke OAuth tokens.

The OAuth client provides these classes:

-   [GlideOAuthClient](https://www.servicenow.com/docs/access?context=c_GlideOAuthClient&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Methods for requesting and revoking the refresh and access tokens.
-   [GlideOAuthClientRequest](https://www.servicenow.com/docs/access?context=c_GlideOAuthClientRequest&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Methods for handling client requests.
-   [GlideOAuthClientResponse](https://www.servicenow.com/docs/access?context=c_GlideOAuthClientResponse&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Methods for handling client responses.
-   [GlideOAuthToken](https://www.servicenow.com/docs/access?context=c_GlideOAuthToken&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Methods for retrieving the access token and information about the access token.

You can also customize the OAuthUtil script include to intercept the request parameters and also parse the responses from external OAuth providers.

When using OAuth classes in a scoped script, use the `sn_auth` namespace identifier.

