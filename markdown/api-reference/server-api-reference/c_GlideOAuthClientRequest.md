---
title: GlideOAuthClientRequest - Scoped, Global
description: The GlideOAuthClientRequest API provides methods for handling OAuth client requests.Retrieves the grant type.Retrieves the HTTP headers for the string you provide.Retrieves the HTTP headers.Retrieves the parameters for the parameter name you provide.Retrieves the password.Retrieves the refresh token.Retrieves the scope.Retrieves the user name.Sets the grant type for the string you provide.Retrieves the HTTP headers for the string you provide.Sets the parameters for the name:value pair of strings you provide.Sets the password with the string you provide.Sets the refresh token with the string you provide.Sets the scope for the string you provide.Sets the user name with the string you provide.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideOAuthClientRequest - Scoped, Global

The GlideOAuthClientRequest API provides methods for handling OAuth client requests.

You can use this API in global and scoped scripts. In scoped scripts use the `sn_auth` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideOAuthClientRequest - getGrantType\(\)

Retrieves the grant type.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The grant type.|

## GlideOAuthClientRequest - getHeader\(String name\)

Retrieves the HTTP headers for the string you provide.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the parameter.|

|Type|Description|
|----|-----------|
|StringMap|The string map with the HTTP headers.|

## GlideOAuthClientRequest - getHeaders\(\)

Retrieves the HTTP headers.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|StringMap|The string map with the HTTP headers.|

## GlideOAuthClientRequest - getParameter\(String name\)

Retrieves the parameters for the parameter name you provide.

|Name|Type|Description|
|----|----|-----------|
|name|String|The parameter name for which you want the parameters.|

|Type|Description|
|----|-----------|
|String|The parameters.|

## GlideOAuthClientRequest - getPassword\(\)

Retrieves the password.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The password.|

## GlideOAuthClientRequest - getRefreshToken\(\)

Retrieves the refresh token.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The refresh token.|

## GlideOAuthClientRequest - getScope\(\)

Retrieves the scope.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The scope.|

## GlideOAuthClientRequest - getUserName\(\)

Retrieves the user name.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|The user name.|

## GlideOAuthClientRequest - setGrantType\(String grantType\)

Sets the grant type for the string you provide.

**Note:** You only need to set the grant type if it is not already defined in the OAuth provider profile.

|Name|Type|Description|
|----|----|-----------|
|name|String|The grant type.|

|Type|Description|
|----|-----------|
|void| |

## GlideOAuthClientRequest - setHead\(String name, String value\)

Retrieves the HTTP headers for the string you provide.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the parameter.|
|value|String|The value of the parameter.|

|Type|Description|
|----|-----------|
|void| |

## GlideOAuthClientRequest - setParameter\(String name, String value\)

Sets the parameters for the name:value pair of strings you provide.

|Name|Type|Description|
|----|----|-----------|
|name|String|The parameter name for which you want the parameters.|
|value|String|The value of the parameter.|

|Type|Description|
|----|-----------|
|void| |

## GlideOAuthClientRequest - setPassword\(String password\)

Sets the password with the string you provide.

|Name|Type|Description|
|----|----|-----------|
|password|String|The user name.|

|Type|Description|
|----|-----------|
|void| |

## GlideOAuthClientRequest - setRefreshToken\(String refreshToken\)

Sets the refresh token with the string you provide.

|Name|Type|Description|
|----|----|-----------|
|refreshToken|String|The refresh token.|

|Type|Description|
|----|-----------|
|void| |

This example shows a resource owner password grant type request.

```

     var tokenRequest =new GlideOAuthClientRequest();
     tokenRequest.setGrantType("password");
     tokenRequest.setUserName("itil");
     tokenRequest.setPassword("itil");
     tokenRequest.setScope(null);
 
     var oAuthClient =new GlideOAuthClient();var tokenResponse = oAuthClient.requestToken("TestClient", tokenRequest);
     gs.log("Error:"+ tokenResponse.getErrorMessage());
 
     var token = tokenResponse.getToken();if(token){
       gs.log("AccessToken:"+ token.getAccessToken());
       gs.log("AccessTokenExpiresIn:"+ token.getExpiresIn());
       gs.log("RefreshToken:"+ token.getRefreshToken());

```

This example shows a refresh token grant type request.

```

     var tokenRequest =new GlideOAuthClientRequest();
     tokenRequest.setGrantType("refresh_token");
     tokenRequest.setRefreshToken("N-GtdSVLkWP_Cr-TysXdmNy59ZYafu5ZzAS4YaSluXDm0kCkInEnu-hwM5SsGYSFwKJ6xauVmoaq7xJNoalXFQ");
     tokenRequest.setScope(null);
 
     var oAuthClient =new GlideOAuthClient();
     tokenResponse = oAuthClient.requestToken("TestClient", tokenRequest);
     gs.log("Error:"+ tokenResponse.getErrorMessage());
     token = tokenResponse.getToken();if( token){
        gs.log("AccessToken:"+ token.getAccessToken());
        gs.log("AccessTokenExpiresIn:"+ token.getExpiresIn());
        gs.log("AccessTokenSysID:"+ token.getAccessTokenSysID());
        gs.log("RefreshToken:"+ token.getRefreshToken());
        gs.log("RefreshTokenSysID:"+ token.getRefreshTokenSysID());
```

## GlideOAuthClientRequest - setScope\(String scope\)

Sets the scope for the string you provide.

**Note:** You only need to set the scope if it is not already defined in the OAuth provider.

|Name|Type|Description|
|----|----|-----------|
|scope|String|The scope.|

|Type|Description|
|----|-----------|
|void| |

## GlideOAuthClientRequest - setUserName\(String userName\)

Sets the user name with the string you provide.

|Name|Type|Description|
|----|----|-----------|
|userName|String|The user name.|

|Type|Description|
|----|-----------|
|void| |

