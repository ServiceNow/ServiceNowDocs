---
title: Product Catalog Open API
description: The Product Catalog Open API provides endpoints to create and retrieve product catalogs, product offerings, and product specifications.Deletes the specified product offering.Deletes or archives the specified product specification.Retrieves a list of all product offering catalogs.Retrieves a product offering catalog.Retrieves all product offerings.Retrieves a product offering.Retrieves all product specifications.Retrieves a specified product specification.Updates the specified product offering.Updates the specified product specification.Creates a product offering catalog.Creates a product offering.Creates a product specification.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 76
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Product Catalog Open API

The Product Catalog Open API provides endpoints to create and retrieve product catalogs, product offerings, and product specifications.

Use this API to manage product catalog information between external systems and the ServiceNow AI Platform. The Product Catalog Open API is a ServiceNow® implementation of the TM Forum Product Catalog Management API REST specification. This implementation is based on the [TMF620 Product Catalog Management API REST Specification Version 4](https://www.tmforum.org/resources/standard/tmf620-product-catalog-management-api-user-guide-v4-1-0/), April 2021.

This API is included in the Product Catalog Advanced application, which is available on the ServiceNow Store.

This API is provided within the `sn_tmf_api` namespace.

The calling user must have the sn\_prd\_pm\_adv.catalog\_integrator role.

This API creates and updates data in the following tables.

-   Characteristic \[sn\_prd\_pm\_characteristic\]
-   Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]
-   Product Offering \[sn\_prd\_pm\_product\_offering\]
-   Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]
-   Product Offering Characteristic \[sn\_prd\_pm\_product\_offering\_characteristic\]
-   Product Specification \[sn\_prd\_pm\_product\_specification\]
-   Specification Relationship \[sn\_prd\_pm\_specification\_relationship\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Product Catalog Open API - DELETE /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}

Deletes the specified product offering.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOffering/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product offering to delete. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

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
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|message|A failure or success message about the deletion or archival of the product specification.|

### cURL request

The following example deletes the product offering with an ID of d6f8d9995b020210235d85cced81c7eb.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productOffering/d6f8d9995b020210235d85cced81c7eb" \ 
--request DELETE\ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

The response body returns a successful deletion message:

```
"The product offering (d6f8d9995b020210235d85cced81c7eb) is successfully deleted"
```

## Product Catalog Open API - DELETE /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}

Deletes or archives the specified product specification.

When calling this DELETE method, a product specification may either be deleted or archived depending on the state it is in:

-   A product specification in the draft state is successfully deleted. The response returns a success message.
-   A product specification in the archived state can't be deleted. The response returns a message that the specification is already archived.
-   A product specification not in the draft state and associated with other product specifications or offerings is archived but not deleted. The response returns a message that the specification is moved from an active state to an archived state.
-   A product specification associated with an active product specification or offering cannot be deleted. The response returns an error message.

### URL format

Default URL: `/sn_tmf_api/catalogmanagement/productSpecification/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product specification to delete. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_u3k_cgq_mbc" class="rest_api_request_headers"><thead><tr><th>

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
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|message|A failure or success message about the deletion or archival of the product specification.|

### cURL request

The following example deletes the product specification with an ID of 8ef57fa05b308210235d85cced81c7d8.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productSpecification/8ef57fa05b308210235d85cced81c7d8" \ 
--request DELETE\ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

The response body returns a success or failure message:

```
"The product specification (8ef57fa05b308210235d85cced81c7d8) is successfully deleted"
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/catalog

Retrieves a list of all product offering catalogs.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/catalog`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_c3q_ylz_gsb" class="rest_api_query_parameters"><thead><tr><th>

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

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_nww_xgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

<table id="table_v1h_tcm_lsb"><thead><tr><th>

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

<table id="table_m2z_clz_gsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the product offering catalog.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product offering catalog from the Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product offering catalog.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all product offering catalogs.

```
curl --location --request GET "https://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/catalog" \
--user 'username':'password'

```

Response body.

```
[
    {
        "id": "SD-WAN1344314wrfw14345",
        "name": "New Catalog",
        "description": "New Catalog"
    },
    {
        "id": "9919291ac34c20105252716b7d40dd0f",
        "name": "Enterprise Mobile Plan",
        "description": " Product Catalog for Enterprise Mobile Plan"
    }
]
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/catalog/\{id\}

Retrieves a product offering catalog.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/catalog/{id}`

### Supported request parameters

<table id="table_apt_nkz_gsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product offering catalog to retrieve. Located in the Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] table.Data type: String

</td></tr></tbody>
</table><table id="table_l5k_tkz_gsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter is not used, all fields are returned. Data type: String

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
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_nxj_ykz_gsb"><thead><tr><th>

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

Bad Request. Could be any of the following reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_m2z_clz_gsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the product offering catalog.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product offering catalog from the Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product offering catalog.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a product offering catalog for an enterprise mobile plan.

```
curl --location --request GET "https://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/catalog/9919291ac34c20105252716b7d40dd0f" \
--user 'username':'password'


```

Response body.

```
{
   "id": "9919291ac34c20105252716b7d40dd0f",
   "name": "Enterprise Mobile Plan",
   "description": " Product Catalog for Enterprise Mobile Plan"
}
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productOffering

Retrieves all product offerings.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOffering`

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

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   category
-   channel
-   description
-   externalId
-   id
-   internalId
-   internalVersion
-   lastUpdate
-   name
-   productCharacteristic
-   productOfferingPrice
-   productOfferingTerm
-   productSpecification
-   prodSpecCharValueUse
-   validFor
-   version

 Default: All fields are returned.

 Data type: String

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

specification

</td><td>

Filter product offerings by product specification sys\_id. Only product offerings with the specified product specification sys\_id are returned in the response. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

state

</td><td>

Filter product offerings by state. Only product offerings in the specified state are returned in the response.Accepted values:

-   archived
-   draft
-   published
-   retired

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_ug4_sgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

<table id="table_qhs_scm_lsb"><thead><tr><th>

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

<table id="table_rqr_2s1_jsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

List of categories that the product belongs to.Data type: Array of Objects

 ```
