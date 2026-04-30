---
title: Service Catalog API
description: The Service Catalog API provides endpoints that access Service Catalog configuration and actions from within a Service Portal.Deletes the specified item from the current cart.Deletes a specified cart, and the contents of the cart.Retrieves the details of the items within the logged in user's cart.Retrieves the shipping address of the specified user based on the glide.sc.req\_for.roles property and the default behavior configured in the glide.sc.req\_for.roles.defaultproperty.Retrieves a list of catalogs to which the user has access based on the passed in parameters.Retrieves the list of available categories for the specified catalog.Retrieves the available information for a specified catalog.Retrieves the available information for a specified category.Retrieves a list of catalog items based on the specified parameters.Verifies whether the specified delegated user has acquisition rights to the specified service catalog item.Retrieves a specified catalog item.Retrieves the list of items in the logged in user's wish list.Retrieves the details of the specified item stored in the wish list cart.Retrieves and processes the checkout for the current cart based on whether the two-step checkout process is enabled.Checks out the user cart, based on the current check-out type \(one-step or two-step\).Adds the specified item to the cart of the current user.Adds the specified item to the wish list cart.Retrieves an array of contents requested for checkout.Returns a list of users whose request for the specified item cannot be delegated \(requested by another user\).Orders the specified catalog item.Creates a record and returns the Table API relative path and redirect URL to access the created record.Returns the display value of the specified variable.Updates the specified item in the logged in user's cart.Retrieves a list of items based on the needs described for an order guide.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 96
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Service Catalog API

The Service Catalog API provides endpoints that access Service Catalog configuration and actions from within a Service Portal.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Service Catalog - DELETE /sn\_sc/servicecatalog/cart/\{cart\_item\_id\}

Deletes the specified item from the current cart.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/cart/{cart_item_id}`

Default URL: `/api/sn_sc/servicecatalog/cart/{cart_item_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

cart\_item\_id

</td><td>

Sys\_id of the item to delete from the current cart.Data type: String

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|204|Indicates that the request completed successfully and the specified item was deleted from the cart.|
|400|Indicates that either the specified **cart\_item\_id** is invalid or the user does not have access to the cart item.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/v1/servicecatalog/cart/1f4cc597db21120064301150f0b8f5fc" \
--request DELETE \
--user "username":"password"
```

```
None
```

## Service Catalog - DELETE /sn\_sc/servicecatalog/cart/\{sys\_id\}/empty

Deletes a specified cart, and the contents of the cart.

The capabilities of what a user can delete \(items and/or cart\) depends on the role in which they use to authenticate.

User roles needed to delete cart and cart contents:

-   admin/catalog\_admin: Can empty any user cart.
-   admin: Can delete the cart after all the contents of the cart are deleted.
-   catalog\_admin: Can delete all the items in the cart.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/cart/{sys_id}/empty`

Default URL: `/api/sn_sc/servicecatalog/cart/{sys_id}/empty`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the cart to empty and delete.Data type: String

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

204

</td><td>

Request completed successfully and both empties and deletes the cart.

</td></tr><tr><td>

400

</td><td>

Indicates an error for one of the following reasons:-   Invalid cartId.
-   User does not have admin/catalog\_admin role, or is trying to empty another user cart.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/cart/dde34ad713426300027879d96144b072/empty" \
--request DELETE \
--user 'username':'password'
```

```
None
```

## Service Catalog - GET /sn\_sc/servicecatalog/cart

Retrieves the details of the items within the logged in user's cart.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/cart`

Default URL: `/api/sn_sc/servicecatalog/cart`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

|Name|Description|
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

|Status code|Description|
|-----------|-----------|
|200|Indicates that the request completed successfully. If there is no item in the cart, it returns basic cart information and pricing for user. If the cart contains any items, then the information about the items and their individual pricing is also included.|
|400|Indicates that the cart is empty and cannot check out.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_id

</td><td>

Sys\_id of the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;

</td><td>

List of items in the cart having a specific recurring frequency. Possible values include:-   daily
-   monthly
-   yearly
-   none \(no recurring fees\)

 Data type: Object

 ```
"<recurring_frequency>": {
  "frequency_label": "String",
  "items": [Array],
  "show_subtotal_price": "String",
  "subtotal_price": "String",
  "subtotal_recurring_frequency": "String",
  "subtotal_recurring_price": "String",
  "subtotal_title": "String",
  "total_title": "String"
```

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.frequency\_label

</td><td>

Frequency of the associated recurring fee.Data type: String

 Default: Null

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items

</td><td>

List of objects that contain details of each item associated with the specified recurring frequency category.Data type: Array

 ```
"items": [{
  "cart_item_id": "String",
  "catalog_item_id": "String",
  "created.by": "String",
  "created_on": "String",
  "delivery_time": "String",
  "item_id": "String",
  "item_name": "String",
  "localized_price": "String",
  "localized_recurring_price": "String",
  "name": "String",
  "order_guide": "String",
  "picture": "String",
  "price": "String",
  "quantity": "String",
  "recurring_frequency": "String",
  "recurring_price": "String",
  "recurring_subtotal": Number,
  "recurring_subtotal_price": "String",
  "short_description": "String",
  "show_price": Boolean,
  "show_quantity": Boolean,
  "show_recurring_price": Boolean,
  "subtotal": Number,
  "subtotal_price": "String",
  "sys_class_name": "String",
  "sys_id": "String",
  "updated_by": "String",
  "updated_on": "String",
  "variables": {Object}
}]
```

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.cart\_item\_id

</td><td>

Sys\_id of the item in this cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.catalog\_item\_id

</td><td>

Sys\_id of catalog associated the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.created.by

</td><td>

User that initially placed the item in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.created\_on

</td><td>

Date on which the item was initially placed in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.delivery\_time

</td><td>

Time that the specified item takes to be delivered.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.item\_id

</td><td>

Catalog sys\_id of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.item\_name

</td><td>

Name of the specified item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.localized\_price

</td><td>

Price of the item in local currency.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.localized\_recurring\_price

</td><td>

Recurring fee for the specified item in local currency.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.name

</td><td>

Item name.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.order\_guide

</td><td>

Name of the order guide to which this item is associated.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.picture

</td><td>

File name of the picture of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.price

</td><td>

Price of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.quantity

</td><td>

Number of the specified item in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_frequency

</td><td>

How often the recurring fee is charged for the specified item.Data type: String

 Default: Null

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_price

</td><td>

Recurring fee for the specified item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_subtotal

</td><td>

Subtotal of the recurring fees for the item \(**recurring\_price** x **quantity**\).Data type: Number

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_subtotal\_price

</td><td>

Subtotal of the recurring fees for the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.short\_description

</td><td>

Short description of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_price

</td><td>

Flag that indicates whether the price of the item is shown in the cart.Possible values:

-   true: Show the price of the item in the cart.
-   false: Do not show the price of the item in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_quantity

</td><td>

Flag that indicates whether to show the item quantity in the cart.Possible values:

-   true: Show the item quantity in the cart.
-   false: Do not show the item quantity in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_recurring\_price

</td><td>

Flag that indicates whether the recurring fees should appear in the cart.Possible values:

-   true: Show the recurring fees in the cart.
-   false: Do not show the recurring fees in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.subtotal

</td><td>

Subtotal number of items.Data type: Number

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.subtotal\_price

</td><td>

Subtotal for the item \(**price** x **quantity**\).Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.sys\_class\_name

</td><td>

System classification name of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.sys\_id

</td><td>

Sys\_id of the item record.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.updated\_by

</td><td>

User that updated the item after it was initially placed in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.updated\_on

</td><td>

Last date/time on which the item was either initially placed in the cart or updated.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.variables

</td><td>

List of name/value pairs of the item variables.Data type: Object

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.show\_subtotal\_price

</td><td>

Flag that indicates whether to show a subtotal for the associated recurring fee category.Possible values:

-   true: Show subtotals in the cart.
-   false: Do not show subtotals in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_price

</td><td>

Subtotal of the cost of all items for the associated recurring frequency category.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_recurring\_frequency

</td><td>

Type of subtotal recurring frequency, such as daily, monthly, etc. Same as **subtotal\_recurring\_frequency**.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_recurring\_price

</td><td>

Subtotal of the recurring fees of the items within the associated recurring frequency category.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_title

</td><td>

If the **show\_subtotal\_price** is set to `true`, the text to display in the cart for the associated subtitle.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.total\_title

</td><td>

Text to display for the total title for the associated recurring frequency category.Data type: String

</td></tr><tr><td>

show\_subtotal\_price

</td><td>

Flag that indicates whether to show the subtotal price in the cart.Possible values:

-   true: Show subtotals in the cart.
-   false: Do not show subtotals in the cart.

 Data type: String

</td></tr><tr><td>

subtotal\_price

</td><td>

Subtotal of all items in the cart in whole dollars.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_frequency

</td><td>

Type of subtotal recurring frequency, such as daily, monthly, etc. Same as **&lt;recurring\_frequency&gt;.subtotal\_recurring\_frequency**.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_price

</td><td>

Subtotal of the recurring frequency fees for all items in the cart.Data type: String

</td></tr><tr><td>

subtotal\_title

</td><td>

Text to display in the cart for the subtotal field title.Data type: String

</td></tr><tr><td>

total\_title

</td><td>

Text to display in the cart for the total field title.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/cart" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "cart_id": "6d88bc29137d2300027879d96144b04b",
    "subtotal_price": "$1,598.00",
    "subtotal_recurring_frequency": "",
    "subtotal_recurring_price": "$0.00",
    "total_title": "Total",
    "none": {
      "subtotal_price": "$1,598.00",
      "subtotal_recurring_frequency": "",
      "subtotal_recurring_price": "$0.00",
      "total_title": "Total",
      "frequency_label": null,
      "items": [
      {
        "updated_on": "2018-11-15 14:24:00",
        "catalog_item_id": "07f1666b0bf00300eba42da0d5673ab0",
        "short_description": "Apple iPhone 7 ",
        "recurring_subtotal_price": "$0.00",
        "delivery_time": "2 Days",
        "sys_class_name": "sc_cat_item",
        "sys_id": "1f88bc29137d2300027879d96144b056",
        "price": "$799.00",
        "recurring_frequency": null,
        "subtotal_price": "$799.00",
        "variables": {},
        "quantity": "1",
        "item_id": "07f1666b0bf00300eba42da0d5673ab0",
        "recurring_price": "$0.00",
        "show_price": true,
        "item_name": "Apple iPhone7",
        "cart_item_id": "1f88bc29137d2300027879d96144b056",
        "recurring_subtotal": 0,
        "show_quantity": true,
        "created_by": "admin",
        "picture": "e823ee6b0bf00300eba42da0d5673a95.iix",
        "created_on": "2018-11-15 14:24:00",
        "localized_price": "$799.00",
        "subtotal": 799,
        "show_recurring_price": false,
        "name": "Apple iPhone7",
        "updated_by": "admin",
        "localized_recurring_price": "$0.00",
        "order_guide": ""
      },
    ],
    "show_subtotal_price": "true",
    "subtotal_title": "Subtotal"
   },
   "show_subtotal_price": "true",
   "subtotal_title": "Subtotal"
 }
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/cart/delivery\_address/\{user\_id\}

