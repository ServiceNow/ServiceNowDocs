---
title: Change OAuth password parameter
description: Use this property to ensure only POST body parameters are accepted as input for all supported grant types.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth 2.0, OAuth authentication, Authentication, Access Management]
---

# Change OAuth password parameter

Use this property to ensure only POST body parameters are accepted as input for all supported grant types.

Sending sensitive information over URI query parameters might lead to sensitive information disclosure by clients, the server, or any host between the requests. Starting with the Madrid release, this new property ensures only the POST body parameters are accepted as input for all supported grant types. Supported grant types include:

-   authorization code
-   password
-   client credential
-   refresh token

|Property|Description|
|--------|-----------|
|`glide.oauth.allow.parameters.in.post.body.only`|This property is set to true for zBoots only, as part of the OAuth 2.0 plugin. If you need this setting for your instance, create and set the property to true.|

