---
title: REST OAuth example
description: This example shows how to authenticate an inbound REST request using OAuth.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/rest-api-explorer/r\_RESTOAuthExample.html
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Enable OAuth with inbound REST, REST APIs, Web services, API implementation, API implementation and reference]
---

# REST OAuth example

This example shows how to authenticate an inbound REST request using OAuth.

In this example, the OAuth application registry entry has a client ID of `example_client_id` and a client secret of `example_client_secret`. Replace these values, and the user name and password shown in the examples, with the values for your own OAuth application and REST user.

## Getting an access token

To request an access token, send a POST request to the oauth\_token.do endpoint of your instance. This example uses the password grant type and passes the client ID, client secret, and the credentials of the user the token is issued for. Replace the placeholder values with your own.

```cmd
curl -d "grant_type=password&client_id=example_client_id&client_secret=example_client_secret&username=example_user&password=example_password" https://<instance>.service-now.com/oauth_token.do
```

## Sample token response

If the request succeeds, the instance returns a JSON response like the following. The **access\_token** value is the token you pass in the Authorization header of subsequent requests. The **refresh\_token** value can be used to request a new access token after the current one expires. The **expires\_in** value is the number of seconds until the access token expires. The token values shown here are placeholders, not real tokens.

```json
{
  "scope": "useraccount",
  "token_type": "Bearer",
  "expires_in": 1799,
  "refresh_token": "example_refresh_token_value",
  "access_token": "example_access_token_value"
}
```

## REST request with OAuth token

To call a REST API with the token, include it in the Authorization header with the Bearer prefix. This example uses the access token from the previous response to retrieve records from the Incident table \(Table API\). Replace `example_access_token_value` with the **access\_token** value returned for your request.

```cmd
curl -H "Accept: application/json" -H "Authorization: Bearer example_access_token_value" "https://<instance>.service-now.com/api/now/table/incident"
```

**Parent Topic:**[Enable OAuth with inbound REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/t_EnableOAuthWithREST.md)

