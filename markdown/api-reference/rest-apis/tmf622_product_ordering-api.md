---
title: Product Order Open API
description: The Product Order Open API provides endpoints that enable a standardized mechanism for placing product orders.Retrieves all product orders.Retrieves all product orders.Retrieves the specified product order.Updates the specified customer order.Updates the specified customer order.Updates the specified customer order.Cancels the specified customer order.Creates the specified customer order and customer order line items.Creates the specified customer order and customer order line items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/tmf622\_product\_ordering-api.html
release: brazil
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 331
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Product Order Open API

The Product Order Open API provides endpoints that enable a standardized mechanism for placing product orders.

A product order is created based on a product offering that is defined and published in a product catalog. The product offering identifies the product or set of products that are available to a customer and includes the relevant product characteristics that capture the unique options of a product, and other relevant attributes such as pricing, contract terms, and availability.

To access this API, the Order Management for Telecommunications \(sn\_ind\_tmt\_orm\) plugin must be activated. For more information, see [Install Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-mgt-install-providers.md). For information about Order Management tables and roles, see [Components installed with Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/components-installed-with-order-management.md).

This API is provided within the `sn_ind_tmt_orm` namespace.

The calling user must have the sn\_ind\_tmt\_orm.order\_integrator role.

This API can be extended to make customizations around required parameters, request body validation, additional REST operations, and field mappings. For more information, see the [Product Order Open API Developer Guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/developer-guides/product-order_dev-guide.md).

The Product Order Open API is a ServiceNow® implementation of the TM Forum Product Ordering Management API Specification. This implementation is based on the [TMF622 Product Ordering Management API User Guide v5.0.0](https://www.tmforum.org/resources/specifications/tmf622-product-ordering-management-api-user-guide-v5-0-0/), September 2024. The Product Order Open API is conformance certified by TM Forum.

\[Omitted image "tmf-conformance.png"\] Alt text: TMF conformance logo

## Version 3.0 updates

The Product Order POST endpoint now supports creation of account, consumer, contact, location, billing accounts and payment profiles, and inline creation of related party entities within order requests. See [Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf622_product_ordering-api.md) for more details. These features are available with version 3.0 and newer releases.

The **relatedParty** field's structure changed between V2 and V3. See endpoints for a side-by-side comparison.

**Note:** This API's **productCharacteristic.valueType** field always returns the backend value \(for example, `choice`\) and is unaffected by the [Product Inventory Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/product-inventory-open-api.md)'s **sn\_prd\_invt.enableseamlessvaluetype** system property, which lets that API match this format.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/api-rest.md)

## Product Order Open API - GET /sn\_ind\_tmt\_orm/order/productOrder

Retrieves all product orders.

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]
-   Order Line Related Items \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

### v3 updates for GET/LIST operations

When you retrieve product orders using GET or LIST operations in TMF 622 V3, the response now includes payment profile details and billing account information for each order line item. These new fields provide complete visibility into the payment methods and billing relationships associated with your orders, enabling you to manage billing, fulfillment, and reconciliation processes with comprehensive order data in a single API call.

### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder`

### Supported request parameters

<table id="table_ofr_vgy_fsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Filter product orders by the associated account. Use this to retrieve all orders for a specific customer account or business unit.Data type: String

</td></tr><tr><td>

consumer \(relatedParty\)

</td><td>

Filter product orders by the consumer or end-user. Use this to retrieve orders for a specific consumer within a customer account, useful in multi-party or wholesale scenarios.Data type: String

</td></tr><tr><td>

contact

</td><td>

Filter product orders by an associated contact. Use this to find all orders linked to a specific person \(like order coordinator, and billing contact\).Data type: String

</td></tr><tr><td>

externalId

</td><td>

Filter product orders by external identifier. Use this to locate orders using identifiers from external systems or legacy integrations \(like legacy order numbers, or third-party reference IDs\).Data type: String

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Data type: String

Default: All fields returned.

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Data type: Number

Default: 20

Maximum: 100

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr><tr><td>

state

</td><td>

Filter orders by state. Only orders with a state matching the value of this parameter are returned in the response.Data type: String

Default: Don't order by state.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_h4r_fxr_nsb" class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr id="content-range-row"><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

</td></tr><tr id="content-type-row"><td>

Content-Type

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr id="links-pagination-row"><td>

Link

</td><td>

Contains the following links to navigate through query results.-   first
-   last
-   next
-   previous

</td></tr><tr id="x-total-count-row"><td id="x-total-count">

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table id="table_wdl_3xr_nsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="tmf-get-status-200-entry">

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

206

</td><td id="tmf-get-status-206-entry">

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td id="tmf-get-status-400-entry">

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="tmf-get-status-404-entry">

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="POST-GET-response-table" class="rest_api_response_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products.Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products.Data type: String

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products.Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.Stored in: committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number. This value is determined by an external system. Stored in: external\_id field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system identifier that originated the order request, appended with `TMF622`. Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

note

</td><td>

Additional notes made by the customer when ordering. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering.Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

orderDate

</td><td>

Date and time when the order was created.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order.Stored in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed.

Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed.-   When an existing billing account ID is passed, the API returns just the matching account's sys\_id and type.
-   When a billing account ID is passed that doesn't match an existing record, the API creates a new billing account with the provided ID as the external\_id. The object includes conditional attributes associated with the new record.

Data type: Object

Example reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Example creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

 Default: If not provided during creation, the system uses the default active value configured in your instance

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.

Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.

Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.

Data type: String

 Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

Conditional. If supplied, each entry requires **externalProductInventoryId**. External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Maximum length: 40

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed. Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile. -   If the passed profile ID already exists, the API returns just the matching payment profile's sys\_Id.
-   If the passed ID doesn't already exist, the API returns the new payment profile's sys\_id and associated attributes.

Data type: Object

Reference structure:

```
"payment": {
  "id": "String"
}
```

Creation structure:

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

See the 'Examples' section for POST requests demonstrating both reference and creation patterns.

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned only for profile creation. A choice field representing the specific payment method type.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned only for profile creation. An external reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Data type: String

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record.Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product.Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   true: Product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   false: If the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an OrderLineItemContact. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order containing customer account or consumer account information. Supports reference and inline creation patterns \(Account, Contact, Location\). Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

realtedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   Account
-   Contact
-   Customer
-   Location

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Record type of the party. Matches the **relatedParty.role** value.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party.-   If the passed ID already exists, the API returns just the **@type** and **id** fields of the matching party.
-   If the passed ID doesn't already exist, the API returns a the new Account, Contact, or Location ID with its conditional attributes, which vary based on the **@type** value.

Data type: Object

Reference pattern:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String"
}
```

Account creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "accountNumber": "String",
  "status": "String"
}
```

Contact creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "firstName": "String",
  "lastName": "String",
  "email": "String"
 }
```

Location creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "name": "String",
  "address": "String",
  "city": "String",
  "postalCode": "String",
  "country": "String"
 }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Indicates the type of reference being provided. Value is always `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Returned for Account party types. External reference number or identifier for the Account.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Returned for Location party types. Street address of the location.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Returned for Location party types. City or municipality name for the location.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Returned for Location party types. Country where the location is physically situated or where the contact is based.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Returned for Contact party types. Contact person's primary email address.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Returned for Contact party types. Contact person's first name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id or external\_id of the party record.Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Returned for Contact party types. Contact person's last name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Returned for Account, Contact, and Location types. Name of the account, contact, or location. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Required for Location party types. Postal code, ZIP code, or PIN code for the location.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Returned for Account party types. Current status of the account. Possible values for the status field depend on how your instance is configured.Common values include:

-   `Active`: Account is in normal operation
-   `Inactive`: Account is not currently conducting business
-   `Suspended`: Account is temporarily restricted
-   `Pending`: Account is awaiting activation
-   `Archived`: Historical accounts
-   `Under Review`: Account is being evaluated

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

state

</td><td>

Current state of the order.Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action carried out on the product.Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Description of the reason for the order line item.Data type: String

Stored in: action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Identifies the billing account and determines how the account is processed.-   When you provide a **billing.id** that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields you include \(**name**, **status**, **active**\) are ignored. The system uses only the ID to find and link the existing billing account.
-   When you provide a **billing.id** that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(**name**, **status**, **active**\) are required.

Data type: Object

Reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Returned for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Returned only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Returned for account creation. Display name of the billing account.Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Returned for account creation. The status of the billing account. Possible values depend on your instance configuration. Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

External IDs which map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed.Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Details about the payment profile.Data type: Object

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected **paymentMethod**.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned for profile creation. External reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Unique identifier of the product sold. Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record. Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product. Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Specification details associated with the product. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Matches the value of **version**.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Matches the value of **internalVersion**.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an Order Line Item Contact. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: `OrderLineItemContact`

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`.Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact.Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact.Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Details of the product offering associated with the product.Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr></tbody>
</table>### cURL request

This example retrieves all product orders.

```
curl --location --request GET 'https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder' \
--user 'username':'password'
```

Response body.

```
[
   {
      "id": "8d75939453126010a795ddeeff7b126a",
      "href": "/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a",
      "ponr": "false",
      "orderCurrency": "USD",
      "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
      "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
      "requestedStartDate": "2020-05-03T08:13:59.000Z",
      "channel": [
         {
            "id": "1",
            "name": "Agent Assist"
         }
      ],
      "note": [
         {
            "author": "System Administrator",
            "date": "2021-02-25T14:22:07.000Z",
            "text": "This is a TMF product order illustration no 2"
         },
         {
            "author": "System Administrator",
            "date": "2021-02-25T14:22:06.000Z",
            "text": "This is a TMF product order illustration"
         }
      ],
      "productOrderItem": [
         {
            "id": "POI130",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "actionReason": "adding service package OLI",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "USD",
                        "value": 20
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productCharacteristic": [
                  {
                     "name": "Security Type",
                     "valueType": "Choice",
                     "value": "Base",
                     "previousValue": ""
                  }
               ],
               "productSpecification": {
                  "id": "a6514bd3534560102f18ddeeff7b1247",
                  "name": "SD-WAN Security",
                  "version": "v1",
                  "internalVersion": "1",
                  "internalId": "a6514bd3534560102f18ddeeff7b1247",
                  "@type": "ProductSpecificationRef"
               },
               "relatedParty": [
                  {
                     "id": "4175939453126010a795ddeeff7b127d",
                     "name": "John Smith",
                     "email": "abc2@example.com",
                     "phone": "32456768",
                     "@type": "RelatedParty",
                     "@referredType": "OrderLineItemContact"
                  },
                  {
                     "id": "c175939453126010a795ddeeff7b127c",
                     "name": "Joe Doe",
                     "email": "abc@example.com",
                     "phone": "1234567890",
                     "@type": "RelatedParty",
                     "@referredType": "OrderLineItemContact"
                  }
               ]
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering",
               "version": "v1",
               "internalId": "69017a0f536520103b6bddeeff7b127d",
               "internalVersion": "1"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI100",
                  "relationshipType": "HasParent"
               }
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         },
         {
            "id": "POI100",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productSpecification": {
                  "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
                  "name": "SD-WAN Service Package",
                  "version": "v1",
                  "internalVersion": "1",
                  "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
                  "@type": "ProductSpecificationRef"
               }
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering",
               "version": "v1",
               "internalId": "69017a0f536520103b6bddeeff7b127d",
               "internalVersion": "1"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI130",
                  "relationshipType": "HasChild"
               },
               {
                  "id": "POI120",
                  "relationshipType": "HasChild"
               },
               {
                  "id": "POI110",
                  "relationshipType": "HasChild"
               }
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         },
         {
            "id": "POI120",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "USD",
                        "value": 20
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productCharacteristic": [
                  {
                     "name": "CPE Type",
                     "valueType": "Choice",
                     "value": "Physical",
                     "previousValue": ""
                  },
                  {
                     "name": "WAN Optimization",
                     "valueType": "Choice",
                     "value": "Advance",
                     "previousValue": ""
                  },
                  {
                     "name": "Routing",
                     "valueType": "Choice",
                     "value": "Premium",
                     "previousValue": ""
                  },
                  {
                     "name": "CPE Model",
                     "valueType": "Choice",
                     "value": "ASR",
                     "previousValue": ""
                  }
               ],
               "productSpecification": {
                  "id": "39b627aa53702010cd6dddeeff7b1202",
                  "name": "SD-WAN Edge Device",
                  "version": "v1",
                  "internalVersion": "1",
                  "internalId": "39b627aa53702010cd6dddeeff7b1202",
                  "@type": "ProductSpecificationRef"
               },
               "productRelationship": [
                  {
                     "id": "326d13f45b5620102dff5e92dc81c785",
                     "relationshipType": "Requires"
                  }
               ]
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "69017a0f536520103b6bddeeff7b127d"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI100",
                  "relationshipType": "HasParent"
               },
               {
                  "id": "POI110",
                  "relationshipType": "Requires"
               }       
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         },
         {
            "id": "POI110",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "USD",
                        "value": 5
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productCharacteristic": [
                  {
                     "name": "Tenancy",
                     "valueType": "Choice",
                     "value": "Base (10 site)",
                     "previousValue": ""
                  }
               ],
               "productSpecification": {
                  "id": "216663aa53702010cd6dddeeff7b12b5",
                  "name": "SD-WAN Controller",
                  "version": "v1",
                  "internalVersion": "1",
                  "internalId": "216663aa53702010cd6dddeeff7b12b5",
                  "@type": "ProductSpecificationRef"
               },
               "place": {
                  "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                  "@type": "Place"
               }
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering",
               "version": "v1",
               "internalId": "69017a0f536520103b6bddeeff7b127d",
               "internalVersion": "1"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI100",
                  "relationshipType": "HasParent"
               }
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         }
      ],
      "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrder"
   }
]
```

GET response with TMF 622 V3 parameters \(relatedParty, billingAccount and payment\)

```
[
  {
    "id": "8d75939453126010a795ddeeff7b126a",
    "href": "/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a",
    "ponr": "false",
    "orderCurrency": "USD",
    "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
    "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
    "requestedStartDate": "2020-05-03T08:13:59.000Z",
    "channel": [
      {
        "id": "1",
        "name": "Agent Assist"
      }
    ],
    "note": [
      {
        "author": "System Administrator",
        "date": "2021-02-25T14:22:07.000Z",
        "text": "This is a TMF product order illustration no 2"
      },
      {
        "author": "System Administrator",
        "date": "2021-02-25T14:22:06.000Z",
        "text": "This is a TMF product order illustration"
      }
    ],
    "productOrderItem": [
      {
        "id": "POI130",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "actionReason": "adding service package OLI",
        "billingAccount": {
          "id": "sys_id_ba_001",
          "name": "Funco Intl - Main Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "id": "sys_id_payment_001",
          "paymentMethod": "Credit Card",
          "paymentMethodType": "Visa",
          "paymentReferenceId": "REF-2024-001"
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "USD",
                "value": 20
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productCharacteristic": [
            {
              "name": "Security Type",
              "valueType": "Choice",
              "value": "Base",
              "previousValue": ""
            }
          ],
          "productSpecification": {
            "id": "a6514bd3534560102f18ddeeff7b1247",
            "name": "SD-WAN Security",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "a6514bd3534560102f18ddeeff7b1247",
            "@type": "ProductSpecificationRef"
          },
          "relatedParty": [
            {
              "id": "4175939453126010a795ddeeff7b127d",
              "name": "John Smith",
              "email": "abc2@example.com",
              "phone": "32456768",
              "@type": "RelatedParty",
              "@referredType": "OrderLineItemContact"
            },
            {
              "id": "c175939453126010a795ddeeff7b127c",
              "name": "Joe Doe",
              "email": "abc@example.com",
              "phone": "1234567890",
              "@type": "RelatedParty",
              "@referredType": "OrderLineItemContact"
            }
          ]
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering",
          "version": "v1",
          "internalId": "69017a0f536520103b6bddeeff7b127d",
          "internalVersion": "1"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI100",
            "relationshipType": "HasParent"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      },
      {
        "id": "POI100",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "billingAccount": {
          "id": "sys_id_ba_002",
          "name": "Funco Intl - Service Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "id": "sys_id_payment_002",
          "paymentMethod": "Bank Transfer",
          "paymentMethodType": "ACH",
          "paymentReferenceId": "REF-2024-002"
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productSpecification": {
            "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
            "name": "SD-WAN Service Package",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
            "@type": "ProductSpecificationRef"
          }
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering",
          "version": "v1",
          "internalId": "69017a0f536520103b6bddeeff7b127d",
          "internalVersion": "1"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI130",
            "relationshipType": "HasChild"
          },
          {
            "id": "POI120",
            "relationshipType": "HasChild"
          },
          {
            "id": "POI110",
            "relationshipType": "HasChild"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      },
      {
        "id": "POI120",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "billingAccount": {
          "id": "sys_id_ba_003",
          "name": "Funco Intl - Equipment Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "id": "sys_id_payment_003",
          "paymentMethod": "Credit Card",
          "paymentMethodType": "MasterCard",
          "paymentReferenceId": "REF-2024-003"
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "USD",
                "value": 20
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productCharacteristic": [
            {
              "name": "CPE Type",
              "valueType": "Choice",
              "value": "Physical",
              "previousValue": ""
            },
            {
              "name": "WAN Optimization",
              "valueType": "Choice",
              "value": "Advance",
              "previousValue": ""
            },
            {
              "name": "Routing",
              "valueType": "Choice",
              "value": "Premium",
              "previousValue": ""
            },
            {
              "name": "CPE Model",
              "valueType": "Choice",
              "value": "ASR",
              "previousValue": ""
            }
          ],
          "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202",
            "@type": "ProductSpecificationRef"
          },
          "productRelationship": [
            {
              "id": "326d13f45b5620102dff5e92dc81c785",
              "relationshipType": "Requires"
            }
          ]
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering",
          "version": "v1",
          "internalVersion": "1",
          "internalId": "69017a0f536520103b6bddeeff7b127d"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI100",
            "relationshipType": "HasParent"
          },
          {
            "id": "POI110",
            "relationshipType": "Requires"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      },
      {
        "id": "POI110",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "billingAccount": {
          "id": "sys_id_ba_002",
          "name": "Funco Intl - Service Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "USD",
                "value": 5
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productCharacteristic": [
            {
              "name": "Tenancy",
              "valueType": "Choice",
              "value": "Base (10 site)",
              "previousValue": ""
            }
          ],
          "productSpecification": {
            "id": "216663aa53702010cd6dddeeff7b12b5",
            "name": "SD-WAN Controller",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "216663aa53702010cd6dddeeff7b12b5",
            "@type": "ProductSpecificationRef"
          },
          "place": {
            "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
            "@type": "Place"
          }
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering",
          "version": "v1",
          "internalId": "69017a0f536520103b6bddeeff7b127d",
          "internalVersion": "1"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI100",
            "relationshipType": "HasParent"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      }
    ],
    "relatedParty": [
      {
        "role": "Contact",
        "@type": "Contact",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "eaf68911c35420105252716b7d40ddde",
          "name": "Sally Thomas",
          "email": "sally.thomas@funcointl.com"
        }
      },
      {
        "role": "Account",
        "@type": "Account",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "ffc68911c35420105252716b7d40dd55",
          "name": "Funco Intl"
        }
      },
      {
        "role": "Consumer",
        "@type": "Consumer",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "59f16de1c3b67110ff00ed23a140dd9e",
          "name": "Funco External"
        }
      }
    ],
    "state": "in_progress",
    "version": "1",
    "@type": "ProductOrder"
  }
]
```

### Reading Payment Information from Orders

When you retrieve an order using GET or LIST operations, the payment object is included in the order line item response only if a payment profile is actively linked. If an order line item \(OLI\) does not have a linked payment profile, the payment field is not included in the response. When the payment object is present, it contains all four fields \(id, paymentMethod, paymentMethodType, paymentReferenceId\) representing the complete profile details.

Example GET response:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "ba_456"
        },
        "payment": {
          "id": "sys_id_payment_profile_123",
          "paymentMethod": "Credit Card",
          "paymentMethodType": "Visa",
          "paymentReferenceId": "REF-2024-001"
        }
      }
    ]
  }
}
```

Example GET response without payment profile:

```
{
  "productOrder": {
    "id": "order_003",
    "orderItem": [
      {
        "id": "order_line_003",
        "product": {
          "id": "prod_789"
        },
        "billingAccount": {
          "id": "ba_999"
        }
      }
    ]
  }
}
```

### Reading Billing Account Information from Orders

When you retrieve an order using GET or LIST operations, the billingAccount field is included in the order line item response with the system ID reference and any available billing account details.

Example GET response with billing account reference:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_456",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

Example GET response with newly created billing account:

```
{
  "productOrder": {
    "id": "order_002",
    "orderItem": [
      {
        "id": "order_line_002",
        "product": {
          "id": "prod_456"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_789",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

## Product Order Open API - GET /sn\_ind\_tmt\_orm/productorder

Retrieves all product orders.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - GET /sn\_ind\_tmt\_orm/order/productOrder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf622_product_ordering-api.md).

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]

### v3 updates for GET/LIST operations

When you retrieve product orders using GET or LIST operations in TMF 622 V3, the response now includes payment profile details and billing account information for each order line item. These new fields provide complete visibility into the payment methods and billing relationships associated with your orders, enabling you to manage billing, fulfillment, and reconciliation processes with comprehensive order data in a single API call.

### URL format

Default URL: `/api/sn_ind_tmt_orm/productorder`

### Supported request parameters

<table id="table_ofr_vgy_fsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Filter product orders by the associated account. Use this to retrieve all orders for a specific customer account or business unit.Data type: String

</td></tr><tr><td>

consumer \(relatedParty\)

</td><td>

Filter product orders by the consumer or end-user. Use this to retrieve orders for a specific consumer within a customer account, useful in multi-party or wholesale scenarios.Data type: String

</td></tr><tr><td>

contact

</td><td>

Filter product orders by an associated contact. Use this to find all orders linked to a specific person \(like order coordinator, and billing contact\).Data type: String

</td></tr><tr><td>

externalId

</td><td>

Filter product orders by external identifier. Use this to locate orders using identifiers from external systems or legacy integrations \(like legacy order numbers, or third-party reference IDs\).Data type: String

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Data type: String

Default: All fields returned.

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Data type: Number

Default: 20

Maximum: 100

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr><tr><td>

state

</td><td>

Filter orders by state. Only orders with a state matching the value of this parameter are returned in the response.Data type: String

Default: Don't order by state.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_h4r_fxr_nsb" class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr id="content-range-row"><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

</td></tr><tr id="content-type-row"><td>

Content-Type

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr id="links-pagination-row"><td>

Link

</td><td>

Contains the following links to navigate through query results.-   first
-   last
-   next
-   previous

</td></tr><tr id="x-total-count-row"><td id="x-total-count">

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table id="table_wdl_3xr_nsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="tmf-get-status-200-entry">

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

206

</td><td id="tmf-get-status-206-entry">

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td id="tmf-get-status-400-entry">

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="tmf-get-status-404-entry">

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="POST-GET-response-table" class="rest_api_response_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products.Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products.Data type: String

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products.Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.Stored in: committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number. This value is determined by an external system. Stored in: external\_id field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system identifier that originated the order request, appended with `TMF622`. Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

note

</td><td>

Additional notes made by the customer when ordering. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering.Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

orderDate

</td><td>

Date and time when the order was created.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order.Stored in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed.

Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed.-   When an existing billing account ID is passed, the API returns just the matching account's sys\_id and type.
-   When a billing account ID is passed that doesn't match an existing record, the API creates a new billing account with the provided ID as the external\_id. The object includes conditional attributes associated with the new record.

Data type: Object

Example reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Example creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

 Default: If not provided during creation, the system uses the default active value configured in your instance

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.

Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.

Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.

Data type: String

 Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

Conditional. If supplied, each entry requires **externalProductInventoryId**. External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Maximum length: 40

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed. Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile. -   If the passed profile ID already exists, the API returns just the matching payment profile's sys\_Id.
-   If the passed ID doesn't already exist, the API returns the new payment profile's sys\_id and associated attributes.

Data type: Object

Reference structure:

```
"payment": {
  "id": "String"
}
```

Creation structure:

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

See the 'Examples' section for POST requests demonstrating both reference and creation patterns.

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned only for profile creation. A choice field representing the specific payment method type.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned only for profile creation. An external reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Data type: String

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record.Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product.Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   true: Product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   false: If the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an OrderLineItemContact. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order containing customer account or consumer account information. Supports reference and inline creation patterns \(Account, Contact, Location\). Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

realtedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   Account
-   Contact
-   Customer
-   Location

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Record type of the party. Matches the **relatedParty.role** value.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party.-   If the passed ID already exists, the API returns just the **@type** and **id** fields of the matching party.
-   If the passed ID doesn't already exist, the API returns a the new Account, Contact, or Location ID with its conditional attributes, which vary based on the **@type** value.

Data type: Object

Reference pattern:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String"
}
```

Account creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "accountNumber": "String",
  "status": "String"
}
```

Contact creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "firstName": "String",
  "lastName": "String",
  "email": "String"
 }
```

