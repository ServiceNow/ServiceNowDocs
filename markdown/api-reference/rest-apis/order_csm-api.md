---
title: Order API
description: The Order API provides endpoints for retrieving and creating orders with order line items for the Customer Service Management application.Retrieves complete order details by specifying the sys\_id or order number.Creates a new order with line items and characteristics.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-11-21"
reading_time_minutes: 26
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Order API

The Order API provides endpoints for retrieving and creating orders with order line items for the Customer Service Management application.

This API requires the Order Management \(app-csm-order-mgmt\) store application and is provided within the `sn_ind_tmt_orm` namespace. For information, see [Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).

This API requires sn\_csm\_om.order\_integrator for access, and one of the following:

-   sn\_csm\_om.consumer\_agent – API write access restricted to B2C orders.
-   sn\_csm\_om.customer\_agent – API write access restricted to B2B orders.
-   sn\_csm\_om.order\_admin – API write access for B2B or B2C orders.

For information on B2B and B2C orders, see [Customer Data Models for B2B2C](https://www.servicenow.com/docs/access?context=customer-data-model-b2b2c&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Order API – GET /sn\_ind\_tmt\_orm/order/\{id\}

Retrieves complete order details by specifying the sys\_id or order number.

### URL format

Versioned URL: `/api/sn_ind_tmt_orm/{api_version}/order/{id}`

Default URL: `/api/sn_ind_tmt_orm/order/{id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or order number \(order\_id\) of the record to retrieve located in the Orders \[sn\_csm\_om\_order\] table.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_display\_value

</td><td>

Flag that indicates whether to show the display value of the reference fields.

 Valid values:

-   true: Show the display value of the reference fields, choice fields, and date field in the response.
-   false: Show the actual value of the reference fields, choice fields, and date field in the response.

 Default: false

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

401

</td><td>

The user is not authenticated.

</td></tr><tr><td>

403

</td><td>

The user is not authorized.-   The user does not have required roles to access the API.
-   The user does not have authorization to read the order.

 This API requires sn\_csm\_om.order\_integrator for access, and one of the following:

-   sn\_csm\_om.consumer\_agent – API write access restricted to B2C orders.
-   sn\_csm\_om.customer\_agent – API write access restricted to B2B orders.
-   sn\_csm\_om.order\_admin – API write access for B2B or B2C orders.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

account

</td><td>

Sys\_id of a record located in the Accounts \[customer\_account\] table. Identifies the account for B2B orders.Data type: String

</td></tr><tr><td>

actual\_end\_date

</td><td>

End date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

actual\_start\_date

</td><td>

Start date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

billing\_city

</td><td>

Name of the billing city.Data type: String

</td></tr><tr><td>

billing\_country

</td><td>

Abbreviation of the billing country.Data type: String

</td></tr><tr><td>

billing\_state

</td><td>

Abbreviation of the billing state or province.Data type: String

</td></tr><tr><td>

billing\_street

</td><td>

Billing street address.Data type: String

</td></tr><tr><td>

billing\_zip

</td><td>

Billing ZIP or postal code.Data type: String

</td></tr><tr><td>

comments

</td><td>

Additional information for the order.Data type: String

</td></tr><tr><td>

consumer

</td><td>

Sys\_id of a record located in the Consumers \[csm\_consumer\] table. Identifies the consumer for B2C orders.Data type: String

</td></tr><tr><td>

contact

</td><td>

Sys\_id of the customer contact related to the account. Listed in the Contacts \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

contract

</td><td>

Sys\_id of the Customer Service contract listed in the Contracts \[ast\_contract\] table.Data type: String

</td></tr><tr><td>

error

</td><td>

Details describing an error encountered during the request process.Data type: Object

 ```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. Each error message has a corresponding description in the **detail** property.Data type: String

</td></tr><tr><td>

expected\_end\_date

</td><td>

Expected end date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

expected\_start\_date

</td><td>

Expected start date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

external\_id

</td><td>

External ID representing a related record on a third party's system. Data type: String

</td></tr><tr><td>

external\_system

</td><td>

Name of the customer's system. Data type: String

</td></tr><tr><td>

order\_category

</td><td>

Customer order type.Possible values:

-   product
-   service

 Data type: String

</td></tr><tr><td>

order\_currency

</td><td>

Currency code representing the currency in which the order was purchased. For example, `USD` for United States Dollars. This currency is used for all amount fields in the order and line orders. Currency codes are listed in the Currencies \[fx\_currency\] table. **Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_date

</td><td>

Date and time of order creation.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

order\_id

</td><td>

Order number of the order listed in the Orders \[sn\_csm\_om\_order\] table.Data type: String

</td></tr><tr><td>

order\_line\_items

</td><td>

Required. List of objects that define each order line item in the order. Located in the Order Line Items \[sn\_csm\_om\_order\_line\_item\] table. Data type: Array

 Required properties in each order line item object:

-   **account** for B2B orders or **consumer** for B2C orders.
-   **product\_offering** –
-   **quantity**
-   **unit\_of\_measurements**
-   **order\_line\_characteristics**

 ```
"order_line_items": [
 {
   "account": "String",
   "action": "String",
   "comments": "String",
   "consumer": "String",
   "contact": "String",
   "delivered_quantity": "String",
   "effective_date": "String",
   "expiration_date": "String",
   "external_id": "String",
   "external_system": "String",
   "list_price": "String",
   "location": "String",
   "order_line_characteristics": [Array],
   "order_line_id": "String",
   "order": "String",
   "parent_line_item": "String",
   "previous_product_model": "String",
   "price_list": "String",
   "product_offering": "String",
   "product_specification": "String",
   "product": "String",
   "quantity": "String",
   "shipping_city": "String",
   "shipping_country": "String",
   "shipping_state": "String",
   "shipping_street": "String",
   "shipping_zip": "String",
   "short_description": "String",
   "sku": "String",
   "sold_product": "String",
   "specification": "String",
   "state": "String",
   "status": "String",
   "sys_class_name": "String",
   "sys_created_by": "String",
   "sys_created_on": "String",
   "sys_id": "String",
   "sys_mod_count": "String",
   "sys_tags": "String",
   "sys_updated_by": "String",
   "sys_updated_on": "String",
   "top_line_item": "String",
   "total_price": "String",
   "unit_of_measurement": "String",
   "unit_price": "String",
   "work_notes": "String"
 }
]
```

</td></tr><tr><td>

order\_line\_items

</td><td>

List of objects that define each order line item in the order. Located in the Order Line Items \[sn\_csm\_om\_order\_line\_item\] table. Data type: Array

 ```
"order_line_items": [
 {
   "account": "String",
   "action": "String",
   "comments": "String",
   "consumer": "String",
   "contact": "String",
   "delivered_quantity": "String",
   "effective_date": "String",
   "expiration_date": "String",
   "external_id": "String",
   "external_system": "String",
   "list_price": "String",
   "location": "String",
   "order_line_characteristics": [Array],
   "order_line_id": "String",
   "order": "String",
   "parent_line_item": "String",
   "previous_product_model": "String",
   "price_list": "String",
   "product_offering": "String",
   "product_specification": "String",
   "product": "String",
   "quantity": "String",
   "shipping_city": "String",
   "shipping_country": "String",
   "shipping_state": "String",
   "shipping_street": "String",
   "shipping_zip": "String",
   "short_description": "String",
   "sku": "String",
   "sold_product": "String",
   "specification": "String",
   "state": "String",
   "status": "String",
   "sys_class_name": "String",
   "sys_created_by": "String",
   "sys_created_on": "String",
   "sys_id": "String",
   "sys_mod_count": "String",
   "sys_tags": "String",
   "sys_updated_by": "String",
   "sys_updated_on": "String",
   "top_line_item": "String",
   "total_price": "String",
   "unit_of_measurement": "String",
   "unit_price": "String",
   "work_notes": "String"
 }
]
```

</td></tr><tr><td>

order\_line\_items.account

</td><td>

Required for B2B orders. Sys\_id of the business account assigned to this order line item. Located in the Accounts \[customer\_account\] table. The consumer property is required for B2C orders.Data type: String

</td></tr><tr><td>

order\_line\_items.account

</td><td>

Sys\_id of the business account assigned to this order line item. Located in the Accounts \[customer\_account\] table. Data type: String

</td></tr><tr><td>

order\_line\_items.action

</td><td>

Action that determines how the order line is added to the order.Possible values:

-   add
-   change

 Data type: String

</td></tr><tr><td>

order\_line\_items.comments

</td><td>

Additional information for the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.consumer

</td><td>

Sys\_id of the consumer assigned to this order line item. Located in the Consumers \[csm\_consumer\] table. Data type: String

</td></tr><tr><td>

order\_line\_items.contact

</td><td>

Contact sys\_id related to the account.Data type: String

</td></tr><tr><td>

order\_line\_items.delivered\_quantity

</td><td>

Number of items in the order delivered.Data type: String

</td></tr><tr><td>

order\_line\_items.effective\_date

</td><td>

Effective date of order line.Format: yyyy-MM-dd HH:mm:ss in UTC time zone

 Data type: String

</td></tr><tr><td>

order\_line\_items.expiration\_date

</td><td>

Expiration date of order line.Format: yyyy-MM-dd HH:mm:ss in UTC time zone

 Data type: String

</td></tr><tr><td>

order\_line\_items.external\_id

</td><td>

External ID of the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.external\_system

</td><td>

External sys\_id of the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.list\_price

</td><td>

List price of the product offering per unit.**Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.location

</td><td>

Sys\_id of a shipping location listed in the Locations \[cmn\_location\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.order

</td><td>

This line item's order number as listed in the Orders \[sn\_csm\_om\_order\] table.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics

</td><td>

List of objects defining associated order line characteristics. Order line characteristics are located in the Order Line Characteristics \[sn\_csm\_om\_order\_characteristic\_value\] table. ```
"order_line_characteristics": [
 {
  "characteristic": "String",
  "characteristic_option": "String"
 }
]
```

 Data type: Array

</td></tr><tr><td>

order\_line\_items.​order\_line\_characteristics.​characteristic\_option

</td><td>

Product characteristic unique option that triggers the exclusion rule. For example, product size or color.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. characteristic\_option\_value

</td><td>

Value of a characteristic option.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. external\_id

</td><td>

External ID of the order line characteristic.Data type: Object

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. number

</td><td>

Order line characteristic number listed in the Order Line Characteristics \[sn\_csm\_om\_order\_characteristic\_value\] table.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. order\_line\_item

</td><td>

Sys\_id of this characteristic's order line item in the Order Line Items \[sn\_csm\_om\_order\_line\_item\] table.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. previous\_characteristic\_option\_value

</td><td>

Name of the previous characteristic option associated with product model in the order line.Data type: Object

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics.specification

</td><td>

Service specification that is associated with the service order characteristic.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_class\_name

</td><td>

System name of the table in which this order line characteristic record is located.Data type: String

</td></tr><tr><td>

order\_line\_characteristics. sys\_created\_by

</td><td>

System name of the user who created this record.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_created\_on

</td><td>

Date and time at which the record was originally created.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_domain

</td><td>

Domain scope in which the order record is accessible. For example, global.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_domain\_path

</td><td>

Domain path for the record.Data type: String

 Default: / \(global\)

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_id

</td><td>

Sys\_id of the order record located in the Order Line Characteristics \[sn\_csm\_om\_order\_characteristic\_value\] table.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_mod\_count

</td><td>

Number of times this record has been modified.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_tags

</td><td>

System tags for the content.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_updated\_by

</td><td>

System name of the user who most recently updated this record.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics. sys\_updated\_on

</td><td>

Date and time at which the record was most recently updated.Data type: String

</td></tr><tr><td>

order\_line\_items. order\_line\_characteristics.type

</td><td>

Type of order line characteristic.Possible values:

-   product
-   service

 Data type: String

</td></tr><tr><td>

order\_line\_items.order\_line\_id

</td><td>

Order number of the order associated with this order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.parent\_line\_item

</td><td>

If applicable, identifies a parent line item to this line item.Data type: String

</td></tr><tr><td>

order\_line\_items.previous\_product\_model

</td><td>

Identifies the product model for the product listed prior to this item in the order line. Sys\_id of the product listed in the Product Models \[cmdb\_model\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.price\_list

</td><td>

Sys\_id of a price list record in the Price Lists \[sn\_csm\_pricing\_price\_list\] table.**Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.product

</td><td>

Sys\_id of the product listed in the Product Models \[cmdb\_model\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.product\_offering

</td><td>

Sys\_id of the product listed in the Product Offerings \[sn\_prd\_pm\_product\_offering\] table. Data type: String

</td></tr><tr><td>

order\_line\_items.product

</td><td>

Sys\_id of the product model listed in the Product Models \[cmdb\_model\] table. Must be provided with matching order line item Data type: String

</td></tr><tr><td>

order\_line\_items.product\_specification

</td><td>

Sys\_id of the product specification associated with the order line item. Listed in the Product Specifications \[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr><tr><td>

order\_line\_items.quantity

</td><td>

Number of product models ordered. Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_city

</td><td>

Name of the destination city.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_country

</td><td>

Abbreviation of the destination country.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_state

</td><td>

Abbreviation of the destination state or province.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_street

</td><td>

Destination street address.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_zip

</td><td>

Destination ZIP or postal code.Data type: String

</td></tr><tr><td>

order\_line\_items.short\_description

</td><td>

Short description of the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.sku

</td><td>

Number that is generated by a supplier that uniquely identifies a product that is sold by that supplier.Data type: String

</td></tr><tr><td>

order\_line\_items.sold\_product

</td><td>

Sys\_id of an install base sold product listed in the Sold Products \[sn\_install\_base\_sold\_product\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.specification

</td><td>

Specification of order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.state

</td><td>

State of order line. For example, draft, new, in\_progress, or completed.Data type: String

</td></tr><tr><td>

order\_line\_items.status

</td><td>

Status of the order line item.Possible values:

-   success
-   failure

 Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_class\_name

</td><td>

System name of the table in which this order line item record is located.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_created\_by

</td><td>

System name of the user who created this record.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_created\_on

</td><td>

Date and time at which the record was originally created.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_domain

</td><td>

Domain scope in which the order record is accessible. For example, global.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_domain\_path

</td><td>

Domain path for the record.Data type: String

 Default: / \(global\)

</td></tr><tr><td>

order\_line\_items.sys\_id

</td><td>

Sys\_id of the line item record located in the Order Line Items \[sn\_csm\_om\_order\_line\_item\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_mod\_count

</td><td>

Number of times this record has been modified.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_tags

</td><td>

System tags for the content.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_updated\_by

</td><td>

System name of the user who most recently updated this record.Data type: String

</td></tr><tr><td>

order\_line\_items.sys\_updated\_on

</td><td>

Date and time at which the record was most recently updated.Data type: String

</td></tr><tr><td>

order\_line\_items.top\_line\_item

</td><td>

Total price of all order line items accumulated in this order.Data type: String

</td></tr><tr><td>

order\_line\_items.total\_price

</td><td>

Total price of order line. The API does not calculate the total based on net price and quantity.Data type: String

</td></tr><tr><td>

order\_line\_items.unit\_of\_measurement

</td><td>

Sys\_id for the ordered unit of measure listed in the Unit of Measures \[sn\_prd\_pm\_uom\] table. **Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.​unit\_of\_measurement

</td><td>

Required. Sys\_id for the ordered unit of measure listed in the Unit of Measures \[sn\_prd\_pm\_uom\] table. **Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.unit\_price

</td><td>

Net price of the product offering per unit listed in the Currency Instances \[fx\_currency\_instance\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.work\_notes

</td><td>

Free-form internal work notes for the order line item.Data type: String

</td></tr><tr><td>

order\_type

</td><td>

Order action that determines how the order is added.Possible values:

-   add
-   change

 Data type: String

</td></tr><tr><td>

partner

</td><td>

For B2B orders, sys\_id of the associated partner for an account listed in the Accounts \[customer\_account\] table.Data type: String

</td></tr><tr><td>

partner\_contact

</td><td>

For B2B orders, sys\_id of the primary contact of the partner for the partner account. Listed in the Contacts \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

payment\_ref\_id

</td><td>

Unique identifier of the payment. For example, check number.Data type: String

</td></tr><tr><td>

price\_list

</td><td>

Sys\_id of the associated price list listed in the Price Lists \[sn\_csm\_pricing\_price\_list\] table. The price is not calculated based on net price and quantity by this API.**Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

quote\_id

</td><td>

Unique ID for the order price quote.Data type: String

</td></tr><tr><td>

same\_as\_shipping\_address

</td><td>

Flag that indicates whether the address of the purchaser is the same as the shipping address.Valid values:

-   true: Address of the purchaser is the same as the shipping address.
-   false: Address of the purchaser is different from the shipping address.

 Data type: Boolean

</td></tr><tr><td>

shipping\_city

</td><td>

Name of the destination city.Data type: String

</td></tr><tr><td>

shipping\_country

</td><td>

Abbreviation of the destination country.Data type: String

</td></tr><tr><td>

shipping\_location

</td><td>

Sys\_id of a shipping location listed in the Locations \[cmn\_location\] table.Data type: String

</td></tr><tr><td>

shipping\_state

</td><td>

Abbreviation of the destination state or province.Data type: String

</td></tr><tr><td>

shipping\_street

</td><td>

Destination street address.Data type: String

</td></tr><tr><td>

shipping\_zip

</td><td>

Destination ZIP or postal code.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Short description of the order.Data type: String

</td></tr><tr><td>

special\_instructions

</td><td>

Special instructions for the order.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the order. For example, new, in\_progress, or completed.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the order.Possible values:

-   success
-   failure

 Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td>

System name of the table in which this order record is located.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td>

System name of the user who created this record.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time at which the record was originally created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td>

Domain scope in which the order record is accessible. For example, global.Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td>

Domain path for the record.Data type: String

 Default: / \(global\)

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the order listed in the Orders \[sn\_csm\_om\_order\] table.Data type: String

</td></tr><tr><td>

sys\_mod\_count

</td><td>

Number of times this record has been modified.Data type: String

</td></tr><tr><td>

sys\_tags

</td><td>

System tags for the content.Data type: String

</td></tr><tr><td>

sys\_updated\_by

</td><td>

System name of the user who most recently updated this record.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time at which the record was most recently updated.Data type: String

</td></tr><tr><td>

total\_amount

</td><td>

Total cost for the entire order.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to get an order by its order number.

```
curl "https://instance.service-now.com/api/sn_ind_tmt_orm/order/ORD0001034" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response:

```
{
  "result": {
    "actual_start_date": "",
    "payment_ref_id": null,
    "shipping_city": null,
    "channel": "api",
    "expected_end_date": "",
    "sys_updated_on": "2022-03-30 21:59:41",
    "price_list": null,
    "sys_updated_by": "username",
    "sys_created_on": "2022-03-30 21:59:41",
    "contact": "96d0461553ab70101aaeddeeff7b120b",
    "sys_domain": "global",
    "state": "draft",
    "order_type": "add",
    "sys_created_by": "eseruser",
    "shipping_street": null,
    "special_instructions": null,
    "contract": null,
    "quote_id": null,
    "expected_start_date": "",
    "sys_domain_path": "/",
    "billing_street": null,
    "billing_city": null,
    "total_amount": "2000",
    "order_id": "ORD0001034",
    "shipping_country": "USA",
    "status": "new",
    "short_description": null,
    "shipping_state": null,
    "external_id": null,
    "sys_class_name": "sn_csm_om_order",
    "sys_id": "24fdf5bd75eec510f877f30c01a15aa0",
    "shipping_zip": null,
    "billing_state": null,
    "billing_zip": null,
    "same_as_shipping_address": "0",
    "consumer": null,
    "comments": "",
    "order_currency": "USD",
    "billing_country": "USA",
    "sys_mod_count": "1",
    "billing_location": null,
    "shipping_location": null,
    "sys_tags": "",
    "order_date": "2022-03-30 21:59:41",
    "order_category": "product",
    "actual_end_date": "",
    "partner": null,
    "partner_contact": null,
    "account": "c480021553ab70101aaeddeeff7b120f",
    "external_system": null,
    "order_line_items": [
      {
        "short_description": null,
        "shipping_state": "CA",
        "shipping_city": "Santa Clara",
        "product_offering": "2d4376760f740110603bf634a7767e46",
        "external_id": null,
        "sys_updated_on": "2022-03-30 21:59:41",
        "expiration_date": "",
        "sys_class_name": "sn_csm_om_order_line_item",
        "sold_product": null,
        "sys_id": "ecfdf5bd75eec510f877f30c01a15aa3",
        "unit_of_measurement": "cb2795d553020110286eddeeff7b12ff",
        "price_list": null,
        "sys_updated_by": "username",
        "shipping_zip": "94560",
        "sys_created_on": "2022-03-30 21:59:41",
        "contact": "96d0461553ab70101aaeddeeff7b120b",
        "sys_domain": "global",
        "effective_date": "",
        "action": "add",
        "order_line_id": "ORDL0001060",
        "state": "draft",
        "sku": null,
        "consumer": null,
        "sys_created_by": "username",
        "order": "24fdf5bd75eec510f877f30c01a15aa0",
        "previous_product_model": null,
        "shipping_street": "222 Star St",
        "product": "561dba7e0f740110603bf634a7767ebe",
        "quantity": "1",
        "comments": "",
        "total_price": "2000",
        "parent_line_item": null,
        "sys_mod_count": "1",
        "specification": "104f66720f740110603bf634a7767e7d",
        "list_price": "2000",
        "unit_price": "2000",
        "sys_domain_path": "/",
        "sys_tags": "",
        "delivered_quantity": null,
        "top_line_item": null,
        "product_specification": "104f66720f740110603bf634a7767e7d",
        "location": null,
        "work_notes": "",
        "shipping_country": "USA",
        "account": "c480021553ab70101aaeddeeff7b120f",
        "external_system": null,
        "status": "new",
        "order_line_characteristics": [
          {
            "characteristic_option": "1c6ceabe0f340110603bf634a7767e97",
            "sys_mod_count": "0",
            "specification": "104f66720f740110603bf634a7767e7d",
            "external_id": null,
            "sys_updated_on": "2022-03-30 21:59:41",
            "type": "1",
            "sys_domain_path": "/",
            "sys_tags": "",
            "characteristic": "4e76f1b20fb00110603bf634a7767ee3",
            "sys_class_name": "sn_csm_om_order_characteristic_value",
            "previous_characteristic_option_value": null,
            "number": "ORC000001041",
            "sys_id": "acfd79bd75eec510f877f30c01a15a94",
            "sys_updated_by": "username",
            "sys_created_on": "2022-03-30 21:59:41",
            "sys_domain": "global",
            "characteristic_option_value": "1.2 cu",
            "order_line_item": "ecfdf5bd75eec510f877f30c01a15aa3",
            "sys_created_by": "user"
          },
          {
            "characteristic_option": "2d0d66fe0f340110603bf634a7767ef6",
            "sys_mod_count": "0",
            "specification": "104f66720f740110603bf634a7767e7d",
            "external_id": null,
            "sys_updated_on": "2022-03-30 21:59:41",
            "type": "1",
            "sys_domain_path": "/",
            "sys_tags": "",
            "characteristic": "11e639b20fb00110603bf634a7767e17",
            "sys_class_name": "sn_csm_om_order_characteristic_value",
            "previous_characteristic_option_value": null,
            "number": "ORC000001042",
            "sys_id": "e0fd79bd75eec510f877f30c01a15a95",
            "sys_updated_by": "username",
            "sys_created_on": "2022-03-30 21:59:41",
            "sys_domain": "global",
            "characteristic_option_value": "Stainless steel",
            "order_line_item": "ecfdf5bd75eec510f877f30c01a15aa3",
            "sys_created_by": "user"
          }
        ]
      }
    ]
  }
}
```

## Order API – POST /sn\_ind\_tmt\_orm/order

Creates a new order with line items and characteristics.

Orders with line items are defined using request body parameters. The following properties are required in most versions of Order Management:

-   **account** for B2B orders or **consumer** for B2C orders.
    -   **account** – Sys\_id of a record located in the Accounts \[customer\_account\] table.
    -   **consumer** – Sys\_id of a record located in the Consumers \[csm\_consumer\] table.
-   **order\_currency** – Currency code representing the currency in which the order was purchased. For example, `USD` for United States Dollars. This currency is used for all amount fields in the order and line orders. Currency codes are listed in the Currencies \[fx\_currency\] table.
-   **order\_line\_items** – List of objects that define each order line item in the order. Located in the Order Line Items \[sn\_csm\_om\_order\_line\_item\] table. Required properties in each order line item object:
    -   **account** for B2B orders or **consumer** for B2C orders.
        -   **account** – Sys\_id of the business account assigned to this order line item. Located in the Accounts \[customer\_account\] table.
        -   **consumer** – Sys\_id of the consumer assigned to this order line item. Located in the Consumers \[csm\_consumer\] table.
    -   **order\_line\_characteristics** – List of objects defining associated order line characteristics. Order line characteristics are located in the Order Line Characteristics \[sn\_csm\_om\_order\_characteristic\_value\] table.
    -   **product\_offering** – Sys\_id of the product listed in the Product Offerings \[sn\_prd\_pm\_product\_offering\] table.
    -   **quantity** – Number of product models ordered.
    -   **unit\_of\_measurements** – Sys\_id for the ordered unit of measure listed in the Unit of Measures \[sn\_prd\_pm\_uom\] table.

The Request body parameters table contains more details.

### URL format

Versioned URL: `/api/sn_ind_tmt_orm/{api_version}/order`

Default URL: `/api/sn_ind_tmt_orm/order`

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

account

</td><td>

Required for B2B orders. Sys\_id of a record located in the Accounts \[customer\_account\] table. The consumer property is required for B2C orders.Data type: String

</td></tr><tr><td>

actual\_end\_date

</td><td>

End date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

actual\_start\_date

</td><td>

Start date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

billing\_city

</td><td>

Name of the billing city.Data type: String

</td></tr><tr><td>

billing\_country

</td><td>

Abbreviation of the billing country.Data type: String

</td></tr><tr><td>

billing\_state

</td><td>

Abbreviation of the billing state or province.Data type: String

</td></tr><tr><td>

billing\_street

</td><td>

Billing street address.Data type: String

</td></tr><tr><td>

billing\_zip

</td><td>

Billing ZIP or postal code.Data type: String

</td></tr><tr><td>

comments

</td><td>

Additional information for the order.Data type: String

</td></tr><tr><td>

consumer

</td><td>

Required for B2C orders. Sys\_id of a record located in the Consumers \[csm\_consumer\] table. The account property is required for B2B orders.Data type: String

</td></tr><tr><td>

contact

</td><td>

Sys\_id of the customer contact related to the account. Listed in the Contacts \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

contract

</td><td>

Sys\_id of the Customer Service contract listed in the Contracts \[ast\_contract\] table.Data type: String

</td></tr><tr><td>

expected\_end\_date

</td><td>

Expected end date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

expected\_start\_date

</td><td>

Expected start date of order.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

external\_id

</td><td>

External ID representing a related record on a third party's system. Data type: String

</td></tr><tr><td>

external\_system

</td><td>

Name of the customer's system. Data type: String

</td></tr><tr><td>

order\_category

</td><td>

Customer order type.Possible values:

-   product
-   service

 Data type: String

</td></tr><tr><td>

order\_currency

</td><td>

Required. Currency code representing the currency in which the order was purchased. For example, `USD` for United States Dollars. This currency is used for all amount fields in the order and line orders. Currency codes are listed in the Currencies \[fx\_currency\] table. **Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_date

</td><td>

Date and time of order creation.Format: UTC format, yyyy-MM-dd HH:mm:ss

 Data type: String

</td></tr><tr><td>

order\_line\_items

</td><td>

Required. List of objects that define each order line item in the order. Located in the Order Line Items \[sn\_csm\_om\_order\_line\_item\] table. Data type: Array

 Required properties in each order line item object:

-   **account** for B2B orders or **consumer** for B2C orders.
-   **product\_offering** –
-   **quantity**
-   **unit\_of\_measurements**
-   **order\_line\_characteristics**

 ```
"order_line_items": [
 {
   "account": "String",
   "action": "String",
   "comments": "String",
   "consumer": "String",
   "contact": "String",
   "delivered_quantity": "String",
   "effective_date": "String",
   "expiration_date": "String",
   "external_id": "String",
   "external_system": "String",
   "list_price": "String",
   "location": "String",
   "order_line_characteristics": [Array],
   "order_line_id": "String",
   "order": "String",
   "parent_line_item": "String",
   "previous_product_model": "String",
   "price_list": "String",
   "product_offering": "String",
   "product_specification": "String",
   "product": "String",
   "quantity": "String",
   "shipping_city": "String",
   "shipping_country": "String",
   "shipping_state": "String",
   "shipping_street": "String",
   "shipping_zip": "String",
   "short_description": "String",
   "sku": "String",
   "sold_product": "String",
   "specification": "String",
   "state": "String",
   "status": "String",
   "sys_class_name": "String",
   "sys_created_by": "String",
   "sys_created_on": "String",
   "sys_id": "String",
   "sys_mod_count": "String",
   "sys_tags": "String",
   "sys_updated_by": "String",
   "sys_updated_on": "String",
   "top_line_item": "String",
   "total_price": "String",
   "unit_of_measurement": "String",
   "unit_price": "String",
   "work_notes": "String"
 }
]
```

</td></tr><tr><td>

order\_line\_items.account

</td><td>

Required for B2B orders. Sys\_id of the business account assigned to this order line item. Located in the Accounts \[customer\_account\] table. The consumer property is required for B2C orders.Data type: String

</td></tr><tr><td>

order\_line\_items.action

</td><td>

Action that determines how the order line is added to the order.Possible values:

-   add
-   change

 Data type: String

</td></tr><tr><td>

order\_line\_items.comments

</td><td>

Additional information for the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.consumer

</td><td>

Required for B2C orders. Sys\_id of the consumer assigned to this order line item. Located in the Consumers \[csm\_consumer\] table. The account property is required for B2B orders.Data type: String

</td></tr><tr><td>

order\_line\_items.contact

</td><td>

Contact sys\_id related to the account.Data type: String

</td></tr><tr><td>

order\_line\_items.delivered\_quantity

</td><td>

Number of items in the order delivered.Data type: String

</td></tr><tr><td>

order\_line\_items.effective\_date

</td><td>

Effective date of order line.Format: yyyy-MM-dd HH:mm:ss in UTC time zone

 Data type: String

</td></tr><tr><td>

order\_line\_items.expiration\_date

</td><td>

Expiration date of order line.Format: yyyy-MM-dd HH:mm:ss in UTC time zone

 Data type: String

</td></tr><tr><td>

order\_line\_items.external\_id

</td><td>

External ID of the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.external\_system

</td><td>

External sys\_id of the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.list\_price

</td><td>

List price of the product offering per unit.**Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.​order\_line\_characteristics

</td><td>

Required. List of objects defining associated order line characteristics. Order line characteristics are located in the Order Line Characteristics \[sn\_csm\_om\_order\_characteristic\_value\] table. In the most recent release, if the offering is associated with product specification, then order characteristics must be included to determine the product model.

 In earlier releases, this property was only required for simple orders with the **order\_line\_items.product\_specification** property set.

 Data type: Array

 ```
"order_line_characteristics": [
 {
  "characteristic": "String",
  "characteristic_option": "String"
 }
]
```

</td></tr><tr><td>

order\_line\_items.​order\_line\_characteristics.​characteristic

</td><td>

Name of the characteristic associated with the product model. For example, Dishwasher Size.Data type: String

</td></tr><tr><td>

order\_line\_items.​order\_line\_characteristics.​characteristic\_option

</td><td>

Product characteristic unique option that triggers the exclusion rule. For example, product size or color.Data type: String

</td></tr><tr><td>

order\_line\_items.price\_list

</td><td>

Sys\_id of a price list record in the Price Lists \[sn\_csm\_pricing\_price\_list\] table.**Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.product

</td><td>

Sys\_id of the product model listed in the Product Models \[cmdb\_model\] table. If included in the request body, the associated order line characteristics must match. Data type: String

</td></tr><tr><td>

order\_line\_items.product\_offering

</td><td>

Required. Sys\_id of the product listed in the Product Offerings \[sn\_prd\_pm\_product\_offering\] table. If the offering is associated with the product model, the product model is determined by the order. If the offering is associated with product specification, then order characteristics must be included to determine the product model.

 Data type: String

</td></tr><tr><td>

order\_line\_items.​product\_specification

</td><td>

Required. Sys\_id of the product specification associated with the order line item. Listed in the Product Specifications \[sn\_prd\_pm\_product\_specification\] table. **Note:** This property was not required in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.quantity

</td><td>

Required. Number of product models ordered. **Note:** This property was required in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_city

</td><td>

Name of the destination city.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_country

</td><td>

Abbreviation of the destination country.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_state

</td><td>

Abbreviation of the destination state or province.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_street

</td><td>

Destination street address.Data type: String

</td></tr><tr><td>

order\_line\_items.shipping\_zip

</td><td>

Destination ZIP or postal code.Data type: String

</td></tr><tr><td>

order\_line\_items.short\_description

</td><td>

Short description of the order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.sku

</td><td>

Number that is generated by a supplier that uniquely identifies a product that is sold by that supplier.Data type: String

</td></tr><tr><td>

order\_line\_items.sold\_product

</td><td>

Sys\_id of an install base sold product listed in the Sold Products \[sn\_install\_base\_sold\_product\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.specification

</td><td>

Specification of order line item.Data type: String

</td></tr><tr><td>

order\_line\_items.state

</td><td>

State of order line. For example, draft, new, in\_progress, or completed.Data type: String

</td></tr><tr><td>

order\_line\_items.total\_price

</td><td>

Total price of order line. The total price is not calculated based on net price and quantity by this API.Data type: String

</td></tr><tr><td>

order\_line\_items.​unit\_of\_measurement

</td><td>

Required. Sys\_id for the ordered unit of measure listed in the Unit of Measures \[sn\_prd\_pm\_uom\] table. **Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

order\_line\_items.unit\_price

</td><td>

Net price of the product offering per unit listed in the Currency Instances \[fx\_currency\_instance\] table.Data type: String

</td></tr><tr><td>

order\_line\_items.work\_notes

</td><td>

Free-form internal work notes for the order line item.Data type: String

</td></tr><tr><td>

order\_type

</td><td>

Order action that determines how the order is added.Possible values:

-   add
-   change

 Data type: String

</td></tr><tr><td>

partner

</td><td>

For B2B orders, sys\_id of the associated partner for an account listed in the Accounts \[customer\_account\] table.Data type: String

</td></tr><tr><td>

partner\_contact

</td><td>

For B2B orders, sys\_id of the primary contact of the partner for the partner account. Listed in the Contacts \[customer\_contact\] table.Data type: String

</td></tr><tr><td>

price\_list

</td><td>

Sys\_id of the associated price list listed in the Price Lists \[sn\_csm\_pricing\_price\_list\] table. The price is not calculated based on net price and quantity by this API.**Note:** This property might not be available in earlier versions of Order Management.

 Data type: String

</td></tr><tr><td>

quote\_id

</td><td>

Unique ID for the order price quote.Data type: String

</td></tr><tr><td>

shipping\_city

</td><td>

Name of the destination city.Data type: String

</td></tr><tr><td>

shipping\_country

</td><td>

Abbreviation of the destination country.Data type: String

</td></tr><tr><td>

shipping\_state

</td><td>

Abbreviation of the destination state or province.Data type: String

</td></tr><tr><td>

shipping\_street

</td><td>

Destination street address.Data type: String

</td></tr><tr><td>

shipping\_zip

</td><td>

Destination ZIP or postal code.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Short description of the order.Data type: String

</td></tr><tr><td>

special\_instructions

</td><td>

Special instructions for the order.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the order. For example, new, in\_progress, or completed.Data type: String

</td></tr><tr><td>

total\_amount

</td><td>

Total cost for the entire order.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

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

Bad request.Payload is not in the expected format.

</td></tr><tr><td>

401

</td><td>

The user is not authenticated.

</td></tr><tr><td>

403

</td><td>

The user is not authorized.-   The user does not have required roles to access the API.
-   The user does not have authorization to read the order.

 This API requires sn\_csm\_om.order\_integrator for access, and one of the following:

-   sn\_csm\_om.consumer\_agent – API write access restricted to B2C orders.
-   sn\_csm\_om.customer\_agent – API write access restricted to B2B orders.
-   sn\_csm\_om.order\_admin – API write access for B2B or B2C orders.

</td></tr><tr><td>

500

</td><td>

Internal server error. One or more validations have failed.Possible issues:

-   **Account** or **consumer** parameter is missing. These fields are mandatory on header and item.
-   **Account**/**contact** and **consumer** parameters have been passed. These parameters cannot be passed together.
-   Choice parameters: Invalid choice values passed.
-   Quantity parameter: Invalid value.
-   Invalid reference field.
-   Missing mandatory fields.
-   Invalid date and time format.
-   Start date is greater than end date.
-   Invalid characteristic.
-   Invalid characteristic option.
-   More than one product model was found for provided characteristics.
-   Product model not found for the provided characteristics.
-   User does not have access to create an order.
-   B2B order contains consumer order lines.
-   B2C order contains account, contact, partner, or partner contact parameters.
-   Amount fields currency does not match the order currency.
-   **Order\_line\_characteristics** were passed for an order line with **product\_offering** associated with product model.
-   The unit of measurement specified for an offer type=configuration does not belong to the allowed units of measure defined on the product offering.
-   No characteristics were passed for an offer type of configuration when the product offering is expecting configuration.
-   Unable to create orders that have a bundle item plus simple configurations on the order line.
-   Passed parameters contain characteristics for a bundle offering.
-   Unable to create parent order line and/or child order line. Only parent bundle items are valid in bundle offering calls.
-   The specified unit\_of\_measurement record for a bundle offering contains a value other than "EACH".

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Details describing an error encountered during the request process.Data type: Object

 ```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. Each error message has a corresponding description in the **detail** property.Data type: String

</td></tr><tr><td>

order\_id

</td><td>

Order number of the order listed in the Orders \[sn\_csm\_om\_order\] table.Data type: String

</td></tr><tr><td>

status

</td><td>

Failure message included in addition to the error object.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the order listed in the Orders \[sn\_csm\_om\_order\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to create a single-item order for a stainless steel microwave.

```
curl "https://instance.service-now.com/api/sn_ind_tmt_orm/order" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
\"account\": \"c480021553ab70101aaeddeeff7b120f\",
\"contact\":\"96d0461553ab70101aaeddeeff7b120b\",
\"order_currency\": \"USD\",
\"order_line_items\": [
{
\"account\": \"c480021553ab70101aaeddeeff7b120f\",
\"action\": \"add\",
\"contact\": \"96d0461553ab70101aaeddeeff7b120b\",
\"list_price\": \"2000\",
\"order_line_characteristics\": [
{
\"characteristic\" : \"Solana color\",
\"characteristic_option\" : \"Stainless steel\"
},
{
\"characteristic\" :\"Microvawe Capacity\",
\"characteristic_option\" : \"1.2 cu\"
}
],
\"product_offering\": \"2d4376760f740110603bf634a7767e46\",
\"quantity\": \"1\",
\"shipping_city\": \"Santa Clara\",
\"shipping_country\": \"USA\",
\"shipping_state\": \"CA\",
\"shipping_street\": \"222 Star St\",
\"shipping_zip\": \"94560\",
\"state\": \"draft\",
\"status\": \"new\",
\"total_price\": \"2000\",
\"unit_of_measurement\": \"cb2795d553020110286eddeeff7b12ff\",
\"unit_price\": \"2000\"
}
]
}" \
--user 'user':'password'
```

Response:

```
{
  "result": {
    "sys_id": "24fdf5bd75eec510f877f30c01a15aa0",
    "order_id": "ORD0001034"
  }
}
```

