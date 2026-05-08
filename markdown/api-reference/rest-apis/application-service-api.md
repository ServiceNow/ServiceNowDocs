---
title: Application Service API
description: The Application Service API provides endpoints that enable you to create, modify, and update application services.Retrieves a list of configuration items \(CI\) in a mapped application service and the relationships between them. Only retrieves content for services that were manually created.Returns basic information about a specified application service and its associated business context.Creates an application service or update an existing application service.Creates an application service record stub in the Service Instance \[cmdb\_ci\_service\_auto\] table and populates it with the passed in information.Populates the specified application service with a specified set of downstream configuration items \(CI\).Updates the specified application service with the passed in basic information.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Application Service API

The Application Service API provides endpoints that enable you to create, modify, and update application services.

This API requires that the user have the Application Service administrator \[app\_service\_admin\] role.

**Important:** Starting with the Rome release, the Application Service API is no longer enhanced or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Application Service - GET /now/cmdb/app\_service/\{sys\_id\}/getContent

Retrieves a list of configuration items \(CI\) in a mapped application service and the relationships between them. Only retrieves content for services that were manually created.

### URL format

Default URL: `/api/now/cmdb/app_service/{sys_id}/getContent`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

Sys\_id of the mapped application service.Data type: String

Table: Mapped Application Service \[cmdb\_ci\_service\_discovered\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mode

</td><td>

Amount of relationship data to return. Valid values:

-   Full: Return CI attributes and lookup information in addition to the data returned in shallow mode.
-   Shallow: Return parent and child relationships between CIs within a service.

The values are not case-sensitive.Data type: String

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or they do not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_nyj_nl4_wlb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cmdb

</td><td>

List of objects that describe the CIs associated with the specified application service.Data type: Object

```
"cmdb": [
  {
    "items": {Object},
    "relations": [Array]
  }
]
```

</td></tr><tr><td>

cmdb.items

</td><td>

CIs within the application service. If the full query parameter was passed in the request, this section includes attributes and lookup information for each CI.Data type: Array

```
"items": [
  {
    "className": "String",
    "values": {Object}
  }
]
```

</td></tr><tr><td>

cmdb.items.className

</td><td>

Name of the class that contains the CI.Data type: String

</td></tr><tr><td>

cmdb.items.values

</td><td>

Information to use to locate an associated CI.Data type: Object

```
"values": {
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

cmdb.items.values.name

</td><td>

Name of the CI.Data type: String

</td></tr><tr><td>

cmdb.items.values.sys\_id

</td><td>

Sys\_id of the CI.Data type: String

</td></tr><tr><td>

cmdb.relations

</td><td>

Relationship data for associated CIs, such as hosts and their children.Data type: Array

</td></tr><tr><td>

service

</td><td>

List of services related to the identified service.Data type: Array of Objects

```
"service": [
  {
    "name": "String",
    "service_relations": [Array],
    "url": "String"
  }
]
```

</td></tr><tr><td>

service.name

</td><td>

Name of the application service.Data type: String

</td></tr><tr><td>

service.service\_relations

</td><td>

Hierarchy data for the CIs within the application service. All CIs form pairs with a parent and child CI. The top-level CI, referred to as the entry point of an application service, does not have a parent CI.Data type: Array of Objects

```
"service_relations": [
  {
    "child": "String",
    "parent": "String"
  }
]
```

</td></tr><tr><td>

service.service\_relations.child

</td><td>

Name of a child CI related to the CI.Data type: String

</td></tr><tr><td>

service.service\_relations.parent

</td><td>

Name of a parent CI related to the CI.Data type: String

</td></tr><tr><td>

service.url

</td><td>

Relative path to the application service. Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com/api/now/cmdb/app_service/2fce42d80a0a0bb4004af34d7e3984c8/getContent?mode=shallow" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

```
{
  "service": {
    "name": "PeopleSoft Portals",
    "url": "/api/now/table/cmdb_ci_service_discovered/2fce42d80a0a0bb4004af34d7e3984c8",
    "service_relations": [
      {
        "parent": "",
        "child": "3a2810c20a0a0bb400268337d6e942ca"
      },
      {
        "parent": "3a27f1520a0a0bb400ecd6ff7afcf036",
        "child": "3a5dd3dbc0a8ce0100655f1ec66ed42c"
      },
      {
        "parent": "3a290cc60a0a0bb400000bdb386af1cf",
        "child": "3a307c930a0a0bb400353965d0b8861f"
      },
      {
        "parent": "3a172e820a0a0bb40034228e9f65f1be",
        "child": "3a27d4370a0a0bb4006316812bf45439"
      },
      {
        "parent": "",
        "child": "3a172e820a0a0bb40034228e9f65f1be"
      },
      {
        "parent": "",
        "child": "3a27f1520a0a0bb400ecd6ff7afcf036"
      },
      {
        "parent": "3a2810c20a0a0bb400268337d6e942ca",
        "child": "3a290cc60a0a0bb400000bdb386af1cf"
      }
    ]
  },
  "cmdb": {
    "relations": [],
    "items": [
      {
        "values": {
          "sys_id": "3a172e820a0a0bb40034228e9f65f1be",
          "name": "PS LoadBal01"
        },
        "className": "cmdb_ci_win_server"
      },
      {
        "values": {
          "sys_id": "3a2810c20a0a0bb400268337d6e942ca",
          "name": "PS Apache03"
        },
        "className": "cmdb_ci_web_server"
      },
      {
        "values": {
          "sys_id": "55b35562c0a8010e01cff22378e0aea9",
          "name": "ny8500-nbxs08"
        },
        "className": "cmdb_ci_netgear"
      },
      {
        "values": {
          "sys_id": "3a27f1520a0a0bb400ecd6ff7afcf036",
          "name": "PS Apache02"
        },
        "className": "cmdb_ci_web_server"
      },
      {
        "values": {
          "sys_id": "3a307c930a0a0bb400353965d0b8861f",
          "name": "PS ORA01"
        },
        "className": "cmdb_ci_database"
      }
    ]
  }
}
```

## Application Service - GET /now/cmdb/csdm/app\_service/find\_service

Returns basic information about a specified application service and its associated business context.

**Note:** This endpoint has been deprecated, use [SG Services – POST /sg\_services/app\_service/find](sg_services-api.md#) instead.

### URL format

Default URL: `/api/now/cmdb/csdm/app_service/find_service`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Required, if **number** is not passed in. Name of the service for which to return information.Data type: String

Table: Service Instance \[cmdb\_ci\_service\_auto\]

</td></tr><tr><td>

number

</td><td>

Required, if **name** is not passed in. Unique number that identifies the application service for which to return information.Data type: String

Table: Service Instance \[cmdb\_ci\_service\_auto\]

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or they do not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error-appservice">

Describes an encountered error.Data type: Object

```
"error": {
  "details": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.details

</td><td id="entry-error-details-appservice">

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="entry-error-message-appservice">

Message describing the error.Data type: String

</td></tr><tr><td>

services

</td><td>

Array of objects, each object containing details of services associated with the specified application service. Data type: Array

 ```
"services": [
  {
    "environment": "String",
    "name": "String",
    "number": "String",
    "relationships": {Object},
    "sys_id": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

services.environment

</td><td>

Environment in which the application service is deployed, such as "Production" or "Test Lab 2." This can be any value that makes sense to the implementer.Data type: String

Maximum length: 40

Default: null

</td></tr><tr><td>

services.name

</td><td>

Required. Name of the application service. Must be a unique name from all other application services. Data type: String

Maximum length: 255

</td></tr><tr><td>

services.number

</td><td>

Unique number that identifies the application service. This value is initially generated by the endpoint.Data type: String

</td></tr><tr><td>

services.relationships

</td><td>

Service types associated with the application service. Data type: Object

 ```
"relationships": {
  "business_app": [Array],
  "business_service_offering": [Array],
  "technical_service_offering": [Array]
}
```

</td></tr><tr><td>

services.relationships.business\_app

</td><td>

List of sys\_ids of the business applications related to the application service.Data type: Array

</td></tr><tr><td>

services.relationships.technical\_service\_offering

</td><td>

List of sys\_ids of the technology management offerings \(formerly technical service offerings\) related to the application service.Data type: Array

</td></tr><tr><td>

services.relationships.business\_service\_offering

</td><td>

List of sys\_ids of the business service offerings related to the application service.Data type: Array

</td></tr><tr><td>

services.sys\_id

</td><td>

Sys\_id of the application service.Data type: String

</td></tr><tr><td>

services.version

</td><td>

Application service version number. Data type: String

Maximum length: 40

Format: User definable

Default: null

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X GET \
  https://instance.servicenow.com/api/now/cmdb/csdm/app_service/find_service?name=Email_East&number=SNSVC0001018 \
  -H 'Accept: application/json' \
  -u 'username':'password'

```

```
{
"result": {
  "services": [
    {
      "name": "Email_East",
      "number": "SNSVC0001018",
      "sys_id": "f809cb60db94101037740f95ca96190f",
      "environment": "Production",
      "version": "1.1.1",
      "relationships": {
        "business_app": [
          "658c7620db54101037740f95ca9619f2"
        ],
        "technical_service_offering": [],
        "business_service_offering": [
          "069c7e20db54101037740f95ca9619bf"
        ]
      }
    }
  ]
 }
}
```

## Application Service - POST /now/cmdb/app\_service/create

Creates an application service or update an existing application service.

### URL format

Default URL: `/api/now/cmdb/app_service/create`

### Supported request parameters

|Parameter|Description|
|---------|-----------|
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

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|

### Request body

The API accepts these JSON elements in the request body. In addition, you can add any field from the Mapped Application Service \[cmdb\_ci\_service\_discovered\] table to pass data to the application service record. For example, to add content to the Comments field, add `"comments": "Passing data to the Comments field"` to the JSON request.

|Element|Description|
|-------|-----------|
|name|Name of the application service you wish to create or update.|
|service\_relations|Information about CIs and the hierarchy they form. All CIs form pairs with a parent CI and a child CI. The top-level CI, referred to as the entry point of an application service, does not have a parent CI.|
|parent|Sys\_ id of the CI whose outgoing connection joins this CI with the CI at the lower level in the map hierarchy.|
|child|Sys\_ id of the CI whose incoming connection joins this CI with the CI located of the higher level in the map hierarchy.|

### Response body

The API returns these JSON elements in the response body.

<table id="table_mc1_pr1_tx"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

URL

</td><td>

URL of the standard table REST API for showing the sys\_id of an application service record. This element appears only if the endpoint is successful.

 Data type: String

</td></tr><tr><td>

getContentUrl

</td><td>

REST API path for getting the application service content. This element appears only if the endpoint is successful.

 Data type: String

</td></tr><tr><td>

info

</td><td>

Number of CIs added to the application service. This element appears only if the endpoint is successful.

 Data type: String

</td></tr><tr><td>

error

</td><td>

Error message details.This element appears only if the endpoint fails.

 Data type: Object

</td></tr><tr><td>

message

</td><td>

Error message describing the nature of the failure.This element appears only if the endpoint fails.

 Data type: String

</td></tr><tr><td>

status

</td><td>

States "failure" if the REST API fails.This element appears only if the endpoint fails.

 Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "http://<instance.servicenow.com>/api/now/cmdb/app_service/create" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
\"name\": \"myTestAppService\",
\"comments\": \"Passing data to the Comments field\",
\"service_relations\": [
{ \"parent\": \"\",
\"child\": \"3a70f789c0a8ce010091b0ea635b982a\"
},{ \"parent\": \"3a70f789c0a8ce010091b0ea635b982a\",
\"child\": \"b4fd7c8437201000deeabfc8bcbe5dc1\"
},{ \"parent\": \"b4fd7c8437201000deeabfc8bcbe5dc1\",
\"child\": \"53fdbc8437201000deeabfc8bcbe5d10\"
}
]
}" \
--user 'admin':'admin'
```

```
{
  "result": {
    "url": "/api/now/table/cmdb_ci_service_discovered/b1cff89fc9e19300964fcbb1ac3059a5",
    "getContentUrl": "/api/now/cmdb/app_service/b1cff89fc9e19300964fcbb1ac3059a5/getContent",
    "info": "3 CIs added to service"
  }
}
```

## Application Service - POST /now/cmdb/csdm/app\_service/register\_service

Creates an application service record stub in the Service Instance \[cmdb\_ci\_service\_auto\] table and populates it with the passed in information.

Before storing the record, it validates the passed parameters and the uniqueness of the application service name. It also creates upstream relationships which provide business context to the service by associating the specified business applications, business service offerings, and technology management offerings \(formerly technical service offerings\) to the service application. It does not create downstream relationships to infrastructure. To define downstream relationships you must call the Application Service - PUT /now/cmdb/csdm/app\_service/\{service\_sys\_id\}/populate\_service endpoint.

**Note:** This endpoint has been deprecated, use [SG Services – POST /sg\_services/app\_service/register](sg_services-api.md#) instead.

### URL format

Default URL: `/api/now/cmdb/csdm/app_service/register_service`

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

basic\_details

</td><td>

Required. Details of the service associated with the specified application service. Data type: Object

```
"basic_details": {
  "environment": "String",
  "name": "String",
  "version": "String"
}
```

</td></tr><tr><td>

basic\_details.environment

</td><td id="entry-basic_details-environment-appservice">

Environment in which the application service is deployed, such as "Production" or "Test Lab 2." This can be any value that makes sense to the implementer.Data type: String

Maximum length: 40

Default: null

</td></tr><tr><td>

basic\_details.name

</td><td id="entry-basic_details-name-appservice">

Required. Name of the application service. Must be a unique name from all other application services. Data type: String

Maximum length: 255

</td></tr><tr><td>

basic\_details.version

</td><td id="entry-basic_details-version-appservice">

Application service version number. Data type: String

Maximum length: 40

Format: User definable

Default: null

</td></tr><tr><td>

relationships

</td><td>

Upstream \(parent\) service types to associate with the application service.Data type: Object

```
"relationships": {
  "business_app": [Array],
  "business_service_offering": [Array],
  "technical_service_offering": [Array]
}
```

Table: CI Relationships \[cmdb\_rel\_ci\]

</td></tr><tr><td>

relationships.business\_app

</td><td id="entry-relationships-bus_app-appservice">

List of sys\_ids of the business applications to relate to the application service.Data type: Array

</td></tr><tr><td>

relationships.business\_service\_offering

</td><td id="entry-relationships-bus_srv_off-appservice">

List of sys\_ids of the business service offerings to relate to the application service.Data type: Array

</td></tr><tr><td>

relationships.technical\_service\_offering

</td><td id="entry-relationships-tech_srv_off-appservice">

List of sys\_ids of the technical service offerings to relate to the application service.Data type: Array

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

|Status code|Description|
|-----------|-----------|
|201|Successful. The application service was successfully registered.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or they do not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error-appservice">

Describes an encountered error.Data type: Object

```
"error": {
  "details": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.details

</td><td id="entry-error-details-appservice">

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="entry-error-message-appservice">

Message describing the error.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the application service. This number is generated by the endpoint.Data type: String

</td></tr><tr><td>

service\_sys\_id

</td><td>

Sys\_id of the registered application service.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X POST \
  https://instance.servicenow.com/api/now/cmdb/csdm/app_service/register_service \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password'
  -d '{
  "basic_details": {
    "environment": "Test Lab 2",
    "name": "Test Lab 2",
    "version": "1.1.1"
  },
  "relationships": {
    "business_app":["f07c7620db54101037740f95ca96199a"],
    "business_service_offering":["069c7e20db54101037740f95ca9619bf"]
  }
}'
```

```
{
  "result": {
    "service_sys_id": "80f21bbadbd410103d3a93c3e296199a",
    "number": "SNSVC0001018"    
  }
}
```

## Application Service - PUT /now/cmdb/csdm/app\_service/\{service\_sys\_id\}/populate\_service

Populates the specified application service with a specified set of downstream configuration items \(CI\).

Before calling this endpoint, you must call the [POST /now/cmdb/csdm/app\_service/register\_service](application-service-api.md#) endpoint to create the application service.

**Note:** This endpoint has been deprecated, use [SG Services – POST /sg\_services/app\_service/populate](sg_services-api.md#) instead.

### URL format

Default URL: `/api/now/cmdb/csdm/app_service/{service_sys_id}/populate_service`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

service\_sys\_id

</td><td>

Sys\_id of the application service to populate with the specified CIs.Data type: String

Table: Service Instance \[cmdb\_ci\_service\_auto\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

population\_method

</td><td>

CIs to associate with the specified application service. The elements in the **population\_method** object depend on the type of information being populated, which is defined by the **type** parameter.Data type: Object

For **type** = cmdb\_group\_based

```
"population_method": {
  "group_id": "String",
  "type": "String"
}
```

For **type** = discovery

**Note:** To use this type you must activate the Service Mapping \(com.snc.service-mapping\) plugin.

```
"population_method": {
  "attributes": [Array],
  "entry_point_id": "String",
  "type": "String"
}
```

For **type** = tag\_list

**Note:** To use this type you must activate the Service Mapping \(com.snc.service-mapping\) plugin.

```
"population_method": {
  "tags": [Array],
  "type": "String"
}
```

</td></tr><tr><td>

population\_method.attributes

</td><td>

List of attributes to associate with the CI, such as host, port, name, and URL.**Note:** You must pass all required attributes.

Data type: Array

```
"attributes": {
  "name":"String",
  "value":"String"
}
```

</td></tr><tr><td>

population\_method.attributes.name

</td><td>

Name of the attribute, such as host, port, name, and URL.Data type: String

</td></tr><tr><td>

population\_method.attributes.value

</td><td>

Attribute value.Data type: String

</td></tr><tr><td>

population\_method.entry\_point

</td><td>

Required if **population\_method.type** = discovery. Entry point into the application service. For additional information on entry points, see Entry point attributes and Create entry point types for Service Mapping.Data type: String

</td></tr><tr><td>

population\_method.group\_id

</td><td>

Required if **population\_method.type** = cmdb\_group\_based. Sys\_id of the group to associate with the CI.Data type: String

Title: CMDB Group \[cmdb\_group\]

</td></tr><tr><td>

population\_method.tags

</td><td>

List of tags to associate with the CI.Data type: Array of Objects

```
[
  "tags": {
    "tag": "String",
    "value": "String"
  }
]
```

Title: Key Values \[cmdb\_key\_value\]

</td></tr><tr><td>

population\_method.tags.tag

</td><td>

Name of the tag.Data type: String

</td></tr><tr><td>

population\_method.tags.value

</td><td>

Tag value.Data type: String

</td></tr><tr><td>

population\_method.type

</td><td>

Required. Type of CI to populate.Valid values:

-   cmdb\_group\_based
-   discovery
-   tag\_list

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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or they do not have the app\_service\_admin role.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error-appservice">

Describes an encountered error.Data type: Object

```
"error": {
  "details": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.details

</td><td id="entry-error-details-appservice">

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="entry-error-message-appservice">

Message describing the error.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

The following code example shows how to populate an application service when the CI type is cmdb\_group\_based.

```
curl -X PUT \
  https://instance.servicenow.com/api/now/cmdb/csdm/app_service/f809cb60db94101037740f95ca96190f/populate_service \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password' \
  -d '{
  "population_method": {
    "type":"cmdb_group_based",
    "group_id": "e809cf60db94101037640f95ca961932"
  }
}'
```

```
{
    "result": {}
}
```

The following code example shows how to populate a discovery application service.

```
curl -X PUT \
  https://instance.servicenow.com/api/now/cmdb/csdm/app_service/f809cb60db94101037740f95ca96190f/populate_service \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password' \
  -d '{
  "population_method": {
    "type":"discovery",
    "entry_point_id":"cmdb_ci_endpoint_ad_forest",
    "attributes": [
      {
        "name":"host",
        "value":"test1.com"
      },
      {
        "name":"port",
        "value":"500"
      },
      {
        "name":"protocol",
        "value":"ssh"
      }
    ]
  }
}'
```

```
{
    "result": {}
}
```

## Application Service - PUT /now/cmdb/csdm/app\_service/\{service\_sys\_id\}/service\_details

Updates the specified application service with the passed in basic information.

It also validates the uniqueness of the application service by checking the passed in information against the Identification and Reconciliation engine \(IRE\) rules defined on the application service class.

**Note:** This endpoint has been deprecated, use [SG Services – POST /sg\_services/app\_service/update](sg_services-api.md#) instead.

### URL format

Default URL: `/api/now/cmdb/csdm/app_service/{service_sys_id}/service_details`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

service\_sys\_id

</td><td>

Sys\_id of the application service to updated.Data type: String

Table: Service Instance \[cmdb\_ci\_service\_auto\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

basic\_details

</td><td id="entry-basic_details-appservice">

Details of the service associated with the specified application service. Data type: Object

```
"basic_details": {
  "environment": "String",
  "name": "String"
}
```

</td></tr><tr><td>

basic\_details.environment

</td><td id="entry-basic_details-environment-appservice">

Environment in which the application service is deployed, such as "Production" or "Test Lab 2." This can be any value that makes sense to the implementer.Data type: String

Maximum length: 40

Default: null

</td></tr><tr><td>

basic\_details.name

</td><td id="entry-basic_details-name-appservice">

Required. Name of the application service. Must be a unique name from all other application services. Data type: String

Maximum length: 255

</td></tr><tr><td>

relationships

</td><td id="entry-relationships-appservice">

Service types to associate with the application service. Located in the CI Relationships \[cmdb\_rel\_ci\] table.Data type: Object

```
"relationships": {
  "business_app": [Array],
  "business_service_offering": [Array],
  "technical_service_offering": [Array]
}
```

</td></tr><tr><td>

relationships.business\_app

</td><td id="entry-relationships-bus_app-appservice">

List of sys\_ids of the business applications to relate to the application service.Data type: Array

</td></tr><tr><td>

relationships.business\_service\_offering

</td><td id="entry-relationships-bus_srv_off-appservice">

List of sys\_ids of the business service offerings to relate to the application service.Data type: Array

</td></tr><tr><td>

relationships.technical\_service\_offering

</td><td id="entry-relationships-tech_srv_off-appservice">

List of sys\_ids of the technical service offerings to relate to the application service.Data type: Array

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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or they do not have the app\_service\_admin role.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error-appservice">

Describes an encountered error.Data type: Object

```
"error": {
  "details": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.details

</td><td id="entry-error-details-appservice">

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td id="entry-error-message-appservice">

Message describing the error.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X PUT \
  https://instance.servicenow.com/api/now/cmdb/csdm/app_service/f809cb60db94101037740f95ca96190f/service_details \
  -H 'Accept: application/json' \
  -H 'Content-Type: application/json' \
  -u 'username':'password' \
  -d '{
  "basic_details": {
    "environment": "Test Lab 2"
  },  "relationships": {
    "business_app" :["f07c7620db54101037740f95ca96199a"]
  }
}'
```

```
{
    "result": {}
}
```