Location creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "name": "String",
  "address": "String",
  "city": "String",
  "postalCode": "String",
  "country": "String"
 }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Indicates the type of reference being provided. Value is always `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Returned for Account party types. External reference number or identifier for the Account.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Returned for Location party types. Street address of the location.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Returned for Location party types. City or municipality name for the location.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Returned for Location party types. Country where the location is physically situated or where the contact is based.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Returned for Contact party types. Contact person's primary email address.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Returned for Contact party types. Contact person's first name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id or external\_id of the party record.Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Returned for Contact party types. Contact person's last name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Returned for Account, Contact, and Location types. Name of the account, contact, or location. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Required for Location party types. Postal code, ZIP code, or PIN code for the location.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Returned for Account party types. Current status of the account. Possible values for the status field depend on how your instance is configured.Common values include:

-   `Active`: Account is in normal operation
-   `Inactive`: Account is not currently conducting business
-   `Suspended`: Account is temporarily restricted
-   `Pending`: Account is awaiting activation
-   `Archived`: Historical accounts
-   `Under Review`: Account is being evaluated

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

state

</td><td>

Current state of the order.Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action carried out on the product.Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Description of the reason for the order line item.Data type: String

Stored in: action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Identifies the billing account and determines how the account is processed.-   When you provide a **billing.id** that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields you include \(**name**, **status**, **active**\) are ignored. The system uses only the ID to find and link the existing billing account.
-   When you provide a **billing.id** that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(**name**, **status**, **active**\) are required.

Data type: Object

Reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Returned for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Returned only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Returned for account creation. Display name of the billing account.Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Returned for account creation. The status of the billing account. Possible values depend on your instance configuration. Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

External IDs which map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed.Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Details about the payment profile.Data type: Object

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected **paymentMethod**.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned for profile creation. External reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Unique identifier of the product sold. Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record. Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product. Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Specification details associated with the product. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Matches the value of **version**.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Matches the value of **internalVersion**.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an Order Line Item Contact. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: `OrderLineItemContact`

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`.Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact.Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact.Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Details of the product offering associated with the product.Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr></tbody>
</table>### cURL request

This example retrieves all product orders.

```
curl --location --request GET 'https://instance.servicenow.com/api/sn_ind_tmt_orm/productorder' \
--user 'username':'password'


```

Response body.

```
[
   {
      "id": "8d75939453126010a795ddeeff7b126a",
      "ponr": "false",
      "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
      "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
      "requestedStartDate": "2020-05-03T08:13:59.000Z",
      "channel": [
         {
            "id": "1",
            "name": "Agent Assist"
         }
      ],
      "note": [
         {
            "author": "System Administrator",
            "date": "2021-02-25T14:22:07.000Z",
            "text": "This is a TMF product order illustration no 2"
         },
         {
            "author": "System Administrator",
            "date": "2021-02-25T14:22:06.000Z",
            "text": "This is a TMF product order illustration"
         }
      ],
      "productOrderItem": [
         {
            "id": "POI130",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "actionReason": "adding service package OLI",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "USD",
                        "value": 20
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productCharacteristic": [
                  {
                     "name": "Security Type",
                     "valueType": "Choice",
                     "value": "Base",
                     "previousValue": ""
                  }
               ],
               "productSpecification": {
                  "id": "a6514bd3534560102f18ddeeff7b1247",
                  "name": "SD-WAN Security",
                  "@type": "ProductSpecificationRef"
               },
               "relatedParty": [
                  {
                     "id": "4175939453126010a795ddeeff7b127d",
                     "name": "John Smith",
                     "email": "abc2@example.com",
                     "phone": "32456768",
                     "@type": "RelatedParty",
                     "@referredType": "OrderLineItemContact"
                  },
                  {
                     "id": "c175939453126010a795ddeeff7b127c",
                     "name": "Joe Doe",
                     "email": "abc@example.com",
                     "phone": "1234567890",
                     "@type": "RelatedParty",
                     "@referredType": "OrderLineItemContact"
                  }
               ]
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI100",
                  "relationshipType": "HasParent"
               }
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         },
         {
            "id": "POI100",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productSpecification": {
                  "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
                  "name": "SD-WAN Service Package",
                  "@type": "ProductSpecificationRef"
               }
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI130",
                  "relationshipType": "HasChild"
               },
               {
                  "id": "POI120",
                  "relationshipType": "HasChild"
               },
               {
                  "id": "POI110",
                  "relationshipType": "HasChild"
               }
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         },
         {
            "id": "POI120",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "actionReason":"adding service package OLI",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "USD",
                        "value": 20
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productCharacteristic": [
                  {
                     "name": "CPE Type",
                     "valueType": "Choice",
                     "value": "Physical",
                     "previousValue": ""
                  },
                  {
                     "name": "WAN Optimization",
                     "valueType": "Choice",
                     "value": "Advance",
                     "previousValue": ""
                  },
                  {
                     "name": "Routing",
                     "valueType": "Choice",
                     "value": "Premium",
                     "previousValue": ""
                  },
                  {
                     "name": "CPE Model",
                     "valueType": "Choice",
                     "value": "ASR",
                     "previousValue": ""
                  }
               ],
               "productSpecification": {
                  "id": "39b627aa53702010cd6dddeeff7b1202",
                  "name": "SD-WAN Edge Device",
                  "@type": "ProductSpecificationRef"
               }
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI100",
                  "relationshipType": "HasParent"
               }
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         },
         {
            "id": "POI110",
            "ponr": "false",
            "quantity": 1,
            "action": "add",
            "actionReason": "adding service package OLI",
            "itemPrice": [
               {
                  "priceType": "recurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "INR",
                        "value": 0
                     }
                  }
               },
               {
                  "priceType": "nonRecurring",
                  "price": {
                     "taxIncludedAmount": {
                        "unit": "USD",
                        "value": 5
                     }
                  }
               }
            ],
            "product": {
               "@type": "Product",
               "productCharacteristic": [
                  {
                     "name": "Tenancy",
                     "valueType": "Choice",
                     "value": "Base (10 site)",
                     "previousValue": ""
                  }
               ],
               "productSpecification": {
                  "id": "216663aa53702010cd6dddeeff7b12b5",
                  "name": "SD-WAN Controller",
                  "@type": "ProductSpecificationRef"
               },
               "place": {
                  "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                  "@type": "Place"
               }
            },
            "productOffering": {
               "id": "69017a0f536520103b6bddeeff7b127d",
               "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
               {
                  "id": "POI100",
                  "relationshipType": "HasParent"
               }
            ],
            "state": "in_progress",
            "version": "1",
            "@type": "ProductOrderItem"
         }
      ],
      "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrder"
   }
]
```

GET response with TMF 622 V3 parameters \(relatedParty, billingAccount and payment\)

```
[
  {
    "id": "8d75939453126010a795ddeeff7b126a",
    "ponr": "false",
    "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
    "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
    "requestedStartDate": "2020-05-03T08:13:59.000Z",
    "channel": [
      {
        "id": "1",
        "name": "Agent Assist"
      }
    ],
    "note": [
      {
        "author": "System Administrator",
        "date": "2021-02-25T14:22:07.000Z",
        "text": "This is a TMF product order illustration no 2"
      },
      {
        "author": "System Administrator",
        "date": "2021-02-25T14:22:06.000Z",
        "text": "This is a TMF product order illustration"
      }
    ],
    "productOrderItem": [
      {
        "id": "POI130",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "actionReason": "adding service package OLI",
        "billingAccount": {
          "id": "ext_ba_funco_security",
          "name": "Funco Intl - Security Services",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "paymentMethod": "Credit Card",
          "paymentMethodType": "Visa",
          "paymentReferenceId": "REF-2024-SD-SECURITY"
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "USD",
                "value": 20
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productCharacteristic": [
            {
              "name": "Security Type",
              "valueType": "Choice",
              "value": "Base",
              "previousValue": ""
            }
          ],
          "productSpecification": {
            "id": "a6514bd3534560102f18ddeeff7b1247",
            "name": "SD-WAN Security",
            "@type": "ProductSpecificationRef"
          },
          "relatedParty": [
            {
              "id": "4175939453126010a795ddeeff7b127d",
              "name": "John Smith",
              "email": "abc2@example.com",
              "phone": "32456768",
              "@type": "RelatedParty",
              "@referredType": "OrderLineItemContact"
            },
            {
              "id": "c175939453126010a795ddeeff7b127c",
              "name": "Joe Doe",
              "email": "abc@example.com",
              "phone": "1234567890",
              "@type": "RelatedParty",
              "@referredType": "OrderLineItemContact"
            }
          ]
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI100",
            "relationshipType": "HasParent"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      },
      {
        "id": "POI100",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "billingAccount": {
          "id": "ext_ba_funco_service",
          "name": "Funco Intl - Service Package",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "paymentMethod": "Bank Transfer",
          "paymentMethodType": "ACH",
          "paymentReferenceId": "REF-2024-SD-SERVICE"
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productSpecification": {
            "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
            "name": "SD-WAN Service Package",
            "@type": "ProductSpecificationRef"
          }
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI130",
            "relationshipType": "HasChild"
          },
          {
            "id": "POI120",
            "relationshipType": "HasChild"
          },
          {
            "id": "POI110",
            "relationshipType": "HasChild"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      },
      {
        "id": "POI120",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "actionReason": "adding service package OLI",
        "billingAccount": {
          "id": "ext_ba_funco_equipment",
          "name": "Funco Intl - Equipment Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "paymentMethod": "Credit Card",
          "paymentMethodType": "MasterCard",
          "paymentReferenceId": "REF-2024-SD-EQUIPMENT"
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "USD",
                "value": 20
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productCharacteristic": [
            {
              "name": "CPE Type",
              "valueType": "Choice",
              "value": "Physical",
              "previousValue": ""
            },
            {
              "name": "WAN Optimization",
              "valueType": "Choice",
              "value": "Advance",
              "previousValue": ""
            },
            {
              "name": "Routing",
              "valueType": "Choice",
              "value": "Premium",
              "previousValue": ""
            },
            {
              "name": "CPE Model",
              "valueType": "Choice",
              "value": "ASR",
              "previousValue": ""
            }
          ],
          "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "@type": "ProductSpecificationRef"
          }
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI100",
            "relationshipType": "HasParent"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      },
      {
        "id": "POI110",
        "ponr": "false",
        "quantity": 1,
        "action": "add",
        "actionReason": "adding service package OLI",
        "billingAccount": {
          "id": "sys_id_ba_existing_controller",
          "@type": "BillingAccountRef"
        },
        "itemPrice": [
          {
            "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          },
          {
            "priceType": "nonRecurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "USD",
                "value": 5
              }
            }
          }
        ],
        "product": {
          "@type": "Product",
          "productCharacteristic": [
            {
              "name": "Tenancy",
              "valueType": "Choice",
              "value": "Base (10 site)",
              "previousValue": ""
            }
          ],
          "productSpecification": {
            "id": "216663aa53702010cd6dddeeff7b12b5",
            "name": "SD-WAN Controller",
            "@type": "ProductSpecificationRef"
          },
          "place": {
            "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
            "@type": "Place"
          }
        },
        "productOffering": {
          "id": "69017a0f536520103b6bddeeff7b127d",
          "name": "Premium SD-WAN Offering"
        },
        "productOrderItemRelationship": [
          {
            "id": "POI100",
            "relationshipType": "HasParent"
          }
        ],
        "state": "in_progress",
        "version": "1",
        "@type": "ProductOrderItem"
      }
    ],
    "relatedParty": [
      {
        "role": "Contact",
        "@type": "Contact",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "eaf68911c35420105252716b7d40ddde"
        }
      },
      {
        "role": "Account",
        "@type": "Account",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "ffc68911c35420105252716b7d40dd55"
        }
      },
      {
        "role": "Consumer",
        "@type": "Consumer",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "59f16de1c3b67110ff00ed23a140dd9e"
        }
      }
    ],
    "state": "in_progress",
    "version": "1",
    "@type": "ProductOrder"
  }
]
```

### Reading Payment Information from Orders

When you retrieve an order using GET or LIST operations, the payment object is included in the order line item response only if a payment profile is actively linked. If an order line item \(OLI\) does not have a linked payment profile, the payment field is not included in the response. When the payment object is present, it contains all four fields \(id, paymentMethod, paymentMethodType, paymentReferenceId\) representing the complete profile details.

