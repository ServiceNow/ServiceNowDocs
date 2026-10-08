---
title: Product Offering Qualification API
description: The Product Offering Qualification API determines eligibility for product offerings in the ServiceNow product catalog, scoped to a customer account, sales channel, and geographic location. Implements the TM Forum TMF679 standard.Synchronously evaluates one or more product offerings for eligibility. Returns green \(eligible\) or red \(ineligible\) per item, with structured reasons for ineligible items.Discovers eligible product offerings for a given customer, channel, and location context. Supports category filtering and pagination via limit and offset query parameters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/product-offering-qualification-api.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 28
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Product Offering Qualification API

The Product Offering Qualification API determines eligibility for product offerings in the ServiceNow® product catalog, scoped to a customer account, sales channel, and geographic location. Implements the TM Forum TMF679 standard.

The TMF679 Product Offering Qualification API is offered with the Telecommunications Open API application. It implements the [TM Forum TMF679 standard](https://www.tmforum.org/resources/standard/tmf679-product-offering-qualification-api-rest-specification-r19-0-0/).

The API exposes two operations:

-   Check Product Offering Qualification: Validates a caller-supplied list of specific product offerings. Use this at the point of sale when confirming a customer's cart or a known shortlist. Enforced via configurable system property `sn_tmf_api.cpoq.max_items_per_request` \(default: 20 items\). This ensures the synchronous API remains within acceptable response times. Items beyond that limit are returned unprocessed.
-   Query Product Offering Qualification: Discovers which offerings in the catalog are eligible for a given context. Use this to populate a storefront or drive CPQ catalog filtering. Supports category filtering, place-based eligibility scoping, and pagination via `limit` and `offset`query parameters.

## API Access and Requirements

The Product Offering Qualification runs in the sn\_tmf\_api namespace and requires the `sn_tmf_api.product_offering_qualification_integrator` role. Administrators must add the following roles to the `sn_tmf_api.product_offering_qualification_integrator` role to enable access to the Product Offering Qualification API:

-   `sn_customerservice.customer_data_viewer`
-   `sn_csm_ctxrul_mgt.rule_matrix_viewer`

The API requires manual installation of the app-csm-price-mtrx \(sn\_csm\_price\_mtrx\) application for product and pricing rules to work.

Pre-call setup required: **ProductOfferings** must be defined in the Product Catalog. Account, Channel, and Location records referenced in requests must exist. `sn_prd_pm.ProductEligibilityAPI` must be configured with eligibility rules.

## Extending the API

Both operations expose default extension script includes that can be overridden to inject custom business logic before the final response is assembled.

|Script Include|Method|
|--------------|------|
|CheckProductOfferingQualificationExtension|checkProductOfferingQualificationExtension|
|QueryProductOfferingQualificationExtension|queryProductOfferingQualificationExtension|

Both extensions receive the request payload and the built **contextJson** object. Return the \(optionally modified\) **contextJson**. If the Query extension returns a structurally invalid context, the API logs the error and falls back to the default-built context.

## Defining eligibility rules and context variables

The eligibility engine \(`sn_prd_pm.ProductEligibilityAPI`\) evaluates each product offering against a set of configurable eligibility rules. To support new context variables \(such as a custom customer attribute, a new channel type, or additional geographic data\) or to define new eligibility rules that consume them, see [Define product eligibility rules in a product eligibility matrix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-define-eligibility-rules.md). This documentation covers how to create eligibility rule records, configure rule conditions, define context variables, and map them to the eligibility engine context that both CPOQ and QPOQ pass at runtime.

## Check endpoint extension script: Custom extension to inject a partner flag

This extension detects when a request is coming through the partner channel and sets a custom partner flag in the context header. The eligibility engine can then use this flag to apply partner-specific eligibility rules when evaluating the product offerings. You can customize the logic to apply channel-specific markings, validate partner permissions, or enforce special pricing and eligibility constraints for different sales channels.

```
var CheckProductOfferingQualificationExtension = Class.create();

CheckProductOfferingQualificationExtension.prototype = {
  initialize: function() {
    // Initialization logic here
  },

  checkProductOfferingQualificationExtension: function(payload, contextJson) {
    if (payload.channel && payload.channel.id === 'PARTNER') {
      contextJson.header.custom_partner_flag = true;
    }
    return contextJson;
  },

  type: 'CheckProductOfferingQualificationExtension'
};
```

## Query endpoint extension script: Custom extension to apply segment and channel-based filtering

This extension retrieves the customer segment from the account record and adds it to the context for segment-based eligibility filtering. It also excludes specific product categories for partner channel queries and returns the modified context for the eligibility engine to evaluate. You can customize the logic to match your business rules; filtering by geography, account status, subscription history, and other account-specific attributes.

```
var QueryProductOfferingQualificationExtension = Class.create();

QueryProductOfferingQualificationExtension.prototype = {
  initialize: function() {
    // Initialization logic here
  },

  queryProductOfferingQualificationExtension: function(payload, contextJson) {
    // Add customer segment to context for segment-based filtering
    if (payload.relatedParty && payload.relatedParty.length > 0) {
      var accountId = payload.relatedParty[0].partyOrPartyRole.id;
      var accountGR = new GlideRecord('customer');
      if (accountGR.get(accountId)) {
        contextJson.header.customer_segment = accountGR.getValue('segment');
      }
    }
    
    // Exclude certain categories for specific channels
    if (payload.channel && payload.channel.id === 'partner') {
      contextJson.header.exclude_categories = ['premium_only', 'internal_use'];
    }
    
    return contextJson;
  },

  type: 'QueryProductOfferingQualificationExtension'
};
```

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/api-rest.md)

