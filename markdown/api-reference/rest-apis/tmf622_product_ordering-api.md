---
title: Product Order Open API
description: The Product Order Open API provides endpoints that enable a standardized mechanism for placing product orders.Retrieves all product orders.Retrieves the specified product order.Retrieves all product orders.Retrieves the specified product order.Updates the specified customer order.Updates the specified customer order.Cancels the specified customer order.Creates the specified customer order and customer order line items.Creates the specified customer order and customer order line items.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 150
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Product Order Open API

The Product Order Open API provides endpoints that enable a standardized mechanism for placing product orders.

A product order is created based on a product offering that is defined and published in a product catalog. The product offering identifies the product or set of products that are available to a customer and includes the relevant product characteristics that capture the unique options of a product, and other relevant attributes such as pricing, contract terms, and availability.

To access this API, the Order Management for Telecommunications \(sn\_ind\_tmt\_orm\) plugin must be activated.

This API is provided within the `sn_ind_tmt_orm` namespace.

The calling user must have the sn\_ind\_tmt\_orm.order\_integrator role.

This API can be extended to make customizations around required parameters, request body validation, additional REST operations, and field mappings. For more information, see the [Product Order Open API Developer Guide](../../guides/telecom/concept/product-order_dev-guide.md#).

The Product Order Open API is a ServiceNow® implementation of TM Forum TMF622 Product Ordering Management API REST Specification and is conformance certified by TM Forum.

![TMF conformance logo](../image/tmf-conformance.png)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Product Order Open API - GET /sn\_ind\_tmt\_orm/order/productOrder

Retrieves all product orders.

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]
-   Order Line Related Items \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter is not used, all fields are returned. Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Default: 20

Maximum: 100

Data type: Number

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Default: 0

Data type: Number

</td></tr><tr><td>

state

</td><td>

Filter orders by state. Only orders with a state matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

Specifies the range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

<table id="table_inf_kxr_nsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

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

expectedCompletionDate

</td><td>

Date on which the order will be completed.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the product order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product order. Data type: String

</td></tr><tr><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

 ```
"note": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.author

</td><td>

User name of the person that authored the associated note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date that the note was created.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array

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

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-resp-descr">

Array of objects containing external ids mapped to the product inventories created for the order. Data type: Array

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-resp-descr">

External id mapped to the product inventory.Data type: String

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

 ```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

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

productOrderItem.ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem.product

</td><td>

Description of the instance details of the product purchased by the customer. Data type: Object

 ```
"product:" {
  "place": {Object},
  "productCharacteristic": [Array],
  "productRelationship": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Only product characteristics whose **value** are different than the **previousValue** are returned.

Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productRelationship

</td><td>

List of product relationship details for an order line item.Data type: Array

```
"productRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.productRelationship.id

</td><td>

Sys\_id or sn\_prd\_invt\_external\_id of the product inventory. Located in the sys\_id or sn\_prd\_invt\_external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productRelationship.relationshipType

</td><td>

Type of relationship between the order line item and the product inventory.Possible value: Requires

Data type: String

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

Initial\_version of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" [
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

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

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

Initial\_version of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of product items purchased.Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.state

</td><td>

State of the order of the associated product item.Data type: String

</td></tr><tr><td>

productOrderItem.version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

```
"relatedParty:" [
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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. Data type: String

</td></tr><tr><td>

version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

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

## Product Order Open API - GET /sn\_ind\_tmt\_orm/order/productOrder/\{id\}

Retrieves the specified product order.

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]
-   Order Line Related Items \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id or external\_id of the customer order to retrieve. Located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="tmf-get-list-status-codes"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed. Full resource returned in response \(no pagination\). The response returns successful with an error message if the selected order has processing issues.

-   A 200 OK response happens if the order is in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table waiting for the scheduler to pick the record to be processed. The error message field includes details for the record. For example:

    ```
{
 "code": 102,
 "reason": "Request in queue",
 "message": "Request in queue",
 "details": [
  {
   "message": "This Order is still in the inbound queue table waiting to be processed.",
   "datapath": ""
  }
 ]
}
    ```

-   A 200 OK response happens if an order creation fails and the record in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table is in an error state. The error message field includes details in for the inbound queue table record. For example:

    ```
{
 "code": 23,
 "reason": "Missing body field",
 "message": "Missing body field",
 "details": [
  {
   "message": "Invalid payload: orderCurrency is missing",
   "datapath": "/"
  }
 ]
}
    ```


</td></tr><tr><td>

206

</td><td>

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td>

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

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

expectedCompletionDate

</td><td>

Date on which the order will be completed.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the product order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product order. Data type: String

</td></tr><tr><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

```
"note": [
  {
    "author": "String",
    "date": "String",
    "text": "String"
  }
]
```

</td></tr><tr><td>

note.author

</td><td>

User name of the person that authored the associated note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date that the note was created.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items.Data type: String

</td></tr><tr><td>

ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array

```
"productOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
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

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-resp-descr">