Example GET response:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "ba_456"
        },
        "payment": {
          "id": "sys_id_payment_profile_123",
          "paymentMethod": "Credit Card",
          "paymentMethodType": "Visa",
          "paymentReferenceId": "REF-2024-001"
        }
      }
    ]
  }
}
```

Example GET response without payment profile:

```
{
  "productOrder": {
    "id": "order_003",
    "orderItem": [
      {
        "id": "order_line_003",
        "product": {
          "id": "prod_789"
        },
        "billingAccount": {
          "id": "ba_999"
        }
      }
    ]
  }
}
```

### Reading Billing Account Information from Orders

When you retrieve an order using GET or LIST operations, the billingAccount field is included in the order line item response with the system ID reference and any available billing account details.

Example GET response with billing account reference:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_456",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

Example GET response with newly created billing account:

```
{
  "productOrder": {
    "id": "order_002",
    "orderItem": [
      {
        "id": "order_line_002",
        "product": {
          "id": "prod_456"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_789",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

## Product Order Open API - GET /sn\_ind\_tmt\_orm/productorder/\{id\}

Retrieves the specified product order.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - GET /sn\_ind\_tmt\_orm/productorder/\{id\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf622_product_ordering-api.md).

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]

### v3 updates for GET/LIST operations

When you retrieve product orders using GET or LIST operations in TMF 622 V3, the response now includes payment profile details and billing account information for each order line item. These new fields provide complete visibility into the payment methods and billing relationships associated with your orders, enabling you to manage billing, fulfillment, and reconciliation processes with comprehensive order data in a single API call.

### URL format

Default URL: `/api/sn_ind_tmt_orm/productorder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the customer order to retrieve.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Filter product orders by the associated account. Use this to retrieve all orders for a specific customer account or business unit.Data type: String

</td></tr><tr><td>

consumer \(relatedParty\)

</td><td>

Filter product orders by the consumer or end-user. Use this to retrieve orders for a specific consumer within a customer account, useful in multi-party or wholesale scenarios.Data type: String

</td></tr><tr><td>

contact

</td><td>

Filter product orders by an associated contact. Use this to find all orders linked to a specific person \(like order coordinator, and billing contact\).Data type: String

</td></tr><tr><td>

externalId

</td><td>

Filter product orders by external identifier. Use this to locate orders using identifiers from external systems or legacy integrations \(like legacy order numbers, or third-party reference IDs\).Data type: String

</td></tr><tr><td>

state

</td><td>

Filter orders by state. Only orders with a state matching the value of this parameter are returned in the response.Data type: String

Default: Don't order by state.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Can be for any of the following reasons:-   Missing query parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="POST-GET-response-table" class="rest_api_response_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products.Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products.Data type: String

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products.Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.Stored in: committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number. This value is determined by an external system. Stored in: external\_id field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system identifier that originated the order request, appended with `TMF622`. Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

note

</td><td>

Additional notes made by the customer when ordering. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering.Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

orderDate

</td><td>

Date and time when the order was created.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order.Stored in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed.

Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed.-   When an existing billing account ID is passed, the API returns just the matching account's sys\_id and type.
-   When a billing account ID is passed that doesn't match an existing record, the API creates a new billing account with the provided ID as the external\_id. The object includes conditional attributes associated with the new record.

Data type: Object

Example reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Example creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

 Default: If not provided during creation, the system uses the default active value configured in your instance

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.

Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.

Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.

Data type: String

 Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

Conditional. If supplied, each entry requires **externalProductInventoryId**. External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Maximum length: 40

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed. Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile. -   If the passed profile ID already exists, the API returns just the matching payment profile's sys\_Id.
-   If the passed ID doesn't already exist, the API returns the new payment profile's sys\_id and associated attributes.

Data type: Object

Reference structure:

```
"payment": {
  "id": "String"
}
```

Creation structure:

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

See the 'Examples' section for POST requests demonstrating both reference and creation patterns.

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned only for profile creation. A choice field representing the specific payment method type.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned only for profile creation. An external reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Data type: String

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record.Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product.Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   true: Product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   false: If the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an OrderLineItemContact. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order containing customer account or consumer account information. Supports reference and inline creation patterns \(Account, Contact, Location\). Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

realtedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   Account
-   Contact
-   Customer
-   Location

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Record type of the party. Matches the **relatedParty.role** value.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party.-   If the passed ID already exists, the API returns just the **@type** and **id** fields of the matching party.
-   If the passed ID doesn't already exist, the API returns a the new Account, Contact, or Location ID with its conditional attributes, which vary based on the **@type** value.

Data type: Object

Reference pattern:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String"
}
```

Account creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "accountNumber": "String",
  "status": "String"
}
```

Contact creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "firstName": "String",
  "lastName": "String",
  "email": "String"
 }
```

Location creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "name": "String",
  "address": "String",
  "city": "String",
  "postalCode": "String",
  "country": "String"
 }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Indicates the type of reference being provided. Value is always `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Returned for Account party types. External reference number or identifier for the Account.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Returned for Location party types. Street address of the location.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Returned for Location party types. City or municipality name for the location.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Returned for Location party types. Country where the location is physically situated or where the contact is based.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Returned for Contact party types. Contact person's primary email address.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Returned for Contact party types. Contact person's first name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id or external\_id of the party record.Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Returned for Contact party types. Contact person's last name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Returned for Account, Contact, and Location types. Name of the account, contact, or location. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Required for Location party types. Postal code, ZIP code, or PIN code for the location.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Returned for Account party types. Current status of the account. Possible values for the status field depend on how your instance is configured.Common values include:

-   `Active`: Account is in normal operation
-   `Inactive`: Account is not currently conducting business
-   `Suspended`: Account is temporarily restricted
-   `Pending`: Account is awaiting activation
-   `Archived`: Historical accounts
-   `Under Review`: Account is being evaluated

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

state

</td><td>

Current state of the order.Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action carried out on the product.Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Description of the reason for the order line item.Data type: String

Stored in: action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Identifies the billing account and determines how the account is processed.-   When you provide a **billing.id** that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields you include \(**name**, **status**, **active**\) are ignored. The system uses only the ID to find and link the existing billing account.
-   When you provide a **billing.id** that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(**name**, **status**, **active**\) are required.

Data type: Object

Reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Returned for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Returned only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Returned for account creation. Display name of the billing account.Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Returned for account creation. The status of the billing account. Possible values depend on your instance configuration. Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

External IDs which map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed.Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Details about the payment profile.Data type: Object

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected **paymentMethod**.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned for profile creation. External reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Unique identifier of the product sold. Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record. Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product. Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Specification details associated with the product. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Matches the value of **version**.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Matches the value of **internalVersion**.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an Order Line Item Contact. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: `OrderLineItemContact`

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`.Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact.Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact.Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Details of the product offering associated with the product.Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr></tbody>
</table>### cURL request

The following code example requests an existing customer order.

```
curl -X GET "https://servicenow-instance/api/sn_ind_tmt_orm/productorder/8d75939453126010a795ddeeff7b126a" \
-u "username":"password" 


```

Response body.

```
{
  "id": "8d75939453126010a795ddeeff7b126a",
  "ponr": "false",
  "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
  "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
  "requestedStartDate": "2020-05-03T08:13:59.000Z",
  "channel": [
    {
      "id": "1",
      "name": "Agent Assist"
    }
  ],
  "note": [
    {
      "author": "System Administrator",
      "date": "2021-02-25T14:22:07.000Z",
      "text": "This is a TMF product order illustration no 2"
    },
    {
      "author": "System Administrator",
      "date": "2021-02-25T14:22:06.000Z",
      "text": "This is a TMF product order illustration"
    }
  ],

  "productOrderItem": [
    {
      "id": "POI130",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "actionReason":"adding service package OLI",
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Security Type",
            "valueType": "Choice",
            "value": "Base",
            "previousValue": ""
          }
        ],
        "productSpecification": {
          "id": "a6514bd3534560102f18ddeeff7b1247",
          "name": "SD-WAN Security",
          "@type": "ProductSpecificationRef"
        },
        "relatedParty": [
          {
            "id": "4175939453126010a795ddeeff7b127d",
            "name": "John Smith",
            "email": "abc2@example.com",
            "phone": "32456768",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          },
          {
            "id": "c175939453126010a795ddeeff7b127c",
            "name": "Joe Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ]
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
    "id": "POI100",
    "ponr": "false",
    "quantity": 1,
    "action": "add",
    "itemPrice": [
      {
        "priceType": "recurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "INR",
            "value": 0
          }
        }
      },
      {
        "priceType": "nonRecurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "INR",
            "value": 0
          }
        }
      }
    ],
    "product": {
      "@type": "Product",
      "productSpecification": {
        "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
        "name": "SD-WAN Service Package",
        "@type": "ProductSpecificationRef"
      }
    },
    "productOffering": {
      "id": "69017a0f536520103b6bddeeff7b127d",
      "name": "Premium SD-WAN Offering"
    },
    "productOrderItemRelationship": [
      {
        "id": "POI130",
        "relationshipType": "HasChild"
      },
      {
        "id": "POI120",
        "relationshipType": "HasChild"
      },
      {
        "id": "POI110",
        "relationshipType": "HasChild"
      }
    ],
    "state": "in_progress",
    "version": "1",
    "@type": "ProductOrderItem"
  },
  {
    "id": "POI120",
    "ponr": "false",
    "quantity": 1,
    "action": "add",
    "itemPrice": [
      {
        "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "CPE Type",
            "valueType": "Choice",
            "value": "Physical",
            "previousValue": ""
          },
          {
            "name": "WAN Optimization",
            "valueType": "Choice",
            "value": "Advance",
            "previousValue": ""
          },
          {
            "name": "Routing",
            "valueType": "Choice",
            "value": "Premium",
            "previousValue": ""
          },
          {
            "name": "CPE Model",
            "valueType": "Choice",
            "value": "ASR",
            "previousValue": ""
           }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI110",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "actionReason":"adding service package OLI",
      "itemPrice": [
        {
          "priceType": "recurring",
            "price": {
              "taxIncludedAmount": {
                "unit": "INR",
                "value": 0
              }
            }
          },
          {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 5
            }
          }
        }
      ],
      "product": {
      "@type": "Product",
      "productCharacteristic": [
        {
          "name": "Tenancy",
          "valueType": "Choice",
          "value": "Base (10 site)",
          "previousValue": ""
        }
      ],
      "productSpecification": {
        "id": "216663aa53702010cd6dddeeff7b12b5",
        "name": "SD-WAN Controller",
        "@type": "ProductSpecificationRef"
      },
      "place": {
        "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
        "@type": "Place"
      }
    },
    "productOffering": {
      "id": "69017a0f536520103b6bddeeff7b127d",
      "name": "Premium SD-WAN Offering"
    },
    "productOrderItemRelationship": [
      {
        "id": "POI100",
        "relationshipType": "HasParent"
      }
    ],
    "state": "in_progress",
    "version": "1",
    "@type": "ProductOrderItem"
  }
],
"relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
"state": "in_progress",
"version": "1",
"@type": "ProductOrder"
}
```

GET response with TMF 622 V3 parameters \(relatedParty, billingAccount and payment\)

```
{
  "id": "8d75939453126010a795ddeeff7b126a",
  "ponr": "false",
  "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
  "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
  "requestedStartDate": "2020-05-03T08:13:59.000Z",
  "channel": [
    {
      "id": "1",
      "name": "Agent Assist"
    }
  ],
  "note": [
    {
      "author": "System Administrator",
      "date": "2021-02-25T14:22:07.000Z",
      "text": "This is a TMF product order illustration no 2"
    },
    {
      "author": "System Administrator",
      "date": "2021-02-25T14:22:06.000Z",
      "text": "This is a TMF product order illustration"
    }
  ],
  "productOrderItem": [
    {
      "id": "POI130",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "actionReason": "adding service package OLI",
      "billingAccount": {
        "id": "ext_ba_security_001",
        "name": "Funco Intl - Security Services",
        "@type": "BillingAccountRef",
        "status": "Active",
        "active": true
      },
      "payment": {
        "paymentMethod": "Credit Card",
        "paymentMethodType": "Visa",
        "paymentReferenceId": "REF-2024-SECURITY"
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Security Type",
            "valueType": "Choice",
            "value": "Base",
            "previousValue": ""
          }
        ],
        "productSpecification": {
          "id": "a6514bd3534560102f18ddeeff7b1247",
          "name": "SD-WAN Security",
          "@type": "ProductSpecificationRef"
        },
        "relatedParty": [
          {
            "id": "4175939453126010a795ddeeff7b127d",
            "name": "John Smith",
            "email": "abc2@example.com",
            "phone": "32456768",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          },
          {
            "id": "c175939453126010a795ddeeff7b127c",
            "name": "Joe Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ]
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI100",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "billingAccount": {
        "id": "ext_ba_service_001",
        "name": "Funco Intl - Service Package",
        "@type": "BillingAccountRef",
        "status": "Active",
        "active": true
      },
      "payment": {
        "paymentMethod": "Bank Transfer",
        "paymentMethodType": "ACH",
        "paymentReferenceId": "REF-2024-SERVICE"
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productSpecification": {
          "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "name": "SD-WAN Service Package",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI130",
          "relationshipType": "HasChild"
        },
        {
          "id": "POI120",
          "relationshipType": "HasChild"
        },
        {
          "id": "POI110",
          "relationshipType": "HasChild"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI120",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "billingAccount": {
        "id": "ext_ba_equipment_001",
        "name": "Funco Intl - Equipment Billing",
        "@type": "BillingAccountRef",
        "status": "Active",
        "active": true
      },
      "payment": {
        "paymentMethod": "Credit Card",
        "paymentMethodType": "MasterCard",
        "paymentReferenceId": "REF-2024-EQUIPMENT"
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "CPE Type",
            "valueType": "Choice",
            "value": "Physical",
            "previousValue": ""
          },
          {
            "name": "WAN Optimization",
            "valueType": "Choice",
            "value": "Advance",
            "previousValue": ""
          },
          {
            "name": "Routing",
            "valueType": "Choice",
            "value": "Premium",
            "previousValue": ""
          },
          {
            "name": "CPE Model",
            "valueType": "Choice",
            "value": "ASR",
            "previousValue": ""
          }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI110",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "actionReason": "adding service package OLI",
      "billingAccount": {
        "id": "sys_id_ba_existing_controller",
        "@type": "BillingAccountRef"
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 5
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Tenancy",
            "valueType": "Choice",
            "value": "Base (10 site)",
            "previousValue": ""
          }
        ],
        "productSpecification": {
          "id": "216663aa53702010cd6dddeeff7b12b5",
          "name": "SD-WAN Controller",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    }
  ],
  "relatedParty": [
    {
      "role": "Contact",
      "@type": "Contact",
      "partyOrPartyRole": {
        "@type": "PartyRef",
        "id": "eaf68911c35420105252716b7d40ddde"
      }
    },
    {
      "role": "Account",
      "@type": "Account",
      "partyOrPartyRole": {
        "@type": "PartyRef",
        "id": "ffc68911c35420105252716b7d40dd55"
      }
    },
    {
      "role": "Consumer",
      "@type": "Consumer",
      "partyOrPartyRole": {
        "@type": "PartyRef",
        "id": "59f16de1c3b67110ff00ed23a140dd9e"
      }
    }
  ],
  "state": "in_progress",
  "version": "1",
  "@type": "ProductOrder"
}
```

### Reading Payment Information from Orders

When you retrieve an order using GET or LIST operations, the payment object is included in the order line item response only if a payment profile is actively linked. If an order line item \(OLI\) does not have a linked payment profile, the payment field is not included in the response. When the payment object is present, it contains all four fields \(id, paymentMethod, paymentMethodType, paymentReferenceId\) representing the complete profile details.

Example GET response:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "ba_456"
        },
        "payment": {
          "id": "sys_id_payment_profile_123",
          "paymentMethod": "Credit Card",
          "paymentMethodType": "Visa",
          "paymentReferenceId": "REF-2024-001"
        }
      }
    ]
  }
}
```

Example GET response without payment profile:

```
{
  "productOrder": {
    "id": "order_003",
    "orderItem": [
      {
        "id": "order_line_003",
        "product": {
          "id": "prod_789"
        },
        "billingAccount": {
          "id": "ba_999"
        }
      }
    ]
  }
}
```

### Reading Billing Account Information from Orders

When you retrieve an order using GET or LIST operations, the billingAccount field is included in the order line item response with the system ID reference and any available billing account details.

Example GET response with billing account reference:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_456",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

Example GET response with newly created billing account:

```
{
  "productOrder": {
    "id": "order_002",
    "orderItem": [
      {
        "id": "order_line_002",
        "product": {
          "id": "prod_456"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_789",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

## Product Order Open API - GET /sn\_ind\_tmt\_orm/order/productOrder/\{id\}

Updates the specified customer order.

### v3 updates for GET/LIST operations

When you retrieve product orders using GET or LIST operations in TMF 622 V3, the response now includes payment profile details and billing account information for each order line item. These new fields provide complete visibility into the payment methods and billing relationships associated with your orders, enabling you to manage billing, fulfillment, and reconciliation processes with comprehensive order data in a single API call.

### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order to update.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Filter product orders by the associated account. Use this to retrieve all orders for a specific customer account or business unit.Data type: String

</td></tr><tr><td>

consumer \(relatedParty\)

</td><td>

Filter product orders by the consumer or end-user. Use this to retrieve orders for a specific consumer within a customer account, useful in multi-party or wholesale scenarios.Data type: String

</td></tr><tr><td>

contact

</td><td>

Filter product orders by an associated contact. Use this to find all orders linked to a specific person \(like order coordinator, and billing contact\).Data type: String

</td></tr><tr><td>

externalId

</td><td>

Filter product orders by external identifier. Use this to locate orders using identifiers from external systems or legacy integrations \(like legacy order numbers, or third-party reference IDs\).Data type: String

</td></tr><tr><td>

state

</td><td>

Filter orders by state. Only orders with a state matching the value of this parameter are returned in the response.Data type: String

Default: Don't order by state.

</td></tr></tbody>
</table><table id="id_vk2_p5n_t4b" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td id="type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always ProductOrder. This information is not stored.Data type: String

</td></tr><tr><td>

changeType

</td><td>

Controls which fields in the PATCH request are processed. When provided, only non-product fields \(notes and contacts\) are updated and the order state remains unchanged without triggering product change workflows or state transitions. When absent, standard product-change behavior applies.Supported value: `nonProduct`

Only these fields are processed when `changeType=nonProduct`:

-   `note` \(order-level\)
-   `relatedParty` \(order-level\)
-   `productOrderItem[].id`
-   `productOrderItem[].relatedParty`
-   `productOrderItem[].note`

All other fields \(including product-related fields\) are silently ignored.

**Note:** When using this field, order state remains unchanged \(does NOT transition to revision\_received\). No inflight or revision flows are triggered, and changes are isolated to metadata fields only.

Data type: String

</td></tr><tr id="channel-row-tmf622"><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products.Data type: Array of Objects

</td></tr><tr id="channel_id-row-tmf622"><td>

channel.id

</td><td>

Required if the **channel** parameter is used. Unique identifier of the channel to use to sell the associated products. Data type: String

Table: In the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

channel.id

</td><td>

Unique identifier of the channel to use to sell the associated products.Data type: String

</td></tr><tr id="channel_name-row-tmf622"><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: empty string

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products.Data type: String

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-PATCH">

Date and time when the action must be performed on the order.This value must be the same as or later than the **committedDueDate** values for each order line item.

If the action for order line items is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order. This value must be the same as or later than the committedDueDate values for each order line item.Data type: String

</td></tr><tr id="externalId-row-tmf622"><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Stored in: The external\_id field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number.Data type: String

</td></tr><tr><td>

externalSystem

</td><td id="tmf622-response-externalSystem">

External system of the service order, appended with `TMF622`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF622`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the product order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order created for this request.Data type: String

</td></tr><tr id="note-row-tmf622"><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering. Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering.Data type: Array of Objects`"note": [{ "text": "String" }]`

</td></tr><tr id="note_text-row-tmf622"><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering.Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items. Updating the currency code of an existing order is not supported. Providing any value other than the currency code already associated with the order causes the update to be rejected.Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order to be created. On successful request, the order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed. This value is the only result if the order is created asynchronously using the mode query parameter.Data type: String

</td></tr><tr id="productOrderItem-row-tmf622"><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "revisionOperation": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem

</td><td>

Required. Items associated with the product order and their associated action.Data type: Array of Objects

```
"productOrderItem": [{
                "action": "String", "billingAccount": {Object}, "id": "String",
                "payment": {Object}, "product": {Object}, "productOffering": {Object}, ...
                }]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td id="prodOrdItem_type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always ProductOrderItem. This information is not stored.Data type: String

</td></tr><tr id="productOrderItem_action-row-tmf622"><td>

productOrderItem.action

</td><td>

Required if the **productOrderItem** parameter is used. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: add

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table.Data type: String

Possible values: add, change, delete, no-change, resume, suspend

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="prodOrdItem_actionReason-response-tmf622">

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed. When you provide a billing.id that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields are ignored. The system uses only the ID to find and link the existing billing account. When you provide a billing.id that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(name, status, active\) are required for inline creation.Data type: Object

```
"billingAccount": { "id": "String",
                "@type": "BillingAccountRef", "name": "String", "status": "String",
                "active": Boolean }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be BillingAccountRef. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.Valid values:

-   true: Billing account is active
-   false: Billing account isn't active

Data type: Boolean

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.Examples: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.Data type: String

Examples: "Active", "Inactive", "Suspended"

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-PATCH">

Date and time when the action must be performed on the order line item.If the action for the item is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.Data type: String

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

Conditional. If supplied, each entry requires externalProductInventoryId. External IDs to map to the product inventories created for the order.Data type: Array of Objects```
"externalProductInventory": [{ "externalProductInventoryId":
                "String" }]
```

</td></tr><tr id="externalProdInvId"><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-decsr">

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the sn\_ind\_tmt\_orm\_order\_line\_item table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID mapped to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr id="externalProdInv-PATCH"><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-descr-PATCH">

Conditional. If supplied, each entry requires **externalProductInventoryId**. List of external IDs to map to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr id="productOrderItem_id-row-tmf622"><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Sys\_id or external\_id of the order line item. Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

Default: empty string

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item.Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.Maximum length: 40

</td></tr><tr id="itemPrice-row-tmf622"><td>

productOrderItem.itemPrice

</td><td id="itemPrice-entry-tmf622">

List that describes the price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product.```
Data type: Array of Objects
```

```
"itemPrice": [{ "price": {Object}, "priceType": "String",
                "recurringChargePeriod": "String" }]
```

</td></tr><tr id="itemPrice_price-row-tmf622"><td>

productOrderItem.itemPrice.price

</td><td id="itemPrice_price-entry-tmf622">

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product.Data type: Object

```
"price": { "taxIncludedAmount": {Object} }
```

</td></tr><tr id="itemPrice_price_taxIncludedAmt-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td id="itemPrice_price_taxIncludedAmt-entry-tmf622">

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax.Data type: Object

```
"taxIncludedAmount": { "unit": "String", "value":
                Number }
```

</td></tr><tr id="itemPrice_price_taxIncludedAmt_unit-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td id="itemPrice_price_taxIncludedAmt_unit-entry-tmf622">

Currency code in which the price is depicted. Data type: String

Stored in: The mrc or nrc field in the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed.Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr id="itemPrice_price_taxIncludedAmt_value-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td id="itemPrice_price_taxIncludedAmt_value-entry-tmf622">

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field in the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax.Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr id="itemPrice_priceType-row-tmf622"><td>

productOrderItem.itemPrice.priceType

</td><td id="itemPrice_priceType-entry-tmf622">

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring.Data type: String

</td></tr><tr id="itemPrice_recurringChargePeriod-row-tmf622"><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td id="itemPrice_recurringChargePeriod-entry-tmf622">

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as month.Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile and determines how the profile is processed. Reference an existing payment profile by passing payment.id, or pass full payment attributes to create payment profile inline. If the ID already exists, the API locates the matching payment profile and links it to the order line item. Any other payment fields are ignored. The system uses only the id to find and link the existing profile. If the ID doesn't already exist, a payment profile is created automatically and linked to the order line item's billing account. paymentMethod, paymentMethodType, paymentReferenceId are required to create the new profile.Data type: Object

```
"payment": { "id": "String", "paymentMethod": "String",
                "paymentMethodType": "String", "paymentReferenceId": "String" }
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Required. Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Conditional, required only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Data type: String

Examples: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Conditional, required only for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected paymentMethod. This field is ignored when referencing an existing profile.Data type: String

Examples: "Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Conditional, required only for profile creation. An external reference identifier for the payment profile. This is typically used for tracking, audit trails, and reconciliation between your order system and your payment processor. This field is ignored when referencing an existing profile.Data type: String

Examples: "REF-2024-001", "CARD-XXXX-5678"

</td></tr><tr id="product-row-tmf622"><td>

productOrderItem.product

</td><td>

Required if **productOrderItem.action** is change or delete. Description of the instance details of the product purchased by the customer. Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product

</td><td>

Required if productOrderItem.action is change or delete. Instance details of the product purchased by the customer.Data type: Object

```
"product": {
 "id": "String",
 "place": {Object},
 "productCharacteristic": [Array],
 "productSpecification": {Object},
 "relatedParty": [Array],
 "@type": "String"
}
```

</td></tr><tr id="product_type-row-tmf622"><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always Product. This information is not stored.Data type: String

</td></tr><tr id="product_id-row-tmf622"><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

Default: empty string

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Required if productOrderItem.action is change or delete. Unique identifier of the product sold.Data type: String

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr id="product_place-row-tmf622"><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product.Data type: Object

```
"place": { "id": "String", "@type": "String"
              }
```

</td></tr><tr id="product_place_type-row-tmf622"><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always Place. This information is not stored.Data type: String

</td></tr><tr id="product_place_id-row-tmf622"><td>

productOrderItem.product.place.id

</td><td>

Required if the **productOrderItem.product.place** parameter is used. Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

Stored in: The location field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record. When employing the change action on a product order item \(via the productOrderItem.action parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location.Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr id="prod_prodChar-row-tmf622"><td>

productOrderItem.product.productCharacteristic

</td><td>

List of characteristics of the associated product. Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product.Data type: Array of Objects

```
"productCharacteristic": [{ "name": "String",
                "previousValue": "String", "value": "String", "valueType": "String"
                }]
```

</td></tr><tr id="prod_prodChar_name-row-tmf622"><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr id="prod_prodChar_previousValue-row-tmf622"><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the productOrderItem.action parameter is other than add.Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr id="prod_prodChar_value-row-tmf622"><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product.Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Data type: String

Possible values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type:String

</td></tr><tr id="product_productSpecification-row-tmf622"><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   When this system property is set to true \(default\), the product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   When this system property is set to false, if the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Optional. Description of the product specification associated with the product.Data type: Object

```
"productSpecification": { "id":
                "String", "internalVersion": "String", "name": "String", "version":
                "String", "@type": "String" }
```

</td></tr><tr id="product_productSpecification_type-row-tmf622"><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always ProductSpecificationRef. This information is not stored.Data type: String

</td></tr><tr id="product_productSpecification_id-row-tmf622"><td>

productOrderItem.product.productSpecification.id

</td><td>

Required if the **productOrderItem.product.productSpecification** parameter is used. Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalId

</td><td>

Initial version of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td id="tmf622-response-internalVersion">

Internal version of the product specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Must match the value of version otherwise an error is thrown.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr id="product_productSpecification_name-row-tmf622"><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td id="tmf622-response-version">

External version of the product specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the product specification. Must match the value of internalVersion otherwise an error is thrown.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr id="product_relatedParty-row-tmf622"><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of contacts for line items. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "id": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of party roles linked to an OrderLineItemContact.Data type: Array of Objects

```
"relatedParty": [{ "email": "String", "firstName":
                "String", "lastName": "String", "phone": "String", "@referredType":
                "String", "@type": "String" }]
```

</td></tr><tr id="product_relatedParty_referredType-row-tmf622"><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer.Possible value: OrderLineItemContact

Data type: String

</td></tr><tr id="product_relatedParty_type-row-tmf622"><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always RelatedParty. This information is not stored.Data type: String

</td></tr><tr id="product_relatedParty_email-row-tmf622"><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact.Data type: StringStored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="product_relatedParty_firstName-row-tmf622"><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact.Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="product_relatedParty_id-row-tmf622"><td>

productOrderItem.product.relatedParty.id

</td><td>

Required. Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

Stored in: The sys\_id field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr id="product_relatedParty_lastName-row-tmf622"><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact.Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="product_relatedParty_phone-row-tmf622"><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact.Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="productOffering-row-tmf622"><td>

productOrderItem.productOffering

</td><td>

Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product.Data type: Object

```
"productOffering": { "id": "String",
                "internalVersion": "String", "name": "String", "version": "String"
                }
```

</td></tr><tr id="productOffering_id-row-tmf622"><td>

productOrderItem.productOffering.id

</td><td>

Required if the **productOrderItem.productOffering** parameter is used. Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: StringTable: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalId

</td><td>

Initial version of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: StringTable: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: StringTable: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr id="productOffering_name-row-tmf622"><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: StringTable: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: StringTable: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr id="productOrdItem_quantity-row-tmf622"><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order.

Default: null

</td></tr><tr id="productOrderItemRelationship-row-tmf622"><td>

productOrderItem.productOrderItemRelationship

</td><td>

Conditional. Item-level relationships. If supplied, each entry requires an **id** and **relationshipType**. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items.Data type: Array of Objects

```
"productOrderItemRelationship":
                [{ "id": "String", "relationshipType": "String" }]
```

</td></tr><tr id="productOrderItemRelationship_id-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required if the **productOrderItem.productOrderItemRelationship** parameter is used. Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Stored in: The parent\_line\_item field of thebsn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required. Same as the productOrderItem.id value. Used for parent/child relationship.Data type: StringStored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr id="productOrderItemRelationship_relType-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify relationship hierarchy.Data type: StringPossible values: HasChild, HasParent

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

productOrderItem.revisionOperation

</td><td>

Type of update to perform on the line item. If this value is empty, the existing line item is updated, or a new line item is added if it does not already exist. If this value is `cancel`, the line item is canceled.Data type: String

Default: empty string

</td></tr><tr id="relatedParty-row-tmf622"><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Contains at least one item with customer account or consumer account information. Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array containing customer account or consumer account information.Data type: Array of Objects

```
"relatedParty": [
 {
   "role": "String",
   "@type": "String",
   "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr id="relatedParty_referredType-row-tmf622"><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   **Consumer**
-   **Customer**
-   **CustomerContact**

Data type: String

</td></tr><tr id="relatedParty_type-row-tmf622"><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Specifies what record type to search for when validating and linking the party. Must match the **role** field.Possible values:

-   `Account`
-   `Contact`
-   `Customer`
-   `Location`

Data type: String

</td></tr><tr id="relatedParty_id-row-tmf622"><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table.

Data type: String

</td></tr><tr id="relatedParty_name-row-tmf622"><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party. Attributes vary based on party type.-   For reference patterns, this object contains just the **@type** and **id** fields.
-   For creation patterns, this object also contains conditional attributes used to create the new record, if the **id** value does not match an existing record.

Data type: Object

```
"partyOrPartyRole": {
 "@type": "PartyRef",
 "id": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Indicates the type of reference being provided. Value must be set to `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Returned for Account party types. External reference number or identifier for the Account. It provides a business-facing account identifier that is distinct from the system-generated ID. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Returned for Location party types during inline creation. Street address of the location. Used only during inline creation; ignored for reference patterns.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Returned for Location party types during inline creation. City or municipality name for the location. Used only during inline creation; ignored for reference patterns.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Returned for Location party types during inline creation. Country where the location is physically situated or where the contact is based. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Returned for Contact party types during inline creation. Contact person's primary email address. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Returned for Contact party types during inline creation. Contact person's first name or given name. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id or external\_id of the party record to reference. The system searches for a record with either a matching system ID or matching External ID.-   For reference patterns with an existing record, only the id is used and all other provided fields are ignored.
-   For creation patterns when no matching record exists, the ID becomes the external ID of the newly created record, and other provided fields populate the new record's attributes.

Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[cmn\_location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Returned for Contact party types during inline creation. Contact person's last name or given name. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Returned for Account, Contact, and Location types during inline creation. Name of the account, contact, or location. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Returned for Location party types during inline creation. Postal code, ZIP code, or PIN code for the location. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Returned for Account party types during inline creation. Current status of the account. The valid values for the status field depend on how your instance is configured. Used only during inline creation; ignored for reference patterns.Common values:

-   `Active`
-   `Inactive`
-   `Suspended`
-   `Pending`
-   `Archived`
-   `Under Review`

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the referenced party plays in the order context. Must match **relatedParty.@type** in the same object.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr id="requestedCompletionDate-row-tmf622"><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

Stored in: The expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer.Data type: String

</td></tr><tr id="requestedStartDate-row-tmf622"><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer. Data type: String

Stored in: The expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. For this endpoint, this value is always new.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table id="table_xfv_2vk_5rb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record:

-   `The following Order Item characteristics does not exist: Review specification <**characteristic.name**> and correct the characteristic and characteristic option in the order line item prior to approving the order.`
-   `Order Item characteristic: <**characteristic.name**> with characteristic value: <**characteristic.value**>is invalid. Correct the characteristic values before approving the order.`

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   `Invalid payload: Request body missing` - Payload was not passed in the request body.
-   `Invalid payload: productOrderItem is missing` - Product order line item object or JSON is missing.
-   `Invalid payload: productOrderItem id is missing` - The **id** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem action is missing` - The **action** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem productOffering is missing` - The product offering object or JSON is missing from the product order line item in the payload.
-   `Invalid payload: productOffering id is missing` - The **id** parameter is missing in the product order line item of the product offering object in the payload.
-   `Invalid payload: Product offering does not exist` - The product offering in the product order line item is not valid.
-   `Invalid payload: productOrderItem product is missing` - The product object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: product productSpecification is missing` - The product specification object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: productSpecification id is missing` - The **id** parameter in the product order line item of the product specification object is missing from the payload.
-   `Invalid payload: Product specification does not exist` - The product specification in the product order line item is not valid.
-   `Invalid payload: Product Inventory does not exist` - In a change order \(action = change\), the quantity of an item is greater than what is in stock.
-   `Invalid payload: Product inventory ID is missing` - In a change order, the **product.id** is missing in the payload.
-   `Invalid payload: Sold Product is inactive` - In a change order, a product specified in the payload is inactive.
-   `Invalid payload: relatedParty is missing` - The related party object is missing from the payload.
-   `Customer Account or Consumer is missing` - The related party customer or consumer object is missing from the payload.
-   `Invalid payload: Consumer does not exist` - The specified related party consumer does not exist in the ServiceNow instance.
-   `Invalid payload: Customer Account does not exist` - The specified related party customer does not exist in the ServiceNow instance.
-   `Invalid payload: Order creation failed` - Not able to create the requested order.
-   `In-flight revision to order currency not supported` - The **orderCurrency** parameter can't be updated after the order is created.
-   `This order is yet to be created in customer order table. Please check in inbound queue for more details.` – The order ID provided is not in the customer order table.
-   `Patch request cannot be made as the order's fulfillment type is not 'deliver.` – The patch request was made on an order which has a fulfillment type other than deliver.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="POST-GET-response-table" class="rest_api_response_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products.Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products.Data type: String

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products.Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.Stored in: committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number. This value is determined by an external system. Stored in: external\_id field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system identifier that originated the order request, appended with `TMF622`. Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

note

</td><td>

Additional notes made by the customer when ordering. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering.Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

orderDate

</td><td>

Date and time when the order was created.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order.Stored in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed.

Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed.-   When an existing billing account ID is passed, the API returns just the matching account's sys\_id and type.
-   When a billing account ID is passed that doesn't match an existing record, the API creates a new billing account with the provided ID as the external\_id. The object includes conditional attributes associated with the new record.

Data type: Object

Example reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Example creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

 Default: If not provided during creation, the system uses the default active value configured in your instance

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.

Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.

Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.

Data type: String

 Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

Conditional. If supplied, each entry requires **externalProductInventoryId**. External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Maximum length: 40

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed. Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile. -   If the passed profile ID already exists, the API returns just the matching payment profile's sys\_Id.
-   If the passed ID doesn't already exist, the API returns the new payment profile's sys\_id and associated attributes.

Data type: Object

Reference structure:

```
"payment": {
  "id": "String"
}
```

Creation structure:

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

See the 'Examples' section for POST requests demonstrating both reference and creation patterns.

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned only for profile creation. A choice field representing the specific payment method type.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned only for profile creation. An external reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Data type: String

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record.Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product.Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   true: Product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   false: If the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an OrderLineItemContact. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order containing customer account or consumer account information. Supports reference and inline creation patterns \(Account, Contact, Location\). Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

realtedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   Account
-   Contact
-   Customer
-   Location

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Record type of the party. Matches the **relatedParty.role** value.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party.-   If the passed ID already exists, the API returns just the **@type** and **id** fields of the matching party.
-   If the passed ID doesn't already exist, the API returns a the new Account, Contact, or Location ID with its conditional attributes, which vary based on the **@type** value.

Data type: Object

Reference pattern:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String"
}
```

Account creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "accountNumber": "String",
  "status": "String"
}
```

Contact creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "firstName": "String",
  "lastName": "String",
  "email": "String"
 }
```

Location creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "name": "String",
  "address": "String",
  "city": "String",
  "postalCode": "String",
  "country": "String"
 }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Indicates the type of reference being provided. Value is always `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Returned for Account party types. External reference number or identifier for the Account.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Returned for Location party types. Street address of the location.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Returned for Location party types. City or municipality name for the location.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Returned for Location party types. Country where the location is physically situated or where the contact is based.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Returned for Contact party types. Contact person's primary email address.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Returned for Contact party types. Contact person's first name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id or external\_id of the party record.Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Returned for Contact party types. Contact person's last name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Returned for Account, Contact, and Location types. Name of the account, contact, or location. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Required for Location party types. Postal code, ZIP code, or PIN code for the location.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Returned for Account party types. Current status of the account. Possible values for the status field depend on how your instance is configured.Common values include:

-   `Active`: Account is in normal operation
-   `Inactive`: Account is not currently conducting business
-   `Suspended`: Account is temporarily restricted
-   `Pending`: Account is awaiting activation
-   `Archived`: Historical accounts
-   `Under Review`: Account is being evaluated

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

state

</td><td>

Current state of the order.Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action carried out on the product.Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Description of the reason for the order line item.Data type: String

Stored in: action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Identifies the billing account and determines how the account is processed.-   When you provide a **billing.id** that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields you include \(**name**, **status**, **active**\) are ignored. The system uses only the ID to find and link the existing billing account.
-   When you provide a **billing.id** that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(**name**, **status**, **active**\) are required.

Data type: Object

Reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Returned for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Returned only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Returned for account creation. Display name of the billing account.Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Returned for account creation. The status of the billing account. Possible values depend on your instance configuration. Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

External IDs which map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed.Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Details about the payment profile.Data type: Object

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected **paymentMethod**.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned for profile creation. External reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Unique identifier of the product sold. Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record. Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product. Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Specification details associated with the product. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Matches the value of **version**.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Matches the value of **internalVersion**.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an Order Line Item Contact. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: `OrderLineItemContact`

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`.Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact.Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact.Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Details of the product offering associated with the product.Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr></tbody>
</table>### cURL request

This example retrieves the given product order associated with the ID 8d75939453126010a795ddeeff7b126a.

```
curl -X GET "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "channel": [
    {
      "id": "1",
      "name": "Agent Assist"
    }
  ]
}
```

Response body.

```
{
   "id": "8d75939453126010a795ddeeff7b126a",
   "href": "/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a",
   "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
   "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
   "requestedStartDate": "2020-05-03T08:13:59.000Z",
   "externalId": "PO-456",
   "orderCurrency": "USD",
   "channel": [
      {
         "id": "1",
         "name": "Agent Assist"
      }
   ],
   "note": [
      {
         "author": "System Administrator",
         "date": "2021-02-25T14:22:07.000Z",
         "text": "This is a TMF product order illustration no 2"
      },
      {
         "author": "System Administrator",
         "date": "2021-02-25T14:22:06.000Z",
         "text": "This is a TMF product order illustration"
      }
   ],
   "productOrderItem": [
      {
         "id": "POI130",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "actionReason": "adding service package OLI",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "USD",
                     "value": 20
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productCharacteristic": [
               {
                  "name": "Security Type",
                  "valueType": "Choice",
                  "value": "Base",
                  "previousValue": ""
               }
            ],
            "productSpecification": {
               "id": "a6514bd3534560102f18ddeeff7b1247",
               "name": "SD-WAN Security",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "a6514bd3534560102f18ddeeff7b1247",
               "@type": "ProductSpecificationRef"
            },
            "relatedParty": [
               {
                  "id": "4175939453126010a795ddeeff7b127d",
                  "name": "John Smith",
                  "email": "abc2@example.com",
                  "phone": "32456768",
                  "@type": "RelatedParty",
                  "@referredType": "OrderLineItemContact"
               },
               {
                  "id": "c175939453126010a795ddeeff7b127c",
                  "name": "Joe Doe",
                  "email": "abc@example.com",
                  "phone": "1234567890",
                  "@type": "RelatedParty",
                  "@referredType": "OrderLineItemContact"
               }
            ]
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalId": "69017a0f536520103b6bddeeff7b127d",
            "internalVersion": "1"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI100",
               "relationshipType": "HasParent"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      },
      {
         "id": "POI100",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productSpecification": {
               "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
               "name": "SD-WAN Service Package",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
               "@type": "ProductSpecificationRef"
            }
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalId": "69017a0f536520103b6bddeeff7b127d",
            "internalVersion": "1"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI130",
               "relationshipType": "HasChild"
            },
            {
               "id": "POI120",
               "relationshipType": "HasChild"
            },
            {
               "id": "POI110",
               "relationshipType": "HasChild"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      },
      {
         "id": "POI120",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "actionReason": "adding service package OLI",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "USD",
                     "value": 20
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productCharacteristic": [
               {
                  "name": "CPE Type",
                  "valueType": "Choice",
                  "value": "Physical",
                  "previousValue": ""
               },
               {
                  "name": "WAN Optimization",
                  "valueType": "Choice",
                  "value": "Advance",
                  "previousValue": ""
               },
               {
                  "name": "Routing",
                  "valueType": "Choice",
                  "value": "Premium",
                  "previousValue": ""
               },
               {
                  "name": "CPE Model",
                  "valueType": "Choice",
                  "value": "ASR",
                  "previousValue": ""
               }
            ],
            "productSpecification": {
               "id": "39b627aa53702010cd6dddeeff7b1202",
               "name": "SD-WAN Edge Device",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "39b627aa53702010cd6dddeeff7b1202",
               "@type": "ProductSpecificationRef"
            }
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "69017a0f536520103b6bddeeff7b127d"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI100",
               "relationshipType": "HasParent"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      },
      {
         "id": "POI110",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "actionReason":"adding service package OLI",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "USD",
                     "value": 5
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productCharacteristic": [
               {
                  "name": "Tenancy",
                  "valueType": "Choice",
                  "value": "Base (10 site)",
                  "previousValue": ""
               }
            ],
            "productSpecification": {
               "id": "216663aa53702010cd6dddeeff7b12b5",
               "name": "SD-WAN Controller",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "216663aa53702010cd6dddeeff7b12b5",
               "@type": "ProductSpecificationRef"
            },
            "place": {
               "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
               "@type": "Place"
            }
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalId": "69017a0f536520103b6bddeeff7b127d",
            "internalVersion": "1"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI100",
               "relationshipType": "HasParent"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      }
   ],
   "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
   "state": "in_progress",
   "@type": "ProductOrder"
}
```

GET response with TMF 622 V3 parameters \(relatedParty, billingAccount and payment\)

```
{
  "id": "8d75939453126010a795ddeeff7b126a",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a",
  "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
  "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
  "requestedStartDate": "2020-05-03T08:13:59.000Z",
  "externalId": "PO-456",
  "orderCurrency": "USD",
  "channel": [
    {
      "id": "1",
      "name": "Agent Assist"
    }
  ],
  "note": [
    {
      "author": "System Administrator",
      "date": "2021-02-25T14:22:07.000Z",
      "text": "This is a TMF product order illustration no 2"
    },
    {
      "author": "System Administrator",
      "date": "2021-02-25T14:22:06.000Z",
      "text": "This is a TMF product order illustration"
    }
  ],
  "productOrderItem": [
    {
      "id": "POI130",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "actionReason": "adding service package OLI",
      "billingAccount": {
        "id": "sys_id_ba_security_789",
        "name": "Funco Intl - Security Services",
        "@type": "BillingAccountRef",
        "status": "Active",
        "active": true
      },
      "payment": {
        "id": "sys_id_payment_visa_001",
        "paymentMethod": "Credit Card",
        "paymentMethodType": "Visa",
        "paymentReferenceId": "REF-2024-SD-SECURITY"
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Security Type",
            "valueType": "Choice",
            "value": "Base",
            "previousValue": ""
          }
        ],
        "productSpecification": {
          "id": "a6514bd3534560102f18ddeeff7b1247",
          "name": "SD-WAN Security",
          "version": "v1",
          "internalVersion": "1",
          "internalId": "a6514bd3534560102f18ddeeff7b1247",
          "@type": "ProductSpecificationRef"
        },
        "relatedParty": [
          {
            "id": "4175939453126010a795ddeeff7b127d",
            "name": "John Smith",
            "email": "abc2@example.com",
            "phone": "32456768",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          },
          {
            "id": "c175939453126010a795ddeeff7b127c",
            "name": "Joe Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ]
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering",
        "version": "v1",
        "internalId": "69017a0f536520103b6bddeeff7b127d",
        "internalVersion": "1"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI100",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "billingAccount": {
        "id": "sys_id_ba_service_456",
        "name": "Funco Intl - Service Package",
        "@type": "BillingAccountRef",
        "status": "Active",
        "active": true
      },
      "payment": {
        "id": "sys_id_payment_ach_002",
        "paymentMethod": "Bank Transfer",
        "paymentMethodType": "ACH",
        "paymentReferenceId": "REF-2024-SD-SERVICE"
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productSpecification": {
          "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "name": "SD-WAN Service Package",
          "version": "v1",
          "internalVersion": "1",
          "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering",
        "version": "v1",
        "internalId": "69017a0f536520103b6bddeeff7b127d",
        "internalVersion": "1"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI130",
          "relationshipType": "HasChild"
        },
        {
          "id": "POI120",
          "relationshipType": "HasChild"
        },
        {
          "id": "POI110",
          "relationshipType": "HasChild"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI120",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "actionReason": "adding service package OLI",
      "billingAccount": {
        "id": "sys_id_ba_equipment_123",
        "name": "Funco Intl - Equipment Billing",
        "@type": "BillingAccountRef",
        "status": "Active",
        "active": true
      },
      "payment": {
        "id": "sys_id_payment_mastercard_003",
        "paymentMethod": "Credit Card",
        "paymentMethodType": "MasterCard",
        "paymentReferenceId": "REF-2024-SD-EQUIPMENT"
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "CPE Type",
            "valueType": "Choice",
            "value": "Physical",
            "previousValue": ""
          },
          {
            "name": "WAN Optimization",
            "valueType": "Choice",
            "value": "Advance",
            "previousValue": ""
          },
          {
            "name": "Routing",
            "valueType": "Choice",
            "value": "Premium",
            "previousValue": ""
          },
          {
            "name": "CPE Model",
            "valueType": "Choice",
            "value": "ASR",
            "previousValue": ""
          }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
          "version": "v1",
          "internalVersion": "1",
          "internalId": "39b627aa53702010cd6dddeeff7b1202",
          "@type": "ProductSpecificationRef"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering",
        "version": "v1",
        "internalVersion": "1",
        "internalId": "69017a0f536520103b6bddeeff7b127d"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI110",
      "ponr": "false",
      "quantity": 1,
      "action": "add",
      "actionReason": "adding service package OLI",
      "billingAccount": {
        "id": "sys_id_ba_controller_999",
        "name": "Funco Intl - Controller Services",
        "@type": "BillingAccountRef",
        "status": "Active",
        "active": true
      },
      "itemPrice": [
        {
          "priceType": "recurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "INR",
              "value": 0
            }
          }
        },
        {
          "priceType": "nonRecurring",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 5
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Tenancy",
            "valueType": "Choice",
            "value": "Base (10 site)",
            "previousValue": ""
          }
        ],
        "productSpecification": {
          "id": "216663aa53702010cd6dddeeff7b12b5",
          "name": "SD-WAN Controller",
          "version": "v1",
          "internalVersion": "1",
          "internalId": "216663aa53702010cd6dddeeff7b12b5",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering",
        "version": "v1",
        "internalId": "69017a0f536520103b6bddeeff7b127d",
        "internalVersion": "1"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "state": "in_progress",
      "version": "1",
      "@type": "ProductOrderItem"
    }
  ],
  "relatedParty": [
    {
      "role": "Contact",
      "@type": "Contact",
      "partyOrPartyRole": {
        "@type": "PartyRef",
        "id": "eaf68911c35420105252716b7d40ddde",
        "name": "Sally Thomas",
        "email": "sally.thomas@funcointl.com"
      }
    },
    {
      "role": "Account",
      "@type": "Account",
      "partyOrPartyRole": {
        "@type": "PartyRef",
        "id": "ffc68911c35420105252716b7d40dd55",
        "name": "Funco Intl"
      }
    },
    {
      "role": "Consumer",
      "@type": "Consumer",
      "partyOrPartyRole": {
        "@type": "PartyRef",
        "id": "59f16de1c3b67110ff00ed23a140dd9e",
        "name": "Funco External"
      }
    }
  ],
  "state": "in_progress",
  "@type": "ProductOrder"
}
```

### Reading Payment Information from Orders

When you retrieve an order using GET or LIST operations, the payment object is included in the order line item response only if a payment profile is actively linked. If an order line item \(OLI\) does not have a linked payment profile, the payment field is not included in the response. When the payment object is present, it contains all four fields \(id, paymentMethod, paymentMethodType, paymentReferenceId\) representing the complete profile details.

Example GET response:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "ba_456"
        },
        "payment": {
          "id": "sys_id_payment_profile_123",
          "paymentMethod": "Credit Card",
          "paymentMethodType": "Visa",
          "paymentReferenceId": "REF-2024-001"
        }
      }
    ]
  }
}
```

Example GET response without payment profile:

```
{
  "productOrder": {
    "id": "order_003",
    "orderItem": [
      {
        "id": "order_line_003",
        "product": {
          "id": "prod_789"
        },
        "billingAccount": {
          "id": "ba_999"
        }
      }
    ]
  }
}
```

### Reading Billing Account Information from Orders

When you retrieve an order using GET or LIST operations, the billingAccount field is included in the order line item response with the system ID reference and any available billing account details.

Example GET response with billing account reference:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_456",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

Example GET response with newly created billing account:

```
{
  "productOrder": {
    "id": "order_002",
    "orderItem": [
      {
        "id": "order_line_002",
        "product": {
          "id": "prod_456"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_789",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

## Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}

Updates the specified customer order.

### v3 updates for PATCH

-   v3 of the Product Order Open API supports a `changeType=nonProduct` parameter to update order and line item administrative details without triggering product change workflows or state transitions.

-   The `relatedParty` field also changed structure in v3:
    -   The V2 item shape \(`id`/`name`/`@referredType`/`@type`\) only supported referencing an existing Account, Consumer, or Contact record by ID.
    -   V3 introduces the `partyOrPartyRole` object in its place \(`role`/`@type`/`partyOrPartyRole`\) so the same field can support both reference and inline-creation patterns.

        On the POST endpoint, `partyOrPartyRole` can carry the attributes needed to create a new Account, Consumer, Contact, location, billing account, or payment record inline, rather than requiring it to already exist. PATCH accepts either item shape but, unlike POST, only supports the reference pattern. See the request body parameters table below for the full field-by-field breakdown of both shapes.


### relatedParty structure differences

The **relatedParty** field is present in both the deprecated V2 and the current V3 versions of the Product Order Open API, but the two versions use different structures for this field. Because [V2 is deprecated, not removed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf622_product_ordering-api.md), both structures may still be encountered depending on which endpoint version a caller is integrated with.

<table id="table_relatedparty_shape"><thead><tr><th>

Aspect

</th><th>

V2

</th><th>

V3

</th></tr></thead><tbody><tr><td>

Sample payload

</td><td>

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td><td>

```
"relatedParty": [
  {
    "role": "String",
    "@type": "String",
    "partyOrPartyRole": {Object}
  }
]
```

</td></tr><tr><td>

Party reference field

</td><td>

**relatedParty.id** — sys\_id or external\_id directly on the relatedParty item.

</td><td>

**relatedParty.partyOrPartyRole.id** — sys\_id or external\_id nested inside the **partyOrPartyRole** object.

</td></tr><tr><td>

Type annotation field

</td><td>

**relatedParty.@referredType** — possible values: `Consumer`, `Customer`, `CustomerContact`.

</td><td>

**relatedParty.@type** — possible values on PATCH: `Account`, `Consumer`, `Contact`.

</td></tr><tr><td>

Display name field

</td><td>

**relatedParty.name** — name of the account, customer, or consumer.

</td><td>

Not applicable on PATCH. \(**partyOrPartyRole.name** exists but applies only to POST inline creation.\)

</td></tr><tr><td>

Business role field

</td><td>

Not applicable. V2 has no equivalent field.

</td><td>

**relatedParty.role** — optional, not validated.

</td></tr><tr><td>

Record creation support

</td><td>

Not supported on PATCH.

</td><td>

Not supported on PATCH — only reference-existing-record patterns are accepted. \(POST does support inline creation; this topic covers PATCH only.\)

</td></tr><tr><td>

Not-found / invalid-reference behavior

</td><td>

Invalid Account: request rejected \(`Invalid payload: Customer Account does not exist`\). Invalid Consumer: request rejected \(`Invalid payload: Consumer does not exist`\). Invalid Contact, or a Contact not linked to the Account: request rejected \(`Customer contact is not related to the account`\).

</td><td>

Same three errors as V2, using the same message text.

</td></tr></tbody>
</table>### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order to update.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="tmf-622-patch-req" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td id="type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

changeType

</td><td>

Controls which fields in the PATCH request are processed. When provided, only non-product fields \(notes and contacts\) are updated and the order state remains unchanged without triggering product change workflows or state transitions. When absent, standard product-change behavior applies.Supported value: `nonProduct`

Only these fields are processed when `changeType=nonProduct`:

-   `note` \(order-level\)
-   `relatedParty` \(order-level\)
-   `productOrderItem[].id`
-   `productOrderItem[].relatedParty`
-   `productOrderItem[].note`

All other fields \(including product-related fields\) are silently ignored.

**Note:** When using this field, order state remains unchanged \(does NOT transition to revision\_received\). No inflight or revision flows are triggered, and changes are isolated to metadata fields only.

Data type: String

</td></tr><tr id="channel-row-tmf622"><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr id="channel_id-row-tmf622"><td>

channel.id

</td><td>

Required if the **channel** parameter is used. Unique identifier of the channel to use to sell the associated products. Data type: String

Table: In the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr id="channel_name-row-tmf622"><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: empty string

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-PATCH">

Date and time when the action must be performed on the order.This value must be the same as or later than the **committedDueDate** values for each order line item.

If the action for order line items is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr id="externalId-row-tmf622"><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Stored in: The external\_id field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

externalSystem

</td><td id="tmf622-response-externalSystem">

External system of the service order, appended with `TMF622`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF622`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the product order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order created for this request.Data type: String

</td></tr><tr id="note-row-tmf622"><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering. Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr id="note_text-row-tmf622"><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items. Updating the currency code of an existing order is not supported. Providing any value other than the currency code already associated with the order causes the update to be rejected.Data type: String

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order to be created. On successful request, the order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed. This value is the only result if the order is created asynchronously using the mode query parameter.Data type: String

</td></tr><tr id="productOrderItem-row-tmf622"><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "revisionOperation": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.@type

</td><td id="prodOrdItem_type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr id="productOrderItem_action-row-tmf622"><td>

productOrderItem.action

</td><td>

Required if the **productOrderItem** parameter is used. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: add

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="prodOrdItem_actionReason-response-tmf622">

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed. When you provide a billing.id that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields are ignored. The system uses only the ID to find and link the existing billing account. When you provide a billing.id that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(name, status, active\) are required for inline creation.Data type: Object

```
"billingAccount": { "id": "String",
                "@type": "BillingAccountRef", "name": "String", "status": "String",
                "active": Boolean }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be BillingAccountRef. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.Valid values:

-   true: Billing account is active
-   false: Billing account isn't active

Data type: Boolean

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.Examples: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.Data type: String

Examples: "Active", "Inactive", "Suspended"

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-PATCH">

Date and time when the action must be performed on the order line item.If the action for the item is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.Data type: String

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr id="externalProdInvId"><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-decsr">

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the sn\_ind\_tmt\_orm\_order\_line\_item table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr id="externalProdInv-PATCH"><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-descr-PATCH">

Conditional. If supplied, each entry requires **externalProductInventoryId**. List of external IDs to map to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr id="productOrderItem_id-row-tmf622"><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Sys\_id or external\_id of the order line item. Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

Default: empty string

</td></tr><tr id="itemPrice-row-tmf622"><td>

productOrderItem.itemPrice

</td><td id="itemPrice-entry-tmf622">

List that describes the price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr id="itemPrice_price-row-tmf622"><td>

productOrderItem.itemPrice.price

</td><td id="itemPrice_price-entry-tmf622">

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Default: empty string

</td></tr><tr id="itemPrice_price_taxIncludedAmt-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td id="itemPrice_price_taxIncludedAmt-entry-tmf622">

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="itemPrice_price_taxIncludedAmt_unit-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td id="itemPrice_price_taxIncludedAmt_unit-entry-tmf622">

Currency code in which the price is depicted. Data type: String

Stored in: The mrc or nrc field in the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr id="itemPrice_price_taxIncludedAmt_value-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td id="itemPrice_price_taxIncludedAmt_value-entry-tmf622">

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field in the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr id="itemPrice_priceType-row-tmf622"><td>

productOrderItem.itemPrice.priceType

</td><td id="itemPrice_priceType-entry-tmf622">

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr id="itemPrice_recurringChargePeriod-row-tmf622"><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td id="itemPrice_recurringChargePeriod-entry-tmf622">

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile and determines how the profile is processed. Reference an existing payment profile by passing payment.id, or pass full payment attributes to create payment profile inline. If the ID already exists, the API locates the matching payment profile and links it to the order line item. Any other payment fields are ignored. The system uses only the id to find and link the existing profile. If the ID doesn't already exist, a payment profile is created automatically and linked to the order line item's billing account. paymentMethod, paymentMethodType, paymentReferenceId are required to create the new profile.Data type: Object

```
"payment": { "id": "String", "paymentMethod": "String",
                "paymentMethodType": "String", "paymentReferenceId": "String" }
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Required. Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Conditional, required only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Data type: String

Examples: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Conditional, required only for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected paymentMethod. This field is ignored when referencing an existing profile.Data type: String

Examples: "Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Conditional, required only for profile creation. An external reference identifier for the payment profile. This is typically used for tracking, audit trails, and reconciliation between your order system and your payment processor. This field is ignored when referencing an existing profile.Data type: String

Examples: "REF-2024-001", "CARD-XXXX-5678"

</td></tr><tr id="product-row-tmf622"><td>

productOrderItem.product

</td><td>

Required if **productOrderItem.action** is change or delete. Description of the instance details of the product purchased by the customer. Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_type-row-tmf622"><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr id="product_id-row-tmf622"><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

Default: empty string

</td></tr><tr id="product_place-row-tmf622"><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_place_type-row-tmf622"><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr id="product_place_id-row-tmf622"><td>

productOrderItem.product.place.id

</td><td>

Required if the **productOrderItem.product.place** parameter is used. Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

Stored in: The location field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr id="prod_prodChar-row-tmf622"><td>

productOrderItem.product.productCharacteristic

</td><td>

List of characteristics of the associated product. Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr id="prod_prodChar_name-row-tmf622"><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr id="prod_prodChar_previousValue-row-tmf622"><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr id="prod_prodChar_value-row-tmf622"><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type:String

 **Note:** This value never changes format on this API. See the [Product Inventory Open API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/product-inventory-open-api.md) concept topic for a related system property.

</td></tr><tr id="product_productSpecification-row-tmf622"><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   When this system property is set to true \(default\), the product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   When this system property is set to false, if the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_productSpecification_type-row-tmf622"><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr id="product_productSpecification_id-row-tmf622"><td>

productOrderItem.product.productSpecification.id

</td><td>

Required if the **productOrderItem.product.productSpecification** parameter is used. Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalId

</td><td>

Initial version of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td id="tmf622-response-internalVersion">

Internal version of the product specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr id="product_productSpecification_name-row-tmf622"><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td id="tmf622-response-version">

External version of the product specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr id="product_relatedParty-row-tmf622"><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of contacts for line items. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "id": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr id="product_relatedParty_referredType-row-tmf622"><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr id="product_relatedParty_type-row-tmf622"><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr id="product_relatedParty_email-row-tmf622"><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr id="product_relatedParty_firstName-row-tmf622"><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr id="product_relatedParty_id-row-tmf622"><td>

productOrderItem.product.relatedParty.id

</td><td>

Required. Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

Stored in: The sys\_id field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr id="product_relatedParty_lastName-row-tmf622"><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr id="product_relatedParty_phone-row-tmf622"><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr id="productOffering-row-tmf622"><td>

productOrderItem.productOffering

</td><td>

Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOffering_id-row-tmf622"><td>

productOrderItem.productOffering.id

</td><td>

Required if the **productOrderItem.productOffering** parameter is used. Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalId

</td><td>

Initial version of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: StringTable: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr id="productOffering_name-row-tmf622"><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr id="productOrdItem_quantity-row-tmf622"><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order.

Default: null

</td></tr><tr id="productOrderItemRelationship-row-tmf622"><td>

productOrderItem.productOrderItemRelationship

</td><td>

Conditional. Item-level relationships. If supplied, each entry requires an **id** and **relationshipType**. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOrderItemRelationship_id-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required if the **productOrderItem.productOrderItemRelationship** parameter is used. Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Stored in: The parent\_line\_item field of thebsn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr id="productOrderItemRelationship_relType-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

productOrderItem.revisionOperation

</td><td>

Type of update to perform on the line item. If this value is empty, the existing line item is updated, or a new line item is added if it does not already exist. If this value is `cancel`, the line item is canceled.Data type: String

Default: empty string

</td></tr><tr id="relatedParty-row-tmf622"><td>

relatedParty

</td><td>

List of parties associated with the order. Contains at least one item identifying the Account or Consumer for the order. Both the V2 item shape and the V3 item shape are shown below. Data type: Array of Objects

V2 item shape:

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

 V3 item shape:

```
"relatedParty": [
  {
    "role": "String",
    "@type": "String",
    "partyOrPartyRole": {Object}
  }
]
```

</td></tr><tr id="relatedParty_referredType-row-tmf622"><td>

relatedParty.@referredType \(V2 only\)

</td><td>

Type of customer. Possible values:

-   **Consumer**
-   **Customer**
-   **CustomerContact**

Data type: String

</td></tr><tr id="relatedParty_id-row-tmf622"><td>

relatedParty.id \(V2 only\)

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table.

Data type: String

</td></tr><tr id="relatedParty_name-row-tmf622"><td>

relatedParty.name \(V2 only\)

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@type \(V2 only\)

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored.Data type: String

</td></tr><tr id="relatedParty_type-row-tmf622"><td>

relatedParty.@type \(V3 only\)

</td><td>

Required. Identifies the type of party the item represents. The system uses this value to determine which table to search when resolving the party. Possible values:

-   `Account`
-   `Consumer`
-   `Contact`

Data type: String

</td></tr><tr id="relatedParty_role-row-tmf622"><td>

relatedParty.role \(V3 only\)

</td><td>

Optional. Not validated against **relatedParty.@type** or any other field. Data type: String

</td></tr><tr id="relatedParty_partyOrPartyRole-row-tmf622"><td>

relatedParty.partyOrPartyRole \(V3 only\)

</td><td>

Required. Object identifying the existing party record to associate with the order. Data type: Object

```
"partyOrPartyRole": {
  "@type": "String",
  "id": "String"
}
```

 **Important:** On PATCH, only reference patterns are supported: the Account, Consumer, or Contact record identified by **partyOrPartyRole.id** must already exist. PATCH does not create Account, Consumer, Contact, location, billing account, or payment records, even if the referenced record does not exist.

</td></tr><tr id="relatedParty_partyOrPartyRole_type-row-tmf622"><td>

relatedParty.partyOrPartyRole.@type \(V3 only\)

</td><td>

Optional. Not validated. Data type: String

</td></tr><tr id="relatedParty_partyOrPartyRole_id-row-tmf622"><td>

relatedParty.partyOrPartyRole.id \(V3 only\)

</td><td>

Required. Sys\_id or external ID of the existing Account, Consumer, or Contact record to associate with the order. If **relatedParty.@type** is `Account` and no matching record exists, the request is rejected with `Invalid payload: Customer Account does not exist`.

 If **relatedParty.@type** is `Consumer` and no matching record exists, the request is rejected with `Invalid payload: Consumer does not exist`.

 If **relatedParty.@type** is `Contact` and no matching record exists, or the Contact is present but not linked to the Account also provided, the request is rejected with `Customer contact is not related to the account` \(same message text for both cases\).

 If both an Account and a Consumer are present in the same **relatedParty** set, the request is rejected with `Invalid payload: Both Account and Consumer cannot be present simultaneously`.

 If a Contact is present without an Account or Consumer also present, the request is rejected with `Invalid payload: Customer Account or Consumer is missing`.

 If **partyOrPartyRole.id** itself is missing, the request is rejected with `Invalid payload: partyOrPartyRole id is missing`.

Data type: String

Table: Account \[customer\_account\], Consumer \[csm\_consumer\], or Contact \[customer\_contact\]

</td></tr><tr id="relatedParty_partyOrPartyRole_patch_scope-row-tmf622"><td>

\(V3 only\)

</td><td>

**Note:** The following **partyOrPartyRole** attributes apply only to inline creation on the POST endpoint and have no effect on PATCH requests, because PATCH does not create records.

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber \(V3 only\)

</td><td>

Returned for Account party types. External reference number or identifier for the Account. It provides a business-facing account identifier that is distinct from the system-generated ID. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address \(V3 only\)

</td><td>

Returned for Location party types during inline creation. Street address of the location. Used only during inline creation; ignored for reference patterns.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city \(V3 only\)

</td><td>

Returned for Location party types during inline creation. City or municipality name for the location. Used only during inline creation; ignored for reference patterns.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country \(V3 only\)

</td><td>

Returned for Location party types during inline creation. Country where the location is physically situated or where the contact is based. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email \(V3 only\)

</td><td>

Returned for Contact party types during inline creation. Contact person's primary email address. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName \(V3 only\)

</td><td>

Returned for Contact party types during inline creation. Contact person's first name or given name. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName \(V3 only\)

</td><td>

Returned for Contact party types during inline creation. Contact person's last name or given name. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name \(V3 only\)

</td><td>

Returned for Account, Contact, and Location types during inline creation. Name of the account, contact, or location. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode \(V3 only\)

</td><td>

Returned for Location party types during inline creation. Postal code, ZIP code, or PIN code for the location. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status \(V3 only\)

</td><td>

Returned for Account party types during inline creation. Current status of the account. The valid values for the status field depend on how your instance is configured. Used only during inline creation; ignored for reference patterns.Common values:

-   `Active`
-   `Inactive`
-   `Suspended`
-   `Pending`
-   `Archived`
-   `Under Review`

Data type: String

</td></tr><tr id="requestedCompletionDate-row-tmf622"><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

Stored in: The expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer.Data type: String

</td></tr><tr id="requestedStartDate-row-tmf622"><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer. Data type: String

Stored in: The expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. For this endpoint, this value is always new.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table id="table_xfv_2vk_5rb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Resource modified successfully. Includes successful non-product changes via **changeType**.

</td></tr><tr><td>

201

</td><td>

Successful. If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record:

-   `The following Order Item characteristics does not exist: Review specification <**characteristic.name**> and correct the characteristic and characteristic option in the order line item prior to approving the order.`
-   `Order Item characteristic: <**characteristic.name**> with characteristic value: <**characteristic.value**>is invalid. Correct the characteristic values before approving the order.`

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   `Invalid payload: Request body missing` - Payload was not passed in the request body.
-   `Invalid payload: productOrderItem is missing` - Product order line item object or JSON is missing.
-   `Invalid payload: productOrderItem id is missing` - The **id** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem action is missing` - The **action** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem productOffering is missing` - The product offering object or JSON is missing from the product order line item in the payload.
-   `Invalid payload: productOffering id is missing` - The **id** parameter is missing in the product order line item of the product offering object in the payload.
-   `Invalid payload: Product offering does not exist` - The product offering in the product order line item is not valid.
-   `Invalid payload: productOrderItem product is missing` - The product object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: product productSpecification is missing` - The product specification object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: productSpecification id is missing` - The **id** parameter in the product order line item of the product specification object is missing from the payload.
-   `Invalid payload: Product specification does not exist` - The product specification in the product order line item is not valid.
-   `Invalid payload: Product Inventory does not exist` - In a change order \(action = change\), the quantity of an item is greater than what is in stock.
-   `Invalid payload: Product inventory ID is missing` - In a change order, the **product.id** is missing in the payload.
-   `Invalid payload: Sold Product is inactive` - In a change order, a product specified in the payload is inactive.
-   `Invalid payload: relatedParty is missing` - The related party object is missing from the payload.
-   `Customer Account or Consumer is missing` - The related party customer or consumer object is missing from the payload.
-   `Invalid payload: Consumer does not exist` - The specified related party consumer does not exist in the ServiceNow instance.
-   `Invalid payload: Customer Account does not exist` - The specified related party customer does not exist in the ServiceNow instance.
-   `Invalid payload: Order creation failed` - Not able to create the requested order.
-   `In-flight revision to order currency not supported` - The **orderCurrency** parameter can't be updated after the order is created.
-   `This order is yet to be created in customer order table. Please check in inbound queue for more details.` – The order ID provided is not in the customer order table.
-   `Patch request cannot be made as the order's fulfillment type is not 'deliver.` – The patch request was made on an order which has a fulfillment type other than deliver.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_c1v_xpk_5rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Unique identifier of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the product order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order updated for this request. Data type: String

</td></tr><tr><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering. Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem:" [
  {
    "action": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemReleationship": [Array],
    "quantity": Number,
    "state": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td id="d4196e5279">

Conditional. If supplied, each entry requires **externalProductInventoryId**. List of external IDs to map to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-resp-descr">

External ID mapped to the product inventory.Data type: String

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Sys\_id or external\_id of the order line item. Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

List that describes the price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount.value

</td><td>

Price of product, including any tax. Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Description of the instance details of the product purchased by the customer. Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

List of characteristics of the associated product. Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. Data type: Object

```
"productSpecification:" {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalId

</td><td>

Initial version of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification.Data type: String

Table: version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the product specification.Data type: String

Table: external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of contacts for line items. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "id": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.id

</td><td>

Required. Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Description of the product offering associated with the product. Data type: Object

```
"productOffering:" {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalId

</td><td>

Initial version of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, field version.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Conditional. Item-level relationships. If supplied, each entry requires an **id** and **relationshipType**. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

</td></tr><tr><td>

productOrderItem.state

</td><td>

Current state of the product order item.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Contains at least one item with customer account or consumer account information. Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table.

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.type

</td><td>

Type of customer. Possible values:

-   **Consumer**
-   **Customer**
-   **CustomerContact**

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### cURL request

This example updates the channel for a product order.

```
curl -X PATCH "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "channel": [
    {
      "id": "1",
      "name": "Agent Assist"
    }
  ]
}
```

Response body.

```
{
   "id": "8d75939453126010a795ddeeff7b126a",
   "href": "/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a",
   "expectedCompletionDate": "2021-05-02T08:13:59.000Z",
   "requestedCompletionDate": "2021-05-02T08:13:59.000Z",
   "requestedStartDate": "2020-05-03T08:13:59.000Z",
   "externalId": "PO-456",
   "orderCurrency": "USD",
   "channel": [
      {
         "id": "1",
         "name": "Agent Assist"
      }
   ],
   "note": [
      {
         "author": "System Administrator",
         "date": "2021-02-25T14:22:07.000Z",
         "text": "This is a TMF product order illustration no 2"
      },
      {
         "author": "System Administrator",
         "date": "2021-02-25T14:22:06.000Z",
         "text": "This is a TMF product order illustration"
      }
   ],
   "productOrderItem": [
      {
         "id": "POI130",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "actionReason": "adding service package OLI",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "USD",
                     "value": 20
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productCharacteristic": [
               {
                  "name": "Security Type",
                  "valueType": "Choice",
                  "value": "Base",
                  "previousValue": ""
               }
            ],
            "productSpecification": {
               "id": "a6514bd3534560102f18ddeeff7b1247",
               "name": "SD-WAN Security",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "a6514bd3534560102f18ddeeff7b1247",
               "@type": "ProductSpecificationRef"
            },
            "relatedParty": [
               {
                  "id": "4175939453126010a795ddeeff7b127d",
                  "name": "John Smith",
                  "email": "abc2@example.com",
                  "phone": "32456768",
                  "@type": "RelatedParty",
                  "@referredType": "OrderLineItemContact"
               },
               {
                  "id": "c175939453126010a795ddeeff7b127c",
                  "name": "Joe Doe",
                  "email": "abc@example.com",
                  "phone": "1234567890",
                  "@type": "RelatedParty",
                  "@referredType": "OrderLineItemContact"
               }
            ]
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalId": "69017a0f536520103b6bddeeff7b127d",
            "internalVersion": "1"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI100",
               "relationshipType": "HasParent"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      },
      {
         "id": "POI100",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productSpecification": {
               "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
               "name": "SD-WAN Service Package",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
               "@type": "ProductSpecificationRef"
            }
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalId": "69017a0f536520103b6bddeeff7b127d",
            "internalVersion": "1"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI130",
               "relationshipType": "HasChild"
            },
            {
               "id": "POI120",
               "relationshipType": "HasChild"
            },
            {
               "id": "POI110",
               "relationshipType": "HasChild"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      },
      {
         "id": "POI120",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "actionReason": "adding service package OLI",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "USD",
                     "value": 20
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productCharacteristic": [
               {
                  "name": "CPE Type",
                  "valueType": "Choice",
                  "value": "Physical",
                  "previousValue": ""
               },
               {
                  "name": "WAN Optimization",
                  "valueType": "Choice",
                  "value": "Advance",
                  "previousValue": ""
               },
               {
                  "name": "Routing",
                  "valueType": "Choice",
                  "value": "Premium",
                  "previousValue": ""
               },
               {
                  "name": "CPE Model",
                  "valueType": "Choice",
                  "value": "ASR",
                  "previousValue": ""
               }
            ],
            "productSpecification": {
               "id": "39b627aa53702010cd6dddeeff7b1202",
               "name": "SD-WAN Edge Device",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "39b627aa53702010cd6dddeeff7b1202",
               "@type": "ProductSpecificationRef"
            }
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "69017a0f536520103b6bddeeff7b127d"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI100",
               "relationshipType": "HasParent"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      },
      {
         "id": "POI110",
         "ponr": "false",
         "quantity": 1,
         "action": "add",
         "actionReason":"adding service package OLI",
         "itemPrice": [
            {
               "priceType": "recurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "INR",
                     "value": 0
                  }
               }
            },
            {
               "priceType": "nonRecurring",
               "price": {
                  "taxIncludedAmount": {
                     "unit": "USD",
                     "value": 5
                  }
               }
            }
         ],
         "product": {
            "@type": "Product",
            "productCharacteristic": [
               {
                  "name": "Tenancy",
                  "valueType": "Choice",
                  "value": "Base (10 site)",
                  "previousValue": ""
               }
            ],
            "productSpecification": {
               "id": "216663aa53702010cd6dddeeff7b12b5",
               "name": "SD-WAN Controller",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "216663aa53702010cd6dddeeff7b12b5",
               "@type": "ProductSpecificationRef"
            },
            "place": {
               "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
               "@type": "Place"
            }
         },
         "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "version": "v1",
            "internalId": "69017a0f536520103b6bddeeff7b127d",
            "internalVersion": "1"
         },
         "productOrderItemRelationship": [
            {
               "id": "POI100",
               "relationshipType": "HasParent"
            }
         ],
         "state": "in_progress",
         "version": "1",
         "@type": "ProductOrderItem"
      }
   ],
   "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
   "state": "in_progress",
   "@type": "ProductOrder"
}
```

### Update Order Notes Only

Add or update internal notes at the order level without triggering product change workflows.

```
curl -X PATCH "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "changeType": "nonProduct",
  "note": [
    {
      "text": "Billing contact updated per customer request."
    }
  ]
}
```

Response body:

```
HTTP 200 OK