"category:" [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

category.id

</td><td>

ID of the category.Data type: String

</td></tr><tr><td>

category.name

</td><td>

Name of the category.Data type: String

</td></tr><tr><td>

channel

</td><td>

Channels to use for selling the product offering.Data type: Array of Objects

```
"channel:" [
  {
    "description": "String",
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.description

</td><td>

Description of the channel.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Sys\_id of the channel from the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

href

</td><td>

A relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. initial\_version or external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

initial\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product offering. Accepted values:

-   Active
-   Inactive
-   Draft

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array of Objects

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

productOfferingPrice

</td><td>

Price information for the product offering.Data type: Array of Objects

```
"productOfferingPrice": [
  {
    "price": {Object},
    "priceType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingPrice.price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.priceType

</td><td>

Type of product offering price, one-time or recurring payment.Valid values:

-   nonRecurring \(one-time\)
-   recurring

 Data type: String

</td></tr><tr><td>

productOfferingTerm

</td><td>

Valid contract term length for the product offering.Data type: String

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

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

external\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td>

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
  {
    "productSpecCharacteristicValue": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"productSpecCharacteristicValue": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.valueType

</td><td>

Value type of the characteristic, such as choice or email.

</td></tr><tr><td>

validFor

</td><td>

Date range the product offering is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the product offering.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the product offering.Data type: String

</td></tr><tr><td>

version

</td><td>

external\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all product offerings.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productOffering" \
--user 'username':'password'
```

Response body:

```
[
   {
      "id": "24413",
      "name": "Premium SD-WAN Offering New",
      "version": "",
      "internalVersion": "1",
      "internalId": "0199f8e65b430110235d85cced81c7d2",
      "description": "Premium SD-WAN Offering",
      "lastUpdate": "2022-01-27 05:41:16",
      "validFor": {
         "startDateTime": "2021-08-05",
         "endDateTime": "2026-09-04"
      },
      "productOfferingTerm": "not_applicable",
      "productOfferingPrice": [
         {
            "priceType": "recurring",
            "price": {
               "taxIncludedAmount": {
                  "unit": "JPY",
                  "value": 984.0913
               }
            }
         },
         {
            "priceType": "nonRecurring",
            "price": {
               "taxIncludedAmount": {
                  "unit": "GBP",
                  "value": 2434
               }
            }
         }
      ],
      "productSpecification": {
         "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
         "name": "SD-WAN Service Package",
         "version": "v1",
         "internalVersion": "1",
         "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
      },
      "prodSpecCharValueUse": [
         {
            "name": "Routing",
            "description": "Routing",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2021-12-15 21:08:20"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Premium",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Base",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Advance",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ],
            "productSpecification": {
               "id": "39b627aa53702010cd6dddeeff7b1202",
               "name": "SD-WAN Edge Device",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "39b627aa53702010cd6dddeeff7b1202"
            }
         },
         {
            "name": "WAN Optimization",
            "description": "WAN Optimization",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2021-12-15 21:10:28"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Base",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Advance",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Premium",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ],
            "productSpecification": {
               "id": "39b627aa53702010cd6dddeeff7b1202",
               "name": "SD-WAN Edge Device",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "39b627aa53702010cd6dddeeff7b1202"
            }
         },
         {
            "name": "CPE Model",
            "description": "CPE Model",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2021-12-15 21:11:54"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "ISR",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "ASR",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ],
            "productSpecification": {
               "id": "39b627aa53702010cd6dddeeff7b1202",
               "name": "SD-WAN Edge Device",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "39b627aa53702010cd6dddeeff7b1202"
            }
         },
         {
            "name": "Security Type",
            "description": "Security Type",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2021-12-30 12:51:13"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Premium",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Advance",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Base",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ],
            "productSpecification": {
               "id": "a6514bd3534560102f18ddeeff7b1247",
               "name": "SD-WAN Security",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "a6514bd3534560102f18ddeeff7b1247"
            }
         },
         {
            "name": "CPE Type",
            "description": "CPE Type",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2021-12-15 21:11:16"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Virtual",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Physical",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ],
            "productSpecification": {
               "id": "39b627aa53702010cd6dddeeff7b1202",
               "name": "SD-WAN Edge Device",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "39b627aa53702010cd6dddeeff7b1202"
            }
         },
         {
            "name": "Tenancy",
            "description": "Tenancy",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2021-12-15 21:04:24"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Advance (50 site)",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Base (10 site)",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Premium (>50 sites)",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ],
            "productSpecification": {
               "id": "216663aa53702010cd6dddeeff7b12b5",
               "name": "SD-WAN Controller",
               "version": "v1",
               "internalVersion": "1",
               "internalId": "216663aa53702010cd6dddeeff7b12b5"
            }
         }
      ],
      "channel": [
         {
            "id": "e561aae4c3e710105252716b7d40dd8f",
            "name": "Web"
         }
      ],
      "category": {
         "id": "c0ed043653b02010cd6dddeeff7b1277",
         "name": "SD-WAN"
      }
   }
]
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}

Retrieves a product offering.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOffering/{id}`

### Supported request parameters

<table id="table_apt_nkz_gsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Initial\_version of the product offering to retrieve. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   category
-   channel
-   description
-   externalId
-   id
-   internalId
-   internalVersion
-   lastUpdate
-   name
-   productCharacteristic
-   productOfferingPrice
-   productOfferingTerm
-   productSpecification
-   prodSpecCharValueUse
-   validFor
-   version

 Default: All fields are returned.

 Data type: String

</td></tr><tr><td>

specification

</td><td>

Filter product offerings by product specification sys\_id. Only product offerings with the specified product specification sys\_id are returned in the response. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

state

</td><td>

Filter product offerings by state. Only product offerings in the specified state are returned in the response.Accepted values:

-   archived
-   draft
-   published
-   retired

Data type: String

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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_rqr_2s1_jsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

List of categories that the product belongs to.Data type: Array

 ```
