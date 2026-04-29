---
title: TISC TAXII Server API
description: Provides Trusted Automated Exchange of Intelligence Information \(TAXII\) server endpoints for sharing threat intelligence data in Threat Intelligence Security Center \(TISC\).Discovery endpoint for the TAXII server. Provides metadata about available API roots, services offered by the TISC TAXII server, and how to interact with it.Provides information about an API root.Returns data about all available TAXII collections at the specified API root.Returns data about a specified collection.Returns objects from a specified collection.Returns a specified object from a collection.Returns all versions of a specified object from a collection.Provides a summary of the objects in a collection.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 23
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# TISC TAXII Server API

Provides Trusted Automated Exchange of Intelligence Information \(TAXII\) server endpoints for sharing threat intelligence data in Threat Intelligence Security Center \(TISC\).

This API requires the Threat Intelligence Security Center application, which is available on the ServiceNow Store.

For additional information about TISC, see [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&version=australia&pubname=australia-security-management&ft:locale=en-US).

This API runs in the `sn_sec_tisc` namespace. The calling user must have the sn\_sec\_tisc.taxii\_server\_api\_user role.

The current version of this API is `v2`. The following capabilities are supported in each version.

-   **v1**

    Supports sharing threat intelligence data from one ServiceNow instance to another.

-   **v2**
    -   Adds support for sharing threat intelligence data from a ServiceNow instance to an external system.
    -   Supports trailing slashes.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/taxii2

Discovery endpoint for the TAXII server. Provides metadata about available API roots, services offered by the TISC TAXII server, and how to interact with it.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/taxii2`

Default URL: `/api/sn_sec_tisc/taxii_server/taxii2`

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

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_roots

</td><td>

List of API roots available in the server.**Note:** The only API root currently supported by Threat Intelligence Security Center is `api/sn_sec_tisc/taxii_server/api_root`.

Data type: Array

</td></tr><tr><td>

contact

</td><td>

Contact information related to the TAXII server. Data type: String

</td></tr><tr><td>

default

</td><td>

Default API root that a TAXII client can use.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the TAXII server. Data type: String

</td></tr><tr><td>

title

</td><td>

Title of the TAXII server.Data type: String

</td></tr></tbody>
</table>### cURL request

This example returns metadata about available API roots.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/taxii2" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password'
```

Response body.

```
{ 
    "title": "ServiceNow TAXII Server", 
    "description": "Discovery endpoint for sharing cyber threat intelligence via TAXII", 
    "contact": "TAXII Server Contact", 
    "default": "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root", 
    "api_roots": [ 
        "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root" 
    ] 
}
```

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}

Provides information about an API root.

**Note:** The only API root currently supported by Threat Intelligence Security Center is `api/sn_sec_tisc/taxii_server/api_root`.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/{api_root}`

Default URL: `/api/sn_sec_tisc/taxii_server/{api_root}`

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

api\_root

</td><td>

The API root to retrieve information about.**Note:** The only value currently supported is `api_root`.

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
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the API root.Data type: String

</td></tr><tr><td>

max\_content\_length

</td><td>

Maximum size of a request body that can be supported by the TAXII server.Data type: Number

Unit: Octets \(8-bit bytes\)

</td></tr><tr><td>

title

</td><td>

Title of the API root.Data type: String

</td></tr><tr><td>

versions

</td><td>

List of TAXII versions that the API root is compatible with. **Note:** The only version currently supported is TAXII 2.1, so this array contains only the value `application/taxii+json;version=2.1`.

Data type: Array

</td></tr></tbody>
</table>### cURL request

This example returns information about an API root.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password'
```

Response body.

```
{ 
    "title": "ServiceNow TAXII Server", 
    "description": "API root endpoint for sharing cyber threat intelligence via TAXII", 
    "versions": [ 
        "application/taxii+json;version=2.1" 
    ], 
    "max_content_length": 1024 
}
```

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections

Returns data about all available TAXII collections at the specified API root.

