---
title: GlideJWTAPI - Scoped
description: Use the GlideJWT API to create a JSON Web Token \(JWT\) for representing claims securely between two parties on the ServiceNow AI Platform.Generates a JSON Web Token \(JWT\).
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideJWTAPI- Scoped

Use the GlideJWT API to create a JSON Web Token \(JWT\) for representing claims securely between two parties on the ServiceNow AI Platform.

This API is provided within the `sn_auth` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideJWTAPI - generateJWT\(String jwtProviderSysId, String jsonSerializedHeader, String jsonSerializedPayload\)

Generates a JSON Web Token \(JWT\).

JWTs consist of three parts: a header, payload, and signature.

<table id="table_oqs_wxg_qbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

jwtProviderSysId

</td><td>

String

</td><td>

Sys\_id of the JWT provider.Table: JWT Provider \[jwt\_provider\]

</td></tr><tr><td>

jsonSerializedHeader

</td><td>

String

</td><td>

Optional. JSON header of the payload.Default: Uses the claims from the JWT provider record.

</td></tr><tr><td>

jsonSerializedPayload

</td><td>

String

</td><td>

Optional. JSON payload.Default: Uses the claims from the JWT provider record.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The generated JWT.|

This example generates a JWT using the claims from the JWT provider record.

```
var jwtAPI = new sn_auth.GlideJWTAPI();

var jwtProviderSysId = "ce7d1a62a3660210f1565f87f31e61f7";
var jwt = jwtAPI.generateJWT(jwtProviderSysId, null, null);

gs.info("JWT:" + jwt);
```

Output:

```
JWT:eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJhdWQiOiI5YzZlMmQxNzU0MzMyMDEwMDFhMTE4Y2FhMGVhMmE0MyIsInN1YiI6ImFkbWluQGV4YW1wbGUuY29tIiwiaXNzIjoiaHR0cHM6Ly9kb21haW4uZXhhbXBsZS5jb20iLCJleHAiOjE3MTc2MDc0MjQsImlhdCI6MTcxNzYwNzM2NCwianRpIjoiMjUzMjRjOWItMzlhMS00ZTc4LWEzNzItMGZjNzA2ZWE2ZDgxIn0.UwfdJzdMNE1zAyOFsaGGKPqatbSgDdYi_LjBwj9KUtKRRLyEDWuS7fErl_6W1_5dvhvtEPPGwBq84FcIjIzdNe17-zTi6tRaVIMfC8PDd2emjlKM1NgyYV1lzGQyDpafl4V0FixqFp1jB-_4XejN2UvWbMT9ylOoPALYGII13R8VabVYdknMOxBO8KMyOefxcAhS2OVFDFfozwMJtgJosPls3bzK1f0_WvGZDEBLdbDobzvrYjqNPIcmYk7pvyJ-ROeaxxj5h4erR4H8gFF_pG8bAxnLnFRMTzp-ZsbALMnC-B331jqj0Pi5gHsfTCNCV-zvGkyQwFwSfLB9uBo1gw
```

Decoded JWT:

```
{
  "typ": "JWT",
  "alg": "RS256"
}
.
{
  "aud": "9c6e2d175433201001a118caa0ea2a43",
  "sub": "admin@example.com",
  "iss": "https://domain.example.com",
  "exp": 1717607424,
  "iat": 1717607364,
  "jti": "25324c9b-39a1-4e78-a372-0fc706ea6d81"
}
```

This example generates a JWT using custom claims.

```
var jwtAPI = new sn_auth.GlideJWTAPI();

var headerJSON = {  "kid": "a1234"  };
var header = JSON.stringify(headerJSON);

var payloadJSON = { "iss": "override_value_in_JWT_provider_record", "custom_claim_1": "custom_claim_1_value" };
var payload = JSON.stringify(payloadJSON);

var jwtProviderSysId = "ce7d1a62a3660210f1565f87f31e61f7";
var jwt = jwtAPI.generateJWT(jwtProviderSysId, header, payload);

gs.info("JWT:" + jwt);
```

Output:

```
JWT:eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6ImExMjM0In0.eyJhdWQiOiI5YzZlMmQxNzU0MzMyMDEwMDFhMTE4Y2FhMGVhMmE0MyIsInN1YiI6ImFkbWluQGV4YW1wbGUuY29tIiwiaXNzIjoib3ZlcnJpZGVfdmFsdWVfaW5fSldUX3Byb3ZpZGVyX3JlY29yZCIsImN1c3RvbV9jbGFpbV8xIjoiY3VzdG9tX2NsYWltXzFfdmFsdWUiLCJleHAiOjE3MTc2MDc4MTksImlhdCI6MTcxNzYwNzc1OSwianRpIjoiNjE3YjMyMjQtYjZmZi00MGZmLTliY2QtNTQ5YTdhNTk4YjkzIn0.Oi6AW0KW8i9yyBgWZnVGDKIqK_GYhIlHMigeNBU141nYXJNhLuk36455TwDKj2z40NMI-nqRaxoVIfo1XQiR7_oXuKnmNSDHQJofedq9sQVFbnQmmPnYNzG-01CVTx4xOm_KdPF_WrWvOqj5nyiqPC7fkjEkVbhXDsygRWcoghRrazFwbmS1ujXbs0sXap99uEexiJfUZ0Ad7bjvQ-T1Wh5Sc4LKZguH-egAze98mxQCiMNQAZLAfSs9qPEnXMe8EjXZnPaz3-wMH4KVUGR_gT49XPWkp4081tX7acE77j_55TvCxVyqAGWIOEqI6hlAO_bQmM35pCvN4NSek_GxbQ
```

Decoded JWT:

```
{
  "alg": "RS256",
  "typ": "JWT",
  "kid": "a1234"
}
.
{
  "aud": "9c6e2d175433201001a118caa0ea2a43",
  "sub": "admin@example.com",
  "iss": "override_value_in_JWT_provider_record",
  "custom_claim_1": "custom_claim_1_value",
  "exp": 1717607819,
  "iat": 1717607759,
  "jti": "617b3224-b6ff-40ff-9bcd-549a7a598b93"
}
```

