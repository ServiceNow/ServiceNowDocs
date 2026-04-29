---
title: Interaction Management API
description: The Interaction Management API provides endpoints to create interactions.Inserts or updates a record in the interaction table.Changes the state of an interaction to closed or closed complete.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Interaction Management API

The Interaction Management API provides endpoints to create interactions.

This class requires the Interaction Logging, Routing, and Queueing plugin \(com.glide.interaction\).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Interaction - POST /now/interaction

Inserts or updates a record in the interaction table.

### URL format

Versioned URL: `/api/now/{api_version}/interaction`

Default URL: `/api/now/interaction`

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

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channel

</td><td>

Required. Sys\_id for the interaction connector you want to create an interaction for.Data type: String

</td></tr><tr><td>

context

</td><td>

A Map or a table/sys\_id pair. By default, interactions have a record in the interaction\_json\_blob table that stores context data as a JSON object. You can point an interaction to a different record for context. Use context or context\_table/context\_id to define the context for an interaction.Data type: String

</td></tr><tr><td>

context\_id

</td><td>

Document ID for a record you want to use to store context. The default is a new record in the insteraction\_json\_blob table. If you define the context ID, you also need to define the table.Data type: String

</td></tr><tr><td>

context\_table

</td><td>

Context table you want to use to store interaction context for. The default is interaction\_json\_blob. If you define the context table, you also need to define the context ID.Data type: String

</td></tr><tr><td>

channel\_metadata

</td><td>

Map or a table/sys\_id pair. Channel metadata contains information that a connector can use to communicate through the associated channel. Data type: String

</td></tr><tr><td>

channel\_metadata\_id

</td><td>

Document ID for a record you want to use to store channel metadata. The default is a new record in the live\_group\_profile table. If you define the channel metadata ID, you also need to define the table.Data type: String

</td></tr><tr><td>

channel\_metadata\_table

</td><td>

Table you want to use to store channel metadata. The default is the live\_group\_profile table. If you define the channel metadata table, you also need to define the channel metadata ID.Data type: String

</td></tr><tr><td>

queue

</td><td>

Sys\_id for the queue you want to associate with the interaction.Data type: String

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
|201|Indicates the query ran successfully.|
|400|Indicates that one or more mandatory parameters were missing from the request.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_bsj_y3z_cmb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assigned\_to

</td><td>

The sys\_id of the user the interaction is assigned to.Data type: String

</td></tr><tr><td>

channelMetadataDocument

</td><td>

The sys\_id of the channel metadata document associated with the interaction.Data type: String

</td></tr><tr><td>

channelMetadataTable

</td><td>

The table name of the channel metadata table associated with the interaction.Data type: String

</td></tr><tr><td>

channel\_metadata

</td><td>

Any channel metadata included for the interaction.Data type: String

</td></tr><tr><td>

closed\_by

</td><td>

The sys\_id of the user who closed the interaction.Data type: String

</td></tr><tr><td>

contextDocument

</td><td>

The sys\_id for the context document associated with the interaction.Data type: String

</td></tr><tr><td>

contextTable

</td><td>

The name of the table associated with the interaction.Data type: String

</td></tr><tr><td>

number

</td><td>

The number of the new interaction.Data type: String

</td></tr><tr><td>

opened\_for

</td><td>

The sys\_id of the user who the interaction was opened for.Data type: String

</td></tr><tr><td>

queue

</td><td>

The sys\_id for the queue you create the interaction for.Data type: String

</td></tr><tr><td>

state

</td><td>

The state the interaction is in. If you assign a queue, the state automatically changes to **Queued**, otherwise the default is **New**.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

The sys\_id of the interaction.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "http://instance.servicenow.com/api/now/interaction" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"channel\":\"28a59893873103002ae97e2526cb0b5d\",\"queue\":\"f3a50867b30303002186a72256a8dcb7\"}" \
--user "username":"password"
```

```
{
  "result": {
    "channel": "28a59893873103002ae97e2526cb0b5d",
    "context": {
      "present": true
    },
    "queue": "f3a50867b30303002186a72256a8dcb7",
    "state": "queued",
    "number": "IMS0000075",
    "contextDocument": "1863a6f0d9471300964f387107a8a36d",
    "contextTable": "interaction_json_blob",
    "channelMetadataDocument": "9463a6f0d9471300964f387107a8a36c",
    "channelMetadataTable": "live_group_profile",
    "channel_metadata": {
      "present": true
    },
    "sys_id": "dc63a6f0d9471300964f387107a8a36b",
    "assigned_to": "",
    "closed_by": "",
    "opened_for": ""
  }
}

```

## Interaction - POST /now/interaction/\{interaction\_id\}/close

Changes the state of an interaction to closed or closed complete.

### URL format

Versioned URL: `/api/now/{api_version}interaction/{interaction_id}/close`

Default URL: `/api/now/interaction/{interaction_id}/close`

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

interaction\_id

</td><td>

Sys\_id for the interaction you want to close.Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_ykz_y3z_cmb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assigned\_to

</td><td>

The sys\_id of the user the interaction is assigned to.Data type: String

</td></tr><tr><td>

channelMetadataDocument

</td><td>

The sys\_id of the channel metadata document associated with the interaction.Data type: String

</td></tr><tr><td>

channelMetadataTable

</td><td>

The table name of the channel metadata table associated with the interaction.Data type: String

</td></tr><tr><td>

channel\_metadata

</td><td>

Any channel metadata included for the interaction.Data type: String

</td></tr><tr><td>

closed\_by

</td><td>

The sys\_id of the user who closed the interaction.Data type: String

</td></tr><tr><td>

contextDocument

</td><td>

The sys\_id for the context document associated with the interaction.Data type: String

</td></tr><tr><td>

contextTable

</td><td>

The name of the table associated with the interaction.Data type: String

</td></tr><tr><td>

number

</td><td>

The number of the new interaction.Data type: String

</td></tr><tr><td>

opened\_for

</td><td>

The sys\_id of the user who the interaction was opened for.Data type: String

</td></tr><tr><td>

queue

</td><td>

The sys\_id for the queue you create the interaction for.Data type: String

</td></tr><tr><td>

state

</td><td>

The state the interaction is in. If you assign a queue, the state automatically changes to **Queued**, otherwise the default is **New**.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

The sys\_id of the interaction.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "http://instance.servicenow.com/api/now/interaction/b243cde4208f1700964f959e0488dee8/close" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "channel": "28a59893873103002ae97e2526cb0b5d",
    "context": {
      "present": true
    },
    "queue": "f3a50867b30303002186a72256a8dcb7",
    "state": "closed_complete",
    "number": "IMS0000060",
    "contextDocument": "3a43cde4208f1700964f959e0488dee7",
    "contextTable": "interaction_json_blob",
    "channelMetadataDocument": "fa43cde4208f1700964f959e0488dee8",
    "channelMetadataTable": "live_group_profile",
    "channel_metadata": {
      "present": true
    },
    "sys_id": "b243cde4208f1700964f959e0488dee8",
    "assigned_to": "",
    "closed_by": "6816f79cc0a8016401c5a33be04be441",
    "opened_for": "46d44a23a9fe19810012d100cca80666"
  }
}

```