A TAXII collection is a logical grouping of threat intelligence data that enables the exchange of information between a TAXII client and a TAXII server.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/{api_root}/collections`

Default URL: `/api/sn_sec_tisc/taxii_server/{api_root}/collections`

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

api\_root

</td><td>

The API root to retrieve information about.**Note:** The only value currently supported is `api_root`.

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
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

collections

</td><td>

List of collection objects available at the requested API root.Data type: Array

```
"collections": [
    { 
        "can_read": Boolean,   
        "can_write": Boolean,
        "description": "String",  
        "id": "String", 
        "media_types": [Array], 
        "title": "String" 
    } 
]
```

</td></tr><tr><td>

collections.can\_read

</td><td>

Flag that indicates whether the calling user can read data from the collection.Valid values:

-   true: The user can read collection data.
-   false: The user can't read collection data.

Data type: Boolean

</td></tr><tr><td>

collections.can\_write

</td><td>

Flag that indicates whether the calling user can write data to the collection.Valid values:

-   true: The user can write collection data.
-   false: The user can't write collection data.

**Note:** The TISC TAXII server doesn't support writing data to collections.

Data type: Boolean

</td></tr><tr><td>

collections.description

</td><td>

Description of the collection.Data type: String

</td></tr><tr><td>

collections.id

</td><td>

Sys\_id of the collection.Table: TAXII Collection \[sn\_sec\_tisc\_taxii\_server\_collection\]

Data type: String

</td></tr><tr><td>

collections.media\_types

</td><td>

List of supported media types for objects in the collection.**Note:** The only version currently supported is TAXII 2.1, so this array contains only the value `application/taxii+json;version=2.1`.

Data type: Array

</td></tr><tr><td>

collections.title

</td><td>

Title of the collection.Data type: String

</td></tr></tbody>
</table>### cURL request

This example returns data about all available TAXII collections at the specified API root.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root/collections" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password'
```

Response body.

```
{ 
    "collections": [ 
        { 
            "id": "308accee37cd22107253a2d734924baf", 
            "title": " Collection-1", 
            "can_read": true, 
            "can_write": false, 
            "media_types": [ 
                "application/taxii+json;version=2.1" 
            ] 
        }, 
        { 
            "id": "308accee37cd22107253a2d734926ghy", 
            "title": " Collection-2", 
            "can_read": true, 
            "can_write": false, 
            "media_types": [ 
                "application/taxii+json;version=2.1" 
            ] 
        } 
    ] 
}
```

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}

Returns data about a specified collection.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/{api_root}/collections/{id}`

Default URL: `/api/sn_sec_tisc/taxii_server/{api_root}/collections/{id}`

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

api\_root

</td><td>

The API root to retrieve information about.**Note:** The only value currently supported is `api_root`.

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the collection.Table: TAXII Collection \[sn\_sec\_tisc\_taxii\_server\_collection\]

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
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_ezw_lzy_hfc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

can\_read

</td><td>

Flag that indicates whether the calling user can read data from the collection.Valid values:

-   true: The user can read collection data.
-   false: The user can't read collection data.

Data type: Boolean

</td></tr><tr><td>

can\_write

</td><td>

Flag that indicates whether the calling user can write data to the collection.Valid values:

-   true: The user can write collection data.
-   false: The user can't write collection data.

**Note:** The TISC TAXII server doesn't support writing data to collections.

Data type: Boolean

</td></tr><tr><td>

description

</td><td>

Description of the collection.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the collection.Table: TAXII Collection \[sn\_sec\_tisc\_taxii\_server\_collection\]

Data type: String

</td></tr><tr><td>

media\_types

</td><td>

List of supported media types for objects in the collection.**Note:** The only version currently supported is TAXII 2.1, so this array contains only the value `application/taxii+json;version=2.1`.

Data type: Array

</td></tr><tr><td>

title

</td><td>

Title of the collection.Data type: String

</td></tr></tbody>
</table>### cURL request

This example returns data about a specified collection.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root/collections/308accee37cd22107253a2d734924baf" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password'
```

Response body.

```
{ 
    "id": "308accee37cd22107253a2d734924baf", 
    "title": " Collection-1", 
    "can_read": true, 
    "can_write": false, 
    "media_types": [ 
        "application/taxii+json;version=2.1" 
    ] 
}
```

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects

