---
title: Sales Cart REST API
description: The Sales Cart REST API gives an external system programmatic control of a ServiceNow sales cart. Operations include creating a cart and its line items, reading a cart or line item, removing a cart or line item, and submitting a cart. Submitting a cart causes Order Management to convert it into an order.Creates a sales cart in draft state with an optional set of line items, or adds line items to a cart that already exists.Updates an existing draft cart: header attributes, line item attributes, line characteristics, pricing adjustments, and child line items.Returns a list of sales carts matching an arbitrary encoded query applied to the Sales Cart \[sn\_sales\_cart\] table.Returns a sales cart with its line items, so a headless interface can render current cart state without keeping a copy of it.Returns a single cart line item from a given parent cart.Converts a draft cart into an order, propagating billing account and payment profile data from the cart lines onto the order lines. Billing data captured on the cart is copied to the order.Deletes a given sales cart.Removes a single line item from a given cart.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/sales-cart-api.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 27
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Sales Cart REST API

The Sales Cart REST API gives an external system programmatic control of a ServiceNow sales cart. Operations include creating a cart and its line items, reading a cart or line item, removing a cart or line item, and submitting a cart. Submitting a cart causes Order Management to convert it into an order.

The Sales Cart REST API \(**sales\_cart**\) is the checkout engine behind headless commerce front ends built on Order Management. For example, a telecommunications self-service portal can own its own user interface and call ServiceNow only for cart state, pricing, and order submission. The resource declares eight routes on API version 1: get carts by encoded query, create cart, update cart, get cart, get cart line item, submit order, delete cart, and delete cart line item.

This API is provided within the `sn_sales_cart` namespace \(Sales Cart scoped application\). Order-line entity attributes and mappings are owned by the `sn_ind_tmt_orm` \(Order Management\) scope; context variables by `sn_csm_ctxrul_mgt`.

The calling user must hold one of the following roles: `sn_customerservice.consumer` \(an authenticated end customer acting on their own cart\), or the pre-existing customer/cart-editor roles behind ACL `496fa8cbffca83503e5cffffffffff5a` \(an account/contact-based business cart\).

Two capabilities were added to this API in the 2026 September Order Management bundle:

-   Consumer persona support: Before this release the API could only be called on behalf of an account and contact — a business-to-business shape. An authenticated end customer holding `sn_customerservice.consumer` can now call the API for their own cart. Cart attributes that were previously derived from the account are now derived from the consumer record instead: currency from the consumer's country, price list from a currency-only pricing context, and shipping and billing address from the consumer's own address fields.
-   Billing account and payment profile on the cart line: The cart line item can now carry a billing account reference \(**billing\_account**\) and a payment profile reference \(**payment\_profile**\), assignable independently per line. This lets a cart containing a personal subscription and a business subscription bill each line to a different account. Both values propagate automatically to the order line when the cart is submitted.

The two new cart-line fields install only when the `com.snc.billing_account` plugin is present. On an instance without that plugin, these two request/response parameters don't exist.

## Call order

The endpoints are stateful with respect to the cart record and must be called in this sequence:

1.  Create the cart, and optionally its line items, with the create-cart endpoint. The response returns the cart identifier.
2.  Optionally discover an existing cart first with the get-carts-by-encoded-query endpoint, rather than creating one. This is useful for resuming an abandoned basket.
3.  Modify the cart with the update endpoint. Add further line items by calling create-cart again with the existing cart identifier, or remove a line item with the delete-line-item endpoint. Reassigning the billing account or payment profile on a line after creation is done through the update endpoint.
4.  Read the cart or a line item to render current state, then submit the cart to create the order. The cart moves out of draft state. Delete and write operations available to a consumer no longer apply, because the consumer ACLs on those operations are conditioned on `state=draft`.

## Association with other APIs and special processing

Cart creation and cart-to-order conversion are executed through the Lead-to-Cash entity mapping framework rather than by direct field assignment in the REST handler. Two mapping configurations are involved: `sn_l2c_cart_to_cart`, applied at cart creation, and `sn_l2c_cart_to_order`, applied at submission. A field is only accepted or propagated if an `sn_l2c_core_entity_attribute` record exists for it on the source table and an `sn_l2c_core_entity_attribute_mapping` record wires it to the target attribute.