"category:" [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

category.id

</td><td>

Id of the category.Data type: String

</td></tr><tr><td>

category.name

</td><td>

Name of the category.Data type: String

</td></tr><tr><td>

channel

</td><td>

Channels to use for selling the product offering.Data type: Array

 ```
"channel:" [
  {
    "description": "String",
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.description

</td><td>

Description of the channel.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Sys\_id of the channel from the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

href

</td><td>

A relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. initial\_version or external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

initial\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Indicates the current lifecycle status of the product offering. Accepted values:-   Active
-   Inactive
-   Draft

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product offering.Data type: String

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

productOfferingPrice

</td><td>

Price information for the product offering.Data type: Array

 ```
"productOfferingPrice": [
   {
      "price": Object,
      "priceType": "String"
   }
]

```

</td></tr><tr><td>

productOfferingPrice.price

</td><td>

Price information for the product offering.Data type: Object

 ```
"price": {
   "taxIncludedAmount": Object
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

 ```
"taxIncludedAmount": {
   "unit": "String",
   "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.priceType

</td><td>

Identifies if the product offering price is a one-time or recurring payment.Valid values:

-   nonRecurring
-   recurring

 Data type: String

</td></tr><tr><td>

productOfferingTerm

</td><td>

Valid contract term length for the product offering.Data type: String

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

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

external\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td>

Product offering characteristic.Data type: Array

 ```
"prodSpecCharValueUse": [
   {
      "productSpecCharacteristicValue": Array,
      "description": "String",
      "name": "String",
      "validFor": Object,
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

Array containing the possible values of the characteristic.Data type: Array

 ```
"productSpecCharacteristicValue": [
   {
      "value": "String"
   }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

 ```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.valueType

</td><td>

The value type of the characteristic, such as choice or email.

</td></tr><tr><td>

validFor

</td><td>

Date range the product offering is valid for.Data type: Object

 ```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the product offering.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the product offering.Data type: String

</td></tr><tr><td>

version

</td><td>

external\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a product offering.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productOffering/24413" \
--user 'username':'password'
```

Response body:

```
{
   "id": "24413",
   "name": "Premium SD-WAN Offering New",
   "description": "Premium SD-WAN Offering",
   "lastUpdate": "2022-01-27 05:41:16",
   "version": "",
   "internalVersion": "2",
   "internalId": "69017a0f536520103b6bddeeff7b127d",
   "validFor": {
      "startDateTime": "2021-08-05",
      "endDateTime": "2026-09-04"
   },
   "productOfferingTerm": "not_applicable",
   "productOfferingPrice": [
      {
         "priceType": "recurring",
         "price": {
            "taxIncludedAmount": {
               "unit": "JPY",
               "value": 984.0913
            }
         }
      },
      {
         "priceType": "nonRecurring",
         "price": {
            "taxIncludedAmount": {
               "unit": "GBP",
               "value": 2434
            }
         }
      }
   ],
   "productSpecification": {
      "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
      "name": "SD-WAN Service Package",
      "version": "v1",
      "internalVersion": "1",
      "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
   },
   "prodSpecCharValueUse": [
      {
         "name": "Routing",
         "description": "Routing",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-12-15 21:08:20"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v2",
            "internalVersion": "2",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "WAN Optimization",
         "description": "WAN Optimization",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-12-15 21:10:28"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v2",
            "internalVersion": "2",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "CPE Model",
         "description": "CPE Model",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-12-15 21:11:54"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "ISR",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "ASR",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v2",
            "internalVersion": "2",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "Security Type",
         "description": "Security Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-12-30 12:51:13"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "a6514bd3534560102f18ddeeff7b1247",
            "name": "SD-WAN Security",
            "version": "abc",
            "internalVersion": "1",
            "internalId": "a6514bd3534560102f18ddeeff7b1247"
         }
      },
      {
         "name": "CPE Type",
         "description": "CPE Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-12-15 21:11:16"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Virtual",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Physical",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "",
            "internalVersion": "2",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "Tenancy",
         "description": "Tenancy",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-12-15 21:04:24"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Advance (50 site)",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Base (10 site)",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Premium (>50 sites)",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "216663aa53702010cd6dddeeff7b12b5",
            "name": "SD-WAN Controller",
            "version": "",
            "internalVersion": "1",
            "internalId": "216663aa53702010cd6dddeeff7b12b5"
         }
      }
   ],
   "channel": [
      {
         "id": "e561aae4c3e710105252716b7d40dd8f",
         "name": "Web"
      }
   ],
   "category": {
      "id": "c0ed043653b02010cd6dddeeff7b1277",
      "name": "SD-WAN"
   }
}
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productSpecification

Retrieves all product specifications.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productSpecification`

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

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   description
-   externalId
-   id
-   internalId
-   internalVersion
-   lastUpdate
-   name
-   productSpecCharacteristic
-   productSpecificationRelationship
-   resourceSpecification
-   serviceSpecification
-   validFor
-   version

 Default: All fields are returned.

 Data type: String

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

Filter product specifications by state. Only product specifications in the specified state are returned in the response.Accepted values:

-   archived
-   draft
-   published
-   retired

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_pkr_rgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

<table id="table_xss_rcm_lsb"><thead><tr><th>

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

<table id="table_zmb_ccb_jsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Required. External\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Initial\_version or external\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

Required. Initial\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether **productSpecification** represents a single product or a bundle of products.Valid values:

-   true: The product specification is a product bundle and contains multiple products.
-   false: The product specification contains a single product.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current lifecycle status of the product specification. Accepted values:

-   Active
-   Inactive
-   Draft

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"productSpecCharacteristic": [
  {
    "description": "String",
    "name": "String",
    "productSpecCharacteristicValue": [Array],
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productSpecCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue

</td><td>

List of possible values of the characteristic.Data type: Array of Objects

```
"productSpecCharacteristicValue": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

productSpecificationRelationship

</td><td>

This specification's relationships to other product specifications.Data type: Array of Objects

 ```
"productSpecificationRelationship": [
  {
    "id": "String",
    "type": "String",
    "validFor": {Object}
  }
]
```

</td></tr><tr><td>

productSpecificationRelationship.id

</td><td>

ID of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.type

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

 ```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

List of resource specifications related to this product specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Initial\_version or external\_id of the resource specification. Located in the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

Initial\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

Version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

External\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification

</td><td>

List of service specifications related to this product specification.Data type: Array of Objects

```
"serviceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalId

</td><td>

Initial\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalVersion

</td><td>

Version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.version

</td><td>

External\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range the specification is valid for.Data type: Object

 ```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Data type: String

</td></tr><tr><td>

version

</td><td>

External\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all product specifications.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productSpecification" \
--user 'username':'password'

```

Response body:

```
[
   {
      "id": "0c47f2257441c110f877ca57242ff9bd",
      "name": "SD-WAN My Device",
      "version": "v1",
      "internalVersion": "1",
      "internalId": "0c47f2257441c110f877ca57242ff9bd",
      "description": "This is my product specification ...",
      "lastUpdate": "2022-01-14 17:57:23",
      "validFor": {
         "startDateTime": "2022-01-11",
         "endDateTime": "2027-01-10"
      },
      "serviceSpecification": [
         {
            "id": "e23ae2d01bb420106ba59acf034bcb56",
            "name": "IP Sec Tunnel",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "e23ae2d01bb420106ba59acf034bcb56"
         }
      ],
      "productSpecificationRelationship": [
         {
            "id": "a6514bd3534560102f18ddeeff7b1247",
            "name": "SD-WAN Security",
            "version": "1",
            "type": "Service",
            "validFor": {
               "startDateTime": "2022-01-11",
               "endDateTime": "2027-02-12"
            }
         }
      ],
      "resourceSpecification": [
         {
            "id": "493fa60b536520103b6bddeeff7b12b6",
            "name": "Customer Premise SD-WAN Router",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "493fa60b536520103b6bddeeff7b12b6"
         }
      ],
      "productSpecCharacteristic": [
         {
            "name": "New characteristic",
            "description": "This product has new spec characteristic.",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-13 06:47:43"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "TestValue",
                  "validFor": {
                     "startDateTime": "2022-01-11"
                  }
               }
            ]
         }
      ]
   }
]
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}

Retrieves a specified product specification.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productSpecification/{id}`

### Supported request parameters

<table id="table_apt_nkz_gsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

specificationId

</td><td>

The initial\_version of the product specification to retrieve. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   description
-   externalId
-   id
-   internalId
-   internalVersion
-   lastUpdate
-   name
-   productSpecCharacteristic
-   productSpecificationRelationship
-   resourceSpecification
-   serviceSpecification
-   validFor
-   version

 Default: All fields are returned.

 Data type: String

</td></tr><tr><td>

state

</td><td>

Filter product specifications by state. Only product specifications in the specified state are returned in the response.Accepted values:

-   archived
-   draft
-   published
-   retired

Data type: String

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
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_nxj_ykz_gsb"><thead><tr><th>

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

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_zmb_ccb_jsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Required. External\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Initial\_version or external\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

Required. Initial\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether **productSpecification** represents a single product or a bundle of products.Valid values:

-   true: The product specification is a product bundle and contains multiple products.
-   false: The product specification contains a single product.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Indicates the current lifecycle status of the product specification. Valid values:

-   Active
-   Inactive
-   Draft

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Specification characteristics.Data type: Array of Objects

```
"productSpecCharacteristic": [
  {
    "description": "String",
    "name": "String",
    "productSpecCharacteristicValue": [Array],
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productSpecCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"productSpecCharacteristicValue": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

productSpecificationRelationship

</td><td>

This specification's relationships to other product specifications.Data type: Array of Objects

```
"productSpecificationRelationship": [
  {
    "id": "String",
    "type": "String",
    "validFor": {Object}
  }
]
```

</td></tr><tr><td>

productSpecificationRelationship.id

</td><td>

ID of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.type

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor

</td><td>

Date range that the relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

List of resource specifications related to this product specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Initial\_version or external\_id of the resource specification. Located in the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

Initial\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

Version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

External\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification

</td><td>

List of service specifications related to this product specification.Data type: Array of Objects

```
"serviceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalId

</td><td>

Initial\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalVersion

</td><td>

Version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.version

</td><td>

External\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range that the specification is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Data type: String

</td></tr><tr><td>

version

</td><td>

External\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a product specification.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productSpecification/0c47f2257441c110f877ca57242ff9bd" \
--user 'username':'password'
```

Response body:

```
{
   "id": "0c47f2257441c110f877ca57242ff9bd",
   "name": "SD-WAN My Device",
   "version": "v1",
   "internalVersion": "1",
   "internalId": "0c47f2257441c110f877ca57242ff9bd",
   "description": "This is my product specification ...",
   "lastUpdate": "2022-01-14 17:57:23",
   "validFor": {
      "startDateTime": "2022-01-11",
      "endDateTime": "2027-01-10"
   },
   "serviceSpecification": [
      {
         "id": "e23ae2d01bb420106ba59acf034bcb56",
         "name": "IP Sec Tunnel",
         "version": "v1",
         "internalVersion": "1",
         "internalId": "e23ae2d01bb420106ba59acf034bcb56"
      }
   ],
   "productSpecificationRelationship": [
      {
         "id": "a6514bd3534560102f18ddeeff7b1247",
         "name": "SD-WAN Security",
         "version": "v1",
         "internalVersion": "1",
         "internalId": " a6514bd3534560102f18ddeeff7b1247",
         "type": "Service",
         "validFor": {
            "startDateTime": "2022-01-11",
            "endDateTime": "2027-02-12"
         }
      }
   ],
   "resourceSpecification": [
      {
         "id": "493fa60b536520103b6bddeeff7b12b6",
         "name": "Customer Premise SD-WAN Router",
         "version": "v1",
         "internalVersion": "1",
         "internalId": "493fa60b536520103b6bddeeff7b12b6"
      }
   ],
   "productSpecCharacteristic": [
      {
         "name": "New characteristic",
         "description": "This product has new spec characteristic.",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-01-13 06:47:43"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "TestValue",
               "validFor": {
                  "startDateTime": "2022-01-11"
               }
            }
         ]
      }
   ]
}
```

## Product Catalog Open API - PATCH /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}

Updates the specified product offering.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOffering/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product offering to update. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_vxh_xvf_hsb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

List of categories that the product belongs to. Located in the Category \[sc\_category\] table.Data type: Array of Objects

 ```
"category:" [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

category.id

</td><td>

Required if using the **category** parameter. ID of the category. Located in the Category \[sc\_category\] table.Data type: String

</td></tr><tr><td>

category.name

</td><td>

Name of the category.Data type: String

Default: Blank string

</td></tr><tr><td>

channel

</td><td>

Required. Channels to use for selling the product offering.Data type: Array of Objects

```
"channel:" [
  {
    "description": "String",
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.description

</td><td>

Description of the channel.Data type: String

Default: Blank string

</td></tr><tr><td>

channel.id

</td><td>

Required. Sys\_id of the channel from the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

Default: Blank string

</td></tr><tr><td>

description

</td><td>

Required. Description of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

id

</td><td>

Required. initial\_version or external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

initial\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Format: YYYY-MM-DD 00:00:00

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Required. Name of the product offering.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array of Objects

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

productOfferingPrice

</td><td>

Price information for the product offering.Data type: Array of Objects

 ```
"productOfferingPrice": [
  {
    "price": {Object},
    "priceType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingPrice.price

</td><td>

Price information for the product offering.Data type: Object

 ```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

Default: Blank string

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.value

</td><td>

Price of the product offering including tax. Use a decimal value, for example 123.45.Data type: String

Default: Blank string

</td></tr><tr><td>

productOfferingPrice.priceType

</td><td>

The type of product offering type. Required if using the **productOfferingPrice** parameter.Valid values:

-   nonRecurring \(one-time\)
-   recurring

 Data type: String

</td></tr><tr><td>

productOfferingTerm

</td><td>

Valid contract term length in months for the product offering.Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecification

</td><td>

Required. Product specification for the product.Data type: Object

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

Required. Initial\_version or external\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

external\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td>

Characteristics of the product offering.Data type: Array of Objects

```
"prodSpecCharValueUse": [
  {
    "productSpecCharacteristicValue": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

Array containing the possible values of the characteristic.Data type: Array of objects

```
"productSpecCharacteristicValue": [
    {
      "validFor": {
        "startDateTime": "String"
      },
      "value": "String"
    }
  ]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor

</td><td>

The date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor.startDateTime

</td><td>

Start date and time of when the characteristic is valid.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.validFor.endDateTime

</td><td>

End date and time of the characteristic.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor.startDateTime

</td><td>

Start date and time of the characteristic.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Required. Date range the product offering is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

Required. End date and time of the product offering.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Required. Start date and time of the product offering.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

version

</td><td>

external\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the response body. Supported types: **application/json** or **application/xml**.Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table id="table_bts_ybj_4bc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

List of categories that the product belongs to.Data type: Array of Objects

```
"category:" [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

category.id

</td><td>

ID of the category.Data type: String

</td></tr><tr><td>

category.name

</td><td>

Name of the category.Data type: String

</td></tr><tr><td>

channel

</td><td>

Channels to use for selling the product offering.Data type: Array of Objects

```
"channel:" [
  {
    "description": "String",
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.description

</td><td>

Description of the channel.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Sys\_id of the channel from the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

href

</td><td>

A relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. initial\_version or external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

initial\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

liftcycleStatus

</td><td>

Indicates the current lifecycle status. Accepted values:-   Active
-   Draft
-   Inactive

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array of Objects

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

productOfferingPrice

</td><td>

Price information for the product offering.Data type: Array of Objects

```
"productOfferingPrice": [
  {
    "price": {Object},
    "priceType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingPrice.price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.priceType

</td><td>

Product offering price type, one-time or recurring payment.Possible values:-   nonRecurring \(one-time\)
-   recurring

Data type: String

</td></tr><tr><td>

productOfferingTerm

</td><td>

Valid contract term length for the product offering.Data type: String

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

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

external\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td>

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
  {
    "productSpecCharacteristicValue": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object}
    "productSpecCharacteristicValue": [Array],
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

Array containing the possible values of the characteristic.Data type: Array of objects

```
"productSpecCharacteristicValue": [
    {
      "validFor": {
        "startDateTime": "String"
      },
      "value": "String"
    }
  ]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor

</td><td>

The date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor.startDateTime

</td><td>

Start date and time of when the characteristic is valid.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.valueType

</td><td>

Value type of the characteristic, such as choice or email.

</td></tr><tr><td>

validFor

</td><td>

Date range the product offering is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the product offering.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the product offering.Data type: String

</td></tr><tr><td>

version

</td><td>

external\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example updates the product offering with ID d6f8d9995b020210235d85cced81c7eb with information provided in the request body.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productOffering/d6f8d9995b020210235d85cced81c7eb" \ 
--request PATCH\ 
--header "Accept:application/json" \ 
--user 'username':'password'
--data '{
  "name": "Offering 1",
  "displayName": "Offering 1",
  "description": "Offering 1 desc",
  "lastUpdate": "2024-04-01 16:05:19",
  "version": "Offering 1 EXTV",
  "validFor": {
    "startDateTime": "2028-02-29",
    "endDateTime": "2033-03-30"
  },
  "productOfferingTerm": "12_months",
  "productOfferingPrice": [
    {
      "priceType": "recurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": 632.1483
        }
      }
    },
    {
      "priceType": "nonRecurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": 1264.2966
        }
      }
    }
  ],
  "productSpecification": {
    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
    "name": "SD-WAN Service Package",
    "internalVersion": "3"
  },
  "prodSpecCharValueUse": [
    {
      "name": "Bandwidth",
      "description": "Bandwidth",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2026-12-06 02:32:11"
      },
      "productSpecCharacteristicValue": [
        {
          "value": "1 Gbps",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "5 Gbps",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 Gbps",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "500 Mbps",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "productSpecification": {
        "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
        "name": "SD-WAN Service Package",
        "internalVersion": "3"
      }
    }
  ],
  "channel": [
    {
      "id": "e561aae4c3e710105252716b7d40dd8f",
      "name": "Web"
    }
  ],
  "category": [
    {
      "id": "13e305a143b631105029d1529ab8f267",
      "name": "SD-WAN_all_offers"
    }
  ]
}'
```

Response body:

```
{
  "result": {
    "name": "Offering 1",
    "displayName": "Offering 1",
    "description": "Offering 1 desc",
    "lastUpdate": "2024-04-01 16:05:19",
    "version": "Offering 1 EXTV",
    "validFor": {
      "startDateTime": "2028-02-29",
      "endDateTime": "2033-03-30"
    },
    "productOfferingTerm": "12_months",
    "productOfferingPrice": [
      {
        "priceType": "recurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "USD",
            "value": 632.1483
          }
        }
      },
      {
        "priceType": "nonRecurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "USD",
            "value": 1264.2966
          }
        }
      }
    ],
    "productSpecification": {
      "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
      "name": "SD-WAN Service Package",
      "internalVersion": "3",
      "sys_id": "79fa17da775131108e191e599a5a997b",
      "version": "",
      "status": "published",
      "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
    },
    "prodSpecCharValueUse": [
      {
        "name": "Bandwidth",
        "description": "Bandwidth",
        "valueType": "choice",
        "validFor": {
          "startDatetime": "2026-12-06 02:32:11"
        },
        "productSpecCharacteristicValue": [
          {
            "value": "1 Gbps",
            "validFor": {
              "startDateTime": ""
            }
          },
          {
            "value": "5 Gbps",
            "validFor": {
              "startDateTime": ""
            }
          },
          {
            "value": "2 Gbps",
            "validFor": {
              "startDateTime": ""
            }
          },
          {
            "value": "500 Mbps",
            "validFor": {
              "startDateTime": ""
            }
          }
        ],
        "productSpecification": {
          "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
          "name": "SD-WAN Service Package",
          "internalVersion": "3",
          "version": "",
          "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
        }
      }
    ],
    "channel": [
      {
        "id": "e561aae4c3e710105252716b7d40dd8f",
        "name": "Web"
      }
    ],
    "category": [
      {
        "id": "13e305a143b631105029d1529ab8f267",
        "name": "SD-WAN_all_offers"
      }
    ],
    "href": "/api/sn_tmf_api/catalogmanagement/productOffering/d6f8d9995b020210235d85cced81c7eb"
  }
}
```

## Product Catalog Open API - PATCH /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}

Updates the specified product specification.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productSpecification/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the product offering to update. Located in the Product Specification\[sn\_prd\_pm\_product\_specification\] table. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Required. Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Required. External\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

id

</td><td>

Initial\_version or external\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

Required. Initial\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether **productSpecification** represents a single product or a bundle of products.

 Valid values:

-   true: The product specification is a product bundle and contains multiple products.
-   false: The product specification contains a single product.

 Data type: Boolean

 Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

 Default: Blank string

</td></tr><tr><td>

name

</td><td>

Required. Name of the specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"productSpecCharacteristic": [
   {
      "description": "String",
      "name": "String",
      "productSpecCharacteristicValue": [Array],
      "validFor": {Object},
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

productSpecCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

Array containing the possible values of the characteristic.Data type: Array of objects

```
"productSpecCharacteristicValue": [
    {
      "validFor": {
        "startDateTime": "String"
      },
      "value": "String"
    }
  ]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor

