---
title: Generate a JSON Web Token \(JWT\)
description: Create a JSON Web Token \(JWT\) for representing claims securely between two parties on the ServiceNow AI Platform.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JWT Bearer, OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# Generate a JSON Web Token \(JWT\)

Create a JSON Web Token \(JWT\) for representing claims securely between two parties on the ServiceNow AI Platform.

The GlideJWT API is a scoped, scriptable API which generates a JWT. There are three arguments necessary before generating the JWT:

-   Sys\_id of [JWT Provider](../task/JWT-Bearer-token-support.md#)
-   JSON serialized header
-   JSON serialized payload

There are two JWT API scripts, JWTTokenInternal and JWTTokenRestricted, that you can use when configuring a JWT Provider. The JWTTokenRestricted script enables administrators to configure who can generate a JWT. The JWTTokenInternal script is read-only and enables only logged in users to generate a JWT.

To generate a JWT:

-   [Create a JWT Key with a shared key \(HMAC\) or a signing keystore \(RSA\)](../task/JWT-Bearer-token-support.md#)
-   [Associate a JWT provider with the signing configuration referring a JWT key](../task/JWT-Bearer-token-support.md#)

You can use the API to create your token.

You can use standard and custom claims when configuring a JWT provider. You can pass dynamic header and payload claims as part of the generateJWT API signature.

Sample script to test API:

```
var jwtAPI = new sn_auth.GlideJWTAPI();
var headerJSON = {  "kid": "a1234"  };
var header = JSON.stringify(headerJSON);

var payloadJSON = { "jti": "testjti", "iss": "testiss", "sub": "testsub" };
var payload = JSON.stringify(payloadJSON);

var jwtProviderSysId = "7a40dde2d5303300964fb7c8f3c14ab5";
var jwt = jwtAPI.generateJWT(jwtProviderSysId, header, payload);

gs.info("JWT:" + jwt);
```

