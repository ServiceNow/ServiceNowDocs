---
title: JWT Authentication
description: The Verifi Issuer API uses JSON Web Tokens \(JWT\) for authentication. A fresh JWT must be generated for every API call. This section explains how to store credentials securely and how the ServiceNow script generates and attaches the JWT.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# JWT Authentication

The Verifi Issuer API uses JSON Web Tokens \(JWT\) for authentication. A fresh JWT must be generated for every API call. This section explains how to store credentials securely and how the ServiceNow® script generates and attaches the JWT.

|Header|Value Format|Description|
|------|------------|-----------|
|Authorization|Bearer &lt;encoded JWT&gt;|Base64url-encoded JWT signed with HMAC SHA-256 using the shared secret.|
|x-verifi-issuer|&lt;Issuer ID&gt;|Your numeric Issuer ID assigned by Verifi. This value must match the iss claim in the JWT payload.|

<table><thead><tr><th>

Type

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Header

</td><td>

```
{ "alg": "HS256", "typ": "JWT" } 
```

</td></tr><tr><td>

Payload

</td><td>

```
{ "iss": "<issuer_id>", "jti": "<UUID — unique per call>", "iat": <epoch_now>, "exp": <epoch_now + 299> } 
```

</td></tr></tbody>
</table>|Claim|Required|Description / Validation Rule|
|-----|--------|-----------------------------|
|iss|Yes|Set to your numeric Issuer ID as a string. Must match the x-verifi-issuer header exactly.|
|jti|Yes|A UUID generated fresh for every request. Verifi rejects duplicate jti values from the same issuer — use crypto.randomUUID\(\) or equivalent.|
|iat|Yes|Unix epoch timestamp \(UTC\) at the moment the JWT is constructed. Must be a number, not a string. Verifi rejects values more than 300 seconds in the past or any value in the future.|
|exp|Yes|Unix epoch timestamp \(UTC\) for token expiration. Must be a number. Must not exceed iat + 300 seconds. Recommended: set to iat + 299.|

**Note:** Both iat and exp must be numeric \(integer\) Unix epoch values and not ISO 8601 date strings. Passing a string will cause Verifi to return a 401 Unauthorized error.

**Parent Topic:**[../concept/referring-financial-services-operations-integration-with-verifi-cdrn.md](../concept/referring-financial-services-operations-integration-with-verifi-cdrn.md)

