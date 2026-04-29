---
title: SAM-Software Usage Data Integration API
description: The SAM-Software Usage Data Integration API provides endpoints to create and update records in the Software Usage \[samp\_sw\_usage\] table.Creates or updates a specified record in the Software Usage \[samp\_sw\_usage\] table.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# SAM-Software Usage Data Integration API

The SAM-Software Usage Data Integration API provides endpoints to create and update records in the Software Usage \[samp\_sw\_usage\] table.

This API requires activation of the Software Asset Management Professional \(com.snc.samp\) plugin. It also requires that you have either the sam\_admin or sam\_developer role to access the endpoint.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## SAM-Software Usage Data Integration - POST /sam\_software\_usage\_integration/createOrUpdate

Creates or updates a specified record in the Software Usage \[samp\_sw\_usage\] table.

You can create/update one or more software usage records in a single call.

### URL format

Versioned URL: `/api/now/{api_version}/sam_software_usage_integration/createOrUpdate`

Default URL: `/api/now/sam_software_usage_integration/createOrUpdate`

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

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

items

</td><td>

List of column names and values for each field to store in the software usage record.The column information that you must pass depends on the value you specify for **reclamation\_type** \(which is a required field\):

 Possible **reclamation\_type** values and the column information that must be passed:

-   total\_usage:
    -   configuration\_item
    -   last\_used\_time
    -   month\_used
    -   norm\_product
    -   year
-   last\_used\_date:
    -   configuration\_item
    -   norm\_product

 The combination of these fields uniquely identify a record. If the record is not found in the table, a new record with the specified fields is created; otherwise the existing record is updated.

 Data type: Array

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
|405|Invalid method. The functionality is disabled.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

items

</td><td>

Name-value pair list of all fields in the software usage record.Data type: Array \(content varies\)

</td></tr></tbody>
</table>### cURL request

The following example illustrates how to create a new software usage record.

```
curl -X POST "https://instance.servicenow/api/now/sam_software_usage_integration/createOrUpdate" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d "{'items': [\
  {
    'configuration_item':'eaa9604d3790200044e0bfc8bcbe5dc1',\
    'month_used':2,\
    'norm_product':'40209c060b3022002d6c650d37673a89',\
    'norm_publisher':'24dcccc20b3022002d6c650d37673ab3',\
    'reclamation_type':'total_usage',\
    'usage_count': 13,\
    'total_usage_time':13,\
    'year':2020
  }\
]}"
```

```
{
  "result": {
    "reply": {
      "items": [
        {
          "configuration_item": "eaa9604d3790200044e0bfc8bcbe5dc1",
          "month_used": 2,
          "norm_product": "40209c060b3022002d6c650d37673a89",
          "norm_publisher": "24dcccc20b3022002d6c650d37673ab3",
          "reclamation_type": "total_usage",
          "usage_count": 13,
          "total_usage_time": 13,
          "year": 2020,
          "sysId": "13d15fe59d511010f8772c637e39afe5",
          "status": "INSERT"
        }
      ]
    },
    "message": "Ok"
  }
}
```

The following example illustrates how to update multiple software usage records in a single call.

```
curl -X POST "https://instance.servicenow/api/now/sam_software_usage_integration/createOrUpdate" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d "{'items': [\
  {\
    'configuration_item': 'eaa9604d3790200044e0bfc8bcbe5dc1',\
    'month_used': 2,\
    'norm_product': '40209c060b3022002d6c650d37673a89',\
    'norm_publisher': '24dcccc20b3022002d6c650d37673ab3',\
    'reclamation_type': 'total_usage',\
    'usage_count': 13,\
    'total_usage_time': 13,\
    'year': 2020
  },
  {\
    'configuration_item': '0aa9e80d3790200044e0bfc8bcbe5da0',\
    'month_used': 2,\
    'norm_product': '40209c060b3022002d6c650d37673a89',\
    'norm_publisher': '24dcccc20b3022002d6c650d37673ab3',\
    'reclamation_type': 'total_usage',\
    'usage_count': 19,\
    'total_usage_time': 19,\
    'year': 2020
  },
  {\
    'configuration_item': 'a0a9a80d3790200044e0bfc8bcbe5d3c',\
    'month_used': 2,\
    'norm_product': '40209c060b3022002d6c650d37673a89',\
    'norm_publisher': '24dcccc20b3022002d6c650d37673ab3',\
    'reclamation_type': 'total_usage',\
    'usage_count': 7,\
    'total_usage_time': 7,\
    'year': 2020},
  {\
    'configuration_item': '48a9280d3790200044e0bfc8bcbe5d55',\
    'month_used': 2,\
    'norm_product': '40209c060b3022002d6c650d37673a89',\
    'norm_publisher': '24dcccc20b3022002d6c650d37673ab3',\
    'reclamation_type': 'total_usage',\
    'usage_count': 1,\
    'total_usage_time': 1,\
    'year': 2020},
  {\
    'configuration_item': '61a9680d3790200044e0bfc8bcbe5d11',\
    'month_used': 2,\
    'norm_product': '40209c060b3022002d6c650d37673a89',\
    'norm_publisher': '24dcccc20b3022002d6c650d37673ab3',\
    'reclamation_type': 'total_usage',\
    'usage_count': 18,\
    'total_usage_time': 18,\
    'year': 2020}
]}"
```

```
{
  "result": {
    "reply": {
      "items": [
        {
          "configuration_item": "eaa9604d3790200044e0bfc8bcbe5dc1",
          "month_used": 2,
          "norm_product": "40209c060b3022002d6c650d37673a89",
          "norm_publisher": "24dcccc20b3022002d6c650d37673ab3",
          "reclamation_type": "total_usage",
          "usage_count": 13,
          "total_usage_time": 13,
          "year": 2020,
          "sysId": "13d15fe59d511010f8772c637e39afe5",
          "status": "INSERT"
        },
        {
          "configuration_item": "0aa9e80d3790200044e0bfc8bcbe5da0",
          "month_used": 2,
          "norm_product": "40209c060b3022002d6c650d37673a89",
          "norm_publisher": "24dcccc20b3022002d6c650d37673ab3",
          "reclamation_type": "total_usage",
          "usage_count": 19,
          "total_usage_time": 19,
          "year": 2020,
          "sysId": "2cd15fe59d521010f9772c637e39aff4",
          "status": "UPDATE"
        },
        {
          ...
        },
      ]
    },
    "message": "Ok"
  }
}
```