Returns objects from a specified collection.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/{api_root}/collections/{id}/objects`

Default URL: `/api/sn_sec_tisc/taxii_server/{api_root}/collections/{id}/objects`

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

api\_root

</td><td>

The API root to retrieve information about.**Note:** The only value currently supported is `api_root`.

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the collection.Table: TAXII Collection \[sn\_sec\_tisc\_taxii\_server\_collection\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

added\_after

</td><td>

Returns only objects added after the specified time. The timestamp must be in ISO 8601 format, such as `2025-10-27T16:36:20.000Z`.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **next** parameter to paginate record retrieval.Data type: Number

Default: 100 records per page

Maximum: 1000

</td></tr><tr><td>

match\[id\]

</td><td>

Unique identifiers of the objects to return, formatted as a string of comma separated values.Object ids can be retrieved using the GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects endpoint. They are located in the **objects.id** parameter in the response body.

Data type: String

</td></tr><tr><td>

match\[spec\_version\]

</td><td>

Specification versions of objects to return, formatted as a string of comma separated values.**Note:** The only value currently supported is `2.1`.

Data type: String

</td></tr><tr><td>

match\[type\]

</td><td>

Types of objects to return, formatted as a string of comma separated values.Data type: String

</td></tr><tr><td>

match\[version\]

</td><td>

Versions of objects to return, formatted as a string of comma separated values.Data type: String

</td></tr><tr><td>

next

</td><td>

Starting page index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

more

</td><td>

Flag that indicates whether the response has a next page.Valid values:

-   true: There is a next page.
-   false: There isn't a next page.

Data type: Boolean

</td></tr><tr><td>

next

</td><td>

Index of the next page of the response.Data type: String

</td></tr><tr><td>

objects

</td><td>

Array of objects in the collection. Objects are returned in [standard STIX format](https://docs.oasis-open.org/cti/stix/v2.1/os/stix-v2.1-os.html). The properties included in each object vary based on the object type.Data type: Array

</td></tr></tbody>
</table>### cURL request

This example returns all objects in the specified collection.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root/collections/308accee37cd22107253a2d734924baf/objects" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password'
```

Response body containing one URL object.

```

{
  "more": false,
  "objects": [
    {
      "id": "url--624ca0a8-ffd1-5210-8253-ffffffffffbe",
      "type": "url",
      "defanged": false,
      "value": "http://testurl.com",
      "object_marking_refs": [
        "marking-definition--613f2e26-407d-48c7-9eca-b8e91df99dc9"
      ],
      "extensions": {
        "extension-definition--ef28a0ac-ff11-4210-8253-ffffffffffbd": {
          "x_is_false_positive": false,
          "x_domain": "testurl.com",
          "x_status": "Active",
          "x_source_count": 2,
          "x_threat_score": 50,
          "extension_type": "property-extension"
        }
      }
    },
    {
      "id": "indicator--657bef11-2b7c-4a50-8758-f8014391bff3",
      "type": "indicator",
      "spec_version": "2.1",
      "created": "2025-10-24T14:09:23.000Z",
      "modified": "2025-11-20T12:14:24.000Z",
      "revoked": false,
      "confidence": 75,
      "object_marking_refs": [
        "marking-definition--613f2e26-407d-48c7-9eca-b8e91df99dc9"
      ],
      "pattern": "url:value = 'http://testurl.com'",
      "pattern_type": "stix",
      "name": "Test Indicator",
      "pattern_version": "2.1",
      "valid_from": "2025-10-24T14:09:19.000Z",
      "extensions": {
        "extension-definition--4f5ba226-ff95-4210-8238-ffffffffff1d": {
          "x_status": "Active",
          "x_source_count": 1,
          "x_used_for_detection": false,
          "x_threat_level": "High",
          "x_threat_severity": "High",
          "x_ioc_classification": "Potential Threat",
          "extension_type": "property-extension"
        }
      }
    },
    {
      "name": "Test Campaign",
      "id": "campaign--a02ce391-2b7c-4a50-8758-f8014391bf45",
      "type": "campaign",
      "spec_version": "2.1",
      "created": "2025-10-24T14:12:19.000Z",
      "modified": "2025-11-20T12:14:39.000Z",
      "revoked": false,
      "confidence": 75,
      "object_marking_refs": [
        "marking-definition--613f2e26-407d-48c7-9eca-b8e91df99dc9"
      ],
      "aliases": [
        "Test Campaign"
      ],
      "extensions": {
        "extension-definition--8b5ba226-ff95-4210-8238-ffffffffff1d": {
          "x_source_count": 1,
          "x_threat_level": "High",
          "x_threat_severity": "High",
          "x_status": "Active",
          "extension_type": "property-extension"
        }
      }
    }
  ]
}
```

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects/\{object\_id\}