</td><td>

The date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor.startDateTime

</td><td>

Start date and time of when the characteristic is valid.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.validFor.endDateTime

</td><td>

End date and time of the characteristic.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor.startDateTime

</td><td>

Start date and time of the characteristic.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.valueType

</td><td>

The value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

productSpecificationRelationship

</td><td>

This specification's relationships to other product specifications.Data type: Array of Objects

```
"productSpecificationRelationship": [
   {
      "id": "String",
      "type": "String",
      "validFor": Object
   }
]
```

</td></tr><tr><td>

productSpecificationRelationship.id

</td><td>

Id of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.type

</td><td>

Required if using the **productSpecificationRelationship** parameter. Type of relationship.Valid values:

-   bundles
-   composed\_of

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Required. Array of resource specifications related to this product specification.Data type: Array of Objects

```
"resourceSpecification": [
   {
      "id": "String",
      "internalId": "String",
      "internalVersion": "String",
      "name": "String",
      "version": "String"
   }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Required. Initial\_version or external\_id of the resource specification. Located in the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

Initial\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

Version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

External\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification

</td><td>

List of service specifications related to this product specification.Data type: Array of Objects

```
"serviceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalId

</td><td>

Initial\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalVersion

</td><td>

Version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.version

</td><td>

External\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Required. Date range the specification is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time of the specification.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time of the specification.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

