---
title: GlideOAuthClient - Scoped, Global
description: The GlideOAuthClient API provides methods for requesting and revoking OAuth refresh and access tokens.Retrieves the access and refresh tokens for the client.Retrieves the token for the client, with the request parameters encoded in JSON format.Retrieves the token for the client, with the client name and the request set into a GlideOAuthClientResponse object.Revokes the access or refresh token for the client, with the request and optional header parameters set into a GlideOAuthClientRequest object.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideOAuthClient - Scoped, Global

The GlideOAuthClient API provides methods for requesting and revoking OAuth refresh and access tokens.

You can use this API in global and scoped scripts. In scoped scripts use the `sn_auth` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideOAuthClient - getToken\(String requestID, String oauthProfileID\)

Retrieves the access and refresh tokens for the client.

|Name|Type|Description|
|----|----|-----------|
|requestID|String|Request ID from the OAuth Requestor Profile \[oauth\_requestor\_profile\] table, which references the OAuth Entity Profile \[oauth\_entity\_profile\] table.|
|oauthProfileID|String|OAuth profile ID from the OAuth Entity Profile \[oauth\_entity\_profile\] table.|

|Type|Description|
|----|-----------|
|GlideOAuthToken|The access and refresh tokens for the client.|

This example code shows how to retrieve access and refresh tokens from the instance database.

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

## GlideOAuthClient - requestToken\(String clientName, String jsonString\)

Retrieves the token for the client, with the request parameters encoded in JSON format.

|Name|Type|Description|
|----|----|-----------|
|clientName|String|The client name.|
|jsonString|String|The JSON string for the client.|

|Type|Description|
|----|-----------|
|GlideOAuthClientResponse|The token for the client.|

This example shows a resource owner password grant type request, with request parameters encoded in JSON format.

```

var oAuthClient = new GlideOAuthClient();
var params ={grant_type:"password", username:"itil", password:'itil'};
var json =new JSON();
var text = json.encode(params);
var tokenResponse = oAuthClient.requestToken('TestClient', text);
var token = tokenResponse.getToken();

gs.log("AccessToken:"+ token.getAccessToken());
gs.log("AccessTokenExpiresIn:"+ token.getExpiresIn());
gs.log(" RefreshToken:"+ token.getRefreshToken());

```

## GlideOAuthClient - requestTokenByRequest\(String clientName, GlideOAuthClientRequest request\)

Retrieves the token for the client, with the client name and the request set into a GlideOAuthClientResponse object.

|Name|Type|Description|
|----|----|-----------|
|clientName|String|The client name.|
|request|GlideOAuthClientRequest|The request.|

|Type|Description|
|----|-----------|
|GlideOAuthClientResponse|The token for the client.|

## GlideOAuthClient - revokeToken\(String clientName, String accessToken, String refreshToken, GlideOAuthClientRequest request\)

Revokes the access or refresh token for the client, with the request and optional header parameters set into a GlideOAuthClientRequest object.

|Name|Type|Description|
|----|----|-----------|
|clientName|String|The client name.|
|accessToken|String|The access token.|
|refreshToken|String|The refresh token.|
|request|GlideOAuthClientRequest|The request.|

|Type|Description|
|----|-----------|
|GlideOAuthClientResponse|The token for the client.|