Retrieves the shipping address of the specified user based on the **glide.sc.req\_for.roles** property and the default behavior configured in the **glide.sc.req\_for.roles.defaultproperty**.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/cart/delivery_address/{user_id}`

Default URL: `/api/sn_sc/servicecatalog/cart/delivery_address/{user_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

user\_id

</td><td>

Sys\_id of the user whose shipping address to retrieve.Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully; returns the shipping address of the specified user.|
|400|User sys\_id is invalid.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Address of the specified user.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/cart/delivery_address/62826bf03710200044e0bfc8bcbe5df1" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
'result': '25 New Chardon Street, Boston\nBoston, MA, 02114-1801\nUSA'
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/catalogs

Retrieves a list of catalogs to which the user has access based on the passed in parameters.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/catalogs`

Default URL: `/api/sn_sc/servicecatalog/catalogs`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_text

</td><td>

Keyword to search for in the "title" field of the available service catalogs.Data type: String

</td></tr><tr><td>

sysparm\_view

</td><td>

Device on which the item can display: -   **desktop**: On the desktop.
-   **mobile**: On a mobile device.
-   **both**: Both on a desktop and on a mobile device.

 Data type: String

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

|Status code|Description|
|-----------|-----------|
|200|Indicates that the request completed successfully. If a valid query returns no results, the response body only contains an empty result array.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the catalog.Data type: String

</td></tr><tr><td>

desktop\_image

</td><td>

Image that appears on the desktop for this catalog.Data type: String

</td></tr><tr><td>

has\_categories

</td><td>

Flag that indicates whether the catalog contains categories.Possible values:

-   true: Catalog contains categories.
-   false: Catalog does not contain categories.

 Data type: Boolean

</td></tr><tr><td>

has\_items

</td><td>

Flag that indicates whether the catalog contains items.Possible values:

-   true: Catalog contains items.
-   false: Catalog does not contain items.

 Data type: Boolean

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the catalog.Data type: String

</td></tr><tr><td>

title

</td><td>

Catalog title.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/catalogs?sysparm_limit=10" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": [
    {
      "title": "Technical Catalog",
      "sys_id": "742ce428d7211100f2d224837e61036d",
      "has_categories": true,
      "has_items": true,
      "description": "Products and services for the IT department",
      "desktop_image": "7a7c8271475211002ee987e8dee4906d.iix"
    },
    {
      "title": "Service Catalog",
      "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
      "has_categories": true,
      "has_items": true,
      "description": "Service Catalog - IT Now",
      "desktop_image": "adbcc271475211002ee987e8dee49001.iix"
    }
  ]
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/catalogs/\{sys\_id\}/categories

Retrieves the list of available categories for the specified catalog.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/catalogs/{sys_id}/categories`

Default URL: `/api/sn_sc/servicecatalog/catalogs/{sys_id}/categories`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the catalog whose categories are requested.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_top\_level\_only

</td><td>

Only return those categories whose parent is a catalog.Valid values:

-   true: Only return those categories whose parent is a catalog.
-   false: Return all categories.

 Data type: Boolean

</td></tr><tr><td>

sysparm\_view

</td><td>

UI view for which to render the data. Determines the fields returned in the response.Valid values:

-   desktop
-   mobile
-   both

If you also specify the **sysparm\_fields** parameter, it takes precedent.

Data type: String

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

|Status code|Description|
|-----------|-----------|
|200|Returns a list of categories in a catalog. If there are no query results, then an empty array is returned.|
|400|Indicates that the request or catalog sys\_id is invalid.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

count

</td><td>

Number of items within the category.Data type: Number

</td></tr><tr><td>

description

</td><td>

Brief category description.Data type: String

</td></tr><tr><td>

full \_description

</td><td>

Detailed category description.Data type: String

</td></tr><tr><td>

header\_icon

</td><td>

Icon used on category headers.Data type: String

</td></tr><tr><td>

homepage\_image

</td><td>

Image that appears for this category on the category's home page.Data type: String

</td></tr><tr><td>

icon

</td><td>

Icon to use to signify this category.Data type: String

</td></tr><tr><td>

subcategories

</td><td>

List of subcategories within the category.Data type: Array

 ```
"subcategories": [
  "sys_id": "String",
  "title": "String
]
```

</td></tr><tr><td>

subcategories.sys\_id

</td><td>

Sys\_id of the subcategory.Data type: String

</td></tr><tr><td>

subcategories.title

</td><td>

Title of the subcategory.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the category.Data type: String

</td></tr><tr><td>

title

</td><td>

Category title.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/catalogs/e0d08b13c3330100c8b837659bba8fb4/categories?sysparm_limit=2 \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": [
    {
      "title": "Can We Help You?",
      "description": "Your IT gateway. Report issues and submit requests.\n\t\t",
      "full_description": null,
      "icon": "",
      "header_icon": "",
      "homepage_image": "29f8ffa9471211002ee987e8dee4905e.iix",
      "count": 14,
      "subcategories": [],
      "sys_id": "e15706fc0a0a0aa7007fc21e1ab70c2f"
    },
    {
      "title": "Departmental Services",
      "description": "Services offered by different departments in the organization",
      "full_description": null,
      "icon": "",
      "header_icon": "",
      "homepage_image": "6fb4a1d95f2211001c9b2572f2b47748.iix",
      "count": 1,
      "subcategories": [],
      "sys_id": "95fc11615f1211001c9b2572f2b477c6"
    },
    {
      "title": "Desktops",
      "description": "Desktop computers for your work area.",
      "full_description": null,
      "icon": "",
      "header_icon": "",
      "homepage_image": "1bface31475211002ee987e8dee49095.iix",
      "count": 1,
      "subcategories": [],
      "sys_id": "900682363731300054b6a3549dbe5d5f"
    }
  ]
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/catalogs/\{sys\_id\}

Retrieves the available information for a specified catalog.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/catalogs/{sys_id}`

Default URL: `/api/sn_sc/servicecatalog/catalogs/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the catalog to retrieve.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_view

</td><td>

Device on which the item can display: -   **desktop**: On the desktop.
-   **mobile**: On a mobile device.
-   **both**: Both on a desktop and on a mobile device.

 Data type: String

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

</td><td>

Indicates that the request has completed successfully and returns the available information for the specified catalog.

</td></tr><tr><td>

400

</td><td>

Indicates that request is invalid for one of the following reasons:-   User does not have access to the catalog.
-   Invalid sys\_id.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

categories

</td><td>

List of objects that describe categories within the catalog.Data type: Array

 ```
"categories": [
  "description": "String",
  "header_image": "String",
  "sys_id": "String",
  "title": "String
]
```

</td></tr><tr><td>

categories.description

</td><td>

Description of the category.Data type: String

</td></tr><tr><td>

categories.header\_image

</td><td>

Category header image.Data type: String

</td></tr><tr><td>

categories.sys\_id

</td><td>

Unique category identifier \(sys\_id\).Data type: String

</td></tr><tr><td>

categories.title

</td><td>

Category title.Data type: String

</td></tr><tr><td>

description

</td><td>

Catalog description.Data type: String

</td></tr><tr><td>

desktop\_image

</td><td>

Source of the image that displays with the catalog in the desktop view.Data type: String

</td></tr><tr><td>

has\_categories

</td><td>

Flag that indicates whether the catalog has categories.Possible values:

-   true: Catalog has categories.
-   false: Catalog does not have categories.

 Data type: Boolean

</td></tr><tr><td>

has\_items

</td><td>

Flag that indicates whether there are items within the category. Possible values:

-   true: Catalog has items associated with it.
-   false: Catalog does not have any items associated with it.

 Data type: Boolean

</td></tr><tr><td>

sys\_id

</td><td>

Unique catalog sys\_id.Data type: String

</td></tr><tr><td>

title

</td><td>

Catalog title.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.comaqsw" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "title": "Customer Service",
    "sys_id": "65bcd377c3011200b12d9f2974d3aea0",
    "has_categories": true,
    "categories": [
      {
        "header_image": "",
        "sys_id": "4cb69d19c3921200b0449f2974d3ae69",
        "description": null,
        "title": "Services"
      },
      {
        "header_image": "",
        "sys_id": "1b8611d5c3921200b0449f2974d3ae12",
        "description": null,
        "title": "Support"
      }
    ],
    "has_items": true,
    "description": "Customer Service",
    "desktop_image": ""
  }
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/categories/\{sys\_id\}

Retrieves the available information for a specified category.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/categories/{sys_id}`

Default URL: `/api/sn_sc/servicecatalog/categories/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the category for which to return information.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_view

</td><td>

UI view for which to render the data. Determines the fields returned in the response.Valid values:

-   desktop
-   mobile
-   both

If you also specify the **sysparm\_fields** parameter, it takes precedent.

Data type: String

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

400

</td><td>

Indicates that request is invalid for one of the following reasons:-   User does not have access to the category.
-   Invalid sys\_id.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

child\_categories

</td><td>

List of objects that describe the child categories that belong to this category. Data type: Array

 ```
"child_categories": [
  "count": Number,
  "isParentCategory": "String",
  "parent": "String",
  "subcategories": [Array],
  "sys_id": "String",
  "title": "String"
]
```

</td></tr><tr><td>

child\_categories.count

</td><td>

Number of items in the child category.Data type: Number

</td></tr><tr><td>

child\_categories.isParentCategory

</td><td>

Flag that indicates if this is a parent category.Possible values:

-   true: Parent category.
-   false: Not the parent category.

 Data type: Boolean

</td></tr><tr><td>

child\_categories.parent

</td><td>

Sys\_id of the child category's parent.Data type: String

</td></tr><tr><td>

child\_categories.subcategories

</td><td>

List of objects that describe the subcategories for this child category.Data type: Array

 ```
"subcategories": [
  "sys_id": "String",
  "title": "String"
]
```

</td></tr><tr><td>

child\_categories.subcategories.sys\_id

</td><td>

Sys\_id of the child subcategory.Data type: String

</td></tr><tr><td>

child\_categories.subcategories.title

</td><td>

Child subcategory title.Data type: String

</td></tr><tr><td>

child\_categories.sys\_id

</td><td>

Sys\_id of the child category.Data type: String

</td></tr><tr><td>

child\_categories.title

</td><td>

Child category title.Data type: String

</td></tr><tr><td>

description

</td><td>

Short category description.Data type: String

</td></tr><tr><td>

full\_description

</td><td>

Detailed category description.Data type: String

</td></tr><tr><td>

header\_icon

</td><td>

Source of the icon displayed beside the category header when the category is listed at the top-level category.Data type: String

</td></tr><tr><td>

homepage\_image

</td><td>

Source of the home page image for the category.Data type: String

</td></tr><tr><td>

icon

</td><td>

Source of the small icon displayed beside the category name when the category is listed as a subcategory.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the category.Data type: String

</td></tr><tr><td>

title

</td><td>

Category title.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/categories/b0fdfb01932002009ca87a75e57ffbe9" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "title": "Office",
    "description": "Office services such as printing, supplies requisition\n\t\t\tand document shipping and delivery.\n\t\t",
    "full_description": null,
    "icon": "",
    "header_icon": "",
    "homepage_image": "498b0271475211002ee987e8dee490ea.iix",
    "sys_id": "109cdff8c6112276003b17991a09ad65",
    "child_categories": [
      {
        "sys_id": "109f0438c6112276003ae8ac13e7009d",
        "title": "Services",
        "count": 16,
        "parent": "109cdff8c6112276003b17991a09ad65",
        "subcategories": [],
        "isParentCategory": false
      }
    ]
  }
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/items

Retrieves a list of catalog items based on the specified parameters.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items`

Default URL: `/api/sn_sc/servicecatalog/items`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sysparm\_catalog

</td><td>

Catalog sys\_id of the item. Use this parameter to locate items in a specific catalog.Data type: String

</td></tr><tr><td>

sysparm\_category

</td><td>

Category sys\_id of the item. Use this parameter to locate catalog items in a specific category.Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. This limit is applied before ACL evaluation. If no records return, including records you have access to, rearrange the record order so records you have access to return first.

**Note:** Unusually large **sysparm\_limit** values can impact system performance.

Data type: Number

Default: 10000

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_text

</td><td>

Specific text for which to search for in the category items. For example, `sysparm_text="iPhone"` or `sysparm_text="Mobile devices"`.Data type: String

</td></tr><tr><td>

sysparm\_type

</td><td>

Type of item.Valid search values:

 -   Record Producer
-   Order Guide

If any other value is passed, the information is ignored.Data type: String

</td></tr><tr><td>

sysparm\_view

</td><td>

UI view for which to render the data. Determines the fields returned in the response.Valid values:

-   desktop
-   mobile
-   both

If you also specify the **sysparm\_fields** parameter, it takes precedent.

Data type: String

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

|Status code|Description|
|-----------|-----------|
|200|Returns a list of catalogs and items based on the specified parameters. If a valid query results in no items, then the response body contains only an empty result array.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalogs

</td><td>

List of objects that describe the catalogs that contain this item.Data type: Array

 ```
"catalogs": [{
  "sys_id": "String",
  "title": "String"
}]
```

</td></tr><tr><td>

catalogs.sys\_id

</td><td>

Sys\_id of the catalog.Data type: String

</td></tr><tr><td>

catalogs.title

</td><td>

Catalog title.Data type: String

</td></tr><tr><td>

category

</td><td>

Describes the category that contains this item.Data type: Object

 ```
