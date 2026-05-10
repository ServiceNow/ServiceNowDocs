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

-   [GlideOAuthClient](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideOAuthClient.md): Methods for requesting and revoking the refresh and access tokens.
-   [GlideOAuthClientRequest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideOAuthClientRequest.md): Methods for handling client requests.
-   [GlideOAuthClientResponse](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideOAuthClientResponse.md): Methods for handling client responses.
-   [GlideOAuthToken](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideOAuthToken.md): Methods for retrieving the access token and information about the access token.

You can also customize the OAuthUtil script include to intercept the request parameters and also parse the responses from external OAuth providers.

When using OAuth classes in a scoped script, use the `sn_auth` namespace identifier.

