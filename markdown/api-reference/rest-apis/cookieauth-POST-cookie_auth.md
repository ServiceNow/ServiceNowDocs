---
title: Cookie Auth - POST /api/sn\_webrtc/webrtc\_cookie\_auth/cookie\_auth
description: Returns a short-lived ticket that the WebRTC phone widget uses to connect to the voice service and start a call. The endpoint doesn’t require login, so guest users can place calls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/rest-apis/cookieauth-POST-cookie\_auth.html
release: zurich
product: REST APIs
classification: rest-apis
topic_type: reference
last_updated: "2026-10-14"
reading_time_minutes: 3
breadcrumb: [Cookie Auth API, REST API reference, API reference, API implementation and reference]
---

# Cookie Auth - POST /api/sn\_webrtc/webrtc\_cookie\_auth/cookie\_auth

Returns a short-lived ticket that the WebRTC phone widget uses to connect to the voice service and start a call. The endpoint doesn’t require login, so guest users can place calls.

## URL format

Default URL: `/api/sn_webrtc/webrtc_cookie_auth/cookie_auth`

## Trusted orchestrator domains

The Cookie Auth POST endpoint creates a ticket only when the **orchestrator\_host** value matches a domain in the following system property, or is a subdomain of one of those domains. If the property is empty, the endpoint uses the default domain, sncapps.service-now.com.

<table id="table_pvx_gjc_xkc"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

sn\_webrtc.orchestrator.trusted\_domains

</td><td>

Comma-separated list of trusted domains. A host is trusted when it equals one of the domains or is a subdomain of one of them. Only users with the maint role can change this property.Data type: String

</td><td>

sncapps.service-now.com

</td></tr></tbody>
</table>## Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

voice\_service\_id

</td><td>

Required

</td><td>

The sys\_id of the voice service configuration. The value must pass the platform sys\_id check and must also be exactly 32 lowercase hexadecimal characters.Data type: String

Format: 32 lowercase hexadecimal characters

Maximum length: 256

</td></tr><tr><td>

orchestrator\_host

</td><td>

Required

</td><td>

The host name of the voice orchestrator, as a bare host name or an https:// URL. The endpoint rejects http:// URLs and values that include a port, path, query string, or credentials. The host must match a trusted domain exactly or be a subdomain of a trusted domain. For information about trusted domains, see the **Trusted orchestrator domains** section.

Data type: String

Maximum length: 256

</td></tr><tr><td>

instance\_name

</td><td>

Required

</td><td>

ServiceNow instance identifier.Format: `[a-z0-9][a-z0-9-]{0,62}` \(max 63 characters\)

Data type: String

</td></tr></tbody>
</table>## Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td>

Required. Must be application/json. The endpoint rejects any other content type with a 400 status code.

</td></tr><tr><td>

X-UserToken

</td><td>

Required. The session CSRF token for the current session. The endpoint rejects requests with a missing or incorrect token.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

## Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-api-explorer/c_RESTAPI.md).

**Note:** See the 'API rate limits' section [Cookie Auth API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-apis/cookieauth-api.md) for issues around rate limiting.

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. The request wasn't valid. Possible causes include a missing or invalid parameter, a content type other than application/json, a request body larger than 2,048 bytes, or an orchestrator host that isn't trusted. The response doesn't identify which check failed due to a security constraint.

 Response body: `{"error": "Bad Request"}`

</td></tr><tr><td>

502

</td><td>

Bad Gateway. The instance couldn't get a ticket from the voice orchestrator.

 Response body: `{"error": "Bad Gateway"}`

</td></tr></tbody>
</table>## Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ws\_ticket

</td><td>

Ticket that the client uses to open the WebSocket connection to the voice orchestrator. The ticket expires after 60 seconds and can be used only once.Data type: String

</td></tr></tbody>
</table>## cURL request

The following example demonstrates how to use the POST endpoint to request a ticket for a voice service. The request includes the session CSRF token header.

```
curl "https://instance.service-now.com/api/sn_webrtc/webrtc_cookie_auth/cookie_auth" \
        --request POST \
        --header "Accept: application/json" \
        --header "Content-Type: application/json" \
        --header "X-UserToken: session_csrf_token" \
        --data "{\"voice_service_id\": \"0123456789abcdef0123456789abcdef\", \"orchestrator_host\": \"https://myservicenoworchestrator.sncapps.service-now.com\"}"
```

Response body. The response contains the ticket.

```
{
        "ws_ticket": "ticket_value"
        }
```

**Parent Topic:**[Cookie Auth API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/rest-apis/cookieauth-api.md)

