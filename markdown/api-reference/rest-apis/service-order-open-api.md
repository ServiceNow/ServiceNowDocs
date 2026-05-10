---
title: Service Order Open API
description: The Service Order Open API provides endpoints that enable a standardized mechanism for placing service orders.Retrieves all service orders.Retrieves a specified service order.Updates the specified service order.Cancels the specified service order.Creates, updates, or deletes a service order or line item.Updates the fulfillment state for the specified domain order records in the Outbound Request \[sn\_tmt\_core\_outbound\_request\] table.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 70
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Service Order Open API

The Service Order Open API provides endpoints that enable a standardized mechanism for placing service orders.

This API is a ServiceNow® implementation of the TM Forum Service Ordering Management API specification. This implementation is based on the [TMF641 Service Ordering Management API User Guide v4.1.1](https://www.tmforum.org/resources/specifications/tmf641-service-ordering-management-api-user-guide-v4-1-1/), March 2021. The Service Order Open API is conformance certified by TM Forum

![TMF conformance logo](../image/tmf-conformance.png)

To access this API, the Order Management for Telecommunications \(sn\_ind\_tmt\_orm\) plugin must be activated. For more information, see [Install Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-install-providers.md). For information about Order Management tables and roles, see [Components installed with Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-with-order-management.md).

This API is provided within the `sn_tmf_api` namespace.

The calling user must have the sn\_ind\_tmt\_orm.order\_integrator role.

This API can be extended to make customizations around required parameters, request body validation, additional REST operations, and field mappings. For more information, see the [Service Order Open API Developer Guide](../../guides/telecom/concept/service-order_dev-guide.md#).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Service Order Open API – GET /sn\_tmf\_api/order/serviceOrder

Retrieves all service orders.

This API retrieves service order information from the following related tables:

-   Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic Value \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]
-   Order Line Related Items \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

### URL format

`/api/sn_tmf_api/order/serviceOrder`

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

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_abf_sn5_4sb"><thead><tr><th>

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

<table id="table_jlb_1qx_kqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Date on which the order is to be completed.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the requested service order.Data type: String

</td></tr><tr><td>

note

</td><td>

List of additional notes made by the customer when ordering. Data type: Array

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

orderDate

</td><td>

Date and timestamp of the order.Format: YYYY-MM-DD HH:MM:SS

Data type: String

Default: Blank string

</td></tr><tr><td>

ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: Point of no return for the order has been reached. The order can't be modified or canceled while fulfillment is in progress.
-   false: Point of no return for the order has not been reached. The order can be modified or canceled.

Data type: Boolean

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

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

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

serviceOrderItem

</td><td>

List of line items in the service order and their associated action. ```
"serviceOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "orderRelationship": [Array],
    "quantity": "Number",
    "place": {Object},   
    "ponr": Boolean,
    "relatedParty": {Object},   
    "service": {Object},
    "state": "String",
    "@type": "String",
    "version": "String"
  }
]
```

 Data type: Array

</td></tr><tr><td>

serviceOrderItem.action

</td><td>

Action to perform on the service order item. Possible actions are defined on the Choice List tab in the Action Dictionary Entry field of the sn\_ind\_tmt\_orm\_order\_line\_item table. For details, see [Action types for customer and service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-customer-order-types.md).

Data type: String

</td></tr><tr><td>

serviceOrderItem.actionReason

</td><td>

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

serviceOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

serviceOrderItem.externalProductInventory

</td><td>

List of external IDs mapped to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID mapped to the product inventory.Data type: String

</td></tr><tr><td>

serviceOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship

</td><td>

List of the relationships between order line items. Data type: Array

```
"orderRelationship:" [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.orderRelationship.id

</td><td>

Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

 Data type: String

</td></tr><tr><td>

serviceOrderItem.quantity

</td><td>

Number of line items ordered.Data type: Number

</td></tr><tr><td>

serviceOrderItem.place

</td><td>

Map of the locations on which to install the service.Data type: Object

```
"place:" {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.place.id

</td><td>

Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

</td></tr><tr><td>

serviceOrderItem.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.ponr

</td><td>

Flag that indicates whether the point of no return for the order line item has been reached.

 Valid values:

-   true: Point of no return for the order line item has been reached. The order line item can't be modified or canceled while fulfillment is in progress.
-   false: Point of no return for the order line item has not been reached. The order line item can be modified or canceled.

Data type: Boolean

</td></tr><tr><td>

serviceOrderItem.relatedParty

</td><td>

List of contacts for line items. Data type: Array

 ```
"relatedParty:" [
  {
    "email": "String",
    "firstName": "String"
    "id": "String",
    "lastName": "String",
    "phone": "String",
    "@referredType": "String",
    "@type": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.id

</td><td>

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

 Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service

</td><td>

Description of the instance details of the service purchased by the customer. Data type: Object

 ```
"service:" {
  "serviceCharacteristic": [Array],
  "serviceRelationship": [Array],
  "serviceSpecification": {Object},
  "serviceType": "String",
  "state": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic

</td><td>

List that describes the characteristics of the associated service. Only service characteristics with a current **value** different from the **previousValue** are returned.

 Data type: Array of Objects

 ```
"serviceCharacteristic:" [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.value

</td><td>

Characteristic option values associated with the service. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date, Address
-   Email
-   Integer, Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship

</td><td>

List of product inventories related to the service.Data type: Array of Objects

```
"serviceRelationship": [ 
  { 
    "id": "String", 
    "relationshipType": "String" 
  } 
] 
```

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.id

</td><td>

Sys\_id or sn\_prd\_invt\_external\_id of the product inventory.Data type: String

Table: In the sys\_id or sn\_prd\_invt\_external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.relationshipType

</td><td>

Type of relationship between the service and the product inventory. Possible value: Requires

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification

</td><td>

Description of the service specification associated with the service. Data type: Object

 ```
"serviceSpecification:" {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the sys\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalVersion

</td><td>

Version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.version

</td><td>

External\_version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceType

</td><td>

Service type.Data type: String

</td></tr><tr><td>

serviceOrderItem.service.state

</td><td>

State of the sold product. For example, new.Data type: String

</td></tr><tr><td>

serviceOrderItem.state

</td><td>

State of the service order item. For example, new.Data type: String

</td></tr><tr><td>

serviceOrderItem.version

</td><td>

Service order line item version.Data type: String

</td></tr><tr><td>

serviceOrderItem.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the service order. For more information, see[Service order states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/service-order-mgt-state-values.md).Data type: String

</td></tr><tr><td>

@type

</td><td id="type-entry-tmf641">

Part of the TMF Open API standard. This value is always `ServiceOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all service orders.

```
curl --location --request GET 'http://instance.service-now.com/api/sn_tmf_api/order/serviceOrder' \
--user 'username':'password'
```

Response body.

```
[
    {
        "id": "bd30366ec3a83010abc8b5183c40dd92",
        "ponr": "true",
        "href": "/api/sn_tmf_api/order/serviceOrder/bd30366ec3a83010abc8b5183c40dd92",
        "completionDate": "2021-06-07T21:52:12.000Z",
        "expectedCompletionDate": "2018-01-14T20:07:40.000Z",
        "orderDate": "2021-06-08T05:34:59.000Z",
        "requestedCompletionDate": "2018-01-14T20:07:40.000Z",
        "requestedStartDate": "2018-01-14T20:07:40.000Z",
        "serviceOrderItem": [
            {
                "id": "100",
                "ponr": "true",
                "quantity": 1,
                "action": "add",
                "service": {
                    "@type": "Service",
                    "id": "4b5072aec3a83010abc8b5183c40dd42",
                    "state": "active",
                    "serviceType": "cfs",
                    "serviceCharacteristic": [
                        {
                            "name": "Firewall coverage",
                            "valueType": "Choice",
                            "value": "Premium(Up to 50 sites)\n\t\t",
                            "previousValue": ""
                        },
                        {
                            "name": "Firewall Security",
                            "valueType": "choice",
                            "value": "Premium",
                            "previousValue": ""
                        },
                        {
                            "name": "CPE Type",
                            "valueType": "choice",
                            "value": "Physical",
                            "previousValue": ""
                        },
                        {
                            "name": "Administration Support",
                            "valueType": "choice",
                            "value": "Basic( Customer Managed)\n\t\t",
                            "previousValue": ""
                        }
                    ],
                    "serviceSpecification": {
                        "id": "f99546ff07266010a7955b7e0ad300a8",
                        "name": "Managed Firewall Service",
                        "version": "",
                        "internalVersion": "1",
                        "internalId": "f99546ff07266010a7955b7e0ad300a8",
                        "@type": "ServiceSpecificationRef"
                    }
                },
                "place": {
                    "id": "920cf6ac73d423002728660c4cf6a799",
                    "@type": "Place"
                },
                "state": "completed",
                "version": "2",
                "@type": "ServiceOrderItem"
            }
        ],
        "relatedParty": [
            {
                "id": "ffc68911c35420105252716b7d40dd55",
                "name": "Funco Intl",
                "@type": "RelatedParty",
                "@referredType": "Customer"
            },
            {
                "id": "eaf68911c35420105252716b7d40ddde",
                "name": "Sally Thomas",
                "@type": "RelatedParty",
                "@referredType": "CustomerContact"
            }
        ],
        "state": "completed",
        "version": "2",
        "@type": "ServiceOrder"
    }
]
```

## Service Order Open API – GET /sn\_tmf\_api/order/serviceOrder/\{id\}

Retrieves a specified service order.

This API retrieves service order information from the following related tables:

-   Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Characteristic Value \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]
-   Order Line Related Items \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

### URL format

`/api/sn_tmf_api/order/serviceOrder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the service order to retrieve.Data type: String

Table: Order \[sn\_ind\_tmt\_orm\_order\]

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

<table id="table_n5s_hjm_gqb"><thead><tr><th>

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

400

</td><td>

Bad request. Possible reasons:-   Missing query parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_jlb_1qx_kqb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Date on which the order is to be completed.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the requested service order.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

note

</td><td>

List of additional notes made by the customer when ordering. Data type: Array

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

orderDate

</td><td>

Date and timestamp of the order.Format: YYYY-MM-DD HH:MM:SS

Data type: String

Default: Blank string

</td></tr><tr><td>

ponr

</td><td>

Flag that indicates whether the point of no return for the order has been reached.Valid values:

-   true: Point of no return for the order has been reached. The order can't be modified or canceled while fulfillment is in progress.
-   false: Point of no return for the order has not been reached. The order can be modified or canceled.

Data type: Boolean

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

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

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

serviceOrderItem

</td><td>

List of line items in the service order and their associated action. Data type: Array

```
"serviceOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "orderRelationship": [Array],
    "quantity": "Number",
    "place": {Object},   
    "ponr": Boolean,
    "relatedParty": {Object},   
    "service": {Object},
    "state": "String",
    "@type": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.action

</td><td>

Action to perform on the service order item. Possible actions are defined on the Choice List tab in the Action Dictionary Entry field of the sn\_ind\_tmt\_orm\_order\_line\_item table. For details, see [Action types for customer and service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-customer-order-types.md)

Data type: String

</td></tr><tr><td>

serviceOrderItem.actionReason

</td><td>

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

serviceOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

serviceOrderItem.externalProductInventory

</td><td>

List of external IDs mapped to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID mapped to the product inventory.Data type: String

</td></tr><tr><td>

serviceOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship

</td><td>

List of the relationships between order line items. Data type: Array of Objects

```
"orderRelationship:" [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.orderRelationship.id

</td><td>

Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

serviceOrderItem.quantity

</td><td>

Number of line items ordered.Data type: Number

</td></tr><tr><td>

serviceOrderItem.place

</td><td>

Map of the locations on which to install the service.Data type: Object

```
"place:" {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.place.id

</td><td>

Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

</td></tr><tr><td>

serviceOrderItem.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.ponr

</td><td>

Flag that indicates whether the point of no return for the order line item has been reached.Valid values:

-   true: Point of no return for the order line item has been reached. The order line item can't be modified or canceled while fulfillment is in progress.
-   false: Point of no return for the order line item has not been reached. The order line item can be modified or canceled.

Data type: Boolean

</td></tr><tr><td>

serviceOrderItem.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" {
  "email": "String",
  "firstName": "String"
  "id": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.id

</td><td>

Sys\_id of the line item contact associated with the order line item. Located in the Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service

</td><td>

Description of the instance details of the service purchased by the customer. Data type: Object

```
"service:" {
  "serviceCharacteristic": [Array],
  "serviceRelationship": [Array],
  "serviceSpecification": {Object},
  "serviceType": "String",
  "state": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic

</td><td>

List that describes the characteristics of the associated service. Only service characteristics with a current **value** different from the **previousValue** are returned.

Data type: Array

```
"serviceCharacteristic:" [ 
  {
    "name": "String",
    "previousValue": "String",
    "value": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.value

</td><td>

Characteristic option values associated with the service. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date, Address
-   Email
-   Integer, Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship

</td><td>

List of product inventories related to the service.Data type: Array of Objects

```
"serviceRelationship": [ 
  { 
    "id": "String", 
    "relationshipType": "String" 
  } 
] 
```

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.id

</td><td>

Sys\_id or sn\_prd\_invt\_external\_id of the product inventory.Data type: String

Table: In the sys\_id or sn\_prd\_invt\_external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.relationshipType

</td><td>

Type of relationship between the service and the product inventory. Possible value: Requires

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification

</td><td>

Description of the service specification associated with the service. Data type: Object

```
"serviceSpecification:" {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the sys\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalVersion

</td><td>

Version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.version

</td><td>

External\_version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceType

</td><td>

Service type.Data type: String

</td></tr><tr><td>

serviceOrderItem.service.state

</td><td>

State of the sold product. For example, new.Data type: String

</td></tr><tr><td>

serviceOrderItem.state

</td><td>

State of the service order item. For example, new.Data type: String

</td></tr><tr><td>

serviceOrderItem.version

</td><td>

Service order line item version.Data type: String

</td></tr><tr><td>

serviceOrderItem.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the service order. For more information, see[Service order states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/service-order-mgt-state-values.md).Data type: String

</td></tr><tr><td>

@type

</td><td id="type-entry-tmf641">

Part of the TMF Open API standard. This value is always `ServiceOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example retrieves a specified service order.

```
curl "https://instance.service-now.com/api/sn_tmf_api/order/serviceOrder/4f2af65ac3a030106e2473ce3640ddcf" \
--request GET \
--user 'username':'password'
```

Response body.

```
{
   "id": "4f2af65ac3a030106e2473ce3640ddcf",
   "ponr": "false",
   "expectedCompletionDate": "2018-01-15T09:37:40.000Z",
   "requestedCompletionDate": "2018-01-15T09:37:40.000Z",
   "requestedStartDate": "2018-01-15T09:37:40.000Z",
   "note": [
      {
         "author": "System Administrator",
         "date": "2021-06-07T14:53:04.000Z",
         "text": "This is a TMF service order illustration no 2"
      },
      {
         "author": "System Administrator",
         "date": "2021-06-07T14:53:03.000Z",
         "text": "This is a TMF service order illustration"
      }
   ],
   "serviceOrderItem": [
      {
         "id": "100",
         "ponr": "false",
         "action": "add",
         "actionReason": "adding service package OLI",
         "quantity": 1,
         "service": {
            "@type": "Service",
            "state": "",
            "serviceType": "cfs",
            "serviceCharacteristic": [
               {
                  "name": "Firewall coverage",
                  "valueType": "Choice",
                  "value": "Premium (Up to 50 sites)",
                  "previousValue": ""
               },
               {
                  "name": "Firewall Security",
                  "valueType": "choice",
                  "value": "Standard",
                  "previousValue": ""
               },
               {
                  "name": "Administration Support",
                  "valueType": "choice",
                  "value": "Basic (Customer Managed)",
                  "previousValue": ""
               }
            ],
            "serviceRelationship": [
               {
                  "id": "326d13f45b5620102dff5e92dc81c785",
                  "relationshipType": "Requires"
               }
            ],
            "serviceSpecification": {
               "id": "f99546ff07266010a7955b7e0ad300a8",
               "name": "Managed Firewall Service",
               "version": "v2",
               "internalVersion": "2",
               "internalId": "f99546ff07266010a7955b7e0ad300a8",
               "@type": "ServiceSpecificationRef"
            }
         },
         "place": {
            "id": "920cf6ac73d423002728660c4cf6a799",
            "@type": "Place"
         },
         "relatedParty": [
            {
               "id": "972af65ac3a030106e2473ce3640ddda",
               "firstName": "Mike",
               "lastName": "Hudson",
               "email": "mike@example.com",
               "phone": "1234567890",
               "@type": "RelatedParty",
               "@referredType": "OrderLineItemContact"
            }
         ],
         "state": "new",
         "version": "1",
         "@type": "ServiceOrderItem"
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
   "state": "new",
   "version": "1",
   "@type": "ServiceOrder"
   "href": "/api/sn_tmf_api/order/serviceOrder/4f2af65ac3a030106e2473ce3640ddcfç",
   "orderDate": "2021-06-08T05:34:59.000Z",
}
```

## Service Order Open API - PATCH /sn\_tmf\_api/order/serviceOrder/\{id\}

Updates the specified service order.

### URL format

Default URL: `/api/sn_tmf_api/order/serviceOrder/{id}`

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

<table id="table_m32_1l1_hwb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.This value must be the same as or later than the **committedDueDate** values for each order line item.

If the action for order line items is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

externalId

</td><td>

Unique order number for the external service order. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

note

</td><td>

List of additional notes made by the customer when ordering. Data type: Array of Objects

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

Additional notes/comments made by the customer while ordering. Data type: String

Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Default: Blank string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. The request must list at least one item which contains customer account or consumer account information.Data type: Array

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

Required. Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Data type: String

Table: Account \[customer\_account\] table, Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\]

Table updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

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

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Stored in: The expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: Blank string

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Stored in: The expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: Blank string

</td></tr><tr><td>

serviceOrderItem

</td><td>

Required. List of line items in the service order and their associated action. Data type: Array of Objects

```
"serviceOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "orderRelationship": [Array],
    "place": {Object},
    "quantity": "Number",
    "relatedParty": {Object},
    "service": {Object},
    "@type": "String",
    "version": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

serviceOrderItem.action

</td><td>

Required. Action to perform on the service order item. Possible actions are defined on the Choice List tab in the Action Dictionary Entry field of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

For details, see [Action types for customer and service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-customer-order-types.md).

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action

</td></tr><tr><td>

serviceOrderItem.actionReason

</td><td>

Optional. Description of the reason for the line item. Data type: String

Table/field updated: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table/action\_reason.

</td></tr><tr><td>

serviceOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.If the action for the item is `suspend` or `resume`, this parameter can't be updated.

Data type: String

Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

serviceOrderItem.externalProductInventory

</td><td>

List of external IDs to map to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr><td>

serviceOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

serviceOrderItem.id

</td><td>

Required. Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_id

</td></tr><tr><td>

serviceOrderItem.orderRelationship

</td><td>

Required. List of relationships between order line items.Data type: Array of Objects

```
"orderRelationship:" [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOrderItemRelationship_id-row-tmf622"><td>

serviceOrderItem.orderRelationship.id

</td><td>

Required. Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/parent\_line\_item or sn\_ind\_tmt\_orm\_order\_line\_related\_items/related\_order\_line\_item

</td></tr><tr id="productOrderItemRelationship_relType-row-tmf622"><td>

serviceOrderItem.orderRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

serviceOrderItem.place

</td><td>

Map of the locations on which to install the service.Data type: Object

```
"place:" {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.place.id

</td><td>

Required. Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/location

</td></tr><tr><td>

serviceOrderItem.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item place.Data type: String

</td></tr><tr><td>

serviceOrderItem.quantity

</td><td>

Sets the number of line items to order.This property is only applicable when adding a service order; that is, the value of the **action** property is `add`.

Data type: Number

Default: Empty string

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

</td></tr><tr><td>

serviceOrderItem.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" {
  "email": "String",
  "firstName": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service

</td><td>

Required. Description of the instance details of the service purchased by the customer. Data type: Object

```
"service:" {
  "id": "String",
  "serviceCharacteristic": [Array],
  "serviceRelationship": [Array],
  "serviceSpecification": {Object},
  "@type": "String"
}
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

serviceOrderItem.service.id

</td><td>

Unique identifier of the service sold. This value can be the sys\_id or external ID in the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. This value is only used for change/disconnect orders.Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic

</td><td>

List that describes the characteristics of the associated service. Only service characteristics with a current **value** different from the **previousValue** are returned.

Data type: Array

```
"serviceCharacteristic:" [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic record to associated with the service. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **serviceOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.value

</td><td>

Characteristic option values associated with the service. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date, Address
-   Email
-   Integer, Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification

</td><td>

Required. Description of the service specification associated with the service. **Note:** Change orders \(**serviceOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property.

-   When the property is set to true \(default\), if the service is a different version than indicated in the order, the service is automatically upgraded to the version in the order by changing the referenced service specification. This allows the order to be successfully processed.
-   When the property is set to false, if the service is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

```
"serviceSpecification:" {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

Stored in: The service\_specification field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.id

</td><td>

Required. Initial\_version or external\_id of the service specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.name

</td><td>

Required. Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrderItem`. This information is not stored. Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrder`. This information is not stored.Data type: String

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

200

</td><td>

Successful. The request was successfully processed.

</td></tr><tr><td>

201

</td><td>

Successful. If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record:

-   `The following Order Item characteristics does not exist: Review specification <**specification.name**> and correct the characteristic and characteristic option in the order line item prior to approving the order.`
-   `Order Item characteristic: <**characteristic.name**> with characteristic value: <**characteristic.value**>is invalid. Correct the characteristic values before approving the order.`

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   `Invalid payload: Request body missing` - Payload was not passed in the request body.
-   `Invalid payload: serviceOrderItem is missing` - Service order line item object or JSON is missing.
-   `Invalid payload: serviceOrderItem id is missing` - The **id** parameter is missing in the service order line item of the payload.
-   `Invalid payload: serviceOrderItem action is missing` - The **action** parameter is missing in the service order line item of the payload.
-   `Invalid payload: serviceOrderItem serviceOffering is missing` - The service offering object or JSON is missing from the service order line item in the payload.
-   `Invalid payload: serviceOffering id is missing` - The **id** parameter is missing in the service order line item of the service offering object in the payload.
-   `Invalid payload: Service offering does not exist` - The service offering in the service order line item is not valid.
-   `Invalid payload: serviceOrderItem service is missing` - The service object or JSON in the service order line item is missing from the payload.
-   `Invalid payload: service serviceSpecification is missing` - The service specification object or JSON in the service order line item is missing from the payload.
-   `Invalid payload: serviceSpecification id is missing` - The **id** parameter in the service order line item of the service specification object is missing from the payload.
-   `Invalid payload: Service specification does not exist` - The service specification in the service order line item is not valid.
-   `Invalid payload: Service Inventory does not exist` - In a change order \(action = change\), the quantity of an item is greater than what is in stock.
-   `Invalid payload: Service inventory ID is missing` - In a change order, the **service.id** is missing in the payload.
-   `Invalid payload: Sold Service is inactive` - In a change order, a service specified in the payload is inactive.
-   `Invalid payload: relatedParty is missing` - The related party object is missing from the payload.
-   `Invalid payload: Customer Account or Consumer is missing` - The related party customer or consumer object is missing from the payload.
-   `Invalid payload: Customer Account does not exist` - The specified related party customer does not exist in the instance.
-   `Invalid payload: Consumer does not exist` - The specified related party consumer does not exist in the instance.
-   `Invalid payload: Order creation failed` - Not able to create the requested order.
-   `In-flight revision to order currency not supported` - The **orderCurrency** parameter can't be updated after the order is created.
-   `This order is yet to be created in customer order table. Please check in inbound queue for more details.` – The order ID provided is not in the customer order table.
-   `Patch request cannot be made as the order's fulfillment type is not 'deliver.` – The patch request was made on an order which has a fulfillment type other than deliver.

</td></tr><tr><td>

404

</td><td>

Not found. The requested item was not found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_t5s_hm1_hwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique order number for the external service order. Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service order.Data type: String

</td></tr><tr><td>

note

</td><td>

List of additional notes made by the customer when ordering. Data type: Array

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

orderDate

</td><td>

Date and timestamp of the order.Format: YYYY-MM-DD HH:MM:SS

Data type: String

Default: Blank string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

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

Sys\_id or external\_id of the account, customer or consumer contact associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Customer
-   CustomerContact
-   Consumer

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

serviceOrderItem

</td><td>

List of line items in the service order and their associated action. Data type: Array

```
"serviceOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "orderRelationship": [Array],
    "place": {Object},
    "quantity": "Number",
    "relatedParty": {Object},
    "service": {Object},
    "@type": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.action

</td><td>

Action to perform on the service order item. Possible actions are defined on the Choice List tab in the Action Dictionary Entry field of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete

For details, see [Action types for customer and service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-customer-order-types.md).

Data type: String

</td></tr><tr><td>

serviceOrderItem.actionReason

</td><td>

Reason for adding the order line item.Data type: String

Stored in: The action\_reason field of the sn\_ind\_tmt\_orm\_order\_line\_item table.

</td></tr><tr><td>

serviceOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

serviceOrderItem.externalProductInventory

</td><td>

List of external IDs to map to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

**Note:** Previously, when creating a PATCH order with an external product inventory ID that already existed, the operation was aborted and returned an error. With the Xanadu release, this parameter is simply ignored when an existing external product inventory ID is supplied and an error is not thrown.

</td></tr><tr><td>

serviceOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID mapped to the product inventory.Data type: String

</td></tr><tr><td>

serviceOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship

</td><td>

List of the relationships between order line items. Data type: Array

```
"orderRelationship:" [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.orderRelationship.id

</td><td>

Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

serviceOrderItem.place

</td><td>

Map of the locations on which to install the service.Data type: Object

```
"place:" {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.place.id

</td><td>

Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

</td></tr><tr><td>

serviceOrderItem.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.quantity

</td><td>

Number of line items ordered.Data type: Number

</td></tr><tr><td>

serviceOrderItem.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" {
  "email": "String",
  "firstName": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@referredType

</td><td>

Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service

</td><td>

Description of the instance details of the service purchased by the customer. Data type: Object

```
"service:" {
  "id": "String",
  "serviceCharacteristic": [Array],
  "serviceRelationship": [Array],
  "serviceSpecification": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.id

</td><td>

Unique identifier of the service sold. This value can be the sys\_id or external ID in the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. This value is only returned for change/disconnect orders.Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic

</td><td>

List that describes the characteristics of the associated service. Only service characteristics with a current **value** different from the **previousValue** are returned.

Data type: Array

```
"serviceCharacteristic:" [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic record to associated with the service. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **serviceOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.value

</td><td>

Characteristic option values associated with the service. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date, Address
-   Email
-   Integer, Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification

</td><td>

Description of the service specification associated with the service. Data type: Object

```
"serviceSpecification:" {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the service order. For more information, see[Service order states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/service-order-mgt-state-values.md).Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to update a service order.

```
curl -X PATCH 'https://instance.service-now.com/api/sn_tmf_api/order/serviceOrder/a831e56e77602110c8b3a4d54b5a9954' \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d '{
  "externalId": "BSS748",
  "priority": "1",
  "description": "Managed Security",
  "category": "TMF resource illustration",
  "requestedStartDate": "2018-01-15T09:37:40.508Z",
  "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
  "@type": "ServiceOrder",
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
  "serviceOrderItem": [
    {
      "id": "100",
      "action": "add",
      "actionReason":"adding service package OLI",
      "quantity": 1,
      "@type": "ServiceOrderItem",
      "service": {
        "serviceState": "active",
        "@type": "CFS",
        "serviceCharacteristic": [
          {
            "name": "CPE Type",
            "valueType": "Choice",
            "value": "Virtual"
          },
          {
            "name": "Administration Support",
            "valueType": "string",
            "value": "Basic( Customer Managed)"
          },
          {
            "name": "Firewall coverage",
            "valueType": "string",
            "value": "Standard(Up to 20 sites)"
          },
          {
            "name": "Firewall Security",
            "valueType": "string",
            "value": "Basic"
          }
        ],
        "serviceSpecification": {
          "id": "f99546ff07266010a7955b7e0ad300a8",
          "name": "Managed Firewall Service",
          "internalVersion": "1",
          "@type": "Managed Firewall Service"
        },
        "serviceRelationship": [
          {
            "id": "326d13f45b5620102dff5e92dc81c785",
            "relationshipType": "Requires"
          }
        ]
      },
      "place": {
        "id": "5671dd2ec3a53010188473ce3640dd81",
        "@type": "Place"
      }
    }
  ],
  "relatedParty":[
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
    ]
}'
```

Response body.

```
{
  "externalId": "BSS748",
  "priority": "1",
  "description": "Managed Security",
  "category": "TMF resource illustration",
  "requestedStartDate": "2018-01-15T09:37:40.508Z",
  "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
  "@type": "ServiceOrder",
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
  "serviceOrderItem": [
    {
      "id": "100",
      "action": "add",
      v"actionReason": "adding service package OLI",
      "quantity": 1,
      "@type": "ServiceOrderItem",
      "service": {
        "serviceState": "active",
        "@type": "CFS",
        "serviceCharacteristic": [
          {
            "name": "CPE Type",
            "valueType": "Choice",
            "value": "Virtual"
          },
          {
            "name": "Administration Support",
            "valueType": "string",
            "value": "Basic(Customer Managed)"
          },
          {
            "name": "Firewall coverage",
            "valueType": "string",
            "value": "Standard(Up to 20 sites)"
          },
          {
            "name": "Firewall Security",
            "valueType": "string",
            "value": "Basic"
          }
        ],
        "serviceSpecification": {
          "id": "f99546ff07266010a7955b7e0ad300a8",
          "name": "Managed Firewall Service",
          "internalVersion": "1",
          "@type": "Managed Firewall Service",
          "sys_id": "f99546ff07266010a7955b7e0ad300a8",
          "version": "",
          "status": "published",
          "internalId": "f99546ff07266010a7955b7e0ad300a8"
        },
        "serviceRelationship": [
          {
            "id": "326d13f45b5620102dff5e92dc81c785",
            "relationshipType": "Requires"
          }
        ]
      },
      "place": {
        "id": "5671dd2ec3a53010188473ce3640dd81",
        "@type": "Place"
      }
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
  "orderType": "add",
  "state": "revision_received",
  "href": "/api/sn_tmf_api/order/serviceOrder/a831e56e77602110c8b3a4d54b5a9954"
}
```

## Service Order Open API - POST /sn\_tmf\_api/order/serviceOrder/cancelserviceorder

Cancels the specified service order.

**Note:** This endpoint can't be used on orders for which the point of no return has been reached. An order line item can't be canceled while fulfillment is in progress.

### URL format

Default URL: `/api/sn_tmf_api/order/serviceOrder/cancelserviceorder`

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

serviceOrder

</td><td>

Data about the service order.Data type: Object

```
"serviceOrder": {
  "id": "String",
  "href": "String",
  "@referredType": "String"
}
```

</td></tr><tr><td>

serviceOrder.id

</td><td>

Required. Sys\_id of the customer order to cancel.Data type: String

Table: Customer Order \[sn\_ind\_tmt\_orm\_order\]

</td></tr><tr><td>

serviceOrder.href

</td><td>

URL of the customer order to cancel.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceOrder.@referredType

</td><td>

Value for this parameter should be `ServiceOrder`.Data type: String

Default: Blank string

</td></tr><tr><td>

requestedCancellationDate

</td><td>

Date to cancel the order.Data type: String

Default: Blank string

</td></tr><tr><td>

@type

</td><td>

Value for this parameter should be `CancelServiceOrder`.Data type: String

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

id

</td><td>

Sys\_id of the cancelled order.Data type: String

</td></tr><tr><td>

serviceOrder

</td><td>

Data about the service order.Data type: Object

```
"serviceOrder": {
  "id": "String",
  "@referredType": "String"
}
```

</td></tr><tr><td>

serviceOrder.id

</td><td>

Sys\_id of the cancelled order.Data type: String

</td></tr><tr><td>

serviceOrder.@referredType

</td><td>

Value for this parameter is `ServiceOrder`.Data type: String

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

Value for this parameter is `CancelServiceOrder`.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example cancels a customer order.

```
curl -X POST "https://instance.servicenow.com/api/sn_tmf_api/cancelserviceorder" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "cancellationReason": "Duplicate order",
  "requestedCancellationDate": "2023-01-24T11:56:21.931Z",
  "serviceOrder": {
    "id": "5f4f5e5377a311101fa5a4d54b5a99fd",
    "@referredType": "ServiceOrder"
  },
  "@type": "CancelServiceOrder"
}
```

```
{
  "id": "5f4f5e5377a311101fa5a4d54b5a99fd",
  "cancellationReason": "Duplicate order",
  "requestedCancellationDate": "2023-01-24T11:56:21.931Z",
  "@type": "CancelServiceOrder",
  "serviceOrder": {
    "id": "5f4f5e5377a311101fa5a4d54b5a99fd",
    "@referredType": "ServiceOrder"
  },
  "state": "done"
}
```

## Service Order Open API – POST /sn\_tmf\_api/order/serviceOrder

Creates, updates, or deletes a service order or line item.

When an add action is received and accepted, a new record is created in the following tables:

-   Order \[sn\_ind\_tmt\_orm\_order\]
-   Order Characteristic Value \[sn\_ind\_tmt\_orm\_order\_characteristic\_value\]
-   Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]
-   Order Line Item Contact \[sn\_ind\_tmt\_orm\_order\_line\_item\_contact\]
-   Order Line Related Items \[sn\_ind\_tmt\_orm\_order\_line\_related\_items\]

### URL format

`/api/sn_tmf_api/order/serviceOrder`

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

Enables asynchronous order processing.​ That is, the order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table to be created. If not included, the order is processed synchronously.Valid value: async

Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

committedDueDate

</td><td>

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

 Stored in: The committed\_due\_date field of the sn\_ind\_tmt\_orm\_order table.

</td></tr><tr><td>

externalId

</td><td>

Unique order number for the external service order. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

note

</td><td>

List of additional notes made by the customer when ordering. Data type: Array of Objects

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

Additional notes/comments made by the customer while ordering. Data type: String

Stored in: The comments field of the sn\_ind\_tmt\_orm\_order table.

Default: Blank string

</td></tr><tr><td>

orderDate

</td><td>

Date and timestamp of the order.Format: YYYY-MM-DD HH:MM:SS

Data type: String

Default: Blank string

</td></tr><tr><td>

relatedParty

</td><td>

List of contacts for the order. Each contact is an object in the array. The request must list at least one item which contains customer account or consumer account information.Data type: Array

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

Required. Sys\_id or external\_id of the account, customer contact, or consumer associated with the order.Data type: String

Table: Account \[customer\_account\] table, Contact \[customer\_contact\] table, or Consumer \[csm\_consumer\]

Table updated: sn\_ind\_tmt\_orm\_order

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Customer
-   CustomerContact
-   Consumer

 Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

Stored in: The expected\_end\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: Blank string

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

Stored in: The expected\_start\_date field of the sn\_ind\_tmt\_orm\_order table.

Default: Blank string

</td></tr><tr><td>

serviceOrderItem

</td><td>

Required. List of line items in the service order and their associated action. Data type: Array of Objects

```
"serviceOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "orderRelationship": [Array],
    "place": {Object},
    "quantity": "Number",
    "relatedParty": {Object},
    "service": {Object},
    "@type": "String",
    "version": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

serviceOrderItem.action

</td><td>

Required. Action to perform on the service order item. Possible actions are defined on the Choice List tab in the Action Dictionary Entry field of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

For details, see [Action types for customer and service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-customer-order-types.md).

Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/action

Default: add

</td></tr><tr><td>

ServiceOrderItem.actionReason

</td><td>

Optional. Description of the reason for the line item. Data type: String

Table/field updated: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table/action\_reason.

</td></tr><tr><td>

serviceOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

 Stored in: The committed\_due\_date field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

serviceOrderItem.externalProductInventory

</td><td>

External IDs to map to the product inventories created for the order.Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID to map to the product inventory.Data type: String

Stored in: The external\_inventory\_id field of the sn\_ind\_tmt\_orm\_order\_line\_item table and the sn\_prd\_invt\_external\_id field of the sn\_prd\_invt\_product\_inventory table.

</td></tr><tr><td>

serviceOrderItem.id

</td><td>

Required. Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/external\_id

</td></tr><tr><td>

serviceOrderItem.orderRelationship

</td><td>

Required. List of relationships between order line items.Data type: Array of Objects

```
"orderRelationship:" [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr id="productOrderItemRelationship_id-row-tmf622"><td>

serviceOrderItem.orderRelationship.id

</td><td>

Required. Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/parent\_line\_item or sn\_ind\_tmt\_orm\_order\_line\_related\_items/related\_order\_line\_item

</td></tr><tr id="productOrderItemRelationship_relType-row-tmf622"><td>

serviceOrderItem.orderRelationship.relationshipType

</td><td>

Required. Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

 Data type: String

</td></tr><tr><td>

serviceOrderItem.place

</td><td>

Map of the locations on which to install the service.Data type: Object

```
"place:" {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.place.id

</td><td>

Required. Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

 Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item/location

 Default: Blank string

</td></tr><tr><td>

serviceOrderItem.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item place.Data type: String

</td></tr><tr><td>

serviceOrderItem.quantity

</td><td>

Sets the number of line items to order.This property is only applicable when adding a service order; that is, the value of the **action** property is `add`.

Data type: Number

Default: Empty string

Table/field updated: sn\_ind\_tmt\_orm\_order/quantity

</td></tr><tr><td>

serviceOrderItem.relatedParty

</td><td>

List of contacts for line items. Data type: Array

 ```
"relatedParty:" {
  "email": "String",
  "firstName": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

 Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service

</td><td>

Required. Description of the instance details of the service purchased by the customer. Data type: Object

```
"service:" {
  "id": "String",
  "serviceCharacteristic": [Array],
  "serviceRelationship": [Array],
  "serviceSpecification": {Object},
  "@type": "String"
}
```

Table/field updated: sn\_ind\_tmt\_orm\_order\_line\_item

</td></tr><tr><td>

serviceOrderItem.service.id

</td><td>

Unique identifier of the service sold. This value can be the sys\_id or external ID in the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. This value is only used for change/disconnect orders.Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic

</td><td>

List that describes the characteristics of the associated service. Only service characteristics with a current **value** different from the **previousValue** are returned.

 Data type: Array

 ```
"serviceCharacteristic:" [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic record to associated with the service. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **serviceOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.value

</td><td>

Characteristic option values associated with the service. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date, Address
-   Email
-   Integer, Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship

</td><td>

List of product inventories related to the service.Data type: Array of Objects

```
"serviceRelationship": [ 
  { 
    "id": "String", 
    "relationshipType": "String" 
  } 
] 
```

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.id

</td><td>

Sys\_id or sn\_prd\_invt\_external\_id of the product inventory.Data type: String

Table: In the sys\_id or sn\_prd\_invt\_external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.relationshipType

</td><td>

Type of relationship between the service and the product inventory. Possible value: Requires

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification

</td><td>

Required. Description of the service specification associated with the service. **Note:** Change orders \(**serviceOrderItem.action** is `change`\) are processed differently based on the value of the **sn\_ind\_tmt\_orm.allowSpecVersionUpdateInChangeOrder** system property.

-   When the property is set to true \(default\), if the service is a different version than indicated in the order, the service is automatically upgraded to the version in the order by changing the referenced service specification. This allows the order to be successfully processed.
-   When the property is set to false, if the service is a different version than indicated in the order, the order fails due to the version mismatch.

Data type: Object

 ```
"serviceSpecification:" {
  "id": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

 Stored in: The service\_specification field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.id

</td><td>

Required. Initial\_version or external\_id of the service specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalVersion

</td><td>

Version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.name

</td><td>

Required. Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.version

</td><td>

External\_version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrderItem`. This information is not stored. Data type: String

</td></tr><tr><td>

@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_kmf_3jm_gqb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

201

</td><td>

Successful. If there are any issues with the characteristics or characteristics option information, the endpoint stores the following comments in the work notes fields of the associated Customer Order Line Item record:

-   The following Order Item characteristics does not exist: Review specification &lt;**specification.name**&gt; and correct the characteristic and characteristic option in the order line item prior to approving the order.
-   Order Item characteristic: &lt;**characteristic.name**&gt; with characteristic value: &lt;**characteristic.value**&gt; is invalid. Correct the characteristic values before approving the order.

</td></tr><tr><td>

202

</td><td>

Accepted. Successful request for an order in asynchronous mode. That is, the request was made with the **mode** parameter set to `async` and the record is scheduled to be processed in the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:-   Invalid payload: Consumer does not exist - The specified related party consumer does not exist in the instance.
-   Invalid payload: Customer Account does not exist. – The related party customer provided in payload is not present in the system.
-   Invalid payload: Customer Account or Consumer is missing - The related party customer or consumer object is missing from the payload.
-   Invalid payload: Order creation failed. - Not able to create the requested order.
-   Invalid payload: Product Inventory does not exist. - In a change or delete order \(i.e., action = change or delete\), the sold service sent is not present in the system.
-   Invalid payload: Product inventory ID is missing. – In a change or delete order, the Sold Product ID is missing from the payload.
-   Invalid payload: Request body missing. - Payload was not passed in the request body.
-   Invalid payload: serviceOrderItem action is missing. – The service object or JSON is missing from the payload.
-   Invalid payload: serviceOrderItem ID is missing. – The ID is missing from the service order line item.
-   Invalid payload: serviceOrderItem missing. - Service order line item object or JSON is missing.
-   Invalid payload: serviceOrderItem service is missing. – The service property is missing from the service order line item.
-   Invalid payload: Service specification does not exist. - The service specification in the service order line item is not valid.
-   Invalid payload: serviceSpecification ID is missing. - The **id** parameter in the service order line item of the service specification object is missing from the payload.
-   Invalid payload: serviceSpecification is missing. - The service specification object or JSON in the service order line item is missing from the payload.
-   Invalid payload: Sold Product is inactive. – In a change or delete order, the Sold Product sent in the payload is not in active state.

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

committedDueDate

</td><td>

Date and time when the action must be performed on the order.

This value must be the same as or later than the **committedDueDate** values for each order line item.

Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique order number for the external service order. Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service order.Data type: String

</td></tr><tr><td>

note

</td><td>

List of additional notes made by the customer when ordering. Data type: Array

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

orderDate

</td><td>

Date and timestamp of the order.Format: YYYY-MM-DD HH:MM:SS

Data type: String

Default: Blank string

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

relatedParty

</td><td>

List of contacts for the order.Data type: Array of Objects

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

Sys\_id or external\_id of the account, customer or consumer contact associated with the order. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the account, customer, or consumer. Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer. Possible values:

-   Customer
-   CustomerContact
-   Consumer

Data type: String

</td></tr><tr><td>

relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Delivery date requested by the customer. Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order start date requested by the customer. Data type: String

</td></tr><tr><td>

serviceOrderItem

</td><td>

List of line items in the service order and their associated action. Data type: Array

```
"serviceOrderItem:" [
  {
    "action": "String",
    "actionReason": "String",
    "committedDueDate": "String",
    "externalProductInventory": [Array],
    "id": "String",
    "orderRelationship": [Array],
    "place": {Object},
    "quantity": "Number",
    "relatedParty": {Object},
    "service": {Object},
    "@type": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.action

</td><td>

Action to perform on the service order item. Possible actions are defined on the Choice List tab in the Action Dictionary Entry field of the sn\_ind\_tmt\_orm\_order\_line\_item table. Possible values:

-   add
-   change
-   delete
-   no-change
-   resume
-   suspend

For details, see [Action types for customer and service orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-customer-order-types.md).

Data type: String

</td></tr><tr><td>

ServiceOrderItem.actionReason

</td><td>

Description of the reason for adding the line item.Data type: String

Table: Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\]

</td></tr><tr><td>

serviceOrderItem.committedDueDate

</td><td>

Date and time when the action must be performed on the order line item.

Data type: String

</td></tr><tr><td>

serviceOrderItem.externalProductInventory

</td><td>

List of external IDs mapped to the product inventories created for the order. Data type: Array of Objects

```
"externalProductInventory": [
  {
    "externalProductInventoryId": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.externalProductInventory.externalProductInventoryId

</td><td>

External ID mapped to the product inventory.Data type: String

</td></tr><tr><td>

serviceOrderItem.id

</td><td>

Unique identifier of the line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship

</td><td>

List of the relationships between order line items. Data type: Array

```
"orderRelationship:" [
  {
    "id": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

serviceOrderItem.orderRelationship.id

</td><td>

Unique identifier of the related line item. Located in the sn\_ind\_tmt\_orm\_external\_id field of the Order Line Item \[sn\_ind\_tmt\_orm\_order\_line\_item\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.orderRelationship.relationshipType

</td><td>

Type of relationship between the two line items. This information is used to identify the relationship hierarchy. Possible values:

-   HasChild
-   HasParent
-   Requires

`HasChild` and `HasParent` are used for parent/child relationships. `Requires` is used for horizontal relationships \(a line item requires another line item\).

Data type: String

</td></tr><tr><td>

serviceOrderItem.place

</td><td>

Map of the locations on which to install the service.Data type: Object

```
"place:" {
  "id": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.place.id

</td><td>

Sys\_id of the associated location record in the Location \[cmn\_location\] table. When employing the change action on a product order item \(via the**productOrderItem.action** parameter\), updating the request with a new place sys\_id creates a move order, where the order is not changed but is fulfilled in a new location. Data type: String

</td></tr><tr><td>

serviceOrderItem.place.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `Place`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.quantity

</td><td>

Number of line items ordered.Data type: Number

</td></tr><tr><td>

serviceOrderItem.relatedParty

</td><td>

List of contacts for line items. Data type: Array

```
"relatedParty:" {
  "email": "String",
  "firstName": "String",
  "lastName": "String",
  "phone": "String",
  "@referredType": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.relatedParty.email

</td><td>

Email address of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.firstName

</td><td>

First name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.lastName

</td><td>

Last name of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.phone

</td><td>

Business phone number of the contact. Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@referredType

</td><td>

Required. Type of customer. Possible value: OrderLineItemContact

Data type: String

</td></tr><tr><td>

serviceOrderItem.relatedParty.@type

</td><td>

Part of TMF Open API standard. Annotation for order line item contact. This value is always `RelatedParty`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.service

</td><td>

Description of the instance details of the service purchased by the customer. Data type: Object

```
"service:" {
  "id": "String",
  "serviceCharacteristic": [Array],
  "serviceRelationship": [Array],
  "serviceSpecification": {Object},
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.id

</td><td>

Unique identifier of the service sold. This value can be the sys\_id or external ID in the Product Inventory \[sn\_ind\_tmt\_orm\_product\_inventory\] table. This value is only returned for change/disconnect orders.Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic

</td><td>

List that describes the characteristics of the associated service. Only service characteristics with a current **value** different from the **previousValue** are returned.

Data type: Array

```
"serviceCharacteristic:" [ 
 {
  "name": "String",
  "previousValue": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.name

</td><td>

Name of the characteristic record to associated with the service. Located in the Characteristic \[sn\_prd\_pm\_characteristic\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.previousValue

</td><td>

Previous characteristic option values if the update is for change order. The request is a change order if the **serviceOrderItem.action** parameter is other than `add`. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.value

</td><td>

Characteristic option values associated with the service. For additional information on characteristic option values, see [Create product characteristics and characteristic options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-product-config-add-characteristics.md). Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceCharacteristic.valueType

</td><td>

Type of characteristic value.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date, Address
-   Email
-   Integer, Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship

</td><td>

List of product inventories related to the service.Data type: Array of Objects

```
"serviceRelationship": [ 
  { 
    "id": "String", 
    "relationshipType": "String" 
  } 
] 
```

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.id

</td><td>

Sys\_id or sn\_prd\_invt\_external\_id of the product inventory.Data type: String

Table: In the sys\_id or sn\_prd\_invt\_external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceRelationship.relationshipType

</td><td>

Type of relationship between the service and the product inventory. Possible value: Requires

Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification

</td><td>

Description of the service specification associated with the service. Data type: Object

```
"serviceSpecification:" {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "name": "String",
  "version": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. The initial\_version is the sys\_id of the first version of the specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the sys\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.internalVersion

</td><td>

Version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table. Data type: String

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.version

</td><td>

External\_version of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceOrderItem.service.serviceSpecification.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceSpecificationRef`. This information is not stored. Data type: String

</td></tr><tr><td>

serviceOrderItem.state

</td><td>

State of the service order item. For example, new.Data type: String

</td></tr><tr><td>

serviceOrderItem.@type

</td><td>

Part of the TMF Open API standard. This value is always `ServiceOrderItem`. This information is not stored.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the service order. For more information, see[Service order states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/service-order-mgt-state-values.md).Data type: String

</td></tr><tr><td>

@type

</td><td id="type-entry-tmf641">

Part of the TMF Open API standard. This value is always `ServiceOrder`. This information is not stored.Data type: String

</td></tr></tbody>
</table>### Processing asynchronously

This example shows how to use the **mode** query parameter to create an order asynchronously. The order is added to the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table on a schedule to be created.

```
curl -X POST 'https://instance.service-now.com/api/sn_tmf_api/serviceorder?mode=async' \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d '{
  "externalId": "BSS748",
  "priority": "1",
  "description": "Managed Security",
  "category": "TMF resource illustration",
  "requestedStartDate": "2018-01-15T09:37:40.508Z",
  "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
  "@type": "ServiceOrder",
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
  "serviceOrderItem": [
    {
      "id": "100",
      "action": "add",
      "actionReason":"adding service package OLI",
      "quantity": 1,
      "@type": "ServiceOrderItem",
      "service": {
        "serviceState": "active",
        "@type": "CFS",
        "serviceCharacteristic": [
          {
            "name": "CPE Type",
            "valueType": "string",
            "value": "Virtual"
          },
          {
            "name": "Administration Support",
            "valueType": "string",
            "value": "Basic( Customer Managed)"
          },
          {
            "name": "Firewall coverage",
            "valueType": "string",
            "value": "Standard(Up to 20 sites)"
          },
          {
            "name": "Firewall Security",
            "valueType": "string",
            "value": "Basic"
          }
        ],
        "serviceSpecification": {
          "id": "f99546ff07266010a7955b7e0ad300a8",
          "name": "Managed Firewall Service",
          "internalVersion": "1",
          "@type": "Managed Firewall Service"
        },
        "serviceRelationship": [
          {
            "id": "326d13f45b5620102dff5e92dc81c785",
            "relationshipType": "Requires"
          }
        ]
      },
      "place": {
        "id": "5671dd2ec3a53010188473ce3640dd81",
        "@type": "Place"
      }
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
    ]
}'
```

Response body.

```
{
  "orderId": "304e877ac3ab5110856d73ce3640dde5"
}
```

### Processing synchronously \(default\)

The following example shows how to create a service order by setting the **serviceOrderItem.action** property to `add`.

```
curl "https://instance.service-now.com/api/sn_tmf_api/serviceorder" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "externalId": "BSS748",
   "requestedStartDate": "2018-01-15T09:37:40.508Z",
   "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
   "@type": "ServiceOrder",
   "note": [
      {
         "text": "This is a TMF service order illustration"
      },
      {
         "text": "This is a TMF service order illustration no 2"
      }
   ],
   "serviceOrderItem": [
      {
         "id": "100",
         "action": "add",
         "actionReason":"adding service package OLI",
         "quantity": 1,
         "@type": "ServiceOrderItem",
         "service": {
            "@type": "CFS",
            "serviceCharacteristic": [
               {
                  "name": "Firewall Security",
                  "valueType": "Choice",
                  "value": "Standard",
               },
               {
                  "name": "Firewall coverage",
                  "value": "Premium (Up to 50 sites)"
               },
               {
                  "name": "Administration Support",
                  "value": "Basic (Customer Managed)"
               }
            ],
            "serviceRelationship": [
               {
                  "id": "326d13f45b5620102dff5e92dc81c785",
                  "relationshipType": "Requires"
               }
            ],
            "serviceSpecification": {
               "id": "f99546ff07266010a7955b7e0ad300a8",
               "name": "Managed Firewall Service",
               "@type": "Managed Firewall Service"
            }
         },
         "relatedParty": [
            {
               "firstName": "Mike",
               "lastName": "Hudson",
               "email": "mike@example.com",
               "phone": "1234567890",
               "@type": "RelatedParty",
               "@referredType": "OrderLineItemContact"
            }
         ],
         "place": {
            "id": "920cf6ac73d423002728660c4cf6a799",
            "@type": "Place"
         }
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
    ]
}" \
--user 'username':'password'
```

Response body:

```
{
   "externalId": "BSS748",
   "requestedStartDate": "2018-01-15T09:37:40.508Z",
   "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
   "@type": "ServiceOrder",
   "note": [
      {
         "text": "This is a TMF service order illustration"
      },
      {
         "text": "This is a TMF service order illustration no 2"
      }
   ],
   "serviceOrderItem": [
      {
         "id": "100",
         "action": "add",
         "actionReason":"adding service package OLI",
         "quantity": 1,
         "@type": "ServiceOrderItem",
         "service": {
            "@type": "CFS",
            "serviceCharacteristic": [
               {
                  "name": "Firewall Security",
                  "valueType": "Choice",
                  "value": "Standard"
               },
               {
                  "name": "Firewall coverage",
                  "value": "Premium (Up to 50 sites)"
               },
               {
                  "name": "Administration Support",
                  "value": "Basic (Customer Managed)"
               }
            ],
            "serviceRelationship": [
               {
                  "id": "326d13f45b5620102dff5e92dc81c785",
                  "relationshipType": "Requires"
               }
            ],
            "serviceSpecification": {
               "id": "f99546ff07266010a7955b7e0ad300a8",
               "name": "Managed Firewall Service",
               "@type": "Managed Firewall Service",
               "internalVersion": "2",
               "version": "v2",
               "internalId": "f99546ff07266010a7955b7e0ad300a8"
            }
         },
         "relatedParty": [
            {
               "firstName": "Mike",
               "lastName": "Hudson",
               "email": "mike@example.com",
               "phone": "1234567890",
               "@type": "RelatedParty",
               "@referredType": "OrderLineItemContact"
            }
         ],
         "place": {
            "id": "920cf6ac73d423002728660c4cf6a799",
            "@type": "Place"
         },
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
   "id": "4f2af65ac3a030106e2473ce3640ddcf",
   "href": "/api/sn_tmf_api/order/serviceOrder/4f2af65ac3a030106e2473ce3640ddcf",
   "orderDate": "2024-06-20T10:38:55.000Z",
   "state": "new"
}
```

### cURL request

The following example updates a service order by setting the **serviceOrderItem.action** property to `change`.

```
curl "https://instance.service-now.com/api/sn_tmf_api/serviceorder" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "externalId": "BSS748",
   "requestedStartDate": "2018-01-15T09:37:40.508Z",
   "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
   "@type": "ServiceOrder",
   "note": [
      {
         "text": "This is a TMF service order illustration"
      },
      {
         "text": "This is a TMF service order illustration no 2"
      }
   ],
   "serviceOrderItem": [
      {
         "id": "100",
         "action": "change",
         "actionReason":"change service package OLI",
         "@type": "ServiceOrderItem",
         "service": {
            "@type": "CFS",
            "serviceCharacteristic": [
               {
                  "name": "Firewall Security",
                  "valueType": "Choice",
                  "value": "Premium",
                  "previousValue": "Standard"
               }
            ],
            "id": "4b5072aec3a83010abc8b5183c40dd42"
         },
         "relatedParty": [
            {
               "firstName": "Mike",
               "lastName": "Hudson",
               "email": "mike@example.com",
               "phone": "1234567890",
               "@type": "RelatedParty",
               "@referredType": "OrderLineItemContact"
            }
         ],
         "place": {
            "id": "920cf6ac73d423002728660c4cf6a799",
            "@type": "Place"
         }
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
    ]
}" \
--user 'username':'password'
```

Response body.

```
{
   "externalId": "BSS748",
   "requestedStartDate": "2018-01-15T09:37:40.508Z",
   "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
   "@type": "ServiceOrder",
   "note": [
      {
         "text": "This is a TMF service order illustration"
      },
      {
         "text": "This is a TMF service order illustration no 2"
      }
   ],
   "serviceOrderItem": [
      {
         "id": "100",
         "action": "change",
         "actionReason":"change service package OLI",
         "@type": "ServiceOrderItem",
         "service": {
            "@type": "CFS",
            "serviceCharacteristic": [
               {
                  "name": "Firewall Security",
                  "valueType": "Choice",
                  "value": "Premium",
                  "previousValue": "Standard"
               }
            ],
            "id": "4b5072aec3a83010abc8b5183c40dd42"
         },
         "relatedParty": [
            {
               "firstName": "Mike",
               "lastName": "Hudson",
               "email": "mike@example.com",
               "phone": "1234567890",
               "@type": "RelatedParty",
               "@referredType": "OrderLineItemContact"
            }
         ],
         "place": {
            "id": "920cf6ac73d423002728660c4cf6a799",
            "@type": "Place"
         },
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
   "id": "4f2af65ac3a030106e2473ce3640ddcf",
   "href": "/api/sn_tmf_api/order/serviceOrder/4f2af65ac3a030106e2473ce3640ddcf",
   "orderDate": "2024-06-20T10:38:55.000Z",
   "state": "new"
}
```

### cURL request

The following example deletes a service order line item by setting the **serviceOrderItem.action** property to `delete`.

```
curl "https://instance.service-now.com/api/sn_tmf_api/serviceorder" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "externalId": "BSS748",
   "requestedStartDate": "2018-01-15T09:37:40.508Z",
   "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
   "@type": "ServiceOrder",
   "note": [
      {
         "text": "This is a TMF service order illustration"
      },
      {
         "text": "This is a TMF service order illustration no 2"
      }
   ],
   "serviceOrderItem": [
      {
         "id": "100",
         "action": "delete",
         "actionReason":"delete service package OLI",
         "@type": "ServiceOrderItem",
         "service": {
            "@type": "CFS",
            "serviceCharacteristic": [
               {
                  "name": "Firewall Security",
                  "valueType": "Choice",
                  "value": "Premium",
                  "previousValue": "Standard"
               }
            ],
            "id": "4b5072aec3a83010abc8b5183c40dd42"
         },
         "relatedParty": [
            {
               "firstName": "Mike",
               "lastName": "Hudson",
               "email": "mike@example.com",
               "phone": "1234567890",
               "@type": "RelatedParty",
               "@referredType": "OrderLineItemContact"
            }
         ],
         "place": {
            "id": "920cf6ac73d423002728660c4cf6a799",
            "@type": "Place"
         }
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
    ]
}" \
--user 'username':'password'
```

Response body.

```
{
   "externalId": "BSS748",
   "requestedStartDate": "2018-01-15T09:37:40.508Z",
   "requestedCompletionDate": "2018-01-15T09:37:40.508Z",
   "@type": "ServiceOrder",
   "note": [
      {
         "text": "This is a TMF service order illustration"
      },
      {
         "text": "This is a TMF service order illustration no 2"
      }
   ],
   "serviceOrderItem": [
      {
         "id": "100",
         "action": "delete",
         "actionReason":"delete service package OLI",
         "@type": "ServiceOrderItem",
         "service": {
            "@type": "CFS",
            "serviceCharacteristic": [
               {
                  "name": "Firewall Security",
                  "valueType": "Choice",
                  "value": "Premium",
                  "previousValue": "Standard"
               }
            ],
            "id": "4b5072aec3a83010abc8b5183c40dd42"
         },
         "relatedParty": [
            {
               "firstName": "Mike",
               "lastName": "Hudson",
               "email": "mike@example.com",
               "phone": "1234567890",
               "@type": "RelatedParty",
               "@referredType": "OrderLineItemContact"
            }
         ],
         "place": {
            "id": "920cf6ac73d423002728660c4cf6a799",
            "@type": "Place"
         },
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
   "id": "4f2af65ac3a030106e2473ce3640ddcf",
   "href": "/api/sn_tmf_api/order/serviceOrder/4f2af65ac3a030106e2473ce3640ddcf",
   "orderDate": "2024-06-20T10:38:55.000Z",
   "state": "new"
}
```

## Service Order Open API – POST /sn\_tmf\_api/order/serviceOrder/outboundresponse

Updates the fulfillment state for the specified domain order records in the Outbound Request \[sn\_tmt\_core\_outbound\_request\] table.

To use this method, the Outbound Request table must contain the specified domain order record. Also, the method validation throws an error if the records or states specified in the request body are not located in the existing outbound record.

**Note:** You can't create new records in this table using this endpoint.

For additional information on domain orders, see [Install Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-install-providers.md).

### URL format

`/api/sn_tmf_api/order/serviceOrder/outboundresponse`

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

externalId

</td><td>

Required. Outbound request identifier of the domain orders record sent for fulfillment.Data type: String

Table: In the request\_id field in the Outbound Request \[sn\_tmt\_core\_outbound\_request\] table.

</td></tr><tr><td>

ServiceOrderItem

</td><td>

Required. List of domain orders whose external fulfillment state needs to be updated. Data type: Array of Objects

```
"ServiceOrderItem": [
  {
    "id": "String",
    "state": "String"
  }
]
```

</td></tr><tr><td>

ServiceOrderItem.id

</td><td>

Required. Sys\_id of a domain order record for which to update the external fulfillment state.Data type: String

Table: Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\]

</td></tr><tr><td>

ServiceOrderItem.state

</td><td>

Required. External fulfillment state of the domain order.Valid values:

-   error
-   fulfilled
-   pending

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

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

Bad Request. Could be any of the following reasons:-   `Invalid payload: externalId is missing`: Indicates that the external ID \(**externalId**\) was not passed.
-   `Invalid payload: serviceOrderItem state is missing:` Indicates that the external fulfillment state \(**ServiceOrderItem.state**\) was not passed in one or more domain orders.
-   `Invalid external id. Please pass the correct external id`: Indicates that the passed external ID \(**externalId**\) is not present in system.
-   `Invalid domain order id. Please pass the correct domain order id`: Indicates that the passed domain order ID \(**ServiceOrderItem.id**\) is not present in the system.
-   `Domain order id passed is not associated with external id`: Indicates that the external ID \(**externalId**\) is not associated with any domain orders. The system only updates domain orders that are associated with an external ID passed in the payload.
-   `Invalid fulfilment state: Please provide correct fulfilment state`: Indicates that the passed fulfilment state \(**ServiceOrderItem.state**\) for one or more domain orders is not valid.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_y44_214_21c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

externalId

</td><td>

Outbound request identifier of the domain orders record sent for fulfillment.Data type: String

Table: In the request\_id field in the Outbound Request \[sn\_tmt\_core\_outbound\_request\] table.

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

orderDate

</td><td>

Date and timestamp of the order.Format: YYYY-MM-DD HH:MM:SS

Data type: String

Default: Blank string

</td></tr><tr><td>

ServiceOrderItem

</td><td>

List of domain orders whose external fulfillment state needs to be updated. Data type: Array of Objects

```
"ServiceOrderItem": [
  {
    "id": "String",
    "state": "String"
  }
]
```

</td></tr><tr><td>

ServiceOrderItem.id

</td><td>

Sys\_id of a domain order record for which to update the external fulfillment state.Data type: String

Table: Domain Order \[sn\_ind\_tmt\_orm\_domain\_order\]

</td></tr><tr><td>

ServiceOrderItem.state

</td><td>

External fulfillment state of the domain order.Possible values:

-   error
-   fulfilled
-   pending

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/serviceorder/outboundresponse" \ 
--request POST \
--header "Accept:application/json" \
--data "{ 
  "externalId": "607017d243322110461f99612bb8f25c",
  "serviceOrderItem": [
    {
      "id": "19913c3577b301108e191e599a5a9988",
      "state": "error"
    }
  ]
}"
--user 'username':'password'
```

Response:

```
{
  "externalId": "607017d243322110461f99612bb8f25c",
  "serviceOrderItem": [
    {
      "id": "19913c3577b301108e191e599a5a9988",
      "state": "error"
    }
  ]
}
```