{
  "id": "PO-0010047",
  "state": "in_progress",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/a2b3c4d5e6f7g8h9"
}
```

### Update Order-Level Contact \(V2 shape\)

Change the primary contact for the entire order \(e.g., billing contact, order coordinator\) without modifying product specifications, using the V2 **relatedParty** shape \(**id** + **@referredType**\).

```
curl -X PATCH "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "changeType": "nonProduct",
  "relatedParty": [
    {
      "id": "8xc9d0e1f2g3h4i5j",
      "@referredType": "CustomerContact"
    }
  ]
}
```

Response body:

```
HTTP 200 OK

{
  "id": "PO-0010047",
  "state": "in_progress",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/a2b3c4d5e6f7g8h9"
}
```

### Update Order-Level Contact \(V3 shape\)

The same update as the previous example, using the V3 **relatedParty** shape \(**@type** + **partyOrPartyRole.id**\). The referenced Contact record must already exist; PATCH does not create it.

```
curl -X PATCH "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "changeType": "nonProduct",
  "relatedParty": [
    {
      "@type": "Contact",
      "partyOrPartyRole": {
        "id": "8xc9d0e1f2g3h4i5j"
      }
    }
  ]
}
```

Response body:

```
HTTP 200 OK

{
  "id": "PO-0010047",
  "state": "in_progress",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/a2b3c4d5e6f7g8h9"
}
```

### Update Line Item Contact

Assign or change a technical contact for a specific product on the order \(e.g., the person responsible for a particular service line item\).

```
curl -X PATCH "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "changeType": "nonProduct",
  "productOrderItem": [
    {
      "id": "POI-0010001",
      "relatedParty": [
        {
          "id": "5m6n7o8p9q0r1s2t",
          "firstName": "Sally",
          "lastName": "Thomas",
          "email": "sally.thomas@example.com",
          "phone": "555-0100",
          "@referredType": "OrderLineItemContact"
        }
      ]
    }
  ]
}
```

Response body:

```
HTTP 200 OK

