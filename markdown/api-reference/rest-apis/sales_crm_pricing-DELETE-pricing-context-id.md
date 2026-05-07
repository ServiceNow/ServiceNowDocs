---
title: Sales CRM Pricing - DELETE - /api/sn\_csm\_pricing/v1/pricingengine/pricing\_context/\{pricing\_context\_id\}
description: Terminate a session with a given ID that was established during a configurator session.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: reference
last_updated: "2019-10-16"
reading_time_minutes: 1
breadcrumb: [Sales CRM Pricing API, REST API reference, API reference, API implementation and reference]
---

# Sales CRM Pricing - DELETE - /api/sn\_csm\_pricing/v1/pricingengine/pricing\_context/\{pricing\_context\_id\}

Terminate a session with a given ID that was established during a configurator session.

## URL format

Versioned URL: `/api/sn_csm_pricing/v1/pricingengine/pricing_context/{pricing_context_id}`

Default URL: `/api/sn_csm_pricing/pricingengine/pricing_context/{pricing_context_id}`

## Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

pricing\_context\_id

</td><td>

ID from pricing engine request when scope is configurator.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

## Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](../concept/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|status|Indicates the overall outcome of the requested operation.|
|message|A human-readable message that provides more detail about the status. It is useful for logging or for displaying a confirmation to an end-user. In this case, it explicitly states that the deletion was successful.|
|pricing\_context\_id|The unique of the resource that was affected by the operation. By returning the ID, the API confirms exactly which pricing context has been deleted, which helps prevent ambiguity.|

## Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](../concept/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

## Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

## cURL request

```
curl -i -X DELETE \
'https://instance.servicenow.com/api/sn_csm_pricing/v1/pricingengine/pricing_context/{pricing_context_id}' \
--user 'username:password'
```

**Parent Topic:**[Sales CRM Pricing API](../concept/sales-crm-pricing-api.md)

