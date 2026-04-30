---
title: GlideOAuthToken - Scoped, Global
description: The GlideOAuthToken API provides methods for retrieving OAuth access token and information about the access token.Retrieves the access token associated with the GlideOAuthToken object.Deprecated. Retrieves the sys\_id of the token ID associated with the GlideOAuthToken object.Retrieves the lifespan of the access token associated with the GlideOAuthToken object.Refreshes the token associated with the GlideOAuthToken object.Deprecated. Retrieves the sys\_id of the refresh token.Retrieves the token scope, which is the amount of access granted by the access token.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideOAuthToken - Scoped, Global

The GlideOAuthToken API provides methods for retrieving OAuth access token and information about the access token.

You can use this API in global and scoped scripts. In scoped scripts use the `sn_auth` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideOAuthToken - getAccessToken\(\)

Retrieves the access token associated with the GlideOAuthToken object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Access token.|

This example code shows how to retrieve access and refresh tokens from the instance database. See also [GlideOAuthClient](../../GlideOAuthClient/concept/c_GlideOAuthClient.md#).

```
function dumpToken(token) {
  if(token) {
     gs.info("AccessToken:" + token.getAccessToken());
     gs.info("AccessTokenExpiresIn:" + token.getExpiresIn());
     gs.info("RefreshToken:" + token.getRefreshToken());
  }
}

var oAuthClient = new  sn_auth.GlideOAuthClient();
var token = oAuthClient.getToken('248e3017c302301089a7dd5c2840dda5', '9c4e78d3c302301089a7dd5c2840dd76');
dumpToken(token);
```

Output:

```
*** Script: AccessToken:6MRxD3TRYYvIaoKr-JCy3KiaOxBPu4C9k8oafo3MYf9q8zDyHQr8UzMSM3Md2alfaES1rzSYe5ydqgbOwpm7TA
*** Script: AccessTokenExpiresIn:1207
*** Script: RefreshToken:sc0iTK-0PcVkRi14HXPM3vT0FyOPO8iCqC10huQoDSSLBGUSnmEv_fUfJzGWCWBb_StsXIOz6r8qF-hRhURWTA
```

## GlideOAuthToken - getAccessTokenSysID\(\)

Deprecated. Retrieves the sys\_id of the token ID associated with the GlideOAuthToken object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the access token.|

## GlideOAuthToken - getExpiresIn\(\)

Retrieves the lifespan of the access token associated with the GlideOAuthToken object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_rc4_bzf_cr" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number \(Long\)

</td><td>

Lifespan of the token.Unit: Seconds

</td></tr></tbody>
</table>This example code shows how to retrieve access and refresh tokens from the instance database. See also [GlideOAuthClient](../../GlideOAuthClient/concept/c_GlideOAuthClient.md#).

```
function dumpToken(token) {
  if(token) {
     gs.info("AccessToken:" + token.getAccessToken());
     gs.info("AccessTokenExpiresIn:" + token.getExpiresIn());
     gs.info("RefreshToken:" + token.getRefreshToken());
  }
}

var oAuthClient = new  sn_auth.GlideOAuthClient();
var token = oAuthClient.getToken('248e3017c302301089a7dd5c2840dda5', '9c4e78d3c302301089a7dd5c2840dd76');
dumpToken(token);
```

Output:

```
*** Script: AccessToken:6MRxD3TRYYvIaoKr-JCy3KiaOxBPu4C9k8oafo3MYf9q8zDyHQr8UzMSM3Md2alfaES1rzSYe5ydqgbOwpm7TA
*** Script: AccessTokenExpiresIn:1207
*** Script: RefreshToken:sc0iTK-0PcVkRi14HXPM3vT0FyOPO8iCqC10huQoDSSLBGUSnmEv_fUfJzGWCWBb_StsXIOz6r8qF-hRhURWTA
```

## GlideOAuthToken - getRefreshToken\(\)

Refreshes the token associated with the GlideOAuthToken object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Refreshed token.|

This example code shows how to retrieve access and refresh tokens from the instance database. See also [GlideOAuthClient](../../GlideOAuthClient/concept/c_GlideOAuthClient.md#).

```
function dumpToken(token) {
  if(token) {
     gs.info("AccessToken:" + token.getAccessToken());
     gs.info("AccessTokenExpiresIn:" + token.getExpiresIn());
     gs.info("RefreshToken:" + token.getRefreshToken());
  }
}

var oAuthClient = new  sn_auth.GlideOAuthClient();
var token = oAuthClient.getToken('248e3017c302301089a7dd5c2840dda5', '9c4e78d3c302301089a7dd5c2840dd76');
dumpToken(token);
```

Output:

```
*** Script: AccessToken:6MRxD3TRYYvIaoKr-JCy3KiaOxBPu4C9k8oafo3MYf9q8zDyHQr8UzMSM3Md2alfaES1rzSYe5ydqgbOwpm7TA
*** Script: AccessTokenExpiresIn:1207
*** Script: RefreshToken:sc0iTK-0PcVkRi14HXPM3vT0FyOPO8iCqC10huQoDSSLBGUSnmEv_fUfJzGWCWBb_StsXIOz6r8qF-hRhURWTA
```

## GlideOAuthToken - getRefreshTokenSysID\(\)

Deprecated. Retrieves the sys\_id of the refresh token.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the refresh token.|

## GlideOAuthToken - getScope\(\)

Retrieves the token scope, which is the amount of access granted by the access token.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Scope of the access token.|