{
  "id": "PO-0010047",
  "state": "in_progress",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/a2b3c4d5e6f7g8h9"
}
```

### Update Line Item Note

Add scheduling notes, site survey details, or other administrative information to a specific line item without changing product specifications.

```
curl -X PATCH "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "changeType": "nonProduct",
  "productOrderItem": [
    {
      "id": "POI-0010001",
      "note": [
        {
          "text": "Site survey rescheduled by field team."
        }
      ]
    }
  ]
}
```

Response body:

```
HTTP 200 OK

{
  "id": "PO-0010047",
  "state": "in_progress",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/a2b3c4d5e6f7g8h9"
}
```

### Update Order Notes, Order Contact, and Line Item Details

Update multiple administrative fields across the order and line items in a single request \(for example, during order handoff or customer contact consolidation\).

```
curl -X PATCH "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "changeType": "nonProduct",
  "note": [
    {
      "text": "Order-level note added by CSR."
    }
  ],
  "relatedParty": [
    {
      "id": "8xc9d0e1f2g3h4i5j",
      "@referredType": "CustomerContact"
    }
  ],
  "productOrderItem": [
    {
      "id": "POI-0010001",
      "note": [
        {
          "text": "OLI-level note."
        }
      ],
      "relatedParty": [
        {
          "id": "5m6n7o8p9q0r1s2t",
          "firstName": "Sally",
          "lastName": "Thomas",
          "email": "sally.thomas@example.com",
          "phone": "555-0100",
          "@referredType": "OrderLineItemContact"
        }
      ]
    }
  ]
}
```

Response body:

```
HTTP 200 OK

{
  "id": "PO-0010047",
  "state": "in_progress",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/a2b3c4d5e6f7g8h9"
}
```

## Product Order Open API - PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}

Updates the specified customer order.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf622_product_ordering-api.md).

### URL format

Default URL: `/api/sn_ind_tmt_orm/productorder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the customer order to update.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="tmf-622-patch-req" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td id="type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always ProductOrder. This information is not stored.Data type: String

</td></tr><tr><td>

changeType

</td><td>

Controls which fields in the PATCH request are processed. When provided, only non-product fields \(notes and contacts\) are updated and the order state remains unchanged without triggering product change workflows or state transitions. When absent, standard product-change behavior applies.Supported value: `nonProduct`

Only these fields are processed when `changeType=nonProduct`:

-   `note` \(order-level\)
-   `relatedParty` \(order-level\)
-   `productOrderItem[].id`
-   `productOrderItem[].relatedParty`
-   `productOrderItem[].note`

All other fields \(including product-related fields\) are silently ignored.

**Note:** When using this field, order state remains unchanged \(does NOT transition to revision\_received\). No inflight or revision flows are triggered, and changes are isolated to metadata fields only.

Data type: String

</td></tr><tr id="channel-row-tmf622"><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products.Data type: Array of Objects

</td></tr><tr id="channel_id-row-tmf622"><td>

channel.id

</td><td>

Required if the **channel** parameter is used. Unique identifier of the channel to use to sell the associated products. Data type: String

Table: In the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

channel.id

</td><td>

Unique identifier of the channel to use to sell the associated products.Data type: String

</td></tr><tr id="channel_name-row-tmf622"><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: empty string

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products.Data type: String

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-PATCH">

Date and time when the action must be performed on the order.This value must be the same as or later than the **committedDueDate** values for each order line item.

If the action for order line items is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order. This value must be the same as or later than the committedDueDate values for each order line item.Data type: String

</td></tr><tr id="externalId-row-tmf622"><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Stored in: The external\_id field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number.Data type: String

</td></tr><tr><td>

externalSystem

</td><td id="tmf622-response-externalSystem">

External system of the service order, appended with `TMF622`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF622`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the product order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order created for this request.Data type: String

</td></tr><tr id="note-row-tmf622"><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering. Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering.Data type: Array of Objects`"note": [{ "text": "String" }]`

</td></tr><tr id="note_text-row-tmf622"><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering.Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items. Updating the currency code of an existing order is not supported. Providing any value other than the currency code already associated with the order causes the update to be rejected.Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order to be created. On successful request, the order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed. This value is the only result if the order is created asynchronously using the mode query parameter.Data type: String

</td></tr><tr id="productOrderItem-row-tmf622"><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "revisionOperation": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem

</td><td>

Required. Items associated with the product order and their associated action.Data type: Array of Objects

```
"productOrderItem": [{
                "action": "String", "billingAccount": {Object}, "id": "String",
                "payment": {Object}, "product": {Object}, "productOffering": {Object}, ...
                }]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td id="prodOrdItem_type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always ProductOrderItem. This information is not stored.Data type: String

</td></tr><tr id="productOrderItem_action-row-tmf622"><td>

productOrderItem.action

</td><td>

Required if the **productOrderItem** parameter is used. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: add

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table.Data type: String

Possible values: add, change, delete, no-change, resume, suspend

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="prodOrdItem_actionReason-response-tmf622">

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed. When you provide a billing.id that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields are ignored. The system uses only the ID to find and link the existing billing account. When you provide a billing.id that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(name, status, active\) are required for inline creation.Data type: Object

```
"billingAccount": { "id": "String",
                "@type": "BillingAccountRef", "name": "String", "status": "String",
                "active": Boolean }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be BillingAccountRef. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.Valid values:

-   true: Billing account is active
-   false: Billing account isn't active

Data type: Boolean

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.Examples: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.Data type: String

Examples: "Active", "Inactive", "Suspended"

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-PATCH">

Date and time when the action must be performed on the order line item.If the action for the item is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.Data type: String

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

Conditional. If supplied, each entry requires externalProductInventoryId. External IDs to map to the product inventories created for the order.Data type: Array of Objects```
"externalProductInventory": [{ "externalProductInventoryId":
                "String" }]
```

</td></tr><tr id="externalProdInvId"><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-decsr">

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the sn\_ind\_tmt\_orm\_order\_line\_item table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID mapped to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr id="externalProdInv-PATCH"><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-descr-PATCH">

Conditional. If supplied, each entry requires **externalProductInventoryId**. List of external IDs to map to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr id="productOrderItem_id-row-tmf622"><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Sys\_id or external\_id of the order line item. Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

Default: empty string

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item.Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.Maximum length: 40

</td></tr><tr id="itemPrice-row-tmf622"><td>

productOrderItem.itemPrice

</td><td id="itemPrice-entry-tmf622">

List that describes the price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product.```
Data type: Array of Objects
```

```
"itemPrice": [{ "price": {Object}, "priceType": "String",
                "recurringChargePeriod": "String" }]
```

</td></tr><tr id="itemPrice_price-row-tmf622"><td>

productOrderItem.itemPrice.price

</td><td id="itemPrice_price-entry-tmf622">

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product.Data type: Object

```
"price": { "taxIncludedAmount": {Object} }
```

</td></tr><tr id="itemPrice_price_taxIncludedAmt-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td id="itemPrice_price_taxIncludedAmt-entry-tmf622">

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax.Data type: Object

```
"taxIncludedAmount": { "unit": "String", "value":
                Number }
```

</td></tr><tr id="itemPrice_price_taxIncludedAmt_unit-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td id="itemPrice_price_taxIncludedAmt_unit-entry-tmf622">

Currency code in which the price is depicted. Data type: String

Stored in: The mrc or nrc field in the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed.Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr id="itemPrice_price_taxIncludedAmt_value-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td id="itemPrice_price_taxIncludedAmt_value-entry-tmf622">

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field in the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax.Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr id="itemPrice_priceType-row-tmf622"><td>

productOrderItem.itemPrice.priceType

</td><td id="itemPrice_priceType-entry-tmf622">

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring.Data type: String

</td></tr><tr id="itemPrice_recurringChargePeriod-row-tmf622"><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td id="itemPrice_recurringChargePeriod-entry-tmf622">

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as month.Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile and determines how the profile is processed. Reference an existing payment profile by passing payment.id, or pass full payment attributes to create payment profile inline. If the ID already exists, the API locates the matching payment profile and links it to the order line item. Any other payment fields are ignored. The system uses only the id to find and link the existing profile. If the ID doesn't already exist, a payment profile is created automatically and linked to the order line item's billing account. paymentMethod, paymentMethodType, paymentReferenceId are required to create the new profile.Data type: Object

```
"payment": { "id": "String", "paymentMethod": "String",
                "paymentMethodType": "String", "paymentReferenceId": "String" }
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Required. Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Conditional, required only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Data type: String

Examples: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Conditional, required only for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected paymentMethod. This field is ignored when referencing an existing profile.Data type: String

Examples: "Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Conditional, required only for profile creation. An external reference identifier for the payment profile. This is typically used for tracking, audit trails, and reconciliation between your order system and your payment processor. This field is ignored when referencing an existing profile.Data type: String

Examples: "REF-2024-001", "CARD-XXXX-5678"

</td></tr><tr id="product-row-tmf622"><td>

productOrderItem.product

</td><td>

Required if **productOrderItem.action** is change or delete. Description of the instance details of the product purchased by the customer. Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product

</td><td>

Required if productOrderItem.action is change or delete. Instance details of the product purchased by the customer.Data type: Object

```
"product": {
 "id": "String",
 "place": {Object},
 "productCharacteristic": [Array],
 "productSpecification": {Object},
 "relatedParty": [Array],
 "@type": "String"
}
```

</td></tr><tr id="product_type-row-tmf622"><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always Product. This information is not stored.Data type: String

</td></tr><tr id="product_id-row-tmf622"><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

Default: empty string

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Required if productOrderItem.action is change or delete. Unique identifier of the product sold.Data type: String

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr id="product_place-row-tmf622"><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product.Data type: Object

```
"place": { "id": "String", "@type": "String"
              }
```

</td></tr><tr id="product_place_type-row-tmf622"><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always Place. This information is not stored.Data type: String

</td></tr><tr id="product_place_id-row-tmf622"><td>

productOrderItem.product.place.id

</td><td>

Required if the **productOrderItem.product.place** parameter is used. Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

