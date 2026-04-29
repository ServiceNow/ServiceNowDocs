---
title: Product Catalog Open API
description: The Product Catalog Open API provides endpoints to create and retrieve product catalogs, product offerings, and product specifications.Deletes the specified product offering.Inactivates, but doesn't delete, a price list line with a specific sys\_id.Deletes or archives the specified product specification.Retrieves a list of all product offering catalogs.Retrieves a product offering catalog.Retrieves all product offerings or a subset of product offerings, based on specified filter settings.Retrieves a specific product offering.Retrieves all price list line records in the instance.Retrieve details about a specific price list line.Retrieves all product specification records.Retrieves a specified product specification record.Updates the specified product offering.Updates a price list line record with a given sys\_id in the Price list line \[sn\_csm\_pricing\_price\_list\_line\] table.Updates the specified product specification.Creates a product offering catalog.Creates a product offering and associated product offering bundles.Creates a new price list line record in the Price List Line \[sn\_csm\_pricing\_price\_list\_line\] table.Creates a product specification record with the specified values.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 151
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Product Catalog Open API

The Product Catalog Open API provides endpoints to create and retrieve product catalogs, product offerings, and product specifications.

Use this API to manage product catalog information between external systems and the ServiceNow AI Platform. The Product Catalog Open API is a ServiceNow® implementation of the TM Forum Product Catalog Management API REST specification. This implementation is based on the [TMF620 Product Catalog Management API User Guide v5.0.0](https://www.tmforum.org/resources/specifications/tmf620-product-catalog-management-api-user-guide-v5-0-0/), September 2024.

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

Sys\_id of the product offering to delete.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

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

## Product Catalog Open API - DELETE /sn\_tmf\_api/catalogmanagement/productOfferingPrice/\{id\}

Inactivates, but doesn't delete, a price list line with a specific sys\_id.

To set a price list line to an inactive state, this DELETE method updates the end date of the price list line to today's date. A price list line with an end date prior to today's date is also considered inactive. Inactive price list lines are not retrievable in related GET methods.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOfferingPrice/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the price list line to delete.Table: Price list line \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

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
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_onp_pnw_22c"><thead><tr><th>

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
</table>### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|message|Status code with a message about the successful or failed inactivation of the price list line.|

### cURL request

The following example demonstrates how to successfully inactivate or delete a price list of the given sys\_id, 994d...

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productOfferingPrice/994d5d364f8b5210f899f61d20ce0b7c" \
--request DELETE\
--user 'username':'password'
```

Response. The response returns a 200 status code with details about the successful inactivation.

```
Status: 200 OK
"The price list line (994d5d364f8b5210f899f61d20ce0b7c) is inactive successfully"
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

Sys\_id of the product specification to delete.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

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

List of fields to return in the response. Invalid fields are ignored.Data type: String

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

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

<table id="table_nww_xgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

Description of the product offering catalog. Only returned if the field contains a value.Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product offering catalog, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product offering catalog.Data type: String

Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the price list line.Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product offering catalog.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the product offering catalog.Possible value: published

Data type: String

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
    "id": "341f4953b71a9910ff00f203ae11a9bb",
    "name": "Home Internet Plan",
    "lifecycleStatus": "Active",
    "status": "published",
    "externalSystem": "Salesforce-TMF641"
  },
  {
    "id": "69f494792b11525047f3f3e30391bf66",
    "name": "Chemical Processing",
    "lifecycleStatus": "Active",
    "description": " Catalog for Chemical Processing Industry",
    "status": "published",
    "externalSystem": "Salesforce-TMF620"
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

Sys\_id of the product offering catalog to retrieve.Data type: String

Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

</td></tr></tbody>
</table><table id="table_l5k_tkz_gsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Data type: String

Default: All fields.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

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

externalSystem

</td><td>

External system of the product offering catalog, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the product offering catalog.Data type: String

Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the price list line.Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the product offering catalog.Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves a product offering catalog for an enterprise mobile plan.

```
curl --location --request GET "https://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/catalog/69f494792b11525047f3f3e30391bf66" \
--user 'username':'password'
```

Response body.

```
{
  "id": "69f494792b11525047f3f3e30391bf66",
  "name": "Chemical Processing",
  "lifecycleStatus": "Active",
  "description": " Catalog for Chemical Processing Industry",
  "externalSystem": "Salesforce-TMF620"
}
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productOffering

Retrieves all product offerings or a subset of product offerings, based on specified filter settings.

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

Data type: String

Default: All fields are returned.

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

specification

</td><td>

Filter product offerings by product specification sys\_id. Only product offerings with the specified product specification sys\_id are returned in the response.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

state

</td><td>

Filter product offerings by state. Only product offerings in the specified state are returned in the response.Valid values:

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
|Content-Type|Data format of the request body. Only supports **application/json**.|

<table id="table_ug4_sgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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
</table>### Response body parameters

<table id="table_rqr_2s1_jsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bundledGroupProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering-entry">

Child groups of product offerings. These show hierarchical sub-grouping.Data type: Array of Objects

```
"bundledGroupProductOffering": [
  {
    "bundledGroupProductOfferingOption": {Object},
    "bundledProductOffering": [Array],
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption-entry">

A range of numbers that specifies the lower and upper limits of the number of the associated product offering that can be procured as part of the related bundled product offering.Data type: Object

```
"bundledGroupProductOfferingOption": {
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering-entry">

Child groups of product offerings associated with the bundle. Same format as **bundledProductOffering** specified below.Data type: Array of Objects

</td></tr><tr><td>

bundledGroupProductOffering.​id

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_id-entry">

Sys\_id of the bundled group record. Useful in cases where the parent product offering or group includes multiple groups.Data type: String

Table: Product Offering Relationship Group \[sn\_prd\_pm\_product\_offering\_relationship\_group\]

</td></tr><tr><td>

bundledGroupProductOffering.​name

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_name-entry">

Name of the group of child product offerings.Data type: String

</td></tr><tr><td>

bundledProductOffering

</td><td id="prodCat-offering-bundledProductOffering-entry">

List of product offerings included in the product offering bundle. The product offering bundle inherits all of the attributes of the included product offerings.Data type: Array of Objects

```
"bundledProductOffering": [
  {
    "bundledProductOfferingOption": {Object},
    "externalId": "String",
    "href": "String",
    "id": "String",
    "name": "String",
    "version": Number
  }
]
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption-entry">

Product bundle options such as the default number of product offerings and any upper and lower product offering procurement constraints.Data type: Object

```
"bundledProductOfferingOption": {
  "numberRelOfferDefault": "String",
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferDefault

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferDefault-entry">

Default number of product offerings that should be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​externalId

</td><td id="prodCat-offering-bundledProductOffering_externalId-entry">

External ID of the product offering   relationship.For additional information on product offering relationships, see [Create product offering relationships](https://www.servicenow.com/docs/access?context=som-product-config-offering-relationships&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

bundledProductOffering.​href

</td><td id="prodCat-offering-bundledProductOffering_href-entry">

Relative link to the associated product offering.Data type: String

</td></tr><tr><td>

bundledProductOffering.​id

</td><td id="prodCat-offering-bundledProductOffering_id-entry">

Sys\_id or external ID of the bundled product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

bundledProductOffering.​name

</td><td id="prodCat-offering-bundledProductOffering_name-entry">

Name of the product offering bundle.Data type: String

</td></tr><tr><td>

bundledProductOffering.​version

</td><td id="prodCat-offering-bundledProductOffering_version-entry">

Catalog version of the product offering. Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. 

</td></tr><tr><td>

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

Sys\_id of the channel.Data type: String

Table: Distribution Channel \[sn\_prd\_pm\_distribution\_channel\]

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the product offering.Data type: String

</td></tr><tr><td>

displayName

</td><td id="prodCat-offering-displayName-entry">

Display name of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the product offering. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, external\_id field

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product offering, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. Initial version or external ID of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version or external\_id field

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product offering record.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version field

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

isBundle

</td><td id="prodCat-offering-isBundle-entry">

Flag that indicates whether the product offering is a bundle.Possible values:

-   true: Product offering is a bundle.
-   false: Single product offering.

Data type: Boolean

Default: false

</td></tr><tr><td>

isSellable

</td><td id="prodCat-offering-isSellable-entry">

Flag that indicates whether the associated product offering can be sold by itself or must be part of a product offering bundle.Possible values:

-   true: Can be sold separately.
-   false: Only sold as part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product offering. Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td id="prodCat-offering-prodSpecCharValueUse-entry">

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
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

prodSpecCharValueUse.​description

</td><td id="prodCat-offering-prodSpecCharValueUse_description-entry">

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​name

</td><td id="prodCat-offering-prodSpecCharValueUse_name-entry">

Name of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue-entry">

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isDefault

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isMandatory

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isMandatory-entry">

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor-entry">

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor_startDateTime-entry">

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​value

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_value-entry">

Value of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor-entry">

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor_startDateTime-entry">

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​valueType

</td><td id="prodCat-offering-prodSpecCharValueUse_valueType-entry">

Data type of the **prodSpecCharValueUse.productSpecCharacteristicValue.value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.​value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic

</td><td id="prodCat-offering-productOfferingCharacteristic-entry">

Characteristic quality or distinctive feature of a product offering. Characteristics can take on a discrete value that is fixed at design time \(catalog authoring\), such as Mobile Plan Rank. These characteristics are not generally modifiable at inventory level.For additional information on product offering characteristics, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: Array of Objects

```
productOfferingCharacteristic": [  
  {
    "characteristicValueSpecification": [Array],
    "name": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification-entry">

List of characteristic values associated with the product offering characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [  
  { 
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "value": "String"
  }  
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isDefault

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the associated characteristic.Possible values:

-   true: Is default value.
-   false: Isn't the default value.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isMandatory

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isMandatory-entry">

Flag that indicates whether the associated characteristic value is mandatory for the associated characteristic.Possible values:

-   true: Is mandatory.
-   false: Isn't mandatory.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​value

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_value-entry">

Number or text assigned to the associated product specification characteristic .For example:

```
"characteristicValueSpecification": [
  {
    "value": "choice 1"
  },
  {
    "value": "choice 2"
  }
]
```

Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​name

</td><td id="prodCat-offering-productOfferingCharacteristic_name-entry">

Name of the associated product offering characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​valueType

</td><td id="prodCat-offering-productOfferingCharacteristic_valueType-entry">

Data type of the **productOfferingCharacteristic.​characteristicValueSpecification.​value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productOfferingPrice.​price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.​price.taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.price.​taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.price.​taxIncludedAmount.value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.​priceType

</td><td>

Type of product offering price, one-time or recurring payment.Possible values:

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
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.​id

</td><td>

Sys\_id of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalId

</td><td>

Sys\_id or internal ID of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​name

</td><td>

Name of the product specification.Data type: String

Table: In the name field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

status

</td><td id="prodCat-offering-status-entry">

Status of the product offering.Possible values:

-   draft
-   published

Data type: String

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

validFor.​​endDateTime

</td><td>

End date of the product offering.Data type: String

Format: YYY-MM-DD

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the product offering.Data type: String

Format: YYY-MM-DD

</td></tr><tr><td>

version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr></tbody>
</table>The following code example retrieves the first two product offering records.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productOffering?limit=2" \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body:

```
[
  {
    "id": "7b012c4d41ea7910f8771355f12634a4",
    "externalId": "7b012c4d41ea7910f8771355f12634a4",
    "href": "/api/sn_tmf_api/catalogmanagement/productOffering/0361dd9fd0a63110f8770dbf976be16f",
    "externalSystem": "Salesforce-TMF620",
    "name": "Ultimate internet - 1Gbps Plan",
    "displayName": "Ultimate internet - 1Gbps Plan",
    "description": "Ultimate internet - 1Gbps Plan",
    "isSellable": true,
    "lifecycleStatus": "Active",
    "isBundle": false,
    "lastUpdate": "2025-03-08 02:07:04",
    "version": "",
    "internalVersion": "1",
    "internalId": "0361dd9fd0a63110f8770dbf976be16f",
    "validFor": {
      "startDateTime": "2023-11-14",
      "endDateTime": ""
    },
    "productOfferingTerm": "not_applicable",
    "productOfferingPrice": [
      {
        "priceType": "recurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "USD",
            "value": 0
          }
        }
      },
      {
        "priceType": "nonRecurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "USD",
            "value": 0
          }
        }
      }
    ],
    "productOfferingCharacteristic": "",
    "bundledProductOffering": [],
    "bundledGroupProductOffering": [],
    "productSpecification": {},
    "prodSpecCharValueUse": [],
    "channel": "",
    "category": [
      {
        "id": "e6f0159fd0a63110f8770dbf976be18c",
        "name": "Internet"
      }
    ],
    "status": "published"
  },
  {
    "id": "313b917843235210a82ed6085bb8f2c7",
    "externalId": "313b917843235210a82ed6085bb8f2c7",
    "href": "/api/sn_tmf_api/catalogmanagement/productOffering/03c99cb53bf066509b48d69a04e45a11",
    "name": "Internet bundle",
    "displayName": "Internet bundle",
    "description": "Internet bundle",
    "isSellable": false,
    "lifecycleStatus": "Draft",
    "isBundle": true,
    "lastUpdate": "2025-04-09 15:59:09",
    "version": "",
    "internalVersion": "1",
    "internalId": "03c99cb53bf066509b48d69a04e45a11",
    "validFor": {
      "startDateTime": "2028-12-15",
      "endDateTime": "2034-01-14"
    },
    "productOfferingTerm": "not_applicable",
    "productOfferingPrice": [
      {
        "priceType": "recurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "USD",
            "value": 0
          }
        }
      },
      {
        "priceType": "nonRecurring",
        "price": {
          "taxIncludedAmount": {
            "unit": "USD",
            "value": 0
          }
        }
      }
    ],
    "productOfferingCharacteristic": [
      {
        "name": "Connectivity need",
        "valueType": "choice",
        "characteristicValueSpecification": [
          {
            "isMandatory": false,
            "isDefault": false,
            "value": "When in use"
          }
        ]
      },
      {
        "name": "Firewall Security",
        "valueType": "choice",
        "characteristicValueSpecification": [
          {
            "isMandatory": false,
            "isDefault": true,
            "value": "Premium"
          }
        ]
      }
    ],
    "bundledProductOffering": [
      {
        "href": "/api/sn_tmf_api/catalogmanagement/productOffering/57c99cb53bf066509b48d69a04e45a17",
        "id": "0f61dd9fd0a63110f8770dbf976be168",
        "externalId": "EXT-123",
        "name": "Solana Sports streaming channel",
        "version": "1",
        "bundledProductOfferingOption": {
          "numberRelOfferDefault": "1",
          "numberRelOfferLowerLimit": "1",
          "numberRelOfferUpperLimit": "1"
        }
      }
    ],
    "bundledGroupProductOffering": [
      {
        "id": "063b957843235210a82ed6085bb8f205",
        "name": "Streaming Channel",
        "bundledProductOffering": [
          {
            "href": "/api/sn_tmf_api/catalogmanagement/productOffering/5bc99cb53bf066509b48d69a04e45a1a",
            "id": "62619d9fd0a63110f8770dbf976be180",
            "externalId": "EXT-345",
            "name": "Solana Movie streaming channel",
            "version": "1",
            "bundledProductOfferingOption": {
              "numberRelOfferDefault": "1",
              "numberRelOfferLowerLimit": "1",
              "numberRelOfferUpperLimit": "1"
            }
          }
        ],
        "bundledGroupProductOfferingOption": {
          "numberRelOfferLowerLimit": "1",
          "numberRelOfferUpperLimit": "1"
        }
      }
    ],
    "productSpecification": {
      "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
      "name": "SD-WAN Service Package",
      "version": "",
      "internalVersion": "3",
      "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
    },
    "prodSpecCharValueUse": [
      {
        "name": "Tenancy",
        "description": "Tenancy",
        "valueType": "choice",
        "validFor": {
          "startDatetime": "2025-02-27 21:04:24"
        },
        "productSpecCharacteristicValue": [
          {
            "value": "Premium (>50 sites)",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": false
          },
          {
            "value": "Base (10 site)",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": false
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
        "id": "58ad5522c3702010df4773ce3640ddb2",
        "name": "Agent Assist"
      }
    ],
    "category": [
      {
        "id": "13e305a143b631105029d1529ab8f267",
        "name": "SD-WAN_all_offers"
      }
    ],
    "status": "draft"
  }
]
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productOffering/\{id\}

Retrieves a specific product offering.

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

Initial version of the product offering to retrieve.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

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

Data type: String

Default: All fields are returned.

</td></tr><tr><td>

specification

</td><td>

Filter product offerings by product specification sys\_id. Only product offerings with the specified product specification sys\_id are returned in the response.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

state

</td><td>

Filter product offerings by state. Only product offerings in the specified state are returned in the response.Valid values:

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
|Accept|Data format of the response body. Only supports **application/json**.|

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
</table>### Response body parameters

<table id="table_rqr_2s1_jsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bundledGroupProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering-entry">

Child groups of product offerings. These show hierarchical sub-grouping.Data type: Array of Objects

```
"bundledGroupProductOffering": [
  {
    "bundledGroupProductOfferingOption": {Object},
    "bundledProductOffering": [Array],
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption-entry">

A range of numbers that specifies the lower and upper limits of the number of the associated product offering that can be procured as part of the related bundled product offering.Data type: Object

```
"bundledGroupProductOfferingOption": {
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering-entry">

Child groups of product offerings associated with the bundle. Same format as **bundledProductOffering** specified below.Data type: Array of Objects

</td></tr><tr><td>

bundledGroupProductOffering.​id

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_id-entry">

Sys\_id of the bundled group record. Useful in cases where the parent product offering or group includes multiple groups.Data type: String

Table: Product Offering Relationship Group \[sn\_prd\_pm\_product\_offering\_relationship\_group\]

</td></tr><tr><td>

bundledGroupProductOffering.​name

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_name-entry">

Name of the group of child product offerings.Data type: String

</td></tr><tr><td>

bundledProductOffering

</td><td id="prodCat-offering-bundledProductOffering-entry">

List of product offerings included in the product offering bundle. The product offering bundle inherits all of the attributes of the included product offerings.Data type: Array of Objects

```
"bundledProductOffering": [
  {
    "bundledProductOfferingOption": {Object},
    "externalId": "String",
    "href": "String",
    "id": "String",
    "name": "String",
    "version": Number
  }
]
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption-entry">

Product bundle options such as the default number of product offerings and any upper and lower product offering procurement constraints.Data type: Object

```
"bundledProductOfferingOption": {
  "numberRelOfferDefault": "String",
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferDefault

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferDefault-entry">

Default number of product offerings that should be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​externalId

</td><td id="prodCat-offering-bundledProductOffering_externalId-entry">

External ID of the product offering   relationship.For additional information on product offering relationships, see [Create product offering relationships](https://www.servicenow.com/docs/access?context=som-product-config-offering-relationships&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

bundledProductOffering.​href

</td><td id="prodCat-offering-bundledProductOffering_href-entry">

Relative link to the associated product offering.Data type: String

</td></tr><tr><td>

bundledProductOffering.​id

</td><td id="prodCat-offering-bundledProductOffering_id-entry">

Sys\_id or external ID of the bundled product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

bundledProductOffering.​name

</td><td id="prodCat-offering-bundledProductOffering_name-entry">

Name of the product offering bundle.Data type: String

</td></tr><tr><td>

bundledProductOffering.​version

</td><td id="prodCat-offering-bundledProductOffering_version-entry">

Catalog version of the product offering. Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. 

</td></tr><tr><td>

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

Sys\_id of the category.Data type: String

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

channel.​description

</td><td>

Description of the channel.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Sys\_id of the channel.Data type: String

Table: Distribution Channel \[sn\_prd\_pm\_distribution\_channel\]

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the product offering.Data type: String

</td></tr><tr><td>

displayName

</td><td id="prodCat-offering-displayName-entry">

Display name of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the product offering. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, external\_id field

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product offering, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. Initial version or external ID of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version or external\_id field

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product offering record.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version field

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

isBundle

</td><td id="prodCat-offering-isBundle-entry">

Flag that indicates whether the product offering is a bundle.Possible values:

-   true: Product offering is a bundle.
-   false: Single product offering.

Data type: Boolean

Default: false

</td></tr><tr><td>

isSellable

</td><td id="prodCat-offering-isSellable-entry">

Flag that indicates whether the associated product offering can be sold by itself or must be part of a product offering bundle.Possible values:

-   true: Can be sold separately.
-   false: Only sold as part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

Format: YYYY-MM-DD HH-mm-SS

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product offering. Possible values:

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

prodSpecCharValueUse

</td><td id="prodCat-offering-prodSpecCharValueUse-entry">

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
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

prodSpecCharValueUse.​description

</td><td id="prodCat-offering-prodSpecCharValueUse_description-entry">

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​name

</td><td id="prodCat-offering-prodSpecCharValueUse_name-entry">

Name of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue-entry">

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isDefault

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isMandatory

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isMandatory-entry">

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor-entry">

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor_startDateTime-entry">

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​value

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_value-entry">

Value of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor-entry">

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor_startDateTime-entry">

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​valueType

</td><td id="prodCat-offering-prodSpecCharValueUse_valueType-entry">

Data type of the **prodSpecCharValueUse.productSpecCharacteristicValue.value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.​value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic

</td><td id="prodCat-offering-productOfferingCharacteristic-entry">

Characteristic quality or distinctive feature of a product offering. Characteristics can take on a discrete value that is fixed at design time \(catalog authoring\), such as Mobile Plan Rank. These characteristics are not generally modifiable at inventory level.For additional information on product offering characteristics, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: Array of Objects

```
productOfferingCharacteristic": [  
  {
    "characteristicValueSpecification": [Array],
    "name": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification-entry">

List of characteristic values associated with the product offering characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [  
  { 
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "value": "String"
  }  
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isDefault

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the associated characteristic.Possible values:

-   true: Is default value.
-   false: Isn't the default value.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isMandatory

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isMandatory-entry">

Flag that indicates whether the associated characteristic value is mandatory for the associated characteristic.Possible values:

-   true: Is mandatory.
-   false: Isn't mandatory.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​value

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_value-entry">

Number or text assigned to the associated product specification characteristic .For example:

```
"characteristicValueSpecification": [
  {
    "value": "choice 1"
  },
  {
    "value": "choice 2"
  }
]
```

Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​name

</td><td id="prodCat-offering-productOfferingCharacteristic_name-entry">

Name of the associated product offering characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​valueType

</td><td id="prodCat-offering-productOfferingCharacteristic_valueType-entry">

Data type of the **productOfferingCharacteristic.​characteristicValueSpecification.​value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productOfferingPrice.​price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
   "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
   "unit": "String",
   "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount.​unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount.​value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.​priceType

</td><td>

Identifies if the product offering price is a one-time or recurring payment.Possible values:

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
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.​id

</td><td>

Sys\_id of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalId

</td><td>

Sys\_id or internal ID of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​name

</td><td>

Name of the product specification.Data type: String

Table: In the name field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

status

</td><td id="prodCat-offering-status-entry">

Status of the product offering.Possible values:

-   draft
-   published

Data type: String

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

validFor.​endDateTime

</td><td>

End date of the product offering.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date of the product offering.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr></tbody>
</table>### cURL request

This example retrieves the specified product offering.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productOffering/03c99cb53bf066509b48d69a04e45a11" 
--user 'username':'password'
```

Response body:

```
{
  "id": "313b917843235210a82ed6085bb8f2c7",
  "externalId": "313b917843235210a82ed6085bb8f2c7",
  "href": "/api/sn_tmf_api/catalogmanagement/productOffering/03c99cb53bf066509b48d69a04e45a11",
  "externalSystem": "Salesforce-TMF620",
  "name": "Internet bundle",
  "displayName": "Internet bundle",
  "description": "Internet bundle",
  "isSellable": false,
  "lifecycleStatus": "Draft",
  "isBundle": true,
  "lastUpdate": "2025-04-09 15:59:09",
  "version": "",
  "internalVersion": "1",
  "internalId": "03c99cb53bf066509b48d69a04e45a11",
  "validFor": {
    "startDateTime": "2028-12-15",
    "endDateTime": "2034-01-14"
  },
  "productOfferingTerm": "not_applicable",
  "productOfferingPrice": [
    {
      "priceType": "recurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": 0
        }
      }
    },
    {
      "priceType": "nonRecurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": 0
        }
      }
    }
  ],
  "productOfferingCharacteristic": [
    {
      "name": "Connectivity need",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "isMandatory": false,
          "isDefault": false,
          "value": "When in use"
        }
      ]
    },
    {
      "name": "Firewall Security",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "isMandatory": false,
          "isDefault": true,
          "value": "Premium"
        }
      ]
    }
  ],
  "bundledProductOffering": [
    {
      "href": "/api/sn_tmf_api/catalogmanagement/productOffering/57c99cb53bf066509b48d69a04e45a17",
      "id": "0f61dd9fd0a63110f8770dbf976be168",
      "externalId": "EXT-123",
      "name": "Solana Sports streaming channel",
      "version": "1",
      "bundledProductOfferingOption": {
        "numberRelOfferDefault": "1",
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "bundledGroupProductOffering": [
    {
      "id": "063b957843235210a82ed6085bb8f205",
      "name": "Streaming Channel",
      "bundledProductOffering": [
        {
          "href": "/api/sn_tmf_api/catalogmanagement/productOffering/5bc99cb53bf066509b48d69a04e45a1a",
          "id": "62619d9fd0a63110f8770dbf976be180",
          "externalId": "EXT-345",
          "name": "Solana Movie streaming channel",
          "version": "1",
          "bundledProductOfferingOption": {
            "numberRelOfferDefault": "1",
            "numberRelOfferLowerLimit": "1",
            "numberRelOfferUpperLimit": "1"
          }
        }
      ],
      "bundledGroupProductOfferingOption": {
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "productSpecification": {
    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
    "name": "SD-WAN Service Package",
    "version": "",
    "internalVersion": "3",
    "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
  },
  "prodSpecCharValueUse": [
    {
      "name": "Tenancy",
      "description": "Tenancy",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2025-02-27 21:04:24"
      },
      "productSpecCharacteristicValue": [
        {
          "value": "Premium (>50 sites)",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "Base (10 site)",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
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
      "id": "58ad5522c3702010df4773ce3640ddb2",
      "name": "Agent Assist"
    }
  ],
  "category": [
    {
      "id": "13e305a143b631105029d1529ab8f267",
      "name": "SD-WAN_all_offers"
    }
  ],
  "status": "draft"
}
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productOfferingPrice

Retrieves all price list line records in the instance.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOfferingPrice`

### Supported request parameters

|Name|Description|
|----|-----------|
|none| |

<table id="id_nzv_ycw_22c" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

lastUpdate

</td><td>

Filter results by the date that the price line was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

name

</td><td>

Filter price list lines that belong to the name of a given price list.Table: Price Lists \[sn\_csm\_pricing\_price\_list\]

Data type: String

</td></tr><tr><td>

price.value

</td><td>

Filter results by a specific list price value.Data type: String

</td></tr><tr><td>

priceList.id

</td><td>

Filter results to return only a price list with a given sys\_id.Table: Price Lists \[sn\_csm\_pricing\_price\_list\]

Data type: String

</td></tr><tr><td>

priceType

</td><td>

Filter results by the pricing method of the product offering.Valid values:

-   recurring: Lets businesses charge recurring pricing amounts with a specified frequency.
-   one\_time: Supports one-time or recurring add-on charges and fees for a product offering.

Data type: String

</td></tr><tr><td>

productOffering.​id

</td><td>

Filter the price list line by the product offering’s sys\_id.Table: Product offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

unitOfMeasure.​id

</td><td>

Filter the price list line by sys\_id of the unit of measure.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

validFor.​endDateTime

</td><td>

Filter the price list line by a given end date and time.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Filter price list line by a given start date and time.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_fj4_nnw_22c"><thead><tr><th>

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
</table>### Response body parameters \(JSON or XML\)

<table id="id_m5r_jdw_22c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="prodOfferingPrice-response-type"><td>

@type

</td><td>

Type of price list line. Always a value of `ProductOfferingPrice`.Data type: String

</td></tr><tr id="prodOfferingPrice-response-href"><td>

href

</td><td>

URL to the price list line record in the instance.Data type: String

</td></tr><tr id="prodOfferingPrice-response-id"><td>

id

</td><td>

Sys\_id of the price list line. Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr id="prodOfferingPrice-response-isBundle"><td>

isBundle

</td><td>

Flag that indicates whether the price list line is part of a single product or a bundle of products.Valid values:

-   true: Price list line is part of a bundle.
-   false: Price list line isn't part of a bundle.

Data type: Boolean

</td></tr><tr id="prodOfferingPrice-response-lastUpdate"><td>

lastUpdate

</td><td>

Date and time that the price list line was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr id="prodOfferingPrice-response-lifeCycleStatus"><td>

lifecycleStatus

</td><td>

Current life cycle status of the price list line.Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

</td></tr><tr id="prodOfferingPrice-response-price"><td>

price

</td><td>

List price details of the price list line.Data type: Object

```
"price": {
  "units": "String",
  "value": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-price.units"><td>

price.units

</td><td>

Currency code of the price. For example, `USD` or `EUR`. Table: Currency \[fx\_currency\]

Data type: String

</td></tr><tr id="prodOfferingPrice-response-price.value"><td>

price.value

</td><td>

Value of the price.Data type: String \(represented with a number\)

</td></tr><tr id="prodOfferingPrice-response-priceList"><td>

priceList

</td><td>

Price list information associated with the price list line.Data type: Object

```
"priceList": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-priceList.id"><td>

priceList.id

</td><td>

Sys\_id of the price list in the Price List \[sn\_csm\_pricing\_price\_list\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-priceList.name"><td>

priceList.name

</td><td>

Name of the price list.Data type: String

</td></tr><tr id="prodOfferingPrice-response-priceList.type"><td>

priceList.@type

</td><td>

The type of price list. When sub-classing, this defines the sub-class extensible name. Always has a value of `priceList`.Data type: String

</td></tr><tr id="prodOfferingPrice-response-priceType"><td>

priceType

</td><td>

The pricing method of the product offering which is associated with this price list line.Possible values:

-   recurring: Charge recurring pricing amounts with a specified frequency. The value of **recurringChargePeriodType** indicates the frequency of the charge.
-   one\_time: One-time or recurring add-on charges and fees for a product offering.

Data type: String

</td></tr><tr id="prodOfferingPrice-response-productOffering"><td>

productOffering

</td><td>

Product offering that is associated with the price list line.Data type: Object

```
"productOffering": {
  "id": "String",
  "name": "String",
  "internalVersion": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-productOffering.id"><td>

productOffering.id

</td><td>

Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-productOffering.internalVersion"><td>

productOffering.​internalVersion

</td><td>

Internal version number of the product offering. For example, `PRDOF01024`. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-productOffering.name"><td>

productOffering.​name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-recurringChargePeriodType"><td>

recurringChargePeriodType

</td><td>

The periodicity or frequency of the product offering associated with this price list line. Returns a frequency type if **priceType** was set to `recurring`, otherwise returns an empty string.Possible values:

-   annually
-   monthly

Data type: String

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure"><td>

unitOfMeasure

</td><td>

Details about the unit of measure associated with the price list line.Data type: Object

```
"unitOfMeasure": {
  "id": "String",
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure.amount"><td>

unitOfMeasure.amount

</td><td>

Amount of the unit of measure.Data type: Number

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure.id"><td>

unitOfMeasure.id

</td><td>

Sys\_id of the unit of measure.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure.units"><td>

unitOfMeasure.​units

</td><td>

Type of the unit of measure associated with the price list line. For example, `year` or `bundle`.Data type: String

</td></tr><tr id="prodOfferingPrice-response-validFor"><td>

validFor

</td><td>

The duration of time that the price list line is valid for.Data type: Object

```
"validFor": {
  "endDate": "String",
  "startDate": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-validFor.endDate"><td>

validFor.endDate

</td><td>

End date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr id="prodOfferingPrice-response-validFor.startDate"><td>

validFor.startDate

</td><td>

Start date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr></tbody>
</table>### cURL request

The following example returns all two price list lines that exist on the instance.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/ catalogmanagement/productOfferingPrice " \
--request GET\
--user 'username':'password'
```

Response body.

```
[
  {
    "id": "2c4628ac7f4f9e50f8994fa63c86653c",
    "name": "new Price list",
    "lastUpdate": "2025-01-08 19:57:28",
    "isBundle": false,
    "lifecycleStatus": "Draft",
    "href": "/api/sn_tmf_api/catalogmanagement/productOfferingPrice/2c4628ac7f4f9e50f8994fa63c86653c",
    "validFor": {
      "startDateTime": "2027-03-22 22:15:58",
      "endDateTime": ""
    },
    "productOffering": {
      "id": "f2c92ac6a5260210f8774c9b4be6ce56",
      "name": "Managed Connectivity Services Supreme Bundle",
      "internalVersion": "1"
    },
    "priceType": "one_time",
    "recurringChargePeriodType": "",
    "unitOfMeasure": {
      "id": "9a7a119953020110286eddeeff7b1238",
      "amount": 1,
      "units": "Month"
    },
    "price": {
      "units": "USD",
      "value": "800"
    },
    "priceList": {
      "id": "d653246c7f4f9e50f8994fa63c86655a",
      "name": "new Price list",
      "@type": "priceList"
    },
    "@type": "ProductOfferingPrice"
  },
  {
    "id": "dfb7ec607f8f9e50f8994fa63c866569",
    "name": "new Price list",
    "lastUpdate": "2025-01-08 19:57:46",
    "isBundle": false,
    "lifecycleStatus": "Draft",
    "href": "/api/sn_tmf_api/catalogmanagement/productOfferingPrice/dfb7ec607f8f9e50f8994fa63c866569",
    "validFor": {
      "startDateTime": "2026-05-28 22:15:58",
      "endDateTime": ""
    },
    "productOffering": {
      "id": "f2c92ac6a5260210f8774c9b4be6ce56",
      "name": "Managed Connectivity Services Supreme Bundle",
      "internalVersion": "1"
    },
    "priceType": "one_time",
    "recurringChargePeriodType": "",
    "unitOfMeasure": {
      "id": "1eaa559953020110286eddeeff7b12c7",
      "amount": 1,
      "units": "Year"
    },
    "price": {
      "units": "USD",
      "value": "800"
    },
    "priceList": {
      "id": "d653246c7f4f9e50f8994fa63c86655a",
      "name": "new Price list",
      "@type": "priceList"
    },
    "@type": "ProductOfferingPrice"
  }
]
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productOfferingPrice/\{id\}

Retrieve details about a specific price list line.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOfferingPrice/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Required. Sys\_id of the price list line to retrieve. Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr></tbody>
</table><table id="id_itn_xcw_22c" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

lastUpdate

</td><td>

Filter results by the date that the price line was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

name

</td><td>

Filter price list lines that belong to the name of a given price list.Table: Price Lists \[sn\_csm\_pricing\_price\_list\]

Data type: String

</td></tr><tr><td>

price.value

</td><td>

Filter results by a specific list price value.Data type: String

</td></tr><tr><td>

priceList.id

</td><td>

Filter results to return only a price list with a given sys\_id.Table: Price Lists \[sn\_csm\_pricing\_price\_list\]

Data type: String

</td></tr><tr><td>

priceType

</td><td>

Filter results by the pricing method of the product offering.Valid values:

-   recurring: Lets businesses charge recurring pricing amounts with a specified frequency.
-   one\_time: Supports one-time or recurring add-on charges and fees for a product offering.

Data type: String

</td></tr><tr><td>

productOffering.​id

</td><td>

Filter the price list line by the product offering’s sys\_id.Table: Product offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

unitOfMeasure.​id

</td><td>

Filter the price list line by sys\_id of the unit of measure.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

validFor.​endDateTime

</td><td>

Filter the price list line by a given end date and time.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Filter price list line by a given start date and time.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

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
</table>### Response body parameters \(JSON or XML\)

<table id="id_ksw_ldw_22c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="prodOfferingPrice-response-type"><td>

@type

</td><td>

Type of price list line. Always a value of `ProductOfferingPrice`.Data type: String

</td></tr><tr id="prodOfferingPrice-response-href"><td>

href

</td><td>

URL to the price list line record in the instance.Data type: String

</td></tr><tr id="prodOfferingPrice-response-id"><td>

id

</td><td>

Sys\_id of the price list line. Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr id="prodOfferingPrice-response-isBundle"><td>

isBundle

</td><td>

Flag that indicates whether the price list line is part of a single product or a bundle of products.Valid values:

-   true: Price list line is part of a bundle.
-   false: Price list line isn't part of a bundle.

Data type: Boolean

</td></tr><tr id="prodOfferingPrice-response-lastUpdate"><td>

lastUpdate

</td><td>

Date and time that the price list line was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr id="prodOfferingPrice-response-lifeCycleStatus"><td>

lifecycleStatus

</td><td>

Current life cycle status of the price list line.Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

</td></tr><tr id="prodOfferingPrice-response-price"><td>

price

</td><td>

List price details of the price list line.Data type: Object

```
"price": {
  "units": "String",
  "value": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-price.units"><td>

price.units

</td><td>

Currency code of the price. For example, `USD` or `EUR`. Table: Currency \[fx\_currency\]

Data type: String

</td></tr><tr id="prodOfferingPrice-response-price.value"><td>

price.value

</td><td>

Value of the price.Data type: String \(represented with a number\)

</td></tr><tr id="prodOfferingPrice-response-priceList"><td>

priceList

</td><td>

Price list information associated with the price list line.Data type: Object

```
"priceList": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-priceList.id"><td>

priceList.id

</td><td>

Sys\_id of the price list in the Price List \[sn\_csm\_pricing\_price\_list\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-priceList.name"><td>

priceList.name

</td><td>

Name of the price list.Data type: String

</td></tr><tr id="prodOfferingPrice-response-priceList.type"><td>

priceList.@type

</td><td>

The type of price list. When sub-classing, this defines the sub-class extensible name. Always has a value of `priceList`.Data type: String

</td></tr><tr id="prodOfferingPrice-response-priceType"><td>

priceType

</td><td>

The pricing method of the product offering which is associated with this price list line.Possible values:

-   recurring: Charge recurring pricing amounts with a specified frequency. The value of **recurringChargePeriodType** indicates the frequency of the charge.
-   one\_time: One-time or recurring add-on charges and fees for a product offering.

Data type: String

</td></tr><tr id="prodOfferingPrice-response-productOffering"><td>

productOffering

</td><td>

Product offering that is associated with the price list line.Data type: Object

```
"productOffering": {
  "id": "String",
  "name": "String",
  "internalVersion": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-productOffering.id"><td>

productOffering.id

</td><td>

Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-productOffering.internalVersion"><td>

productOffering.​internalVersion

</td><td>

Internal version number of the product offering. For example, `PRDOF01024`. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-productOffering.name"><td>

productOffering.​name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr id="prodOfferingPrice-response-recurringChargePeriodType"><td>

recurringChargePeriodType

</td><td>

The periodicity or frequency of the product offering associated with this price list line. Returns a frequency type if **priceType** was set to `recurring`, otherwise returns an empty string.Possible values:

-   annually
-   monthly

Data type: String

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure"><td>

unitOfMeasure

</td><td>

Details about the unit of measure associated with the price list line.Data type: Object

```
"unitOfMeasure": {
  "id": "String",
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure.amount"><td>

unitOfMeasure.amount

</td><td>

Amount of the unit of measure.Data type: Number

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure.id"><td>

unitOfMeasure.id

</td><td>

Sys\_id of the unit of measure.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr id="prodOfferingPrice-response-unitOfMeasure.units"><td>

unitOfMeasure.​units

</td><td>

Type of the unit of measure associated with the price list line. For example, `year` or `bundle`.Data type: String

</td></tr><tr id="prodOfferingPrice-response-validFor"><td>

validFor

</td><td>

The duration of time that the price list line is valid for.Data type: Object

```
"validFor": {
  "endDate": "String",
  "startDate": "String"
}
```

</td></tr><tr id="prodOfferingPrice-response-validFor.endDate"><td>

validFor.endDate

</td><td>

End date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr id="prodOfferingPrice-response-validFor.startDate"><td>

validFor.startDate

</td><td>

Start date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr></tbody>
</table>### cURL request

The following example returns details of the product offering price with ID dfb7ec60...

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productOfferingPrice/dfb7ec607f8f9e50f8994fa63c866569" \
--request GET\
--user 'username':'password'
```

Response.

```
{
  "id": "dfb7ec607f8f9e50f8994fa63c866569",
  "name": "new Price list",
  "lastUpdate": "2025-01-08 19:57:46",
  "isBundle": false,
  "lifecycleStatus": "Draft",
  "href": "/api/sn_tmf_api/catalogmanagement/productOfferingPrice/dfb7ec607f8f9e50f8994fa63c866569",
  "validFor": {
    "startDateTime": "2026-05-28 22:15:58",
    "endDateTime": ""
  },
  "productOffering": {
    "id": "f2c92ac6a5260210f8774c9b4be6ce56",
    "name": "Managed Connectivity Services Supreme Bundle",
    "internalVersion": "1"
  },
  "priceType": "one_time",
  "recurringChargePeriodType": "",
  "unitOfMeasure": {
    "id": "1eaa559953020110286eddeeff7b12c7",
    "amount": 1,
    "units": "Year"
  },
  "price": {
    "units": "USD",
    "value": "800"
  },
  "priceList": {
    "id": "d653246c7f4f9e50f8994fa63c86655a",
    "name": "new Price list",
    "@type": "priceList"
  },
  "@type": "ProductOfferingPrice"
}
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productSpecification

Retrieves all product specification records.

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

Data type: String

Default: All fields are returned.

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

<table id="table_kqy_wgy_fsb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table><table id="table_pkr_rgm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

displayName

</td><td>

Display name for the product specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the product specification. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.

Data type: String

Table: In the external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product specification, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external ID of the product specification.Data type: String

Table: In the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product specification.

Data type: String

Table: In the initial\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether **productSpecification** represents a single product or a bundle of products.Possible values:

-   true: The product specification is a product bundle and contains multiple products.
-   false: The product specification contains a single product.

Data type: Boolean

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product specification. Possible values:

-   Active
-   Inactive
-   Draft

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Product specification characteristic.Data type: Array of Objects

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

productSpecCharacteristic.​description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue

</td><td>

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isDefault

</td><td>

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isMandatory

</td><td>

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor

</td><td>

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor.​​startDateTime

</td><td>

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​startDateTime

</td><td>

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be of complex or non-complex type.Data type: String

Accepted values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Test
-   Array.Object
-   Array.Date
-   Array.Decimal
-   Yes/No
-   Object
-   Array.Datetime
-   Checkbox
-   Email
-   Choice

</td></tr><tr><td>

productSpecificationRelationship

</td><td id="productSpecificationRelationship-entry">

This specification's relationships to other product specifications.Data type: Array of Objects

```
"productSpecificationRelationship": [
  {
    "compatibilityRelationshipType": "String",
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "prodSpecRelationshipOption": {Object},
    "type": "String",
    "validFor": {Object},
    "version": "String"
]
```

</td></tr><tr><td>

productSpecificationRelationship.​compatibilityRelationshipType

</td><td id="productSpecificationRelationship_compatibilityRelationshipType-entry">

Compatibility relationship type in the product specification expected values. For additional information on compatibility relationships, see [Configuring compatibility rules for horizontal relationships](https://www.servicenow.com/docs/access?context=order-mgt-compatibility-management&version=australia&pubname=australia-order-management&ft:locale=en-US).

Table: Compatibles \[sn\_compt\_mgmt\_compatibles\]

</td></tr><tr><td>

productSpecificationRelationship​.id

</td><td id="productSpecificationRelationship_id-entry">

Sys\_id of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​internalId

</td><td id="productSpecificationRelationship_internalId-entry">

Sys\_id \(internal ID\) of the product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​internalVersion

</td><td id="productSpecificationRelationship_internalVersion-entry">

Version of the product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​name

</td><td id="productSpecificationRelationship_name-entry">

Name of the product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption-entry">

Cardinality of the product specification relationship.Data type: Object

```
"prodSpecRelationshipOption": {
  "numberSpecRelDefault": "String",
  "numberSpecRelLowerLimit": "String",
  "numberSpecRelUpperLimit": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption.​numberSpecRelDefault

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption_numberSpecRelDefault-entry">

Default value of the product specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption.​numberSpecRelLowerLimit

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption_numberSpecRelLowerLimit-entry">

Minimum number of orders that can be purchased.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption.​numberSpecRelUpperLimit

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption_numberSpecRelUpperLimit-entry">

Maximum number of orders that can be purchased.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​type

</td><td id="productSpecificationRelationship_type-entry">

Type of product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor

</td><td id="productSpecificationRelationship_validFor-entry">

Date range the product specification relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​endDateTime

</td><td id="productSpecificationRelationship_validFor_endDateTime-entry">

End date of the relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​startDateTime

</td><td id="productSpecificationRelationship_validFor_startDateTime-entry">

Start date of the relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​version

</td><td id="productSpecificationRelationship_validFor_version-entry">

Version of the product specification relationship.Data type: String

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

resourceSpecification.​id

</td><td>

Sys\_id or external ID of the resource specification.Data type: String

Table: In the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalId

</td><td>

Initial version \(sys\_id\) of the resource specification record.Data type: String

Table: In the initial\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalVersion

</td><td>

Version of the resource specification.Data type: String

Table: In the version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​name

</td><td>

Name of the resource specification.Data type: String

Table: Resource Specification \[sn\_prd\_pm\_resource\_specification\]

</td></tr><tr><td>

resourceSpecification.​version

</td><td>

External version of the resource specification.Data type: String

Table: In the external\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

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

serviceSpecification.​id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​name

</td><td>

Name of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceSpecification.​version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

status

</td><td>

Status of the product specification.Possible values:

-   draft
-   published

Data type: String

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

validFor.​endDateTime

</td><td>

End date of the specification.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date of the specification.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr></tbody>
</table>### cURL request

This example retrieves the first two product specification records.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productSpecification?limit=2" \
--header "Accept:application/json" \
--user 'username':'password'

```

Response body:

```
[
  {
    "id": "0435b48a742e4a10f877468e695efa3c",
    "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/0435b48a742e4a10f877468e695efa3c",
    "externalSystem": "Salesforce-TMF620",
    "name": "Managed PoS PS",
    "displayName": "Managed PoS PS",
    "version": "",
    "internalVersion": "1",
    "internalId": "0435b48a742e4a10f877468e695efa3c",
    "description": "Managed PoS PS",
    "lastUpdate": "2032-09-26 20:07:12",
    "lifecycleStatus": "Active",
    "isBundle": false,
    "validFor": {
      "startDateTime": "2032-09-26",
      "endDateTime": ""
    },
    "serviceSpecification": [],
    "productSpecificationRelationship": [],
    "resourceSpecification": [],
    "productSpecCharacteristic": [
      {
        "productSpecCharacteristicValue": [
          {
            "value": "4",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": true
          },
          {
            "value": "2",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": true
          },
          {
            "value": "1",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": true
          }
        ],
        "name": "Number of POS Terminals",
        "description": "Number of POS Terminals",
        "valueType": "choice",
        "validFor": {
          "startDatetime": "2024-05-31 21:43:14"
        }
      },
      {
        "productSpecCharacteristicValue": [
          {
            "value": "Gold",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": true
          },
          {
            "value": "Bronze",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": true
          },
          {
            "value": "Silver",
            "validFor": {
              "startDateTime": ""
            },
            "isDefault": false,
            "isMandatory": true
          }
        ],
        "name": "Managed Service Level",
        "description": "Managed Service Level",
        "valueType": "choice",
        "validFor": {
          "startDatetime": "2024-05-31 21:15:24"
        }
      }
    ],
    "status": "published"
  },
  {
    "id": "1a0936f840102610f87798b149fd435d",
    "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/1a0936f840102610f87798b149fd435d",
    "name": "Wi-Fi Configuration Setup Service PS",
    "displayName": "Wi-Fi Configuration Setup Service PS",
    "version": "",
    "internalVersion": "1",
    "internalId": "1a0936f840102610f87798b149fd435d",
    "description": "Wi-Fi Configuration Setup Service PS",
    "lastUpdate": "2025-03-13 21:01:14",
    "lifecycleStatus": "Active",
    "isBundle": false,
    "validFor": {
      "startDateTime": "2025-03-12",
      "endDateTime": ""
    },
    "serviceSpecification": [],
    "productSpecificationRelationship": [],
    "resourceSpecification": [],
    "productSpecCharacteristic": [],
    "status": "published"
  }
]
```

## Product Catalog Open API - GET /sn\_tmf\_api/catalogmanagement/productSpecification/\{id\}

Retrieves a specified product specification record.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productSpecification/{id}`

### Supported request parameters

<table id="table_apt_nkz_gsb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Id

</td><td>

Sys\_id or Initial version of the product specification to retrieve.Data type: String

Table: In the sys\_id or initial\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

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

Data type: String

Default: All fields are returned.

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
|Accept|Data format of the response body. Only supports **application/json**.|

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

<table id="table_zmb_ccb_jsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

displayName

</td><td>

Display name for the product specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the product specification. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.

Data type: String

Table: In the external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product specification, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Sys\_id or external ID of the product specification.Data type: String

Table: In the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product specification.

Data type: String

Table: In the initial\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

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

Date the product specification was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product specification. Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product specification.Data type: String

</td></tr><tr><td>

productSpecCharacteristic

</td><td>

Product specification characteristics.Data type: Array of Objects

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

productSpecCharacteristic.​description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue

</td><td>

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isDefault

</td><td>

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isMandatory

</td><td>

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor

</td><td>

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td>

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​valueType

</td><td>

Value type of the characteristic. Can be of complex or non-complex type, such as choice or email.Accepted values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Test
-   Array.Object
-   Array.Date
-   Array.Decimal
-   Yes/No
-   Object
-   Array.Datetime
-   Checkbox
-   Email
-   Choice

Data type: String

</td></tr><tr><td>

productSpecificationRelationship

</td><td id="productSpecificationRelationship-entry">

This specification's relationships to other product specifications.Data type: Array of Objects

```
"productSpecificationRelationship": [
  {
    "compatibilityRelationshipType": "String",
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "name": "String",
    "prodSpecRelationshipOption": {Object},
    "type": "String",
    "validFor": {Object},
    "version": "String"
]
```

</td></tr><tr><td>

productSpecificationRelationship.​compatibilityRelationshipType

</td><td id="productSpecificationRelationship_compatibilityRelationshipType-entry">

Compatibility relationship type in the product specification expected values. For additional information on compatibility relationships, see [Configuring compatibility rules for horizontal relationships](https://www.servicenow.com/docs/access?context=order-mgt-compatibility-management&version=australia&pubname=australia-order-management&ft:locale=en-US).

Table: Compatibles \[sn\_compt\_mgmt\_compatibles\]

</td></tr><tr><td>

productSpecificationRelationship​.id

</td><td id="productSpecificationRelationship_id-entry">

Sys\_id of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​internalId

</td><td id="productSpecificationRelationship_internalId-entry">

Sys\_id \(internal ID\) of the product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​internalVersion

</td><td id="productSpecificationRelationship_internalVersion-entry">

Version of the product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​name

</td><td id="productSpecificationRelationship_name-entry">

Name of the product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption-entry">

Cardinality of the product specification relationship.Data type: Object

```
"prodSpecRelationshipOption": {
  "numberSpecRelDefault": "String",
  "numberSpecRelLowerLimit": "String",
  "numberSpecRelUpperLimit": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption.​numberSpecRelDefault

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption_numberSpecRelDefault-entry">

Default value of the product specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption.​numberSpecRelLowerLimit

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption_numberSpecRelLowerLimit-entry">

Minimum number of orders that can be purchased.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​prodSpecRelationshipOption.​numberSpecRelUpperLimit

</td><td id="productSpecificationRelationship_prodSpecRelationshipOption_numberSpecRelUpperLimit-entry">

Maximum number of orders that can be purchased.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​type

</td><td id="productSpecificationRelationship_type-entry">

Type of product specification relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor

</td><td id="productSpecificationRelationship_validFor-entry">

Date range the product specification relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​endDateTime

</td><td id="productSpecificationRelationship_validFor_endDateTime-entry">

End date of the relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​startDateTime

</td><td id="productSpecificationRelationship_validFor_startDateTime-entry">

Start date of the relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​version

</td><td id="productSpecificationRelationship_validFor_version-entry">

Version of the product specification relationship.Data type: String

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

resourceSpecification.​id

</td><td>

Sys\_id or external ID of the resource specification.Data type: String

Table: In the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalId

</td><td>

Initial version \(sys\_id\) of the resource specification record.Data type: String

Table: In the initial\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalVersion

</td><td>

Version of the resource specification.Data type: String

Table: In the version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​name

</td><td>

Name of the resource specification.Data type: String

Table: Resource Specification \[sn\_prd\_pm\_resource\_specification\]

</td></tr><tr><td>

resourceSpecification.​version

</td><td>

External version of the resource specification.Data type: String

Table: In the external\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

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

serviceSpecification.​id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​name

</td><td>

Name of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceSpecification.​version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

status

</td><td>

Status of the product specification.Possible values:

-   draft
-   published

Data type: String

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

validFor.​endDateTime

</td><td>

End date of the specification.Data type: String

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date of the specification.Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr></tbody>
</table>This example retrieves the specified product specification record.

```
curl --location --request GET "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productSpecification/cfe5ef6a53702010cd6dddeeff7b12f6" \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body:

```
{
  "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/497a39a7c3d312105acc9e62b540dd14",,
  "externalSystem": "Salesforce-TMF620",
  "name": "SD-WAN Service Package",
  "displayName": "SD-WAN Service Package v4",
  "version": "",
  "internalVersion": "4",
  "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "description": "SD WAN Service Package",
  "lastUpdate": "2029-04-15 20:05:37",
  "lifecycleStatus": "Active",
  "isBundle": true,
  "validFor": {
    "startDateTime": "2033-04-15",
    "endDateTime": ""
  },
  "serviceSpecification": [],
  "productSpecificationRelationship": [
    {
      "id": "a6514bd3534560102f18ddeeff7b1247",
      "name": "SD-WAN Security",
      "version": "",
      "internalVersion": "2",
      "internalId": "a6514bd3534560102f18ddeeff7b1247",
      "type": "Service",
      "compatibilityRelationshipType": "",
      "validFor": {
        "startDateTime": "2030-09-25",
        "endDateTime": "2035-10-27"
      }
    },
    {
      "id": "39b627aa53702010cd6dddeeff7b1202",
      "name": "SD-WAN Edge Device",
      "version": "",
      "internalVersion": "2",
      "internalId": "39b627aa53702010cd6dddeeff7b1202",
      "type": "Service",
      "compatibilityRelationshipType": "",
      "validFor": {
        "startDateTime": "2030-09-27",
        "endDateTime": "2035-10-27"
      }
    },
    {
      "id": "216663aa53702010cd6dddeeff7b12b5",
      "name": "SD-WAN Controller",
      "version": "",
      "internalVersion": "2",
      "internalId": "216663aa53702010cd6dddeeff7b12b5",
      "type": "Service",
      "compatibilityRelationshipType": "",
      "validFor": {
        "startDateTime": "2029-04-03",
        "endDateTime": ""
      }
    }
  ],
  "resourceSpecification": [],
  "productSpecCharacteristic": [
    {
      "productSpecCharacteristicValue": [
        {
          "value": "0.01",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "0.25",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "0.5",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "1",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        }
      ],
      "name": "Down Time",
      "description": "Down Time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-12-13 02:36:15"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1 hr",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "2 hrs",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "4 hrs",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        }
      ],
      "name": "Mean Time to Restore (MTR)",
      "description": "Mean Time to Restore (MTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-12-13 02:39:05"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1 hr",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "4 hrs",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "2 hrs",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        }
      ],
      "name": "Time to Restore (TTR)",
      "description": "Time to Restore (TTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-12-13 02:37:25"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "99.50",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "99.99",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "99.00",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "99.75",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        }
      ],
      "name": "Up Time",
      "description": "Up time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-12-13 02:34:30"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "5 Gbps",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "1 Gbps",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "500 Mbps",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "2 Gbps",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        }
      ],
      "name": "Bandwidth",
      "description": "Bandwidth",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-12-13 02:32:11"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "No",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        }
      ],
      "name": "Application Encryption",
      "description": "Application Encryption",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-12-13 02:29:08"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        },
        {
          "value": "No",
          "validFor": {
            "startDateTime": ""
          },
          "isDefault": false,
          "isMandatory": false
        }
      ],
      "name": "Application Flow Backup",
      "description": "Application Flow Backup",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-12-13 02:30:39"
      }
    }
  ],
  "status": "published"
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

Sys\_id of the product offering to update.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_vxh_xvf_hsb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bundledGroupProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering-entry">

Child groups of product offerings. These show hierarchical sub-grouping.Data type: Array of Objects

```
"bundledGroupProductOffering": [
  {
    "bundledGroupProductOfferingOption": {Object},
    "bundledProductOffering": [Array],
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption-entry">

A range of numbers that specifies the lower and upper limits of the number of the associated product offering that can be procured as part of the related bundled product offering.Data type: Object

```
"bundledGroupProductOfferingOption": {
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering-entry">

Child groups of product offerings associated with the bundle. Same format as **bundledProductOffering** specified below.Data type: Array of Objects

</td></tr><tr><td>

bundledGroupProductOffering.​id

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_id-entry">

Sys\_id of the bundled group record. Useful in cases where the parent product offering or group includes multiple groups.Data type: String

Table: Product Offering Relationship Group \[sn\_prd\_pm\_product\_offering\_relationship\_group\]

</td></tr><tr><td>

bundledGroupProductOffering.​name

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_name-entry">

Name of the group of child product offerings.Data type: String

</td></tr><tr><td>

bundledProductOffering

</td><td id="prodCat-offering-bundledProductOffering-entry">

List of product offerings included in the product offering bundle. The product offering bundle inherits all of the attributes of the included product offerings.Data type: Array of Objects

```
"bundledProductOffering": [
  {
    "bundledProductOfferingOption": {Object},
    "externalId": "String",
    "id": "String",
    "name": "String",
    "version": Number
  }
]
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption-entry">

Product bundle options such as the default number of product offerings and any upper and lower product offering procurement constraints.Data type: Object

```
"bundledProductOfferingOption": {
  "numberRelOfferDefault": "String",
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferDefault

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferDefault-entry">

Default number of product offerings that should be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​id

</td><td id="prodCat-offering-bundledProductOffering_id-entry">

Sys\_id or external ID of the bundled product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

bundledProductOffering.​externalId

</td><td id="prodCat-offering-bundledProductOffering_externalId-entry">

External ID of the product offering   relationship.For additional information on product offering relationships, see [Create product offering relationships](https://www.servicenow.com/docs/access?context=som-product-config-offering-relationships&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

bundledProductOffering.​name

</td><td id="prodCat-offering-bundledProductOffering_name-entry">

Name of the product offering bundle.Data type: String

</td></tr><tr><td>

bundledProductOffering.​version

</td><td id="prodCat-offering-bundledProductOffering_version-entry">

Catalog version of the product offering. Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. 

</td></tr><tr><td>

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

Table: Category \[sc\_category\]

</td></tr><tr><td>

category.id

</td><td>

Required if using the **category** parameter. ID of the category. Data type: String

Table: Category \[sc\_category\]

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

Required. Sys\_id of the channel.Data type: String

Table: Distribution Channel \[sn\_prd\_pm\_distribution\_channel\]

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

externalSystem

</td><td>

External system of the product offering, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

displayName

</td><td id="prodCat-offering-displayName-entry">

Display name of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the product offering. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, external\_id field

</td></tr><tr><td>

id

</td><td>

Required. Initial version or external ID of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version or external\_id field

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product offering record.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version field

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

isBundle

</td><td id="prodCat-offering-isBundle-entry">

Flag that indicates whether the product offering is a bundle.Possible values:

-   true: Product offering is a bundle.
-   false: Single product offering.

Data type: Boolean

Default: false

</td></tr><tr><td>

isSellable

</td><td id="prodCat-offering-isSellable-entry">

Flag that indicates whether the associated product offering can be sold by itself or must be part of a product offering bundle.Possible values:

-   true: Can be sold separately.
-   false: Only sold as part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

Format: YYYY-MM-DD HH:mm:SS

Default: Blank string

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product offering. Possible values:

-   Active
-   Inactive
-   Draft

Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the product offering.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td id="prodCat-offering-prodSpecCharValueUse-entry">

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
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

prodSpecCharValueUse.​description

</td><td id="prodCat-offering-prodSpecCharValueUse_description-entry">

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.name

</td><td>

Required. Name of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue-entry">

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isDefault

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isMandatory

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isMandatory-entry">

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor-entry">

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor_startDateTime-entry">

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​value

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_value-entry">

Value of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor-entry">

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor_startDateTime-entry">

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​valueType

</td><td id="prodCat-offering-prodSpecCharValueUse_valueType-entry">

Data type of the **prodSpecCharValueUse.productSpecCharacteristicValue.value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productOfferingCharacteristic

</td><td id="prodCat-offering-productOfferingCharacteristic-entry">

Characteristic quality or distinctive feature of a product offering. Characteristics can take on a discrete value that is fixed at design time \(catalog authoring\), such as Mobile Plan Rank. These characteristics are not generally modifiable at inventory level.For additional information on product offering characteristics, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: Array of Objects

```
productOfferingCharacteristic": [  
  {
    "characteristicValueSpecification": [Array],
    "name": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification-entry">

List of characteristic values associated with the product offering characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [  
  { 
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "value": "String"
  }  
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isDefault

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the associated characteristic.Possible values:

-   true: Is default value.
-   false: Isn't the default value.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isMandatory

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isMandatory-entry">

Flag that indicates whether the associated characteristic value is mandatory for the associated characteristic.Possible values:

-   true: Is mandatory.
-   false: Isn't mandatory.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​value

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_value-entry">

Number or text assigned to the associated product specification characteristic .For example:

```
"characteristicValueSpecification": [
  {
    "value": "choice 1"
  },
  {
    "value": "choice 2"
  }
]
```

Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​name

</td><td id="prodCat-offering-productOfferingCharacteristic_name-entry">

Name of the associated product offering characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​valueType

</td><td id="prodCat-offering-productOfferingCharacteristic_valueType-entry">

Data type of the **productOfferingCharacteristic.​characteristicValueSpecification.​value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

Price of the product offering including tax.Data type: String

Default: Blank string

</td></tr><tr><td>

productOfferingPrice.priceType

</td><td>

Type of product offering type. Required if using the **productOfferingPrice** parameter.Valid values:

-   nonRecurring \(one-time\)
-   recurring

Data type: String

</td></tr><tr><td>

productOfferingTerm

</td><td>

Valid contract term length for the product offering.Data type: String

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
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Required. Sys\_id or external ID of the product specification.Data type: String

Table: In the sys\_id or external\_id fields in Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productSpecification.​internalId

</td><td>

Sys\_id or internal ID of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​name

</td><td>

Name of the product specification.Data type: String

Table: In the name field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

status

</td><td id="prodCat-offering-status-entry">

Status of the product offering.Possible values:

-   draft
-   published

Data type: String

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

Required. End date and time of the product offering.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Required. Start date and time of the product offering.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

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

bundledGroupProductOffering

</td><td id="d3040e285">

Child groups of product offerings. These show hierarchical sub-grouping.Data type: Array of Objects

```
"bundledGroupProductOffering": [
  {
    "bundledGroupProductOfferingOption": {Object},
    "bundledProductOffering": [Array],
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption

</td><td id="d3040e298">

A range of numbers that specifies the lower and upper limits of the number of the associated product offering that can be procured as part of the related bundled product offering.Data type: Object

```
"bundledGroupProductOfferingOption": {
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="d3040e311">

Lower limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="d3040e322">

Upper limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledProductOffering

</td><td id="d3040e333">

Child groups of product offerings associated with the bundle. Same format as **bundledProductOffering** specified below.Data type: Array of Objects

</td></tr><tr><td>

bundledGroupProductOffering.​id

</td><td id="d3040e387">

Sys\_id of the bundled group record. Useful in cases where the parent product offering or group includes multiple groups.Data type: String

Table: Product Offering Relationship Group \[sn\_prd\_pm\_product\_offering\_relationship\_group\]

</td></tr><tr><td>

bundledGroupProductOffering.​name

</td><td id="d3040e400">

Name of the group of child product offerings.Data type: String

</td></tr><tr><td>

bundledProductOffering

</td><td>

List of product offerings included in the product offering bundle. The product offering bundle inherits all of the attributes of the included product offerings.Data type: Array of Objects

```
"bundledProductOffering": [
  {
    "bundledProductOfferingOption": {Object},
    "externalId": "String",
    "id": "String",
    "name": "String",
    "version": Number
  }
]
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption

</td><td id="d3040e425">

Product bundle options such as the default number of product offerings and any upper and lower product offering procurement constraints.Data type: Object

```
"bundledProductOfferingOption": {
  "numberRelOfferDefault": "String",
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferDefault

</td><td id="d3040e438">

Default number of product offerings that should be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="d3040e451">

Lower limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="d3040e464">

Upper limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​externalId

</td><td id="d3040e477">

External ID of the product offering   relationship.For additional information on product offering relationships, see [Create product offering relationships](https://www.servicenow.com/docs/access?context=som-product-config-offering-relationships&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

bundledProductOffering.​id

</td><td id="d3040e505">

Sys\_id or external ID of the bundled product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

bundledProductOffering.​name

</td><td id="d3040e518">

Name of the product offering bundle.Data type: String

</td></tr><tr><td>

bundledProductOffering.​version

</td><td id="d3040e529">

Catalog version of the product offering. Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. 

</td></tr><tr><td>

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

Sys\_id of the channel.Data type: String

Table: Distribution Channel \[sn\_prd\_pm\_distribution\_channel\]

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the product offering.Data type: String

</td></tr><tr><td>

displayName

</td><td id="d3040e542">

Display name of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the product offering. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, external\_id field

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product offering, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. Initial version or external ID of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version or external\_id field

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product offering record.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version field

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

isBundle

</td><td id="d3040e619">

Flag that indicates whether the product offering is a bundle.Possible values:

-   true: Product offering is a bundle.
-   false: Single product offering.

Data type: Boolean

Default: false

</td></tr><tr><td>

isSellable

</td><td id="d3040e642">

Flag that indicates whether the associated product offering can be sold by itself or must be part of a product offering bundle.Possible values:

-   true: Can be sold separately.
-   false: Only sold as part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

liftcycleStatus

</td><td>

Current lifecycle status. Accepted values:-   Active
-   Draft
-   Inactive

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td id="d3040e692">

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
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

prodSpecCharValueUse.​description

</td><td id="d3040e705">

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​name

</td><td id="prodCat-offering-prodSpecCharValueUse_name-entry">

Name of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue

</td><td id="d3040e730">

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isDefault

</td><td id="d3040e746">

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isMandatory

</td><td id="d3040e767">

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor

</td><td id="d3040e789">

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td id="d3040e802">

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​value

</td><td id="d3040e815">

Value of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​validFor

</td><td id="d3040e829">

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​validFor.​startDateTime

</td><td id="d3040e842">

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​valueType

</td><td id="d3040e855">

Data type of the **prodSpecCharValueUse.productSpecCharacteristicValue.value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.​value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic

</td><td id="d3040e918">

Characteristic quality or distinctive feature of a product offering. Characteristics can take on a discrete value that is fixed at design time \(catalog authoring\), such as Mobile Plan Rank. These characteristics are not generally modifiable at inventory level.For additional information on product offering characteristics, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: Array of Objects

```
productOfferingCharacteristic": [  
  {
    "characteristicValueSpecification": [Array],
    "name": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification

</td><td id="d3040e936">

List of characteristic values associated with the product offering characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [  
  { 
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "value": "String"
  }  
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isDefault

</td><td id="d3040e949">

Flag that indicates whether the associated characteristic value is the default value for the associated characteristic.Possible values:

-   true: Is default value.
-   false: Isn't the default value.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isMandatory

</td><td id="d3040e972">

Flag that indicates whether the associated characteristic value is mandatory for the associated characteristic.Possible values:

-   true: Is mandatory.
-   false: Isn't mandatory.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​value

</td><td id="d3040e995">

Number or text assigned to the associated product specification characteristic .For example:

```
"characteristicValueSpecification": [
  {
    "value": "choice 1"
  },
  {
    "value": "choice 2"
  }
]
```

Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​name

</td><td id="d3040e1010">

Name of the associated product offering characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​valueType

</td><td id="d3040e1022">

Data type of the **productOfferingCharacteristic.​characteristicValueSpecification.​value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productOfferingPrice.​price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount.​value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.​priceType

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
  "name": "String",
  "status": "String",
  "sys_id": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.​id

</td><td>

Sys\_id of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalId

</td><td>

Sys\_id or internal ID of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​status

</td><td>

Status of the product specification, such as published or draft.Data type: String

</td></tr><tr><td>

productSpecification.​sys\_id

</td><td>

Sys\_id of the product specification.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

</td></tr><tr><td>

productSpecification.​version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

status

</td><td id="d3040e1163">

Status of the product offering.Possible values:

-   draft
-   published

Data type: String

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

validFor.​endDateTime

</td><td>

End date of the product offering.Data type: String

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date of the product offering.Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr></tbody>
</table>The following example updates the product offering with the sys\_id 313b917843235210a82ed6085bb8f2c7 with information provided in the request body.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productOffering/313b917843235210a82ed6085bb8f2c7" \ 
--request PATCH\ 
--header "Accept:application/json" \ 
--user 'username':'password'
--data '{
  "id": "313b917843235210a82ed6085bb8f2c7",
  "name": "Internet bundle",
  "displayName": "Internet bundle",
  "description": "Internet bundle",
  "externalSystem": "Salesforce-TMF620",
  "isSellable": false,
  "lifecycleStatus": "Draft",
  "isBundle": true,
  "lastUpdate": "2025-02-05 06:39:45",
  "version": "",
  "internalVersion": "1",
  "internalId": "313b917843235210a82ed6085bb8f2c7",
  "validFor": {
    "startDateTime": "2028-12-15",
    "endDateTime": "2034-01-14"
  },
  "productOfferingTerm": "not_applicable",
  "productOfferingPrice": [
    {
      "priceType": "recurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    },
    {
      "priceType": "nonRecurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    }
  ],
  "productOfferingCharacteristic": [
    {
      "name": "Firewall Security",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "Premium",
          "isMandatory": false,
          "isDefault": true
        }
      ]
    },
    {
      "name": "Connectivity need",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "When in use",
          "isMandatory": false,
          "isDefault": false
        }
      ]
    }
  ],
  "bundledProductOffering": [
    {
     
      "id": "0f61dd9fd0a63110f8770dbf976be168",
      "name": "Solana Sports streaming channel",
      "version": "1",
      "externalId": "EXT-123",

      "bundledProductOfferingOption": {
        "numberRelOfferDefault": "1",
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "bundledGroupProductOffering": [
    {
      "id": "063b957843235210a82ed6085bb8f205",
      "name": "Streaming Channel",
      "bundledProductOffering": [
        {
          "id": "62619d9fd0a63110f8770dbf976be180",
          "name": "Solana Movie streaming channel",
          "version": "1",
          "externalId": "EXT-123",
          "bundledProductOfferingOption": {
            "numberRelOfferDefault": "1",
            "numberRelOfferLowerLimit": "1",
            "numberRelOfferUpperLimit": "1"
          }
        }
      ],
      "bundledGroupProductOfferingOption": {
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "productSpecification": {
    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
    "name": "SD-WAN Service Package",
    "version": "",
    "internalVersion": "3",
    "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
  },
  "prodSpecCharValueUse": [
    {
      "name": "Tenancy",
      "description": "Tenancy",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2024-12-18 21:04:24"
      },
      "productSpecCharacteristicValue": [
        {
          "value": "Premium (>50 sites)",
          "isDefault": false,
          "isMandatory": false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Base (10 site)",
          "isDefault": false,
          "isMandatory": false,
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
      "id": "58ad5522c3702010df4773ce3640ddb2",
      "name": "Agent Assist"
    }
  ],
  "category": [
    {
      "id": "13e305a143b631105029d1529ab8f267",
      "name": "SD-WAN_all_offers"
    }
  ],
  "status": "draft"
}'
```

Response body:

```
{
  "id": "313b917843235210a82ed6085bb8f2c7",
  "href": "/api/sn_tmf_api/catalogmanagement/productOffering/313b917843235210a82ed6085bb8f2c7",
  "externalSystem": "Salesforce-TMF620"
  "name": "Internet",
  "displayName": "Internet",
  "description": "Internet bundle",
  "isSellable": false,
  "lifecycleStatus": "Draft",
  "isBundle": true,
  "lastUpdate": "2025-02-05 06:39:45",
  "version": "",
  "internalVersion": "1",
  "internalId": "313b917843235210a82ed6085bb8f2c7",
  "validFor": {
    "startDateTime": "2028-12-15",
    "endDateTime": "2034-01-14"
  },
  "productOfferingTerm": "not_applicable",
  "productOfferingPrice": [
    {
      "priceType": "recurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    },
    {
      "priceType": "nonRecurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    }
  ],
  "productOfferingCharacteristic": [
    {
      "name": "Firewall Security",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "Premium",
          "isMandatory": false,
          "isDefault": true
        }
      ]
    },
    {
      "name": "Connectivity need",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "When in use",
          "isMandatory": false,
          "isDefault": false
        }
      ]
    }
  ],
  "bundledProductOffering": [
    {
            "id": "0f61dd9fd0a63110f8770dbf976be168",
      "name": "Solana Sports streaming channel",
      "version": "1",
      "externalId": "EXT-123",
      "bundledProductOfferingOption": {
        "numberRelOfferDefault": "1",
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    },
    {
      "id": "0f61dd9fd0a63110f8770dbf976be16c",
      "name": "Solana TV shows streaming channel",
      "version": "1",
      "externalId": "EXT-456",

      "bundledProductOfferingOption": {
        "numberRelOfferDefault": "1",
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "bundledGroupProductOffering": [
    {
      "id": "063b957843235210a82ed6085bb8f205",
      "name": "Streaming Channel",
      "bundledProductOffering": [
        {
          
          "name": "Internet",
          "version": "1",
          "externalId": "EXT-678",
          "bundledProductOfferingOption": {
            "numberRelOfferDefault": "1",
            "numberRelOfferLowerLimit": "1",
            "numberRelOfferUpperLimit": "1"
          }
        }
      ],
      "bundledGroupProductOfferingOption": {
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "3"
      }
    },
    {
      "id": "313b917843235210a82ed6085bb8f2c7",
      "name": "Streaming Channel",
      "bundledProductOffering": [
        {
          "id": "1161a4f8436b1210a82ed6085bb8f216",
          "name": "Internet",
          "version": "1",
          "externalId": "EXT-910",
          "bundledProductOfferingOption": {
            "numberRelOfferDefault": "1",
            "numberRelOfferLowerLimit": "1",
            "numberRelOfferUpperLimit": "1"
          }
        }
      ],
      "bundledGroupProductOfferingOption": {
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "productSpecification": {
    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
    "name": "SD-WAN Service Package",
    "version": "",
    "internalVersion": "3",
    "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
  },
  "prodSpecCharValueUse": [
    {
      "name": "Tenancy",
      "description": "Tenancy",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2024-12-18 21:04:24"
      },
      "productSpecCharacteristicValue": [
        {
          "value": "Premium (>50 sites)",
          "isDefault": false,
          "isMandatory": false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Advance (50 site)",
          "isDefault": false,
          "isMandatory": false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Base (10 site)",
          "isDefault": false,
          "isMandatory": false,
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
      "id": "58ad5522c3702010df4773ce3640ddb2",
      "name": "Agent Assist"
    }
  ],
  "category": [
    {
      "id": "13e305a143b631105029d1529ab8f267",
      "name": "SD-WAN_all_offers"
    }
  ],
  "status": "draft"
}
```

## Product Catalog Open API - PATCH /sn\_tmf\_api/catalogmanagement/productOfferingPrice/\{id\}

Updates a price list line record with a given sys\_id in the Price list line \[sn\_csm\_pricing\_price\_list\_line\] table.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOfferingPrice/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Required. Sys\_id of the price list line to retrieve. Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="id_abw_fvw_22c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Required. Type of price list line. Always a value of `ProductOfferingPrice`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

The external ID of the price list line.Data type: String

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether the price list line is part of a single product or a bundle of products.Valid values:

-   true: Price list line is part of a bundle.
-   false: Price list line isn't part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Required. Date that the price line was last updated.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

lifeCycleStatus

</td><td>

Required. Current life cycle status of the product list line.Valid values:

-   active
-   draft
-   inactive

Data type: String

Default: draft

</td></tr><tr><td>

name

</td><td>

Required. Name to give the price list line.Data type: String

</td></tr><tr><td>

price

</td><td>

Required. List price details of the price list line.Data type: Object

```
"price": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

price.unit

</td><td>

Required. Currency code of the price list line. For example, `USD` or `EUR`.Table: Currency \[fx\_currency\] table.

Data type: String

</td></tr><tr><td>

price.value

</td><td>

Required. Value of the price.Data type: String \(represented with a number. For example, `"800"`.\)

</td></tr><tr><td>

priceList

</td><td>

Required. Price list information associated with the price list line.Data type: Object

```
"priceList": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

priceList.id

</td><td>

Required. Sys\_id of the price list line.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

priceList.name

</td><td>

Name of the price list line.Data type: String

</td></tr><tr><td>

priceList.@type

</td><td>

The type of price list line. When sub-classing, this defines the sub-class extensible name. Value is always `priceList`.Data type: String

</td></tr><tr><td>

priceType

</td><td>

Required. Filter the price list line by the pricing method of the product offering.Valid values:

-   recurring: Charge recurring pricing amounts with a specified frequency. Frequency is set in the **recurringChargePeriodType** parameter.
-   one\_time: Supports one-time or recurring add-on charges and fees for a product offering.

Data type: String

Default: recurring

</td></tr><tr><td>

productOffering

</td><td>

Required. Product offering of the price list line.Data type: Object

```
"productOffering": {
  "id": "String",
  "name": "String",
  "internalVersion": "String"
}
```

</td></tr><tr><td>

productOffering.​id

</td><td>

Required. Sys\_id of the product offering.Table: Product offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

productOffering.​internalVersion

</td><td>

Internal version number of the product offering.Data type: String \(represented with a number. For example, `"1"`.\)

</td></tr><tr><td>

productOffering.​name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

recurringChargePeriodType

</td><td>

Required if **priceType** is recurring. Commitment terms that are selected when the product offering was created.Valid values:

-   annually
-   monthly

Data type: String

</td></tr><tr><td>

unitOfMeasure

</td><td>

Required. Details about the unit of measure associated with the price list line.Data type: Object

```
"unitOfMeasure": {
  "id": "String",
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

unitOfMeasure.​amount

</td><td>

Amount of the unit of measure.Data type: Number

</td></tr><tr><td>

unitOfMeasure.​id

</td><td>

Required. Sys\_id of the unit of measure in the Price Line List table.Table: Price List Line \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

unitOfMeasure.​units

</td><td>

Type of the unit of measure associated with the price list line. For example, `each` or `bundle`.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Required. The duration of time that the price list line is valid for.Data type: Object

```
"validFor": {
  "endDate": "String",
  "startDate": "String"
}
```

</td></tr><tr><td>

validFor.endDate

</td><td>

End date that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time that the price list line is valid for.Format: YYYY-MM-DD HH:mm:ss

Data type: String \(glide\_date\)

</td></tr><tr><td>

validFor.startDate

</td><td>

Start date that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time that the price list line is valid for.Format: YYYY-MM-DD HH:mm:ss

Data type: String \(glide\_date\)

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

<table id="table_onp_pnw_22c"><thead><tr><th>

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
</table>### Response body parameters \(JSON or XML\)

<table id="table_r3r_rvw_22c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the price list line. Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

href

</td><td>

URL to the price list line record in the instance.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date and time that the price list line was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

validFor

</td><td>

The duration of time that the price list line is valid for.Data type: Object

```
"validFor": {
  "endDate": "String",
  "startDate": "String"
}
```

</td></tr><tr><td>

validFor.endDate

</td><td>

End date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

validFor.startDate

</td><td>

Start date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether the price list line is part of a single product or a bundle of products.Valid values:

-   true: Price list line is part of a bundle.
-   false: Price list line isn't part of a bundle.

Data type: Boolean

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the price list line.Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that is associated with the price list line.Data type: Object

```
"productOffering": {
  "id": "String",
  "name": "String",
  "internalVersion": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.​internalVersion

</td><td>

Internal version number of the product offering. For example, `PRDOF01024`. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.​name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

priceType

</td><td>

The pricing method of the product offering which is associated with this price list line.Possible values:

-   recurring: Charge recurring pricing amounts with a specified frequency. The value of **recurringChargePeriodType** indicates the frequency of the charge.
-   one\_time: One-time or recurring add-on charges and fees for a product offering.

Data type: String

</td></tr><tr><td>

recurringChargePeriodType

</td><td>

The periodicity or frequency of the product offering associated with this price list line. Returns a frequency type if **priceType** was set to `recurring`, otherwise returns an empty string.Possible values:

-   annually
-   monthly

Data type: String

</td></tr><tr><td>

unitOfMeasure

</td><td>

Details about the unit of measure associated with the price list line.Data type: Object

```
"unitOfMeasure": {
  "id": "String",
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

unitOfMeasure.amount

</td><td>

Amount of the unit of measure.Data type: Number

</td></tr><tr><td>

unitOfMeasure.id

</td><td>

Sys\_id of the unit of measure.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

unitOfMeasure.​units

</td><td>

Type of the unit of measure associated with the price list line. For example, `year` or `bundle`.Data type: String

</td></tr><tr><td>

price

</td><td>

List price details of the price list line.Data type: Object

```
"price": {
  "units": "String",
  "value": "String"
}
```

</td></tr><tr><td>

price.units

</td><td>

Currency code of the price. For example, `USD` or `EUR`. Table: Currency \[fx\_currency\]

Data type: String

</td></tr><tr><td>

price.value

</td><td>

Value of the price.Data type: String \(represented with a number\)

</td></tr><tr><td>

priceList

</td><td>

Price list information associated with the price list line.Data type: Object

```
"priceList": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

priceList.id

</td><td>

Sys\_id of the price list in the Price List \[sn\_csm\_pricing\_price\_list\] table.Data type: String

</td></tr><tr><td>

priceList.name

</td><td>

Name of the price list.Data type: String

</td></tr><tr><td>

priceList.@type

</td><td>

The type of price list. When sub-classing, this defines the sub-class extensible name. Always has a value of `priceList`.Data type: String

</td></tr><tr><td>

@type

</td><td>

Always a value of `ProductOfferingPrice`. When sub-classing, this defines the sub-class extensible name.Data type: String

</td></tr><tr><td>

state

</td><td>

The state of the price list which is associated with this price list line.Data type: String

</td></tr><tr><td>

externalId

</td><td>

The external ID of this price list line.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example updates the dates of when the product offering price with ID 3ddd0... is valid for.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productOfferingPrice/994d5d364f8b5210f899f61d20ce0b7c" \
--request patch\
--user 'username':'password'
--data {
  "validFor": {
    "endDateTime": "2024-06-25 15:15:58"
  }
}
```

Response body:

```
{
  "validFor": {
    "endDateTime": "2024-06-25 15:15:58"
  },
  "id": "994d5d364f8b5210f899f61d20ce0b7c",
  "name": "new Price list",
  "lastUpdate": "2025-01-16 00:15:32",
  "href": "/api/sn_tmf_api/catalogmanagement/productOfferingPrice/994d5d364f8b5210f899f61d20ce0b7c",
  "lifecycleStatus": "Draft"
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

Sys\_id of the product offering to update.Data type: String

Table: Product Specification \[sn\_prd\_pm\_product\_specification\]

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

Required. External ID of the product specification. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.

Data type: String

Table: In the external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

id

</td><td>

Sys\_id or external ID of the product specification.Data type: String

Table: In the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Required. Sys\_id or internal ID of the product specification.

Data type: String

Table: In the initial\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

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

productSpecCharacteristic.​description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue

</td><td>

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isDefault

</td><td>

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isMandatory

</td><td>

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor

</td><td>

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td>

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​endDateTime

</td><td>

End date and time of the characteristic.Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​startDateTime

</td><td>

Start date and time of the characteristic.Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be of complex or non-complex type.Data type: String

Accepted values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Test
-   Array.Object
-   Array.Date
-   Array.Decimal
-   Yes/No
-   Object
-   Array.Datetime
-   Checkbox
-   Email
-   Choice

Default value: empty string

</td></tr><tr><td>

productSpecificationRelationship

</td><td>

Details of the specification's relationships to other product specifications.Data type: Array of Objects

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

productSpecificationRelationship.​id

</td><td>

ID of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​type

</td><td>

Required if using the **productSpecificationRelationship** parameter. Type of relationship.Valid values:

-   bundles
-   composed\_of

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​endDateTime

</td><td>

End date of the relationship.Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​startDateTime

</td><td>

Start date of the relationship.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Required. Details of the resource specifications related to this product specification.Data type: Array of Objects

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

resourceSpecification.​id

</td><td>

Required. Initial version or external ID of the resource specification.Data type: String

Table: In the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalId

</td><td>

Initial version \(sys\_id\) of the resource specification record.Data type: String

Table: In the initial\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalVersion

</td><td>

Version of the resource specification.Data type: String

Table: In the version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​name

</td><td>

Name of the resource specification.Data type: String

Table: Resource Specification \[sn\_prd\_pm\_resource\_specification\]

</td></tr><tr><td>

resourceSpecification.​version

</td><td>

External version of the resource specification.Data type: String

Table: In the external\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

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

serviceSpecification.​id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​name

</td><td>

Name of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceSpecification.​version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

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

validFor.​endDateTime

</td><td>

End date and time of the specification.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date and time of the specification.Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

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

Bad request. Possible reasons: -   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr></tbody>
</table>### Response body parameters

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

Relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external ID of the product specification.Data type: String

Table: In the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Required. Sys\_id or internal ID of the product specification.

Data type: String

Table: In the initial\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

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
    "productSpecCharacteristicValue": [Array],
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productSpecCharacteristic.​description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue

</td><td>

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isDefault

</td><td>

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isMandatory

</td><td>

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor

</td><td>

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td>

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​endDateTime

</td><td>

End date and time of the characteristic.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​startDateTime

</td><td>

Start date and time of the characteristic.Format: YYYY-MM-DD 00:00:00.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be of complex or non-complex type.Data type: String

Accepted values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Test
-   Array.Object
-   Array.Date
-   Array.Decimal
-   Yes/No
-   Object
-   Array.Datetime
-   Checkbox
-   Email
-   Choice

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

productSpecificationRelationship.​id

</td><td>

Sys\_id of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​type

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​endDateTime

</td><td>

End date and type of the relationship.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​startDateTime

</td><td>

Start date and type of the relationship.Format: YYYY-MM-DD

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

resourceSpecification.​id

</td><td>

Sys\_id or external ID of the resource specification.Data type: String

Table: In the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalId

</td><td>

Initial version \(sys\_id\) of the resource specification record.Data type: String

Table: In the initial\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalVersion

</td><td>

Version of the resource specification.Data type: String

Table: In the version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​name

</td><td>

Name of the resource specification.Data type: String

Table: Resource Specification \[sn\_prd\_pm\_resource\_specification\]

</td></tr><tr><td>

resourceSpecification.​version

</td><td>

External version of the resource specification.Data type: String

Table: In the external\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

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

serviceSpecification.​id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​name

</td><td>

Name of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceSpecification.​version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

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

validFor.​endDateTime

</td><td>

End date and time of the specification.Format: YYYY-MM-DD HH:mm:SS.

Data type: String

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date and time of the specification.Format: YYYY-MM-DD HH:mm:SS.

Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr></tbody>
</table>The following example updates the product specification ID d6f8d9995b020210235d85cced81c7eb with information provided in the request body.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productSpecification/d6f8d9995b020210235d85cced81c7eb" \ 
--request PATCH\ 
--header "Accept:application/json" \ 
--user 'username':'password'
--data '{
  "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/cfe5ef6a53702010cd6dddeeff7b12f6",
  "name": "SD-WAN Service Package",
  "displayName": "SD-WAN Service Package v3",
  "version": "",
  "internalVersion": "3",
  "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "description": "SD WAN Service Package",
  "lastUpdate": "2027-10-11 06:58:12",
  "isBundle": true,
  "validFor": {
    "startDateTime": "2029-02-05",
    "endDateTime": ""
  },
  "serviceSpecification": [],
  "productSpecificationRelationship": [
    {
      "id": "216663aa53702010cd6dddeeff7b12b5",
      "name": "SD-WAN Controller",
      "version": "",
      "internalVersion": "1",
      "internalId": "216663aa53702010cd6dddeeff7b12b5",
      "type": "Service",
      "validFor": {
        "startDateTime": "2025-01-24",
        "endDateTime": ""
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "1",
        "numberSpecRelUpperLimit": "1"
      }
    },
    {
      "id": "39b627aa53702010cd6dddeeff7b1202",
      "name": "SD-WAN Edge Device",
      "version": "",
      "internalVersion": "2",
      "internalId": "39b627aa53702010cd6dddeeff7b1202",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-05",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "2",
        "numberSpecRelUpperLimit": "4"
      }
    },
    {
      "id": "a6514bd3534560102f18ddeeff7b1247",
      "name": "SD-WAN Security",
      "version": "",
      "internalVersion": "2",
      "internalId": "a6514bd3534560102f18ddeeff7b1247",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-03",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "4",
        "numberSpecRelUpperLimit": "20"
      }
    }
  ],
  "resourceSpecification": [],
  "productSpecCharacteristic": [
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.25",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.01",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.5",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Down Time",
      "description": "Down Time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:36:15"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "500 Mbps",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "5 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Bandwidth",
      "description": "Bandwidth",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:32:11"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "4 hrs",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 hr",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Time to Restore (TTR)",
      "description": "Time to Restore (TTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:37:25"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1 hr",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "4 hrs",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Mean Time to Restore (MTR)",
      "description": "Mean Time to Restore (MTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:39:05"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Flow Backup",
      "description": "Application Flow Backup",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:30:39"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "99.00",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.50",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.75",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.99",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Up Time",
      "description": "Up time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:34:30"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Encryption",
      "description": "Application Encryption",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:29:08"
      }
    }
  ],
  "status": "published"
}'
```

Response body:

```
{ 
  "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/cfe5ef6a53702010cd6dddeeff7b12f6",
  "name": "SD-WAN Service Package",
  "displayName": "SD-WAN Service Package v3",
  "version": "",
  "internalVersion": "3",
  "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "description": "SD WAN Service Package",
  "lastUpdate": "2027-10-11 06:58:12",
  "isBundle": true,
  "validFor": {
    "startDateTime": "2029-02-05",
    "endDateTime": ""
  },
  "serviceSpecification": [],
  "productSpecificationRelationship": [
    {
      "id": "216663aa53702010cd6dddeeff7b12b5",
      "name": "SD-WAN Controller",
      "version": "",
      "internalVersion": "1",
      "internalId": "216663aa53702010cd6dddeeff7b12b5",
      "type": "Service",
      "validFor": {
        "startDateTime": "2025-01-24",
        "endDateTime": ""
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "1",
        "numberSpecRelUpperLimit": "1"
      }
    },
    {
      "id": "39b627aa53702010cd6dddeeff7b1202",
      "name": "SD-WAN Edge Device",
      "version": "",
      "internalVersion": "2",
      "internalId": "39b627aa53702010cd6dddeeff7b1202",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-05",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "2",
        "numberSpecRelUpperLimit": "4"
      }
    },
    {
      "id": "a6514bd3534560102f18ddeeff7b1247",
      "name": "SD-WAN Security",
      "version": "",
      "internalVersion": "2",
      "internalId": "a6514bd3534560102f18ddeeff7b1247",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-03",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "4",
        "numberSpecRelUpperLimit": "20"
      }
    }
  ],
  "resourceSpecification": [],
  "productSpecCharacteristic": [
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.25",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.01",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.5",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Down Time",
      "description": "Down Time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:36:15"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "500 Mbps",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "5 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Bandwidth",
      "description": "Bandwidth",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:32:11"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "4 hrs",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 hr",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Time to Restore (TTR)",
      "description": "Time to Restore (TTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:37:25"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1 hr",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "4 hrs",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Mean Time to Restore (MTR)",
      "description": "Mean Time to Restore (MTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:39:05"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Flow Backup",
      "description": "Application Flow Backup",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:30:39"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "99.00",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.50",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.75",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.99",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Up Time",
      "description": "Up time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:34:30"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Encryption",
      "description": "Application Encryption",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:29:08"
      }
    }
  ],
  "status": "published"
}'
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

Sys\_id of the product offering catalogData type: String

Table: Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\]

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

Response body:

```
{
   "id": "45715d02c3510110bc0526083c40dd6b",
   "description": "Description",
   "name": "Catalog1"
}
```

## Product Catalog Open API - POST /sn\_tmf\_api/catalogmanagement/productOffering

Creates a product offering and associated product offering bundles.

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

bundledGroupProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering-entry">

Child groups of product offerings. These show hierarchical sub-grouping.Data type: Array of Objects

```
"bundledGroupProductOffering": [
  {
    "bundledGroupProductOfferingOption": {Object},
    "bundledProductOffering": [Array],
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption-entry">

A range of numbers that specifies the lower and upper limits of the number of the associated product offering that can be procured as part of the related bundled product offering.Data type: Object

```
"bundledGroupProductOfferingOption": {
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledGroupProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledProductOffering

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering-entry">

Child groups of product offerings associated with the bundle. Same format as **bundledProductOffering** specified below.Data type: Array of Objects

</td></tr><tr><td>

bundledGroupProductOffering.​id

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_id-entry">

Sys\_id of the bundled group record. Useful in cases where the parent product offering or group includes multiple groups.Data type: String

Table: Product Offering Relationship Group \[sn\_prd\_pm\_product\_offering\_relationship\_group\]

</td></tr><tr><td>

bundledGroupProductOffering.​name

</td><td id="prodCat-offering-bundledGroupProductOffering_bundledProductOffering_name-entry">

Name of the group of child product offerings.Data type: String

</td></tr><tr><td>

bundledProductOffering

</td><td id="prodCat-offering-bundledProductOffering-entry">

List of product offerings included in the product offering bundle. The product offering bundle inherits all of the attributes of the included product offerings.Data type: Array of Objects

```
"bundledProductOffering": [
  {
    "bundledProductOfferingOption": {Object},
    "externalId": "String",
    "id": "String",
    "name": "String",
    "version": Number
  }
]
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption-entry">

Product bundle options such as the default number of product offerings and any upper and lower product offering procurement constraints.Data type: Object

```
"bundledProductOfferingOption": {
  "numberRelOfferDefault": "String",
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferDefault

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferDefault-entry">

Default number of product offerings that should be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferLowerLimit-entry">

Lower limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="prodCat-offering-bundledProductOffering_bundledProductOfferingOption_numberRelOfferUpperLimit-entry">

Upper limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​externalId

</td><td id="prodCat-offering-bundledProductOffering_externalId-entry">

External ID of the product offering   relationship.For additional information on product offering relationships, see [Create product offering relationships](https://www.servicenow.com/docs/access?context=som-product-config-offering-relationships&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

bundledProductOffering.​id

</td><td id="prodCat-offering-bundledProductOffering_id-entry">

Sys\_id or external ID of the bundled product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

bundledProductOffering.​name

</td><td id="prodCat-offering-bundledProductOffering_name-entry">

Name of the product offering bundle.Data type: String

</td></tr><tr><td>

bundledProductOffering.​version

</td><td id="prodCat-offering-bundledProductOffering_version-entry">

Catalog version of the product offering. Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. 

</td></tr><tr><td>

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

Required if using the **category** parameter. ID of the category.Data type: String

Table: Category \[sc\_category\]

</td></tr><tr><td>

category.name

</td><td>

Name of the category.Data type: String

Table: Category \[sc\_category\]

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

</td></tr><tr><td>

channel.id

</td><td>

Required. Sys\_id of the channel.Data type: String

Table: Distribution Channel \[sn\_prd\_pm\_distribution\_channel\]

</td></tr><tr><td>

channel.name

</td><td>

Name of the channel.Data type: String

</td></tr><tr><td>

description

</td><td>

Required. Description of the product offering.Data type: String

</td></tr><tr><td>

displayName

</td><td id="prodCat-offering-displayName-entry">

Display name of the product offering.Data type: String

</td></tr><tr><td>

externalId

</td><td>

Unique identifier for the product offering from the external system.Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product offering, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

</td></tr><tr><td>

id

</td><td>

Required. Initial version or external ID of the product offering.Data type: String

Table: In the initial\_version or external\_id fields of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product offering record.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version field

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

isBundle

</td><td id="prodCat-offering-isBundle-entry">

Flag that indicates whether the product offering is a bundle.Possible values:

-   true: Product offering is a bundle.
-   false: Single product offering.

Data type: Boolean

Default: false

</td></tr><tr><td>

isSellable

</td><td id="prodCat-offering-isSellable-entry">

Flag that indicates whether the associated product offering can be sold by itself or must be part of a product offering bundle.Possible values:

-   true: Can be sold separately.
-   false: Only sold as part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current lifecycle status. Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the product offering.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td id="prodCat-offering-prodSpecCharValueUse-entry">

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
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

prodSpecCharValueUse.​description

</td><td id="prodCat-offering-prodSpecCharValueUse_description-entry">

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​name

</td><td id="prodCat-offering-prodSpecCharValueUse_name-entry">

Name of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue-entry">

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isDefault

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isMandatory

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_isMandatory-entry">

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor-entry">

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_validFor_startDateTime-entry">

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​value

</td><td id="prodCat-offering-prodSpecCharValueUse_productSpecCharacteristicValue_value-entry">

Value of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​validFor

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor-entry">

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​validFor.​startDateTime

</td><td id="prodCat-offering-prodSpecCharValueUse_validFor_startDateTime-entry">

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​valueType

</td><td id="prodCat-offering-prodSpecCharValueUse_valueType-entry">

Data type of the **prodSpecCharValueUse.productSpecCharacteristicValue.value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productOfferingCharacteristic

</td><td id="prodCat-offering-productOfferingCharacteristic-entry">

Characteristic quality or distinctive feature of a product offering. Characteristics can take on a discrete value that is fixed at design time \(catalog authoring\), such as Mobile Plan Rank. These characteristics are not generally modifiable at inventory level.For additional information on product offering characteristics, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: Array of Objects

```
productOfferingCharacteristic": [  
  {
    "characteristicValueSpecification": [Array],
    "name": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification-entry">

List of characteristic values associated with the product offering characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [  
  { 
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "value": "String"
  }  
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isDefault

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isDefault-entry">

Flag that indicates whether the associated characteristic value is the default value for the associated characteristic.Possible values:

-   true: Is default value.
-   false: Isn't the default value.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isMandatory

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_isMandatory-entry">

Flag that indicates whether the associated characteristic value is mandatory for the associated characteristic.Possible values:

-   true: Is mandatory.
-   false: Isn't mandatory.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​value

</td><td id="prodCat-offering-productOfferingCharacteristic_characteristicValueSpecification_value-entry">

Number or text assigned to the associated product specification characteristic .For example:

```
"characteristicValueSpecification": [
  {
    "value": "choice 1"
  },
  {
    "value": "choice 2"
  }
]
```

Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​name

</td><td id="prodCat-offering-productOfferingCharacteristic_name-entry">

Name of the associated product offering characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​valueType

</td><td id="prodCat-offering-productOfferingCharacteristic_valueType-entry">

Data type of the **productOfferingCharacteristic.​characteristicValueSpecification.​value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

Format: ISO 4217

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

Valid contract term length for the product offering, such as 12 months, 24 months, or not\_applicable.Data type: String

</td></tr><tr><td>

productSpecification

</td><td>

Required. Product specification for the product.Data type: Object

```
"productSpecification": {
  "id": "String",
  "internalId": "String",
  "internalVersion": "String",
  "name"
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.id

</td><td>

Required. Initial version or external ID of the product specification.Data type: String

Table: In the initial\_version or externa\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

productSpecification.​internalId

</td><td>

Sys\_id or internal ID of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​name

</td><td>

Name of the product specification.Data type: String

Table: In the name field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

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

Format: YYYY-MM-DD

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the product offering.Data type: String

Format: YYYY-MM-DD

</td></tr><tr><td>

version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

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
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

bundledGroupProductOffering

</td><td id="d3040e285">

Child groups of product offerings. These show hierarchical sub-grouping.Data type: Array of Objects

```
"bundledGroupProductOffering": [
  {
    "bundledGroupProductOfferingOption": {Object},
    "bundledProductOffering": [Array],
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption

</td><td id="d3040e298">

A range of numbers that specifies the lower and upper limits of the number of the associated product offering that can be procured as part of the related bundled product offering.Data type: Object

```
"bundledGroupProductOfferingOption": {
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="d3040e311">

Lower limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledGroupProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="d3040e322">

Upper limit for a product offering that can be procured as part of the related bundled product offering. Data type: String

</td></tr><tr><td>

bundledGroupProductOffering.​bundledProductOffering

</td><td id="d3040e333">

Child groups of product offerings associated with the bundle. Same format as **bundledProductOffering** specified below.Data type: Array of Objects

</td></tr><tr><td>

bundledGroupProductOffering.​id

</td><td id="d3040e387">

Sys\_id of the bundled group record. Useful in cases where the parent product offering or group includes multiple groups.Data type: String

Table: Product Offering Relationship Group \[sn\_prd\_pm\_product\_offering\_relationship\_group\]

</td></tr><tr><td>

bundledGroupProductOffering.​name

</td><td id="d3040e400">

Name of the group of child product offerings.Data type: String

</td></tr><tr><td>

bundledProductOffering

</td><td id="d3040e411">

List of product offerings included in the product offering bundle. The product offering bundle inherits all of the attributes of the included product offerings.Data type: Array of Objects

```
"bundledProductOffering": [
  {
    "bundledProductOfferingOption": {Object},
    "externalId": "String",
    "href": "String",
    "id": "String",
    "name": "String",
    "version": Number
  }
]
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption

</td><td id="d3040e425">

Product bundle options such as the default number of product offerings and any upper and lower product offering procurement constraints.Data type: Object

```
"bundledProductOfferingOption": {
  "numberRelOfferDefault": "String",
  "numberRelOfferLowerLimit": "String",
  "numberRelOfferUpperLimit": "String"
}
```

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferDefault

</td><td id="d3040e438">

Default number of product offerings that should be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferLowerLimit

</td><td id="d3040e451">

Lower limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​bundledProductOfferingOption.​numberRelOfferUpperLimit

</td><td id="d3040e464">

Upper limit of the number of the associated product offerings that can be procured as part of the related bundled product offering.Data type: String

Possible values: 0 to unbound.

</td></tr><tr><td>

bundledProductOffering.​externalId

</td><td id="d3040e477">

External ID of the product offering   relationship.For additional information on product offering relationships, see [Create product offering relationships](https://www.servicenow.com/docs/access?context=som-product-config-offering-relationships&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

bundledProductOffering.​href

</td><td id="prodCat-offering-bundledProductOffering_href-entry">

Relative link to the associated product offering.Data type: String

</td></tr><tr><td>

bundledProductOffering.​id

</td><td id="d3040e505">

Sys\_id or external ID of the bundled product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\]

</td></tr><tr><td>

bundledProductOffering.​name

</td><td id="d3040e518">

Name of the product offering bundle.Data type: String

</td></tr><tr><td>

bundledProductOffering.​version

</td><td id="d3040e529">

Catalog version of the product offering. Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table. 

</td></tr><tr><td>

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

channel.​description

</td><td>

Description of the channel.Data type: String

</td></tr><tr><td>

channel.id

</td><td>

Sys\_id of the channel.Data type: String

Table: Distribution Channel \[sn\_prd\_pm\_distribution\_channel\]

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

External ID of the product offering. If multiple versions are published, returns the highest published version among them. If no versions are published, returns the highest version regardless of state.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, external\_id field

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product offering, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Required. Initial version or external ID of the product offering.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version or external\_id field

</td></tr><tr><td>

internalId

</td><td>

Sys\_id or internal ID of the product offering record.Data type: String

Table: Product Offering \[sn\_prd\_pm\_product\_offering\] table, initial\_version field

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product offering.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

isBundle

</td><td id="d3040e619">

Flag that indicates whether the product offering is a bundle.Possible values:

-   true: Product offering is a bundle.
-   false: Single product offering.

Data type: Boolean

Default: false

</td></tr><tr><td>

isSellable

</td><td id="d3040e642">

Flag that indicates whether the associated product offering can be sold by itself or must be part of a product offering bundle.Possible values:

-   true: Can be sold separately.
-   false: Only sold as part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Date the product offering was last updated.Data type: String

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the product offering. Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

Default: Blank string

</td></tr><tr><td>

name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse

</td><td id="d3040e692">

Product offering characteristics.Data type: Array of Objects

```
"prodSpecCharValueUse": [
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

prodSpecCharValueUse.​description

</td><td id="d3040e705">

Description of the characteristic.Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​name

</td><td id="d3040e716">

Name of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue

</td><td id="d3040e730">

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isDefault

</td><td id="d3040e746">

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​isMandatory

</td><td id="d3040e767">

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor

</td><td id="d3040e789">

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td id="d3040e802">

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​productSpecCharacteristicValue.​value

</td><td id="d3040e815">

Value of the characteristic.

Data type: String

</td></tr><tr><td>

prodSpecCharValueUse.​validFor

</td><td id="d3040e829">

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

prodSpecCharValueUse.​validFor.​startDateTime

</td><td id="d3040e842">

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

prodSpecCharValueUse.​valueType

</td><td id="d3040e855">

Data type of the **prodSpecCharValueUse.productSpecCharacteristicValue.value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productCharacteristic.​value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic

</td><td id="d3040e918">

Characteristic quality or distinctive feature of a product offering. Characteristics can take on a discrete value that is fixed at design time \(catalog authoring\), such as Mobile Plan Rank. These characteristics are not generally modifiable at inventory level.For additional information on product offering characteristics, see [Create product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=australia&pubname=australia-order-management&ft:locale=en-US).

Data type: Array of Objects

```
productOfferingCharacteristic": [  
  {
    "characteristicValueSpecification": [Array],
    "name": "String",
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification

</td><td id="d3040e936">

List of characteristic values associated with the product offering characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [  
  { 
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "value": "String"
  }  
]
```

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isDefault

</td><td id="d3040e949">

Flag that indicates whether the associated characteristic value is the default value for the associated characteristic.Possible values:

-   true: Is default value.
-   false: Isn't the default value.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​isMandatory

</td><td id="d3040e972">

Flag that indicates whether the associated characteristic value is mandatory for the associated characteristic.Possible values:

-   true: Is mandatory.
-   false: Isn't mandatory.

Data type: Boolean

Default: false

</td></tr><tr><td>

productOfferingCharacteristic.​characteristicValueSpecification.​value

</td><td id="d3040e995">

Number or text assigned to the associated product specification characteristic .For example:

```
"characteristicValueSpecification": [
  {
    "value": "choice 1"
  },
  {
    "value": "choice 2"
  }
]
```

Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​name

</td><td id="d3040e1010">

Name of the associated product offering characteristic.Data type: String

</td></tr><tr><td>

productOfferingCharacteristic.​valueType

</td><td id="d3040e1022">

Data type of the **productOfferingCharacteristic.​characteristicValueSpecification.​value** parameter.Possible values:

-   Array.Date
-   Array.Datetime
-   Array.Decimal
-   Array.Integer
-   Array.Object
-   Array.Single Line Test
-   Checkbox
-   Choice
-   Date,Address
-   Email
-   Integer,Date/Time
-   Object
-   Single Line Text
-   Yes/No

Data type: String

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

productOfferingPrice.​price

</td><td>

Price information for the product offering.Data type: Object

```
"price": {
  "taxIncludedAmount": {Object}
}
```

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount

</td><td>

Price information for the product offering.Data type: Object

```
"taxIncludedAmount": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount.unit

</td><td>

Currency code for the product offering price.Data type: String

</td></tr><tr><td>

productOfferingPrice.​price.​taxIncludedAmount.​value

</td><td>

Price of the product offering including tax.Data type: String

</td></tr><tr><td>

productOfferingPrice.​priceType

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
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

productSpecification.​id

</td><td>

Sys\_id of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalId

</td><td>

Sys\_id or internal ID of the product specification record.Data type: String

Table: In the initial\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

productSpecification.​version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr><tr><td>

status

</td><td id="prodCat-offering-status-entry">

Status of the product offering.Possible values:

-   draft
-   published

Data type: String

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

validFor.​endDateTime

</td><td>

End date of the product offering.Data type: String

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date of the product offering.Data type: String

</td></tr><tr><td>

version

</td><td>

External version of the product offering.Data type: String

Table: In the external\_version field of the Product Offering \[sn\_prd\_pm\_product\_offering\] table.

</td></tr></tbody>
</table>This example creates a product offering.

```
curl --location --request POST "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productOffering" \
--header "Content-Type: application/json" \
--header "Accept:application/json" \
--data-raw '{
  "id": "313b917843235210a82ed6085bb8f2c7",,
  "externalSystem": "Salesforce-TMF620",
  "name": "Internet bundle",
  "displayName": "Internet bundle",
  "description": "Internet bundle",
  "isSellable": false,
  "lifecycleStatus": "Draft",
  "isBundle": true,
  "lastUpdate": "2025-02-05 06:39:45",
  "version": "",
  "internalVersion": "1",
  "internalId": "313b917843235210a82ed6085bb8f2c7",
  "validFor": {
    "startDateTime": "2028-12-15",
    "endDateTime": "2034-01-14"
  },
  "productOfferingTerm": "not_applicable",
  "productOfferingPrice": [
    {
      "priceType": "recurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    },
    {
      "priceType": "nonRecurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    }
  ],
  "productOfferingCharacteristic": [
    {
      "name": "Firewall Security",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "Premium",
          "isMandatory": false,
          "isDefault": true
        }
      ]
    },
    {
      "name": "Connectivity need",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "When in use",
          "isMandatory": false,
          "isDefault": false
        }
      ]
    }
  ],
  "bundledProductOffering": [
    {
      

      "id": "0f61dd9fd0a63110f8770dbf976be168",
      "name": "Solana Sports streaming channel",
      "version": "1",
      "externalId": "EXT-123",
      "bundledProductOfferingOption": {
        "numberRelOfferDefault": "1",
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "bundledGroupProductOffering": [
    {
      "id": "063b957843235210a82ed6085bb8f205",
      "name": "Streaming Channel",
      "bundledProductOffering": [
        { 
        

          "id": "62619d9fd0a63110f8770dbf976be180",
          "name": "Solana Movie streaming channel",
          "version": "1",
          "externalId": "EXT-345",
          "bundledProductOfferingOption": {
            "numberRelOfferDefault": "1",
            "numberRelOfferLowerLimit": "1",
            "numberRelOfferUpperLimit": "1"
          }
        }
      ],
      "bundledGroupProductOfferingOption": {
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "productSpecification": {
    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
    "name": "SD-WAN Service Package",
    "version": "",
    "internalVersion": "3",
    "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
  },
  "prodSpecCharValueUse": [
    {
      "name": "Tenancy",
      "description": "Tenancy",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2024-12-18 21:04:24"
      },
      "productSpecCharacteristicValue": [
        {
          "value": "Premium (>50 sites)",
          "isDefault": false,
          "isMandatory": false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Base (10 site)",
          "isDefault": false,
          "isMandatory": false,
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
      "id": "58ad5522c3702010df4773ce3640ddb2",
      "name": "Agent Assist"
    }
  ],
  "category": [
    {
      "id": "13e305a143b631105029d1529ab8f267",
      "name": "SD-WAN_all_offers"
    }
  ],
  "status": "draft"
}'
--user 'username':'password'
```

Response body:

```
{
  "id": "313b917843235210a82ed6085bb8f2c7",
  "name": "Internet bundle",
  "externalSystem": "Salesforce-TMF620",
  "displayName": "Internet bundle",
  "description": "Internet bundle",
  "isSellable": false,
  "lifecycleStatus": "Draft",
  "isBundle": true,
  "lastUpdate": "2025-04-09 15:59:09",
  "version": "",
  "internalVersion": "1",
  "validFor": {
    "startDateTime": "2028-12-15",
    "endDateTime": "2034-01-14"
  },
  "productOfferingTerm": "not_applicable",
  "productOfferingPrice": [
    {
      "priceType": "recurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    },
    {
      "priceType": "nonRecurring",
      "price": {
        "taxIncludedAmount": {
          "unit": "USD",
          "value": "0"
        }
      }
    }
  ],
  "productOfferingCharacteristic": [
    {
      "name": "Firewall Security",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "Premium",
          "isMandatory": false,
          "isDefault": true
        }
      ]
    },
    {
      "name": "Connectivity need",
      "valueType": "choice",
      "characteristicValueSpecification": [
        {
          "value": "When in use",
          "isMandatory": false,
          "isDefault": false
        }
      ]
    }
  ],
  "bundledProductOffering": [
    {
      "id": "0f61dd9fd0a63110f8770dbf976be168",
      "name": "Solana Sports streaming channel",
      "version": "1",
      "externalId": "EXT-123",
      "bundledProductOfferingOption": {
        "numberRelOfferDefault": "1",
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "bundledGroupProductOffering": [
    {
      "id": "063b957843235210a82ed6085bb8f205",
      "name": "Streaming Channel",
      "bundledProductOffering": [
        {
          "id": "62619d9fd0a63110f8770dbf976be180",
          "name": "Solana Movie streaming channel",
          "version": "1",
          "externalId": "EXT-345",
          "bundledProductOfferingOption": {
            "numberRelOfferDefault": "1",
            "numberRelOfferLowerLimit": "1",
            "numberRelOfferUpperLimit": "1"
          }
        }
      ],
      "bundledGroupProductOfferingOption": {
        "numberRelOfferLowerLimit": "1",
        "numberRelOfferUpperLimit": "1"
      }
    }
  ],
  "productSpecification": {
    "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
    "name": "SD-WAN Service Package",
    "version": "",
    "internalVersion": "3",
    "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6"
  },
  "prodSpecCharValueUse": [
    {
      "name": "Tenancy",
      "description": "Tenancy",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2024-12-18 21:04:24"
      },
      "productSpecCharacteristicValue": [
        {
          "value": "Premium (>50 sites)",
          "isDefault": false,
          "isMandatory": false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Base (10 site)",
          "isDefault": false,
          "isMandatory": false,
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
      "id": "58ad5522c3702010df4773ce3640ddb2",
      "name": "Agent Assist"
    }
  ],
  "category": [
    {
      "id": "13e305a143b631105029d1529ab8f267",
      "name": "SD-WAN_all_offers"
    }
  ],
  "status": "draft",
  "externalId": "313b917843235210a82ed6085bb8f2c7",
  "internalId": "03c99cb53bf066509b48d69a04e45a11",
  "href": "/api/sn_tmf_api/catalogmanagement/productOffering/03c99cb53bf066509b48d69a04e45a11"
}
```

## Product Catalog Open API - POST /sn\_tmf\_api/catalogmanagement/productOfferingPrice

Creates a new price list line record in the Price List Line \[sn\_csm\_pricing\_price\_list\_line\] table.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/productOfferingPrice`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="id_b21_1nc_f2c" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Required. Type of price list line. Always a value of `ProductOfferingPrice`.Data type: String

</td></tr><tr><td>

externalId

</td><td>

The external ID of the price list line.Data type: String

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether the price list line is part of a single product or a bundle of products.Valid values:

-   true: Price list line is part of a bundle.
-   false: Price list line isn't part of a bundle.

Data type: Boolean

Default: false

</td></tr><tr><td>

lastUpdate

</td><td>

Required. Date that the price line was last updated.Format: YYYY-MM-DD

Data type: String

</td></tr><tr><td>

lifeCycleStatus

</td><td>

Required. Current life cycle status of the product list line.Valid values:

-   active
-   draft
-   inactive

Data type: String

Default: draft

</td></tr><tr><td>

name

</td><td>

Required. Name to give the price list line.Data type: String

</td></tr><tr><td>

price

</td><td>

Required. List price details of the price list line.Data type: Object

```
"price": {
  "unit": "String",
  "value": "String"
}
```

</td></tr><tr><td>

price.unit

</td><td>

Required. Currency code of the price list line. For example, `USD` or `EUR`.Table: Currency \[fx\_currency\] table.

Data type: String

</td></tr><tr><td>

price.value

</td><td>

Required. Value of the price.Data type: String \(represented with a number. For example, `"800"`.\)

</td></tr><tr><td>

priceList

</td><td>

Required. Price list information associated with the price list line.Data type: Object

```
"priceList": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

priceList.id

</td><td>

Required. Sys\_id of the price list line.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

priceList.name

</td><td>

Name of the price list line.Data type: String

</td></tr><tr><td>

priceList.@type

</td><td>

The type of price list line. When sub-classing, this defines the sub-class extensible name. Value is always `priceList`.Data type: String

</td></tr><tr><td>

priceType

</td><td>

Required. Filter the price list line by the pricing method of the product offering.Valid values:

-   recurring: Charge recurring pricing amounts with a specified frequency. Frequency is set in the **recurringChargePeriodType** parameter.
-   one\_time: Supports one-time or recurring add-on charges and fees for a product offering.

Data type: String

Default: recurring

</td></tr><tr><td>

productOffering

</td><td>

Required. Product offering of the price list line.Data type: Object

```
"productOffering": {
  "id": "String",
  "name": "String",
  "internalVersion": "String"
}
```

</td></tr><tr><td>

productOffering.​id

</td><td>

Required. Sys\_id of the product offering.Table: Product offering \[sn\_prd\_pm\_product\_offering\]

Data type: String

</td></tr><tr><td>

productOffering.​internalVersion

</td><td>

Internal version number of the product offering.Data type: String \(represented with a number. For example, `"1"`.\)

</td></tr><tr><td>

productOffering.​name

</td><td>

Name of the product offering.Data type: String

</td></tr><tr><td>

recurringChargePeriodType

</td><td>

Required if **priceType** is recurring. Commitment terms that are selected when the product offering was created.Valid values:

-   annually
-   monthly

Data type: String

</td></tr><tr><td>

unitOfMeasure

</td><td>

Required. Details about the unit of measure associated with the price list line.Data type: Object

```
"unitOfMeasure": {
  "id": "String",
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

unitOfMeasure.​amount

</td><td>

Amount of the unit of measure.Data type: Number

</td></tr><tr><td>

unitOfMeasure.​id

</td><td>

Required. Sys\_id of the unit of measure in the Price Line List table.Table: Price List Line \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

unitOfMeasure.​units

</td><td>

Type of the unit of measure associated with the price list line. For example, `each` or `bundle`.Data type: String

</td></tr><tr><td>

validFor

</td><td>

Required. The duration of time that the price list line is valid for.Data type: Object

```
"validFor": {
  "endDate": "String",
  "startDate": "String"
}
```

</td></tr><tr><td>

validFor.endDate

</td><td>

End date that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time that the price list line is valid for.Format: YYYY-MM-DD HH:mm:ss

Data type: String \(glide\_date\)

</td></tr><tr><td>

validFor.startDate

</td><td>

Start date that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time that the price list line is valid for.Format: YYYY-MM-DD HH:mm:ss

Data type: String \(glide\_date\)

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

<table id="table_onp_pnw_22c"><thead><tr><th>

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
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the price list line. Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

href

</td><td>

URL to the price list line record in the instance.Data type: String

</td></tr><tr><td>

lastUpdate

</td><td>

Date and time that the price list line was last updated.Format: YYYY-MM-DD HH:mm:ss

Data type: String

</td></tr><tr><td>

validFor

</td><td>

The duration of time that the price list line is valid for.Data type: Object

```
"validFor": {
  "endDate": "String",
  "startDate": "String"
}
```

</td></tr><tr><td>

validFor.endDate

</td><td>

End date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

validFor.startDate

</td><td>

Start date and time that the price list line is valid for.Data type: String \(glide\_date\_time\)

</td></tr><tr><td>

isBundle

</td><td>

Flag that indicates whether the price list line is part of a single product or a bundle of products.Valid values:

-   true: Price list line is part of a bundle.
-   false: Price list line isn't part of a bundle.

Data type: Boolean

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current life cycle status of the price list line.Valid values:

-   Active
-   Draft
-   Inactive

Data type: String

</td></tr><tr><td>

productOffering

</td><td>

Product offering that is associated with the price list line.Data type: Object

```
"productOffering": {
  "id": "String",
  "name": "String",
  "internalVersion": "String"
}
```

</td></tr><tr><td>

productOffering.id

</td><td>

Sys\_id of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.​internalVersion

</td><td>

Internal version number of the product offering. For example, `PRDOF01024`. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

productOffering.​name

</td><td>

Name of the product offering. Located in the Product Offering \[sn\_prd\_pm\_product\_offering\] table.Data type: String

</td></tr><tr><td>

priceType

</td><td>

The pricing method of the product offering which is associated with this price list line.Possible values:

-   recurring: Charge recurring pricing amounts with a specified frequency. The value of **recurringChargePeriodType** indicates the frequency of the charge.
-   one\_time: One-time or recurring add-on charges and fees for a product offering.

Data type: String

</td></tr><tr><td>

recurringChargePeriodType

</td><td>

The periodicity or frequency of the product offering associated with this price list line. Returns a frequency type if **priceType** was set to `recurring`, otherwise returns an empty string.Possible values:

-   annually
-   monthly

Data type: String

</td></tr><tr><td>

unitOfMeasure

</td><td>

Details about the unit of measure associated with the price list line.Data type: Object

```
"unitOfMeasure": {
  "id": "String",
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

unitOfMeasure.amount

</td><td>

Amount of the unit of measure.Data type: Number

</td></tr><tr><td>

unitOfMeasure.id

</td><td>

Sys\_id of the unit of measure.Table: Price List Lines \[sn\_csm\_pricing\_price\_list\_line\]

Data type: String

</td></tr><tr><td>

unitOfMeasure.​units

</td><td>

Type of the unit of measure associated with the price list line. For example, `year` or `bundle`.Data type: String

</td></tr><tr><td>

price

</td><td>

List price details of the price list line.Data type: Object

```
"price": {
  "units": "String",
  "value": "String"
}
```

</td></tr><tr><td>

price.units

</td><td>

Currency code of the price. For example, `USD` or `EUR`. Table: Currency \[fx\_currency\]

Data type: String

</td></tr><tr><td>

price.value

</td><td>

Value of the price.Data type: String \(represented with a number\)

</td></tr><tr><td>

priceList

</td><td>

Price list information associated with the price list line.Data type: Object

```
"priceList": {
  "id": "String",
  "name": "String",
  "@type": "String"
}
```

</td></tr><tr><td>

priceList.id

</td><td>

Sys\_id of the price list in the Price List \[sn\_csm\_pricing\_price\_list\] table.Data type: String

</td></tr><tr><td>

priceList.name

</td><td>

Name of the price list.Data type: String

</td></tr><tr><td>

priceList.@type

</td><td>

The type of price list. When sub-classing, this defines the sub-class extensible name. Always has a value of `priceList`.Data type: String

</td></tr><tr><td>

@type

</td><td>

Always a value of `ProductOfferingPrice`. When sub-classing, this defines the sub-class extensible name.Data type: String

</td></tr><tr><td>

state

</td><td>

The state of the price list which is associated with this price list line.Data type: String

</td></tr><tr><td>

externalId

</td><td>

The external ID of this price list line.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example creates a new price list line record according to data specified in the request body, and inserts it in the Price list line \[sn\_csm\_pricing\_price\_list\_line\] table.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/catalogmanagement/productOfferingPrice " \
--request POST\
--user 'username':'password'
--data {
  "name": "new Price list",
  "validFor": {
    "startDateTime": "2024-05-28 15:15:58",
    "endDateTime": "2025-06-28 15:15:58"
  },
  "priceType": "recurring",
  "recurringChargePeriodType": "monthly",
  "lastUpdate": "2023-09-23 00:00:00",
  "isBundle": false,
  "lifecycleStatus": "Draft",
  "unitOfMeasure": {
    "id": "1eaa559953020110286eddeeff7b12c7",
    "amount": 1,
    "units": "Year"
  },
  "price": {
    "unit": "USD",
    "value": "800"
  },
  "productOffering": {
    "id": "9e3dd57a4fcb5210f899f61d20ce0bf2",
    "name": "Maintenance Fee",
    "internalVersion": "1"
  },
  "priceList": {
    "name": "new price list",
    "@type": "priceList"
  },
  "externalId": "test123",
  "@type": "ProductOfferingPrice"
}
```

Response body. This new price list line record is assigned a unique ID; the response body returns this information along with a URL to the new record using the **href** response parameter.

```
{
  "name": "new Price list",
  "validFor": {
    "startDateTime": "2024-05-28 15:15:58",
    "endDateTime": "2025-06-28 15:15:58"
  },
  "priceType": "recurring",
  "recurringChargePeriodType": "monthly",
  "lastUpdate": "2023-09-23 00:00:00",
  "isBundle": false,
  "lifecycleStatus": "Draft",
  "unitOfMeasure": {
    "id": "1eaa559953020110286eddeeff7b12c7",
    "amount": 1,
    "units": "Year"
  },
  "price": {
    "unit": "USD",
    "value": "800"
  },
  "productOffering": {
    "id": "9e3dd57a4fcb5210f899f61d20ce0bf2",
    "name": "Maintenance Fee",
    "internalVersion": "1"
  },
  "priceList": {
    "id": "194d5d364f8b5210f899f61d20ce0b7a",
    "name": "new Price list",
    "@type": "priceList"
  },
  "externalId": "test123",
  "@type": "ProductOfferingPrice",
  "id": "994d5d364f8b5210f899f61d20ce0b7c",
  "state": "draft",
  "href": "/api/sn_tmf_api/catalogmanagement/productOfferingPrice/994d5d364f8b5210f899f61d20ce0b7c"
}
```

## Product Catalog Open API - POST /sn\_tmf\_api/catalogmanagement/productSpecification

Creates a product specification record with the specified values.

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

externalSystem

</td><td>

External system of the product specification, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

id

</td><td>

Required. Sys\_id or external ID of the product specification.Data type: String

Table: In the initial\_version or external\_id of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Required. Sys\_id or internal ID of the product specification.

Data type: String

Table: In the initial\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

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

productSpecCharacteristic.​description

</td><td>

Description of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecCharacteristic.​name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue

</td><td>

Required. List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isDefault

</td><td>

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isMandatory

</td><td>

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor

</td><td>

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td>

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​value

</td><td>

Required. Value of the characteristic.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​endDateTime

</td><td>

End date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Default: Blank string

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​startDateTime

</td><td>

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Default: Blank string

</td></tr><tr><td>

productSpecCharacteristic.​valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be of complex or non-complex type.Data type: String

Accepted values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Test
-   Array.Object
-   Array.Date
-   Array.Decimal
-   Yes/No
-   Object
-   Array.Datetime
-   Checkbox
-   Email
-   Choice

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

productSpecificationRelationship.​id

</td><td>

ID of the related specification.Data type: String

Default: Blank string

</td></tr><tr><td>

productSpecificationRelationship.​type

</td><td>

Required if using the **productSpecificationRelationship** parameter. Type of relationship.Valid values:

-   bundles
-   composed\_of

Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​endDateTime

</td><td>

End date of the relationship.Data type: String

Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Default: Blank string

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​startDateTime

</td><td>

Start date of the relationship.Data type: String

Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Default: Blank string

</td></tr><tr><td>

resourceSpecification

</td><td>

Required. Resource specifications related to this product specification.Data type: Array of Objects

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

resourceSpecification.​id

</td><td>

Required. Initial version or external ID of the resource specification.Data type: String

Table: In the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalId

</td><td>

Initial version \(sys\_id\) of the resource specification record.Data type: String

Table: In the initial\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalVersion

</td><td>

Version of the resource specification.Data type: String

Table: In the version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​name

</td><td>

Name of the resource specification.Data type: String

Table: Resource Specification \[sn\_prd\_pm\_resource\_specification\]

</td></tr><tr><td>

resourceSpecification.​version

</td><td>

External version of the resource specification.Data type: String

Table: In the external\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

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

serviceSpecification.​id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​name

</td><td>

Name of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceSpecification.​version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

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

validFor.​endDateTime

</td><td>

End date of the specification.Data type: String

Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Default: Blank string

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date of the specification.Data type: String

Format: YYYY-MM-DD HH:mm:SS. For example, `2025-01-31 09:35:43`.

Default: Blank string

</td></tr><tr><td>

version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the response body. Only supports **application/json**.|

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
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalSystem

</td><td>

External system of the product specification, appended with `TMF620`. For example, if the external system is ABC then the value is `ABC-TMF620`.

Data Type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the resource record.Data type: String

Default: Blank string

</td></tr><tr><td>

id

</td><td>

Sys\_id or external ID of the product specification.Data type: String

Table: In the sys\_id or external\_id field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Required. Sys\_id or internal ID of the product specification.

Data type: String

Table: In the initial\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the product specification.Data type: String

Table: In the version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

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

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

lifecycleStatus

</td><td>

Current lifecycle status of the product specification. Possible values:

-   Active
-   Draft
-   Inactive

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

productSpecCharacteristic.​description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue

</td><td>

List of the possible values of the characteristic.

Data type: Array of Objects

```
"productSpecCharacteristicValue": [
 {
    "isDefault": Boolean,
    "isMandatory": Boolean,
    "validFor": {Object},
    "value": "String"
 }
]
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isDefault

</td><td>

Flag that indicates whether the associated characteristic value is the default value for the characteristic.Possible values:

-   true: Default value.
-   false: Not the default value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​isMandatory

</td><td>

Flag that indicates whether the associated characteristic value is a mandatory value for the characteristic.Possible values:

-   true: Mandatory value.
-   false: Not a mandatory value.

Default: false

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor

</td><td>

Date and time of when the characteristic is valid.Data type: Object

```
"validFor": {
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​validFor.​startDateTime

</td><td>

Start date and time of when the characteristic value is valid.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​productSpecCharacteristicValue.​value

</td><td>

Value of the characteristic.

Data type: String

</td></tr><tr><td>

productSpecCharacteristic.​validFor

</td><td>

Date range for which the characteristic is valid.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​endDateTime

</td><td>

End date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​validFor.​startDateTime

</td><td>

Start date of the characteristic.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecCharacteristic.​valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be of complex or non-complex type.Data type: String

Accepted values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Test
-   Array.Object
-   Array.Date
-   Array.Decimal
-   Yes/No
-   Object
-   Array.Datetime
-   Checkbox
-   Email
-   Choice

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

productSpecificationRelationship.​id

</td><td>

Sys\_id of the related specification.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​type

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

productSpecificationRelationship.​validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​endDateTime

</td><td>

End date of the relationship.Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

productSpecificationRelationship.​validFor.​startDateTime

</td><td>

Start date of the relationship.Data type: String

Format: YYYY-MM-DD HH:mm:SS

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

resourceSpecification.​id

</td><td>

Sys\_id or external ID of the resource specification.Data type: String

Table: In the sys\_id or external\_id field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalId

</td><td>

Initial version \(sys\_id\) of the resource specification record.Data type: String

Table: In the initial\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​internalVersion

</td><td>

Version of the resource specification.Data type: String

Table: In the version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

</td></tr><tr><td>

resourceSpecification.​name

</td><td>

Name of the resource specification.Data type: String

Table: Resource Specification \[sn\_prd\_pm\_resource\_specification\]

</td></tr><tr><td>

resourceSpecification.​version

</td><td>

External version of the resource specification.Data type: String

Table: In the external\_version field of the Resource Specification \[sn\_prd\_pm\_resource\_specification\] table.

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

serviceSpecification.​id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

serviceSpecification.​name

</td><td>

Name of the service specification.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

serviceSpecification.​version

</td><td>

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

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

validFor.​endDateTime

</td><td>

End date of the specification. Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

validFor.​startDateTime

</td><td>

Start date of the specification. Data type: String

Format: YYYY-MM-DD HH:mm:SS

</td></tr><tr><td>

version

</td><td>

External version of the product specification.Data type: String

Table: In the external\_version field of the Product Specification \[sn\_prd\_pm\_product\_specification\] table.

</td></tr></tbody>
</table>This example creates a product specification record with the specified values.

```
curl --location --request POST "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/productSpecification" \
--header "Content-Type: application/json" \
--data-raw '{
  "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/cfe5ef6a53702010cd6dddeeff7b12f6",
  "externalSystem": "Salesforce-TMF620",
  "name": "SD-WAN Service Package",
  "displayName": "SD-WAN Service Package v3",
  "version": "",
  "internalVersion": "3",
  "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "description": "SD WAN Service Package",
  "lastUpdate": "2027-10-11 06:58:12",
  "isBundle": true,
  "validFor": {
    "startDateTime": "2029-02-05",
    "endDateTime": ""
  },
  "serviceSpecification": [],
  "productSpecificationRelationship": [
    {
      "id": "216663aa53702010cd6dddeeff7b12b5",
      "name": "SD-WAN Controller",
      "version": "",
      "internalVersion": "1",
      "internalId": "216663aa53702010cd6dddeeff7b12b5",
      "type": "Service",
      "validFor": {
        "startDateTime": "2025-01-24",
        "endDateTime": ""
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "1",
        "numberSpecRelUpperLimit": "1"
      }
    },
    {
      "id": "39b627aa53702010cd6dddeeff7b1202",
      "name": "SD-WAN Edge Device",
      "version": "",
      "internalVersion": "2",
      "internalId": "39b627aa53702010cd6dddeeff7b1202",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-05",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "2",
        "numberSpecRelUpperLimit": "4"
      }
    },
    {
      "id": "a6514bd3534560102f18ddeeff7b1247",
      "name": "SD-WAN Security",
      "version": "",
      "internalVersion": "2",
      "internalId": "a6514bd3534560102f18ddeeff7b1247",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-03",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "4",
        "numberSpecRelUpperLimit": "20"
      }
    }
  ],
  "resourceSpecification": [],
  "productSpecCharacteristic": [
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.25",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.01",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.5",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Down Time",
      "description": "Down Time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:36:15"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "500 Mbps",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "5 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Bandwidth",
      "description": "Bandwidth",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:32:11"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "4 hrs",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 hr",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Time to Restore (TTR)",
      "description": "Time to Restore (TTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:37:25"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1 hr",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "4 hrs",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Mean Time to Restore (MTR)",
      "description": "Mean Time to Restore (MTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:39:05"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Flow Backup",
      "description": "Application Flow Backup",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:30:39"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "99.00",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.50",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.75",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.99",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Up Time",
      "description": "Up time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:34:30"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Encryption",
      "description": "Application Encryption",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:29:08"
      }
    }
  ],
  "status": "published"
}'

--user 'username':'password'

```

Response body.

```
{
  "id": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "href": "/api/sn_tmf_api/catalogmanagement/productSpecification/cfe5ef6a53702010cd6dddeeff7b12f6",
  "externalSystem": "Salesforce-TMF620",
  "name": "SD-WAN Service Package",
  "displayName": "SD-WAN Service Package v3",
  "version": "",
  "internalVersion": "3",
  "internalId": "cfe5ef6a53702010cd6dddeeff7b12f6",
  "description": "SD WAN Service Package",
  "lastUpdate": "2027-10-11 06:58:12",
  "isBundle": true,
  "validFor": {
    "startDateTime": "2029-02-05",
    "endDateTime": ""
  },
  "serviceSpecification": [],
  "productSpecificationRelationship": [
    {
      "id": "216663aa53702010cd6dddeeff7b12b5",
      "name": "SD-WAN Controller",
      "version": "",
      "internalVersion": "1",
      "internalId": "216663aa53702010cd6dddeeff7b12b5",
      "type": "Service",
      "validFor": {
        "startDateTime": "2025-01-24",
        "endDateTime": ""
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "1",
        "numberSpecRelUpperLimit": "1"
      }
    },
    {
      "id": "39b627aa53702010cd6dddeeff7b1202",
      "name": "SD-WAN Edge Device",
      "version": "",
      "internalVersion": "2",
      "internalId": "39b627aa53702010cd6dddeeff7b1202",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-05",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "2",
        "numberSpecRelUpperLimit": "4"
      }
    },
    {
      "id": "a6514bd3534560102f18ddeeff7b1247",
      "name": "SD-WAN Security",
      "version": "",
      "internalVersion": "2",
      "internalId": "a6514bd3534560102f18ddeeff7b1247",
      "type": "Service",
      "validFor": {
        "startDateTime": "2026-06-03",
        "endDateTime": "2031-07-05"
      },
      "relationshipType": "bundles",
      "ProdSpecRelationshipOption": {
        "numberSpecRelLowerLimit": "1",
        "numberSpecRelDefault": "4",
        "numberSpecRelUpperLimit": "20"
      }
    }
  ],
  "resourceSpecification": [],
  "productSpecCharacteristic": [
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.25",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.01",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "0.5",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Down Time",
      "description": "Down Time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:36:15"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "500 Mbps",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "5 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 Gbps",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Bandwidth",
      "description": "Bandwidth",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:32:11"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "4 hrs",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "1 hr",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Time to Restore (TTR)",
      "description": "Time to Restore (TTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:37:25"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "1 hr",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "2 hrs",
          "isMandatory":true,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "4 hrs",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Mean Time to Restore (MTR)",
      "description": "Mean Time to Restore (MTR)",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:39:05"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Flow Backup",
      "description": "Application Flow Backup",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:30:39"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "99.00",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.50",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.75",
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "99.99",
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Up Time",
      "description": "Up time",
      "valueType": "choice",
      "validFor": {
        "startDatetime": "2027-10-11 02:34:30"
      }
    },
    {
      "productSpecCharacteristicValue": [
        {
          "value": "No",
          "isMandatory":true,
          "isDefault":true,
          "validFor": {
            "startDateTime": ""
          }
        },
        {
          "value": "Yes",
          "isMandatory":false,
          "isDefault":false,
          "validFor": {
            "startDateTime": ""
          }
        }
      ],
      "name": "Application Encryption",
      "description": "Application Encryption",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2027-10-11 02:29:08"
      }
    }
  ],
  "status": "published"
}'
```