"catalogs": {
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr><td>

category.sys\_id

</td><td>

Sys\_id of the category.Data type: String

</td></tr><tr><td>

category.title

</td><td>

Category titleData type: String

</td></tr><tr><td>

content\_type

</td><td>

Type of content.Data type: String

</td></tr><tr><td>

description

</td><td>

Detailed description of the item.Data type: String

</td></tr><tr><td>

icon

</td><td>

Source of the small icon displayed beside the item name.Data type: String

</td></tr><tr><td>

kb\_article

</td><td>

Knowledge based article associated with the item.Data type: String

</td></tr><tr><td>

local\_currency

</td><td>

Country currency code for the local currency.Data type: String

</td></tr><tr><td>

localized\_price

</td><td>

Price of the item expressed in the currency defined by **local\_currency**.Data type: String

</td></tr><tr><td>

localized\_recurring\_price

</td><td>

Price of the recurring fee expressed in the currency defined by **local\_currency**.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the item.Data type: String

</td></tr><tr><td>

order

</td><td>

Pre-defined order to which the item belongs.Data type: Number

</td></tr><tr><td>

picture

</td><td>

Path to the image to display for the item.Data type: String

</td></tr><tr><td>

price

</td><td>

Price of item expressed in the currency defined by **price\_currency**.Data type: String

</td></tr><tr><td>

price\_currency

</td><td>

Country currency code for which the item price is expressed.Data type: String

</td></tr><tr><td>

recurring\_frequency

</td><td>

Frequency at which the recurring fees are applied, such as daily, monthly, or yearly; null if there are no fees for the item.Data type: String

</td></tr><tr><td>

recurring\_price

</td><td>

Amount of the recurring fee associated with the item.Data type: String

</td></tr><tr><td>

recurring\_price\_currency

</td><td>

Country currency code for which the recurring fees are expressed.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief description of the item.Data type: String

</td></tr><tr><td>

show\_price

</td><td>

Flag that indicates whether to show item pricing in the cart. Possible values:

-   true: Name-value pairs are returned in the response parameters.
-   false: Name-value pairs are not returned in the response parameters.

 Data type: Boolean

</td></tr><tr><td>

show\_quantity

</td><td>

Flag that indicates whether to display the item quantity in the cart.Possible values:

-   true: Display the item quantity in the cart.
-   false: Do not display the item quantity in the cart.

 Data type: Boolean

</td></tr><tr><td>

sys\_class\_name

</td><td>

Table to which the record belongs, such as sc\_cat\_item\_producer.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the item.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of item.Data type: String

</td></tr><tr><td>

url

</td><td>

URL of the item.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/items?sysparm_catalog=e0d08b13c3330100c8b837659bba8fb4&sysparm_limit=2" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": [
    {
      "short_description": null,
      "kb_article": "",
      "icon": "images/icons/catalog_item.gifx",
      "description": "<p class=\"p1\"><font size=\"2\"><span class=\"s1\">Request an existing Standard Change Template is made unavailable when it is no longer required or no longer acceptable as a Standard Change.  This will be confirmed by your Change Management team.</span></font></p>",
      "show_price": false,
      "type": "record_producer",
      "show_quantity": true,
      "sys_class_name": "sc_cat_item_producer",
      "picture": "",
      "url": "",
      "sys_id": "011f117a9f3002002920bde8132e7020",
      "content_type": "",
      "catalogs": [
        {
          "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
          "title": "Service Catalog"
        }
      ],
      "name": "Retire a Standard Change Template",
      "category": {
        "sys_id": "00728916937002002dcef157b67ffb6d",
        "title": "Template Management"
      },
      "order": 30
    },
    {
      "short_description": null,
      "kb_article": "",
      "icon": "4cc3ec3d471211002ee987e8dee490d0.iix",
      "description": "<p><font size=\"3\" color=\"#808080\" face=\"arial,helvetica,sans-serif\">A role delegator may delegate any role they have to any member of the specified group</font></p>",
      "show_price": false,
      "type": "record_producer",
      "show_quantity": true,
      "sys_class_name": "sc_cat_item_producer",
      "picture": "ed44b5804f889200086eeed18110c7ca.iix",
      "url": "",
      "sys_id": "01205b180a0a0b3000b6efd641d24b75",
      "content_type": "",
      "catalogs": [
        {
          "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
          "title": "Service Catalog"
        }
      ],
      "name": "Grant role delegation rights within a group",
      "category": {
        "sys_id": "496a3a7e0a0a0bc00089b39df14eb56e",
        "title": "Role Delegation"
      },
      "order": 100
    }
  ]
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/items/\{item\_sys\_id\}/delegation/\{user\_sys\_id\}

Verifies whether the specified delegated user has acquisition rights to the specified service catalog item.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{item_sys_id}/delegation/{user_sys_id}`

Default URL: `/api/sn_sc/servicecatalog/items/{item_sys_id}/delegation/{user_sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

item\_sys\_id

</td><td id="entry-item_sys_id-servcat">

Sys\_id of the service catalog item to verify whether the specified user has acquisition rights.Data type: String

Table: Service Catalog \[sc\_catalog\]

</td></tr><tr><td>

user\_sys\_id

</td><td>

Sys\_id of the user to check whether they have acquisition rights to the specified service catalog item.Data type: String

Table: Users \[sys\_users\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Flag that indicates whether the specified user has acquisition rights to the specified service catalog item.Valid values:

-   true: User has acquisition rights.
-   false: User does not have acquisition rights.

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/items/5c7e9fd20f1010108af26b198b767eb8/delegation/62826bf03710200044e0bfc8bcbe5df1" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "result": true
  }
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/items/\{sys\_id\}

Retrieves a specified catalog item.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{sys_id}`

Default URL: `/api/sn_sc/servicecatalog/items/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the catalog item to return.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_view

</td><td>

UI view for which to render the data. Determines the fields returned in the response.Valid values:

-   desktop
-   mobile
-   both

If you also specify the **sysparm\_fields** parameter, it takes precedent.

Data type: String

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

</td><td>

Indicates that the request has completed successfully and returns the details of the catalog item.

</td></tr><tr><td>

400

</td><td>

Indicates that request is invalid for one of the following reasons:-   User does not have access to the catalog item.
-   Invalid sys\_id.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalogs

</td><td>

List of objects that describe the catalogs that contain this item.Data type: Array

 ```
"catalogs": [{
  "sys_id": "String",
  "title": "String"
}]
```

</td></tr><tr><td>

catalogs.sys\_id

</td><td>

Sys\_id of the catalog.Data type: String

</td></tr><tr><td>

catalogs.title

</td><td>

Catalog title.Data type: String

</td></tr><tr><td>

categories

</td><td>

List of objects that describe the categories that contains this item.Data type: Array

 ```
"categories": [{
  "active": Boolean,
  "category": {Object},
  "sys_id": "String",
  "title": "String"
}]
```

</td></tr><tr><td>

categories.active

</td><td>

Flag that indicates whether the category is active.Possible values:

-   true: Category is active.
-   false: Category is inactive.

 Data type: Boolean

</td></tr><tr><td>

categories.category

</td><td>

Describes the associated category.Data type: Object

 ```
"category": {
  "active": Boolean,
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr><td>

categories.category.active

</td><td>

Flag that indicates whether the category is active.Possible values:

-   true: Category is active.
-   false: Category is inactive.

 Data type: Boolean

</td></tr><tr><td>

categories.category.sys\_id

</td><td>

Sys\_id of the category.Data type: String

</td></tr><tr><td>

categories.category.title

</td><td>

Category title.Data type: String

</td></tr><tr><td>

categories.sys\_id

</td><td>

Parent category of the category specified in **categories.category**.Data type: String

</td></tr><tr><td>

category

</td><td>

Primary category to which the item belongs.Data type: Object

 ```
"category": {
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr><td>

category.sys\_id

</td><td>

Sys\_id of the primary category.Data type: String

</td></tr><tr><td>

category.title

</td><td>

Primary category's title.Data type: String

</td></tr><tr><td>

client\_script

</td><td>

List of all the catalog client scripts defined on the catalog item.Data type: Object

 ```
"client_script": {
  "onChange": [Array],
  "onLoad": [Array],
  "onSubmit": [Array]
}
```

</td></tr><tr><td>

client\_script.onChange

</td><td>

List of onChange client scripts associated with the item.Data type: Array

</td></tr><tr><td>

client\_script.onSubmit

</td><td>

List of onSubmit client scripts associated with the item.Data type: Array

</td></tr><tr><td>

client\_script.onLoad

</td><td>

List of onLoad client scripts associated with the item.Data type: Array

</td></tr><tr><td>

content\_type

</td><td>

Type of content.Data type: String

</td></tr><tr><td>

data\_lookup

</td><td>

List of data lookups defined on the catalog item.Data type: Array

</td></tr><tr><td>

description

</td><td>

Detailed description of the item.Data type: String

</td></tr><tr><td>

icon

</td><td>

Source of the small icon displayed beside the item name.Data type: String

</td></tr><tr><td>

kb\_article

</td><td>

Knowledge based article associated with the item.Data type: String

</td></tr><tr><td>

local\_currency

</td><td>

Country currency code for the local currency.Data type: String

</td></tr><tr><td>

localized\_price

</td><td>

Price of the item expressed in the currency defined by **local\_currency**.Data type: String

</td></tr><tr><td>

localized\_recurring\_price

</td><td>

Price of the recurring fee expressed in the currency defined by **local\_currency**.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the item.Data type: String

</td></tr><tr><td>

order

</td><td>

Number of orders for the item.Data type: Number

</td></tr><tr><td>

picture

</td><td>

File name of the image to display for the item.Data type: String

</td></tr><tr><td>

price

</td><td>

Price of item expressed in the currency defined by **price\_currency**.Data type: String

</td></tr><tr><td>

price\_currency

</td><td>

Country currency code for which the item price is expressed.Data type: String

</td></tr><tr><td>

recurring\_frequency

</td><td>

Frequency at which the recurring fees are applied, such as daily, monthly, or yearly.Data type: String

</td></tr><tr><td>

recurring\_price

</td><td>

Amount of the recurring fee associated with the itemData type: String

</td></tr><tr><td>

recurring\_price\_currency

</td><td>

Country currency code for which the recurring fees are expressed.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Brief description of the item.Data type: String

</td></tr><tr><td>

show\_price

</td><td>

Flag that indicates whether to show item pricing in the cart.Possible values:

-   true: Pricing name/value pairs are returned in the response parameters.
-   false: Pricing name/value pairs are not returned in the response parameters.

 Data type: Boolean

</td></tr><tr><td>

show\_quantity

</td><td>

Flag that indicates whether to display the item quantity in the cart.Possible values:

-   true: Display the item quantity in the cart.
-   false: Do not display the item quantity in the cart.

 Data type: Boolean

</td></tr><tr><td>

sys\_class\_name

</td><td>

Name of the table to which this record belongs.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the item.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of item.Data type: String

</td></tr><tr><td>

ui\_policy

</td><td>

List of UI policies associated with the item.Data type: Array

</td></tr><tr><td>

url

</td><td>

URL of item image.Data type: String

</td></tr><tr><td>

variables

</td><td>

List of available variables associated with the item.Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/items/0cf7477237153000158bbfc8bcbe5dec" \
  --request GET \
  --header "Accept:application/json" \
  --user "username":"password"
```

```
{
  "result": {
    "short_description": "Apple iPad 3",
    "kb_article": "",
    "icon": "e6b3bc0647311200e0ef563dbb9a71fc.iix",
    "description": "\n\t\t\t<p>\n\t\t\t\t<font size=\"3\">\n\t\t\t\t\t<span style=\"color: gray;\">\n\t\t\t\t\t\tiPad with Retina display Wi-Fi 16GB - Black </span>\n\t\t\t\t</font>\n\t\t\t</p>\n\t\t\t<p>\n\t\t\t\t<span style=\"color: gray;\">Key Features:</span>\n\t\t\t</p>\n\t\t\t<ul><li style=\"color: gray;\">\n\t\t\t\t\t<span style=\"font-size: 10.0pt;\">Retina display (2048x1536 resolution)</span>\n\t\t\t\t</li><li style=\"color: gray;\">\n\t\t\t\t\t<span style=\"font-size: 10.0pt;\">16GB storage</span>\n\t\t\t\t</li><li style=\"color: gray;\">\n\t\t\t\t\t<span style=\"font-size: 10.0pt;\">Wi-Fi enabled</span>\n\t\t\t\t</li><li style=\"color: gray;\">\n\t\t\t\t\t<span style=\"font-size: 10.0pt;\">Built-in speaker, microphone and camera</span>\n\t\t\t\t</li><li style=\"color: gray;\">\n\t\t\t\t\t<span style=\"font-size: 10.0pt;\">Up to 10 hours battery life</span>\n\t\t\t\t</li></ul>",
    "show_price": true,
    "recurring_price": "$0.00",
    "type": "catalog_item",
    "show_quantity": true,
    "local_currency": "USD",
    "sys_class_name": "pc_hardware_cat_item",
    "picture": "5b977690cb921200f2de77a4634c9c6a.iix",
    "url": "",
    "sys_id": "060f3afa3731300054b6a3549dbe5d3e",
    "recurring_price_currency": "USD",
    "content_type": "",
    "localized_price": "$600.00",
    "price": "$600.00",
    "catalogs": [
      {
        "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
         "title": "Service Catalog"
      }
    ],
    "recurring_frequency": null,
    "name": "Apple iPad 3",
    "localized_recurring_price": "$0.00",
    "category": {
      "sys_id": "b06546f23731300054b6a3549dbe5dd8",
      "title": "Tablets"
    },
    "price_currency": "USD",
    "order": 0,
    "categories": [
      {
        "sys_id": "d258b953c611227a0146101fb1be7c31",
        "active": true,
        "category": {
          "sys_id": "b06546f23731300054b6a3549dbe5dd8",
          "active": true,
          "title": "Tablets"
        },
        "title": "Hardware"
      }
    ],
    "variables": [],
    "ui_policy": [],
    "client_script": {
      "onChange": [],
      "onSubmit": [],
      "onLoad": []
    },
    "data_lookup": []
  }
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/wishlist

Retrieves the list of items in the logged in user's wish list.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/wishlist`

Default URL: `/api/sn_sc/servicecatalog/wishlist`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

|Name|Description|
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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_id

</td><td>

Sys\_id of the wish list cart.Data type: String

</td></tr><tr><td>

items

</td><td>

List of objects that describe the items in the wish list cart.Data type: Array

 ```
"items": [{
  "cart_item_id": "String",
  "catalog_item_id": "String",
  "created_by": "String",
  "created_on": "String",
  "delivery_time": "String",
  "item_id": "String",
  "item_name": "String",
  "localized_price": "String",
  "localized_recurring_price": "String",
  "name": "String",
  "order_guide": "String",
  "picture": "String",
  "price": "String",
  "quantity": "String",
  "recurring_frequency": "String",
  "recurring_price": "String",
  "recurring_subtotal": Number,
  "recurring_subtotal_price": "String",
  "short_descriptions": "String",
  "show_price": Boolean,
  "show_quantity": Boolean,
  "show_recurring_price": Boolean,
  "subtotal": Number,
  "subtotal_price": "String",
  "sys_class_name": "String",
  "sys_id": "String",
  "updated_by": "String",
  "updated_on": "String",
  "variables": {Object}
}]
```

</td></tr><tr><td>

items.cart\_item\_id

</td><td>

Sys\_id of the item. Same as **items.sys\_id**.Data type: String

</td></tr><tr><td>

items.catalog\_item\_id

</td><td>

Sys\_id of the catalog identifier for this item in the wish list cart. Same as **items.item\_id**.Data type: String

</td></tr><tr><td>

items.created\_by

</td><td>

User that initially put the item in the wish list cart.Data type: String

</td></tr><tr><td>

items.created\_on

</td><td>

Date and time that the item was initially placed in the wishlist cart.Data type: String

</td></tr><tr><td>

items.delivery\_time

</td><td>

Amount of time that it takes to deliver the item.Data type: String

</td></tr><tr><td>

items.item\_id

</td><td>

Unique catalog identifier for this item in the wish list cart \(sys\_id\). Same as items.catalog\_item\_id.Data type: String

</td></tr><tr><td>

items.item\_name

</td><td>

Name of the item.Data type: String

</td></tr><tr><td>

items.localized\_price

</td><td>

Price of the item expressed in the local currency.Data type: String

</td></tr><tr><td>

items.localized\_recurring\_price

</td><td>

Price of the recurring fee expressed in the local currency.Data type: String

</td></tr><tr><td>

items.name

</td><td>

Name of the item.Data type: String

</td></tr><tr><td>

items.order\_guide

</td><td>

Order guide to which the item is associated.Data type: String

</td></tr><tr><td>

items.picture

</td><td>

Path to the image to display for the item.Data type: String

</td></tr><tr><td>

items.price

</td><td>

Price of item.Data type: String

</td></tr><tr><td>

items.quantity

</td><td>

Number of this item in the wish list cart.Data type: String

</td></tr><tr><td>

items.recurring\_frequency

</td><td>

Frequency at which the recurring fees are applied, such as daily, monthly, or yearly. Null if no recurring fees for this item.Data type: String

</td></tr><tr><td>

items.recurring\_price

</td><td>

Amount of the recurring fee associated with the item.Data type: String

</td></tr><tr><td>

items.recurring\_subtotal

</td><td>

Subtotal for the recurring fees for this item \(recurring\_price x quantity\).Data type: Number

</td></tr><tr><td>

items.recurring\_subtotal\_price

</td><td>

Subtotal for the recurring fees for this item \(recurring\_price x quantity\).Data type: String

</td></tr><tr><td>

items.short\_description

</td><td>

Brief description of the item.Data type: String

</td></tr><tr><td>

items.show\_price

</td><td>

Flag that indicates whether to show item pricing in the cart. If this parameter is set to "false", pricing name/value pairs are not returned in the response parameters.Data type: Boolean

</td></tr><tr><td>

items.show\_quantity

</td><td>

Flag that indicates whether to display the item quantity in the cart.Data type: Boolean

</td></tr><tr><td>

items.show\_recurring\_price

</td><td>

Flag that indicates whether to display the recurring fees in the cart.Data type: Boolean

</td></tr><tr><td>

items.subtotal

</td><td>

Subtotal for this item - not including cents \(price x quantity\).Data type: Number

</td></tr><tr><td>

items.subtotal\_price

</td><td>

Subtotal for this item - including cents \(price x quantity\).Data type: String

</td></tr><tr><td>

items.sys\_class\_name

</td><td>

Child class to which the associated item record belongs.Data type: String

</td></tr><tr><td>

items.sys\_id

</td><td>

Unique identifier of the item \(sys\_id\). Same as items.cart\_item\_id.Data type: String

</td></tr><tr><td>

items.updated\_by

</td><td>

User that updated this item in the wish list cart.Data type: String

</td></tr><tr><td>

items.updated\_on

</td><td>

Date and time that the item was put on the wishlist.Data type: String

</td></tr><tr><td>

items.variables

</td><td>

Name-value pairs of variables associated with the item.Data type: Object

</td></tr></tbody>
</table>### cURL request

```
curl "http://instance.servicenow.com/api/sn_sc/servicecatalog/wishlist" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "result": {
    "cart_id": "3a68c46013f12300027879d96144b0ce",
    "items": [
      {
        "updated_on": "2018-11-16 05:54:41",
        "catalog_item_id": "774906834fbb4200086eeed18110c737",
        "short_description": "Macbook Pro",
        "recurring_subtotal_price": "$100.00",
        "delivery_time": "5 Days 0 seconds",
        "sys_class_name": "sc_cat_item",
        "sys_id": "3b8d887113b5a300027879d96144b0c2",
        "price": "$1,499.00",
        "recurring_frequency": "Annually",
        "subtotal_price": "$1,499.00",
        "variables": {
          "Adobe Photoshop": "false",
          "Adobe Acrobat": "false",
          "Optional Software": "true",
          "Additional software requirements": "",
          "Eclipse IDE": "true"
        },
        "quantity": "1",
        "item_id": "774906834fbb4200086eeed18110c737",
        "recurring_price": "$100.00",
        "show_price": true,
        "item_name": "Developer Laptop (Mac)",
        "cart_item_id": "3b8d887113b5a300027879d96144b0c2",
        "recurring_subtotal": 100,
        "show_quantity": true,
        "created_by": "admin",
        "picture": "4e4efd444f889200086eeed18110c7e6.iix",
        "created_on": "2018-11-16 05:54:41",
        "localized_price": "$1,499.00",
        "subtotal": 1499,
        "show_recurring_price": true,
        "name": "Developer Laptop (Mac)",
        "updated_by": "admin",
        "localized_recurring_price": "$100.00",
        "order_guide": ""
      }
    ]
  }
}
```

## Service Catalog - GET /sn\_sc/servicecatalog/wishlist/\{cart\_item\_id\}

Retrieves the details of the specified item stored in the wish list cart.

### URL format

Versioned URL: `/api/sn_sc/v1/servicecatalog/wishlist/{cart_item_id}`

Default URL: `/api/sn_sc/servicecatalog/wishlist/{cart_item_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_item\_id

</td><td>

Sys\_id of the wish list cart item to retrieve.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Indicates a failed request. Incorrect cart item id or the item does not exist in the wish list cart.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_item\_id

</td><td>

Sys\_id of the item.Data type: String

</td></tr><tr><td>

catalog\_item\_id

</td><td>

Sys\_id of the catalog identifier for this item in the wish list cart.Data type: String

</td></tr><tr><td>

delivery\_time

</td><td>

Amount of time that it takes to deliver the item.Data type: String

</td></tr><tr><td>

item\_name

</td><td>

Name of the item.Data type: String

</td></tr><tr><td>

localized\_price

</td><td>

Price of the item expressed in the local currency.Data type: String

</td></tr><tr><td>

localized\_recurring\_price

</td><td>

Price of the recurring fee expressed in the local currency.Data type: String

</td></tr><tr><td>

price

</td><td>

Price of item.Data type: String

</td></tr><tr><td>

quantity

</td><td>

Number of this item in the wish list cart.Data type: String

</td></tr><tr><td>

recurring\_frequency

</td><td>

Frequency at which the recurring fees are applied, such as daily, monthly, or yearly. Null if no recurring fees for this item.Data type: String

</td></tr><tr><td>

recurring\_price

</td><td>

Amount of the recurring fee associated with the item.Data type: String

</td></tr><tr><td>

variables

</td><td>

Name-value pairs of the variables associated with the item.Data type: Object

</td></tr></tbody>
</table>### cURL request

```
curl "http://instance.servicenow.com/api/sn_sc/servicecatalog/wishlist/774906834fbb4200086eeed18110c737" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "catalog_item_id": "04b7e94b4f7b4200086eeed18110c7fd",
    "variables": {
      "Adobe Photoshop": "",
      "Adobe Acrobat": "",
      "Optional Software": "",
      "Additional software requirements": ""
    },
    "quantity": "1",
    "localized_price": "$1,100.00",
    "price": "$1,100.00",
    "recurring_frequency": "Annually",
    "localized_recurring_price": "$100.00",
    "recurring_price": "$100.00",
    "item_name": "Standard Laptop &",
    "cart_item_id": "d31be364c3012200d68d3b0ac3d3aecf",
    "delivery_time": "5 Days"
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/cart/checkout

Retrieves and processes the checkout for the current cart based on whether the two-step checkout process is enabled.

If one-step checkout, the method checks out \(saves\) the cart and returns the request number and the request order ID. If two-step checkout, the method returns the cart order status and all the information required for two-step checkout.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/cart/checkout`

Default URL: `/api/sn_sc/servicecatalog/cart/checkout`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

|Name|Description|
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

</td><td>

Indicates that the request completed successfully. Returns the total and subtotal information and information on the items in the cart. If one-step checkout, the method checks out \(saves\) the cart and returns the request number and the request order ID. If two-step checkout, the method returns the cart order status and all the information required for two-step checkout.

</td></tr><tr><td>

400

</td><td>

Indicates that the cart is empty and cannot check out.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_id

</td><td>

Sys\_id of the cart.Data type: String

</td></tr><tr><td>

delivery\_address

</td><td>

Address to which to deliver the cart items.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;

</td><td>

List of items in the cart having a specific recurring frequency. Possible values include:-   daily
-   monthly
-   yearly
-   none \(no recurring fees\)

 Data type: Object

 ```
"<recurring_frequency>": {
  "frequency_label": "String",
  "items": [Array],
  "show_subtotal_price": "String",
  "subtotal_price": "String",
  "subtotal_recurring_frequency": "String",
  "subtotal_recurring_price": "String",
  "subtotal_title": "String",
  "total_title": "String"
}
```

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.frequency\_label

</td><td>

Frequency of the associated recurring fee. If there are no recurring fees for the item, this parameter contains "null".Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items

</td><td>

Array of objects that contains details of each item associated with the specified recurring frequency category.Data type: Array

 ```
"items": [{
  "cart_item_id": "String",
  "catalog_item_id": "String",
  "created.by": "String",
  "created_on": "String",
  "delivery_time": "String",
  "item_id": "String",
  "item_name": "String",
  "localized_price": "String",
  "localized_recurring_price": "String",
  "name": "String",
  "order_guide": "String",
  "picture": "String",
  "price": "String",
  "quantity": "String",
  "recurring_frequency": "String",
  "recurring_price": "String",
  "recurring_subtotal": Number,
  "recurring_subtotal_price": "String",
  "short_description": "String",
  "show_price": Boolean,
  "show_quantity": Boolean,
  "show_recurring_price": Boolean,
  "subtotal": Number,
  "subtotal_price": "String",
  "sys_class_name": "String",
  "sys_id": "String",
  "updated_by": "String",
  "updated_on": "String",
  "variables": {Object}
}]
```

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.cart\_item\_id

</td><td>

Sys\_id of the item in this cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.catalog\_item\_id

</td><td>

Catalog sys\_id of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.created.by

</td><td>

User that initially placed the item in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.created\_on

</td><td>

Date on which the item was initially placed in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.delivery\_time

</td><td>

Time that the specified item takes to be delivered.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.item\_id

</td><td>

Sys\_id of the item. Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.item\_name

</td><td>

Name of the specified item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.localized\_price

</td><td>

Price of the item in local currency.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.localized\_recurring\_price

</td><td>

Recurring fee for the specified item in local currency.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.name

</td><td>

Item name.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.order\_guide

</td><td>

Name of the order guide to which this item is associated. If this item is not associated with an order guide this parameter contains an empty string.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.picture

</td><td>

File name of the picture of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.price

</td><td>

Price of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.quantity

</td><td>

Number of the specified item in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_frequency

</td><td>

How often the recurring fee is charged for the specified item. If there are no recurring fees for the item, this parameter contains "null".Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_price

</td><td>

Recurring fee for the specified item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_subtotal

</td><td>

Subtotal of the recurring fees for the item \(**recurring\_price** x **quantity**\).Data type: Number

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_subtotal\_price

</td><td>

Subtotal of the recurring fees for the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.short\_description

</td><td>

Short description of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_price

</td><td>

Flag that indicates whether the price of the item is shown in the cart.Possible values:

-   true: Show the price of the item in the cart.
-   false: Do not show the price of the item in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_quantity

</td><td>

Flag that indicates whether to show the item quantity in the cart.Possible values:

-   true: Show the item quantity in the cart.
-   false: Do not show the item quantity in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_recurring\_price

</td><td>

Flag that indicates whether the recurring fees should appear in the cart.Possible values:

-   true: Show the recurring fees in the cart.
-   false: Do not show the recurring fees in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.subtotal

</td><td>

Subtotal number of items.Data type: Number

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.subtotal\_price

</td><td>

Subtotal for the item \(**price** x **quantity**\).Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.sys\_class\_name

</td><td>

System classification name of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.sys\_id

</td><td>

Sys\_id of the item record.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.updated\_by

</td><td>

User that updated the item after it was initially placed in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.updated\_on

</td><td>

Last date/time on which the item was either initially placed in the cart or updated.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.variables

</td><td>

List of name-value pairs of the item variables.Data type: Object

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.show\_subtotal\_price

</td><td>

Flag that indicates whether to show a subtotal for the associated recurring fee category.Possible values:

-   true: Show subtotals in the cart.
-   false: Do not show subtotals in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_price

</td><td>

Subtotal of the cost of all items for the associated recurring frequency category.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_recurring\_frequency

</td><td>

Type of subtotal recurring frequency, such as daily, monthly, etc. Same as **subtotal\_recurring\_frequency**.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_recurring\_price

</td><td>

Subtotal of the recurring fees of the items within the associated recurring frequency category.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_title

</td><td>

If the **show\_subtotal\_price** is set to `true`, the text to display in the cart for the associated subtitle.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.total\_title

</td><td>

Text to display for the total title for the associated recurring frequency category.Data type: String

</td></tr><tr><td>

requested\_for

</td><td>

Sys\_id of the user for whom the item was ordered.Data type: String

</td></tr><tr><td>

requested\_for\_user

</td><td>

User that requested the item on behalf of someone else.Data type: String

</td></tr><tr><td>

show\_subtotal\_price

</td><td>

Flag that indicates whether to show the subtotal price in the cart.Possible values:

-   true: Show subtotals in the cart.
-   false: Do not show subtotals in the cart.

 Data type: String

</td></tr><tr><td>

special\_instructions

</td><td>

Any instructions given by the customer on the item.Data type: String

</td></tr><tr><td>

subtotal\_price

</td><td>

Subtotal of all items in the cart in whole dollars.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_frequency

</td><td>

Type of subtotal recurring frequency, such as daily, monthly, etc. Same as **&lt;recurring\_frequency&gt;.subtotal\_recurring\_frequency**.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_price

</td><td>

Subtotal of the recurring frequency fees for all items in the cart.Data type: String

</td></tr><tr><td>

subtotal\_title

</td><td>

Text to display in the cart for the subtotal field title.Data type: String

</td></tr><tr><td>

total\_title

</td><td>

Text to display in the cart for the total field title.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/cart/checkout" \
--request POST \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "cart_id": "0830db8413a56300397533e2e144b0ba",
    "subtotal_price": "$1,598.00",
    "subtotal_recurring_frequency": "",
    "delivery_address": "",
    "special_instructions": "",
    "subtotal_recurring_price": "$0.00",
    "total_title": "Total",
    "requested_for_user": "System Administrator",
    "none": {
      "subtotal_price": "$1,598.00",
      "subtotal_recurring_frequency": "",
      "subtotal_recurring_price": "$0.00",
      "total_title": "Total",
      "frequency_label": null,
      "items": [
        {
          "updated_on": "2018-11-06 17:01:21",
          "catalog_item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "short_description": "Apple iPhone 7 ",
          "recurring_subtotal_price": "$0.00",
          "delivery_time": "2 Days",
          "sys_class_name": "sc_cat_item",
          "sys_id": "a846872a1369e300027879d96144b07e",
          "price": "$799.00",
          "recurring_frequency": null,
          "subtotal_price": "$799.00",
          "variables": {},
          "quantity": "1",
          "item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "recurring_price": "$0.00",
          "show_price": true,
          "item_name": "Apple iPhone7",
          "cart_item_id": "a846872a1369e300027879d96144b07e",
          "recurring_subtotal": 0,
          "show_quantity": true,
          "created_by": "admin",
          "picture": "e823ee6b0bf00300eba42da0d5673a95.iix",
          "created_on": "2018-11-06 17:01:21",
          "localized_price": "$799.00",
          "subtotal": 799,
          "show_recurring_price": false,
          "name": "Apple iPhone7",
          "updated_by": "admin",
          "localized_recurring_price": "$0.00",
          "order_guide": ""
        },
        {
          "updated_on": "2018-11-06 17:34:15",
          "catalog_item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "short_description": "Apple iPhone 7 ",
          "recurring_subtotal_price": "$0.00",
          "delivery_time": "2 Days",
          "sys_class_name": "sc_cat_item",
          "sys_id": "7d138fa21329e300027879d96144b065",
          "price": "$799.00",
          "recurring_frequency": null,
          "subtotal_price": "$799.00",
          "variables": {},
          "quantity": "1",
          "item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "recurring_price": "$0.00",
          "show_price": true,
          "item_name": "Apple iPhone7",
          "cart_item_id": "7d138fa21329e300027879d96144b065",
          "recurring_subtotal": 0,
          "show_quantity": true,
          "created_by": "admin",
          "picture": "e823ee6b0bf00300eba42da0d5673a95.iix",
          "created_on": "2018-11-06 16:47:30",
          "localized_price": "$799.00",
          "subtotal": 799,
          "show_recurring_price": false,
          "name": "Apple iPhone7",
          "updated_by": "admin",
          "localized_recurring_price": "$0.00",
          "order_guide": ""
        }
      ],
      "show_subtotal_price": "true",
      "subtotal_title": "Subtotal"
    },
    "requested_for": "6816f79cc0a8016401c5a33be04be441",
    "show_subtotal_price": "true",
    "subtotal_title": "Subtotal"
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/cart/submit\_order

Checks out the user cart, based on the current check-out type \(one-step or two-step\).

If one-step checkout, the method checks out \(saves\) the cart and returns the request number and the request order ID. If two-step checkout, the method returns the cart order status and all the information required for two-step checkout.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/cart/submit_order`

Default URL: `/api/sn_sc/servicecatalog/cart/submit_order`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

|Name|Description|
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

</td><td>

Indicates that the request completed successfully and the items in the cart are successfully checked out.If one-step checkout, the method checks out \(saves\) the cart and returns the request number and the request order ID. If two-step checkout, the method returns the cart order status and all the information required for two-step checkout.

</td></tr><tr><td>

400

</td><td>

Indicates that the user cart is empty.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

parent\_id

</td><td>

If available, sys\_id of the parent record from which the request is created. For more information, see [Configure a parent mapping for a request](https://www.servicenow.com/docs/access?context=configure-mapping-for-request&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).Data type: String

</td></tr><tr><td>

parent\_table

</td><td>

Name of the parent table.Data type: String

</td></tr><tr><td>

request\_id

</td><td>

Sys\_id of the order request generated.Data type: String

</td></tr><tr><td>

request\_number

</td><td>

Number of the request generated.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com /api/sn_sc/v1/servicecatalog/cart/submit_order " \
--request POST \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "request_number": "REQ0010010",
    "request_id": "f89ed597db21120064301150f0b8f5ff"
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/items/\{sys\_id\}/add\_to\_cart

Adds the specified item to the cart of the current user.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{sys_id}/add_to_cart`

Default URL: `/api/sn_sc/servicecatalog/items/{sys_id}/add_to_cart`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the item to add to the current cart.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_also\_request\_for

</td><td id="entry-sysparm_also_request_for-servcat">

Comma-separated string of user sys\_ids of other users for which to order the specified item.-   You cannot specify more than 50 additional users to receive the item.
-   If any person in the list doesn't qualify for the item, the entire request is rejected.
-   If the associated item does not have the **requested\_for** variable set, the request is rejected.
-   If the associated item has the **requested\_for** variable set, but the **Enable also Request for** variable is not configured, or the calling user doesn’t have the proper roles, the request is rejected.

Table: User \[sys\_user\]

</td></tr><tr><td>

sysparm\_quantity

</td><td id="entry-sysparm_quantity-servcat">

Required. Quantity of the item. Cannot be a negative number.Data type: Number

</td></tr><tr><td>

sysparm\_requested\_for

</td><td>

Sys\_id of the user for whom to order the specified item.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

variables

</td><td id="entry-variables-servcat">

Name-value pairs of all mandatory cart item variables. Mandatory variables are defined on the associated form.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

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

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

The following errors can occur:-   Invalid quantity value: Indicates that either the **sysparm\_quantity** parameter is not provided or contains an invalid value.
-   Security constraints prevent ordering of Item: Indicates that either the cart item sys\_id specified in the path parameters is invalid or the user does not have access to the item.
-   Mandatory Variables are required: Indicates that one or more of the mandatory variables is not provided in the request.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_id

</td><td>

Cart sys\_id.Data type: String

</td></tr><tr><td>

items

</td><td>

Details of all of the items in the cart.Data type: Array

 ```
"items":[
  {
    "cart_item_id":"String",
    "catalog_item_id":"String",
    "item_name":"String",
    "localized_recurring_price":"String",
    "localized_price":"String",
    "price":"String",
    "quantity":"String",
    "recurring_frequency":"String",
    "recurring_price":"String"
  }
]
```

</td></tr><tr><td>

items.cart\_item\_id

</td><td>

Sys\_id of the item.Data type: String

</td></tr><tr><td>

items.catalog\_item\_id

</td><td>

Catalog sys\_id of the item.Data type: String

</td></tr><tr><td>

items.item\_name

</td><td>

Name of the item.Data type: String

</td></tr><tr><td>

items.localized\_price

</td><td>

Price of the item, in the user's local currency.Data type: String

</td></tr><tr><td>

items.localized\_recurring\_price

</td><td>

Recurring price of the item, in the user's local currency.Data type: String

</td></tr><tr><td>

items.price

</td><td>

Base price.Data type: String

</td></tr><tr><td>

items.quantity

</td><td>

Quantity of the item in the cart.Data type: String

</td></tr><tr><td>

items.recurring\_frequency

</td><td>

Frequency at which the recurring price is applied.Data type: String

</td></tr><tr><td>

items.recurring\_price

</td><td>

Recurring price.Data type: String

</td></tr><tr><td>

subtotal

</td><td>

Subtotal of the items in the cart.Data type: String

</td></tr></tbody>
</table>### Sample cURL request and response

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/items/0d08837237153000158bbfc8bcbe5d02/add_to_cart" \
--request POST \
--header "Accept:application/json" \
--data "{ 'sysparm_quantity' : '1',
  'variables' : {
    'acrobat' : 'true'
  }
}" \
--user "username":"password"
```

```
{
  "result": {
    "cart_id": "0951c597db21120064301150f0b8f5cf",
    "subtotal": "$1,599.98",
    "items": [
      {
        "catalog_item_id": "0d08837237153000158bbfc8bcbe5d02",
        "quantity": "1",
        "localized_price": "$799.99",
        "price": "$799.99",
        "recurring_frequency": "Monthly",
        "localized_recurring_price": "$30.00",
        "recurring_price": "$29.00",
        "item_name": "Apple iPhone 5",
        "cart_item_id": "ac61c597db21120064301150f0b8f5f9"
      }
    ]
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/items/\{sys\_id\}/add\_to\_wishlist

Adds the specified item to the wish list cart.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{sys_id}/add_to_wishlist`

Default URL: `/api/sn_sc/ servicecatalog/items/{sys_id}/add_to_wishlist`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the item to add to the wish list. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Indicates a failed request. Invalid request data or the user cannot add item to the wish list.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

```
curl "http://instance.servicenow.com/api/sn_sc/servicecatalog/items/04b7e94b4f7b4200086eeed18110c7fd/add_to_wishlist" \
 --request POST \
 --header "Accept:application/json" \
 --header "Content-Type:application/json" \
 --data "{\"sysparm_quantity\":\"1\"}" \
 --user "username":"password"
```

```
{
  "result": {
    "cart_id": "02a559a7c3b02200d68d3b0ac3d3ae5d",
    "items": [
      {
        "catalog_item_id": "04b7e94b4f7b4200086eeed18110c7fd",
        "variables": {
          "Adobe Photoshop": "",
          "Adobe Acrobat": "",
          "Optional Software": "",
          "Additional software requirements": ""
        },
        "quantity": "1",
        "localized_price": "$1,100.00",
        "price": "$1,100.00",
        "recurring_frequency": "Annually",
        "localized_recurring_price": "$100.00",
        "recurring_price": "$100.00",
        "item_name": "Standard Laptop &",
        "cart_item_id": "d31be364c3012200d68d3b0ac3d3aecf",
        "delivery_time": "5 Days"
      }
    ]
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/items/\{sys\_id\}/checkout\_guide

Retrieves an array of contents requested for checkout.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{sys_id}/checkout_guide`

Default URL: `/api/sn_sc/servicecatalog/items/{sys_id}/checkout_guide`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the checkout guide for which to return the information.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

items

</td><td>

List of object that describe the items requested for checkout. Data type: Array

```
"items": [{
  "sys_id": "String",
  "sysparm_quantity": "String",
  "variables": {Object}
}]
```

</td></tr><tr><td>

items.sys\_id

</td><td>

Required. Sys\_id of the catalog item.Data type: String

</td></tr><tr><td>

items.sysparm\_quantity

</td><td>

Number of items.Data type: String

 Default: 1

</td></tr><tr><td>

items.variables

</td><td>

Name-value pairs of variables associated with the item.Data type: Object

 Default: No variables

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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

</td><td>

Indicates that the request has completed successfully.-   Is not two-step: Items are added to the cart and the cart contents are returned.
-   Is two-step: Returns the request number and request sys\_id after checkout.

</td></tr><tr><td>

400

</td><td>

Indicates that the request is invalid. Could be due to one of the following reasons:-   One or more items sent do not exist.
-   User does not have access to one or more of the items.
-   Mandatory variables of one or more items have not been answered. \(Only variables defined as mandatory are honored.\)
-   Quantity value is sent and is not a positive integer.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_id

</td><td>

Sys\_id of the cart.Data type: String

</td></tr><tr><td>

items

</td><td>

List of objects that contain details of all the items in the cart.Data type: Array

 ```
"items": [{
  "cart_item_id": "String",
  "catalog_item_id": "String",
  "delivery_time": "String",
  "item_name": "String",
  "localized_price": "String",
  "localized_recurring_price": "String",
  "price": "String",
  "quantity": "String",
  "recurring_frequency": "String",
  "recurring_price": "String",
  "variables": {Object}
}]
```

</td></tr><tr><td>

items.cart\_item\_id

</td><td>

Sys\_id of the item in the cart.Data type: String

</td></tr><tr><td>

items.catalog\_item\_id

</td><td>

Sys\_id of the catalog item in the cart.Data type: String

</td></tr><tr><td>

items.delivery\_time

</td><td>

Amount of time it takes to deliver the item.Data type: String

</td></tr><tr><td>

items.item\_name

</td><td>

Name of the item in the cart.Data type: String

</td></tr><tr><td>

items.localized\_price

</td><td>

Price of the item in local currency.Data type: String

</td></tr><tr><td>

items.localized\_recurring\_price

</td><td>

Recurring price of the item in local currency.Data type: String

</td></tr><tr><td>

items.price

</td><td>

Price of the item.Data type: String

</td></tr><tr><td>

items.quantity

</td><td>

Number of the item in the cart.Data type: String

</td></tr><tr><td>

items.recurring\_frequency

</td><td>

Recurring frequency of the item.Data type: String

</td></tr><tr><td>

items.recurring\_price

</td><td>

Recurring price of the item.Data type: String

</td></tr><tr><td>

items.variables

</td><td>

Name-value pairs associated with the item in the cart.Data type: Object

</td></tr><tr><td>

parent\_id

</td><td>

If available, the sys\_id of the parent record from which the request is created. For more information, see [Configure a parent mapping for a request](https://www.servicenow.com/docs/access?context=configure-mapping-for-request&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).Data type: String

</td></tr><tr><td>

parent\_table

</td><td>

Name of the parent table \(case sensitive\).Data type: String

</td></tr><tr><td>

request\_number

</td><td>

Request record number.Data type: String

</td></tr><tr><td>

request\_id

</td><td>

Sys\_id of the request.Data type: String

</td></tr><tr><td>

subtotal\_price

</td><td>

Cart subtotal.Data type: String

</td></tr><tr><td>

subtotal\_price

</td><td>

Subtotal of the current frequency block.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_frequency

</td><td>

Recurring frequency subtotal of the cart.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_frequency

</td><td>

Recurring frequency subtotal of the current frequency block.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_price

</td><td>

Recurring price subtotal of the cart.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_price

</td><td>

Recurring price subtotal of the current frequency blockData type: String

</td></tr><tr><td>

total\_title

</td><td>

Title for total field on page.Data type: String

</td></tr><tr><td>

total\_title

</td><td>

Title for total field on the current frequency block.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/v1/servicecatalog/items/6690750f4f7b4200086eeed18110c761/checkout_guide" \
--request POST \
--header "Accept:application/json"  \
--header "Content-Type:application/json" \
--data "{\"items\":[{
  \"sys_id\":\"04b7e94b4f7b4200086eeed18110c7fd\",
  \"variables\":{
    \"acrobat\":\"true\",
    \"Additional_software_requirements\":\"MS Office 2007\"
  },
  \"sysparm_quantity\":\"3\"
},
{
  \"sys_id\":\"e1be6dcb4f7b4200086eeed18110c74c\"
},
{
  \"sys_id\":\"186d917a6fab7980575967ddbb3ee4f2\",
  \"variables\":{
    \"new_email\":\"abel.tuter@example.com\"
  }
},
{
  \"sys_id\":\"8b3ae7fedc1be1004ece5c08239e522b\"
},
{
  \"sys_id\":\"962967674ff38200086eeed18110c7e7\",
  \"variables\":{
    \"ergonomic_office\":\"Office chair should have lumbar support\"
  }
}]}" \
--user "username":"password"
```

```
<!--Case-1: if two-step is false:-->
{
  "result": {
    "cart_id": "0d8c7a32c3211200d68d3b0ac3d3aeba",
    "subtotal_price": "$3,350.00",
    "subtotal_recurring_frequency": "",
    "subtotal_recurring_price": "$300.00",
    "total_title": "Total",
    "monthly": {
      "subtotal_price": "$50.00",
      "subtotal_recurring_frequency": "Monthly",
      "subtotal_recurring_price": "$0.00",
      "total_title": "Total",
      "items": [
        {
          "catalog_item_id": "90af095bcd38798071a208d710d1b64f",
          "variables": {},
          "quantity": "1",
          "localized_price": "$50.00",
          "price": "$50.00",
          "recurring_frequency": "Monthly",
          "localized_recurring_price": "$0.00",
          "recurring_price": "$0.00",
          "item_name": "Belkin iPad Mini Case",
          "cart_item_id": "cb6e485fc3211200d68d3b0ac3d3ae35",
          "delivery_time": "2 Days"
        }
      ],
      "show_subtotal_price": "true",
      "subtotal_title": "Subtotal"
    },
    "none": {
      "subtotal_price": "-",
      "subtotal_recurring_frequency": "",
      "subtotal_recurring_price": "$0.00",
      "total_title": "Total",
      "items": [
        {
          "catalog_item_id": "186d917a6fab7980575967ddbb3ee4f2",
          "variables": {
            "Preferred Email address": "abel.tuter@example.com"
          },
          "quantity": "1",
          "localized_price": "$0.00",
          "price": "$0.00",
          "recurring_frequency": "",
          "localized_recurring_price": "$0.00",
          "recurring_price": "$0.00",
          "item_name": "New Email Account",
          "cart_item_id": "17c5241fc3211200d68d3b0ac3d3ae7f",
          "delivery_time": "global.Workflow"
        },
        {
          "catalog_item_id": "8b3ae7fedc1be1004ece5c08239e522b",
          "variables": {},
          "quantity": "1",
          "localized_price": "$0.00",
          "price": "$0.00",
          "recurring_frequency": "",
          "localized_recurring_price": "$0.00",
          "recurring_price": "$0.00",
          "item_name": "Corp VPN",
          "cart_item_id": "97c5241fc3211200d68d3b0ac3d3ae7f",
          "delivery_time": "2 Days"
        },
        {
          "catalog_item_id": "e1be6dcb4f7b4200086eeed18110c74c",
          "variables": {},
          "quantity": "1",
          "localized_price": "$0.00",
          "price": "$0.00",
          "recurring_frequency": "",
          "localized_recurring_price": "$0.00",
          "recurring_price": "$0.00",
          "item_name": "External Monitor",
          "cart_item_id": "d3c5241fc3211200d68d3b0ac3d3ae7f",
          "delivery_time": "2 Days"
        },
        {
          "catalog_item_id": "962967674ff38200086eeed18110c7e7",
          "variables": {
            "Please describe any ergonomic requirements\n\t\t": "Office chair should have lumbar support"
          },
          "quantity": "1",
          "localized_price": "$0.00",
          "price": "$0.00",
          "recurring_frequency": "",
          "localized_recurring_price": "$0.00",
          "recurring_price": "$0.00",
          "item_name": "Desk Set Up",
          "cart_item_id": "d7c5241fc3211200d68d3b0ac3d3ae7f",
          "delivery_time": "5 Days"
        }
      ],
      "show_subtotal_price": "false",
      "subtotal_title": "Subtotal"
    },
    "yearly": {
      "subtotal_price": "$3,300.00",
      "subtotal_recurring_frequency": "Annually",
      "subtotal_recurring_price": "$300.00",
      "total_title": "Total",
      "items": [
        {
          "catalog_item_id": "04b7e94b4f7b4200086eeed18110c7fd",
          "variables": {
            "Adobe Photoshop": "",
            "Adobe Acrobat": "true",
            "Optional Software": "",
            "Additional software requirements": "MS Office 2007"
          },
          "quantity": "3",
          "localized_price": "$1,100.00",
          "price": "$1,100.00",
          "recurring_frequency": "Annually",
          "localized_recurring_price": "$100.00",
          "recurring_price": "$100.00",
          "item_name": "Standard Laptop",
          "cart_item_id": "9fc5241fc3211200d68d3b0ac3d3ae7e",
          "delivery_time": "5 Days"
        }
      ],
      "show_subtotal_price": "true",
      "subtotal_title": "Subtotal"
    },
    "show_subtotal_price": "true",
    "subtotal_title": "Subtotal"
  }
}

Case-2: if two-step is true:
{
  "result": {
    "request_number": "REQ0010001",
    "request_id": "82a7e89fc3211200d68d3b0ac3d3ae0a"
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/items/\{item\_sys\_id\}/get\_invalid\_delegated\_users

Returns a list of users whose request for the specified item cannot be delegated \(requested by another user\).

You can call this endpoint prior to calling an endpoint such as [Service Catalog API - POST /sn\_sc/servicecatalog/items/\{sys\_id\}/add\_to\_cart](c_ServiceCatalogAPI.md#) or [Service Catalog API - POST /sn\_sc/servicecatalog/items/\{sys\_id\}/order\_now](c_ServiceCatalogAPI.md#) that allow the requisition of a service catalog item on behalf of another person. These calls fail if you pass in a user that is not authorized for the associated item. This endpoint allows you to verify your list of users prior to calling an endpoint that orders the item or tries to add the item to a cart.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{item_sys_id}/get_invalid_delegated_users`

Default URL: `/api/sn_sc/servicecatalog/items/{item_sys_id}/get_invalid_delegated_users`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

item\_sys\_id

</td><td id="entry-item_sys_id-servcat">

Sys\_id of the service catalog item to verify whether the specified user has acquisition rights.Data type: String

Table: Service Catalog \[sc\_catalog\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_also\_request\_for

</td><td>

Comma separated string of valid user sys\_ids. The endpoint verifies that these users have acquisition rights to the specified service catalog item.Data type: String

Table: Users \[sys\_users\]

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Request failed. Bad request given for processing. Refer to the message in the return results for additional information on the error.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errCode

</td><td>

Number associated with the error. Only returned if the endpoint fails.Data type: String

</td></tr><tr><td>

errMsg

</td><td>

Description of the error that the endpoint encountered when it failed.

</td></tr><tr><td>

invalidUsers

</td><td>

Names of the users that are not able to request the specified catalog item.Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/items/04b7e94b4f7b4200086eeed18110c7fd/get_invalid_delegated_users" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"sysparm_also_request_for\":\"a8f98bb0eb32010045e1a5115206fe3a,62826bf03710200044e0bfc8bcbe5df1\"}" \
--user "username":"password"

```

```
{
  "result": {
    "invalidUsers": [
      "Abel Tuter"
    ]
  }
}
```

### cURL request

```
curl "https://instance.servicenow.com /api/sn_sc/servicecatalog/items/04b7e94b4f7b4200086eeed18110c7fd/get_invalid_delegated_users" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"sysparm_also_request_for\":\"a8f98bb0eb32010045e1a5115206fe3a,62826bf03710200044e0bfc8bcbe5df1\"}" \
--user "username":"password"
```

```
{
  "result": {
    "errCode": "42202",
    "errMsg": "This item cannot be submitted for multiple people as it is not configured with Requested For"
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/items/\{sys\_id\}/order\_now

Orders the specified catalog item.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{sys_id}/order_now`

Default URL: `/api/sn_sc/servicecatalog/items/{sys_id}/order_now`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the service catalog item.Data type: String

Table: Catalog Item \[sc\_cat\_item\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_also\_request\_for

</td><td id="entry-sysparm_also_request_for-servcat">

Comma-separated string of user sys\_ids of other users for which to order the specified item.-   You cannot specify more than 50 additional users to receive the item.
-   If any person in the list doesn't qualify for the item, the entire request is rejected.
-   If the associated item does not have the **requested\_for** variable set, the request is rejected.
-   If the associated item has the **requested\_for** variable set, but the **Enable also Request for** variable is not configured, or the calling user doesn’t have the proper roles, the request is rejected.

Table: User \[sys\_user\]

</td></tr><tr><td>

sysparm\_quantity

</td><td id="entry-sysparm_quantity-servcat">

Required. Quantity of the item. Cannot be a negative number.Data type: Number

</td></tr><tr><td>

sysparm\_requested\_for

</td><td>

Sys\_id of the user for whom to order the specified item.The settings of the **glide.sc.req\_for.roles** and **glide.sc.req\_for.roles.default** properties determine the level at which a user can request items.

-   If a value is specified in the **glide.sc.req\_for.roles** property, the system checks if the user has the specified role to request information of other users.
-   If the **glide.sc.req\_for.roles** property value is empty and the **glide.sc.req\_for.roles.default** property value is `deny`, no user can request items for other users.
-   If the **glide.sc.req\_for.roles** property value is empty and the **glide.sc.req\_for.roles.default** property value is `allow`, any user can request items for other users.

Data type: String

</td></tr><tr><td>

variables

</td><td id="entry-variables-servcat">

Name-value pairs of all mandatory cart item variables. Mandatory variables are defined on the associated form.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_kt4_4ph_nlb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Indicates that the quantity value is invalid and the request is not placed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

number

</td><td>

Number of the generated request.Data type: String

</td></tr><tr><td>

parent\_id

</td><td>

If available, the sys\_id of the parent record from which the request is created. For more information, see [Configure a parent mapping for a request](https://www.servicenow.com/docs/access?context=configure-mapping-for-request&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).Data type: String

</td></tr><tr><td>

parent\_table

</td><td>

If available, the name of the parent table from which the request is created.Data type: String

</td></tr><tr><td>

request\_id

</td><td>

Sys\_id of the order request.Data type: String

</td></tr><tr><td>

request\_number

</td><td>

Request number.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the order.Data type: String

</td></tr><tr><td>

table

</td><td>

Table name of the request.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/items/d82ea08510247200964f77ffeec6c4ee/order_now" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  sysparm_quantity: 1,
  variables: {
    replacement: 'Yes',
    originalnumber: '1640000',
    data_plan: '500MB'
  }
}" \
--user "username":"password"
```

```
{
  "result": {
    "sys_id": "cf56a3fcdb3a2300e890f71fbf9619ac",
    "number": "REQ0010012",
    "request_number": "REQ0010012",
    "request_id": "cf56a3fcdb3a2300e890f71fbf9619ac",
    "table": "sc_request"
  }
}
```

## Service Catalog - POST /sn\_sc/servicecatalog/items/\{sys\_id\}/submit\_producer

Creates a record and returns the Table API relative path and redirect URL to access the created record.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{sys_id}/submit_producer`

Default URL: `/api/sn_sc/servicecatalog/items/{sys_id}/submit_producer`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the table in which to create the record producer.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_view

</td><td>

UI view for which to render the data. Determines the fields returned in the response.Valid values:

-   desktop
-   mobile
-   both

If you also specify the **sysparm\_fields** parameter, it takes precedent.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|variables|Name-value pairs of the variables of the producer record to define.|

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Indicates successful request and returns the response object consisting of Table API and URL to access the created record.|
|400|Request is not processed due to incorrect request message.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Requested resource cannot be found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

number

</td><td>

Number of the ticket associated with the record producer.Data type: String

</td></tr><tr><td>

parent\_id

</td><td>

If available, sys\_id of the parent record from which the request is created. For more information, see [Configure a parent mapping for a request](https://www.servicenow.com/docs/access?context=configure-mapping-for-request&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).Data type: String

</td></tr><tr><td>

parent\_table

</td><td>

Name of the parent table.Data type: String

</td></tr><tr><td>

record

</td><td>

Table API relative path of the newly created record producer.Data type: String

</td></tr><tr><td>

redirect\_portal\_url

</td><td>

URL to which to redirect the Service Portal.Data type: String

</td></tr><tr><td>

redirect\_to

</td><td>

Redirect value.Data type: String

</td></tr><tr><td>

redirect\_url

</td><td>

Redirect URL to access the created record producer.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the record created.Data type: String

</td></tr><tr><td>

table

</td><td>

Name of the table on which the request was made.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/items/3f1dd0320a0a0b99000a53f7604a2ef9/submit_producer" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{'variables':{'urgency':'2','comments':'This is sample incident'}}" \
--user "username":"password"
```

```
{
  "result": {
    "sys_id": "6baf4e1ddbba2300e890f71fbf961963",
    "number": "INC0010006",
    "parent_id": null,
    "record": "api/now/table/incident/6baf4e1ddbba2300e890f71fbf961963",
    "redirect_portal_url": "",
    "parent_table": "task",
    "redirect_url": "incident.do?sys_id=6baf4e1ddbba2300e890f71fbf961963&sysparm_view=ess",
    "table": "incident",
    "redirect_to": ""
  }
}
```

## Service Catalog - POST /sn/sc/servicecatalog/variables/\{sys\_id\}/display\_value

Returns the display value of the specified variable.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/variables/{sys_id}/display_value`

Default URL: `/api/sn_sc/servicecatalog/variables/{sys_id}/display_value`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the variable for which to return the display value.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_value

</td><td>

Sys\_id of the record that contains the display value to return.Data type: String

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Display value of the variable.Data type: String

</td></tr></tbody>
</table>### cURL request

```

 curl "https://instance.servicenow.com/api/sn_sc/servicecatalog/variables/2a3947a10a0a020e007f12648f8790c0/display_value" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"sysparm_value\":\"62826bf03710200044e0bfc8bcbe5df1\"}" \ 
--user "username":"password" 
```

```
{
  "result": "Abel Tuter (Architect)"
}
```

## Service Catalog - PUT /sn\_sc/servicecatalog/cart/\{cart\_item\_id\}

Updates the specified item in the logged in user's cart.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/cart/{cart_item_id}`

Default URL: `/api/sn_sc/servicecatalog/cart/{cart_item_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

cart\_item\_id

</td><td>

Sys\_id of the cart item to update.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_quantity

</td><td>

Required. Quantity of the item to update the cart.Data type: String

</td></tr><tr><td>

variables

</td><td>

Required if there are mandatory variables specified for the item. Object consisting of all mandatory variable names-value pairs.Data type: Object

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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

201

</td><td>

Indicates that the request completed successfully and that the item is added to the cart.

</td></tr><tr><td>

400

</td><td>

Following three errors can occur:-   Invalid quantity value:Indicates that either the sysparm\_quantity parameter is not provided or contains invalid value.
-   Security constraints prevent ordering of Item:Indicates that either the item ID specified in the path parameters is either invalid or the user does not have access to the item.
-   Mandatory Variables are required:Indicates that one or more of the mandatory variable values is not provided in the request.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cart\_id

</td><td>

Sys\_id of the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;

</td><td>

Describes an items in the cart having a specific recurring frequency. Possible values include:

-   daily
-   monthly
-   yearly
-   none \(no recurring fees\)

 Data type: Object

 ```
"<recurring_frequency>": {
  "frequency_label": "String",
  "items": [Array],
  "show_subtotal_price": "String",
  "subtotal_price": "String",
  "subtotal_recurring_frequency": "String",
  "subtotal_recurring_price": "String",
  "subtotal_title": "String",
  "total_title": "String"
}
```

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.frequency\_label

</td><td>

Frequency of the associated recurring fee. If there are no recurring fees for the item, this parameter contains "null".Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items

</td><td>

List of objects that describe each item associated with the specified recurring frequency category.Data type: Array

 ```
"items": [{
  "cart_item_id": "String",
  "catalog_item_id": "String",
  "created.by": "String",
  "created_on": "String",
  "delivery_time": "String",
  "item_id": "String",
  "item_name": "String",
  "localized_price": "String",
  "localized_recurring_price": "String",
  "name": "String",
  "order_guide": "String",
  "picture": "String",
  "price": "String",
  "quantity": "String",
  "recurring_frequency": "String",
  "recurring_price": "String",
  "recurring_subtotal": Number,
  "recurring_subtotal_price": "String",
  "short_description": "String",
  "show_price": Boolean,
  "show_quantity": Boolean,
  "show_recurring_price": Boolean,
  "subtotal": Number,
  "subtotal_price": "String",
  "sys_class_name": "String",
  "sys_id": "String",
  "updated_by": "String",
  "updated_on": "String",
  "variables": {Object}
}]
```

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.cart\_item\_id

</td><td>

Sys\_id of the item in this cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.catalog\_item\_id

</td><td>

Catalog sys\_id of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.created.by

</td><td>

User that initially placed the item in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.created\_on

</td><td>

Date on which the item was initially placed in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.delivery\_time

</td><td>

Time that the specified item takes to be delivered.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.item\_id

</td><td>

Item sys\_id.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.item\_name

</td><td>

Name of the specified item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.localized\_price

</td><td>

Price of the item \(in local currency\).Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.localized\_recurring\_price

</td><td>

Recurring fee for the specified item \(in local currency\).Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.name

</td><td>

Item name.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.order\_guide

</td><td>

Name of the order guide to which this item is associated. If this item is not associated with an order guide this parameter contains an empty string.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.picture

</td><td>

File name of the picture of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.price

</td><td>

Price of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.quantity

</td><td>

Number of the specified item in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_frequency

</td><td>

How often the recurring fee is charged for the specified item.Data type: String

 Default: Null

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_price

</td><td>

Recurring fee for the specified item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_subtotal

</td><td>

Subtotal of the recurring fees for the item \(**recurring\_price** x **quantity**\).Data type: Number

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.recurring\_subtotal\_price

</td><td>

Subtotal of the recurring fees for the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.short\_description

</td><td>

Short description of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_price

</td><td>

Flag that indicates whether the price of the item is shown in the cart.Possible values:

-   true: Show the price of the item in the cart.
-   false: Do not show the price of the item in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show.quantity

</td><td>

Flag that indicates whether to show the item quantity in the cart.Possible values:

-   true: Show the item quantity in the cart.
-   false: Do not show the item quantity in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.show\_recurring\_price

</td><td>

Flag that indicates whether the recurring fees should appear in the cart.Possible values:

-   true: Show the recurring fees in the cart.
-   false: Do not show the recurring fees in the cart.

 Data type: Boolean

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.subtotal

</td><td>

Subtotal of the number of items.Data type: Number

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.subtotal\_price

</td><td>

Subtotal for the item \(**price** x **quantity**\).Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.sys\_class\_name

</td><td>

System classification name of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.sys\_id

</td><td>

Sys\_id of the item.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.updated\_by

</td><td>

User that updated the item after it was initially placed in the cart.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.updated\_on

</td><td>

Last date/time on which the item was either initially placed in the cart or updated.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.items.variables

</td><td>

Name-value pairs of the item variables.Data type: Object

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.show\_subtotal\_price

</td><td>

Flag that indicates whether to show a subtotal for the associated recurring fee category.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_price

</td><td>

Subtotal of the cost of all items for the associated recurring frequency category.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_recurring\_frequency

</td><td>

Type of subtotal recurring frequency, such as daily, monthly, etc.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_recurring\_price

</td><td>

Subtotal of the recurring fees of the items within the associated recurring frequency category.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.subtotal\_title

</td><td>

If the **show\_subtotal\_price** is set to `true`, the text to display in the cart for the associated subtitle.Data type: String

</td></tr><tr><td>

&lt;recurring\_frequency&gt;.total\_title

</td><td>

Text to display for the total title for the associated recurring frequency category.Data type: String

</td></tr><tr><td>

show\_subtotal\_price

</td><td>

Flag that indicates whether to show the subtotal price in the cart.Possible values:

-   true: Show subtotals in the cart.
-   false: Do not show subtotals in the cart.

 Data type: String

</td></tr><tr><td>

subtotal\_price

</td><td>

Subtotal of all items in the cart.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_frequency

</td><td>

Type of subtotal recurring frequency, such as daily, monthly, etc. Same as **&lt;recurring\_frequency&gt;.subtotal\_recurring\_frequency**.Data type: String

</td></tr><tr><td>

subtotal\_recurring\_price

</td><td>

Subtotal of the recurring frequency fees for all items in the cart.Data type: String

</td></tr><tr><td>

subtotal\_title

</td><td>

Text to display in the cart for the subtotal field title.Data type: String

</td></tr><tr><td>

total\_title

</td><td>

Text to display in the cart for the total field title.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/v1/servicecatalog/cart/7d138fa21329e300027879d96144b065" \
--request PUT \
--header "Accept:application/json" \
--data "{\"sysparm_quantity\": \"2\" }" \
--user "username":"password"
```

```
{
  "result": {
    "cart_id": "0830db8413a56300397533e2e144b0ba",
    "subtotal_price": "$2,397.00",
    "subtotal_recurring_frequency": "",
    "subtotal_recurring_price": "$0.00",
    "total_title": "Total",
    "none": {
      "subtotal_price": "$2,397.00",
      "subtotal_recurring_frequency": "",
      "subtotal_recurring_price": "$0.00",
      "total_title": "Total",
      "frequency_label": null,
      "items": [
        {
          "updated_on": "2018-11-06 17:01:21",
          "catalog_item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "short_description": "Apple iPhone 7 ",
          "recurring_subtotal_price": "$0.00",
          "delivery_time": "2 Days",
          "sys_class_name": "sc_cat_item",
          "sys_id": "a846872a1369e300027879d96144b07e",
          "price": "$799.00",
          "recurring_frequency": null,
          "subtotal_price": "$799.00",
          "variables": {},
          "quantity": "1",
          "item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "recurring_price": "$0.00",
          "show_price": true,
          "item_name": "Apple iPhone7",
          "cart_item_id": "a846872a1369e300027879d96144b07e",
          "recurring_subtotal": 0,
          "show_quantity": true,
          "created_by": "admin",
          "picture": "e823ee6b0bf00300eba42da0d5673a95.iix",
          "created_on": "2018-11-06 17:01:21",
          "localized_price": "$799.00",
          "subtotal": 799,
          "show_recurring_price": false,
          "name": "Apple iPhone7",
          "updated_by": "admin",
          "localized_recurring_price": "$0.00",
          "order_guide": ""
        },
        {
          "updated_on": "2018-11-06 17:21:08",
          "catalog_item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "short_description": "Apple iPhone 7 ",
          "recurring_subtotal_price": "$0.00",
          "delivery_time": "2 Days",
          "sys_class_name": "sc_cat_item",
          "sys_id": "7d138fa21329e300027879d96144b065",
          "price": "$799.00",
          "recurring_frequency": null,
          "subtotal_price": "$1,598.00",
          "variables": {},
          "quantity": "2",
          "item_id": "07f1666b0bf00300eba42da0d5673ab0",
          "recurring_price": "$0.00",
          "show_price": true,
          "item_name": "Apple iPhone7",
          "cart_item_id": "7d138fa21329e300027879d96144b065",
          "recurring_subtotal": 0,
          "show_quantity": true,
          "created_by": "admin",
          "picture": "e823ee6b0bf00300eba42da0d5673a95.iix",
          "created_on": "2018-11-06 16:47:30",
          "localized_price": "$799.00",
          "subtotal": 1598,
          "show_recurring_price": false,
          "name": "Apple iPhone7",
          "updated_by": "admin",
          "localized_recurring_price": "$0.00",
          "order_guide": ""
        }
      ],
      "show_subtotal_price": "true",
      "subtotal_title": "Subtotal"
    },
    "show_subtotal_price": "true",
    "subtotal_title": "Subtotal"
  }
}
```

## Service Catalog - PUT /sn\_sc/servicecatalog/items/\{sys\_id\}/submit\_guide

Retrieves a list of items based on the needs described for an order guide.

### URL format

Versioned URL: `/api/sn_sc/{api_version}/servicecatalog/items/{sys_id}/submit_guide`

Default URL: `/api/sn_sc/servicecatalog/items/{sys_id}/submit_guide`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

sys\_id

</td><td>

Sys\_id of the order guide whose items are to be retrieved.Data type: String

Table: Order guide \[sc\_cat\_item\_guide\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

variables

</td><td>

Variables requested for an item. Each variable is a JSON object consisting of name-value pairs. Data type: Array

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

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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

</td><td>

Indicates that the request has completed successfully. Returns a list of items based on the passed-in variable list. If the result set does not contain any items, then an empty array is returned.

</td></tr><tr><td>

400

</td><td>

Indicates that the request is invalid. Could be due to one of the following reasons:-   User does not have access to the item.
-   Mandatory variables of one or more items have not been answered. \(Only variables defined as mandatory are honored.\)

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td>

Internal error while calculating items depending on options chosen.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalogs

</td><td>

List of objects to which the item belongs and each catalog title and sys\_id of the catalog.Data type: Array of Objects

```
"catalogs": [
  {
    "sys_id": "String",
    "title": "String"  
  }
]
```

</td></tr><tr><td>

catalogs.sys\_id

</td><td>

Sys\_id of the catalog.Data type: String

</td></tr><tr><td>

catalogs.title

</td><td>

Catalog title.Data type: String

</td></tr><tr><td>

category

</td><td>

Category that contains this item.Data type: Object

```
"catalogs": {
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr><td>

category.sys\_id

</td><td>

Sys\_id of the category.Data type: String

</td></tr><tr><td>

category.title

</td><td>

Category titleData type: String

</td></tr><tr><td>

client\_script

</td><td>

List of all the catalog client scripts defined on the catalog item.Data type: Object

```
"client_script": {
  "onChange": [Array],
  "onLoad": [Array],
  "onSubmit": [Array]
}
```

</td></tr><tr><td>

client\_script.onChange

</td><td>

List of onChange client scripts associated with the item.Data type: Array

</td></tr><tr><td>

client\_script.onLoad

</td><td>

List of onLoad client scripts associated with the item.Data type: Array

</td></tr><tr><td>

client\_script.onSubmit

</td><td>

List of onSubmit client scripts associated with the item.Data type: Array

</td></tr><tr><td>

data\_lookup

</td><td>

Data lookups defined on the catalog item.Data type: Array

</td></tr><tr><td>

description

</td><td>

Full description of catalog item.Data type: String

</td></tr><tr><td>

icon

</td><td>

Path of the image that appears as an icon beside the catalog item.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the catalog item.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Text on the service catalog homepage or search results page, or the title on the order form of the catalog item.Data type: String

</td></tr><tr><td>

show\_price

</td><td>

Flag that indicates whether to show the price details. If true, returns the following details. -   local\_currency
-   localized\_price
-   localized\_recurring\_price
-   price
-   price\_currency
-   recurring\_frequency
-   recurring\_price
-   recurring\_price\_currency

Data type: Boolean

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the catalog item.Data type: String

</td></tr><tr><td>

type

</td><td>

Item type. Possible values:

-   catalog item
-   order guide
-   record producer item

Data type: String

</td></tr><tr><td>

variables

</td><td>

Name-value pairs of all the variables associated with the catalog item.Data type: Array

</td></tr><tr><td>

ui\_policy

</td><td>

List of all catalog UI policies defined on the catalog item.Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_sc/v1/servicecatalog/items/6690750f4f7b4200086eeed18110c761/submit_guide" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"variables\":{
    \"hiring_manager\":\"6816f79cc0a8016401c5a33be04be441\",
    \"hiring_group\":\"221f3db5c6112284009f4becd3039cc9\",
    \"remote\":\"No\",
    \"standard_package\":\"No\",
    \"laptop_type\":\"developer\"
  }
}" \
--user "username":"password"
```

```
{
  "result": [
    {
      "short_description": "Lenovo - Carbon x1",
      "icon": "1195c2084f889200086eeed18110c74a.iix",
      "description": "<p class=\"p1\"><font size=\"3\" color=\"#808080\"><span class=\"s1\">x1 Carbon</span></font></p>\n<p class=\"p1\"><font size=\"2\" color=\"#808080\" face=\"arial,helvetica,sans-serif\"><span class=\"s1\">The x1 Carbon is Lenovo&#39;s lightest ThinkPad yet. It provides a QHD display that fights glare and weighs less than three pounds. Ideal for most computing tasks, and highly mobile. </span></font></p>\n<p class=\"p2\"><font size=\"2\" color=\"#808080\" face=\"arial,helvetica,sans-serif\"><span class=\"s1\">Technical Specs:</span></font></p>\n<ul class=\"ul1\"><li class=\"li3\"><font size=\"2\" color=\"#808080\"><span class=\"s1\">Intel core i5 processor</span></font></li><li class=\"li3\"><font size=\"2\" color=\"#808080\"><span class=\"s1\">512GB solid state drive (SSD) </span></font></li><li class=\"li3\"><font size=\"2\" color=\"#808080\"><span class=\"s1\">Backlit keyboard</span></font></li></ul>",
      "show_price": true,
      "recurring_price": "$100.00",
      "type": "catalog_item",
      "local_currency": "USD",
      "sys_id": "04b7e94b4f7b4200086eeed18110c7fd",
      "recurring_price_currency": "USD",
      "localized_price": "$1,100.00",
      "price": "$1,100.00",
      "catalogs": [
       {
         "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
         "title": "Service Catalog"
       }
      ],
      "recurring_frequency": "Annually",
      "name": "Standard Laptop",
      "localized_recurring_price": "$100.00",
      "category": {
        "sys_id": "d258b953c611227a0146101fb1be7c31",
        "title": "Hardware"
      },
      "price_currency": "USD",
      "show_quantity": false,
      "quantity": "1",
      "order": "100",
      "variables": [
        {
          "label": "Optional Software",
          "type": 0,
          "mandatory": false,
          "displayvalue": "",
          "friendly_type": "container_start",
          "render_label": true,
          "read_only": false,
          "children": [
            {
              "label": "Adobe Acrobat",
              "type": 7,
              "mandatory": false,
              "displayvalue": "false",
              "friendly_type": "check_box",
              "display_type": "CheckBox",
              "render_label": true,
              "read_only": false,
              "pricing_implications": false,
              "name": "acrobat",
              "attributes": "edge_encryption_enabled=true",
              "id": "90b72d4b4f7b4200086eeed18110c701",
              "value": false,
              "help_text": "",
              "max_length": 0
            },
            {
              "label": "Adobe Photoshop",
              "type": 7,
              "mandatory": false,
              "displayvalue": "false",
              "friendly_type": "check_box",
              "display_type": "CheckBox",
              "render_label": true,
              "read_only": false,
              "pricing_implications": false,
              "name": "photoshop",
              "attributes": "edge_encryption_enabled=true",
              "id": "a8b72d4b4f7b4200086eeed18110c701",
              "value": false,
              "help_text": "",
              "max_length": 0
            }
          ],
          "name": "optional_label",
          "attributes": "edge_encryption_enabled=true",
          "id": "10b72d4b4f7b4200086eeed18110c700",
          "value": "",
          "help_text": "",
          "max_length": 0
        },
        {
          "label": "Additional software requirements",
          "type": 2,
          "mandatory": false,
          "displayvalue": "",
          "friendly_type": "multi_line_text",
          "display_type": "Multi Line Text",
          "render_label": true,
          "read_only": false,
          "name": "Additional_software_requirements",
          "attributes": "edge_encryption_enabled=true",
          "id": "a8b72d4b4f7b4200086eeed18110c702",
          "value": "",
          "help_text": "",
          "max_length": 0
        }
      ],
      "ui_policy": [],
      "client_script": {
        "onChange": [],
        "onSubmit": [],
        "onLoad": []
      },
      "data_lookup": []
    },
    {
      "sys_id": "e1be6dcb4f7b4200086eeed18110c74c",
      "short_description": "LG IPS 27\" Monitor",
      "catalogs": [
        {
          "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
          "title": "Service Catalog"
        }
      ],
      "name": "External Monitor",
      "icon": "08569a4c4f889200086eeed18110c77b.iix",
      "description": "<p><font size=\"2\"><span style=\"color: #485563;\"><br /> <font size=\"3\" color=\"#808080\">The striking design of the LG Cinema Screen incorporates an ultra-narrow bezel, so virtually all you see is picture. The viewing experience is more immersive for your favorite movies and games. Make the most of your time, with an LG Full HD LED monitor. </font></span></font></p>\n<p><font size=\"2\" color=\"#808080\">Item Specs:</font></p>\n<ul><li style=\"color: #485563;\"><font size=\"2\" color=\"#808080\">Screen Size: 27&#34;</font></li><li style=\"color: #485563;\"><font size=\"2\" color=\"#808080\">Resolution: 1920 x 1080</font></li><li style=\"color: #485563;\"><font size=\"2\" color=\"#808080\">Aspect Ratio: 16:9</font></li><li style=\"color: #485563;\"><font size=\"2\" color=\"#808080\">Brightness: 250 cd/m2</font></li><li style=\"color: #485563;\"><font size=\"2\" color=\"#808080\">Supports Split Screen</font></li></ul>",
      "show_price": false,
      "type": "catalog_item",
      "category": {
        "sys_id": "2c0b59874f7b4200086eeed18110c71f",
        "title": "Peripherals"
      },
      "show_quantity": false,
      "quantity": "1",
      "order": "200",
      "variables": [],
      "ui_policy": [],
      "client_script": {
        "onChange": [],
        "onSubmit": [],
        "onLoad": []
      },
      "data_lookup": []
    },
    {
      "sys_id": "186d917a6fab7980575967ddbb3ee4f2",
      "short_description": "New Email Creation",
      "catalogs": [
        {
          "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
          "title": "Service Catalog"
        }
      ],
      "name": "New Email Account",
      "icon": "b630e97e6fab7980575967ddbb3ee4d2.iix",
      "description": "<p style=\"font-size: 13px;\"><font size=\"4\"><span style=\"color: #485563;\">Service Overview:</span></font></p>\n\t<p style=\"font-size: 13px;\"><font size=\"3\">Creation of a new email account within our Microsoft Exchange environment.  Creation of your email address will also create your Active Directory account. </font></p>\n\t<p> </p>",
      "show_price": false,
      "type": "catalog_item",
      "category": {
        "sys_id": "109f0438c6112276003ae8ac13e7009d",
        "title": "Services"
      },
      "show_quantity": false,
      "quantity": "1",
      "order": "300",
      "variables": [
        {
          "label": "Preferred Email address",
          "type": 6,
          "mandatory": true,
          "displayvalue": "",
          "friendly_type": "single_line_text",
          "display_type": "Single Line Text",
          "render_label": true,
          "read_only": false,
          "name": "new_email",
          "attributes": "edge_encryption_enabled=true",
          "id": "65865e474fbb4200086eeed18110c7dd",
          "value": "",
          "help_text": "",
          "max_length": 0
        }
      ],
      "ui_policy": [],
      "client_script": {
        "onChange": [],
        "onSubmit": [],
        "onLoad": []
      },
      "data_lookup": []
    },
    {
      "sys_id": "8b3ae7fedc1be1004ece5c08239e522b",
      "short_description": "Remote access to Internal Corporate Systems\n\t\t",
      "catalogs": [
        {
          "sys_id": "e0d08b13c3330100c8b837659bba8fb4",
          "title": "Service Catalog"
        }
      ],
      "name": "Corp VPN",
      "icon": "11dc8df74f778200086eeed18110c78e.iix",
      "description": "<p><font size=\"3\"><span style=\"color: #485563;\">Corp VPN Account</span></font></p>\n<ul><li style=\"color: #485563;\"><font size=\"2\">Corp VPN provides VPN (Virtual Private Network) access to all Internal Corporate Systems and to IP Restricted Customer Instances</font></li><li style=\"color: #485563;\"><font size=\"2\">By utilizing Corp VPN, users will be provided a similar experience to being within one of the Corporate office locations, while offsite</font></li></ul>\n<p><font size=\"2\"><span style=\"color: #485563;\"> </span></font></p>\n<p><font size=\"2\"><span style=\"color: #485563;\">Please reference the <span style=\"color: #485563;\">CORP VPN </span><span style=\"color: #485563;\">Installation</span><span style=\"color: #485563;\"> and Support Documentation</span> for instructions on installation, usage and FAQ’s. For all other questions, please contact <span style=\"color: #485563;\">IT Support.</span></span></font></p>\n<p> </p>\n<p><span style=\"font-size: 10pt; font-family: tahoma, arial, helvetica, sans-serif;\"><br /><br /></span></p>",
      "show_price": false,
      "type": "catalog_item",
      "category": {
        "sys_id": "d2f7cae4c611227a018ddc481b34e099",
        "title": "Security and Access"
      },
      "show_quantity": false,
      "quantity": "1",
      "order": "600",
      "variables": [],
      "ui_policy": [],
      "client_script": {
        "onChange": [],
        "onSubmit": [],
        "onLoad": []
      },
      "data_lookup": []
    },
    {
      "sys_id": "962967674ff38200086eeed18110c7e7",
      "short_description": "Desk Set Up for New Hires or Employee Moves\n\t\t",
      "catalogs": [
        {
          "sys_id": "",
          "title": "Service Catalog"
        }
      ],
      "name": "Desk Set Up",
      "icon": "aa6b08ff4ff38200086eeed18110c7ed.iix",
      "description": "<p><font size=\"3\" face=\"arial, helvetica, sans-serif\">The facilities organization will set up your new desk with the following configuration:</font></p>\n<ul><li><font size=\"3\" face=\"arial, helvetica, sans-serif\">Docking Station</font></li><li><font size=\"3\" face=\"arial, helvetica, sans-serif\">Power Station</font></li><li><font size=\"3\" face=\"arial, helvetica, sans-serif\">Phone</font></li><li><font size=\"3\" face=\"arial, helvetica, sans-serif\">Office Chair</font></li></ul>",
      "show_price": false,
      "type": "catalog_item",
      "category": {
        "sys_id": "",
        "title": null
      },
      "show_quantity": false,
      "quantity": "1",
      "order": "900",
      "variables": [
        {
          "label": "Please describe any ergonomic requirements\n\t\t",
          "type": 2,
          "mandatory": false,
          "displayvalue": "",
          "friendly_type": "multi_line_text",
          "display_type": "Multi Line Text",
          "render_label": true,
          "read_only": false,
          "name": "ergonomic_office",
          "attributes": "edge_encryption_enabled=true",
          "id": "b0b9ab674ff38200086eeed18110c755",
          "value": "",
          "help_text": "",
          "max_length": 0
        }
      ],
      "ui_policy": [],
      "client_script": {
        "onChange": [],
        "onSubmit": [],
        "onLoad": []
      },
      "data_lookup": []
    }
  ]
}

```

