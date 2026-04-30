---
title: API Key and HMAC Authentication for inbound REST APIs
description: Support API tokens for REST API endpoints so that the ServiceNow user name and password isn't visible in the webhook URL.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Token-based authentication, API Authentication, Authentication, Access Management]
---

# API Key and HMAC Authentication for inbound REST APIs

Support API tokens for REST API endpoints so that the ServiceNow® user name and password isn't visible in the webhook URL.

Enable API key-based authentication to securely authenticate inbound webhook URL.

To use the API Key and HMAC Authentication, you must install the \(Plugin: `com.glide.tokenbased_auth`\) in the ServiceNow® instance.

**Warning:** Use **POST** request when submitting any sensitive information to the server.

Installing API Key and HMAC Authentication has dependencies on the following plugins:

-   REST API Auth Scope Plugin \(`com.glide.rest.auth.scope`\)
-   REST API Access Policy Plugin \(`com.glide.rest.policy`\)
-   Authentication scope \(`com.glide.auth.scope`\)

## Benefits

API Key and HMAC Authentication for inbound REST APIs enables:

-   Ability to specify API key or HMAC token for REST API authentication.
-   Ability to associate a user account with the API key or HMAC token.
-   Ability to specify a token as query parameter or header within the REST API call.
-   Ability to associate authentication scope with API key or HMAC token configurations so that API keys can only be used to invoke APIs associated with a particular scopes.
-   Ability to associate an API key or HMAC token configuration with an authentication profile that can be used in API access policies.

