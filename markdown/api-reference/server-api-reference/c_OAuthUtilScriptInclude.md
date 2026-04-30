---
title: OAuthUtil - Global
description: The OAuthUtil script include modifies request parameters and parses the token response during runtime.Returns a GlideRecord representing the current OAuth profileAdds a name:value pair to the request parameters.Parses the token received into a parameter map.Set the endpoiont for your OAuth requestAdd a header to an outbound token request.Add a query parameter to an OAuth request.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OAuthUtil- Global

The OAuthUtil script include modifies request parameters and parses the token response during runtime.

If the external OAuth provider returns a response other than an application/JSON type response, you can customize your own version of this script include to parse responses that are in different format. Extend or copy this script include, and then reference your version from the **OAuth API Script** field on the Application Registry form for third-party OAuth providers. The custom script include name must start with `OAuth`.

For example, if the OAuth provider requires a resource parameter with value `https://outlook.office365.com`, the code would look like:

```
preprocessAccessToken: function(requestParamMap) {
  requestParamMap.put("resource", "https://outlook.office365.com");
},
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OAuthUtil - getOAuthProfile\(\)

Returns a GlideRecord representing the current OAuth profile

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord representing the current OAuth profile|

## OAuthUtil - interceptRequestParameters\(requestParamMap\)

Adds a name:value pair to the request parameters.

|Name|Type|Description|
|----|----|-----------|
|requestParamMap|String|The name:value pair you want to add.|

|Type|Description|
|----|-----------|
|void| |

## OAuthUtil - parseTokenResponse\(accessTokenResponse\)

Parses the token received into a parameter map.

|Name|Type|Description|
|----|----|-----------|
|accessTokenResponse|String|The access token response that you want to parse.|

|Type|Description|
|----|-----------|
|void| |

## OAuthUtil - setEndpoint\(url\)

Set the endpoiont for your OAuth request

|Name|Type|Description|
|----|----|-----------|
|url|String|URL endpoint for your request|

|Type|Description|
|----|-----------|
|void| |

## OAuthUtil - setHeader\(headerName, headerValue\)

Add a header to an outbound token request.

|Name|Type|Description|
|----|----|-----------|
|headerName|String|Name of your token request header|
|headerValue|String|Value of your token request header|

|Type|Description|
|----|-----------|
|void| |

## OAuthUtil - setQueryParameter\(paramName, paramValue\)

Add a query parameter to an OAuth request.

|Name|Type|Description|
|----|----|-----------|
|paramName|String|Name of your parameter|
|paramValue|String|Value of your parameter|

|Type|Description|
|----|-----------|
|void| |

