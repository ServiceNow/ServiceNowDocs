---
title: GlideOAuthClientResponse - Scoped, Global
description: The GlideOAuthClientResponse API provides methods for handling OAuth client responses.Retrieves all of the response information, including instance information.Retrieves the HTTP response content header from an external OAuth provider.Retrieves the error message if authentication is not successful.Retrieves the HTTP response code from the external OAuth provider.Retrieves the error message if authentication is not successful.Retrieves the refresh token.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideOAuthClientResponse - Scoped, Global

The GlideOAuthClientResponse API provides methods for handling OAuth client responses.

You can use this API in global and scoped scripts. In scoped scripts use the `sn_auth` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideOAuthClientResponse - getBody\(\)

Retrieves all of the response information, including instance information.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The response information.|

## GlideOAuthClientResponse - getContentType\(\)

Retrieves the HTTP response content header from an external OAuth provider.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The HTTP response header.|

## GlideOAuthClientResponse - getErrorMessage\(\)

Retrieves the error message if authentication is not successful.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The error message.|

## GlideOAuthClientResponse - getResponseCode\(\)

Retrieves the HTTP response code from the external OAuth provider.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The HTTP response code.|

## GlideOAuthClientResponse - getResponseParameters\(\)

Retrieves the error message if authentication is not successful.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|MapString|The response content.|

## GlideOAuthClientResponse - getToken\(\)

Retrieves the refresh token.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|GlideOAuthToken|The refresh token.|