version

</td><td>

External\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_kqy_wgy_fsb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

Bad request. Possible reasons:

-   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_xj1_jcj_4bc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

href

</td><td>

A relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Initial\_version or external\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

Required. Initial\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Characteristics of the specification.Data type: Array of Objects

```
"productSpecCharacteristic": [
   {
      "description": "String",
      "name": "String",
      "productSpecCharacteristicValue": Array,
      "validFor": Object,
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

productSpecCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

Array containing the possible values of the characteristic.Data type: Array of objects

```
"productSpecCharacteristicValue": [
    {
      "validFor": {
        "startDateTime": "String"
      },
      "value": "String"
    }
  ]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor

</td><td>

The date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.validFor.startDateTime

</td><td>

Start date and time of when the characteristic is valid.Format: YYYY-MM-DD 00:00:00

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

 ```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.validFor.endDateTime

</td><td>

End date and time of the characteristic.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor.startDateTime

</td><td>

Start date and time of the characteristic.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.valueType

</td><td>

The value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

productSpecificationRelationship

</td><td>

This specification's relationships to other product specifications.Data type: Array of Objects

```
"productSpecificationRelationship": [
   {
      "id": "String",
      "type": "String",
      "validFor": Object
   }
]
```

</td></tr><tr><td>

productSpecificationRelationship.id

</td><td>

Sys\_id of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.type

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

 ```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.validFor.endDateTime

</td><td>

End date and type of the relationship.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor.startDateTime

</td><td>

Start date and type of the relationship.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

List of resource specifications related to this product specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Initial\_version or external\_id of the resource specification. Located in the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

Initial\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

Version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

External\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification

</td><td>