Array of objects containing external ids mapped to the product inventories created for the order. Data type: Array

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-resp-descr">

External id mapped to the product inventory.Data type: String

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

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

productOrderItem.ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem.product

</td><td>

Description of the instance details of the product purchased by the customer. Data type: Object

```
"product:" {
  "place": {Object},
  "productCharacteristic": [Array],
  "productRelationship": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Only product characteristics whose **value** are different than the **previousValue** are returned.

Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productRelationship

</td><td>

List of product relationship details for an order line item.Data type: Array

```
"productRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.productRelationship.id

</td><td>

Sys\_id or sn\_prd\_invt\_external\_id of the product inventory. Located in the sys\_id or sn\_prd\_invt\_external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productRelationship.relationshipType

</td><td>

Type of relationship between the order line item and the product inventory.Possible value: Requires

Data type: String

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

Initial\_version of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" {
  "email": "String",
  "firstName": "String",
  "id": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
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

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

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

Initial\_version of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of product items purchased.Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

 Data type: String

</td></tr><tr><td>

productOrderItem.state

</td><td>

State of the order of the associated product item.Data type: String

</td></tr><tr><td>

productOrderItem.version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

```
"relatedParty:" [
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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. Data type: String

</td></tr><tr><td>

version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a specified product order.

```
curl -X GET "https://instance.service-now.com/api/sn_ind_tmt_orm/order/productOrder/8d75939453126010a795ddeeff7b126a" \
-u "username":"password"
```

Response body.

```
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
```

## Product Order Open API - GET /sn\_ind\_tmt\_orm/productorder

Retrieves all product orders.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - GET /sn\_ind\_tmt\_orm/order/productOrder](tmf622_product_ordering-api.md#).

This endpoint retrieves order information from the following tables:

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

<table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Data type: String

Default: All fields returned.

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Default: 20

Maximum: 100

Data type: Number

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Default: 0

Data type: Number

</td></tr><tr><td>

state

</td><td>

Filter orders by state. Only orders with a state matching the value of this parameter are returned in the response.Data type: String

Default: All states returned.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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

Specifies the range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

<table id="table_inf_kxr_nsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Date on which the order will be completed.Data type: String

</td></tr><tr><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

```
"note": {
  "author": "String",
  "date": "String",
  "text": "String"
}
```

</td></tr><tr><td>

note.author

</td><td>

User name of the person that authored the associated note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date that the note was created.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

</td></tr><tr><td>

ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array

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

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

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

productOrderItem.ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem.product

</td><td>

Description of the instance details of the product purchased by the customer. Data type: Object

```
"product:" {
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Only product characteristics whose **value** are different than the **previousValue** are returned.

Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. Data type: Object

```
"productSpecification:" {
  "id": "String",
  "name": "String",
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

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" {
  "email": "String",
  "firstName": "String",
  "id": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
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

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

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

productOrderItem.quantity

</td><td>

Number of product items purchased.Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.state

</td><td>

State of the order of the associated product item.Data type: String

</td></tr><tr><td>

productOrderItem.version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

```
"relatedParty:" [
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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. Data type: String

</td></tr><tr><td>

version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

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

## Product Order Open API - GET /sn\_ind\_tmt\_orm/productorder/\{id\}

Retrieves the specified product order.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - GET /sn\_ind\_tmt\_orm/order/productOrder/\{id\}](tmf622_product_ordering-api.md#).

This endpoint retrieves order information from the following tables:

-   Customer Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]

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

Sys\_id or external\_id of the customer order to retrieve. Located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Date on which the order will be completed.Data type: String

</td></tr><tr><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

```
"note": {
  "author": "String",
  "date": "String",
  "text": "String"
}
```

</td></tr><tr><td>

note.author

</td><td>

User name of the person that authored the associated note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date that the note was created.Data type: String

</td></tr><tr><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

</td></tr><tr><td>

ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array

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

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

productOrderItem.itemPrice.price.taxIncludedAmount

</td><td>

Description of the price of the associated product, including the tax. Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": Number
}
```

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

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

productOrderItem.ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: The point of no return for the order has been reached.
-   false: The point of no return for the order has not been reached.

Data type: Boolean

</td></tr><tr><td>

productOrderItem.product

</td><td>

Description of the instance details of the product purchased by the customer. Data type: Object

```
"product:" {
  "place": {Object},
  "productCharacteristic": [Array],
  "productSpecification": {Object},
  "relatedParty": {Object},
  "@type": "String"
}
```

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Only product characteristics whose **value** are different than the **previousValue** are returned.

Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Description of the product specification associated with the product. Data type: Object

```
"productSpecification:" {
  "id": "String",
  "name": "String",
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

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" {
  "email": "String",
  "firstName": "String",
  "id": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
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

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

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

productOrderItem.quantity

</td><td>

Number of product items purchased.Data type: Number

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.state

</td><td>

State of the order of the associated product item.Data type: String

</td></tr><tr><td>

productOrderItem.version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

```
"relatedParty:" [
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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. Data type: String

</td></tr><tr><td>

version

</td><td>

Order version.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

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

## Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}

Updates the specified customer order.

### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the customer order to update. Located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_vk2_p5n_t4b" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="channel-row-tmf622"><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr id="channel_id-row-tmf622"><td>

channel.id

</td><td>

Required if the **channel** parameter is used. Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/channel

Default: Blank string

</td></tr><tr id="channel_name-row-tmf622"><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the Choice List tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: Blank string

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-PATCH">

Date and time when the action must be performed on the order.This value must be the same as or later than the **committedDueDate** values for each order line item.

If the action for order line items is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/committed\_due\_date

</td></tr><tr id="externalId-row-tmf622"><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/external\_id

Default: Blank string

</td></tr><tr id="note-row-tmf622"><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

```
"note": [
  {
    "text": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr id="note_text-row-tmf622"><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/comments

Default: Blank string

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items. Updating the currency code of an existing order is not supported. Providing any value other than the currency code already associated with the order causes the update to be rejected.Data type: String

</td></tr><tr id="productOrderItem-row-tmf622"><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOrderItem_action-row-tmf622"><td>

productOrderItem.action

</td><td>

Required if the **productOrderItem** parameter is used. Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action

Default: add

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="prodOrdItem_actionReason-response-tmf622">

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-PATCH">

Date and time when the action must be performed on the order line item.If the action for the item is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/committed\_due\_date

</td></tr><tr id="externalProdInv-PATCH"><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-descr-PATCH">

Array of objects containing external ids to map to the product inventories created for the order. Data type: Array

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr id="externalProdInvId"><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-decsr">

External id to map to the product inventory.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_inventory\_id and sn\_prd\_invt\_product\_inventory/sn\_prd\_invt\_external\_id

</td></tr><tr id="productOrderItem_id-row-tmf622"><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_id

Maximum length: 40

Default: Blank string

</td></tr><tr id="itemPrice-row-tmf622"><td>

productOrderItem.itemPrice

</td><td id="itemPrice-entry-tmf622">

Array of objects that describe the price associated with the product. Data type: Array

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Table updated: sn\_ind\_tmt\_orm\_order

Default: Blank string

</td></tr><tr id="itemPrice_price-row-tmf622"><td>

productOrderItem.itemPrice.price

</td><td id="itemPrice_price-entry-tmf622">

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

Default: Blank string

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

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="itemPrice_price_taxIncludedAmt_unit-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td id="itemPrice_price_taxIncludedAmt_unit-entry-tmf622">

Currency code in which the price is depicted. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr id="itemPrice_price_taxIncludedAmt_value-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td id="itemPrice_price_taxIncludedAmt_value-entry-tmf622">

Price of product, including any tax. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr id="itemPrice_priceType-row-tmf622"><td>

productOrderItem.itemPrice.priceType

</td><td id="itemPrice_priceType-entry-tmf622">

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr id="itemPrice_recurringChargePeriod-row-tmf622"><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td id="itemPrice_recurringChargePeriod-entry-tmf622">

If the price is recurring, the recurring period, such as `month`. Data type: String

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_id-row-tmf622"><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_place_id-row-tmf622"><td>

productOrderItem.product.place.id

</td><td>

Required if the **productOrderItem.product.place** parameter is used. Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/location

Default: Blank string

</td></tr><tr id="product_place_type-row-tmf622"><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr id="prod_prodChar-row-tmf622"><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr id="prod_prodChar_name-row-tmf622"><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristics

Default: Blank string

</td></tr><tr id="prod_prodChar_previousValue-row-tmf622"><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/previous\_characteristic\_option\_value

Default: Blank string

</td></tr><tr id="prod_prodChar_value-row-tmf622"><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristic\_option\_value

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_productSpecification_id-row-tmf622"><td>

productOrderItem.product.productSpecification.id

</td><td>

Required if the **productOrderItem.product.productSpecification** parameter is used. Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr id="product_productSpecification_name-row-tmf622"><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr id="product_productSpecification_type-row-tmf622"><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr id="product_relatedParty-row-tmf622"><td>

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr id="product_relatedParty_email-row-tmf622"><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/email

Default: Blank string

</td></tr><tr id="product_relatedParty_firstName-row-tmf622"><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/first\_name

Default: Blank string

</td></tr><tr id="product_relatedParty_id-row-tmf622"><td>

productOrderItem.product.relatedParty.id

</td><td>

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/sys\_id

Default: Blank string

</td></tr><tr id="product_relatedParty_lastName-row-tmf622"><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/lastName

Default: Blank string

</td></tr><tr id="product_relatedParty_phone-row-tmf622"><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/business\_phone

Default: Blank string

</td></tr><tr id="product_relatedParty_referredType-row-tmf622"><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr id="product_relatedParty_type-row-tmf622"><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr id="product_type-row-tmf622"><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

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

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOffering_id-row-tmf622"><td>

productOrderItem.productOffering.id

</td><td>

Required if the **productOrderItem.productOffering** parameter is used. Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="productOffering_name-row-tmf622"><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="productOrdItem_quantity-row-tmf622"><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: null

</td></tr><tr id="productOrderItemRelationship-row-tmf622"><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOrderItemRelationship_id-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required if the **productOrderItem.productOrderItemRelationship** parameter is used. Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/parent\_line\_item

Default: Blank string

</td></tr><tr id="productOrderItemRelationship_relType-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: Blank string

</td></tr><tr><td>

productOrderItem.revisionOperation

</td><td>

Type of update to perform on the line item. If this value is empty, the existing line item is updated, or a new line item is added if it does not already exist. If this value is `cancel`, the line item is canceled.Data type: String

Default: Blank string

</td></tr><tr><td>

productOrderItem.@type

</td><td id="prodOrdItem_type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr id="relatedParty-row-tmf622"><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

</td></tr><tr id="relatedParty_id-row-tmf622"><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr id="relatedParty_name-row-tmf622"><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr id="relatedParty_referredType-row-tmf622"><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr id="relatedParty_type-row-tmf622"><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr id="requestedCompletionDate-row-tmf622"><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_end\_date

Default: Blank string

</td></tr><tr id="requestedStartDate-row-tmf622"><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_start\_date

Default: Blank string

</td></tr><tr><td>

@type

</td><td id="type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

<table id="table_c1v_xpk_5rb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

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

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

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

List that describes items associated with the product order and their associated action. Data type: Array

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

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td id="d3022e1602">

Array of objects containing external ids to map to the product inventories created for the order. Data type: Array

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

External id mapped to the product inventory.Data type: String

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

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

Initial\_version of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

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

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

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

Initial\_version of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Data type: String

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

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.type

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

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

## Product Order Open API - PATCH /sn\_ind\_tmt\_orm/productorder/\{id\}

Updates the specified customer order.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - PATCH /sn\_ind\_tmt\_orm/order/productOrder/\{id\}](tmf622_product_ordering-api.md#).

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

Sys\_id of the customer order to update. Located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_vk2_p5n_t4b" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="channel-row-tmf622"><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr id="channel_id-row-tmf622"><td>

channel.id

</td><td>

Required if the **channel** parameter is used. Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/channel

Default: Blank string

</td></tr><tr id="channel_name-row-tmf622"><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the Choice List tab in the Channel Dictionary Entry of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: Blank string

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-PATCH">

Date and time when the action must be performed on the order.This value must be the same as or later than the **committedDueDate** values for each order line item.

If the action for order line items is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/committed\_due\_date

</td></tr><tr id="externalId-row-tmf622"><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/external\_id

Default: Blank string

</td></tr><tr id="note-row-tmf622"><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

```
"note": [
  {
    "text": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr id="note_text-row-tmf622"><td>

note.text

</td><td>

Additional notes/comments made by the customer while ordering. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/comments

Default: Blank string

</td></tr><tr><td>

orderCurrency

</td><td>

Currency code for the order and order line items. Updating the currency code of an existing order is not supported. Providing any value other than the currency code already associated with the order causes the update to be rejected.Data type: String

</td></tr><tr id="productOrderItem-row-tmf622"><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOrderItem_action-row-tmf622"><td>

productOrderItem.action

</td><td>

Required if the **productOrderItem** parameter is used. Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action

Default: add

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="prodOrdItem_actionReason-response-tmf622">

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-PATCH">

Date and time when the action must be performed on the order line item.If the action for the item is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/committed\_due\_date

</td></tr><tr id="externalProdInv-PATCH"><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-descr-PATCH">

Array of objects containing external ids to map to the product inventories created for the order. Data type: Array

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr id="externalProdInvId"><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-decsr">

External id to map to the product inventory.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_inventory\_id and sn\_prd\_invt\_product\_inventory/sn\_prd\_invt\_external\_id

</td></tr><tr id="productOrderItem_id-row-tmf622"><td>

productOrderItem.id

</td><td>

Required if the **productOrderItem** parameter is used. Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_id

Maximum length: 40

Default: Blank string

</td></tr><tr id="itemPrice-row-tmf622"><td>

productOrderItem.itemPrice

</td><td id="itemPrice-entry-tmf622">

Array of objects that describe the price associated with the product. Data type: Array

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Table updated: sn\_ind\_tmt\_orm\_order

Default: Blank string

</td></tr><tr id="itemPrice_price-row-tmf622"><td>

productOrderItem.itemPrice.price

</td><td id="itemPrice_price-entry-tmf622">

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

Default: Blank string

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

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="itemPrice_price_taxIncludedAmt_unit-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td id="itemPrice_price_taxIncludedAmt_unit-entry-tmf622">

Currency code in which the price is depicted. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr id="itemPrice_price_taxIncludedAmt_value-row-tmf622"><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td id="itemPrice_price_taxIncludedAmt_value-entry-tmf622">

Price of product, including any tax. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr id="itemPrice_priceType-row-tmf622"><td>

productOrderItem.itemPrice.priceType

</td><td id="itemPrice_priceType-entry-tmf622">

Type of item price, recurring or non-recurring. Data type: String

</td></tr><tr id="itemPrice_recurringChargePeriod-row-tmf622"><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td id="itemPrice_recurringChargePeriod-entry-tmf622">

If the price is recurring, the recurring period, such as `month`. Data type: String

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_id-row-tmf622"><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_place_id-row-tmf622"><td>

productOrderItem.product.place.id

</td><td>

Required if the **productOrderItem.product.place** parameter is used. Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/location

Default: Blank string

</td></tr><tr id="product_place_type-row-tmf622"><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr id="prod_prodChar-row-tmf622"><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr id="prod_prodChar_name-row-tmf622"><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associate with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristics

Default: Blank string

</td></tr><tr id="prod_prodChar_previousValue-row-tmf622"><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/previous\_characteristic\_option\_value

Default: Blank string

</td></tr><tr id="prod_prodChar_value-row-tmf622"><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristic\_option\_value

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="product_productSpecification_id-row-tmf622"><td>

productOrderItem.product.productSpecification.id

</td><td>

Required if the **productOrderItem.product.productSpecification** parameter is used. Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr id="product_productSpecification_name-row-tmf622"><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr id="product_productSpecification_type-row-tmf622"><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr id="product_relatedParty-row-tmf622"><td>

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr id="product_relatedParty_email-row-tmf622"><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/email

Default: Blank string

</td></tr><tr id="product_relatedParty_firstName-row-tmf622"><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/first\_name

Default: Blank string

</td></tr><tr id="product_relatedParty_id-row-tmf622"><td>

productOrderItem.product.relatedParty.id

</td><td>

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/sys\_id

Default: Blank string

</td></tr><tr id="product_relatedParty_lastName-row-tmf622"><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/lastName

Default: Blank string

</td></tr><tr id="product_relatedParty_phone-row-tmf622"><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/business\_phone

Default: Blank string

</td></tr><tr id="product_relatedParty_referredType-row-tmf622"><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr id="product_relatedParty_type-row-tmf622"><td>

productOrderItem.product.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr id="product_type-row-tmf622"><td>

productOrderItem.product.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `Product`. This information is not stored. Data type: String

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

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOffering_id-row-tmf622"><td>

productOrderItem.productOffering.id

</td><td>

Required if the **productOrderItem.productOffering** parameter is used. Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="productOffering_name-row-tmf622"><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="productOrdItem_quantity-row-tmf622"><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: null

</td></tr><tr id="productOrderItemRelationship-row-tmf622"><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOrderItemRelationship_id-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required if the **productOrderItem.productOrderItemRelationship** parameter is used. Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/parent\_line\_item

Default: Blank string

</td></tr><tr id="productOrderItemRelationship_relType-row-tmf622"><td>

productOrderItem.productOrderItemRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of items ordered.Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: Blank string

</td></tr><tr><td>

productOrderItem.revisionOperation

</td><td>

Type of update to perform on the line item. If this value is empty, the existing line item is updated, or a new line item is added if it does not already exist. If this value is `cancel`, the line item is canceled.Data type: String

Default: Blank string

</td></tr><tr><td>

productOrderItem.@type

</td><td id="prodOrdItem_type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr id="relatedParty-row-tmf622"><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

</td></tr><tr id="relatedParty_id-row-tmf622"><td>

relatedParty.id

</td><td>

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr id="relatedParty_name-row-tmf622"><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr id="relatedParty_referredType-row-tmf622"><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr id="relatedParty_type-row-tmf622"><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr id="requestedCompletionDate-row-tmf622"><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_end\_date

Default: Blank string

</td></tr><tr id="requestedStartDate-row-tmf622"><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_start\_date

Default: Blank string

</td></tr><tr><td>

@type

</td><td id="type-entry-tmf622">

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

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

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

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

List that describes items associated with the product order and their associated action. Data type: Array

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

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

 ```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

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

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

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

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

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

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Data type: String

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

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.type

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

 Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

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
    "state": "in_progress"
}
```

## Product Order Open API - POST /sn\_ind\_tmt\_orm/cancelproductorder

Cancels the specified customer order.

### URL format

Default URL: `/api/sn_ind_tmt_orm/cancelproductorder`

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

Required. Sys\_id of the customer order to cancel. Located in the Customer Order \[sn\_ind\_tmt\_orm\_order\] table.Data type: String

</td></tr><tr><td>

productOrder.href

</td><td>

URL of the customer order to cancel.Data type: String

 Default: Blank string

</td></tr><tr><td>

productOrder.@referredType

</td><td>

The value for this parameter should be `ProductOrder`.Data type: String

 Default: Blank string

</td></tr><tr><td>

requestedCancellationDate

</td><td>

Date to cancel the order.Data type: String

 Default: Blank string

</td></tr><tr><td>

@type

</td><td>

The value for this parameter should be `CancelProductOrder`.Data type: String

 Default: Blank string

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

Sys\_id of the cancelled order.Data type: String

</td></tr><tr><td>

productOrder.href

</td><td>

URL of the cancelled order.Data type: String

</td></tr><tr><td>

productOrder.@referredType

</td><td>

The value for this parameter is `ProductOrder`.Data type: String

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

The value for this parameter is `CancelProductOrder`.Data type: String

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

### URL format

Default URL: `/api/sn_ind_tmt_orm/order/productOrder`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mode

</td><td>

Enables asynchronous order processing.​ That is, the order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table to be created. If not included, the order is processed synchronously.Possible value: async

Data type: String

</td></tr></tbody>
</table><table id="id_vk2_p5n_t4b" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the **external\_id** field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/channel

Default: Blank string

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the **Choice List** tab in the **Channel Dictionary Entry** of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: Blank string

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-entry">

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

 Table/field updated: sn\_ind\_tmt\_orm\_order/committed\_due\_date

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/external\_id

Default: Blank string

</td></tr><tr id="productOrder-href-request"><td>

href

</td><td>

A relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

note

</td><td>

Array of objects that contain additional notes made by the customer when ordering. Data type: Array

```
"note": [
  {
    "text": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

note.text

</td><td>

Required. Additional notes/comments made by the customer while ordering. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/comments

Default: Blank string

</td></tr><tr><td>

orderCurrency

</td><td>

Required. Currency code for the order and order line items. The currency must be the same for all elements of the order and order line items, otherwise an error is returned and the order isn't created. Once an order is created, its currency code can't be changed. Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Required. Array of objects that describe items associated with the product order and their associated action. Data type: Array

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
    "@type": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="productOrder-addReason-request">

Optional. Description of the reason for the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-entry">

Date and time when the action must be performed on the order line item.

Data type: String

 Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/committed\_due\_date

</td></tr><tr id="externalProductInventory-GET-request"><td>

productOrderItem.externalProductInventory

</td><td id="externalProductInventory-GET-desc-request">

Array of objects containing external ids to map to the product inventories created for the order.Data type: Array of objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProductInventoryId-desc">

External id to map to the product inventory.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_inventory\_id and sn\_prd\_invt\_product\_inventory/sn\_prd\_invt\_external\_id

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_id

Maximum length: 40

Default: Blank string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Table updated: sn\_ind\_tmt\_orm\_order

Default: Blank string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

Default: Blank string

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

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, specifies the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/location

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristics

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/previous\_characteristic\_option\_value

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristic\_option\_value

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Required. Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

Array of objects that describe the party role linked to an OrderLineItemContact. Data type: Array

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/email

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/first\_name

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/lastName

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/business\_phone

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value – OrderLineItemContact

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

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. Array of objects that describe the parent/child relationship between order items. Data type: Array

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required. Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/parent\_line\_item

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: Blank string

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

Sys\_id or external\_id of the account or customer contact associated with the order. Located in either the account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Required. Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_end\_date

Default: Blank string

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_start\_date

Default: Blank string

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

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

Sys\_id of the customer order created for this request. Data type: String

</td></tr><tr><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

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

orderId

</td><td>

Sys\_id of the order to be created. Upon succussful request, the order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be processed.**Note:** This value is the only result if the order is created asynchronously using the **mode** query parameter.

```
{
 "orderId": "b0fc877ac3ab5110856d73ce3640dde0"
}
```

Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

List that describes items associated with the product order and their associated action. Data type: Array

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

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOrderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

productOrderItem.externalProductInventory

</td><td id="externalProdInv-resp-descr">

Array of objects containing external ids mapped to the product inventories created for the order. Data type: Array

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProdInvId-resp-descr">

External id mapped to the product inventory.Data type: String

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productRelationship

</td><td>

List of product relationship details for an order line item.Data type: Array

```
"productRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.product.productRelationship.id

</td><td>

Sys\_id or sn\_prd\_invt\_external\_id of the product inventory. Located in the sys\_id or sn\_prd\_invt\_external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productRelationship.relationshipType

</td><td>

Type of relationship between the order line item and the product inventory.Possible value: Requires

Data type: String

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

Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table. If both sys\_id and external\_id are present, the external\_id is returned.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalId

</td><td>

Initial\_version of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

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

Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. If both sys\_id and external\_id are present, the external\_id is returned.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalId

</td><td>

Initial\_version of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

</td></tr><tr><td>

productOrderItem.state

</td><td>

Current state of the product order item. This value is always `new`.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.type

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. For this endpoint, this value is always `new`.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

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
  "currencyCode": "USD",
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
  "currencyCode": "USD",
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

## Product Order Open API - POST /sn\_ind\_tmt\_orm/productorder

Creates the specified customer order and customer order line items.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Order Open API - POST /sn\_ind\_tmt\_orm/order/productOrder](tmf622_product_ordering-api.md#).

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

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

```
"channel": [
  {
    "id": "String",
    "name": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

channel.id

</td><td>

Required. Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the **external\_id** field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/channel

Default: Blank string

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Possible channel names are defined on the **Choice List** tab in the **Channel Dictionary Entry** of the sn\_ind\_tmt\_orm\_order table.Data type: String

Default: Blank string

</td></tr><tr><td>

committedDueDate

</td><td id="due-date-entry">

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

 Table/field updated: sn\_ind\_tmt\_orm\_order/committed\_due\_date

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the customer order. This value is determined by an external system. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/external\_id

Default: Blank string

</td></tr><tr id="productOrder-href-request"><td>

href

</td><td>

A relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

note

</td><td>

Array of objects that contain additional notes made by the customer when ordering. Data type: Array

```
"note": [
  {
    "text": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

note.text

</td><td>

Required. Additional notes/comments made by the customer while ordering. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/comments

Default: Blank string

</td></tr><tr><td>

orderCurrency

</td><td>

Required. Currency code for the order and order line items. The currency must be the same for all elements of the order and order line items, otherwise an error is returned and the order isn't created. Once an order is created, its currency code can't be changed. Data type: String

</td></tr><tr><td>

productOrderItem

</td><td>

Required. Array of objects that describe items associated with the product order and their associated action. Data type: Array

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
    "@type": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.action

</td><td>

Required. Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action

</td></tr><tr><td>

productOrderItem.actionReason

</td><td id="productOrder-addReason-request">

Optional. Description of the reason for the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.committedDueDate

</td><td id="due-date-item-entry">

Date and time when the action must be performed on the order line item.

Data type: String

 Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/committed\_due\_date

</td></tr><tr id="externalProductInventory-GET-request"><td>

productOrderItem.externalProductInventory

</td><td id="externalProductInventory-GET-desc-request">

Array of objects containing external ids to map to the product inventories created for the order.Data type: Array of objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

productOrderItem.externalProductInventory.externalProductInventoryId

</td><td id="externalProductInventoryId-desc">

External id to map to the product inventory.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_inventory\_id and sn\_prd\_invt\_product\_inventory/sn\_prd\_invt\_external\_id

</td></tr><tr><td>

productOrderItem.id

</td><td>

Required. Unique identifier of the line item. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_id

Maximum length: 40

Default: Blank string

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

```
"itemPrice": [
  {
    "price": {Object},
    "priceType": "String",
    "recurringChargePeriod": "String"
  }
]
```

Table updated: sn\_ind\_tmt\_orm\_order

Default: Blank string

</td></tr><tr><td>

productOrderItem.itemPrice.price

</td><td>

Description of the price of the associated product. Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

Default: Blank string

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

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.unit

</td><td>

Currency code in which the price is depicted. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr><td>

productOrderItem.itemPrice.price.taxIncludedAmount.value

</td><td>

Price of product, including any tax. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/mrc or nrc

</td></tr><tr><td>

productOrderItem.itemPrice.priceType

</td><td>

Specifies whether the price of the item is recurring or non-recurring. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice.recurringChargePeriod

</td><td>

If the price is recurring, specifies the recurring period, such as `month`. Data type: String

</td></tr><tr><td>

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.id

</td><td>

Required if **productOrderItem.action** is change or delete. Unique identifier of the product sold. Located in the sys\_id or sn\_ind\_tmt\_orm\_external\_id field of the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. Data type: String

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.place.id

</td><td>

Required. Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/location

</td></tr><tr><td>

productOrderItem.product.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.name

</td><td>

Name of the characteristic record to associated with the product. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristics

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/previous\_characteristic\_option\_value

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_characteristic\_value/characteristic\_option\_value

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.productSpecification

</td><td>

Required. Description of the product specification associated with the product. **Note:** Change orders \(**productOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property. The value of this system property determines how the order is processed if the product inventory is a different version than indicated in the order.

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.product.productSpecification.id

</td><td>

Required. Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

Array of objects that describe the party role linked to an OrderLineItemContact. Data type: Array

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

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact

</td></tr><tr><td>

productOrderItem.product.relatedParty.email

</td><td>

Email address of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/email

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/first\_name

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/lastName

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item\_contact/business\_phone

Default: Blank string

</td></tr><tr><td>

productOrderItem.product.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value – OrderLineItemContact

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

Required. Description of the product offering associated with the product. Data type: Object

```
"productOffering": {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String"
}
```

Table updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOffering.id

</td><td>

Required. Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: null

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Required. Array of objects that describe the parent/child relationship between order items. Data type: Array

```
"productOrderItemRelationship": [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship.id

</td><td>

Required. Same as the **productOrderItem.id** value. Used for parent/child relationship Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/parent\_line\_item

Default: Blank string

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

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

Default: Blank string

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

Sys\_id or external\_id of the account or customer contact associated with the order. Located in either the account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Required. Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_end\_date

Default: Blank string

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order/expected\_start\_date

Default: Blank string

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

channel

</td><td>

Array of objects that describe the channels to use for selling the products. Data type: Array

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

Unique identifier of the channel to use to sell the associated products. Channel ID values are located in the external\_id field of the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel to use to sell the associated products. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the customer order created for this request. Data type: String

</td></tr><tr><td>

externalId

</td><td>

External identifier for the customer order, such as a purchase order number.Data type: String

</td></tr><tr><td>

note

</td><td>

Array of objects that describe additional notes made by the customer when ordering. Data type: Array

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

List that describes items associated with the product order and their associated action. Data type: Array

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

productOrderItem.action

</td><td>

Action to carry out on the product. Possible actions are defined on the Choice List tab in the Action Dictionary Entry of the sn\_ind\_tmt\_orm\_order\_line\_item table. Data type: String

</td></tr><tr><td>

productOderItem.actionReason

</td><td>

The reason for adding the order line item.Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action\_reason

</td></tr><tr><td>

productOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

productOrderItem.itemPrice

</td><td>

Array of objects that describe the price associated with the product. Data type: Array

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

Sys\_id of the associated location record in the Location \[cmn\_location\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic

</td><td>

Array of objects that describe the characteristics of the associated product. Data type: Array

 ```
"productCharacteristic": [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String"
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

Previous characteristic option values if the update is for a change order. The request is a change order if the **productOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

</td></tr><tr><td>

productOrderItem.product.productCharacteristic.value

</td><td>

Characteristic option values associated with the product. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US). Data type: String

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

Initial\_version or external\_id of the product specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table. If both sys\_id and external\_id are present, the external\_id is returned.Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.name

</td><td>

Name of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

productOrderItem.product.productSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ProductSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

productOrderItem.product.relatedParty

</td><td>

List of contacts for line items. Data type: Array

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

Initial\_version or external\_id of the product offering. The initial\_version is the sys\_id of the first version of the offering. Located in the sys\_id or external\_id field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. If both sys\_id and external\_id are present, the external\_id is returned.Data type: String

</td></tr><tr><td>

productOrderItem.productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

productOrderItem.productOrderItemRelationship

</td><td>

Array of objects that describe the relationships between order line items. Data type: Array

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

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Data type: String

</td></tr><tr><td>

productOrderItem.quantity

</td><td>

Number of the associated items to order. Data type: Number

</td></tr><tr><td>

productOrderItem.state

</td><td>

Current state of the product order item. This value is always `new`.Data type: String

</td></tr><tr><td>

productOrderItem.@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. Must list at least one item which contains customer account or consumer account information. Data type: Array

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

Sys\_id or external\_id of the account, customer contact, or consumer associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.type

</td><td>

Type of customer. Possible values:

-   Consumer
-   Customer
-   CustomerContact

 Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the order. For this endpoint, this value is always `new`.Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of TMF Open API standard. Annotation for the product. This value is always `ProductOrder`. This information is not stored.Data type: String

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
            "value": "Base",
            "previousValue": "Advance"
          }
        ],
        "productSpecification": {
          "id": "39b627aa53702010cd6dddeeff7b1202",
          "name": "SD-WAN Edge Device",
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
                        "value": "Base",
                        "previousValue": "Advance"
                    }
                ],
                "productSpecification": {
                    "id": "39b627aa53702010cd6dddeeff7b1202",
                    "name": "SD-WAN Edge Device",
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