One naming asymmetry is deliberate and matters to anyone reading the payloads: the field is **payment\_profile** on the cart line and **payment** on the order line. Both reference the Payment Profile \[`sn_billing_account_payment_profile`\] table. The **billing\_account** field keeps the same name on both sides.

## Extending the API

To make an additional cart-line or order-line field readable and writable through the API, register it with the Lead-to-Cash entity mapping framework. This also makes it propagate from cart to order. Use `sn_l2c_core_entity_attribute` plus `sn_l2c_core_entity_attribute_mapping` records for `sn_l2c_cart_to_cart`, `sn_l2c_cart_to_order`, or both. No change to the REST handler script is required. Install the target attribute definition before or together with the mapping rows that reference it. Installing mapping rows first resolves the target reference to null, and the mapping silently does nothing.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/api-rest.md)

## Sales Cart - POST /sn\_sales\_cart/sales\_cart

Creates a sales cart in draft state with an optional set of line items, or adds line items to a cart that already exists.

Whether a cart is created or line items are added is decided by whether the payload carries an existing cart identifier:

-   With an identifier, the endpoint adds lines to that cart \(Case B\).
-   Without an identifier, it creates a new cart \(Case A\).

The response flag **isCartCreated** tells the caller which path ran.

### Brazil release updates

A caller holding `sn_customerservice.consumer` may now create a cart for themselves by supplying a consumer reference instead of an account and contact. For a consumer cart, the endpoint derives currency from the consumer record's country and derives the price list from a currency-only pricing context. When **shipping\_city** is not supplied, it also defaults shipping and billing address from the consumer record's own address fields and sets **same\_as\_shipping\_address** to true.

A consumer may hold only one draft cart at a time. If a draft cart already exists for the consumer, the request is rejected \(409\). The identifier of the existing cart is returned so the caller can continue with it instead. The same guard already applied per contact for account-based carts.

### URL format

Default URL: `/api/sn_sales_cart/sales_cart`

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

attributes

</td><td>

Required. Cart header attributes. Each member is itself an object of the form `{ "value": "<value>" }`, not a bare scalar.Data type: Object

</td></tr><tr><td>

attributes.account

</td><td>

Conditional. Sys\_id of the account for a business cart.Data type: String

</td></tr><tr><td>

attributes.consumer

</td><td>