List of service specifications related to this product specification.Data type: Array of Objects

```
"serviceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalId

</td><td>

Initial\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalVersion

</td><td>

Version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.version

</td><td>

External\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range the specification is valid for.Data type: Object

 ```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time of the specification.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time of the specification.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

version

</td><td>

External\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example updates the product specification ID d6f8d9995b020210235d85cced81c7eb with information provided in the request body.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productSpecification/d6f8d9995b020210235d85cced81c7eb" \ 
--request PATCH\ 
--header "Accept:application/json" \ 
--user 'username':'password'
--data '{
  "id": "1001",
  "name": "SD-WAN 0322 test",
  "description": "This is my product specification ...",
  "validFor": {
    "startDateTime": "2017-06-19T00:00",
    "endDateTime": "2018-01-13T00:00"
  },
  "productSpecCharacteristic": [
    {
      "name": "New characteristic",
      "description": "This product has new spec characteristic.",
      "valueType": "label",
      "validFor": {
        "startDateTime": "2017-06-20T00:00"
      }
    }
  ],
  "serviceSpecification": [
    {
      "id": "e23ae2d01bb420106ba59acf034bcb56",
      "name": "IP Sec Tunnel",
      "internalVersion": "2"
    }
  ],
  "productSpecificationRelationship": [
    {
      "id": "a6514bd3534560102f18ddeeff7b1247",
      "name": "SD-WAN Security",
      "internalVersion": "2",
      "type": "bundles",
      "validFor": {
        "startDateTime": "2017-06-16T00:00"
      }
    }
  ],
  "resourceSpecification": [
    {
      "id": "493fa60b536520103b6bddeeff7b12b6",
      "name": "Customer Premise SD-WAN Router"
    }
  ],
  "@type": "ProductSpecification"
}
```

Response body:

```
{
  "result": {
    "id": "1001",
    "name": "SD-WAN 0322 test",
    "description": "This is my product specification ...",
    "validFor": {
      "startDateTime": "2017-06-19T00:00",
      "endDateTime": "2018-01-13T00:00"
    },
    "productSpecCharacteristic": [
      {
        "name": "New characteristic",
        "description": "This product has new spec characteristic.",
        "valueType": "label",
        "validFor": {
          "startDateTime": "2017-06-20T00:00"
        }
      }
    ],
    "serviceSpecification": [
      {
        "id": "e23ae2d01bb420106ba59acf034bcb56",
        "name": "IP Sec Tunnel",
        "internalVersion": "2",
        "sys_id": "dd8354205b550210235d85cced81c7cd",
        "version": "",
        "status": "published",
        "internalId": "e23ae2d01bb420106ba59acf034bcb56"
      }
    ],
    "productSpecificationRelationship": [
      {
        "id": "a6514bd3534560102f18ddeeff7b1247",
        "name": "SD-WAN Security",
        "internalVersion": "2",
        "type": "bundles",
        "validFor": {
          "startDateTime": "2017-06-16T00:00"
        },
        "sys_id": "7a491dd3776301108b2a1e599a5a99d3",
        "version": "",
        "status": "published",
        "internalId": "a6514bd3534560102f18ddeeff7b1247"
      }
    ],
    "resourceSpecification": [
      {
        "id": "493fa60b536520103b6bddeeff7b12b6",
        "name": "Customer Premise SD-WAN Router",
        "sys_id": "493fa60b536520103b6bddeeff7b12b6",
        "internalVersion": "1",
        "version": "",
        "status": "published",
        "internalId": "493fa60b536520103b6bddeeff7b12b6"
      }
    ],
    "@type": "ProductSpecification",
    "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/3d140fe85be1c210235d85cced81c73a"
  }
}
```

## Product Catalog Open API - POST /sn\_tmf\_api/catalogmanagement/catalog

Creates a product offering catalog.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/catalog`

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

description

</td><td>

Description of the product offering catalog.Data type: String

 Default: Blank string

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the product offering catalog from the external system.Data type: String

 Default: Blank string

</td></tr><tr><td>

name

</td><td>

Required. Name of the product offering catalog.Data type: String

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

description

</td><td>

Description of the product offering catalog.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product offering catalog from the Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product offering catalog.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a product offering catalog.

```
curl --location --request POST "https://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/catalog" \
--header "Content-Type: application/json" \
--data-raw '{
    "id": "testId",
    "name": "Catalog",
    "description": "Description"
}'
--user 'username':'password'

```

Response body.

```
{
   "id": "45715d02c3510110bc0526083c40dd6b",
   "description": "Description",
   "name": "Catalog1"
}
```

## Product Catalog Open API - POST /sn\_tmf\_api/catalogmanagement/productOffering

