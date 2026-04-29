---
title: Service Catalog Open API
description: The Service Catalog Open API provides endpoints to create and retrieve service specifications.Deletes the specified service category record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.Retrieves a list of all service category records in the Service Category \[sn\_prd\_pm\_specification\_category\] table.Retrieves a specific service category record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.Retrieves a list of all service specifications.Retrieves a service specification.Updates a specified record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.Creates a new service category record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.Creates a service specification.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 40
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Service Catalog Open API

The Service Catalog Open API provides endpoints to create and retrieve service specifications.

Use this API to manage service catalog information between external systems and the ServiceNow AI Platform. The Service Catalog Open API is a ServiceNow® implementation of the TM Forum Service Catalog API REST specification. This implementation is based on the [TMF633 Service Catalog API REST Specification Version 4](https://www.tmforum.org/resources/standard/tmf633-service-catalog-api-user-guide-v4-0-0/), October 2020.

This API is included in the Product Catalog Advanced application, which is available on the ServiceNow Store.

This API's endpoints are provided within the `sn_tmf-api` namespace under the Product Catalog Open API name:

-   Create Service Category \(POST\) - [Service Catalog Open - POST /api/sn\_tmf\_api/catalogmanagement/serviceCategory](service-catalog-open-api.md#)
-   Create Service Specification \(POST\) - [Service Catalog Open - POST /servicespecification](service-catalog-open-api.md#)
-   Delete Service Category \(DELETE\) - [Service Catalog Open - DELETE /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}](service-catalog-open-api.md#)
-   Get Service Category \(GET\) - [Service Catalog Open - GET /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}](service-catalog-open-api.md#)
-   Get Service Specification \(GET\) - [Service Catalog Open - GET /servicespecification/\{specificationId\}](service-catalog-open-api.md#)
-   List Service Specifications \(GET\) - [Service Catalog Open - GET /servicespecification](service-catalog-open-api.md#)
-   Update Service Category \(PATCH\) - [Service Catalog Open - POST /api/sn\_tmf\_api/catalogmanagement/serviceCategory](service-catalog-open-api.md#)

The calling user must have the sn\_prd\_pm\_adv.catalog\_integrator role.

This API creates and updates data in the following tables.

-   Characteristic \[sn\_prd\_pm\_characteristic\]
-   Characteristic Option \[sn\_prd\_pm\_characteristic\_option\]
-   Service Specification \[sn\_prd\_pm\_service\_specification\]
-   Specification Relationship \[sn\_prd\_pm\_specification\_relationship\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Service Catalog Open - DELETE /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}

Deletes the specified service category record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/serviceCategory/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the service category to delete. Table: Service category \[sn\_prd\_pm\_specification\_category\]

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

|Header|Description|
|------|-----------|
|Accept|Data format of the request body. Only supports application/json.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|204|No content.|
|400|Bad request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

The following example deletes a service category with ID, a1b23456c7de8a90f0123456gh789ij. Returns a status code with messaging.

```
curl "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/serviceCategory/a1b23456c7de8a90f0123456gh789ij" \
  --request DELETE \
  --header "Accept:application/json" \
  --user 'user:password'
```

## Service Catalog Open - GET /api/sn\_tmf\_api/catalogmanagement/serviceCategory

Retrieves a list of all service category records in the Service Category \[sn\_prd\_pm\_specification\_category\] table.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/serviceCategory`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Valid fields:

-   href
-   id
-   name

Data type: String

Default: Returns all fields

</td></tr><tr><td>

id

</td><td>

Filter service categories by specific sys\_id\(s\). Table: Service Category \[service\_category\]

Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Data type: Number

Default: 20

Maximum: 100

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. Use this value to paginate record retrieval. Don't use a negative number value.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept:application/json| |

<table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the Content-Range header is items `3-5`.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the response body. Only supports application/json.

</td></tr><tr><td>

Link

</td><td>

Contains the following links to navigate through query results:

-   first
-   last
-   next
-   previous

</td></tr><tr><td>

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

206

</td><td>

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td>

Bad request.Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

externalIdentifier

</td><td>

Identifying information for an external system involved in managing categories.Data type: Array of Objects

```
"externalIdentifier": [
 {
  "id": "String",
  "owner": "String"
 }
]
```

</td></tr><tr><td>

externalIdentifier.id

</td><td>

Unique identifier for the service category. This value is determined by an external system. Data type: String

Table: Service Category \[sn\_prd\_pm\_specification\_category\], field external\_id

</td></tr><tr><td>

externalIdentifier.owner

</td><td>

The system that owns the given external ID. Data type: String

</td></tr><tr><td>

href

</td><td>

Hyperlink to access the service category.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service category. Table: Service Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr><tr><td>

isRoot

</td><td>

Flag that indicates whether the category is a root of categories.Valid values:

-   true: Category is a root of categories.
-   false: Category isn't a root of categories.

Data type: Boolean

</td></tr><tr><td>

modelCategory

</td><td>

List of model categories associated with the service category.Data type: Array of Objects

```
"modelCategory": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

modelCategory.id

</td><td>

Sys\_id of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

modelCategory.name

</td><td>

Name of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the service category.Data type: String

</td></tr><tr><td>

serviceCandidate

</td><td>

List of service candidates references associated with this category.Data type: Array of Objects

```
"serviceCandidate": [
 {
  "id": "String",
  "href": "String",
  "name": "String",
  "@referredType": "String",
  "version": "String" 
 }
]
```

</td></tr><tr><td>

serviceCandidate.@referredType

</td><td>

Value is always `ServiceCategory`.Data type: String

</td></tr><tr><td>

serviceCandidate.href

</td><td>

Hyperlink to access the service specification.Data type: String

</td></tr><tr><td>

serviceCandidate.id

</td><td>

Sys\_id of the service specification.Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

Data type: String

</td></tr><tr><td>

serviceCandidate.version

</td><td>

Version of the service candidate.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example calls the GET operation to return a list of all service category records in theService Category \[sn\_prd\_pm\_specification\_category\] table.

```
curl "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/serviceCategory" \
  --request GET \
  --header "Accept:application/json" \
  --user 'user:password'
``
```

Response body.

```
{
  "id": "a1b23456c7de8a90f0123456gh789ij",
  "href": "api/sn_tmf_api/service_catalog_api/serviceCategory/a2a68216d9ce2a90f87718429ae503dd",
  "name": "Cloud Services",
  "serviceCandidate": [
    {
      "id": "14fbd5ead902ea90f87718429ae503f7",
      "href": "api/sn_tmf_api/catalogmanagement/serviceSpecification/14fbd5ead902ea90f87718429ae503f7",
      "version": "1",
      "name": "servicenow",
      "@referredType": "ServiceCategory"
    }
  ],
  "modelCategory": [
    {
      "id": "a1d5bc14c3031000b959fd251eba8f5f",
      "name": "Business Service"
    }
  ],
  "externalIdentifier": [
    {
      "id": "1234234312",
      "owner": "TMF200000123233"
    }
  ],
  "isRoot": "true"
}
```

## Service Catalog Open - GET /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}

Retrieves a specific service category record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/serviceCategory`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the service category to retrieve.Table: Specification Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. Valid fields:

-   href
-   id
-   name

Data type: String

Default: Returns all fields

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Data type: Number

Default: 20

Maximum: 100

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. Use this value to paginate record retrieval. Don't use a negative number value.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept:application/json| |

<table id="table_oth_bdp_zgc" class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the Content-Range header is items `3-5`.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the response body. Only supports application/json.

</td></tr><tr><td>

Link

</td><td>

Contains the following links to navigate through query results:

-   first
-   last
-   next
-   previous

</td></tr><tr><td>

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_xwz_ncp_zgc"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

206

</td><td>

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td>

Bad request.Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td>

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_d3r_4cp_zgc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

externalIdentifier

</td><td>

Identifying information for an external system involved in managing categories.Data type: Array of objects

```
"externalIdentifier": [
 {
  "id": "String",
  "owner": "String"
 }
]
```

</td></tr><tr><td>

externalIdentifier.id

</td><td>

Unique identifier for the service category. This value is determined by an external system. Data type: String

Table: Specification Category \[sn\_prd\_pm\_specification\_category\], Field: external\_id

</td></tr><tr><td>

externalIdentifier.owner

</td><td>

The system that owns this ID. Data type: String

</td></tr><tr><td>

href

</td><td>

Hyperlink to access the service category.Data type: string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service category. Table: Specification Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr><tr><td>

isRoot

</td><td>

Flag that indicates whether the category is a root of categories.Valid values:

-   true: Category is a root of categories.
-   false: Category isn't a root of categories.

Data type:Boolean

</td></tr><tr><td>

modelCategory

</td><td>

List of model categories associated with the service category.Data type: Array of objects

```
"modelCategory": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

modelCategory.id

</td><td>

Sys\_id of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

modelCategory.name

</td><td>

Name of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the service category.Data type: String

</td></tr><tr><td>

serviceCandidate

</td><td>

List of service candidates associated with this category.Data type: Array of Objects

```
"serviceCandidate": [
 {
  "id": "String",
  "href": "String",
  "name": "String",
  "@referredType": "String",
  "version": "String" 
 }
]
```

</td></tr><tr><td>

serviceCandidate.@referredType

</td><td>

Referred type of the service candidate. Value is always `ServiceCategory`.Data type: String

</td></tr><tr><td>

serviceCandidate.href

</td><td>

Hyperlink to access the service specification.Data type: String

</td></tr><tr><td>

serviceCandidate.id

</td><td>

Sys\_id of the service specification.Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

Data type: String

</td></tr><tr><td>

serviceCandidate.version

</td><td>

Version of the service candidate.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example calls the GET operation to return a specific service category record according to a given ID, a2a68216d9ce2a90f87718429ae503dd.

```
curl "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/serviceCategory/a1b23456c7de8a90f0123456gh789ij" \
  --request GET \
  --header "Accept:application/json" \
  --user 'user:password'
```

Response body.

```
{
  "id": "a2a68216d9ce2a90f87718429ae503dd",
  "href": "api/sn_tmf_api/service_catalog_api/serviceCategory/a1b23456c7de8a90f0123456gh789ij",
  "name": "Cloud Services",
  "serviceCandidate": [
    {
      "id": "a1b23456c7de8a90f0123456gh789ij",
      "href": "api/sn_tmf_api/catalogmanagement/serviceSpecification/a1b23456c7de8a90f0123456gh789ij",
      "version": "1",
      "name": "servicenow",
     
```

## Service Catalog Open - GET /servicespecification

Retrieves a list of all service specifications.

### URL format

Default URL: `/api/sn_prd_pm_adv/catalogmanagement/servicespecification`

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

Filter service specifications by state. Only specifications with a state matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_c2r_4gm_lsb" class="rest_api_response_headers"><thead><tr><th>

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

<table id="table_qbg_4cm_lsb"><thead><tr><th>

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

<table id="table_hnx_3gy_fsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Type of specification.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.Data type: String

Table: In the external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

externalSystem

</td><td>

External system of the service specification, appended with `TMF633`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF633`.

Data Type: String

</td></tr><tr><td>

externalSystem

</td><td>

Third-party or non-native platform that interacts with the service catalog. Value is always appended with `TMF633`. For example, if the external system is `ABC` then the value in the external source should be `ABC-TMF633`. Data type: String

</td></tr><tr><td>

id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the initial\_version or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specifications for this service specification.Data type: Array of Objects

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

The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

The initial\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

This specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

The initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalId

</td><td>

The initial\_version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

List of possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be a simple or complex characteristic.Possible values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Text
-   Array.Obect
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

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr></tbody>
</table>### cURL request

This example retrieves all service specifications.

```
curl --location --request GET "https://instance.servicenow.com/api/sn_prd_pm_adv/catalogmanagement/servicespecification" \
--user 'username':'password'

```

Response body.

```
[
   {
      "id": "16d79ec3532520103b6bddeeff7b12a6",
      "name": "SD WAN Optimization Service",
       "externalSystem": "Salesforce - TMF633",
      "description": "SD WAN Optimization Service",
      "lastUpdate": "2022-01-23 22:48:55",
      "validFor": {
         "startDateTime": "2022-01-12",
         "endDateTime": "2027-02-11"
      },
      "serviceSpecificationRelationship": [
         {
            "id": "a1f5fe981bb420106ba59acf034bcb4f",
            "name": "Deduplication and Compression",
            "version": "1",
            "type": "rfs",
            "validFor": {
               "startDateTime": "2021-02-11",
               "endDateTime": "2027-02-11"
            }
         }
      ],
      "resourceSpecification": [],
      "serviceSpecCharacteristic": [
         {
            "name": "SSL Optimization",
            "description": "SSL Optimization",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-14 07:47:57"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "False",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "True",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "CIFS Optimization",
            "description": "CIFS Optimization Protocol",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-14 07:49:09"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "SMB1",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "SMB2",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         }
      ]
      "externalSource": "ABC-TMF633"
   },
   {
      "id": "31c5caff07266010a7955b7e0ad3006b",
      "name": "Firewall Administration",
      "description": "Firewall Administration",
      "lastUpdate": "2022-01-23 11:46:48",
      "validFor": {
         "startDateTime": "2021-11-22",
         "endDateTime": ""
      },
      "serviceSpecificationRelationship": [],
      "resourceSpecification": [
         {
            "id": "3546463307666010a7955b7e0ad3005d",
            "name": "Cisco Firewall Management system",
            "version": "1"
         }
      ],
      "serviceSpecCharacteristic": [
         {
            "name": "Firewall Administration CPE Model",
            "description": "Firewall Administration CPE Model",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-02-20 00:55:37"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "2100 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "4100 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "7300 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "9300 series",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
    "externalSource": "ABC-TMF633"
         },
         {
            "name": "Firewall Administration CPE Type",
            "description": "Firewall Administration CPE Type",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-02-20 00:53:45"
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
            ]
         },
         {
            "name": "Configuration and Policy backup",
            "description": "Configuration and Policy backup",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-21 10:46:02"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Weekly",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Monthly",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Daily",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "Remote CLI troubleshoot support",
            "description": "Remote CLI troubleshoot support",
            "valueType": "choice",
            "validFor": {
               "startDatetime": "2022-01-21 10:45:38"
            },
            "productSpecCharacteristicValue": [
               {
                  "value": "Standard support",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Premium support",
                  "validFor": {
                     "startDateTime": ""
                  }
               },
               {
                  "value": "Basic support",
                  "validFor": {
                     "startDateTime": ""
                  }
               }
            ]
         },
         {
            "name": "Firewall Administration CPE ID",
            "description": "Firewall Administration CPE ID",
            "valueType": "single_line_text",
            "validFor": {
               "startDatetime": "2022-02-20 00:57:50"
            },
            "productSpecCharacteristicValue": []
         }
      ]
   }
]
```

## Service Catalog Open - GET /servicespecification/\{specificationId\}

Retrieves a service specification.

### URL format

Default URL: `/api/sn_prd_pm_adv/catalogmanagement/servicespecification/{specificationId}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

specificationId

</td><td>

Sys\_id of the service specification to retrieve.Data type: String

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr></tbody>
</table><table id="table_pfr_vgy_fsb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter is not used, all fields are returned. Data type: String

</td></tr><tr><td>

state

</td><td>

Filter service specifications by state. Only specifications with a state matching the value of this parameter are returned in the response.Data type: String

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

<table><thead><tr><th>

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

<table id="table_hnx_3gy_fsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Type of specification.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.Data type: String

Table: In the external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

externalSystem

</td><td>

External system of the service specification, appended with `TMF633`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF633`.

Data Type: String

</td></tr><tr><td>

externalSystem

</td><td>

Third-party or non-native platform that interacts with the service catalog. Value is always appended with `TMF633`. For example, if the external system is `ABC` then the value in the external source should be `ABC-TMF633`. Data type: String

</td></tr><tr><td>

id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the initial\_version or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specifications for this service specification.Data type: Array of Objects

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

The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

The initial\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

This specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

The initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalId

</td><td>

The initial\_version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

List of possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be a simple or complex characteristic.Possible values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Text
-   Array.Obect
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

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr></tbody>
</table>### cURL request

This example retrieves a service specification for a firewall service.

```
curl --location --request GET "https://instance.servicenow.com/api/sn_prd_pm_adv/catalogmanagement/servicespecification/31c5caff07266010a7955b7e0ad3006b" \
--user 'username':'password'
```

Response body.

```

{
   "id": "31c5caff07266010a7955b7e0ad3006b",
   "name": "Firewall Administration",
   "description": "Firewall Administration",
   "externalSystem": "Salesforce - TMF633",
   "lastUpdate": "2022-01-23 11:46:48",
   "validFor": {
      "startDateTime": "2021-11-22",
      "endDateTime": ""
   },
   "serviceSpecificationRelationship": [],
   "resourceSpecification": [
      {
         "id": "3546463307666010a7955b7e0ad3005d",
         "name": "Cisco Firewall Management system",
         "version": "1"
      }
   ],
   "serviceSpecCharacteristic": [
      {
         "name": "Firewall Administration CPE Model",
         "description": "Firewall Administration CPE Model",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-02-20 00:55:37"
         },
         "productSpecCharacteristicValue": [
            { "value": "2100 series", "validFor": { "startDateTime": "" } },
            { "value": "4100 series", "validFor": { "startDateTime": "" } },
            { "value": "7300 series", "validFor": { "startDateTime": "" } },
            { "value": "9300 series", "validFor": { "startDateTime": "" } }
         ]
      },
      {
         "name": "Firewall Administration CPE Type",
         "description": "Firewall Administration CPE Type",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-02-20 00:53:45"
         },
         "productSpecCharacteristicValue": [
            { "value": "Physical", "validFor": { "startDateTime": "" } },
            { "value": "Virtual", "validFor": { "startDateTime": "" } }
         ]
      },
      {
         "name": "Configuration and Policy backup",
         "description": "Configuration and Policy backup",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-01-21 10:46:02"
         },
         "productSpecCharacteristicValue": [
            { "value": "Weekly", "validFor": { "startDateTime": "" } },
            { "value": "Monthly", "validFor": { "startDateTime": "" } },
            { "value": "Daily", "validFor": { "startDateTime": "" } }
         ]
      },
      {
         "name": "Remote CLI troubleshoot support",
         "description": "Remote CLI troubleshoot support",
         "valueType": "choice",
         "validFor": {
            "startDatetime": "2022-01-21 10:45:38"
         },
         "productSpecCharacteristicValue": [
            { "value": "Standard support", "validFor": { "startDateTime": "" } },
            { "value": "Premium support", "validFor": { "startDateTime": "" } },
            { "value": "Basic support", "validFor": { "startDateTime": "" } }
         ]
      },
      {
         "name": "Firewall Administration CPE ID",
         "description": "Firewall Administration CPE ID",
         "valueType": "single_line_text",
         "validFor": {
            "startDatetime": "2022-02-20 00:57:50"
         },
         "productSpecCharacteristicValue": []
      }
   ],
   "externalSource": "ABC-TMF633"
}
```

## Service Category Open - PATCH /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}

Updates a specified record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/serviceCategory/ {id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id of the service category table.Table: Specification Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

externalIdentifier

</td><td>

Identifying information for an external system involved in managing categories.Data type: Array of Objects

```
"externalIdentifier": [
 {
  "id": "String",
  "owner": "String"
 }
]
```

</td></tr><tr><td>

externalIdentifier.id

</td><td>

Unique identifier for the service category. This value is determined by an external system. Table: Specification Category \[sn\_prd\_pm\_specification\_category\], Field: external\_id

Data type: String

</td></tr><tr><td>

externalIdentifier.owner

</td><td>

The system that owns this ID. Data type: String

</td></tr><tr><td>

href

</td><td>

Hyperlink to access the service category.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service category. Table: Specification Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr><tr><td>

isRoot

</td><td>

Flag that indicates whether the category is a root of categories.Valid values:

-   true: Category is a root of categories.
-   false: Category isn't a root of categories.

Data type: Boolean

</td></tr><tr><td>

modelCategory

</td><td>

List of model categories associated with the service category.Data type: Array of Objects

```
"modelCategory": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

modelCategory.id

</td><td>

Sys\_id of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

modelCategory.name

</td><td>

Name of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the service category.Data type: String

</td></tr><tr><td>

serviceCandidate

</td><td>

List of service candidates associated with this category.Data type: Array of objects

```
"serviceCandidate": [
 {
  "@referredType": "String",
  "href": "String",
  "id": "String",
  "name": "String",
  "version": "String" 
 }
]
```

</td></tr><tr><td>

serviceCandidate.@referredType

</td><td>

Value is always `ServiceCategory`.Data type: String

</td></tr><tr><td>

serviceCandidate.href

</td><td>

Hyperlink to access the service specification.Data type: String

</td></tr><tr><td>

serviceCandidate.id

</td><td>

Sys\_id of the service specification.Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

Data type: String

</td></tr><tr><td>

serviceCandidate.version

</td><td>

Version of the service candidate.Data type: String

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

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the request body. Only supports application/json.|
|Content-Type|Data format of the request body. Only supports application/json.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_lpd_1kp_zgc"><thead><tr><th>

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

Bad Request. A bad request type or malformed request was detected for one or more of the following reasons:

-   Empty payload.
-   Invalid payload.
-   Mandatory field missing.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_d3r_4cp_zgc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

externalIdentifier

</td><td>

Identifying information for an external system involved in managing categories.Data type: Array of objects

```
"externalIdentifier": [
 {
  "id": "String",
  "owner": "String"
 }
]
```

</td></tr><tr><td>

externalIdentifier.id

</td><td>

Unique identifier for the service category. This value is determined by an external system. Data type: String

Table: Specification Category \[sn\_prd\_pm\_specification\_category\], Field: external\_id

</td></tr><tr><td>

externalIdentifier.owner

</td><td>

The system that owns this ID. Data type: String

</td></tr><tr><td>

href

</td><td>

Hyperlink to access the service category.Data type: string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service category. Table: Specification Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr><tr><td>

isRoot

</td><td>

Flag that indicates whether the category is a root of categories.Valid values:

-   true: Category is a root of categories.
-   false: Category isn't a root of categories.

Data type:Boolean

</td></tr><tr><td>

modelCategory

</td><td>

List of model categories associated with the service category.Data type: Array of objects

```
"modelCategory": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

modelCategory.id

</td><td>

Sys\_id of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

modelCategory.name

</td><td>

Name of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the service category.Data type: string

</td></tr><tr><td>

serviceCandidate

</td><td>

List of service candidates associated with this category.Data type: Array of objects

```
"serviceCandidate": [
 {
  "@referredType": "String",
  "href": "String",
  "id": "String",
  "name": "String",
  "version": "String" 
 }
]
```

</td></tr><tr><td>

serviceCandidate.@referredType

</td><td>

Value is always `ServiceCategory`.Data type: String

</td></tr><tr><td>

serviceCandidate.href

</td><td>

Hyperlink to access the service specification.Data type: String

</td></tr><tr><td>

serviceCandidate.id

</td><td>

Sys\_id of the service specification.Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

Data type: String

</td></tr><tr><td>

serviceCandidate.version

</td><td>

Version of the service candidate.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example updates the service category's name, version, service candidate, model category, and external identifier information.

```
curl "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/serviceCategory/a1b23456c7de8a90f0123456gh789ij" \
  --request PATCH \
  --header "Accept:application/json" \
  --header "Content-Type:application/json" \
  --data '{
    "name": "Cloud Services",
    "version": "1.0",
    "serviceCandidate": [
      {
        "id": "a1b23456c7de8a90f0123456gh789ij",
        "href": "https://mycsp.com:8080/tmf-api/serviceCatalogManagement/v4/serviceCategory/5980",
        "version": "3.2",
        "name": "Cloud Services",
        "@referredType": "ServiceCategory"
      }
    ],
    "modelCategory": [
      {
        "id": "b2d5bc14c3031000b959fd251eba8f96",
        "name": "model"
      }
    ],
    "externalIdentifier": {
      "id": "1234234312",
      "owner": "TMF200000123233"
    },
    "isRoot": true
  }' \
  --user 'user:password
```

Response body.

```
{
  "name": "Cloud Services",
  "version": "1.0",
  "serviceCandidate": [
    {
      "id": "a1b23456c7de8a90f0123456gh789ij",
      "href": "https://mycsp.com:8080/tmf-api/serviceCatalogManagement/v4/serviceCategory/5980",
      "version": "3.2",
      "name": "Cloud Services",
      "@referredType": "ServiceCategory"
    }
  ],
  "modelCategory": [
    {
      "id": "b2d5bc14c3031000b959fd251eba8f96",
      "name": "model"
    }
  ],
  "externalIdentifier": {
    "id": "1234234312",
    "owner": "TMF200000123233"
  },
  "isRoot": true,
  "id": "8138241b1caaaa10f87703c075c809fe",
  "href": "api/sn_tmf_api/catalogmanagement/serviceCategory/8138241b1caaaa10f87703c075c809fe"
}
```

## Service Catalog Open - POST /api/sn\_tmf\_api/catalogmanagement/serviceCategory

Creates a new service category record in the Specification Category \[sn\_prd\_pm\_specification\_category\] table.

### URL format

Default URL: `/api/sn_tmf_api/catalogmanagement/serviceCategory`

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

externalIdentifier

</td><td>

Identifying information for an external system involved in managing categories.Data type: Array of Objects

```
"externalIdentifier": [
 {
  "id": "String",
  "owner": "String"
 }
]
```

</td></tr><tr><td>

externalIdentifier.id

</td><td>

Unique identifier for the service category. This value is determined by an external system. Table: Specification Category \[sn\_prd\_pm\_specification\_category\], Field: external\_id

Data type: String

</td></tr><tr><td>

externalIdentifier.owner

</td><td>

The system that owns this ID. Data type: String

</td></tr><tr><td>

href

</td><td>

Hyperlink to access the service category.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service category. Table: Specification Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr><tr><td>

isRoot

</td><td>

Flag that indicates whether the category is a root of categories.Valid values:

-   true: Category is a root of categories.
-   false: Category isn't a root of categories.

Data type: Boolean

</td></tr><tr><td>

modelCategory

</td><td>

List of model categories associated with the service category.Data type: Array of Objects

```
"modelCategory": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

modelCategory.id

</td><td>

Sys\_id of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

modelCategory.name

</td><td>

Name of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the service category.Data type: String

</td></tr><tr><td>

serviceCandidate

</td><td>

List of service candidates associated with this category.Data type: Array of objects

```
"serviceCandidate": [
 {
  "id": "String",
  "href": "String",
  "name": "String",
  "@referredType": "String",
  "version": "String" 
 }
]
```

</td></tr><tr><td>

serviceCandidate.@referredType

</td><td>

Value is always `ServiceCategory`.Data type: String

</td></tr><tr><td>

serviceCandidate.href

</td><td>

Hyperlink to access the service specification.Data type: String

</td></tr><tr><td>

serviceCandidate.id

</td><td>

Sys\_id of the service specification.Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

Data type: String

</td></tr><tr><td>

serviceCandidate.version

</td><td>

Version of the service candidate.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the request body. Only supports application/json.|
|Content-Type|Data format of the request body. Only supports application/json.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports application/json.|

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

Bad Request. A bad request type or malformed request was detected for one or more of the following reasons:

-   Empty payload.
-   Invalid payload.
-   Mandatory field missing.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_d3r_4cp_zgc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

externalIdentifier

</td><td>

Identifying information for an external system involved in managing categories.Data type: Array of objects

```
"externalIdentifier": [
 {
  "id": "String",
  "owner": "String"
 }
]
```

</td></tr><tr><td>

externalIdentifier.id

</td><td>

Unique identifier for the service category. This value is determined by an external system. Data type: String

Table: Specification Category \[sn\_prd\_pm\_specification\_category\], Field: external\_id

</td></tr><tr><td>

externalIdentifier.owner

</td><td>

The system that owns this ID. Data type: String

</td></tr><tr><td>

href

</td><td>

Hyperlink to access the service category.Data type: string

</td></tr><tr><td>

id

</td><td>

Sys\_id of the service category. Table: Specification Category \[sn\_prd\_pm\_specification\_category\]

Data type: String

</td></tr><tr><td>

isRoot

</td><td>

Flag that indicates whether the category is a root of categories.Valid values:

-   true: Category is a root of categories.
-   false: Category isn't a root of categories.

Data type:Boolean

</td></tr><tr><td>

modelCategory

</td><td>

List of model categories associated with the service category.Data type: Array of objects

```
"modelCategory": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

modelCategory.id

</td><td>

Sys\_id of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

modelCategory.name

</td><td>

Name of the model category. Table: Model Category \[cmdb\_model\_category\]

Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the service category.Data type: string

</td></tr><tr><td>

serviceCandidate

</td><td>

List of service candidates associated with this category.Data type: Array of objects

```
"serviceCandidate": [
 {
  "id": "String",
  "href": "String",
  "name": "String",
  "@referredType": "String",
  "version": "String" 
 }
]
```

</td></tr><tr><td>

serviceCandidate.@referredType

</td><td>

Value is always `ServiceCategory`.Data type: String

</td></tr><tr><td>

serviceCandidate.href

</td><td>

Hyperlink to access the service specification.Data type: String

</td></tr><tr><td>

serviceCandidate.id

</td><td>

Sys\_id of the service specification.Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

Data type: String

</td></tr><tr><td>

serviceCandidate.version

</td><td>

Version of the service candidate.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example calls POST to create a new service category record according to details provided in the request body.

```
curl "https://instance.service-now.com/api/sn_tmf_api/catalogmanagement/serviceCategory" \
  --request POST \
  --header "Accept:application/json" \
  --header "Content-Type:application/json" \
  --user 'user:password' \
  --data '{
    "name": "Cloud Services",
    "version": "1.0",
    "serviceCandidate": [
      {
        "id": "a1b23456c7de8a90f0123456gh789ij",
        "href": "https://mycsp.com:8080/tmf-api/serviceCatalogManagement/v4/serviceCategory/5980",
        "version": "3.2",
        "name": "Cloud Services",
        "@referredType": "ServiceCategory"
      }
    ],
    "modelCategory": [
      {
        "id": "b2d5bc14c3031000b959fd251eba8f96",
        "name": "model"
      }
    ],
    "externalIdentifier": {
      "id": "1234234312",
      "owner": "TMF200000123233"
    },
    "isRoot": true
  }'
```

Response body.

```
{
  "name": "Cloud Services",
  "version": "1.0",
  "serviceCandidate": [
    {
      "id": "a1b23456c7de8a90f0123456gh789ij",
      "href": "https://mycsp.com:8080/tmf-api/serviceCatalogManagement/v4/serviceCategory/5980",
      "version": "3.2",
      "name": "Cloud Services",
      "@referredType": "ServiceCategory"
    }
  ],
  "modelCategory": [
    {
      "id": "b2d5bc14c3031000b959fd251eba8f96",
      "name": "model"
    }
  ],
  "externalIdentifier": {
    "id": "1234234312",
    "owner": "TMF200000123233"
  },
  "isRoot": true,
  "id": "8138241b1caaaa10f87703c075c809fe",
  "href": "api/sn_tmf_api/service_catalog_api/serviceCategory/8138241b1caaaa10f87703c075c809fe"
}
```

## Service Catalog Open - POST /servicespecification

Creates a service specification.

### URL format

Default URL: `/api/sn_prd_pm_adv/catalogmanagement/servicespecification`

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

Required. Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.If both **externalId** and **id** are provided, they must refer to the same specification.

Data type: String

Default: Blank string

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

</td></tr><tr><td>

externalSystem

</td><td>

Third-party or non-native platform that interacts with the service catalog. Value is always appended with `TMF633`.For example, if the external system is `ABC` then the value in the external source should be `ABC-TMF633`.

 Data type: String

</td></tr><tr><td>

id

</td><td>

The initial\_version or external\_id of the service specification. If **id** is not provided, this endpoint creates a new specification with version=1. If **id** is provided, this endpoint creates a new version of the given specification. If both **externalId** and **id** are provided, they must refer to the same specification.

Data type: String

Default: Blank string

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Default: Blank string

Table: Service Specification \[sn\_prd\_pm\_service\_specification\]

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

resourceSpecification

</td><td>

Required. Resource specifications for this service specification.Data type: Array of Objects

```
"resourceSpecification": [
  {
    "id": "String",
    "internalVersion": "String",
    "name": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

resourceSpecification.id

</td><td>

Required. The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

Default: Blank string

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

Default: Blank string

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

Details of the specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

Required if using the **serviceSpecificationRelationship** parameter. Initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Required if using the **serviceSpecificationRelationship** parameter. Type of relationship.Valid values:

-   bundles
-   composed\_of

Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

Default: Blank string

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Required. Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Required. Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Required. Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

Default: Blank string

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be a simple or complex characteristic.Possible values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Text
-   Array.Obect
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

End date of the specification.Data type: String

Default: Blank string

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date of the specification.Data type: String

Default: Blank string

</td></tr><tr><td>

version

</td><td>

External version of the service specification. Version must be unique for the given version chain.

Data type: String

Default: Blank string

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

@type

</td><td>

Required. Type of specification.Valid values:

-   CustomerFacingServiceSpecification
-   ResourceFacingServiceSpecification

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

Request successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Could be any of the following reasons: -   Empty payload.
-   Invalid payload. Mandatory field missing: &lt;field name&gt;

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_hnx_3gy_fsb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

Type of specification.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the specification.Data type: String

</td></tr><tr><td>

externalId

</td><td>

External ID of the service specification.Data type: String

Table: In the external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

externalSystem

</td><td>

External system of the service specification, appended with `TMF633`. For example, if the external system is ABC then enter the value in **externalSystem** as `ABC-TMF633`.

Data Type: String

</td></tr><tr><td>

externalSystem

</td><td>

Third-party or non-native platform that interacts with the service catalog. Value is always appended with `TMF633`. For example, if the external system is `ABC` then the value in the external source should be `ABC-TMF633`. Data type: String

</td></tr><tr><td>

id

</td><td>

Initial version or external ID of the service specification.Data type: String

Table: In the initial\_version or external\_id field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalId

</td><td>

Initial version of the service specification.Data type: String

Table: In the initial\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

internalVersion

</td><td>

Version of the service specification.Data type: String

Table: In the version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr><tr><td>

lastUpdate

</td><td>

Date the specification was last updated.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the specification.Data type: String

</td></tr><tr><td>

resourceSpecification

</td><td>

Resource specifications for this service specification.Data type: Array of Objects

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

The initial\_version or external\_id of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalId

</td><td>

The initial\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.internalVersion

</td><td>

The external\_version of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.name

</td><td>

Name of the resource specification.Data type: String

</td></tr><tr><td>

resourceSpecification.version

</td><td>

Version of the resource specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship

</td><td>

This specification's relationships to other service specifications.Data type: Array of Objects

```
"serviceSpecificationRelationship": [
  {
    "id": "String",
    "internalId": "String",
    "internalVersion": "String",
    "relationshipType": "String",
    "validFor": {Object},
    "version": "String"
  }
]
```

</td></tr><tr><td>

serviceSpecificationRelationship.id

</td><td>

The initial\_version or external\_id of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalId

</td><td>

The initial\_version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.internalVersion

</td><td>

Version of the related specification.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.relationshipType

</td><td>

Type of relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor

</td><td>

Date range the relationship is valid for.Data type: Object

```
"validFor": {
   "endDateTime": "String",
   "startDateTime": "String"
}
```

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.endDateTime

</td><td>

End date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.validFor.startDateTime

</td><td>

Start date of the relationship.Data type: String

</td></tr><tr><td>

serviceSpecificationRelationship.version

</td><td>

The external\_version of the related specification.Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Specification characteristic.Data type: Array of Objects

```
"specCharacteristic": [
  {
    "characteristicValueSpecification": [Array],
    "description": "String",
    "name": "String",
    "validFor": {Object},
    "valueType": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

List of possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Value type of the characteristic, such as choice or email. Can be a simple or complex characteristic.Possible values:

-   Date,Address
-   Integer,Date/Time
-   Array.Integer
-   Array.Single Line Test
-   Single Line Text
-   Array.Obect
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

External version of the service specification.Data type: String

Table: In the external\_version field of the Service Specification \[sn\_prd\_pm\_service\_specification\] table.

</td></tr></tbody>
</table>### cURL request

This example creates a service specification for a firewall service.

```
curl "https://instance.servicenow.com/api/sn_prd_pm_adv/catalogmanagement/servicespecification" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"externalId\": \"7655\",
   \"name\": \"Firewall Service\",
   \"description\": \"This service specification describes a firewall service that can be deployed in customer-premises equipment.\",
   \"validFor\": {
      \"startDateTime\": \"2017-08-23T00:00\",
      \"endDateTime\": \"2021-03-25T00:00\"
   },
   \"lastUpdate\": \"2020-08-15T00:00\",
   \"externalSource\": \"ABC-TMF633\",
   \"resourceSpecification\": [
      {
         \"id\": \"af66e551c32f10105252716b7d40dd52\",
         \"name\": \"Firewall\"
      }
   ],
   \"specCharacteristic\": [
      {
         \"name\": \"Edge\",
         \"description\": \"This characteristic describes the operating system run by the service\",
         \"valueType\": \"choice\",
         \"validFor\": {
            \"startDateTime\": \"2017-08-12T00:00\",
            \"endDateTime\": \"2021-03-07T00:00\"
         },
         \"characteristicValueSpecification\": [
            {
               \"value\": \"Android KitKat\"
            }
         ]
      }
   ],
   \"serviceSpecRelationship\": [
      {
         \"relationshipType\": \"composed_of\",
         \"id\": \"65033023ebdb30107ee5302698522849\",
         \"validFor\": {
            \"startDateTime\": \"2017-08-25T00:00\",
            \"endDateTime\": \"2021-03-25T00:00\"
         }
      }
   ],
   \"@type\": \"ResourceFacingServiceSpecification\"
}" \
--user 'username':'password'
```

Response body.

```
{
   "id": "21a7ee64c32310105253716b8d40dd60",
   "name": "Firewall Service",
   "description": "This service specification describes a firewall service that can be deployed in customer-premises equipment.",
   "validFor": {
      "startDateTime": "2017-08-23T00:00",
      "endDateTime": "2021-03-25T00:00"
   },
   "lastUpdate": "2020-08-15T00:00",
   "externalSource": "ABC-TMF633",
   "resourceSpecification": [
      {
         "id": "af66e551c32f10105252716b7d40dd52",
         "name": "Firewall"
      }
   ],
   "specCharacteristic": [
      {
         "name": "Edge",
         "description": "This characteristic describes the operating system run by the service",
         "valueType": "choice",
         "validFor": {
            "startDateTime": "2017-08-12T00:00",
            "endDateTime": "2021-03-07T00:00"
         },
         "characteristicValueSpecification": [
            {
               "value": "Android KitKat"
            }
         ]
      }
   ],
   "serviceSpecRelationship": [
      {
         "relationshipType": "composed_of",
         "id": "65033023ebdb30107ee5302698522849",
         "validFor": {
            "startDateTime": "2017-08-25T00:00",
            "endDateTime": "2021-03-25T00:00"
         }
      }
   ],
   "@type": "ResourceFacingServiceSpecification"
}
```