Conditional. Sys\_id of the consumer record the cart belongs to. Required for a consumer cart; mutually exclusive in practice with the **attributes.account**/**attributes.contact** pair.Table: Consumer \[csm\_consumer\]

Data type: String

</td></tr><tr><td>

attributes.contact

</td><td>

Conditional. Sys\_id of the contact for a business cart. Required for an account-based cart.Data type: String

</td></tr><tr><td>

attributes.currency

</td><td>

Currency code for the cart.Data type: String

Default: Server resolution

</td></tr><tr><td>

attributes.opened\_by

</td><td>

Sys\_id of the user the cart is opened by.Data type: String

Table: User \[sys\_user\]

Default: Defaults to the contact for an account cart

</td></tr><tr><td>

attributes.price\_list

</td><td>

Sys\_id of the price list applied to the cart.Data type: String

Default: Resolved by the server from the default price list for the resolved currency

</td></tr><tr><td>

attributes.same\_as\_shipping\_address

</td><td>

Flag that indicates whether the billing address is the same as the shipping address. Possible values:

-   true: The billing address is the same as the shipping address.
-   false: The billing address is different from the shipping address.

Data type: Boolean

Default: true when the server defaults the address block; otherwise unset

</td></tr><tr><td>

attributes.shipping\_city

</td><td>

Shipping city.Data type: String

Default: Defaulted from the consumer or account primary address

</td></tr><tr><td>

attributes.state

</td><td>

Cart state. Set to `draft` on creation. Consumer write and delete ACLs apply only while the cart is in draft.Data type: String

Default: draft

</td></tr><tr><td>

cartId

</td><td>

Sys\_id of an existing draft cart. Supply it to add line items to that cart instead of creating a new one \(Case B\).Data type: String

</td></tr><tr><td>

line\_items

</td><td>

Line items to create on the cart. Each element carries a product offering reference plus the cart-line attributes described in the following rows. Data type: Array of Objects

</td></tr><tr><td>

line\_items\[\].billing\_account

</td><td>

Sys\_id of the billing account this line is billed to. Nullable and independent per line item. Propagates to the order line field of the same name on submission.Table location: Billing Account \[sn\_billing\_account\_billing\_account\]

Data type: String

</td></tr><tr><td>

line\_items\[\].payment\_profile

</td><td>

Sys\_id of the payment profile used for this line. Propagates to the order line field named payment, not payment\_profile.Table location: Payment Profile \[sn\_billing\_account\_payment\_profile\]

Data type: String

</td></tr><tr><td>

skip\_pricing

</td><td>

Flag that indicates whether the pricing engine is bypassed for this request.Possible values:

-   true: The pricing engine is bypassed for this request.
-   false: The pricing engine runs normally for this request.

Data type: Boolean

Default: false

</td></tr></tbody>
</table>### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md) concept topic. Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|

### Status codes

|Status code|Description|
|-----------|-----------|
|201|Created. The cart was created, or line items were added to the supplied cart.|
|400|Bad request. Missing or invalid input. Covers CONTACT\_REQUIRED \(no contact on an account cart\), CONTACT\_NOT\_FOUND, CONSUMER\_NOT\_FOUND, and INVALID\_PRODUCT\_OFFERINGS \(one or more product offerings did not resolve\).|
|401|Unauthorized. The request was not authenticated.|
|404|Not found. In Case B, the supplied cart identifier does not resolve to a cart.|
|409|Conflict. Either a draft cart already exists for this consumer or contact \(DRAFT\_CART\_EXISTS\), or the target cart in Case B is not in draft state. The response data carries the identifier of the conflicting cart.|
|500|Internal server error. Returned when the handler's catch block traps an unexpected failure, including CART\_CREATION\_FAILED.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Supplementary error context.Data type: Object

</td></tr><tr><td>

error

</td><td>

Human-readable error message, present on failure only.Data type: String

</td></tr><tr><td>

result

</td><td>

Container for the response payload.Data type: Object

</td></tr><tr><td>

result.cartId

</td><td>

Sys\_id of the created or updated cart.Data type: String

</td></tr><tr><td>

result.isCartCreated

</td><td>

Flag that indicates which path the request took.Possible values:

-   true: A new cart was created \(Case A\).
-   false: Line items were added to an existing cart \(Case B\).

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

A consumer creates a cart with a single line item, assigning a billing account and a payment profile to that line. No currency, price list, or address is supplied, so the server resolves all three from the consumer record.

```
curl --location --request POST 'https://<instance>.service-now.com/api/sn_sales_cart/sales_cart' \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --user '<consumer_user>:<password>' \
  --data '{
    "attributes": {
      "consumer": { "value": "b1f2c3d4e5f60718293a4b5c6d7e8f90" }
    },
    "skip_pricing": false,
    "line_items": [
      {
        "product_offering": { "value": "9a8b7c6d5e4f30211f0e9d8c7b6a5f40" },
        "quantity": { "value": "1" },
        "billing_account": { "value": "c1a1b2c3d4e5f60709acbffffffffff01" },
        "payment_profile": { "value": "d2b1c3a4e5f60718293a4b5c6d7e8f91" }
      }
    ]
  }' 
```

Response body.

```
HTTP/1.1 201 Created
Content-Type: application/json

{
  "result": {
    "cartId": "7f3e2d1c0b9a8877665544332211ffee",
    "isCartCreated": true
  }
}
```

## Sales Cart - PATCH /sn\_sales\_cart/v1/sales\_cart

Updates an existing draft cart: header attributes, line item attributes, line characteristics, pricing adjustments, and child line items.

This is the endpoint a portal uses between cart creation and submission. Typical uses include changing a quantity, switching a configuration option, correcting a shipping address, or reassigning the billing account on a line. The cart must be in draft state. A non-draft cart is rejected with 409.

Line-level create and delete behavior differs by nesting depth. At the top level, a line item must carry a valid existing sys\_id. New line creation and deletion are not supported at that level. Lines whose sys\_id is missing or -1 are silently skipped rather than rejected. For nested child line items, an empty or -1 sys\_id is an insert signal, and **"action": "Delete"** is a removal.

### URL format

Versioned URL: `/api/sn_sales_cart/v1/sales_cart`

Default URL: `/api/sn_sales_cart/sales_cart`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

skip\_pricing

</td><td>

Flag that indicates whether the pricing engine is bypassed for this update.Possible values:

-   true: The pricing engine is bypassed for this update.
-   false: The pricing engine runs normally for this update.

Data type: Boolean

Default: false

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributes

</td><td>

Cart header attributes to change, each as a `{ "value": "<value>" }` wrapper keyed by database field name. Omitted members are left untouched.Examples: shipping\_location, shipping\_city, notes.

Data type: Object

</td></tr><tr><td>

cartId

</td><td>

Required. Sys\_id of the draft cart to update.Data type: String

</td></tr><tr><td>

lineItems

</td><td>

Line items to update. Each element identifies an existing cart line and carries the nested collections described in the following rows. Elements whose sys\_id is missing or `-1` are silently skipped at the top level.

Data type: Array of Objects

</td></tr><tr><td>

lineItems.attributes

</td><td>

Line item fields to change, keyed by database field name, each a `{ "value": ... }` wrapper. Examples: quantity, term\_month. Also accepts billing\_account and payment\_profile.

Data type: Object

</td></tr><tr><td>

lineItems.attributes.billing\_account

</td><td>

Sys\_id of the billing account to assign to this line. Whether the API applies the same reference qualifier server-side as the form does was not confirmed.Table location: Billing Account \[sn\_billing\_account\_billing\_account\]

Data type: String

</td></tr><tr><td>

lineItems.attributes.payment\_profile

</td><td>

Sys\_id of the payment profile to assign to this line.Table location: Payment Profile \[sn\_billing\_account\_payment\_profile\]

Data type: String

</td></tr><tr><td>

lineItems.characteristics

</td><td>

Line characteristics to change. Each element carries a sys\_id wrapper and an attributes object.Data type: Array of Objects

</td></tr><tr><td>

lineItems.lineItems

</td><td>

Child line items of this line. Unlike the top level, this collection supports insert and delete:

-   A sys\_id of `""` or `"-1"` signals a new child line.
-   An element carrying `"action": "Delete"` removes one.

Data type: Array of Objects

</td></tr><tr><td>

lineItems.lineItems.action

</td><td>

Operation to perform on the child line.Valid value: `Delete`

Omit for an update or insert.

Data type: String

</td></tr><tr><td>

lineItems.pricingAdjustments

</td><td>

Pricing adjustments to change. Each element carries a sys\_id wrapper and an attributes object.Data type: Array of Objects

</td></tr><tr><td>

lineItems.sys\_id

</td><td>

Required on every top-level element. Sys\_id of the existing cart line item, as a `{ "value": "<sys_id>" }`wrapper. Data type: Object

</td></tr></tbody>
</table>### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md) concept topic. Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|
|X-Total-Count|Not emitted by this endpoint.|

### Status codes

|Status code|Description|
|-----------|-----------|
|200|Success. The cart was updated. The response reports which line items were matched and changed.|
|400|Bad request. Missing cartId, an invalid request body, or an invalid product offering sys\_id on a new child line.|
|401|Unauthorized. The request was not authenticated.|
|404|Not found. The cart does not resolve, or the caller can't see it.|
|409|Conflict. The cart is not in draft state.|
|500|Internal server error. An Entity Pipeline service failure or an unexpected error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Container for the update outcome.Data type: Object

</td></tr><tr><td>

result.cartId

</td><td>

Sys\_id of the cart that was updated. Echoes the request.Data type: String

</td></tr><tr><td>

result.isCartUpdated

</td><td>

Flag that indicates whether the update was applied. Possible values:

-   true: The update was applied.
-   false: The update was not applied.

Data type: Boolean

</td></tr><tr><td>

result.lineItemIds

</td><td>

Sys\_ids of the top-level line items matched and changed by this request.**Note:** Provide only the matched lines, not every root line the Entity Pipeline loaded. Don't treat it as a full cart line inventory.

Data type: Array of Strings

</td></tr><tr><td>

error

</td><td>

Present on failure only, in the form `{ "message": "<string>" }`.**Note:** This differs from the create-cart endpoint, which returns error as a bare string.

Data type: Object

</td></tr></tbody>
</table>### cURL request

A consumer changes the quantity on one cart line and reassigns that line to a different billing account and payment profile in the same call. Only the members supplied are compared and changed.

```
curl --location --request PATCH 'https://<instance>.service-now.com/api/sn_sales_cart/v1/sales_cart' \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --user '<consumer_user>:<password>' \
  --data '{
    "cartId": "7f3e2d1c0b9a8877665544332211ffee",
    "skip_pricing": false,
    "attributes": {
      "shipping_city": { "value": "Zurich" }
    },
    "lineItems": [
      {
        "sys_id": { "value": "1a2b3c4d5e6f708192a3b4c5d6e7f809" },
        "attributes": {
          "quantity": { "value": "3" },
          "billing_account": { "value": "c5a1b2c3d4e5f60709acbffffffffff05" },
          "payment_profile": { "value": "e3c2d4b5f60718293a4b5c6d7e8f90a2" }
        }
      }
    ]
  }' 
```

Response body.

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "result": {
    "cartId": "7f3e2d1c0b9a8877665544332211ffee",
    "isCartUpdated": true,
    "lineItemIds": ["1a2b3c4d5e6f708192a3b4c5d6e7f809"]
  }
}
```

## Sales Cart - GET /sn\_sales\_cart/v1/sales\_cart

Returns a list of sales carts matching an arbitrary encoded query applied to the Sales Cart \[sn\_sales\_cart\] table.

Use this endpoint for discovery. An interface that does not already hold a cart identifier uses it to find the caller's carts. For example, filter on `state=draft` to resume an abandoned basket.

### URL format

Versioned URL: `/api/sn_sales_cart/v1/sales_cart`

Default URL: `/api/sn_sales_cart/sales_cart`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_query

</td><td>

Encoded query applied to the Sales Cart \[sn\_sales\_cart\] table, in standard GlideRecord encoded query syntax \(for example `state=draft` or `state=draft^consumer=<sys_id>`\). Data type: String

Default: All carts readable by the caller are returned

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`. Not required on this GET/DELETE request.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md) concept topic. Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|

### Status codes

|Status code|Description|
|-----------|-----------|
|200|Success. Returns the matching carts, including an empty list when nothing matches. Also returned when individual carts were skipped because they failed to expand.|
|400|Bad request. Not emitted by the handler for a malformed encoded query — no validation of sysparm\_query syntax was found.|
|401|Unauthorized. The request was not authenticated.|
|403|Forbidden. The caller lacks execute access to the REST resource.|
|500|Internal server error. Returned when the Entity Pipeline service can't be obtained, with the INTERNAL\_SERVER\_ERROR message.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Container for the result set.Data type: Object

</td></tr><tr><td>

result.carts

</td><td>

Matching carts, each expanded into a full cart instance including its line items. A line item carries**billing\_account** and **payment\_profile**. Returns an empty array when nothing matches.Data type: Array of Objects

</td></tr><tr><td>

result.count

</td><td>

Number of carts in the **carts** array. Counts successfully expanded carts, not rows matched by the query. A cart that failed to expand is omitted from both.Data type: Number

</td></tr><tr><td>

error

</td><td>

Present on failure only. The 500 case returns the INTERNAL\_SERVER\_ERROR constant message.Data type: String

</td></tr></tbody>
</table>### cURL request

A portal resumes a shopper's session by looking for an existing draft cart. The consumer sends state=draft; the query rule silently adds the ownership restriction, so the response contains only their own draft cart.

```
curl --location --request GET \
  'https://<instance>.service-now.com/api/sn_sales_cart/v1/sales_cart?sysparm_query=state%3Ddraft' \
  --header 'Accept: application/json' \
  --user '<consumer_user>:<password>' 
```

Response body.

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "result": {
    "count": 1,
    "carts": [
      {
        "sys_id": "7f3e2d1c0b9a8877665544332211ffee",
        "state": "draft",
        "currency": "CHF",
        "line_items": [
          {
            "sys_id": "1a2b3c4d5e6f708192a3b4c5d6e7f809",
            "billing_account": "c1a1b2c3d4e5f60709acbffffffffff01",
            "payment_profile": "d2b1c3a4e5f60718293a4b5c6d7e8f91"
          }
        ]
      }
    ]
  }
}
```

## Sales Cart - GET /sn\_sales\_cart/sales\_cart/\{cart\_id\}

Returns a sales cart with its line items, so a headless interface can render current cart state without keeping a copy of it.

### URL format

Default URL: `/api/sn_sales_cart/sales_cart/{cartId}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cartId

</td><td>

Sys\_id of the cart to return.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`. Not required on this GET/DELETE request.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md). Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|

### Status codes

|Status code|Description|
|-----------|-----------|
|200|Success. The cart and its line items were returned.|
|401|Unauthorized. The request was not authenticated.|
|403|Forbidden. The caller lacks a role granted execute access to the REST resource.|
|404|Not found. No cart matches the identifier, or the caller can't see it.|
|500|Internal server error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

The cart record with its line items.Data type: Object

</td></tr><tr><td>

result.currency

</td><td>

Currency code resolved for the cart. For a consumer cart this was derived from the consumer's country.Data type: String

</td></tr><tr><td>

result.price\_list

</td><td>

Sys\_id of the price list applied to the cart.Data type: String

</td></tr><tr><td>

result.state

</td><td>

Cart state. A consumer can write to or delete the cart only while this is draft.Data type: String

</td></tr><tr><td>

&lt;line items&gt;\[\].billing\_account

</td><td>

The billing account assigned to the line, from sn\_billing\_account\_billing\_account.Data type: String or Object

</td></tr><tr><td>

&lt;line items&gt;\[\].payment\_profile

</td><td>

The payment profile assigned to the line, from sn\_billing\_account\_payment\_profile.Data type: String or Object

</td></tr></tbody>
</table>### cURL request

A consumer reads their own cart to render the checkout screen, including which billing account and payment profile each line is currently assigned to.

```
curl --location --request GET 'https://<instance>.service-now.com/api/sn_sales_cart/sales_cart/7f3e2d1c0b9a8877665544332211ffee' \
  --header 'Accept: application/json' \
  --user '<consumer_user>:<password>' 
```

Response body.

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "result": {
    "sys_id": "7f3e2d1c0b9a8877665544332211ffee",
    "state": "draft",
    "currency": "CHF",
    "price_list": "4c5d6e7f8091a2b3c4d5e6f708192a3b",
    "consumer": "b1f2c3d4e5f60718293a4b5c6d7e8f90",
    "line_items": [
      {
        "sys_id": "1a2b3c4d5e6f708192a3b4c5d6e7f809",
        "billing_account": "c1a1b2c3d4e5f60709acbffffffffff01",
        "payment_profile": "d2b1c3a4e5f60718293a4b5c6d7e8f91"
      }
    ]
  }
}
```

## Sales Cart - GET /sn\_sales\_cart/sales\_cart/\{cartId\}/line-item/\{lineItemId\}

Returns a single cart line item from a given parent cart.

This endpoint is useful when an interface needs to refresh one product row after a change rather than re-reading the whole cart.

### URL format

Default URL: `/api/sn_sales_cart/sales_cart/{cartId}/line-item/{lineItemId}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cartId

</td><td>

Sys\_id of the parent cart.Data type: String

</td></tr><tr><td>

lineItemId

</td><td>

Sys\_id of the cart line item to return. Table location: Sales Cart Line Item \[sn\_sales\_cart\_line\_item\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`. Not required on this GET/DELETE request.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md) concept topic. Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|

### Status codes

|Status code|Description|
|-----------|-----------|
|200|Success. The line item was returned.|
|401|Unauthorized. The request was not authenticated.|
|403|Forbidden. The caller lacks execute access to the REST resource.|
|404|Not found. The line item or its parent cart does not resolve, or the caller can't read the parent cart.|
|500|Internal server error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

The cart line item record.Data type: Object

</td></tr><tr><td>

result.billing\_account

</td><td>

Billing account assigned to this line, from sn\_billing\_account\_billing\_account.Data type: String or Object

</td></tr><tr><td>

result.payment\_profile

</td><td>

Payment profile assigned to this line, from sn\_billing\_account\_payment\_profile.Data type: String or Object

</td></tr><tr><td>

result.price\_list

</td><td>

Price list propagated from the cart header at creation.Data type: String

</td></tr><tr><td>

error

</td><td>

Error message on failure.Data type: String

</td></tr></tbody>
</table>### cURL request

A portal refreshes one product row after the shopper reassigns its billing account.

```
curl --location --request GET \
  'https://<instance>.service-now.com/api/sn_sales_cart/sales_cart/7f3e2d1c0b9a8877665544332211ffee/line-item/1a2b3c4d5e6f708192a3b4c5d6e7f809' \
  --header 'Accept: application/json' \
  --user '<consumer_user>:<password>' 
```

Response body.

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "result": {
    "sys_id": "1a2b3c4d5e6f708192a3b4c5d6e7f809",
    "cart": "7f3e2d1c0b9a8877665544332211ffee",
    "billing_account": "c1a1b2c3d4e5f60709acbffffffffff01",
    "payment_profile": "d2b1c3a4e5f60718293a4b5c6d7e8f91"
  }
}
```

## Sales Cart - POST /sn\_sales\_cart/sales\_cart/\{cart\_id\}/submitOrder

Converts a draft cart into an order, propagating billing account and payment profile data from the cart lines onto the order lines. Billing data captured on the cart is copied to the order.

Propagation is performed by the Lead-to-Cash `sn_l2c_cart_to_order` mapping configuration, not by the handler. For each cart line, **billing\_account** is copied to the order line's **billing\_account** and **payment\_profile** is copied to the order line's payment.

Both target fields already existed on the order line dictionary; the Brazil release added only the entity attribute definitions and mapping rows that connect them. There is nothing for the caller to pass; the propagation is a side effect of submission.

A cart line with **billing\_account** and **payment\_profile** unset produces an order line with those fields empty, without error. Behavior for cascaded child order lines was explicitly left out of scope. The source integration test asserts only that propagation occurred, not that exactly one order line carries the values.

Once the cart leaves draft state, the consumer write and delete ACLs no longer apply to it, so submission is effectively the end of consumer-side mutation.

### URL format

Default URL: `/api/sn_sales_cart/sales_cart/{cartId}/submitOrder`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cartId

</td><td>

Sys\_id of the draft cart to submit.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|

### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md) concept topic. Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|

### Status codes

|Status code|Description|
|-----------|-----------|
|200 or 201|Success. The order and its order lines were created.|
|400|Bad request. Invalid or unsubmittable cart.|
|401|Unauthorized. The request was not authenticated.|
|403|Forbidden. The caller lacks execute access to the REST resource.|
|404|Not found. The cart does not resolve, or the caller can't see it.|
|409|Conflict. The cart is not in a submittable state, for example already submitted.|
|500|Internal server error, including a failure inside the cart-to-order mapping. If the order-line attribute definitions from app-ind-tmt-orm are absent, the mapping targets resolve to null and billing data is silently not propagated rather than erroring.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Container for the submission outcome.Data type: Object

</td></tr><tr><td>

result.orderId

</td><td>

Sys\_id of the created order.Data type: String

</td></tr><tr><td>

result.orderLines

</td><td>

Created order lines. Each carries **billing\_account** and **payment**, propagated from the corresponding cart line's billing\_account and payment\_profile.Data type: Array of Objects

</td></tr><tr><td>

error

</td><td>

Error message on failure.Data type: String

</td></tr></tbody>
</table>### cURL request

A consumer submits their draft cart. The order line that results carries the billing account and payment profile assigned to the corresponding cart line. The payment profile lands in the order line's payment field.

```
curl --location --request POST \
  'https://<instance>.service-now.com/api/sn_sales_cart/sales_cart/7f3e2d1c0b9a8877665544332211ffee/submitOrder' \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --user '<consumer_user>:<password>' 
```

Response body.

```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "result": {
    "orderId": "5b6c7d8e9f00112233445566778899aa",
    "order_lines": [
      {
        "sys_id": "aa9988776655443322110f9e8d7c6b5a",
        "billing_account": "c1a1b2c3d4e5f60709acbffffffffff01",
        "payment": "d2b1c3a4e5f60718293a4b5c6d7e8f91"
      }
    ]
  }
}
```

## Sales Cart - DELETE /sn\_sales\_cart/sales\_cart/\{cart\_id\}

Deletes a given sales cart.

### URL format

Default URL: `/api/sn_sales_cart/sales_cart/{cartId}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cartId

</td><td>

Sys\_id of the cart to delete.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`. Not required on this GET/DELETE request.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md) concept topic. Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|

### Status codes

|Status code|Description|
|-----------|-----------|
|200 or 204|Success. The cart was deleted.|
|401|Unauthorized. The request was not authenticated.|
|403|Forbidden. The caller lacks execute access, or the cart is not in draft state and the caller's delete ACL therefore does not apply.|
|404|Not found. The cart does not resolve, or the caller can't see it.|
|500|Internal server error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing details about the deletion.Data type: Object

</td></tr><tr><td>

error

</td><td>

Error message on failure.Data type: String

</td></tr></tbody>
</table>### cURL request

A consumer abandons their draft cart.

```
curl --location --request DELETE \
  'https://<instance>.service-now.com/api/sn_sales_cart/sales_cart/7f3e2d1c0b9a8877665544332211ffee' \
  --header 'Accept: application/json' \
  --user '<consumer_user>:<password>' 
```

Response body.

```
HTTP/1.1 200 OK
Content-Type: application/json

{ "result": { "deleted": true } }
```

## Sales Cart - DELETE /sn\_sales\_cart/sales\_cart/\{cartId\}/line-item/\{lineItemId\}

Removes a single line item from a given cart.

### URL format

Default URL: `/api/sn_sales_cart/sales_cart/{cartId}/line-item/{lineItemId}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cartId

</td><td>

Sys\_id of the parent cart.Data type: String

</td></tr><tr><td>

lineItemId

</td><td>

Sys\_id of the cart line item to delete.Table location: Sales Cart Line Item \[sn\_sales\_cart\_line\_item\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only **application/json** is supported; the resource declares `produces: application/json`.|
|Content-Type|Data format of the request body. Only **application/json** is supported; the resource declares `consumes: application/json`. Not required on this GET/DELETE request.|
|Authorization|Standard ServiceNow inbound REST authentication \(Basic or OAuth 2.0 bearer token\). The authenticated user must hold one of the roles named in the [Sales Cart REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/sales-cart-api.md) concept topic. Unauthenticated calls return 401.|

|Header|Description|
|------|-----------|
|Content-Type|Always **application/json**.|
|X-Total-Count|Not emitted by this endpoint.|

### Status codes

|Status code|Description|
|-----------|-----------|
|200 or 204|Success. The line item was deleted.|
|401|Unauthorized. The request was not authenticated.|
|403|Forbidden. The caller can't delete the parent cart, so the delegated line item delete is refused.|
|404|Not found. The line item or its parent cart does not resolve.|
|500|Internal server error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing details about the deletion.Data type: Object

</td></tr><tr><td>

error

</td><td>

Error message on failure.Data type: String

</td></tr></tbody>
</table>### cURL request

A consumer removes one product from their draft cart.

```
curl --location --request DELETE \
  'https://<instance>.service-now.com/api/sn_sales_cart/sales_cart/7f3e2d1c0b9a8877665544332211ffee/line-item/1a2b3c4d5e6f708192a3b4c5d6e7f809' \
  --header 'Accept: application/json' \
  --user '<consumer_user>:<password>' 
```

Response body.

```
HTTP/1.1 200 OK
Content-Type: application/json

{ "result": { "deleted": true } }
```