Creates a product offering.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOffering`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="table_vxh_xvf_hsb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

List of categories that the product belongs to. Located in the Category \[sc\_category\] table.Data type: Array of Objects

```
"category:" [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

category.id

</td><td>

Required if using the **category** parameter. ID of the category.Data type: String

</td></tr><tr><td>

category.name

</td><td>

Name of the category.Data type: String

</td></tr><tr><td>

channel

</td><td>

Required. Channels to use for selling the product offering.Data type: Array

 ```
"channel:" [
  {
    "description": "String",
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.description

</td><td>

Description of the channel.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Required. Sys\_id of the channel from the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Required. Description of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the product offering from the external system.Data type: String

</td></tr><tr><td>

href

</td><td>

A relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Required. Initial\_version or external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

initial\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Indicates the current lifecycle status. Accepted values:-   Active
-   Inactive
-   Draft

Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the product offering.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array of Objects

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

productOfferingPrice

</td><td>

Price information for the product offering.Data type: Array of Objects

```
"productOfferingPrice": [
  {
    "price": {Object},
    "priceType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingPrice.price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.priceType

</td><td>

Required if using the **productOfferingPrice** parameter. Product offering price type, one-time or recurring payment.Valid values:

-   nonRecurring \(one-time\)
-   recurring

Data type: String

</td></tr><tr><td>

productOfferingTerm

</td><td>

Valid contract term length for the product offering.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Required. Product specification for the product.Data type: Object

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

Required. Initial\_version or external\_id of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

external\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td>

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
  {
    "productSpecCharacteristicValue": Array,
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

Required. List of the possible values of the characteristic.Data type: Array of Objects

```
"productSpecCharacteristicValue": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Required. Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Required. Date range the product offering is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the product offering.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the product offering.Data type: String

</td></tr><tr><td>

version

</td><td>

external\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

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

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad request. Possible reasons: -   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

category

</td><td>

List of categories that the product belongs to.Data type: Array

 ```
"category:" [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

category.id

</td><td>

ID of the category.Data type: String

</td></tr><tr><td>

category.name

</td><td>

Name of the category.Data type: String

</td></tr><tr><td>

channel

</td><td>

Channels to use for selling the product offering.Data type: Array of Objects

 ```
"channel:" [
  {
    "description": "String",
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

channel.description

</td><td>

Description of the channel.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Sys\_id of the channel from the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.Data type: String

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

href

</td><td>

A relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. initial\_version or external\_id of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

initial\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product offering. Accepted values:

-   Active
-   Inactive
-   Draft

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

productCharacteristic

</td><td>

List of product characteristics.Data type: Array of Objects

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

productOfferingPrice

</td><td>

Price information for the product offering.Data type: Array of Objects

```
"productOfferingPrice": [
  {
    "price": {Object},
    "priceType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingPrice.price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.price.taxIncludedAmount.value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.priceType

</td><td>

Product offering price type, one-time or recurring payment.Possible values:

-   nonRecurring \(one-time\)
-   recurring

 Data type: String

</td></tr><tr><td>

productOfferingTerm

</td><td>

Valid contract term length for the product offering.Data type: String

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

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalId

</td><td>

initial\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.internalVersion

</td><td>

Version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

productSpecification.version

</td><td>

external\_version of the product specification. Located in the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td>

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
  {
    "productSpecCharacteristicValue": Array,
    "description": "String",
    "name": "String",
    "validFor": Object,
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue

</td><td>

List of the possible values of the characteristic.Data type: Array of Objects

```
"productSpecCharacteristicValue": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.valueType

</td><td>

Value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range the product offering is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the product offering.Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the product offering.Data type: String

</td></tr><tr><td>

version

</td><td>

external\_version of the product offering from the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a product offering.

```
curl --location --request POST "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productOffering" \
--header "Content-Type: application/json" \
--data-raw '{
   "id": "d52a756b5bde0110235d85cced81c7ab",
   "name": "Premium SD-WAN Offering New",
   "version": "",
   "internalVersion": "2",
   "description": "Premium SD-WAN Offering",
   "lastUpdate": "2021-08-16 04:55:52",
   "validFor": {
      "startDateTime": "2021-08-05",
      "endDateTime": "2026-09-04"
   },
   "productOfferingTerm": "24_months",
   "productOfferingPrice": [
      {
         "priceType": "recurring",
         "price": {
            "taxIncludedAmount": {
               "unit": "JPY",
               "value": 984.0913488140197
            }
         }
      },
      {
         "priceType": "nonRecurring",
         "price": {
            "taxIncludedAmount": {
               "unit": "GBP",
               "value": 2434
            }
         }
      }
   ],
   "productSpecification": {
      "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
      "name": "SD-WAN Service Package",
      "version": "v1",
      "internalVersion": "1",
      "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
   },
   "prodSpecCharValueUse": [
      {
         "name": "Tenancy",
         "description": "Tenancy",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:04:24"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Premium (>50 sites)",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance (50 site)",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Base (10 site)",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "216663aa53702010cd6dddeeff7b12b5",
            "name": "SD-WAN Controller",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "216663aa53702010cd6dddeeff7b12b5"
         }
      },
      {
         "name": "CPE Id",
         "description": "CPE Id",
         "valueType": "single_line_text",
         "validFor": {
            "startDatetime": "2021-08-15 17:50:26"
         },
         "productSpecCharacteristicValue": [],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "Routing",
         "description": "Routing",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:08:20"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "WAN Optimization",
         "description": "WAN Optimization",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:10:28"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "CPE Model",
         "description": "CPE Model",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:11:54"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "ISR",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "ASR",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v1",
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "Security Type",
         "description": "Security Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-23 12:51:13"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "a6514bd3534560102f18ddeeff7b1247",
            "name": "SD-WAN Security",
            "version": "v1",
            "internalVersion": "1",
            "internalId": " a6514bd3534560102f18ddeeff7b1247"
         }
      },
      {
         "name": "CPE Type",
         "description": "CPE Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:11:16"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Physical",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Virtual",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": "v1",
            "internalVersion": "1",
            "internalId": " 39b627aa53702010cd6dddeeff7b1202"
         }
      }
   ],
   "channel": [
      {
         "id": "e561aae4c3e710105252716b7d40dd8f",
         "name": "Web"
      }
   ],
   "category": {
      "id": "c0ed043653b02010cd6dddeeff7b1277",
      "name": "SD-WAN"
   }
}'
--user 'username':'password'

```

Response body:

```
{
   "id": "d52a756b5bde0110235d85cced81c7ab",
   "name": "Premium SD-WAN Offering New",
   "version": null,
   "internalVersion": "5",
   "description": "Premium SD-WAN Offering",
   "lastUpdate": "2021-08-16 04:55:52",
   "validFor": {
      "startDateTime": "2021-08-05",
      "endDateTime": "2026-09-04"
   },
   "productOfferingTerm": "24_months",
   "productOfferingPrice": [
      {
         "priceType": "recurring",
         "price": {
            "taxIncludedAmount": {
               "unit": "JPY",
               "value": 984.0913488140197
            }
         }
      },
      {
         "priceType": "nonRecurring",
         "price": {
            "taxIncludedAmount": {
               "unit": "GBP",
               "value": 2434
            }
         }
      }
   ],
   "productSpecification": {
      "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
      "name": "SD-WAN Service Package",
      "version": null,
      "internalVersion": "1",
      "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
   },
   "prodSpecCharValueUse": [
      {
         "name": "Tenancy",
         "description": "Tenancy",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:04:24"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Premium (>50 sites)",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance (50 site)",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Base (10 site)",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "216663aa53702010cd6dddeeff7b12b5",
            "name": "SD-WAN Controller",
            "version": null,
            "internalVersion": "1",
            "internalId": "216663aa53702010cd6dddeeff7b12b5"
         }
      },
      {
         "name": "CPE Id",
         "description": "CPE Id",
         "valueType": "single_line_text",
         "validFor": {
            "startDatetime": "2021-08-15 17:50:26"
         },
         "productSpecCharacteristicValue": [],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": null,
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "Routing",
         "description": "Routing",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:08:20"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": null,
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "WAN Optimization",
         "description": "WAN Optimization",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:10:28"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": null,
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "CPE Model",
         "description": "CPE Model",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:11:54"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "ISR",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "ASR",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": null,
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      },
      {
         "name": "Security Type",
         "description": "Security Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-23 12:51:13"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Base",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Premium",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Advance",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "a6514bd3534560102f18ddeeff7b1247",
            "name": "SD-WAN Security",
            "version": null,
            "internalVersion": "1",
            "internalId": "a6514bd3534560102f18ddeeff7b1247"
         }
      },
      {
         "name": "CPE Type",
         "description": "CPE Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2021-07-08 21:11:16"
         },
         "productSpecCharacteristicValue": [
            {
               "value": "Physical",
               "validFor": {
                  "startDateTime": ""
               }
            },
            {
               "value": "Virtual",
               "validFor": {
                  "startDateTime": ""
               }
            }
         ],
         "productSpecification": {
            "id": "39b627aa53702010cd6dddeeff7b1202",
            "name": "SD-WAN Edge Device",
            "version": null,
            "internalVersion": "1",
            "internalId": "39b627aa53702010cd6dddeeff7b1202"
         }
      }
   ],
   "channel": [
      {
         "id": "e561aae4c3e710105252716b7d40dd8f",
         "name": "Web"
      }
   ],
   "category": {
      "id": "c0ed043653b02010cd6dddeeff7b1277",
      "name": "SD-WAN"
   },
   "internalId": "fbc1c0a25b030110235d85cced81c724",
   "externalId": "d52a756b5bde0110235d85cced81c7ab"
}
```

## Product Catalog Open API - POST /sn\_tmf\_api/catalogmanagement/productSpecification

Creates a product specification.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productSpecification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="table_db1_q51_jsb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Required. Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the product specification from the external system.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. Initial\_version or external\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

Required. Initial\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Required. Name of the specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Specification characteristic.Data type: Array

```
"productSpecCharacteristic": [
   {
      "description": "String",
      "name": "String",
      "productSpecCharacteristicValue": Array,
      "validFor": Object,
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

productSpecCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecCharacteristic.name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue

</td><td>

Required. Array containing the possible values of the characteristic.Data type: Array

```
"productSpecCharacteristicValue": [
   {
      "value": "String"
   }
]
```

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue.value

</td><td>

Required. Value of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecCharacteristic.valueType

</td><td>

The value type of the characteristic, such as choice or email.Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecificationRelationship

</td><td>

This specification's relationships to other product specifications.Data type: Array

```
"productSpecificationRelationship": [
   {
      "id": "String",
      "type": "String",
      "validFor": Object
   }
]
```

</td></tr><tr><td>

productSpecificationRelationship.id

</td><td>

ID of the related specification.Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecificationRelationship.type

</td><td>

Required if using the **productSpecificationRelationship** parameter. Type of relationship.Valid values:

-   composed\_of
-   bundles

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

Default: Blank string

</td></tr><tr><td>

resourceSpecification

</td><td>

Required. Array of resource specifications related to this product specification.Data type: Array

```
"resourceSpecification": [
   {
      "id": "String",
      "internalId": "String",
      "internalVersion": "String",
      "name": "String",
      "version": "String"
   }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Required. The initial\_version or external\_id of the resource specification. Located in the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

Initial\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

Version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

External\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification

</td><td>

List of service specifications related to this product specification.Data type: Array of Objects

```
"serviceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalId

</td><td>

Initial\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalVersion

</td><td>

Version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.version

</td><td>

External\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Required. Date range the specification is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

Default: Blank string

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

Default: Blank string

</td></tr><tr><td>

version

</td><td>

External\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

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

Bad request. Possible reasons: -   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Initial\_version or external\_id of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalId

</td><td>

Required. Initial\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether **productSpecification** represents a single product or a bundle of products.Valid values:

-   true: The product specification is a product bundle and contains multiple products.
-   false: The product specification contains a single product.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current lifecycle status of the product specification. Possible values:

-   Active
-   Inactive
-   Draft

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Specification characteristic.Data type: Array

```
"productSpecCharacteristic": [
   {
      "description": "String",
      "name": "String",
      "productSpecCharacteristicValue": Array,
      "validFor": Object,
      "valueType": "String"
   }
]
```

</td></tr><tr><td>

productSpecCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue

</td><td>

Array containing the possible values of the characteristic.Data type: Array

```
"productSpecCharacteristicValue": [
   {
      "value": "String"
   }
]
```

</td></tr><tr><td>

productSpecCharacteristic.productSpecCharacteristicValue.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

 ```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.valueType

</td><td>

The value type of the characteristic, such as choice or email.Data type: String

</td></tr><tr><td>

productSpecificationRelationship

</td><td>

This specification's relationships to other product specifications.Data type: Array

```
"productSpecificationRelationship": [
   {
      "id": "String",
      "type": "String",
      "validFor": Object
   }
]
```

</td></tr><tr><td>

productSpecificationRelationship.id

</td><td>

Sys\_id of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.type

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

List of resource specifications related to this product specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Initial\_version or external\_id of the resource specification. Located in the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

Initial\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

Version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

External\_version of the resource specification. Located in the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification

</td><td>

List of service specifications related to this product specification.Data type: Array of Objects

```
"serviceSpecification": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecification.id

</td><td>

Initial\_version or external\_id of the service specification. Located in the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalId

</td><td>

Initial\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.internalVersion

</td><td>

Version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.name

</td><td>

Name of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

serviceSpecification.version

</td><td>

External\_version of the service specification. Located in the Service Specification \[sn\_prd\_pm\_service\_specification\] table.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Date range the specification is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date of the specification. Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification. Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

version

</td><td>

External\_version of the product specification from the Product Specification \[sn\_prd\_pm\_product\_specification\] table.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a product specification.

```
curl --location --request POST "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productSpecification" \
--header "Content-Type: application/json" \
--data-raw '{
   "name": "SD-WAN My Device",
   "description": "This is my product specification ...",
   "internalId": "1c3c9a325bc34110235d85cced81c7d5",
   "isBundle": false,
   "lastUpdate": "2017-06-17T00:00",
   "validFor": {
      "startDateTime": "2017-06-19T00:00",
      "endDateTime": "2018-01-13T00:00"
   },
   "productSpecCharacteristic": [
      {
         "name": "New characteristic",
         "description": "This product has new spec characteristic.",
         "valueType": "label",
         "validFor": {
            "startDateTime": "2017-06-20T00:00"
         },
         "productSpecCharacteristicValue": [
            {
               "validFor": {
                  "startDateTime": "2017-06-17T00:00"
               },
               "value": "TestValue"
            }
         ]
      }
   ],
   "serviceSpecification": [
      {
         "id": "e23ae2d01bb420106ba59acf034bcb56",
         "name": "IP Sec Tunnel"
      }
   ],
   "productSpecificationRelationship": [
      {
         "id": "a6514bd3534560102f18ddeeff7b1247",
         "name": "SD-WAN Security",
         "type": "bundles",
         "validFor": {
            "startDateTime": "2017-06-16T00:00"
         }
      }
   ],
   "resourceSpecification": [
      {
         "id": "493fa60b536520103b6bddeeff7b12b6",
         "name": "Customer Premise SD-WAN Router"
      }
   ]
}'
--user 'username':'password'

```

Response body.

```
{
   "id": "exter123",
   "name": "SD-WAN My Device",
   "version": "v1",
   "internalId": "63c3d946745d8150f877ca57242ff918",
   "description": "This is my product specification ...",
   "isBundle": false,
   "lastUpdate": "2017-06-17T00:00",
   "validFor": {
      "startDateTime": "2017-06-19T00:00",
      "endDateTime": "2018-01-13T00:00"
   },
   "productSpecCharacteristic": [
      {
         "name": "New characteristic",
         "description": "This product has new spec characteristic.",
         "valueType": "choice",
         "validFor": {
            "startDateTime": "2017-06-20T00:00"
         },
         "productSpecCharacteristicValue": [
            {
               "validFor": {
                  "startDateTime": "2017-06-17T00:00"
               },
               "value": "TestValue"
            }
         ]
      }
   ],
   "serviceSpecification": [
      {
         "id": "e23ae2d01bb420106ba59acf034bcb56",
         "name": "IP Sec Tunnel",
         "version": "v1",
         "internalVersion": "1",
         "internalId": "e23ae2d01bb420106ba59acf034bcb56"
      }
   ],
   "productSpecificationRelationship": [
      {
         "id": "a6514bd3534560102f18ddeeff7b1247",
         "name": "SD-WAN Security",
         "type": "bundles",
         "validFor": {
            "startDateTime": "2017-06-16T00:00"
         },
         "valid": true,
         "version": "v1",
         "internalVersion": "1",
         "internalId": "a6514bd3534560102f18ddeeff7b1247"
      }
   ],
   "resourceSpecification": [
      {
         "id": "493fa60b536520103b6bddeeff7b12b6",
         "name": "Customer Premise SD-WAN Router",
         "version": "v1",
         "internalVersion": "1",
         "internalId": "493fa60b536520103b6bddeeff7b12b6"
      }
   ]
}
```

