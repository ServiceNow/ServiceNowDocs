---
title: REST OAuth example
description: This example shows how to authenticate an inbound REST request using OAuth.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enable OAuth with inbound REST, REST APIs, Web services, API implementation, API implementation and reference]
---

# REST OAuth example

This example shows how to authenticate an inbound REST request using OAuth.

In this example, the OAuth token has a `client_id` of `a329c4515612210071a5e0c298ee2be8` and a `client_secret` of `password22`.

## Getting an access token

```cmd
curl -d "grant_type=password&client_id=a329c4515612210071a5e0c298ee2be8&client_secret=password22&username=RESTUser&password=RESTUserPassword"  https://<instance>.service-now.com/oauth_token.do
```

## Sample token response

```json
{
"scope": "useraccount",
"token_type": "Bearer",
"expires_in": 1799,
"refresh_token": "jZPdkEVrWvtMjrspldNjIS0uWM4D7QV9mgmcQXDVo5Qa_GVvmdR6NOp7OM038EHJnd6nZpWocFer1NcJz4zwdw",
"access_token": "2wRlsRCT2SYjCCJP91kwo2EFzj5qg4O3I3aC09e0-0hz6Ib3YK7If-LMiNorNuglfqbkL4AfkYC92KYHUCcbpQ"
}
```

## REST request with OAuth token

```cmd
curl -H "Accept:application/json" -H "Authorization:Bearer 2wRlsRCT2SYjCCJP91kwo2EFzj5qg4O3I3aC09e0-0hz6Ib3YK7If-LMiNorNuglfqbkL4AfkYC92KYHUCcbpQ"  "https://<instance>.service-now.com/api/now/table/incident
```

**Parent Topic:**[Enable OAuth with inbound REST](../task/t_EnableOAuthWithREST.md)