## Product Offering Qualification - POST /api/sn\_tmf\_api/product\_offering\_qualification\_api/v1/checkProductOfferingQualification

Synchronously evaluates one or more product offerings for eligibility. Returns green \(eligible\) or red \(ineligible\) per item, with structured reasons for ineligible items.

Use this operation when you already have a specific list of product offerings and need to verify eligibility for a customer.

Typical scenarios:

-   Validating items in a customer's shopping cart before checkout.
-   Confirming eligibility of a pre-defined product bundle.
-   Batch-checking a known set of offerings against account, channel, and location.

The maximum number of `checkProductOfferingQualificationItem` entries per request is enforced via system property `sn_tmf_api.cpoq.max_items_per_request` \(default: 20 items\). Items beyond the limit are returned unprocessed.

### URL format

Default URL: `/api/sn_tmf_api/product_offering_qualification_api/v1/checkProductOfferingQualification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Sales channel through which the customer is interacting \(for example, `"web"`\). When provided, the eligibility engine applies any channel-specific eligibility rules. The **channel.id** must match an existing channel value; a missing or empty `id` is rejected with a 400.

Data type: Object

```
"channel": {
 "id": "String",
 "@type": "String"
}
```

</td></tr><tr><td>

channel.id

</td><td>

Choice value identifying the channel. Mandatory when **channel** is present. This is the value field from the sys\_choice table for the channel field, not a sys\_id. An empty string is rejected with a 400 validation error.

Example: `"web"`

Data type: String

</td></tr><tr><td>

channel.type

</td><td>

Discriminator for the channel object. Mandatory when **channel** is present. Set to `"ChannelRef"`.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem

</td><td>

Required. List of product offerings to evaluate for eligibility. Must contain at least one entry.Each element is a `CheckProductOfferingQualificationItem` object that identifies a specific product offering and optionally provides location context.

Processing is capped at the value of system property `sn_tmf_api.cpoq.max_items_per_request` \(default: 20\); items beyond this limit are included in the response without `qualificationItemResult` set, and a `warnings` array is added to the response.

Data type: Array of Objects

```
"checkProductOfferingQualificationItem": [
 {
   "@type": "String",
   "productOffering": {Object},
   "place": [Array]
 }
]
```

</td></tr><tr><td>

checkProductOfferingQualificationItem.@type

</td><td>

Required. Discriminator for the item object. Set to `"CheckProductOfferingQualificationItem"`. Informational; the API does not enforce this value but it's recommended for TMF compliance.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place

</td><td>

Geographic location context scoped to this individual item. Use this to supply the service or billing address for location-based eligibility rules. Each entry in the array represents one location with a `role` \(e.g. service address vs billing address\) and a `place` typed as either a reference to an existing Location record \(`PlaceRef`\) or inline address fields \(`GeographicAddress`\).

Providing duplicate `role` values within one item causes that item to be returned ineligible. Omit the field entirely \(or supply an empty array\) for location-agnostic evaluation.

Data type: Array of Objects

```
"place": [
 { 
 "@type": "string",
 "role": "String",
 "place": {Object}
 }
]
```

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.@type

</td><td>

Mandatory when a place entry is present. Discriminator for the place wrapper. Set to `"Place"`.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.@type

</td><td>

Determines how the location is identified. Mandatory when a place entry is present. Two values are supported:-   `"PlaceRef"`: Reference to an existing Location record in the instance. Provide only the **id** field; no other address fields are permitted.
-   `"GeographicAddress"`: Inline address. Provide address fields \(**city**, **country**, etc.\); **id** is not permitted.

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.city

</td><td>

City name for the inline geographic address. Only applicable when **@type** is `"GeographicAddress"`. Used by location-based eligibility rules to match service territories.Example: `"San Diego"`

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.country

</td><td>

Country name or ISO country code. Only applicable when **@type** is `"GeographicAddress"`.Example: `"US"`, `"France"`

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.id

</td><td>

Sys\_id of the Location record in the instance. Required when **@type** is `"PlaceRef"`. Must refer to an existing Location record; an unresolved ID causes the item to be returned as ineligible \(`"red"`\).

Must not be provided when **@type** is `"GeographicAddress"`.

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.postcode

</td><td>

Postal or ZIP code. Only applicable when **@type** is `"GeographicAddress"`. Eligibility rules can use this for postcode-based service territory matching.Example: `"92101"`, `"75001"`

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.stateOrProvince

</td><td>

State or province name. Only applicable when **@type** is `"GeographicAddress"`.Example: `"CA"`, `"California"`

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.streetName

</td><td>

Street name without the number. Only applicable when **@type** is `"GeographicAddress"`. When **streetNumber** is also provided, the API combines them as `"{streetNumber} {streetName}"` for eligibility rule matching.Example: `"Main St"`

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.place.streetNumber

</td><td>

Street number. Prepended to **streetName** when present.Example: `"123"`

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.place.role

</td><td>

Conditional. Mandatory when a place entry is present. Valid values: serviceLocation, billingLocation.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.productOffering

</td><td>

Required. Reference to the product offering to evaluate. The eligibility engine looks up this offering in the Product Catalog by its `id`. If the offering does not exist, the item receives `qualificationItemResult: "red"` with an eligibility reason explaining the lookup failure.

Data type: Object

```
"productOffering": {
 "id": "String",
 "@type": "String"
}
```

</td></tr><tr><td>

checkProductOfferingQualificationItem.productOffering.@type

</td><td>

Required. Discriminator for the product offering reference. Set to `"ProductOfferingRef"`. Informational; recommended for TMF compliance.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.productOffering.id

</td><td>

Required. Sys\_id or external ID of the offering. When an external ID maps to multiple versions, the latest version is used for evaluation. If the ID does not resolve to a known offering, the item is returned as ineligible \(`"red"`\) with an eligibility reason.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Required. Identifies the customer account for which qualification is being checked. Must contain at least one entry. The eligibility engine uses the referenced account to apply customer-specific eligibility rules \(for example, existing subscriptions, customer segment\).

If multiple entries are provided, only the first is used and a `warnings` entry is added to the response.

Data type: Array of Objects

```
"relatedParty" [
 { 
  "@type": "RelatedParty",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Required. Discriminator for this related party entry. Set to `"RelatedParty"`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

The account reference nested inside the related party. Contains the **@type** discriminator and the `id` that identifies the customer account.Data type: Object

```
"partyOrPartyRole": {
 "@type": "String",
 "id": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Discriminator for the account reference. Mandatory when **partyOrPartyRole** is present. Must be exactly `"AccountRef"`. Any other value \(for example, `"IndividualRef"`\) causes the API to return a 400 error because only account-based eligibility is supported.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the customer account record. Mandatory when `partyOrPartyRole` is present. The eligibility engine loads this account to apply account-level eligibility rules. The request is rejected with a 400 if the account does not exist.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

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
|Content-Type|`application/json`|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|`200 OK`|Qualification processed successfully. All valid items have `qualificationItemResult` set. Items beyond the 20-item limit are returned without qualification fields. Note: if a `PlaceRef` ID is not found, the item is returned with `qualificationItemResult: "red"` and an eligibility reason — this is still a **200** response, not an error.|
|`400`|Validation errors — schema failure, missing/empty `checkProductOfferingQualificationItem`, invalid `relatedParty`, channel, or geographic address. Response includes `code`, `reason`, `message`, and `details` array.|
|`401`|Unauthenticated — missing or invalid credentials. Enforced by the platform REST framework.|
|`403`|Forbidden — caller lacks the `sn_tmf_api.product_offering_qualification_integrator` role. Enforced by the REST endpoint ACL.|
|`429`|Too Many Requests — rate limit of 6,000 req/hr exceeded. Response includes a `Retry-After` header.|
|`500`|Unhandled exception during processing.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

TMF discriminator for the top-level response object. Always `"CheckProductOfferingQualification"`.Data type: String

</td></tr><tr><td>

state

</td><td>

Processing state of the qualification request. Always `"done"` on a successful 200 response, indicating all submitted items have been evaluated \(or marked as over-limit\).Data type: String

</td></tr><tr><td>

provideAlternative

</td><td>

Flag that indicates whether alternative product offerings are included in the response for ineligible items. Always `false` in the current implementation; the API does not suggest alternatives.Data type: Boolean

Default: false

</td></tr><tr><td>

provideResultReason

</td><td>

Flag that indicates whether eligibility result reasons are included for ineligible items. Always `true` — the `eligibilityResultReason` array is populated on `"red"` items.Data type: Boolean

Default: true

</td></tr><tr><td>

effectiveQualificationDate

</td><td>

Time stamp at which the eligibility engine processed this request. Useful for audit and debugging. Correlates with server-side log entries.Format: `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Echo of the `relatedParty` array from the request. Returned as-is so callers can correlate the response with the originating request. Absent from the response when `relatedParty` was not provided in the request.Data type: Array of Objects

```
"relatedParty": [
 {
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

checkProductOfferingQualificationItem

</td><td>

Result array. One entry for every item submitted in the request, in the same order. Items within the processing limit have `qualificationItemResult` set; items beyond the limit do not. Always the same length as the input array.Data type: Object

```
"checkProductOfferingQualificationItem": {
 "@type": "String",
 "state": "String",
 "productOffering": {Object},
 "qualificationItemResult": "String",
 "eligibilityResultReason": [Array]
}
```

</td></tr><tr><td>

checkProductOfferingQualificationItem.@type

</td><td>

TMF discriminator for the result item. Always `"CheckProductOfferingQualificationItem"`. Informational; the API does not enforce this value but it's recommended for TMF compliance.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.state

</td><td>

Processing state of this individual item. Always `"done"` for items that were evaluated by the eligibility engine. Items beyond the processing limit also receive `"done"` but will not have `qualificationItemResult` set.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.productOffering

</td><td>

Echo of the `productOffering` reference from the request item — returned so callers can match each result back to its input without relying on array index.Data type: Object

```
"productOffering": {
 "@type": "String",
 "id": "String"
}
```

</td></tr><tr><td>

checkProductOfferingQualificationItem.productOffering.@type

</td><td>

Discriminator for the product offering reference. Always `"ProductOfferingRef"`. Informational; recommended for TMF compliance.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.productOffering.id

</td><td>

Sys\_id or external ID of the product offering from the request item.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.qualificationItemResult

</td><td>

Eligibility verdict for this item.Two values are possible:

-   `"green"`: The offering is eligible for the customer and context provided. The customer can be offered this product.
-   `"red"`: The offering is ineligible.

See **eligibilityResultReason** for the specific reasons. Absent for items beyond the processing limit.

**Note:** An unpublished offering that isn't explicitly excluded by an eligibility rule still returns `"green"`.

Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.eligibilityResultReason

</td><td>

Present only when **qualificationItemResult** is `"red"`. Contains one or more reason objects explaining why the offering was found ineligible.Data type: Array of Objects

```
"eligibilityResultReason": [
{
  "@type": "String",
  "label": "String" 
 }
]
```

</td></tr><tr><td>

checkProductOfferingQualificationItem.eligibilityResultReason.@type

</td><td>

Always `"EligibilityResultReason"`.Data type: String

</td></tr><tr><td>

checkProductOfferingQualificationItem.eligibilityResultReason.label

</td><td>

Human-readable description of the disqualifying rule or condition. Example: `"The product offer is ineligible"`, `"PlaceRef id not found"`.

Data type: String

</td></tr><tr><td>

warnings

</td><td>

Present when the number of submitted items exceeded the processing limit set by the `sn_tmf_api.cpoq.max_items_per_request` system property.Contains the message: "The request exceeds the default line item limit. Only the line items within the default limit were considered for processing."

The over-limit items are still returned in `checkProductOfferingQualificationItem` without a `qualificationItemResult`.

Data type: Array of Strings

</td></tr><tr><td>

code

</td><td>

Numeric error code. Present only on error responses \(4xx / 5xx\). Identifies the specific error condition.For example: Validation failure category

Data type: Integer

</td></tr><tr><td>

reason

</td><td>

Short human-readable error category. Present only on error responses. Example: `"Invalid Place Information"`

Data type: String

</td></tr><tr><td>

message

</td><td>

Detailed error message. Present only on error responses. Usually the same as **reason** for validation errors, or a stack-trace summary for 500 errors.Data type: String

</td></tr><tr><td>

details

</td><td>

List of per-field validation errors. Present only on 400 error responses.Data type: Array of Objects

```
"details": {
  "message": "String",
  "datapath": "String"
}
```

</td></tr><tr><td>

details.message

</td><td>

Description of the specific field error.Data type: String

</td></tr><tr><td>

details.datapath

</td><td>

JSON path to the offending field.For example: `"/checkProductOfferingQualificationItem[0]/place[0]/role"`

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example checks whether specific product offerings are available and qualified for an account at the specified service and billing locations.

```
curl -X POST \
  "https://<instance>.service-now.com/api/sn_tmf_api/product_offering_qualification_api/v1/checkProductOfferingQualification" \
  -H "Content-Type: application/json" \
  -H "Authorization: Basic <base64-credentials>" \
  -d '{
    "@type": "CheckProductOfferingQualification",
    "relatedParty": [
      {
        "@type": "RelatedParty",
        "partyOrPartyRole": {
          "@type": "AccountRef",
          "id": "<account-sys-id>"
        }
      }
    ],
    "channel": { "id": "web", "@type": "ChannelRef" },
    "checkProductOfferingQualificationItem": [
      {
        "@type": "CheckProductOfferingQualificationItem",
        "productOffering": { "@type": "ProductOfferingRef", "id": "<product-offering-sys-id-1>" },
        "place": [
          {
            "@type": "Place",
            "role": "serviceLocation",
            "place": {
              "@type": "GeographicAddress",
              "city": "San Diego",
              "country": "US",
              "stateOrProvince": "CA",
              "streetNumber": "123",
              "streetName": "Main St",
              "postcode": "92101"
            }
          }
        ]
      },
      {
        "@type": "CheckProductOfferingQualificationItem",
        "productOffering": { "@type": "ProductOfferingRef", "id": "<product-offering-sys-id-2>" },
        "place": [
          {
            "@type": "Place",
            "role": "billingLocation",
            "place": { "@type": "PlaceRef", "id": "<place-sys-id>" }
          }
        ]
      }
    ]
  }'
```

Response body.

```
{
  "@type": "CheckProductOfferingQualification",
  "state": "done",
  "provideAlternative": false,
  "provideResultReason": true,
  "effectiveQualificationDate": "2026-08-20 10:30:00",
  "relatedParty": [
    {
      "@type": "RelatedParty",
      "partyOrPartyRole": { "@type": "AccountRef", "id": "<account-sys-id>" }
    }
  ],
  "checkProductOfferingQualificationItem": [
    {
      "@type": "CheckProductOfferingQualificationItem",
      "state": "done",
      "productOffering": { "@type": "ProductOfferingRef", "id": "<product-offering-sys-id-1>" },
      "qualificationItemResult": "green"
    },
    {
      "@type": "CheckProductOfferingQualificationItem",
      "state": "done",
      "productOffering": { "@type": "ProductOfferingRef", "id": "<product-offering-sys-id-2>" },
      "qualificationItemResult": "red",
      "eligibilityResultReason": [
        { "@type": "EligibilityResultReason", "label": "The product offer is ineligible" }
      ]
    }
  ]
}
```

## Product Offering Qualification - POST /api/sn\_tmf\_api/product\_offering\_qualification\_api/v1/queryProductOfferingQualification

Discovers eligible product offerings for a given customer, channel, and location context. Supports category filtering and pagination via limit and offset query parameters.

Use this operation when you need to discover which offerings are eligible for a customer without a pre-defined list.

Typical scenarios:

-   Populating a dynamic storefront or catalog UI filtered by customer eligibility.
-   CPQ catalog filtering based on account and location.
-   Finding available offerings in a specific product category for a given context.

### URL format

Default URL: `/api/sn_tmf_api/product_offering_qualification_api/v1/queryProductOfferingQualification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

limit

</td><td>

Max number of items to return. Non-numeric value or value exceeding MAX\_LIMIT returns a 404 error.Data type: String

Default: 20 \(configurable via the sn\_tmf\_api.pagination.set\_limit system parameter.\)

Maximum: 100 \(configurable via the sn\_tmf\_api.pagination.maximum\_limit system parameter\).

</td></tr><tr><td>

offset

</td><td>

Zero-based index of the first result. Non-numeric value or value ≥ totalCount \(when totalCount &gt; 0\) returns a 404 error.Data type: String

Default: 0

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Required. TMF discriminator for the request body. Set to `"QueryProductOfferingQualification"`. Informational; recommended for TMF conformance.Data type: String

</td></tr><tr><td>

category

</td><td>

Optional. Filters the catalog query to a specific product category. When provided, only offerings that belong to the referenced category are evaluated and returned. This is useful for building category-specific storefronts or CPQ catalog panels.

The id must refer to an existing Product Category record.

Data type: Object

```
"category": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

category.@type

</td><td>

Conditional. Discriminator for the category reference. Mandatory when **category** is present. Set to `"CategoryRef"`.Data type: String

</td></tr><tr><td>

category.id

</td><td>

Conditional. Sys\_id of the Product Category record. Mandatory when **category** is provided. The API filters the catalog to offerings linked to this category. A non-existent ID returns a 400 validation error.

Data type: String

</td></tr><tr><td>

channel

</td><td>

Optional. Identifies the sales channel for this query. When provided, the eligibility engine applies channel-specific rules and may restrict results to offerings available through this channel. The channel is also echoed back in the response.

The ID must match an existing Channel record; a missing or empty id is rejected with a 400.

Data type: Object

```
"channel": {
 "id": "String",
 "@type": "String"
}
```

</td></tr><tr><td>

channel.@type

</td><td>

Conditional. Discriminator for the channel object. Mandatory when **channel** is present. Set to `"ChannelRef"`.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Conditional. The choice value identifying the channel. Mandatory when **channel** is present. This is the value field from the sys\_choice table for the channel field \(for example, `"web"`\), not a sys\_id.

An empty string is rejected with a 400 validation error.

Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Optional. Display name of the channel. Informational; echoed back in the response.Example: `"Web"`, `"Retail"`

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Required. Identifies the customer account for which the catalog query is run. The eligibility engine uses this account to apply customer-segment and account-level eligibility rules; results are personalized to this customer. Must contain at least one entry. If more than one entry is provided, only the first is used and a warnings message is added to the response.

Data type: Array of Objects

```
"relatedParty" [
 { 
  "@type": "RelatedParty",
  "partyOrPartyRole": {Object},
  "role": "String"
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Required. Discriminator for this related party entry. Set to `"RelatedPartyOrPartyRole"`. Used to validate the entry structure.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Optional. The account reference nested inside the related party. Contains the discriminator and the sys\_id of the customer account to qualify against.

 Data type: Object

 ```
"partyOrPartyRole": {
 "@type": "String",
 "id": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Conditional. Discriminator for the account reference. Mandatory when **partyOrPartyRole** is present. Must be exactly `"AccountRef"`.Only account-based eligibility is supported. Any other value returns a 400 error.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Conditional. Sys\_id of the customer account record. Mandatory when **partyOrPartyRole** is present. The eligibility engine loads this account to evaluate account-level eligibility rules. A non-existent account ID returns a 400 error.

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Required. Describes the role of the related party in this query. Must not be empty.Used by the eligibility engine to interpret the party's relationship to the qualification request. A missing or empty value returns a 400 validation error.

Example: `"requester"``"customer"`

Data type: String

</td></tr><tr><td>

searchCriteria

</td><td>

Optional. Container for location-based search filters. When provided, the eligibility engine uses the nested place array to restrict results to offerings available at the specified geographic location\(s\).The entire **searchCriteria** object is echoed back in the response. Omit this field entirely to run an unconstrained catalog query.

Data type: Object

```
"searchCriteria": {
 "@type": "String",
 "place": [Array]
}
```

</td></tr><tr><td>

searchCriteria.@type

</td><td>

Optional. Discriminator for the **searchCriteria** object. Typically set to `"QueryProductOfferingQualification"`. Informational; echoed in the response.Data type: String

</td></tr><tr><td>

searchCriteria.place

</td><td>

Optional. List of location constraints for the query. The eligibility engine filters the catalog to offerings that are available at all provided locations.At most one entry per role value — one **serviceLocation** and one **billingLocation**. Passing an explicit null or empty array is rejected with a 400; omit the field entirely to skip place filtering.

Data type: Array of Objects

```
"place": [
 {
  "@type": "String",
  "role": "String",
  "place": {Object}
 }
]
```

</td></tr><tr><td>

searchCriteria.place.@type

</td><td>

Conditional. Mandatory when a place entry is present. Discriminator for the place wrapper object. Set to `"Place"`.Data type: String

</td></tr><tr><td>

searchCriteria.place.place

</td><td>

The location reference, either a `PlaceRef` or `GeographicAddress`.Data type: Object

```
"place": {
 "@type": "String",
 "streetName": "String",
 "streetNumber": "String",
 "city": "String",
 "postcode": "String",
 "country": "String"
}
```

</td></tr><tr><td>

searchCriteria.place.place.@type

</td><td>

Conditional. Determines how the location is identified. Mandatory when a **place** entry is present. Valid values:

-   `PlaceRef`: Reference to an existing Location record. Only **id** is permitted; no other address fields may be present.
-   `GeographicAddress`: Inline address supplied by the caller. Address fields such as **city**, **country**, **postcode**, etc. are used; **id** is not permitted.

Data type: String

</td></tr><tr><td>

searchCriteria.place.place.city

</td><td>

Optional. City name. Only applicable when **@type** is `"GeographicAddress"`. Used by location-based eligibility rules to match service territories.Example: `"Paris"`, `"San Diego"`

Data type: String

</td></tr><tr><td>

searchCriteria.place.place.country

</td><td>

Optional. Country name or ISO code. Only applicable when **@type** is `"GeographicAddress"`.Example: `"France"`, `"US"`

Data type: String

</td></tr><tr><td>

searchCriteria.place.place.id

</td><td>

Conditional. Sys\_id of the Location record. Required when **@type** is `PlaceRef`. The API looks up this record to retrieve the address used for eligibility matching. An unresolved ID returns a 400 error with reason: `"Invalid Place Information". Must not be provided when @type is "GeographicAddress".`

Data type: String

</td></tr><tr><td>

searchCriteria.place.place.postcode

</td><td>

Optional. Postal or ZIP code. Only applicable when **@type** is `"GeographicAddress"`. Can be used by postcode-based service territory eligibility rules.Example: `"75001"`

Data type: String

</td></tr><tr><td>

searchCriteria.place.place.stateOrProvince

</td><td>

Optional. State or province name. Only applicable when **@type** is `"GeographicAddress"`.Example: `"CA"`

Data type: String

</td></tr><tr><td>

searchCriteria.place.place.streetName

</td><td>

Optional. Street name without the number. Only applicable when **@type** is `"GeographicAddress"`. Combined with **streetNumber** as "`{streetNumber} {streetName}"` when both are present.Example: `"Main Street"`

Data type: String

</td></tr><tr><td>

searchCriteria.place.place.streetNumber

</td><td>

Optional. Street number. Only applicable when **@type** is `"GeographicAddress"`. Prepended to **streetName** when both are provided.Example: `"123"`

Data type: String

</td></tr><tr><td>

searchCriteria.place.role

</td><td>

Conditional. Purpose of this location in the query. Mandatory when a **place** entry is present. Accepted values:

-   `serviceLocation`: Where the product will be delivered or used.
-   `billingLocation`: Customer billing address.

Each role may appear at most once in the array; a duplicate role returns a 400 error.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Content-Type|Must be `application/json`.|
|Authorization|Basic auth or OAuth token. Unauthenticated requests return HTTP 401; missing role returns HTTP 403.|
|Accept|`application/json` \(recommended\).|

|Header|Description|
|------|-----------|
|Content-Type|`application/json`|
|X-Total-Count|Total number of eligible offerings matching the query \(before pagination is applied\). Integer value, for example `4`.|
|Content-Range|Range of records in this page. Format: `{start}-{end}/{total}`. For example, `1-3/4`.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Query processed successfully. `qualifiedProductOfferingItem` may be an empty array if no offerings qualify.|
|400|Validation errors. Schema failure, invalid `place`, `relatedParty`, category, or channel validation failures. Response includes `code`, `reason`, `message`, and `details` array.|
|404|Non-numeric `limit` or `offset`; `limit` exceeding `MAX_LIMIT`; `offset` ≥ `totalCount` \(when totalCount &gt; 0\).|
|401|Unauthenticated. Missing or invalid credentials. Enforced by the platform REST framework.|
|403|Forbidden. Caller lacks the `sn_tmf_api.product_offering_qualification_integrator` role. Enforced by the REST endpoint ACL.|
|429|Too Many Requests. Rate limit of 6,000 req/hr exceeded. Response includes a `Retry-After` header.|
|500|Unexpected exception from the eligibility engine \(`ProductEligibilityAPI`\).|

### Response body parameters \(JSON or XML\)

<table class="rest_api_response_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

TMF discriminator for the top-level response object. Always `"QueryProductOfferingQualification"`.Data type: String

</td></tr><tr><td>

state

</td><td>

Processing state of the query. Always `"done"` on a successful 200 response.An empty result set \(`qualifiedProductOfferingItem: []`\) is still "done"; it means no offerings matched the criteria, not that the query failed.

Data type: String

</td></tr><tr><td>

qualifiedProductOfferingItem

</td><td>

List of product offerings that passed all eligibility rules for the provided customer, channel, category, and location context. Each entry represents one eligible offering.The array may be empty if no offerings qualify. The total count \(before pagination\) is in the X-Total-Count response header.

Data type: Array of Objects

```
"qualifiedProductOfferingItem": [
  {
    "@type": "String",
    "productOffering": {Object}
  }
]
```

</td></tr><tr><td>

qualifiedProductOfferingItem.@type

</td><td>

TMF discriminator for each result item. Always `"QueryProductOfferingQualificationItem"`.Data type: String

</td></tr><tr><td>

qualifiedProductOfferingItem.productOffering

</td><td>

Required. Reference to the eligible product offering. Contains the fields needed to identify and link to the offering in the Product Catalog.Data type: Object

```
"productOffering": {
      "id": "String",
      "name": "String",
      "href": "String",
      "@type": "String"
    }
```

</td></tr><tr><td>

qualifiedProductOfferingItem.productOffering.id

</td><td>

Sys\_id of the product offering record. Use this value to retrieve full offering details from the Product Catalog API or to pass to POST /checkproductofferingqualification to confirm eligibility before purchase.Data type: String

</td></tr><tr><td>

qualifiedProductOfferingItem.productOffering.name

</td><td>

Human-readable display name of the product offering as configured in the Product Catalog. Use this to display the offering name in a storefront or CPQ interface.Example: `"All in one mobile plan starting from $39/month"`

Data type: String

</td></tr><tr><td>

qualifiedProductOfferingItem.productOffering.href

</td><td>

Self-link to the product offering resource on this instance. Use this as a hypermedia link to fetch the full offering details.Format: `/api/sn_tmf_api/catalogmanagement/productOffering/{id}`

Data type: String

</td></tr><tr><td>

qualifiedProductOfferingItem.productOffering.@type

</td><td>

Required. TMF discriminator for the product offering reference. Always `"ProductOfferingRef"`.Data type: String

</td></tr><tr><td>

channel

</td><td>

Echo of the channel object from the request. Returned as-is so callers can confirm which channel context was applied. Absent when channel was not provided in the request.Data type: Object

```
"channel": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

channel.id

</td><td>

Choice value identifying the channel. This is the value field from the sys\_choice table for the channel field \(for example, `"web"`\), not a sys\_id. Echoed from the request.Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Display name of the channel. Informational; echoed from the request.Example: `"Web"`, `"Retail"`

Data type: String

</td></tr><tr><td>

channel.@type

</td><td>

Discriminator for the channel object. Always `"ChannelRef"`. Echoed from the request.Data type: String

</td></tr><tr><td>

category

</td><td>

Echo of the category filter from the request. Returned as-is so callers can confirm which category scope was applied. Absent when category wasn't provided in the request.Data type: Object

```
"category": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

category.id

</td><td>

Sys\_id of the Product Category record. The API used this to filter the catalog to offerings linked to this category. Echoed from the request.Data type: String

</td></tr><tr><td>

category.@type

</td><td>

Discriminator for the category reference. Always `"CategoryRef"`. Echoed from the request.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

Echo of the **relatedParty** array from the request. Returned as-is so callers can confirm which customer account the eligibility was evaluated for.Data type: Array of Objects

```
"relatedParty": [
  {
    "@type": "String",
    "role": "String",
    "partyOrPartyRole": {Object}
  }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Discriminator for this related party entry. Always `"RelatedPartyOrPartyRole"`. Echoed from the request.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Describes the role of the related party in this query. Echoed from the request.Example: `"requestor"`, `"customer"`

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

The account reference nested inside the related party. Contains the discriminator and the sys\_id of the customer account. Echoed from the request.Data type: Object

```
"partyOrPartyRole": {
      "id": "String",
      "@type": "String"
    }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Discriminator for the account reference. Always `"AccountRef"`. Echoed from the request.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id of the customer account record. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria

</td><td>

Echo of the **searchCriteria** object from the request. Returned as-is so callers can confirm which location filters were applied. Absent when **searchCriteria** was not provided in the request.Data type: Object

```
"searchCriteria": {
  "@type": "String",
  "place": [Array]
}
```

</td></tr><tr><td>

searchCriteria.@type

</td><td>

Discriminator for the **searchCriteria** object. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place

</td><td>

List of location constraints used to filter the catalog. Echoed from the request.Data type: Array of Objects

```
"place": [
    {
      "@type": "String",
      "role": "String",
      "place": {Object}
    }
  ]
```

</td></tr><tr><td>

searchCriteria.place.@type

</td><td>

Discriminator for the **place** wrapper object. Always `"Place"`. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.role

</td><td>

Purpose of this location in the query \(`"serviceLocation"`or `"billingLocation"`\). Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place

</td><td>

The location reference, either a PlaceRef or GeographicAddress. Echoed from the request.Data type: Object

```
"place": {
  "@type": "String",
  "streetName": "String",
  "streetNumber": "String",
  "city": "String",
  "postcode": "String",
  "country": "String"
 }
}
```

</td></tr><tr><td>

searchCriteria.place.place.@type

</td><td>

Determines how the location is identified \(`"PlaceRef"` or `"GeographicAddress"`\). Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.place.id

</td><td>

Sys\_id of the Location record. Present when **@type** is `"PlaceRef"`. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.place.city

</td><td>

City name. Present when **@type** is `"GeographicAddress"`. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.place.country

</td><td>

Country name or ISO code. Present when **@type** is `"GeographicAddress"`. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.place.stateOrProvince

</td><td>

State or province name. Present when **@type** is `"GeographicAddress"`. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.place.streetName

</td><td>

Street name. Present when **@type** is `"GeographicAddress"`. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.place.streetNumber

</td><td>

Street number. Present when **@type** is `"GeographicAddress"`. Echoed from the request.Data type: String

</td></tr><tr><td>

searchCriteria.place.place.postcode

</td><td>

Postal or ZIP code. Present when **@type** is `"GeographicAddress"`. Echoed from the request.Data type: String

</td></tr><tr><td>

warnings

</td><td>

Advisory messages about non-fatal issues with the request. Present when multiple **AccountRef** entries were supplied in **relatedParty**. which indicates that only the first entry was used for eligibility evaluation and the rest were ignored.Data type: Array of Strings

```
"warnings": [
  "String"
]
```

</td></tr><tr><td>

code

</td><td>

Numeric error code. Present only on error responses \(4xx / 5xx\). Identifies the error category \(for example, 24 for invalid place information\).Data type: Integer

</td></tr><tr><td>

reason

</td><td>

Short human-readable error category. Present only on error responses. Example: `"Invalid Place Information"`.Data type: String

</td></tr><tr><td>

message

</td><td>

Detailed error message. Present only on error responses. Describes the specific failure condition.Data type: String

</td></tr><tr><td>

details

</td><td>

Per-field validation errors. Present only on 400 error responses.Data type: Array of Objects

```
"details": [
  {
    "message": "String",
    "datapath": "String"
  }
]
```

</td></tr><tr><td>

details.message

</td><td>

Description of the specific field error. Example: `"PlaceRef id not found: f90ad912..."`

Data type: String

</td></tr><tr><td>

details.datapath

</td><td>

The JSON datapath to the offending field. Example: `"/searchCriteria/place[1]/place/id"`

Data type: String

</td></tr></tbody>
</table>### cURL request

This example request queries product offerings available in the web channel and specified category for an account, filtered to those serviceable at a Paris street address and billable to a referenced location.

```
curl -X POST \
  "https://<instance>.service-now.com/api/sn_tmf_api/product_offering_qualification_api/v1/queryProductOfferingQualification?limit=10&offset=0" \
  -H "Content-Type: application/json" \
  -H "Authorization: Basic <base64-credentials>" \
  -d '{
    "@type": "QueryProductOfferingQualification",
    "channel": { "id": "web", "name": "Web", "@type": "ChannelRef" },
    "category": { "id": "<category-sys-id>", "@type": "CategoryRef" },
    "relatedParty": [
      {
        "@type": "RelatedPartyOrPartyRole",
        "role": "requestor",
        "partyOrPartyRole": {
          "id": "<account-sys-id>",
          "@type": "AccountRef"
        }
      }
    ],
    "searchCriteria": {
      "@type": "QueryProductOfferingQualification",
      "place": [
        {
          "@type": "Place",
          "role": "serviceLocation",
          "place": {
            "@type": "GeographicAddress",
            "streetName": "Main Street",
            "streetNumber": "123",
            "city": "Paris",
            "postcode": "75001",
            "country": "France"
          }
        },
        {
          "@type": "Place",
          "role": "billingLocation",
          "place": { "@type": "PlaceRef", "id": "<place-sys-id>" }
        }
      ]
    }
  }'
```

Response body 200 success response:

```
HTTP/1.1 200 OK
Content-Type: application/json
X-Total-Count: 2
Content-Range: 1-2/2

{
  "@type": "QueryProductOfferingQualification",
  "state": "done",
  "channel": { "id": "web", "name": "Web", "@type": "ChannelRef" },
  "category": { "id": "<category-sys-id>", "@type": "CategoryRef" },
  "relatedParty": [
    {
      "@type": "RelatedPartyOrPartyRole",
      "role": "requestor",
      "partyOrPartyRole": { "@type": "AccountRef", "id": "<account-sys-id>" }
    }
  ],
  "searchCriteria": { "@type": "QueryProductOfferingQualification", "place": [ ... ] },
  "qualifiedProductOfferingItem": [
    {
      "@type": "QueryProductOfferingQualificationItem",
      "productOffering": {
        "id": "<product-offering-sys-id-1>",
        "href": "/api/sn_tmf_api/catalogmanagement/productOffering/<product-offering-sys-id-1>",
        "name": "All in one mobile plan starting from $39/month",
        "@type": "ProductOfferingRef"
      }
    },
    {
      "@type": "QueryProductOfferingQualificationItem",
      "productOffering": {
        "id": "<product-offering-sys-id-2>",
        "href": "/api/sn_tmf_api/catalogmanagement/productOffering/<product-offering-sys-id-2>",
        "name": "All in one mobile plan starting from $49/month",
        "@type": "ProductOfferingRef"
      }
    }
  ]
}
```

Response for 400 validation failure:

```
{
  "code": 24,
  "reason": "Invalid Place Information",
  "message": "Invalid Place Information",
  "details": [
    {
      "message": "PlaceRef id not found: <place-sys-id>",
      "datapath": "/searchCriteria/place[1]/place/id"
    }
  ]
}
```