Returns a specified object from a collection.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/{api_root}/collections/{id}/objects/{object_id}`

Default URL: `/api/sn_sec_tisc/taxii_server/{api_root}/collections/{id}/objects/{object_id}`

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

api\_root

</td><td>

The API root to retrieve information about.**Note:** The only value currently supported is `api_root`.

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the collection.Table: TAXII Collection \[sn\_sec\_tisc\_taxii\_server\_collection\]

Data type: String

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the object.Object ids can be retrieved using the GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects endpoint. They are located in the **objects.id** parameter in the response body.

Data type: String

</td></tr></tbody>
</table><table id="table_z2w_xjd_h3c" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

added\_after

</td><td>

Returns only objects added after the specified time. The timestamp must be in ISO 8601 format, such as `2025-10-27T16:36:20.000Z`.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **next** parameter to paginate record retrieval.Data type: Number

Default: 100 records per page

Maximum: 1000

</td></tr><tr><td>

match\[spec\_version\]

</td><td>

Specification versions of objects to return, formatted as a string of comma separated values.**Note:** The only value currently supported is `2.1`.

Data type: String

</td></tr><tr><td>

match\[version\]

</td><td>

Versions of objects to return, formatted as a string of comma separated values.Data type: String

</td></tr><tr><td>

next

</td><td>

Starting page index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

objects

</td><td>

The requested object returned in [standard STIX format](https://docs.oasis-open.org/cti/stix/v2.1/os/stix-v2.1-os.html). The properties included in the object vary based on the object type.Data type: Array

</td></tr></tbody>
</table>### cURL request

This example returns a specified URL object.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root/collections/308accee37cd22107253a2d734924baf/objects/url--624ca0a8-ffd1-5210-8253-ffffffffffbe" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password' 
```

Response body.

```
{ 
    "objects": [ 
        { 
            "id": "url--624ca0a8-ffd1-5210-8253-ffffffffffbe", 
            "type": "url", 
            "defanged": false, 
            "value": "http://testurl.com ", 
            "object_marking_refs": [ 
                "marking-definition--613f2e26-407d-48c7-9eca-b8e91df99dc9" 
            ], 
            "extensions": { 
                "extension-definition--ef28a0ac-ff11-4210-8253-ffffffffffbd": { 
                    "x_is_false_positive": false, 
                    "x_domain": "testurl.com", 
                    "x_status": "Active", 
                    "x_source_count": 2, 
                    "x_threat_score": 50, 
                    "extension_type": "property-extension" 
                } 
            } 
        } 
    ] 
}
```

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects/\{object\_id\}/versions

Returns all versions of a specified object from a collection.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/{api_root}/collections/{id}/objects/{object_id}/versions`

Default URL: `/api/sn_sec_tisc/taxii_server/{api_root}/collections/{id}/objects/{object_id}/versions`

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

api\_root

</td><td>

The API root to retrieve information about.**Note:** The only value currently supported is `api_root`.

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the collection.Table: TAXII Collection \[sn\_sec\_tisc\_taxii\_server\_collection\]

Data type: String

</td></tr><tr><td>

object\_id

</td><td>

Unique identifier of the object.Object ids can be retrieved using the GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects endpoint. They are located in the **objects.id** parameter in the response body.

Data type: String

</td></tr></tbody>
</table><table id="table_r1r_wjw_g3c" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

added\_after

</td><td>

Returns only objects added after the specified time. The timestamp must be in ISO 8601 format, such as `2025-10-27T16:36:20.000Z`.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **next** parameter to paginate record retrieval.Data type: Number

Default: 100 records per page

Maximum: 1000

</td></tr><tr><td>

match\[spec\_version\]

</td><td>

Specification versions of objects to return, formatted as a string of comma separated values.**Note:** The only value currently supported is `2.1`.

Data type: String

</td></tr><tr><td>

next

</td><td>

Starting page index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

versions

</td><td>

List of versions of the object.Data type: Array

</td></tr></tbody>
</table>### cURL request

This example returns all versions of a specified object from a collection.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root/collections/308accee37cd22107253a2d734924baf/objects/url--624ca0a8-ffd1-5210-8253-ffffffffffbe/versions" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password'
```

Response body.