Stored in: The location field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record. When employing the change action on a product order item \(via the productOrderItem.action parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location.Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr id="prod_prodChar-row-tmf622"><td>

productOrderItem.product.productCharacteristic

</td><td>

List of characteristics of the associated product. Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product.Data type: Array of Objects

```
"productCharacteristic": [{ "name": "String",
                "previousValue": "String", "value": "String", "valueType": "String"
                }]
```

</td></tr><tr id="prod_prodChar_name-row-tmf622"><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr id="prod_prodChar_previousValue-row-tmf622"><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the productOrderItem.action parameter is other than add.Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr id="prod_prodChar_value-row-tmf622"><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product.Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Data type: String

Possible values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type:String

</td></tr><tr id="product_productSpecification-row-tmf622"><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   When this system property is set to true \(default\), the product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   When this system property is set to false, if the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Optional. Description of the product specification associated with the product.Data type: Object

```
"productSpecification": { "id":
                "String", "internalVersion": "String", "name": "String", "version":
                "String", "@type": "String" }
```

</td></tr><tr id="product_productSpecification_type-row-tmf622"><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always ProductSpecificationRef. This information is not stored.Data type: String

</td></tr><tr id="product_productSpecification_id-row-tmf622"><td>

productOrderItem.product.productSpecification.id

</td><td>

Required if the **productOrderItem.product.productSpecification** parameter is used. Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalId

</td><td>

Initial version of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td id="tmf622-response-internalVersion">

Internal version of the product specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Must match the value of version otherwise an error is thrown.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr id="product_productSpecification_name-row-tmf622"><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td id="tmf622-response-version">

External version of the product specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the product specification. Must match the value of internalVersion otherwise an error is thrown.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr id="product_relatedParty-row-tmf622"><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of contacts for line items. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "id": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of party roles linked to an OrderLineItemContact.Data type: Array of Objects

```
"relatedParty": [{ "email": "String", "firstName":
                "String", "lastName": "String", "phone": "String", "@referredType":
                "String", "@type": "String" }]
```

</td></tr><tr id="product_relatedParty_referredType-row-tmf622"><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer.Possible value: OrderLineItemContact

Data type: String

</td></tr><tr id="product_relatedParty_type-row-tmf622"><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always RelatedParty. This information is not stored.Data type: String

</td></tr><tr id="product_relatedParty_email-row-tmf622"><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact.Data type: StringStored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="product_relatedParty_firstName-row-tmf622"><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact.Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="product_relatedParty_id-row-tmf622"><td>

productOrderItem.product.relatedParty.id

</td><td>

Required. Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

Stored in: The sys\_id field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr id="product_relatedParty_lastName-row-tmf622"><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact.Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="product_relatedParty_phone-row-tmf622"><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact.Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

</td></tr><tr id="productOffering-row-tmf622"><td>

productOrderItem.productOffering

</td><td>

Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product.Data type: Object

```
"productOffering": { "id": "String",
                "internalVersion": "String", "name": "String", "version": "String"
                }
```

</td></tr><tr id="productOffering_id-row-tmf622"><td>

productOrderItem.productOffering.id

</td><td>

Required if the **productOrderItem.productOffering** parameter is used. Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: StringTable: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalId

</td><td>

Initial version of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: StringTable: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: StringTable: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr id="productOffering_name-row-tmf622"><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: StringTable: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: StringTable: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr id="productOrdItem_quantity-row-tmf622"><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order.

Default: null

</td></tr><tr id="productOrderItemRelationship-row-tmf622"><td>

productOrderItem.productOrderItemRelationship

</td><td>

Conditional. Item-level relationships. If supplied, each entry requires an **id** and **relationshipType**. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items.Data type: Array of Objects

```
"productOrderItemRelationship":
                [{ "id": "String", "relationshipType": "String" }]
```

</td></tr><tr id="productOrderItemRelationship_id-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required if the **productOrderItem.productOrderItemRelationship** parameter is used. Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Stored in: The parent\_line\_item field of thebsn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required. Same as the productOrderItem.id value. Used for parent/child relationship.Data type: StringStored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr id="productOrderItemRelationship_relType-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify relationship hierarchy.Data type: StringPossible values: HasChild, HasParent

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

productOrderItem.revisionOperation

</td><td>

Type of update to perform on the line item. If this value is empty, the existing line item is updated, or a new line item is added if it does not already exist. If this value is `cancel`, the line item is canceled.Data type: String

Default: empty string

</td></tr><tr id="relatedParty-row-tmf622"><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Contains at least one item with customer account or consumer account information. Data type: Array of Objects

```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array containing customer account or consumer account information.Data type: Array of Objects

```
"relatedParty": [
 {
   "role": "String",
   "@type": "String",
   "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr id="relatedParty_referredType-row-tmf622"><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   **Consumer**
-   **Customer**
-   **CustomerContact**

Data type: String

</td></tr><tr id="relatedParty_type-row-tmf622"><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Specifies what record type to search for when validating and linking the party. Must match the **role** field.Possible values:

-   `Account`
-   `Contact`
-   `Customer`
-   `Location`

Data type: String

</td></tr><tr id="relatedParty_id-row-tmf622"><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table.

Data type: String

</td></tr><tr id="relatedParty_name-row-tmf622"><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party. Attributes vary based on party type.-   For reference patterns, this object contains just the **@type** and **id** fields.
-   For creation patterns, this object also contains conditional attributes used to create the new record, if the **id** value does not match an existing record.

Data type: Object

```
"partyOrPartyRole": {
 "@type": "PartyRef",
 "id": "String"
}
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Indicates the type of reference being provided. Value must be set to `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Returned for Account party types. External reference number or identifier for the Account. It provides a business-facing account identifier that is distinct from the system-generated ID. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Returned for Location party types during inline creation. Street address of the location. Used only during inline creation; ignored for reference patterns.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Returned for Location party types during inline creation. City or municipality name for the location. Used only during inline creation; ignored for reference patterns.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Returned for Location party types during inline creation. Country where the location is physically situated or where the contact is based. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Returned for Contact party types during inline creation. Contact person's primary email address. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Returned for Contact party types during inline creation. Contact person's first name or given name. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id or external\_id of the party record to reference. The system searches for a record with either a matching system ID or matching External ID.-   For reference patterns with an existing record, only the id is used and all other provided fields are ignored.
-   For creation patterns when no matching record exists, the ID becomes the external ID of the newly created record, and other provided fields populate the new record's attributes.

Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[cmn\_location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Returned for Contact party types during inline creation. Contact person's last name or given name. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Returned for Account, Contact, and Location types during inline creation. Name of the account, contact, or location. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Returned for Location party types during inline creation. Postal code, ZIP code, or PIN code for the location. Used only during inline creation; ignored for reference patterns.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Returned for Account party types during inline creation. Current status of the account. The valid values for the status field depend on how your instance is configured. Used only during inline creation; ignored for reference patterns.Common values:

-   `Active`
-   `Inactive`
-   `Suspended`
-   `Pending`
-   `Archived`
-   `Under Review`

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the referenced party plays in the order context. Must match **relatedParty.@type** in the same object.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr id="requestedCompletionDate-row-tmf622"><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

Stored in: The expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer.Data type: String

</td></tr><tr id="requestedStartDate-row-tmf622"><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer. Data type: String

Stored in: The expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. For this endpoint, this value is always new.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table id="table_xfv_2vk_5rb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record:

-   `The following Order Item characteristics does not exist: Review specification <**characteristic.name**> and correct the characteristic and characteristic option in the order line item prior to approving the order.`
-   `Order Item characteristic: <**characteristic.name**> with characteristic value: <**characteristic.value**>is invalid. Correct the characteristic values before approving the order.`

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   `Invalid payload: Request body missing` - Payload was not passed in the request body.
-   `Invalid payload: productOrderItem is missing` - Product order line item object or JSON is missing.
-   `Invalid payload: productOrderItem id is missing` - The **id** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem action is missing` - The **action** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem productOffering is missing` - The product offering object or JSON is missing from the product order line item in the payload.
-   `Invalid payload: productOffering id is missing` - The **id** parameter is missing in the product order line item of the product offering object in the payload.
-   `Invalid payload: Product offering does not exist` - The product offering in the product order line item is not valid.
-   `Invalid payload: productOrderItem product is missing` - The product object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: product productSpecification is missing` - The product specification object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: productSpecification id is missing` - The **id** parameter in the product order line item of the product specification object is missing from the payload.
-   `Invalid payload: Product specification does not exist` - The product specification in the product order line item is not valid.
-   `Invalid payload: Product Inventory does not exist` - In a change order \(action = change\), the quantity of an item is greater than what is in stock.
-   `Invalid payload: Product inventory ID is missing` - In a change order, the **product.id** is missing in the payload.
-   `Invalid payload: Sold Product is inactive` - In a change order, a product specified in the payload is inactive.
-   `Invalid payload: relatedParty is missing` - The related party object is missing from the payload.
-   `Invalid payload: Customer Account or Consumer is missing` - The related party customer or consumer object is missing from the payload.
-   `Invalid payload: Consumer does not exist` - The specified related party consumer does not exist in the ServiceNow instance.
-   `Invalid payload: Customer Account does not exist` - The specified related party customer does not exist in the ServiceNow instance.
-   `Invalid payload: Order creation failed` - Not able to create the requested order.
-   `Invalid payload: This order is yet to be created in customer order table. Please check in inbound queue for more details.` - The patch request was made for an order that is not in the customer order table yet. The order is in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table waiting for the scheduler to pick the record to be processed.
-   `Invalid payload: Patch request cannot be made as the order's fulfillment type is not 'deliver'.` - The patch request was made for an order which has a fulfillment type other than**deliver**.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_c1v_xpk_5rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

 ```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Unique identifier of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order updated for this request. Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number.Data type: String

</td></tr><tr><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering. Data type: Array of Objects

 ```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array of Objects

 ```
"productOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
    "id": "String",
    "itemPrice": [Array],
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemReleationship": [Array],
    "quantity": Number,
    "state": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Sys\_id of the order line item. Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

Default: Blank string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

List that describes the price associated with the product. Data type: Array of Objects

 ```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

 ```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

 ```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount.value

</td><td>

Price of product, including any tax. Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Description of the instance details of the product purchased by the customer. Data type: Object

 ```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

 ```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

List of characteristics of the associated product. Data type: Array of Objects

 ```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. Data type: Object

 ```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the product specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the product specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of contacts for line items. Data type: Array of Objects

 ```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "id": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.id

</td><td>

Required. Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

 Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

 Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Description of the product offering associated with the product. Data type: Object

 ```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Conditional. Item-level relationships. If supplied, each entry requires an **id** and **relationshipType**. Data type: Array of Objects

 ```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

</td></tr><tr><td>

productOrderItem.state

</td><td>

Current state of the product order item.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Contains at least one item with customer account or consumer account information. Data type: Array of Objects

 ```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table.

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.type

</td><td>

Type of customer. Possible values:

-   **Consumer**
-   **Customer**
-   **CustomerContact**

 Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example updates the channel for a customer order.

```
curl -X PATCH "https://instance.servicenow.com/api/sn_ind_tmt_orm/productorder/6be0a925c3a220103e2e73ce3640ddfe" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "channel": [
    {
      "id": "1",
      "name": "Agent Assist"
    }
  ]
}
```

Response body.

```
{
    "requestedCompletionDate": "2021-05-02T08:13:59.506Z",
    "requestedStartDate": "2020-05-03T08:13:59.506Z",
    "externalId": "PO-456",
    "externalSystem": "Salesforce – TMF 641",
    "channel": [
        {
            "id": "1",
            "name": "Agent Assist"
        }
    ],
    "note": [
        {
            "text": "This is a TMF product order illustration"
        },
        {
            "text": "This is a TMF product order illustration no 2"
        }
    ],
    "productOrderItem": [
        {
            "id": "POI100",
            "quantity": 1,
            "action": "change",
            "actionReason":"adding service package OLI",
            "product": {
                "id": "fa6d13f45b5620102dff5e92dc81c77f",
                "@type": "Product",
                "productSpecification": {
                    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
                    "name": "SD-WAN Service Package",
                    "@type": "ProductSpecificationRef"
                },
                "place": {
                    "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                    "@type": "Place"
                }
            },
            "productOffering": {
                "id": "69017a0f536520103b6bddeeff7b127d",
                "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
                {
                    "id": "POI120",
                    "relationshipType": "HasChild"
                },
                {
                    "id": "POI130",
                    "relationshipType": "HasChild"
                }
            ],
            "@type": "ProductOrderItem",
            "state": "new"
        },
        {
            "id": "POI120",
            "quantity": 1,
            "action": "change",
            "actionReason":"adding service package OLI",
            "itemPrice": [
                {
                    "priceType": "recurring",
                    "recurringChargePeriod": "month",
                    "price": {
                        "taxIncludedAmount": {
                            "unit": "USD",
                            "value": 20
                        }
                    }
                }
            ],
            "product": {
                "id": "766d13f45b5620102dff5e92dc81c78a",
                "@type": "Product",
                "productCharacteristic": [
                    {
                        "name": "WAN Optimization"
                        "valueType": "Choice",
                        "value": "Base",
                        "previousValue": "Advance"
                    }
                ],
                "productSpecification": {
                    "id": "39b627aa53702010cd6dddeeff7b1202",
                    "name": "SD-WAN Edge Device",
                    "@type": "ProductSpecificationRef",
                    "externalVersion": "1",
                    "@version": "v1"
                },
                "relatedParty": [
                    {
                        "id": "51670151c35420105252716b7d40ddfe",
                        "firstName": "Joe",
                        "lastName": "Doe",
                        "email": "abc@example.com",
                        "phone": "1234567890",
                        "@type": "RelatedParty",
                        "@referredType": "OrderLineItemContact"
                    }
                ],
                "place": {
                    "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                    "@type": "Place"
                }
            },
            "productOffering": {
                "id": "69017a0f536520103b6bddeeff7b127d",
                "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
                {
                    "id": "POI100",
                    "relationshipType": "HasParent"
                }
            ],
            "@type": "ProductOrderItem",
            "state": "new"
        },
        {
            "id": "POI130",
            "quantity": 1,
            "action": "add",
            "actionReason":"adding service package OLI",
            "itemPrice": [
                {
                    "priceType": "recurring",
                    "recurringChargePeriod": "month",
                    "price": {
                        "taxIncludedAmount": {
                            "unit": "USD",
                            "value": 20
                        }
                    }
                }
            ],
            "product": {
                "@type": "Product",
                "productCharacteristic": [
                    {
                        "name": "Security Type",
                        "valueType": "Choice",
                        "value": "Base",
                        "previousValue": "Advance"
                    }
                ],
                "productSpecification": {
                    "id": "a6514bd3534560102f18ddeeff7b1247",
                    "name": "SD-WAN Security",
                    "@type": "ProductSpecificationRef"
                    "externalVersion": "1",
                    "@version": "v1"
                },
                "relatedParty": [
                    {
                        "id": "51670151c35420105252716b7d40ddfe",
                        "firstName": "Joe",
                        "lastName": "Doe",
                        "email": "abc@example.com",
                        "phone": "1234567890",
                        "@type": "RelatedParty",
                        "@referredType": "OrderLineItemContact"
                    }
                ],
                "place": {
                    "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                    "@type": "Place"
                }
            },
            "productOffering": {
                "id": "69017a0f536520103b6bddeeff7b127d",
                "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
                {
                    "id": "POI100",
                    "relationshipType": "HasParent"
                }
            ],
            "@type": "ProductOrderItem",
            "state": "new"
        }
    ],
    "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
    "@type": "ProductOrder",
    "id": "6be0a925c3a220103e2e73ce3640ddfe",
    "state": "in_progress"
}
```

## Product Order Open API - POST /sn\_ind\_tmt\_orm/cancelproductorder

Cancels the specified customer order.

### URL format

Default URL: `/api/sn_ind_tmt_orm/cancelproductorder`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cancellationReason

</td><td>

Reason for cancellation.Data type: String

 Default: Blank string

</td></tr><tr><td>

productOrder

</td><td>

Contains data about the product order.Data type: Object

 ```
"productOrder": {
  "id": "String",
  "href": "String",
  "@referredType": "String"
}
```

</td></tr><tr><td>

productOrder.id

</td><td>

Required. Sys\_id of the customer order to cancel.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr><td>

productOrder.href

</td><td>

URL of the customer order to cancel.Data type: String

Default: Blank string

</td></tr><tr><td>

productOrder.@referredType

</td><td>

Value for this parameter should be `ProductOrder`.Data type: String

Default: Blank string

</td></tr><tr><td>

requestedCancellationDate

</td><td>

Date to cancel the order.Data type: String

Default: Blank string

</td></tr><tr><td>

@type

</td><td>

Value for this parameter should be `CancelProductOrder`.Data type: String

Default: Blank string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;.
-   Invalid order ID.
-   Invalid order ID: `This order is yet to be created in customer order table`. The cancel request was made for an order that has not been created yet. The order is in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table waiting for the scheduler to pick up the record.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cancellationReason

</td><td>

Reason for cancellation.Data type: String

</td></tr><tr><td>

href

</td><td>

URL of the cancelled order.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the cancelled order.Data type: String

</td></tr><tr><td>

productOrder

</td><td>

Data about the product order.Data type: Object

```
"productOrder": {
  "id": "String",
  "href": "String",
  "@referredType": "String"
}
```

</td></tr><tr><td>

productOrder.id

</td><td>

Sys\_id of the cancelled order.Data type: String

</td></tr><tr><td>

productOrder.href

</td><td>

URL of the cancelled order.Data type: String

</td></tr><tr><td>

productOrder.@referredType

</td><td>

Value for this parameter is `ProductOrder`.Data type: String

</td></tr><tr><td>

productOrder.@referredType

</td><td>

Value for this parameter is `ProductOrderRef`.Data type: String

</td></tr><tr><td>

requestedCancellationDate

</td><td>

Date to cancel the order.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the cancellation. If the cancellation request was successfully processed \(201 status code\), the value for this parameter is `done`.Data type: String

</td></tr><tr><td>

@type

</td><td>

Value for this parameter is `CancelProductOrder`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example cancels a customer order.

```
curl -X POST "https://instance.servicenow.com/api/sn_ind_tmt_orm/cancelproductorder" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
    "cancellationReason": "Duplicate order",
    "requestedCancellationDate": "2019-04-30T12:56:21.931Z",
    "productOrder": {
        "id": "163ee2805358811032a4ddeeff7b122d",
        "href": "https://instance.servicenow.com/productOrderingManagement/v4/productOrder/64a9607feb45301032a442871352285b",
        "@referredType": "ProductOrder"
    },
    "@type": "CancelProductorder"
}
```

```
{
    "id": "163ee2805358811032a4ddeeff7b122d",
    "href": "https://instance.servicenow.com/productOrderingManagement/v4/productOrder/64a9607feb45301032a442871352285b",
    "cancellationReason": "Duplicate order",
    "requestedCancellationDate": "2019-04-30T12:56:21.931Z",
    "@type": "CancelProductorder",
    "productOrder": {
        "id": "163ee2805358811032a4ddeeff7b122d",
        "href": "https://instance.servicenow.com/productOrderingManagement/v4/productOrder/64a9607feb45301032a442871352285b",
        "@referredType": "ProductOrder"
    },
    "state": "done"
}
```

## Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder

Creates the specified customer order and customer order line items.

Once processed, records are created in the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]
-   Order Line Related Items \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

### Version 3.0 updates

The Product Order POST endpoint now supports billing accounts and payment profiles at the order line item \(OLI\) level, and inline creation of related party entities within order requests. v3.0 contains the following features:

1.  The system property, `sn_ind_tmt_orm.disableCharValueValidation`, indicates how to control characteristic value validation behavior for choice-type characteristics. The property isn't shipped by default and must be added manually.

    Behavior when set to:

    -   true: Validation is inactive \(disabled\) and `characteristic_option_value` is set directly from the request payload without generating work notes.
    -   false: \(Default\) Validates characteristic values against allowed choices and adds a work note to the record for any invalid value.
2.  Related party entities: Previously in v1 and v2, all related parties were pre-created and referenced by a system ID \(**relatedParty.partyOrPartyRole**\). In v3, you can now pass entity data in the **relatedParty** array to create new parties or continue using the reference pattern to link to existing entity IDs. Inline creation allows you to create new entities in a single POST request and improve order processing time.

    When referencing or creating a new entity in a product order, note that:

    -   **@type** is now required in all requests.
    -   Pair **id** with **@type** when referencing existing entities.
    -   Pass entity properties, like **name**, **firstName**, **lastName**, when creating new entities.
    See the **relatedParty.@type**parameter description for more information.

3.  Billing accounts: TMF 622 Product Order API V3 now supports billing account associations at the order line item \(**productOrderItem**\) level. When you place a product order, you can associate a billing account with each line item by either referencing an existing billing account or providing billing account details that the system will create as a new record before persisting the order. This functionality streamlines order workflows by enabling automatic billing account creation and linking during the order placement process. Billing accounts are created before the order is persisted, ensuring data consistency and proper linkage to both the order line item and the associated Account party.

    When referencing or creating a billing account in an order item, note that:

    -   **billingAccount.id** is required in all requests.
    -   Pass entity properties, like **name**, **@type**, **status**, **active** when creating new entities.
    See the **productOrderItem.billingAccount** parameter description for more information.

4.  The TMF 622 Product Order API V3 now supports payment profiles at the order line item \(OLI\) level. When you place a product order, you can associate a payment profile with one or more line items by either referencing an existing profile or creating a new one inline during the order request. The system automatically links the payment profile to the order line item's billing account. This functionality streamlines payment workflows by allowing payment method details to be captured and managed as part of the core order data. Payment information is returned in GET and LIST responses when an active profile is linked to the OLI. If no profile is linked, the payment field is omitted from the response.

    When referencing or creating a payment profile in an order item, note that:

    -   **payment.id** is required in all requests.
    -   Pass entity properties, like **paymentMethod**,**paymentMethodType**, and **paymentReferenceId**, when creating new entities.
    See the **productOrderItem.payment** parameter description for more information.


### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mode

</td><td>

Enables asynchronous order processing.​ That is, the order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table to be created. If not included, the order is processed synchronously.Valid value: async

Data type: String

</td></tr></tbody>
</table><table id="tmf622-table" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: empty string

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-entry">

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

 Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Stored in: The external\_id field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product order, appended with `TMF622`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF622`.

Data Type: String

</td></tr><tr id="productOrder-href-request"><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: empty string

</td></tr><tr><td>

note

</td><td>

Additional notes made by the customer when ordering. Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

note.text

</td><td>

Required. Additional notes/comments made by the customer while ordering. Data type: String

Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

orderCurrency

</td><td>

Required. Currency code for the order and order line items. The currency must be the same for all elements of the order and order line items, otherwise an error is returned and the order isn't created. Once an order is created, its currency code can't be changed. Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Required. Items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="productOrder-addReason-request">

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required when **productOrderItem.payment** is provided. Identifies the billing account and determines how the account is processed.-   When you provide a **billing.id** that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields you include \(**name**, **status**, **active**\) are ignored. The system uses only the ID to find and link the existing billing account.
-   When you provide a **billing.id** that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(**name**, **status**, **active**\) are required.

Data type: Object

Example reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Example creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

 Default: If not provided during creation, the system uses the default active value configured in your instance

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.

Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.

Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-entry">

Optional. Date and time when the action must be performed on the order line item.

Data type: String

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProductInventoryId-desc">

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr id="externalProductInventory-GET-request"><td>

productOrderItem.externalProductInventory

</td><td id="externalProductInventory-GET-desc-request">

Conditional. If supplied, each entry requires **externalProductInventoryId**. External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Maximum length: 40

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed. Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile and determines how the profile is processed. Reference an existing payment profile by passing **payment.id**, or pass full payment attributes to create payment profile inline.

-   If the ID already exists, the API locates the matching payment profile and links it to the order line item. Any other payment fields you include \(**paymentMethod**, **paymentMethodType**, **paymentReferenceId**\) are ignored. The system uses only the id to find and link the existing profile.
-   If the ID doesn't already exist, a payment profile is created automatically and linked to the order line item's billing account. **paymentMethod**, **paymentMethodType**, **paymentReferenceId** are required to create the new profile.

Data type: Object

Reference structure:

```
"payment": {
  "id": "String"
}
```

Creation structure:

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

See the 'Examples' section for POST requests demonstrating both reference and creation patterns.

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Required. Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Conditional, required only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Conditional, required only for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected **paymentMethod**. This field is ignored when referencing an existing profile.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Conditional, required only for profile creation. An external reference identifier for the payment profile. This is typically used for tracking, audit trails, and reconciliation between your order system and your payment processor. This field is ignored when referencing an existing profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Required if **productOrderItem.action** is change or delete. Instance details of the product purchased by the customer. Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Data type: String

Default: empty string

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location.

Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product. Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr id="tmf-prod-order_prodChar.valueType"><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Optional. Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   When this system property is set to true \(default\), the product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   When this system property is set to false, if the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an OrderLineItemContact. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required. Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

relatedParty

</td><td>

Array that contains one or more party objects. Each object in this array represents a party \(Account, Contact, or Location\) that should be associated with the order. The **relatedParty** array is optional at the order level, but if you provide party associations, each entry in the array must follow the required structure and validation rules.

Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Required. Specifies what record type to search for when validating and linking the party. Must match the **role** field.When you provide an @type of "Account", the system knows to search the Account table for the matching record. When you provide an @type of "Contact", the system knows to search the Contact table. This field ensures that the API searches the correct record type and applies the correct validation and linking logic.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party. Reference an existing party by passing **payment.id**, or pass full party attributes to create a new party record inline.-   If the ID already exists, the API locates the matching party and links it to the order line item. For reference patterns, this object contains just the **@type** and **id** fields. Any other payment fields are ignored. The system uses only the ID to find and link the existing party.
-   If the ID doesn't already exist, an Account, Contact, or Location party is created automatically and linked to the order line item. Conditional attributes like **name**, **email**, **address** are required to create the new profile. Conditional attributes vary on the **@type** value.

Data type: Object

Reference pattern:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String"
}
```

Account creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "accountNumber": "String",
  "status": "String"
}
```

Contact creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "firstName": "String",
  "lastName": "String",
  "email": "String"
 }
```

Location creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "name": "String",
  "address": "String",
  "city": "String",
  "postalCode": "String",
  "country": "String"
 }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Required. Indicates the type of reference being provided. Value must be set to `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Required for Account party types. External reference number or identifier for the Account. It provides a business-facing account identifier that is distinct from the system-generated ID.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Required for Location party types. Street address of the location.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Required for Location party types. City or municipality name for the location.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Required for Location party types. Country where the location is physically situated or where the contact is based.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Required for Contact party types. Contact person's primary email address.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Required for Contact party types. Contact person's first name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Required. Sys\_id or external\_id of the party record to reference. The system searches for a record with either a matching system ID or matching External ID.For reference patterns with an existing record, only the id is used and all other provided fields are ignored. For creation patterns when no matching record exists, the ID becomes the external ID of the newly created record, and other provided fields populate the new record's attributes.

Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Required for Contact party types. Contact person's last name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Required for Account, Contact, and Location types. Name of the account, contact, or location. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Required for Location party types. Postal code, ZIP code, or PIN code for the location.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Required for Account party types. Current status of the account. The valid values for the status field depend on how your instance is configured.Common status values include:

-   `Active`: Account is in normal operation
-   `Inactive`: Account is not currently conducting business
-   `Suspended`: Account is temporarily restricted
-   `Pending`: Account is awaiting activation
-   `Archived`: Historical accounts
-   `Under Review`: Account is being evaluated

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Required. Business role that the referenced party plays in the order context. Must match **relatedParty.@type** in the same object.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

Stored in: The expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Default: empty string

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Stored in: The expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Default: empty string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record:

-   `The following Order Item characteristics does not exist: Review specification <**characteristic.name**> and correct the characteristic and characteristic option in the order line item prior to approving the order.`
-   `Order Item characteristic: <**characteristic.name**> with characteristic value: <**characteristic.value**>is invalid. Correct the characteristic values before approving the order.`

</td></tr><tr><td>

202

</td><td>

Accepted. Successful request for an order in asynchronous mode. That is, the request was made with the **mode** parameter set to `async` and the record is scheduled to be processed in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   `Invalid payload: Request body missing` - Payload was not passed in the request body.
-   `Invalid payload: productOrderItem is missing` - Product order line item object or JSON is missing.
-   `Invalid payload: productOrderItem id is missing` - The **id** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem action is missing` - The **action** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem productOffering is missing` - The product offering object or JSON is missing from the product order line item in the payload.
-   `Invalid payload: productOffering id is missing` - The **id** parameter is missing in the product order line item of the product offering object in the payload.
-   `Invalid payload: Product offering does not exist` - The product offering in the product order line item is not valid.
-   `Invalid payload: productOrderItem product is missing` - The product object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: product productSpecification is missing` - The product specification object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: productSpecification id is missing` - The **id** parameter in the product order line item of the product specification object is missing from the payload.
-   `Invalid payload: Product specification does not exist` - The product specification in the product order line item is not valid.
-   `Invalid payload: Product Inventory does not exist` - In a change order \(action = change\), the quantity of an item is greater than what is in stock.
-   `Invalid payload: Product inventory ID is missing` - In change order, the **product.id** is missing in the payload.
-   `Invalid payload: Sold Product is inactive` - In a change order, a product specified in the payload is inactive.
-   `Invalid payload: relatedParty is missing` - The related party object is missing from the payload.
-   `Invalid payload: Customer Account or Consumer is missing` - The related party customer or consumer object is missing from the payload.
-   `Invalid payload: Consumer does not exist` - The specified related party consumer does not exist in the ServiceNow instance.
-   `Invalid payload: Customer Account does not exist` - The specified related party customer does not exist in the ServiceNow instance.
-   `Invalid payload: Order creation failed` - Not able to create the requested order.
-   `Invalid payload: orderCurrency is required` - The **orderCurrency** parameter is missing from the payload.
-   `Inactive Currency Code: <currency>` - The provided currency is inactive in the ServiceNow instance.
-   `One or more line items has a different currency code than the order currency` - All line items do not have the same currency code as the order currency.
-   `In-flight revision to order currency not supported` - The **orderCurrency** parameter can't be updated after the order is created.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="POST-GET-response-table" class="rest_api_response_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products.Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products.Data type: String

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products.Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.Stored in: committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number. This value is determined by an external system. Stored in: external\_id field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system identifier that originated the order request, appended with `TMF622`. Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

note

</td><td>

Additional notes made by the customer when ordering. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering.Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

orderDate

</td><td>

Date and time when the order was created.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

</td></tr><tr><td>

orderId

</td><td>

Sys\_id of the order.Stored in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed.

Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed.-   When an existing billing account ID is passed, the API returns just the matching account's sys\_id and type.
-   When a billing account ID is passed that doesn't match an existing record, the API creates a new billing account with the provided ID as the external\_id. The object includes conditional attributes associated with the new record.

Data type: Object

Example reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Example creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

 Default: If not provided during creation, the system uses the default active value configured in your instance

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.

Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.

Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Optional. Date and time when the action must be performed on the order line item.

Data type: String

 Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

Conditional. If supplied, each entry requires **externalProductInventoryId**. External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Maximum length: 40

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed. Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile. -   If the passed profile ID already exists, the API returns just the matching payment profile's sys\_Id.
-   If the passed ID doesn't already exist, the API returns the new payment profile's sys\_id and associated attributes.

Data type: Object

Reference structure:

```
"payment": {
  "id": "String"
}
```

Creation structure:

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

See the 'Examples' section for POST requests demonstrating both reference and creation patterns.

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned only for profile creation. A choice field representing the specific payment method type.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned only for profile creation. An external reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Data type: String

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record.Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product.Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Accepted values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   true: Product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   false: If the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an OrderLineItemContact. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order containing customer account or consumer account information. Supports reference and inline creation patterns \(Account, Contact, Location\). Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

realtedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   Account
-   Contact
-   Customer
-   Location

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Record type of the party. Matches the **relatedParty.role** value.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party.-   If the passed ID already exists, the API returns just the **@type** and **id** fields of the matching party.
-   If the passed ID doesn't already exist, the API returns a the new Account, Contact, or Location ID with its conditional attributes, which vary based on the **@type** value.

Data type: Object

Reference pattern:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String"
}
```

Account creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "accountNumber": "String",
  "status": "String"
}
```

Contact creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "firstName": "String",
  "lastName": "String",
  "email": "String"
 }
```

