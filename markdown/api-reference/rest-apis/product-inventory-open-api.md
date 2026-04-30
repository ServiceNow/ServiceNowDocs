---
title: Product Inventory Open API
description: The Product Inventory Open API provides endpoints to create and retrieve product inventories.Retrieves a list of all product inventories.Retrieves a specified product inventory record.Retrieves a list of all product inventories.Retrieves a product inventory.Creates a product inventory record.Creates a product inventory.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 34
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Product Inventory Open API

The Product Inventory Open API provides endpoints to create and retrieve product inventories.

Use this API to manage product inventory information between external systems and the ServiceNow AI Platform.

This API is included in the Product Inventory Advanced application, which is available on the ServiceNow Store.

This API is provided within the `sn_prd_invt` namespace.

The calling user must have the sn\_prd\_invt.product\_inventory\_integrator role.

This API creates and updates data in the following tables.

-   Product Characteristics \[sn\_prd\_invt\_product\_characteristics\]
-   Product Inventory \[sn\_prd\_invt\_product\_inventory\]
-   Product Model \[cmdb\_model\]
-   Product Model Characteristic \[sn\_prd\_pm\_product\_model\_characteristic\]

The Product Inventory Open API is a ServiceNow® implementation of the TM Forum Product Inventory Management API REST specification. This implementation is based on the [TMF637 Product Inventory Management API REST Specification Release 19](https://www.tmforum.org/resources/standard/tmf637-product-inventory-management-api-rest-specification-r19-0-0/), August 2019. The Product Inventory Open API is conformance certified by TM Forum.

![TMF conformance logo](../image/tmf-conformance.png)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Product Inventory Open API - GET /sn\_prd\_invt/product

Retrieves a list of all product inventories.

### URL format

Default URL: `api/sn_prd_invt/product`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

customer

</td><td>

Filter product inventories by customer. Only product offerings with a customer sys\_id or external ID matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

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

place

</td><td>

Filter product inventories by place. Only product offerings with a place sys\_id or external id matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

status

</td><td>

Filter product inventories by status. Only product inventories with a status matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_idy_qgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

<table id="table_hl1_rcm_lsb"><thead><tr><th>

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

<table id="table_shr_nvy_3sb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

href

</td><td>

Relative link to the product inventory record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product inventory from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

place

</td><td>

Place associated with the product.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

 ```
"productCharacteristic": [
  {
    "name": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "internalId": "String",
   "internalVersion": "String",
   "name": "String",
   "version": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Initial\_version or external\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.internalId

</td><td>

Initial\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productPrice

</td><td>

Returns an empty array.Data type: Array

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
  {
    "productId": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Product specification for the product.Data type: Object

 ```
"productSpecification": {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Initial\_version or external\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

Initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Resource that realizes the product. The realizing resource is a child product inventory of this product inventory.Data type: Object

 ```
"realizingResource": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Sys\_id of the realizing resource. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource.Valid value: child

 Data type: String

</td></tr><tr><td>

realizingService

</td><td>

Service that realizes the product. The realizing service is a child product inventory of this product inventory.Data type: Object

 ```
"realizingService": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Sys\_id of the realizing service. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service.Valid value: child

 Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
   {
      "id": "String",
      "@referredType": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Possible values:

-   Customer
-   CustomerContact
-   Consumer

Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the product.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all product inventories.

```
curl --location --request GET "https://instance.service-now.com/api/sn_prd_invt/product" \
--user 'username':'password'
```

Response body.

```
[
   {
      "id": "037fd87ec3603010abc8b5183c40ddf2",
      "relatedParty": [
         {
            "id": "ffc68911c35420105252716b7d40dd55",
            "name": "Example Company",
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
      "name": "Routing and Configuration PI0000318",
      "productSpecification": {
         "id": "aec57e981bb420106ba59acf034bcb08",
         "name": "Routing and Configuration",
         "version": "",
         "internalVersion": "1",
         "internalId": "aec57e981bb420106ba59acf034bcb08"
      },
      "status": "Active",
      "productOffering": {
         "id": "69017a0f536520103b6bddeeff7b127d",
         "name": "Premium SD-WAN Offering",
         "version": "",
         "internalVersion": "1",
         "internalId": "69017a0f536520103b6bddeeff7b127d"
      },
      "product": "ce0b52c7532520103b6bddeeff7b12f5",
      "place": {
         "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
         "name": "100 South Charles Street, Baltimore,MD"
      },
      "productCharacteristic": [],
      "productRelationship": [],
      "realizingService": [],
      "realizingResource": [
         {
            "id": "9b2fa60b536520103b6bddeeff7b1233",
            "name": "Route Target"
         }
      ],
      "productPrice": [],
      "href": "/api/sn_prd_invt/product/037fd87ec3603010abc8b5183c40ddf2",
      "billingAccount": "Not Specified."
   }
]
```

## Product Inventory Open API - GET /sn\_prd\_invt/product/\{id\}

Retrieves a specified product inventory record.

### URL format

Default URL: `/api/sn_prd_invt/product/{id}`

### Supported request parameters

<table id="table_apt_nkz_gsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product inventory to retrieve. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

customer

</td><td>

Filter product inventories by customer. Only product offerings with a customer sys\_id or external id matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter is not used, all fields are returned. Data type: String

</td></tr><tr><td>

place

</td><td>

Filter product inventories by place. Only product offerings with a place sys\_id or external id matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

status

</td><td>

Filter product inventories by status. Only product inventories with a status matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
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

<table id="table_nxj_ykz_gsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. Record associated with the ID is not found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_shr_nvy_3sb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

href

</td><td>

Relative link to the product inventory record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product inventory from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

place

</td><td>

Place associated with the product.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

 ```
"productCharacteristic": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "internalId": "String",
   "internalVersion": "String",
   "name": "String",
   "version": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Initial\_version or external\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.internalId

</td><td>

Initial\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productPrice

</td><td>

Returns an empty array.Data type: Array

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
   {
      "productId": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Product specification for the product.Data type: Object

 ```
"productSpecification": {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Initial\_version or external\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

Initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Resource that realizes the product. The realizing resource is a child product inventory of this product inventory.Data type: Object

 ```
"realizingResource": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Sys\_id of the realizing resource. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource.Valid value: child

 Data type: String

</td></tr><tr><td>

realizingService

</td><td>

Service that realizes the product. The realizing service is a child product inventory of this product inventory.Data type: Object

 ```
"realizingService": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Sys\_id of the realizing service. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service.Valid value: child

 Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
  {
    "id": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the product.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a specified product inventory.

```
curl -X GET 'https://instance.service-now.com/api/sn_prd_invt/product/037fd87ec3603010abc8b5183c40ddf2' \
--user 'username':'password'
```

Output:

```
{
   "id": "037fd87ec3603010abc8b5183c40ddf2",
   "relatedParty": [
      {
         "id": "ffc68911c35420105252716b7d40dd55",
         "name": "Example Company",
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
   "name": "Routing and Configuration PI0000318",
   "productSpecification": {
      "id": "aec57e981bb420106ba59acf034bcb08",
      "name": "Routing and Configuration",
      "version": "",
      "internalVersion": "1",
      "internalId": "aec57e981bb420106ba59acf034bcb08"
   },
   "status": "Active",
   "productOffering": {
      "id": "69017a0f536520103b6bddeeff7b127d",
      "name": "Premium SD-WAN Offering",
      "version": "",
      "internalVersion": "1",
      "internalId": "69017a0f536520103b6bddeeff7b127d"
   },
   "product": "ce0b52c7532520103b6bddeeff7b12f5",
   "place": {
      "id": "25ab9c4d0a0a0bb300f7dabdc0ca7c1c",
      "name": "100 South Charles Street, Baltimore,MD"
   },
   "productCharacteristic": [],
   "productRelationship": [],
   "realizingService": [],
   "realizingResource": [
      {
         "id": "9b2fa60b536520103b6bddeeff7b1233",
         "name": "Route Target"
      }
   ],
   "productPrice": [],
   "href": "/api/sn_prd_invt/product/037fd87ec3603010abc8b5183c40ddf2",
   "billingAccount": "Not Specified."
}
```

## Product Inventory Open API - GET /sn\_prd\_invt/productinventory

Retrieves a list of all product inventories.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Inventory Open API - GET /sn\_prd\_invt/product](product-inventory-open-api.md#).

### URL format

Default URL: `api/sn_prd_invt/productinventory`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

customer

</td><td>

Filter product inventories by customer. Only product offerings with a customer sys\_id or external id matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

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

place

</td><td>

Filter product inventories by place. Only product offerings with a place sys\_id or external id matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

status

</td><td>

Filter product inventories by status. Only product inventories with a status matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_idy_qgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

<table id="table_hl1_rcm_lsb"><thead><tr><th>

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

<table id="table_shr_nvy_3sb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product inventory from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

place

</td><td>

Place associated with the product.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

 ```
"productCharacteristic": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
   {
      "productId": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Product specification for the product.Data type: Object

 ```
"productSpecification": {
      "id": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Sys\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Realizing resource.Data type: Object

 ```
"realizingResource": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Sys\_id of the realizing resource from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource.Data type: String

</td></tr><tr><td>

realizingService

</td><td>

Realizing service.Data type: Object

 ```
"realizingService": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Sys\_id of the realizing service from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
   {
      "id": "String",
      "@referredType": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\] or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Possible values:

-   customer
-   customerContact
-   consumer

Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the product.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all product inventories.

```
curl "https://instance.servicenow.com/api/sn_prd_invt/productinventory" \
--request GET \
--user 'username':'password'



```

Response body.

```
[
   {
      "id": "075072aec3a83010abc8b5183c40dd44",
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
      "name": "Firewall Administration PI0000300",
      "productSpecification": {
         "id": "31c5caff07266010a7955b7e0ad3006b",
         "name": "Firewall Administration"
      },
      "status": "Active",
      "productOffering": {
         "id": "",
         "name": ""
      },
      "place": {
         "id": "920cf6ac73d423002728660c4cf6a799",
         "name": "200 South James street,Atlanta, GA"
      },
      "productCharacteristic": [
         {
            "name": "Firewall Administration CPE Type",
            "valueType": "Choice",
            "value": "Physical"
         },
         {
            "name": "Configuration and Policy backup",
            "valueType": "Choice",
            "value": ""
         },
         {
            "name": "Firewall Administration CPE ID",
            "valueType": "Single Line Text",
            "value": "CPE123456789"
         },
         {
            "name": "Remote CLI troubleshoot support",
            "valueType": "Choice",
            "value": ""
         },
         {
            "name": "Firewall Administration CPE Model",
            "valueType": "Choice",
            "value": "9300 series"
         }
      ],
      "productRelationship": [],
      "realizingService": [],
      "realizingResource": [
         {
            "id": "3546463307666010a7955b7e0ad3005d",
            "name": "Cisco Firewall Management system"
         }
      ]
   },
   {
      "id": "0303a8ea74418510f877ca57242ff96d",
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
      "name": "SD-WAN Edge Device PI0001114",
      "productSpecification": {
         "id": "39b627aa53702010cd6dddeeff7b1202",
         "name": "SD-WAN Edge Device"
      },
      "status": "Installation Pending",
      "productOffering": {
         "id": "69017a0f536520103b6bddeeff7b127d",
         "name": "Premium SD-WAN Offering"
      },
      "place": "",
      "productCharacteristic": [],
      "productRelationship": [],
      "realizingService": [
         {
            "id": "bf65eadc1b7420106ba59acf034bcb57",
            "name": "SD-WAN Routing"
         },
         {
            "id": "16d79ec3532520103b6bddeeff7b12a6",
            "name": "SD WAN Optimization Service"
         },
         {
            "id": "16d79ec3532520103b6bddeeff7b12a6",
            "name": "SD WAN Optimization Service"
         },
         {
            "id": "bf65eadc1b7420106ba59acf034bcb57",
            "name": "SD-WAN Routing"
         },
         {
            "id": "bf65eadc1b7420106ba59acf034bcb57",
            "name": "SD-WAN Routing"
         },
         {
            "id": "bf65eadc1b7420106ba59acf034bcb57",
            "name": "SD-WAN Routing"
         }
      ],
      "realizingResource": [
         {
            "id": "493fa60b536520103b6bddeeff7b12b6",
            "name": "Customer Premise SD-WAN Router"
         }
      ]
   }
]
```

## Product Inventory Open API - GET /sn\_prd\_invt/productinventory/\{inventoryId\}

Retrieves a product inventory.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Inventory Open API - GET /sn\_prd\_invt/product/\{id\}](product-inventory-open-api.md#).

### URL format

Default URL: `/api/sn_prd_invt/productinventory/{inventoryId}`

### Supported request parameters

<table id="table_apt_nkz_gsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inventoryId

</td><td>

Sys\_id of the product inventory to retrieve. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

customer

</td><td>

Filter product inventories by customer. Only product offerings with a customer sys\_id or external id matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter is not used, all fields are returned. Data type: String

</td></tr><tr><td>

place

</td><td>

Filter product inventories by place. Only product offerings with a place sys\_id or external id matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

status

</td><td>

Filter product inventories by status. Only product inventories with a status matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
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

<table id="table_nxj_ykz_gsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. Record associated with the ID is not found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_shr_nvy_3sb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product inventory from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

place

</td><td>

Place associated with the product.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

 ```
"productCharacteristic": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
   {
      "productId": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Product specification for the product.Data type: Object

 ```
"productSpecification": {
      "id": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Sys\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Realizing resource.Data type: Object

 ```
"realizingResource": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Sys\_id of the realizing resource from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource.Data type: String

</td></tr><tr><td>

realizingService

</td><td>

Realizing service.Data type: Object

 ```
"realizingService": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Sys\_id of the realizing service from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
   {
      "id": "String",
      "@referredType": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Possible values:

-   Customer
-   CustomerContact
-   Consumer

Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the product.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a product inventory for an SD-WAN service package.

```
curl --location --request GET 'https:// instance.servicenow.com/api/sn_prd_invt/productinventory/074450fc74918d10f877ca57242ff9e3' \
--user 'username':'password'



```

Output:

```
{
   "id": "074450fc74918d10f877ca57242ff9e3",
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
   "name": "SD-WAN Service Package PI0001576",
   "productSpecification": {
      "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
      "name": "SD-WAN Service Package"
   },
   "status": "Installation Pending",
   "productOffering": {
      "id": "69017a0f536520103b6bddeeff7b127d",
      "name": "Premium SD-WAN Offering"
   },
   "place": "",
   "productCharacteristic": [],
   "productRelationship": [
      {
         "id": "a74490fc74918d10f877ca57242ff942",
         "name": "SD-WAN Edge Device PI0001582",
         "relationshipType": "Bundles"
      },
      {
         "id": "b85414fc74918d10f877ca57242ff90e",
         "name": "SD-WAN Controller PI0001602",
         "relationshipType": "Bundles"
      },
      {
         "id": "d74490fc74918d10f877ca57242ff907",
         "name": "SD-WAN Security PI0001577",
         "relationshipType": "Bundles"
      }
   ],
   "realizingService": [],
   "realizingResource": []
}
```

## Product Inventory Open API - POST /sn\_prd\_invt/product

Creates a product inventory record.

### URL format

Default URL: `/api/sn_prd_invt/product`

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

name

</td><td>

Required. Name of the product inventory.Data type: String

</td></tr><tr><td>

pid

</td><td>

Unique identifier for the product inventory from the external system.Data type: String

 Default: Blank string

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

 ```
"productCharacteristic": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

 Default: Blank string

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

 Default: Blank string

</td></tr><tr><td>

productOffering

</td><td>

Required. Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "internalVersion": "String",
   "name": "String",
   "version": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Required. Initial\_version or external\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

 Default: Blank string

</td></tr><tr><td>

productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
   {
      "productId": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Required if using the **productRelationship** parameter. Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship. The only valid value is `child`.Data type: String

 Default: Blank string

</td></tr><tr><td>

productSpecification

</td><td>

Required. Product specification for the product.Data type: Object

 ```
"productSpecification": {
      "id": "String",
      "internalVersion": "String",
      "version": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Required. Initial\_version or external\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Resource that realizes the product. The realizing resource is a child product inventory of this product inventory.Data type: Object

 ```
"realizingResource": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Required if using the **realizingResource** parameter. Sys\_id of the realizing resource. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource.Valid value: child

 Data type: String

</td></tr><tr><td>

realizingService

</td><td>

Service that realizes the product. The realizing service is a child product inventory of this product inventory.Data type: Object

 ```
"realizingService": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Required if using the **realizingService** parameter. Sys\_id of the realizing service. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service.Valid value: child

 Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
  {
    "id": "String",
    "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Required if using the **relatedParty** parameter. Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Possible values:

-   customer
-   customer\_contact
-   consumer

 Data type: String

 Default: Blank string

</td></tr><tr><td>

state

</td><td>

Current state of the product.Possible values:

-   active
-   change\_pending
-   inactivation\_pending
-   inactive
-   installation\_pending

 Data type: String

 Default: installation\_pending

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

<table id="table_fbw_k3z_gsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Request successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons: -   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

href

</td><td>

Relative link to the product inventory record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product inventory from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

pid

</td><td>

Unique identifier for the product inventory from the external system.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

 ```
"productCharacteristic": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "internalId": "String",
   "internalVersion": "String",
   "name": "String",
   "version": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Initial\_version or external\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.internalId

</td><td>

Initial\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.internalVersion

</td><td>

Version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.version

</td><td>

External\_version of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productPrice

</td><td>

Returns an empty array.Data type: Array

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
  {
    "productId": "String",
    "relationshipType": "String"
  }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Product specification for the product.Data type: Object

 ```
"productSpecification": {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Initial\_version or external\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

Initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

External\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Resource that realizes the product. The realizing resource is a child product inventory of this product inventory.Data type: Object

 ```
"realizingResource": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Sys\_id of the realizing resource. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource.Valid value: child

 Data type: String

</td></tr><tr><td>

realizingService

</td><td>

Service that realizes the product. The realizing service is a child product inventory of this product inventory.Data type: Object

 ```
"realizingService": {
  "id": "String",
  "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Sys\_id of the realizing service. Located in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service.Valid value: child

 Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
  {
     "id": "String",
     "@referredType": "String"
  }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Possible values:

-   Customer
-   CustomerContact
-   Consumer

Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the product.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a product inventory for a voice over IP solution for a user.

```
curl -X POST "https://instance.service-now.com/api/sn_prd_invt/product" \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--user "username":"password" \
--data "[
   {
      "pid": "PO-456",
      "description": "inventory description",
      "isBundle": false,
      "name": "Voice Over IP Basic instance for Jean",
      "productOffering": {
         "@referredType": "ProductOffering",
         "name": "Premium SD-WAN Offering",
         "id": "69017a0f536520103b6bddeeff7b127d"
      },
      "productCharacteristic": [],
      "productRelationship": [
         {
            "productId": "fa6d13f45b5620102dff5e92dc81c77f",
            "relationshipType": "child"
         }
      ],
      "realizingService": {
         "id": "fe6d13f45b5620102dff5e92dc81c786",
         "relationshipType": "child"
      },
      "realizingResource": {
         "id": "326d13f45b5620102dff5e92dc81c78c",
         "relationshipType": "child"
      },
      "relatedParty": [
         {
            "@referredType": "CustomerContact",
            "@type": "RelatedParty",
            "name": "Sally Thomas",
            "id": "eaf68911c35420105252716b7d40ddde"
         },
         {
            "@referredType": "Customer",
            "@type": "RelatedParty",
            "name": "Funco Intl",
            "id": "ffc68911c35420105252716b7d40dd55"
         }
      ],
      "productSpecification": {
         "@referredType": "ProductSpecification",
         "@type": null,
         "name": null,
         "id": "3ee1fdb1c3331010d216b5183c40dd81",
         "internalVersion": "1"
      },
      "bundle": false
   }
]"
```

Response body.

```
{
   "pid": "PO-456",
   "description": "inventory description",
   "isBundle": false,
   "name": "Voice Over IP Basic instance for Jean",
   "productOffering": {
      "@referredType": "ProductOffering",
      "name": "Premium SD-WAN Offering",
      "id": "69017a0f536520103b6bddeeff7b127d",
      "internalVersion": "1",
      "version": null,
      "status": "published",
      "internalId": "69017a0f536520103b6bddeeff7b127d"
   },
   "productCharacteristic": [],
   "productRelationship": [
      {
         "productId": "fa6d13f45b5620102dff5e92dc81c77f",
         "relationshipType": "child"
      }
   ],
   "realizingService": {
      "id": "fe6d13f45b5620102dff5e92dc81c786",
      "relationshipType": "child"
   },
   "realizingResource": {
      "id": "326d13f45b5620102dff5e92dc81c78c",
      "relationshipType": "child"
   },
   "relatedParty": [
      {
         "@referredType": "CustomerContact",
         "@type": "RelatedParty",
         "name": "Sally Thomas",
         "id": "eaf68911c35420105252716b7d40ddde"
      },
      {
         "@referredType": "Customer",
         "@type": "RelatedParty",
         "name": "Example Company",
         "id": "ffc68911c35420105252716b7d40dd55"
      }
   ],
   "productSpecification": {
      "@referredType": "ProductSpecification",
      "@type": null,
      "name": null,
      "id": "3ee1fdb1c3331010d216b5183c40dd81",
      "internalVersion": "1",
      "version": null,
      "status": "published",
      "internalId": "3ee1fdb1c3331010d216b5183c40dd81"
   },
   "bundle": false,
   "productPrice": [],
   "id": "25b07475471789108761b955d36d439d",
   "href": "/api/sn_prd_invt/product/25b07475471789108761b955d36d439d"
}
```

## Product Inventory Open API - POST /sn\_prd\_invt/productinventory

Creates a product inventory.

**Important:** Starting with the Tokyo release, this endpoint is deprecated. The new version of this endpoint is [Product Inventory Open API - POST /sn\_prd\_invt/product](product-inventory-open-api.md#).

### URL format

Default URL: `/api/sn_prd_invt/productinventory`

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

name

</td><td>

Required. Name of the product inventory.Data type: String

</td></tr><tr><td>

pid

</td><td>

Unique identifier for the product inventory from the external system.Data type: String

Default: Blank string

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

```
"productCharacteristic": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

 Default: Blank string

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

 Default: Blank string

</td></tr><tr><td>

productOffering

</td><td>

Required. Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Required. Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

Default: Blank string

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
   {
      "productId": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Required if using the **productRelationship** parameter. Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship. The only valid value is `child`.Data type: String

 Default: Blank string

</td></tr><tr><td>

productSpecification

</td><td>

Required. Product specification for the product.Data type: Object

 ```
"productSpecification": {
      "id": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Required. Sys\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Realizing resource.Data type: Object

 ```
"realizingResource": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Required if using the **realizingResource** parameter. Sys\_id of the realizing resource from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource. The only valid value is `child`.Data type: String

 Default: Blank string

</td></tr><tr><td>

realizingService

</td><td>

Realizing service.Data type: Object

 ```
"realizingService": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Required if using the **realizingService** parameter. Sys\_id of the realizing service from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service. The only valid value is `child`.Data type: String

 Default: Blank string

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
   {
      "id": "String",
      "@referredType": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Required if using the **relatedParty** parameter. Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_Consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Possible values:

-   customer
-   customer\_contact
-   consumer

 Data type: String

 Default: Blank string

</td></tr><tr><td>

state

</td><td>

Current state of the product.Possible values:

-   active
-   change\_pending
-   inactivation\_pending
-   inactive
-   installation\_pending

 Data type: String

 Default: installation\_pending

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

<table id="table_fbw_k3z_gsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Request successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons: -   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product inventory from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

pid

</td><td>

Unique identifier for the product inventory from the external system.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array

 ```
"productCharacteristic": [
   {
      "name": "String",
      "value": "String"
   }
]
```

</td></tr><tr><td>

productCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that the product inventory is associated with.Data type: Object

 ```
"productOffering": {
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productRelationship

</td><td>

List of related products.Data type: Array

 ```
"productRelationship": [
   {
      "productId": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

productRelationship.productId

</td><td>

Sys\_id of the related product from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

productRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Product specification for the product.Data type: Object

 ```
"productSpecification": {
      "id": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Sys\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

realizingResource

</td><td>

Realizing resource.Data type: Object

 ```
"realizingResource": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingResource.id

</td><td>

Sys\_id of the realizing resource from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingResource.type

</td><td>

Type of the realizing resource.Data type: String

</td></tr><tr><td>

realizingService

</td><td>

Realizing service.Data type: Object

 ```
"realizingService": {
      "id": "String",
      "type": "String"
}
```

</td></tr><tr><td>

realizingService.id

</td><td>

Sys\_id of the realizing service from the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.Data type: String

</td></tr><tr><td>

realizingService.type

</td><td>

Type of the realizing service.Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of parties associated with the ticket.Data type: Array

 ```
"relatedParty": [
   {
      "id": "String",
      "@referredType": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the account or customer contact associated with the ticket. Located in the Account \[customer\_account\], Contact \[customer\_contact\], or Consumer \[csm\_consumer\] table.Data type: String

</td></tr><tr><td>

relatedParty.@referredType

</td><td>

Type of customer.Possible values:

-   Customer
-   CustomerContact
-   Consumer

Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the product.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a product inventory for a voice over IP solution for a user.

```
curl --location --request POST “https://instance.servicenow.com/api/sn_prd_invt/productinventory” \
--header “Content-Type: application/json” \
--data-raw '[
    {
        "pid": "demoInventory",
        "description": "inventory description",
        "isBundle": false,
        "name": "Voice Over IP Basic instance for Jean",
        "productOffering": {
            "id": "69017a0f536520103b6bddeeff7b127d",
            "name": "Premium SD-WAN Offering",
            "@referredType": "ProductOffering"
        },
        "productCharacteristic": [
            {
                "name": "CPE Type",
                "valueType": "choice",
                "value": "Virtual"
            },
            {
                "name":"Routing",
                "valueType": "choice",
                "value": "Premium"
            }
        ],
        "productRelationship": [
            {
                "productId": "7e6d13f45b5620102dff5e92dc81c787",
                "relationshipType": "child"
            }
        ],
        "relatedParty": [
            {
                "id": "eaf68911c35420105252716b7d40ddde",
                "name": "Sally Thomas",
                "role": "User",
                "@type": "RelatedParty",
                "@referredType": "CustomerContact"
            },
            {
                "id": "ffc68911c35420105252716b7d40dd55",
                "name": "Funco Intl",
                "@type": "RelatedParty",
                "@referredType": "Customer"
            }
        ],
        "productSpecification": {
            "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
            "@referredType": "ProductSpecification",
            "version": "1"
        }
    }
]'
--user 'username':'password'

```

Response body.

```
{
   "pid": "demoInventory",
   "description": "inventory description",
   "isBundle": false,
   "name": "Voice Over IP Basic instance for Jean",
   "productOffering": {
      "id": "69017a0f536520103b6bddeeff7b127d",
      "name": "Premium SD-WAN Offering",
      "@referredType": "ProductOffering"
   },
   "productCharacteristic": [
      {
         "name": "CPE Type",
         "valueType": "choice",
         "value": "Virtual"
      },
      {
         "name": "Routing",
         "valueType": "choice",
         "value": "Premium"
      }
   ],
   "productRelationship": [
      {
         "productId": "7e6d13f45b5620102dff5e92dc81c787",
         "relationshipType": "child"
      }
   ],
   "relatedParty": [
      {
         "id": "eaf68911c35420105252716b7d40ddde",
         "name": "Sally Thomas",
         "role": "User",
         "@type": "RelatedParty",
         "@referredType": "CustomerContact"
      },
      {
         "id": "ffc68911c35420105252716b7d40dd55",
         "name": "Funco Intl",
         "@type": "RelatedParty",
         "@referredType": "Customer"
      }
   ],
   "productSpecification": {
      "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
      "@referredType": "ProductSpecification",
      "version": "1"
   },
   "id": "3ac715c6745d8150f877ca57242ff97a"
}
```

