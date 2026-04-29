---
title: OAuth API response parameters
description: The OAuth 2.0 API produces a JSON response containing the following parameters as name:value pairs.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an endpoint for clients to access the instance, Old Inbound integrations experience, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# OAuth API response parameters

The OAuth 2.0 API produces a JSON response containing the following parameters as name:value pairs.

|Response parameter|Description|
|------------------|-----------|
|scope|Amount of access granted by the access token. The scope is always **useraccount**, meaning that the access token has the same rights as the user account that authorized the token. For example, if Abel Tuter authorizes an application by providing login credentials, then the resulting access token grants the token bearer the same access privileges as Abel Tuter.|
|token\_type|Type of token issued by the request as defined in the OAuth RFC. The token type is always **Bearer**, meaning that anyone in possession of the access token can access a protected resource without providing a cryptographic key. See [RFC6750](http://tools.ietf.org/html/rfc6750) for more information about how OAuth 2.0 uses bearer tokens.|
|expires\_in|Lifespan of the access token in seconds.|
|refresh\_token|String value of the refresh token.|
|access\_token|String value of the access token. Access requests made within the access token expiration time always return the current access token.|
|format|\[Optional\] Output format of the response. This value is always JSON.|

**Note:** If any OAuth provider sends the response body as "content-type" instead of "Content-Type", the OAuth HTTP client may not parse the response correctly. To correct this issue, create a system property using these parameters.

|Field|Value|
|-----|-----|
|Name|glide.oauth.inhouse.httpclient.enabled|
|Type|true\|false|
|Value|false|

For details on creating system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

The following example illustrates the JSON string returned by an access token request. \(Spaces have been added to improve readability\).

```

{"scope":"useraccount","token_type":"Bearer","expires_in":1800,
"refresh_token":"w599voG89897rGVDmdp12WA681r9E5948c1CJTPi8g4HGc4NWaz62k6k1K0FMxHW40H8yOO3Hoe",
"access_token":"F0jh9korTyzd9kaZqZ0SzjKZuS3ut0i4P46Lc52m2JYHiLIcqzFAumpyxshU9mMQ13gJHtxD2fy"}

```