Location creation:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "name": "String",
  "address": "String",
  "city": "String",
  "postalCode": "String",
  "country": "String"
 }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Indicates the type of reference being provided. Value is always `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Returned for Account party types. External reference number or identifier for the Account.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Returned for Location party types. Street address of the location.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Returned for Location party types. City or municipality name for the location.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Returned for Location party types. Country where the location is physically situated or where the contact is based.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Returned for Contact party types. Contact person's primary email address.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Returned for Contact party types. Contact person's first name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Sys\_id or external\_id of the party record.Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Returned for Contact party types. Contact person's last name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Returned for Account, Contact, and Location types. Name of the account, contact, or location. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Required for Location party types. Postal code, ZIP code, or PIN code for the location.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Returned for Account party types. Current status of the account. Possible values for the status field depend on how your instance is configured.Common values include:

-   `Active`: Account is in normal operation
-   `Inactive`: Account is not currently conducting business
-   `Suspended`: Account is temporarily restricted
-   `Pending`: Account is awaiting activation
-   `Archived`: Historical accounts
-   `Under Review`: Account is being evaluated

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Business role that the referenced party plays in the order context. Matches the **relatedParty.@type** value.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

state

</td><td>

Current state of the order.Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Items associated with the product order and their associated action.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action carried out on the product.Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

Description of the reason for the order line item.Data type: String

Stored in: action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Identifies the billing account and determines how the account is processed.-   When you provide a **billing.id** that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields you include \(**name**, **status**, **active**\) are ignored. The system uses only the ID to find and link the existing billing account.
-   When you provide a **billing.id** that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(**name**, **status**, **active**\) are required.

Data type: Object

Reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Returned for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Returned only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Returned for account creation. Display name of the billing account.Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Returned for account creation. The status of the billing account. Possible values depend on your instance configuration. Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.Data type: String

Format: ISO 8601 \(Example: 2021-05-02T08:13:59.506Z\)

Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td>

External IDs which map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Stored in: sn\_ind\_tmt\_orm\_order

Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed.Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Details about the payment profile.Data type: Object

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Returned for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Returned for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected **paymentMethod**.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Returned for profile creation. External reference identifier for the payment profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Instance details of the product purchased by the customer.Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`.Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Returned if **productOrderItem.action** is `change` or `delete`. Unique identifier of the product sold. Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`.Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record. Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product. Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   `Array.Date`
-   `Array.Datetime`
-   `Array.Decimal`
-   `Array.Integer`
-   `Array.Object`
-   `Array.Single Line Test`
-   `check box`
-   `Choice`
-   `Date,Address`
-   `Email`
-   `Integer,Date/time`
-   `Object`
-   `Single Line Text`
-   `Yes/No`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Specification details associated with the product. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Matches the value of **version**.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Matches the value of **internalVersion**.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an Order Line Item Contact. Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: `OrderLineItemContact`

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`.Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact.Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact.Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Details of the product offering associated with the product.Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Same as the **productOrderItem.id** value. Used for parent/child relationship Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

</td></tr></tbody>
</table>### Processing asynchronously

This example shows how to use the **mode** query parameter to create an order asynchronously. The order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be created.

```
curl -X POST 'https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder?mode=async' \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d '{
  "requestedCompletionDate": "2021-05-02T08:13:59.506Z",
  "requestedStartDate": "2020-05-03T08:13:59.506Z",
  "orderDate": "2020-05-03T08:13:59.506Z",
  "externalId": "PO-4ddd56",
  "orderCurrency": "USD",
  "note": [
    {
      "id": "1",
      "author": "Jean Pontus",
      "date": "2019-04-30T08:13:59.509Z",
      "text": "This is a TMF product order illustration"
    },
    {
      "id": "2",
      "author": "Jean Pontus1",
      "date": "2019-04-30T08:13:59.509Z",
      "text": "This is a TMF product order illustration no 2"
    }
  ],
  "productOrderItem": [
    {
      "id": "100",
      "quantity": 1,
      "action": "add",
      "actionReason":"adding service package OLI",
      "product": {
        "isBundle": false,
        "@type": "Product",
        "productSpecification": {
          "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "name": "SD-WAN Service Package",
          "@type": "ProductSpecificationRef"
        },
        "relatedParty": [
          {
            "firstName": "John",
            "lastName": "Smith",
            "email": "abc2@example.com",
            "phone": "32456768",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "productRelationship": [
          {
            "id": "be6d13f45b5620102dff5e92dc81c781",
            "relationshipType": "Requires"
          }
        ]
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "110",
          "relationshipType": "HasChild"
        },
        {
          "id": "120",
          "relationshipType": "HasChild"
        },
        {
          "id": "130",
          "relationshipType": "HasChild"
        }
      ],
      "@type": "ProductOrderItem"
    },
    {
      "id": "110",
      "quantity": 1,
      "action": "add",
      "itemPrice": [
        {
          "description": "Access Fee",
          "name": "Access Fee",
          "priceType": "nonRecurring",
          "price": {
            "taxRate": 0,
            "dutyFreeAmount": {
              "unit": "USD",
              "value": 100
            },
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 220
            }
          }
        }
      ],
      "product": {
        "isBundle": false,
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Tenancy",
            "valueType": "string",
            "value": "Premium (>50 sites)"
          }
        ],
        "productSpecification": {
          "id": "216663aa53702010cd6dddeeff7b12b5",
          "name": "SD-WAN Controller",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "@type": "Place",
          "id": "5671dd2ec3a53010188473ce3640dd81"
        },
        "relatedParty": [
          {
            "firstName": "John",
            "lastName": "Smith",
            "email": "abc2@example.com",
            "phone": "32456768",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "productRelationship": [
          {
            "id": "be6d13f45b5620102dff5e92dc81c781",
            "relationshipType": "Requires"
          }
        ]
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "100",
          "relationshipType": "HasParent"
        }
      ],
      "@type": "ProductOrderItem"
    },
    {
      "id": "120",
      "action": "add",
      "actionReason":"adding service package OLI",
      "quantity": 1,
      "itemPrice": [
        {
          "description": "Tariff plan monthly fee",
          "name": "MonthlyFee",
          "priceType": "recurring",
          "recurringChargePeriod": "month",
          "price": {
            "taxRate": 0,
            "dutyFreeAmount": {
              "unit": "USD",
              "value": 300
            },
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 349
            }
          }
        }
      ],
      "product": {
        "isBundle": false,
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "CPE Model",
            "valueType": "string",
            "value": "ASR"
          },
          {
            "name": "WAN Optimization",
            "valueType": "string",
            "value": "Advance"
          },
          {
            "name": "CPE Type",
            "valueType": "string",
            "value": "Physical"
          },
          {
            "name": "Routing",
            "valueType": "string",
            "value": "Premium"
          }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "@type": "Place",
          "id": "5671dd2ec3a53010188473ce3640dd81"
        },
        "relatedParty": [
          {
            "firstName": "John",
            "lastName": "Smith",
            "email": "abc2@example.com",
            "phone": "32456768",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "productRelationship": [
          {
            "id": "be6d13f45b5620102dff5e92dc81c781",
            "relationshipType": "Requires"
          }
        ]
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "100",
          "relationshipType": "HasParent"
        }
      ],
      "@type": "ProductOrderItem"
    },
    {
      "id": "130",
      "quantity": 1,
      "action": "add",
      "actionReason":"adding service package OLI",
      "itemPrice": [
        {
          "description": "Tariff plan monthly security",
          "name": "MonthlySecurity",
          "priceType": "nonRecurring",
          "price": {
            "taxRate": 0,
            "dutyFreeAmount": {
              "unit": "USD",
              "value": 30
            },
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 30
            }
          }
        }
      ],
      "product": {
        "isBundle": false,
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Security Type",
            "valueType": "string",
            "value": "Premium"
          }
        ],
        "productSpecification": {
          "id": "a6514bd3534560102f18ddeeff7b1247",
          "name": "SD-WAN Security",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "@type": "Place",
          "id": "5671dd2ec3a53010188473ce3640dd81"
        },
        "relatedParty": [
          {
            "firstName": "John",
            "lastName": "Smith",
            "email": "abc2@example.com",
            "phone": "32456768",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "productRelationship": [
          {
            "id": "be6d13f45b5620102dff5e92dc81c781",
            "relationshipType": "Requires"
          }
        ]
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "100",
          "relationshipType": "HasParent"
        }
      ],
      "@type": "ProductOrderItem"
    }
  ],
  "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
  "@type": "ProductOrder"
}'
```

Response body.

```
{
  "orderId": "304e877ac3ab5110856d73ce3640dde5"
}
```

### Processing synchronously \(default\)

The following example shows how to create a product order.

```
curl -X POST "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "requestedCompletionDate": "2021-05-02T08:13:59.506Z",
  "requestedStartDate": "2020-05-03T08:13:59.506Z",
  "externalId": "PO-456",
  "orderCurrency": "USD",
  "channel": [
    {
      "id": "2",
      "name": "Online channel"
    }
  ],
  "note": [
    {
      "text": "This is a TMF product order illustration"
    },
    {
      "text": "This is a TMF product order illustration no 2"
    }
  ],
  "productOrderItem": [
    {
      "id": "POI100",
      "quantity": 1,
      "action": "change",
      "product": {
        "id": "fa6d13f45b5620102dff5e92dc81c77f",
        "@type": "Product",
        "productSpecification": {
          "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "name": "SD-WAN Service Package",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI120",
          "relationshipType": "HasChild"
        },
        {
          "id": "POI130",
          "relationshipType": "HasChild"
        }
      ],
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI120",
      "quantity": 1,
      "action": "change",
      "actionReason":"adding service package OLI",
      "itemPrice": [
        {
          "priceType": "recurring",
          "recurringChargePeriod": "month",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        }
      ],
      "product": {
        "id": "766d13f45b5620102dff5e92dc81c78a",
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "WAN Optimization",
            "value": "Base",
            "previousValue": "Advance"
          }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
          "@type": "ProductSpecificationRef"
        },
        "productRelationship": [
           {
              "id": "326d13f45b5620102dff5e92dc81c785",
              "relationshipType": "Requires"
           }
        ],
        "relatedParty": [
          {
            "id": "51670151c35420105252716b7d40ddfe",
            "firstName": "Joe",
            "lastName": "Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        },
        {
          "id": "POI130",
          "relationshipType": "Requires"
        }  
      ],
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI130",
      "quantity": 1,
      "action": "add",
      "actionReason":"adding service package OLI",
      "itemPrice": [
        {
          "priceType": "recurring",
          "recurringChargePeriod": "month",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Security Type",
            "value": "Base",
            "previousValue": "Advance"
          }
        ],
        "productSpecification": {
          "id": "a6514bd3534560102f18ddeeff7b1247",
          "name": "SD-WAN Security",
          "@type": "ProductSpecificationRef"
        },
        "relatedParty": [
          {
            "id": "51670151c35420105252716b7d40ddfe",
            "firstName": "Joe",
            "lastName": "Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "@type": "ProductOrderItem"
    }
  ],
  "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
  "@type": "ProductOrder"
}
```

Response body.

```
{
  "requestedCompletionDate": "2021-05-02T08:13:59.506Z",
  "requestedStartDate": "2020-05-03T08:13:59.506Z",
  "externalId": "PO-456",
  "orderCurrency": "USD",
  "channel": [
    {
      "id": "2",
      "name": "Online channel"
    }
  ],
  "note": [
    {
      "text": "This is a TMF product order illustration"
    },
    {
      "text": "This is a TMF product order illustration no 2"
    }
  ],
  "productOrderItem": [
    {
      "id": "POI100",
      "quantity": 1,
      "action": "change",
      "actionReason":"adding service package OLI",
      "product": {
        "id": "fa6d13f45b5620102dff5e92dc81c77f",
        "@type": "Product",
        "productSpecification": {
          "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "name": "SD-WAN Service Package",
          "internalVersion": "1",
          "version": "v1",
          "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering",
        "internalVersion": "1",
        "version": "v1",
        "internalId": "69017a0f536520103b6bddeeff7b127d"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI120",
          "relationshipType": "HasChild"
        },
        {
          "id": "POI130",
          "relationshipType": "HasChild"
        }
      ],
      "@type": "ProductOrderItem",
      "state": "new"
    },
    {
      "id": "POI120",
      "quantity": 1,
      "action": "change",
      "actionReason":"adding service package OLI",
      "itemPrice": [
        {
          "priceType": "recurring",
          "recurringChargePeriod": "month",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        }
      ],
      "product": {
        "id": "766d13f45b5620102dff5e92dc81c78a",
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "WAN Optimization",
            "value": "Base",
            "previousValue": "Advance"
          }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
          "internalVersion": "1",
          "version": "v1",
          "internalId": "39b627aa53702010cd6dddeeff7b1202",
          "@type": "ProductSpecificationRef"
        },
        "productRelationship": [
          {
            "id": "326d13f45b5620102dff5e92dc81c785",
            "relationshipType": "Requires"
          }
        ],
        "relatedParty": [
          {
            "id": "51670151c35420105252716b7d40ddfe",
            "firstName": "Joe",
            "lastName": "Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering",
        "internalVersion": "1",
        "version": "v1",
        "internalId": "69017a0f536520103b6bddeeff7b127d"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        },
        {
          "id": "POI130",
          "relationshipType": "Requires"
        }  
      ],
      "@type": "ProductOrderItem",
      "state": "new"
    },
    {
      "id": "POI130",
      "quantity": 1,
      "action": "add",
      "actionReason":"adding service package OLI",
      "itemPrice": [
        {
          "priceType": "recurring",
          "recurringChargePeriod": "month",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Security Type",
            "value": "Base",
            "previousValue": "Advance"
          }
        ],
        "productSpecification": {
          "id": "a6514bd3534560102f18ddeeff7b1247",
          "name": "SD-WAN Security",
          "internalVersion": "1",
          "version": "v1",
          "internalId": "a6514bd3534560102f18ddeeff7b1247",
          "@type": "ProductSpecificationRef"
        },
        "relatedParty": [
          {
            "id": "51670151c35420105252716b7d40ddfe",
            "firstName": "Joe",
            "lastName": "Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering",
        "internalVersion": "1",
        "version": "v1",
        "internalId": "69017a0f536520103b6bddeeff7b127d"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "@type": "ProductOrderItem",
      "state": "new"
    }
  ],
  "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
  "@type": "ProductOrder",
  "id": "8d75939453126010a795ddeeff7b126a",
  "href": "/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a",
  "state": "new"
}
```

### Linking an Existing Payment Profile

To associate an existing payment profile with an order line item, include a payment object in your POST request with only the id field. Provide the system ID or External ID of the payment profile you want to link. The API locates the profile and establishes the association. When using the reference pattern, any other payment fields you include \(paymentMethod, paymentMethodType, paymentReferenceId\) are ignored. The system uses only the id to find and link the existing profile.

Request example:

```
{
  "productOrder": {
    "id": "order_001",
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "ba_456"
        },
        "payment": {
          "id": "sys_id_payment_profile_123"
        }
      }
    ]
  }
}
```

### Creating a Payment Profile Inline

To create a new payment profile during order placement, include a payment object with the payment details but omit the id field. Provide the paymentMethod, paymentMethodType, and paymentReferenceId. The API creates the profile, links it to the order line item's billing account, and associates it with the OLI all in a single operation. Using the inline pattern, you don't need to pre-create the payment profile. This is useful when the payment information is only known at order time or when you want to streamline the order creation workflow without pre-staging payment records.

Request example:

```
{
  "productOrder": {
    "id": "order_002",
    "orderItem": [
      {
        "id": "order_line_002",
        "product": {
          "id": "prod_456"
        },
        "billingAccount": {
          "id": "ba_789"
        },
        "payment": {
          "paymentMethod": "Credit Card",
          "paymentMethodType": "Visa",
          "paymentReferenceId": "REF-2024-001"
        }
      }
    ]
  }
}
```

### Reference Existing Billing Accounts

To associate an existing billing account with an order line item, include a billingAccount object in your POST request with the id field set to the system ID or External ID of the billing account. The API locates the matching billing account and links it to the order line item. When using the reference pattern, any other billing account fields you include \(name, status, active\) are ignored. The system uses only the id to find and link the existing billing account.

Request example:

```
{
  "productOrder": {
    "id": "order_001",
    "relatedParty": [
      {
        "role": "Account",
        "@type": "Account",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "sys_id_account_123"
        }
      }
    ],
    "orderItem": [
      {
        "id": "order_line_001",
        "product": {
          "id": "prod_123"
        },
        "billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
      }
    ]
  }
}
```

### Creating a Billing Account Inline

To create a billing account during order placement, include a billingAccount object with the id field set to the External ID for the new billing account, along with optional name, status, and active fields. The API creates the billing account, associates it with the Account referenced in relatedParty, and links it to the order line item before the order is persisted. Using the inline pattern, you do not need to pre-create the billing account. This is useful when billing account information is only known at order time or when you want to streamline the order creation workflow without pre-staging billing account records. The id field you provide becomes the External ID of the newly created billing account. The system also generates a system ID internally. The order creation response includes the system ID reference to the newly created billing account.

Request example:

```
{
  "productOrder": {
    "id": "order_002",
    "relatedParty": [
      {
        "role": "Account",
        "@type": "Account",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "sys_id_account_789"
        }
      }
    ],
    "orderItem": [
      {
        "id": "order_line_002",
        "product": {
          "id": "prod_456"
        },
        "billingAccount": {
          "id": "ext_ba_2024_001",
          "name": "Project 2024 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
      }
    ]
  }
}
```

### Create account, contact, and location

The following example demonstrates how to create new Account, Contact, and Location records inline during a product order request. This pattern is useful when you have new customer information at order time and want to create the parties as part of the order placement process.

Request body:

```
{
  "productOrder": {
    "id": "order_new_customer_001",
    "expectedCompletionDate": "2025-06-30T23:59:59.000Z",
    "requestedCompletionDate": "2025-06-30T23:59:59.000Z",
    "channel": [
      {
        "id": "1",
        "name": "Web Portal"
      }
    ],
    "relatedParty": [
      {
        "role": "Account",
        "@type": "Account",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "ext_acct_new_tech_2025",
          "accountNumber": "ACC-NEWTECH-2025-001",
          "status": "Active"
        }
      },
      {
        "role": "Contact",
        "@type": "Contact",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "ext_contact_procurement_mgr",
          "firstName": "Maria",
          "lastName": "Garcia",
          "email": "maria.garcia@newtech.com"
        }
      },
      {
        "role": "Location",
        "@type": "Location",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "ext_loc_main_warehouse",
          "name": "Main Distribution Center",
          "address": "500 Industrial Boulevard",
          "city": "Austin",
          "postalCode": "78704",
          "country": "USA"
        }
      }
    ],
    "productOrderItem": [
      {
        "id": "POI001",
        "quantity": 1,
        "action": "add",
        "billingAccount": {
          "id": "ext_ba_newtech_billing",
          "name": "NewTech Solutions - Primary Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "paymentMethod": "Credit Card",
          "paymentMethodType": "American Express",
          "paymentReferenceId": "REF-NEWTECH-2025-001"
        },
        "product": {
          "id": "prod_enterprise_suite",
          "@type": "Product"
        },
        "productOffering": {
          "id": "offering_cloud_platform",
          "name": "Enterprise Cloud Platform"
        },
        "state": "pending",
        "@type": "ProductOrderItem"
      }
    ],
    "state": "pending",
    "@type": "ProductOrder"
  }
}
```

Response body:

```
{
  "productOrder": {
    "id": "order_new_customer_001",
    "status": "created",
    "relatedParty": [
      {
        "role": "Account",
        "@type": "Account",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "sys_id_account_generated_123",
          "accountNumber": "ACC-NEWTECH-2025-001",
          "status": "Active"
        }
      },
      {
        "role": "Contact",
        "@type": "Contact",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "sys_id_contact_generated_456",
          "firstName": "Maria",
          "lastName": "Garcia",
          "email": "maria.garcia@newtech.com"
        }
      },
      {
        "role": "Location",
        "@type": "Location",
        "partyOrPartyRole": {
          "@type": "PartyRef",
          "id": "sys_id_location_generated_789",
          "name": "Main Distribution Center",
          "address": "500 Industrial Boulevard",
          "city": "Austin",
          "postalCode": "78704",
          "country": "USA"
        }
      }
    ],
    "productOrderItem": [
      {
        "id": "POI001",
        "billingAccount": {
          "id": "sys_id_ba_generated_999",
          "name": "NewTech Solutions - Primary Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        },
        "payment": {
          "id": "sys_id_payment_generated_111",
          "paymentMethod": "Credit Card",
          "paymentMethodType": "American Express",
          "paymentReferenceId": "REF-NEWTECH-2025-001"
        }
      }
    ],
    "state": "created"
  }
}
```