```
{
  "versions": [
    "2025-11-20T12:16:38.000000Z",
    "2025-11-20T12:18:51.000000Z"
  ]
```

## TISC TAXII Server - GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/manifest

Provides a summary of the objects in a collection.

This endpoint enables clients to quickly understand what data is available without retrieving the full objects.

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/taxii_server/{api_root}/collections/{id}/manifest`

Default URL: `/api/sn_sec_tisc/taxii_server/{api_root}/collections/{id}/manifest`

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

api\_root

</td><td>

The API root to retrieve information about.**Note:** The only value currently supported is `api_root`.

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the collection.Table: TAXII Collection \[sn\_sec\_tisc\_taxii\_server\_collection\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

added\_after

</td><td>

Returns only objects added after the specified time. The timestamp must be in ISO 8601 format, such as `2025-10-27T16:36:20.000Z`.Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **next** parameter to paginate record retrieval.Data type: Number

Default: 100 records per page

Maximum: 1000

</td></tr><tr><td>

match\[id\]

</td><td>

Unique identifiers of the objects to return, formatted as a string of comma separated values.Object ids can be retrieved using the GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects endpoint. They are located in the **objects.id** parameter in the response body.

Data type: String

</td></tr><tr><td>

match\[spec\_version\]

</td><td>

Specification versions of objects to return, formatted as a string of comma separated values.**Note:** The only value currently supported is `2.1`.

Data type: String

</td></tr><tr><td>

match\[type\]

</td><td>

Types of objects to return, formatted as a string of comma separated values.Data type: String

</td></tr><tr><td>

match\[version\]

</td><td>

Versions of objects to return, formatted as a string of comma separated values.Data type: String

</td></tr><tr><td>

next

</td><td>

Starting page index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/taxii+json;version=2.1**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

more

</td><td>

Flag that indicates whether the response has a next page.Valid values:

-   true: There is a next page.
-   false: There isn't a next page.

Data type: Boolean

</td></tr><tr><td>

next

</td><td>

Index of the next page of the response.Data type: String

</td></tr><tr><td>

objects

</td><td>

Array of manifests for each object in the collection. A manifest provides a brief overview of an object.Data type: Array

```
"objects": [ 
    { 
        "date_added": "String",
        "id": "String",
        "media_types": "String",
        "version": "String"
    }
]
```

</td></tr><tr><td>

objects.date\_added

</td><td>

Date the object was added to the collection in ISO 8601 format, such as `2025-10-27T16:36:20.000Z`.Data type: String

</td></tr><tr><td>

objects.id

</td><td>

Unique identifier of the object.Object ids can be retrieved using the GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects endpoint. They are located in the **objects.id** parameter in the response body.

Data type: String

</td></tr><tr><td>

objects.media\_types

</td><td>

Media type of the object.**Note:** The only currently supported type is TAXII 2.1, so this value is always `application/taxii+json;version=2.1`.

Data type: String

</td></tr><tr><td>

objects.version

</td><td>

Version of the object.Data type: String

</td></tr></tbody>
</table>### cURL request

This example returns manifests for all objects in a collection.

```
curl "https://instance.servicenow.com/api/sn_sec_tisc/taxii_server/api_root/collections/308accee37cd22107253a2d734924baf/manifest" \ 
--request GET \ 
--header "Accept:application/taxii+json;version=2.1" \ 
--user 'username':'password'
```

Response body containing a manifest for one object.

```

{
  "more": false,
  "objects": [
    {
      "version": "2025-11-20T12:16:38.000000Z",
      "media_types": "application/taxii+json;version=2.1",
      "id": "indicator--657bef11-2b7c-4a50-8758-f8014391bff3",
      "date_added": "2025-11-20T04:16:38.000000Z"
    },
    {
      "version": "2025-11-20T12:16:38.000000Z",
      "media_types": "application/taxii+json;version=2.1",
      "id": "campaign--a02ce391-2b7c-4a50-8758-f8014391bf45",
      "date_added": "2025-11-20T04:16:38.000000Z"
    },
    {
      "version": "2025-11-20T12:18:51.000000Z",
      "media_types": "application/taxii+json;version=2.1",
      "id": "url--624ca0a8-ffd1-5210-8253-ffffffffffbe",
      "date_added": "2025-11-20T04:18:51.000000Z"
    }
  ]
}
```