## Product Order Open API - POST /sn\_ind\_tmt\_orm/productorder

Creates the specified customer order and customer order line items.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-apis/tmf622_product_ordering-api.md).

Once processed, new records are created in the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]

### URL format

Default URL: `/api/sn_ind_tmt_orm/productorder`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="id_vk2_p5n_t4b" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

Stored in: The channel field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the list tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: empty string

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-entry">

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

 Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

disableCharValueValidation

</td><td>

Flag that indicates how to control characteristic value validation behavior for choice-type characteristics.Valid values:

-   true: Validation is inactive and `characteristic_option_value` is set directly from the request payload without generating work notes.
-   false: Validates characteristic values against allowed choices and adds a work note to the record for any invalid value.

Default: false

To disable validation, create a system property named `sn_ind_tmt_orm.disableCharValueValidation` and set the value to `true`. When inactive, the value is set directly from the request payload and no work notes are generated. The property isn't shipped by default.

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Stored in: The external\_id field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product order, appended with `TMF622`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF622`.

Data Type: String

</td></tr><tr id="productOrder-href-request"><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: empty string

</td></tr><tr><td>

note

</td><td>

Additional notes made by the customer when ordering. Data type: Array of Objects

```
"note": [
  {
    "text": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

note.text

</td><td>

Required. Additional notes/comments made by the customer while ordering. Data type: String

Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

orderCurrency

</td><td>

Required. Currency code for the order and order line items. The currency must be the same for all elements of the order and order line items, otherwise an error is returned and the order isn't created. Once an order is created, its currency code can't be changed. Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Required. Items associated with the product order and their associated action. Data type: Array of Objects

```
"productOrderItem": [
  {
    "action": "String",
    "actionReason": "String",
    "billingAccount": {Object},
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "itemPrice": [Array],
    "payment": {Object},
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemRelationship": [Array],
    "quantity": Number,
    "@type": "String"
  }
]
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change

**Note:** Submitting a change payload that includes a new service location via **productOrderItem.product.place.id** is processed as a move order.

-   delete
-   no-change
-   resume
-   suspend

Data type: String

Stored in: The action field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="productOrder-addReason-request">

Optional. Description of the reason for the order line item.Data type: String

Stored in: The action\_reason field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.billingAccount

</td><td>

Required. Identifies the billing account and determines how the account is processed.-   When you provide a **billing.id** that matches an existing billing account, the API uses the reference pattern to link the account to the order line item. Other billing account fields you include \(**name**, **status**, **active**\) are ignored. The system uses only the ID to find and link the existing billing account.
-   When you provide a **billing.id** that doesn't match an existing billing account, the API creates a new billing account with the provided ID as the external\_id. Billing account fields \(**name**, **status**, **active**\) are required.

Data type: Object

Example reference structure:

```
"billingAccount": {
          "id": "sys_id_billing_account_456",
          "@type": "BillingAccountRef"
        }
```

Example creation structure:

```
"billingAccount": {
          "id": "billingID",
          "name": "Project 1234 Billing",
          "@type": "BillingAccountRef",
          "status": "Active",
          "active": true
        }
```

</td></tr><tr><td>

productOrderItem.billingAccount.@type

</td><td>

Conditional, required only for account creation. Must always be `BillingAccountRef`. This indicates that the object is a reference to a billing account record.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.active

</td><td>

Conditional, required only for account creation. Flag that indicates whether the billing account is active. This field is used when creating a new billing account, and is ignored when referencing an existing billing account.

 Valid values:

-   true: Billing account is active.
-   false: Billing account isn't active.

 Default: If not provided during creation, the system uses the default active value configured in your instance

</td></tr><tr><td>

productOrderItem.billingAccount.id

</td><td>

Required. Sys\_id or external\_id of the billing account to reference or create inline.Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.name

</td><td>

Conditional, required only for account creation. Display name of the billing account. This field is used when creating a new billing account. If not provided during creation, the system uses a default name pattern. This field is ignored when referencing an existing billing account.

Example: "Main Office Billing", "Project 2024 Billing"

Data type: String

</td></tr><tr><td>

productOrderItem.billingAccount.status

</td><td>

Conditional, required only for account creation. The status of the billing account. This field is used when creating a new billing account. Valid values depend on your instance configuration. If not provided during creation, the system uses the default status value configured in your instance. This field is ignored when referencing an existing billing account.

Example: "Active", "Inactive", "Suspended"

Data type: String

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-entry">

Optional. Date and time when the action must be performed on the order line item.

Data type: String

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProductInventoryId-desc">

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr id="externalProductInventory-GET-request"><td>

productOrderItem.externalProductInventory

</td><td id="externalProductInventory-GET-desc-request">

Conditional. If supplied, each entry requires **externalProductInventoryId**. External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Stored in: The external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

Maximum length: 40

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Price associated with the product. Data type: Array of Objects

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

Default: empty string

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is expressed. Data type: String

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Stored in: The mrc or nrc field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.payment

</td><td>

Required. Identifies the payment profile and determines how the profile is processed. Reference an existing payment profile by passing **payment.id**, or pass full payment attributes to create payment profile inline.

-   If the ID already exists, the API locates the matching payment profile and links it to the order line item. Any other payment fields you include \(**paymentMethod**, **paymentMethodType**, **paymentReferenceId**\) are ignored. The system uses only the id to find and link the existing profile.
-   If the ID doesn't already exist, a payment profile is created automatically and linked to the order line item's billing account. **paymentMethod**, **paymentMethodType**, **paymentReferenceId** are required to create the new profile.

Data type: Object

Reference structure:

```
"payment": {
  "id": "String"
}
```

Creation structure:

```
"payment": {
  "id": "String",
  "paymentMethod": "String",
  "paymentMethodType": "String",
  "paymentReferenceId": "String"
}
```

See the 'Examples' section for POST requests demonstrating both reference and creation patterns.

</td></tr><tr><td>

productOrderItem.payment.id

</td><td>

Required. Sys\_id or external\_id of an existing payment profile record.Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethod

</td><td>

Conditional, required only for profile creation. A choice field representing the payment method category. This field is validated against configured payment method choices in your instance. This field is ignored when referencing an existing profile.Example: "Credit Card", "Bank Transfer", "Check", "Digital Wallet"

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentMethodType

</td><td>

Conditional, required only for profile creation. A choice field representing the specific payment method type. This field is validated against configured payment method type choices and is typically dependent on the selected **paymentMethod**. This field is ignored when referencing an existing profile.Example: Visa", "MasterCard", "American Express" for credit cards; "ACH" or "Wire" for bank transfers

Data type: String

</td></tr><tr><td>

productOrderItem.payment.paymentReferenceId

</td><td>

Conditional, required only for profile creation. An external reference identifier for the payment profile. This is typically used for tracking, audit trails, and reconciliation between your order system and your payment processor. This field is ignored when referencing an existing profile.Example: "REF-2024-001", "CARD-XXXX-5678"

Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Required if **productOrderItem.action** is change or delete. Instance details of the product purchased by the customer. Data type: Object

```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Data type: String

Default: empty string

Table: In the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table.

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

```
"place": {
  "id": "String",
  "@type": "String"
}
```

Stored in: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location.

Data type: String

Table: Location \[cmn\_location\]

Stored in: The location field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Characteristics of the associated product. Data type: Array of Objects

```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product.Data type: String

Table: Characteristic \[sn\_prd\_pm\_characteristic\]

Stored in: The characteristics field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The previous\_characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

Stored in: The characteristic\_option\_value field of the sn\_ind\_tmt\_orm\_order\_characteristic\_value table.

Default: empty string

</td></tr><tr id="tmf-prod-order_prodChar.valueType"><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Optional. Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

-   When this system property is set to true \(default\), the product inventory is automatically upgraded to the version in the order by changing the referenced product specification. This allows the order to be successfully processed.
-   When this system property is set to false, if the product inventory is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification. The initial version is the sys\_id of the first version of the specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of party roles linked to an OrderLineItemContact. Data type: Array of Objects

```
"relatedParty": [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Stored in: The email field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Stored in: The first\_name field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Stored in: The lastName field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Stored in: The business\_phone field of the sn\_ind\_tmt\_orm\_order\_line\_item\_contact table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial version or external ID of the product offering. The initial version is the sys\_id of the first version of the offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. List that describes the parent/child relationship between order items. Data type: Array of Objects

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Stored in: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required. Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Stored in: The parent\_line\_item field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

Default: empty string

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify relationship hierarchy. Possible values:

-   HasChild
-   HasParent

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Stored in: The quantity field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

relatedParty

</td><td>

Array that contains one or more party objects. Each object in this array represents a party \(Account, Contact, or Location\) that should be associated with the order. The **relatedParty** array is optional at the order level, but if you provide party associations, each entry in the array must follow the required structure and validation rules.

Data type: Array of Objects

```
"relatedParty": [
 {
  "role": "String",
  "@type": "String",
  "partyOrPartyRole": {Object}
 }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

Required. Specifies what record type to search for when validating and linking the party. Must match the **role** field.When you provide an @type of "Account", the system knows to search the Account table for the matching record. When you provide an @type of "Contact", the system knows to search the Contact table. This field ensures that the API searches the correct record type and applies the correct validation and linking logic.

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole

</td><td>

Object containing the specific reference details about the party. Contains the party identifier and any optional attributes that should be used if creating a new party record.-   For reference patterns, this object contains just the **@type** and **id** fields.
-   For creation patterns, this object also contains conditional attributes like **name**, **email**, **address** that is used to create the new record if the **id** value does not match an existing record. Attributes vary based on party type.

Data type: Object

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String"
}
```

Account creation Object structure:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "accountNumber": "String",
  "status": "String"
}
```

Contact creation Object structure:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "firstName": "String",
  "lastName": "String",
  "email": "String"
 }
```

Location creation Object structure:

```
"partyOrPartyRole": {
  "@type": "PartyRef",
  "id": "String",
  "name": "String",
  "address": "String",
  "city": "String",
  "postalCode": "String",
  "country": "String"
 }
```

</td></tr><tr><td>

relatedParty.partyOrPartyRole.@type

</td><td>

Required. Indicates the type of reference being provided. Value must be set to `PartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.accountNumber

</td><td>

Required for Account party types. External reference number or identifier for the Account. It provides a business-facing account identifier that is distinct from the system-generated ID.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.address

</td><td>

Required for Location party types. Street address of the location.Example: "123 Main Street"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.city

</td><td>

Required for Location party types. City or municipality name for the location.Example: "San Francisco", "New York"

Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.country

</td><td>

Required for Location party types. Country where the location is physically situated or where the contact is based.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.email

</td><td>

Required for Contact party types. Contact person's primary email address.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.firstName

</td><td>

Required for Contact party types. Contact person's first name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.id

</td><td>

Required. Sys\_id or external\_id of the party record to reference. The system searches for a record with either a matching system ID or matching External ID.For reference patterns with an existing record, only the id is used and all other provided fields are ignored. For creation patterns when no matching record exists, the ID becomes the external ID of the newly created record, and other provided fields populate the new record's attributes.

Data type: String

Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Location \[location\]

</td></tr><tr><td>

relatedParty.partyOrPartyRole.lastName

</td><td>

Required for Contact party types. Contact person's last name or given name.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.name

</td><td>

Required for Account, Contact, and Location types. Name of the account, contact, or location. Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.postalCode

</td><td>

Required for Location party types. Postal code, ZIP code, or PIN code for the location.Data type: String

</td></tr><tr><td>

relatedParty.partyOrPartyRole.status

</td><td>

Required for Account party types. Current status of the account. The valid values for the status field depend on how your instance is configured.Common status values include:

-   `Active`: Account is in normal operation
-   `Inactive`: Account is not currently conducting business
-   `Suspended`: Account is temporarily restricted
-   `Pending`: Account is awaiting activation
-   `Archived`: Historical accounts
-   `Under Review`: Account is being evaluated

Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Required. Business role that the referenced party plays in the order context. Must match **relatedParty.@type** in the same object.Possible values:

-   `Account`: parties representing a customer or business entity
-   `Contact`: parties representing a contact person
-   `Customer`: parties representing an end consumer or individual
-   `Location`: parties representing a service address or fulfillment location

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

Stored in: The expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Stored in: The expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: empty string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record:

-   `The following Order Item characteristics does not exist: Review specification <**characteristic.name**> and correct the characteristic and characteristic option in the order line item prior to approving the order.`
-   `Order Item characteristic: <**characteristic.name**> with characteristic value: <**characteristic.value**>is invalid. Correct the characteristic values before approving the order.`

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   `Invalid payload: Request body missing` - Payload was not passed in the request body.
-   `Invalid payload: productOrderItem is missing` - Product order line item object or JSON is missing.
-   `Invalid payload: productOrderItem id is missing` - The **id** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem action is missing` - The **action** parameter is missing in the product order line item of the payload.
-   `Invalid payload: productOrderItem productOffering is missing` - The product offering object or JSON is missing from the product order line item in the payload.
-   `Invalid payload: productOffering id is missing` - The **id** parameter is missing in the product order line item of the product offering object in the payload.
-   `Invalid payload: Product offering does not exist` - The product offering in the product order line item is not valid.
-   `Invalid payload: productOrderItem product is missing` - The product object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: product productSpecification is missing` - The product specification object or JSON in the product order line item is missing from the payload.
-   `Invalid payload: productSpecification id is missing` - The **id** parameter in the product order line item of the product specification object is missing from the payload.
-   `Invalid payload: Product specification does not exist` - The product specification in the product order line item is not valid.
-   `Invalid payload: Product Inventory does not exist` - In a change order \(action = change\), the quantity of an item is greater than what is in stock.
-   `Invalid payload: Product inventory ID is missing` - In change order, the **product.id** is missing in the payload.
-   `Invalid payload: Sold Product is inactive` - In a change order, a product specified in the payload is inactive.
-   `Invalid payload: relatedParty is missing` - The related party object is missing from the payload.
-   `Invalid payload: Customer Account or Consumer is missing` - The related party customer or consumer object is missing from the payload.
-   `Invalid payload: Consumer does not exist` - The specified related party consumer does not exist in the ServiceNow instance.
-   `Invalid payload: Customer Account does not exist` - The specified related party customer does not exist in the ServiceNow instance.
-   `Invalid payload: Order creation failed` - Not able to create the requested order.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr><tr><td>

channel

</td><td>

List of channels to use for selling the products. Data type: Array of Objects

 ```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.id

</td><td>

Unique identifier of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number.Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product order, appended with `TMF622`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF622`.

Data Type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order created for this request. Data type: String

</td></tr><tr><td>

note

</td><td>

Optional. List of additional notes made by the customer when ordering. Data type: Array of Objects

 ```
"note": [
  {
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

</td></tr><tr><td>

productOderItem.actionReason

</td><td>

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array of Objects

 ```
"productOrderItem:" [
  {
    "action": "String",
    "id": "String",
    "itemPrice": [Array],
    "product": {Object},
    "productOffering": {Object},
    "productOrderItemReleationship": [Array],
    "quantity": Number,
    "state": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

productOrderItem.action

</td><td>

Action to carry out on the product. Possible actions are defined on the list tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Sys\_id of the order line item. Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table

Data type: String

Default: Blank string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

List that describes the price associated with the product. Data type: Array of Objects

 ```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

 ```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

 ```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludeAmount.value

</td><td>

Price of product, including any tax. Data type: Number

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

productOrderItem.product

</td><td>

Description of the instance details of the product purchased by the customer. Data type: Object

 ```
"product": {
  "id": "String",
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. This parameter is only returned if **productOrderItem.action** is `change` or `delete`. If both sys\_id and external\_id are present, the external\_id is returned. Data type: String

</td></tr><tr><td>

productOrderItem.product.place

</td><td>

Maps of the locations on which to install the product. Data type: Object

 ```
"place": {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

List of characteristics of the associated product. Data type: Array of Objects

 ```
"productCharacteristic": [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   `address`
-   `array.date`
-   `array.datetime`
-   `array.decimal`
-   `array.integer`
-   `array.object`
-   `array.single_line_text`
-   `attachment`
-   `checkbox`
-   `choice`
-   `date`
-   `date_time`
-   `decimal`
-   `duration`
-   `email`
-   `integer`
-   `object`
-   `single_line_text`
-   `yes_no`

Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. Data type: Object

 ```
"productSpecification": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table. If both sys\_id and external\_id are present, the external\_id is returned.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Internal version of the product specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External version of the product specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

Optional. List of contacts for line items. Data type: Array of Objects

 ```
"relatedParty:" [
  {
    "email": "String",
    "firstName": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

 Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

 Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering

</td><td>

Description of the product offering associated with the product. Data type: Object

 ```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. If both sys\_id and external\_id are present, the external\_id is returned.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Conditional. Item-level relationships. If supplied, each entry requires an **id** and **relationshipType**. Data type: Array of Objects

 ```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

</td></tr><tr><td>

productOrderItem.state

</td><td>

Current state of the product order item. This value is always `new`.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Contains at least one item with customer account or consumer account information. Data type: Array of Objects

 ```
"relatedParty": [
  {
    "id": "String",
    "name": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Table: Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table.

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.type

</td><td>

Type of customer. Possible values:

-   **Consumer**
-   **Customer**
-   **CustomerContact**

 Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Optional. Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Optional. Order start date requested by the customer. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalVersion

</td><td>

Internal version of the service specification. Must match the value of **version** otherwise an error is thrown.Data Type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.version

</td><td>

External version of the service specification. Must match the value of **internalVersion** otherwise an error is thrown.Data Type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. For this endpoint, this value is always `new`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example creates a customer order.

```
curl -X POST "https://servicenow-instance/api/sn_ind_tmt_orm/productorder" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "requestedCompletionDate": "2021-05-02T08:13:59.506Z",
  "requestedStartDate": "2020-05-03T08:13:59.506Z",
  "externalId": "PO-456",
  "externalSystem": "Salesforce – TMF 622",
  "channel": [
    {
      "id": "2",
      "name": "Online channel"
    }
  ],
  "note": [
    {
      "text": "This is a TMF product order illustration"
    },
    {
      "text": "This is a TMF product order illustration no 2"
    }
  ],
  "productOrderItem": [
    {
      "id": "POI100",
      "quantity": 1,
      "action": "change",
      "product": {
        "id": "fa6d13f45b5620102dff5e92dc81c77f",
        "@type": "Product",
        "productSpecification": {
          "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "name": "SD-WAN Service Package",
          "@type": "ProductSpecificationRef"
        },
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI120",
          "relationshipType": "HasChild"
        },
        {
          "id": "POI130",
          "relationshipType": "HasChild"
        }
      ],
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI120",
      "quantity": 1,
      "action": "change",
      "itemPrice": [
        {
          "priceType": "recurring",
          "recurringChargePeriod": "month",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        }
      ],
      "product": {
        "id": "766d13f45b5620102dff5e92dc81c78a",
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "WAN Optimization",
            "valueType": "Object",
            "value": "Base",
            "previousValue": "Advance"
          }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
          "@type": "ProductSpecificationRef",
          "externalVersion": "1",
          "@version": "v1"
        },
        "relatedParty": [
          {
            "id": "51670151c35420105252716b7d40ddfe",
            "firstName": "Joe",
            "lastName": "Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "@type": "ProductOrderItem"
    },
    {
      "id": "POI130",
      "quantity": 1,
      "action": "add",
      "itemPrice": [
        {
          "priceType": "recurring",
          "recurringChargePeriod": "month",
          "price": {
            "taxIncludedAmount": {
              "unit": "USD",
              "value": 20
            }
          }
        }
      ],
      "product": {
        "@type": "Product",
        "productCharacteristic": [
          {
            "name": "Security Type",
            "valueType": "Object",
            "value": "Base",
            "previousValue": "Advance"
          }
        ],
        "productSpecification": {
          "id": "a6514bd3534560102f18ddeeff7b1247",
          "name": "SD-WAN Security",
          "@type": "ProductSpecificationRef"
        },
        "relatedParty": [
          {
            "id": "51670151c35420105252716b7d40ddfe",
            "firstName": "Joe",
            "lastName": "Doe",
            "email": "abc@example.com",
            "phone": "1234567890",
            "@type": "RelatedParty",
            "@referredType": "OrderLineItemContact"
          }
        ],
        "place": {
          "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
          "@type": "Place"
        }
      },
      "productOffering": {
        "id": "69017a0f536520103b6bddeeff7b127d",
        "name": "Premium SD-WAN Offering"
      },
      "productOrderItemRelationship": [
        {
          "id": "POI100",
          "relationshipType": "HasParent"
        }
      ],
      "@type": "ProductOrderItem"
    }
  ],
  "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
  "@type": "ProductOrder"
}
```

Response body.

```
{
    "requestedCompletionDate": "2021-05-02T08:13:59.506Z",
    "requestedStartDate": "2020-05-03T08:13:59.506Z",
    "externalId": "PO-456",
    "externalSystem": "Salesforce – TMF 622",
    "channel": [
        {
            "id": "2",
            "name": "Online chanel"
        }
    ],
    "note": [
        {
            "text": "This is a TMF product order illustration"
        },
        {
            "text": "This is a TMF product order illustration no 2"
        }
    ],
    "productOrderItem": [
        {
            "id": "POI100",
            "quantity": 1,
            "action": "change",
            "product": {
                "id": "fa6d13f45b5620102dff5e92dc81c77f",
                "@type": "Product",
                "productSpecification": {
                    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
                    "name": "SD-WAN Service Package",
                    "@type": "ProductSpecificationRef"
                },
                "place": {
                    "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                    "@type": "Place"
                }
            },
            "productOffering": {
                "id": "69017a0f536520103b6bddeeff7b127d",
                "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
                {
                    "id": "POI120",
                    "relationshipType": "HasChild"
                },
                {
                    "id": "POI130",
                    "relationshipType": "HasChild"
                }
            ],
            "@type": "ProductOrderItem",
            "state": "new"
        },
        {
            "id": "POI120",
            "quantity": 1,
            "action": "change",
            "itemPrice": [
                {
                    "priceType": "recurring",
                    "recurringChargePeriod": "month",
                    "price": {
                        "taxIncludedAmount": {
                            "unit": "USD",
                            "value": 20
                        }
                    }
                }
            ],
            "product": {
                "id": "766d13f45b5620102dff5e92dc81c78a",
                "@type": "Product",
                "productCharacteristic": [
                    {
                        "name": "WAN Optimization",
                        "valueType": "Object",
                        "value": "Base",
                        "previousValue": "Advance"
                    }
                ],
                "productSpecification": {
                    "id": "39b627aa53702010cd6dddeeff7b1202",
                    "name": "SD-WAN Edge Device",
                    "@type": "ProductSpecificationRef",
                    "externalVersion": "1",
                    "@version": "v1"
                "relatedParty": [
                    {
                        "id": "51670151c35420105252716b7d40ddfe",
                        "firstName": "Joe",
                        "lastName": "Doe",
                        "email": "abc@example.com",
                        "phone": "1234567890",
                        "@type": "RelatedParty",
                        "@referredType": "OrderLineItemContact"
                    }
                ],
                "place": {
                    "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                    "@type": "Place"
                }
            },
            "productOffering": {
                "id": "69017a0f536520103b6bddeeff7b127d",
                "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
                {
                    "id": "POI100",
                    "relationshipType": "HasParent"
                }
            ],
            "@type": "ProductOrderItem",
            "state": "new"
        },
        {
            "id": "POI130",
            "quantity": 1,
            "action": "add",
            "itemPrice": [
                {
                    "priceType": "recurring",
                    "recurringChargePeriod": "month",
                    "price": {
                        "taxIncludedAmount": {
                            "unit": "USD",
                            "value": 20
                        }
                    }
                }
            ],
            "product": {
                "@type": "Product",
                "productCharacteristic": [
                    {
                        "name": "Security Type",
                        "valueType": "Object",
                        "value": "Base",
                        "previousValue": "Advance"
                    }
                ],
                "productSpecification": {
                    "id": "a6514bd3534560102f18ddeeff7b1247",
                    "name": "SD-WAN Security",
                    "@type": "ProductSpecificationRef"
                },
                "relatedParty": [
                    {
                        "id": "51670151c35420105252716b7d40ddfe",
                        "firstName": "Joe",
                        "lastName": "Doe",
                        "email": "abc@example.com",
                        "phone": "1234567890",
                        "@type": "RelatedParty",
                        "@referredType": "OrderLineItemContact"
                    }
                ],
                "place": {
                    "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
                    "@type": "Place"
                }
            },
            "productOffering": {
                "id": "69017a0f536520103b6bddeeff7b127d",
                "name": "Premium SD-WAN Offering"
            },
            "productOrderItemRelationship": [
                {
                    "id": "POI100",
                    "relationshipType": "HasParent"
                }
            ],
            "@type": "ProductOrderItem",
            "state": "new"
        }
    ],
    "relatedParty": [
        {
            "id": "eaf68911c35420105252716b7d40ddde",
            "name": "Sally Thomas",
            "@type": "RelatedParty",
            "@referredType": "CustomerContact"
        },
        {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Funco Intl",
            "@type": "RelatedParty",
            "@referredType": "Customer"
        },
        {
            "id": "59f16de1c3b67110ff00ed23a140dd9e",
            "name": "Funco External",
            "@type": "RelatedParty",
            "@referredType": "Consumer"
        }
    ],
    "@type": "ProductOrder",
    "id": "6be0a925c3a220103e2e73ce3640ddfe",
    "state": "new"
}
```

