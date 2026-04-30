---
title: Wrap Up API
description: Provides endpoints for managing wrap-up functionality for external Contact Center as a Service \(CCaaS\) systems or ServiceNow AI Platform workspaces.Retrieves details for a specified wrap-up code.Retrieves details for a specified wrap-up segment.Retrieves details for a wrap-up segment based on a specified agent and interaction.Creates or updates wrap-up codes.Opens a wrap-up segment for an interaction.Updates and closes a wrap-up segment for an interaction.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-02-19"
reading_time_minutes: 34
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Wrap Up API

Provides endpoints for managing wrap-up functionality for external Contact Center as a Service \(CCaaS\) systems or ServiceNow AI Platform workspaces.

This API requires the Interactions Management \(com.glide.interaction.awa\) plugin. To call this API, you must have the interaction\_integration\_user role.

When agents close an interaction, the wrap-up feature enables them to enter closing details and wrap-up codes for future reference. For more information about wrap-up functionality, see [Wrap up overview](https://www.servicenow.com/docs/access?context=wrap-up-overview&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

To use this API for segmented wrap-up of interactions from external systems, you must implement the InteractionSegment scripted extension point to create and retrieve segment records in your chosen table. If you're using [OpenFrame](https://www.servicenow.com/docs/access?context=c_OpenFrameOverview&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), the extension point has an existing implementation to create and retrieve segment records in the Phone Log \[sn\_openframe\_phone\_log\] table.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Wrap Up - GET /now/wrapup/code/\{code\_id\}

Retrieves details for a specified wrap-up code.

### URL format

Versioned URL: `/api/now/{api_version}/wrapup/code/{code_id}`

Default URL: `/api/now/wrapup/code/{code_id}`

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

code\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

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

Object containing information about the API request and the wrap-up code.Data type: Object

```
"result": {
   "message": "String",
   "resultMap": {Object},
   "success": Boolean
}
```

</td></tr><tr><td>

result.message

</td><td id="message">

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

result.result\_map

</td><td>

Object containing the wrap-up code.Data type: Object

```
"result_map": {
   "wrap_up_code": {Object}
}
```

</td></tr><tr><td>

result.result\_map.wrap\_up\_code

</td><td>

Object with details about the wrap-up code.Data type: Object

```
"wrap_up_code": {
   "active": Boolean,
   "code": "String",
   "description": "String",
   "external": Boolean,
   "sys_id": "String",
   "translated_code": "String",
   "translated_description": "String"
}
```

</td></tr><tr><td>

result.result\_map.wrap\_up\_code.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

result.result\_map.wrap\_up\_code.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

result.result\_map.wrap\_up\_code.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

result.result\_map.wrap\_up\_code.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

result.result\_map.wrap\_up\_code.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

result.result\_map.wrap\_up\_code.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

result.result\_map.wrap\_up\_code.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

result.success

</td><td id="success">

Flag that indicates whether the API request was successfully processed.Valid values:

-   true: The API request was successful.
-   false: The API request failed.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

This example retrieves details for a specified wrap-up code.

```
curl "https://instance.service-now.com/api/now/v1/wrapup/code/49c27b679f201210c89656effa0a1cd7" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "message": "Wrap up code found.",
    "result_map": {
      "wrap_up_code": {
        "code": "Billing Issue",
        "description": "A code for billing issues",
        "active": true,
        "external": true,
        "sys_id": "49c27b679f201210c89656effa0a1cd7",
        "translated_code": "Abrechnungsproblem",
        "translated_description": "Ein code für Abrechnungsprobleme"
      }
    },
    "success": true
  }
}
```

## Wrap Up - GET /now/wrapup/segment/\{segment\_id\}

Retrieves details for a specified wrap-up segment.

### URL format

Versioned URL: `/api/now/{api_version}/wrapup/segment/{segment_id}`

Default URL: `/api/now/wrapup/segment/{segment_id}`

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

segment\_id

</td><td>

Sys\_id of the wrap-up segment in the Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\] table, or identifier representing the interaction segment on the external system. Data type: String

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_xpr_b42_42c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

segment

</td><td>

Object containing data about the interaction and wrap-up segment.Data type: Object

```
"segment": {
  "agent": "String",
  "awaiting_confirmation": Boolean,
  "confirmed_on": "String",
  "external": Boolean,
  "interaction": "String",
  "opened_on": "String",
  "segmented": Boolean,
  "segment_id": "String",
  "segment_table": "String",
  "state": "String",
  "submitted_on": "String",
  "sys_id": "String",
  "wrap_up_configuration": {Object} 
}
```

</td></tr><tr><td>

segment.agent

</td><td id="segment-agent">

Sys\_id of the agent assigned to the interaction.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

segment.awaiting\_confirmation

</td><td>

Flag that indicates whether the wrap-up segment submitted by the agent is awaiting confirmation that it was processed by the external CCaaS system.Valid values:

-   true: The wrap-up segment is awaiting confirmation.
-   false: The wrap-up segment was processed by the external system.

Data type: Boolean

</td></tr><tr><td>

segment.confirmed\_on

</td><td>

Date and time the submitted wrap-up segment is processed in the external CCaaS system.Data type: String

</td></tr><tr><td>

segment.external

</td><td>

Flag that indicates whether the interaction segment is from an external system.Valid values:

-   true: The interaction segment is from an external system.
-   false: The interaction segment is internal.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.interaction

</td><td id="interaction-id">

Sys\_id of the interaction.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

segment.opened\_on

</td><td>

The start date and time of the wrap-up period according to the external system.Data type: String

</td></tr><tr><td>

segment.segmented

</td><td>

Flag that indicates whether the wrap-up is segmented.Valid values:

-   true: The wrap-up is segmented into multiple parts.
-   false: The wrap-up is one complete segment.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.segment\_id

</td><td>

Sys\_id of the interaction segment.Data type: String

</td></tr><tr><td>

segment.segment\_table

</td><td>

Name of the table containing the interaction segment.Data type: String

</td></tr><tr><td>

segment.state

</td><td>

State of the interaction segment.Data type: String

</td></tr><tr><td>

segment.submitted\_on

</td><td>

Date and time the agent submitted the wrap-up segment.Data type: String

</td></tr><tr><td>

segment.sys\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr><tr><td>

segment.wrap\_up\_configuration

</td><td>

Object containing details about the wrap-up configuration used for the wrap-up segment.Data type: Object

```
"wrap_up_configuration": {  
  "allowed_codes": [Array],
  "default_code": {Object},
  "enable_codes": Boolean
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes

</td><td>

Array of objects each representing a wrap-up code the agent is allowed to use.Data type: Array

```
"allowed_codes": [
  {
    "active": Boolean, 
    "code": "String",
    "description": "String",
    "external": Boolean,
    "sys_id": "String",
    "translated_code": "String",
    "translated_description": "String"
  }
]
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code

</td><td>

Object containing the wrap-up code to use as the default.Data type: Object

```
"default_code": {
  "active": Boolean,
  "code": "String",
  "description": "String",
  "external": Boolean,
  "sys_id": "String",
  "translated_code": "String",
  "translated_description": "String"
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.enable\_codes

</td><td>

Flag that indicates whether the agent must select a wrap-up code.Valid values:

-   true: Agent must select a wrap-up code.
-   false: Agent isn't required to select a wrap-up code.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the API request was successfully processed.Valid values:

-   true: The API request was successful.
-   false: The API request failed.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

This example retrieves details for a specified wrap-up segment.

```
curl "https://instance.service-now.com/api/now/v1/wrapup/segment/dgajbcef12345678defdbxef123435678" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
  "success": true,
  "message": "Wrap up segment retrieved successfully.",
  "segment_id": "dgajbcef12345678defdbxef123435678",
  "segment": {
    "agent": "123412345678567890ab90abcdefcdef",
    "segment_table": "sn_openframe_phone_log",
    "segment_id": "dgajbcef12345678defdbxef123435678",
    "external": true,
    "interaction": "213412345678567890ab90abcdefcdef",
    "state": "closed",
    "wrap_up_configuration": {
      "enable_codes": true,
      "allowed_codes": [
        {
          "code": "Billing Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "49c27b679f201210c89656effa0a1cd7",
          "translated_code": "Abrechnungsproblem",
          "translated_description": ""
        },
        {
          "code": "Store Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "54327b679f201210c89656effa0a1cd7",
          "translated_code": " Einkaufsproblem",
          "translated_description": ""
        }
      ],
      "default_code": {
        "code": "Billing Issue",
        "description": "",
        "active": true,
        "external": true,
        "sys_id": "49c27b679f201210c89656effa0a1cd7",
        "translated_code": "Abrechnungsproblem",
        "translated_description": ""
      }
    },
    "segmented": true,
    "sys_id": "dgajbcef12345678defdbxef123435678",
    "opened_on": "2024-09-16 17:52:01",
    "submitted_on": "2024-09-16 18:51:59",
    "confirmed_on": "2024-09-16 18:52:01",
    "awaiting_confirmation": false
  }
}
```

## Wrap Up - GET /now/wrapup/segment/agent/\{agent\_id\}/interaction/\{interaction\_id\}

Retrieves details for a wrap-up segment based on a specified agent and interaction.

### URL format

Versioned URL: `/api/now/{api_version}/wrapup/segment/agent/{agent_id}/interaction/{interaction_id}`

Default URL: `/api/now/wrapup/segment/agent/{agent_id}/interaction/{interaction_id}`

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

agent\_id

</td><td>

Sys\_id of the agent assigned to the interaction.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

interaction\_id

</td><td>

Sys\_id of the interaction.Data type: String

Table: Interaction \[interaction\]

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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_xpr_b42_42c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

segment

</td><td>

Object containing data about the interaction and wrap-up segment.Data type: Object

```
"segment": {
  "agent": "String",
  "awaiting_confirmation": Boolean,
  "confirmed_on": "String",
  "external": Boolean,
  "interaction": "String",
  "opened_on": "String",
  "segmented": Boolean,
  "segment_id": "String",
  "segment_table": "String",
  "state": "String",
  "submitted_on": "String",
  "sys_id": "String",
  "wrap_up_configuration": {Object} 
}
```

</td></tr><tr><td>

segment.agent

</td><td id="segment-agent">

Sys\_id of the agent assigned to the interaction.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

segment.awaiting\_confirmation

</td><td>

Flag that indicates whether the wrap-up segment submitted by the agent is awaiting confirmation that it was processed by the external CCaaS system.Valid values:

-   true: The wrap-up segment is awaiting confirmation.
-   false: The wrap-up segment was processed by the external system.

Data type: Boolean

</td></tr><tr><td>

segment.confirmed\_on

</td><td>

Date and time the submitted wrap-up segment is processed in the external CCaaS system.Data type: String

</td></tr><tr><td>

segment.external

</td><td>

Flag that indicates whether the interaction segment is from an external system.Valid values:

-   true: The interaction segment is from an external system.
-   false: The interaction segment is internal.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.interaction

</td><td id="interaction-id">

Sys\_id of the interaction.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

segment.opened\_on

</td><td>

The start date and time of the wrap-up period according to the external system.Data type: String

</td></tr><tr><td>

segment.segmented

</td><td>

Flag that indicates whether the wrap-up is segmented.Valid values:

-   true: The wrap-up is segmented into multiple parts.
-   false: The wrap-up is one complete segment.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.segment\_id

</td><td>

Sys\_id of the interaction segment.Data type: String

</td></tr><tr><td>

segment.segment\_table

</td><td>

Name of the table containing the interaction segment.Data type: String

</td></tr><tr><td>

segment.state

</td><td>

State of the interaction segment.Data type: String

</td></tr><tr><td>

segment.submitted\_on

</td><td>

Date and time the agent submitted the wrap-up segment.Data type: String

</td></tr><tr><td>

segment.sys\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr><tr><td>

segment.wrap\_up\_configuration

</td><td>

Object containing details about the wrap-up configuration used for the wrap-up segment.Data type: Object

```
"wrap_up_configuration": {  
  "allowed_codes": [Array],
  "default_code": {Object},
  "enable_codes": Boolean
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes

</td><td>

Array of objects each representing a wrap-up code the agent is allowed to use.Data type: Array

```
"allowed_codes": [
  {
    "active": Boolean, 
    "code": "String",
    "description": "String",
    "external": Boolean,
    "sys_id": "String",
    "translated_code": "String",
    "translated_description": "String"
  }
]
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code

</td><td>

Object containing the wrap-up code to use as the default.Data type: Object

```
"default_code": {
  "active": Boolean,
  "code": "String",
  "description": "String",
  "external": Boolean,
  "sys_id": "String",
  "translated_code": "String",
  "translated_description": "String"
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.enable\_codes

</td><td>

Flag that indicates whether the agent must select a wrap-up code.Valid values:

-   true: Agent must select a wrap-up code.
-   false: Agent isn't required to select a wrap-up code.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the API request was successfully processed.Valid values:

-   true: The API request was successful.
-   false: The API request failed.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

This example retrieves details for a wrap-up segment based on a specified agent and interaction.

```
curl "https://instance.service-now.com/api/now/v1/wrapup/segment/agent/123412345678567890ab90abcdefcdef/interaction/213412345678567890ab90abcdefcdef" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
  "success": true,
  "message": "Wrap up segment retrieved successfully.",
  "segment_id": "dgajbcef12345678defdbxef123435678",
  "segment": {
    "agent": "123412345678567890ab90abcdefcdef",
    "segment_table": "sn_openframe_phone_log",
    "segment_id": "dgajbcef12345678defdbxef123435678",
    "external": true,
    "interaction": "213412345678567890ab90abcdefcdef",
    "state": "closed",
    "wrap_up_configuration": {
      "enable_codes": true,
      "allowed_codes": [
        {
          "code": "Billing Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "49c27b679f201210c89656effa0a1cd7",
          "translated_code": "Abrechnungsproblem",
          "translated_description": ""
        },
        {
          "code": "Store Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "54327b679f201210c89656effa0a1cd7",
          "translated_code": " Einkaufsproblem",
          "translated_description": ""
        }
      ],
      "default_code": {
        "code": "Billing Issue",
        "description": "",
        "active": true,
        "external": true,
        "sys_id": "49c27b679f201210c89656effa0a1cd7",
        "translated_code": "Abrechnungsproblem",
        "translated_description": ""
      }
    },
    "segmented": true,
    "sys_id": "dgajbcef12345678defdbxef123435678",
    "opened_on": "2024-09-16 17:52:01",
    "submitted_on": "2024-09-16 18:51:59",
    "confirmed_on": "2024-09-16 18:52:01",
    "awaiting_confirmation": false
  }
}
```

## Wrap Up - POST /now/wrapup/code

Creates or updates wrap-up codes.

Wrap-up codes are created in the Interaction Wrap Up Code \[interaction\_wrap\_up\_code\] table.

### URL format

Versioned URL: `/api/now/{api_version}/wrapup/code`

Default URL: `/api/now/wrapup/code`

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

codes

</td><td>

Required. Array of objects each representing a wrap-up code.Data type: Array

```
"codes": [
   {
      "active": Boolean,
      "code": "String",
      "description": "String",
      "translations": [Array]
   }
]
```

</td></tr><tr><td>

codes.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

codes.code

</td><td>

Required. Label of the wrap-up code.Data type: String

</td></tr><tr><td>

codes.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

codes.translations

</td><td>

Array of objects each representing a translation of the wrap-up code.Data type: Array

```
"translations": [
   {    
      "code": "Abrechnungsproblem",
      "description": "Ein code für Abrechnungsprobleme",
      "language": "de"
   }
]
```

</td></tr><tr><td>

codes.translations.code

</td><td>

A translation of the wrap-up code label \(**codes.code**\). Required if using the **codes.translations** parameter.Data type: String

</td></tr><tr><td>

codes.translations.description

</td><td>

A translation of the wrap-up code description \(**codes.description**\). Required if using the **codes.translations** parameter and a value was provided for **codes.description**.Data type: String

</td></tr><tr><td>

codes.translations.language

</td><td>

Two-letter code for the language used in the translation. Required if using the **codes.translations** parameter.Data type: String

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
|207|Successful. Some wrap-up codes created successfully. Validation errors occurred while creating others.|
|400|Bad Request. A bad request type or malformed request was detected.|
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

Object containing information about the API request and the created wrap-up codes.Data type: Object

```
"result": {
   "message": "String",
   "resultMap": {Object},
   "success": Boolean
}
```

</td></tr><tr><td>

result.message

</td><td id="message">

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

result.result\_map

</td><td>

Object containing an array of created wrap-up codes.Data type: Object

```
"result_map": {
   "created_wrap_up_codes": [Array]
}
```

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes

</td><td>

Array of objects each representing a created wrap-up code.Data type: Array

```
"created_wrap_up_codes": [
   {
      "active": Boolean,
      "code": "String",
      "description": "String",
      "external": Boolean,
      "sys_id": "String",
      "translated_code": "String",
      "translated_description": "String"
   }
]
```

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

result.result\_map.created\_wrap\_up\_codes.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

result.success

</td><td id="success">

Flag that indicates whether the API request was successfully processed.Valid values:

-   true: The API request was successful.
-   false: The API request failed.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

This example creates a wrap-up code for billing issues with a translation in German.

```
curl "https://instance.service-now.com/api/now/v1/wrapup/code" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"codes\": [
    {
      \"code\": \"Billing Issue\",
      \"description\": \"A code for billing issues\",
      \"translations\": [
        {
          \"language\": \"de\",
          \"code\": \"Abrechnungsproblem\",
          \"description\": \"Ein code für Abrechnungsprobleme\"
        }
      ]
    }
  ]
}" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "message": "All wrap up codes created successfully.",
    "result_map": {
      "created_wrap_up_codes": [
        {
          "code": "Billing Issue",
          "description": "A code for billing issues",
          "active": true,
          "external": true,
          "sys_id": "49c27b679f201210c89656effa0a1cd7",
          "translated_code": "Abrechnungsproblem",
          "translated_description": "Ein code für Abrechnungsprobleme"
        }
      ]
    },
    "success": true
  }
}
```

## Wrap Up - POST /now/wrapup/segment/create

Opens a wrap-up segment for an interaction.

Wrap-ups are created in the Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\] table.

### URL format

Versioned URL: `/api/now/{api_version}/wrapup/segment/create`

Default URL: `/api/now/wrapup/segment/create`

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

agent\_sys\_id

</td><td>

Required. Sys\_id of the agent assigned to the interaction.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

configuration

</td><td>

Object containing the code and duration details for an external wrap-up. Required if **external** is `true`.Data type: Object

```
"configuration": {  
   "allowed_codes": [Array], 
   "default_code": "String", 
   "duration": "String", 
   "enable_codes": Boolean,
   "show_timer": Boolean
}
```

</td></tr><tr><td>

configuration.allowed\_codes

</td><td>

Array of objects each representing a wrap-up code the agent is allowed to use. Required if **external** and **configuration.enable\_codes** are both `true`.Data type: Array

```
"allowed_codes": [ 
   { 
      "code": "String", 
      "translation": {Object}  
   } 
]
```

</td></tr><tr><td>

configuration.allowed\_codes.code

</td><td>

Label of the wrap-up code. Required if using the **configuration.allowed\_codes** parameter.Data type: String

</td></tr><tr><td>

configuration.allowed\_codes.translation

</td><td>

A translation of the wrap-up code.Data type: Object

```
"translation": {  
   "code": "String",
   "language": "String"  
}
```

</td></tr><tr><td>

configuration.allowed\_codes.translation.code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

configuration.allowed\_codes.translation.language

</td><td>

Two-letter code for the language used in the translation.Data type: String

</td></tr><tr><td>

configuration.default\_code

</td><td>

Label of the wrap-up code to use as the default. Required if **external** and **configuration.enable\_codes** are both `true`.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

Field: Code

</td></tr><tr><td>

configuration.duration

</td><td>

Maximum allowed wrap-up duration. Must be used with **show\_timer**.Data type: String

Unit: Seconds

Default: Empty string \(No time limit\).

</td></tr><tr><td>

configuration.enable\_codes

</td><td>

Flag that indicates whether the agent must select a wrap-up code.Valid values:

-   true: Agent must select a wrap-up code.
-   false: Agent isn't required to select a wrap-up code.

Data type: Boolean

Default: false

</td></tr><tr><td>

configuration.show\_timer

</td><td>

Required when using the duration property. Flag that indicates whether the timer displays.Valid values:

-   true: Timer displays in the UI.
-   false: Timer does not display in the UI.

Data type: Boolean

Default: false

</td></tr><tr><td>

external

</td><td id="external-seg">

Flag that indicates whether the interaction segment is from an external system.Valid values:

-   true: The interaction segment is from an external system.
-   false: The interaction segment is internal.

Data type: Boolean

Default: false

</td></tr><tr><td>

external\_segment\_id

</td><td>

Identifier representing the interaction segment on the external system. Required if **external** is `true`.Data type: String

</td></tr><tr><td>

interaction\_sys\_id

</td><td>

Required. Sys\_id of the interaction.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

opened\_on

</td><td>

The start date and time of the wrap-up period according to the external system. Required if using the **configuration.duration** parameter.Data type: String

</td></tr><tr><td>

segmented

</td><td>

Flag that indicates whether the wrap-up is segmented.Valid values:

-   true: The wrap-up is segmented into multiple parts.
-   false: The wrap-up is one complete segment.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment\_id

</td><td>

Sys\_id of the interaction segment. Required if **external** and **segmented** are both `true`.**Note:** You must implement the InteractionSegment scripted extension point to create and retrieve segment records in your chosen table or use the [OpenFrame](https://www.servicenow.com/docs/access?context=c_OpenFrameOverview&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) implementation to create and retrieve segment records in the Phone Log \[sn\_openframe\_phone\_log\] table.

Data type: String

</td></tr><tr><td>

segment\_table

</td><td>

Name of the table containing the interaction segment. Required if **external** and **segmented** are both `true`.Data type: String

</td></tr><tr><td>

wrap\_up\_configuration\_sys\_id

</td><td>

Sys\_id of the wrap-up configuration to use. Required if **external** is `false`.Data type: String

Table: Interaction Wrap Up Configuration \[interaction\_wrap\_up\_configuration\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_r5j_h1f_42c" class="rest_api_request_headers"><thead><tr><th>

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

segment

</td><td>

Object containing data about the interaction and wrap-up segment.Data type: Object

```
"segment": {
  "agent": "String",
  "external": Boolean,
  "interaction": "String",
  "opened_on": "String",
  "segmented": Boolean,
  "segment_id": "String",
  "segment_table": "String",
  "state": "String",
  "sys_id": "String",
  "wrap_up_configuration": {Object} 
}
```

</td></tr><tr><td>

segment.agent

</td><td>

Sys\_id of the agent assigned to the interaction segment.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

segment.external

</td><td>

Flag that indicates whether the interaction segment is from an external system.Valid values:

-   true: The interaction segment is from an external system.
-   false: The interaction segment is internal.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.interaction

</td><td>

Sys\_id of the interaction.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

segment.opened\_on

</td><td>

The start date and time of the wrap-up period according to the external system.Data type: String

</td></tr><tr><td>

segment.segmented

</td><td>

Flag that indicates whether the wrap-up is segmented.Valid values:

-   true: The wrap-up is segmented into multiple parts.
-   false: The wrap-up is one complete segment.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.segment\_id

</td><td>

Sys\_id of the interaction segment.Data type: String

</td></tr><tr><td>

segment.segment\_table

</td><td>

Name of the table containing the interaction segment.Data type: String

</td></tr><tr><td>

segment.state

</td><td>

State of the interaction segment. Interaction segments that the Wrap Up API creates successfully are in the open state.Data type: String

</td></tr><tr><td>

segment.sys\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr><tr><td>

segment.wrap\_up\_configuration

</td><td>

Object containing details about the wrap-up configuration used for the wrap-up segment.Data type: Object

```
"wrap_up_configuration": {  
  "allowed_codes": [Array],
  "default_code": {Object},
  "enable_codes": Boolean
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes

</td><td>

Array of objects each representing a wrap-up code the agent is allowed to use.Data type: Array

```
"allowed_codes": [
  {
    "active": Boolean, 
    "code": "String",
    "description": "String",
    "external": Boolean,
    "sys_id": "String",
    "translated_code": "String",
    "translated_description": "String"
  }
]
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code

</td><td>

Object containing the wrap-up code to use as the default.Data type: Object

```
"default_code": {
  "active": Boolean,
  "code": "String",
  "description": "String",
  "external": Boolean,
  "sys_id": "String",
  "translated_code": "String",
  "translated_description": "String"
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.enable\_codes

</td><td>

Flag that indicates whether the agent must select a wrap-up code.Valid values:

-   true: Agent must select a wrap-up code.
-   false: Agent isn't required to select a wrap-up code.

Data type: Boolean

Default: false

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the API request was successfully processed.Valid values:

-   true: The API request was successful.
-   false: The API request failed.

Data type: Boolean

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr></tbody>
</table>### cURL request

This example opens a wrap-up segment for an interaction.

```
curl "https://instance.service-now.com/api/now/v1/wrapup/segment/create" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"agent_sys_id\": \"123412345678567890ab90abcdefcdef\",
  \"interaction_sys_id\": \"213412345678567890ab90abcdefcdef\",
  \"external\": \"true\",
  \"segmented\": \"true\",
  \"segment_table\": \"sn_openframe_phone_log\",
  \"segment_id\": \"dgajbcef12345678defdbxef123435678\",
  \"external_segment_id\": \"PL_402548\",
  \"configuration\": {
    \"enable_codes\": true,
    \"allowed_codes\": [
      {
        \"code\": \"Billing Issue\",
        \"translation\": {
          \"language\": \"de\",
          \"code\": \"Abrechnungsproblem\"
        }
      },
      {
        \"code\": \"Store Issue\",
        \"translation\": {
          \"language\": \"de\",
          \"code\": \"Einkaufsproblem\"
        }
      }
    ],
    \"default_code\": \"Billing Issue\",
    \"duration\": \"30\",
    \"show_timer\": true
  },
  \"opened_on\": \"2024-09-16 17:52:01\"
}" \
--user 'username':'password'
```

Response body.

```
{
  "success": true,
  "message": "Open wrap-up segment successfully created.",
  "sys_id": "98769876543254321fed1fedcba0cba0",
  "segment": {
    "agent": "123412345678567890ab90abcdefcdef",
    "segment_table": "sn_openframe_phone_log",
    "segment_id": "dgajbcef12345678defdbxef123435678",
    "external": true,
    "interaction": "213412345678567890ab90abcdefcdef",
    "state": "open",
    "wrap_up_configuration": {
      "enable_codes": true,
      "allowed_codes": [
        {
          "code": "Billing Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "49c27b679f201210c89656effa0a1cd7",
          "translated_code": "Abrechnungsproblem",
          "translated_description": ""
        },
        {
          "code": "Store Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "54327b679f201210c89656effa0a1cd7",
          "translated_code": " Einkaufsproblem",
          "translated_description": ""
        }
      ],
      "default_code": {
        "code": "Billing Issue",
        "description": "",
        "active": true,
        "external": true,
        "sys_id": "49c27b679f201210c89656effa0a1cd7",
        "translated_code": "Abrechnungsproblem",
        "translated_description": ""
      }
    },
    "segmented": true,
    "sys_id": "98769876543254321fed1fedcba0cba0",
    "opened_on": "2024-09-16 17:52:01"
  }
}
```

## Wrap Up - PUT /now/wrapup/segment/update

Updates and closes a wrap-up segment for an interaction.

### URL format

Versioned URL: `/api/now/{api_version}/wrapup/segment/update`

Default URL: `/api/now/wrapup/segment/update`

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

agent\_sys\_id

</td><td>

Sys\_id of the agent assigned to the interaction. Required along with **interaction\_sys\_id** if neither **segment\_sys\_id** nor **external\_segment\_id** are provided.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

external\_segment\_id

</td><td>

Identifier representing the interaction segment on the external system. Used to identify the wrap-up segment to update if **segment\_sys\_id** isn't provided.

</td></tr><tr><td>

interaction\_sys\_id

</td><td>

Sys\_id of the interaction. Required along with **agent\_sys\_id** if neither **segment\_sys\_id** nor **external\_segment\_id** are provided.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

segment\_sys\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

confirmed\_on

</td><td>

The end date and time of the wrap-up period according to the external system.Data type: String

</td></tr><tr><td>

notes

</td><td>

Additional notes added to the wrap-up by the agent.Data type: String

</td></tr><tr><td>

wrap\_up\_code

</td><td>

Label of the wrap-up code selected by the agent. If the agent doesn't select a code, the configured default code is used.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

Field: Code

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_ubl_j1f_42c" class="rest_api_request_headers"><thead><tr><th>

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_xpr_b42_42c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message that describes the outcome of the API request.Data type: String

</td></tr><tr><td>

segment

</td><td>

Object containing data about the interaction and wrap-up segment.Data type: Object

```
"segment": {
  "agent": "String",
  "awaiting_confirmation": Boolean,
  "code": {Object},
  "confirmed_on": "String",
  "external": Boolean,
  "interaction": "String",
  "notes": "String",
  "opened_on": "String",
  "segmented": Boolean,
  "segment_id": "String",
  "segment_table": "String",
  "state": "String",
  "submitted_on": "String",
  "sys_id": "String",
  "wrap_up_configuration": {Object} 
}
```

</td></tr><tr><td>

segment.agent

</td><td id="segment-agent">

Sys\_id of the agent assigned to the interaction.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

segment.awaiting\_confirmation

</td><td>

Flag that indicates whether the wrap-up segment submitted by the agent is awaiting confirmation that it was processed by the external CCaaS system.Valid values:

-   true: The wrap-up segment is awaiting confirmation.
-   false: The wrap-up segment was processed by the external system.

Data type: Boolean

</td></tr><tr><td>

segment.code

</td><td>

Object containing the wrap-up code selected by the agent.Data type: Object

```
"code": {
  "active": Boolean,
  "code": "String",
  "description": "String",
  "external": Boolean,
  "sys_id": "String",
  "translated_code": "String",
  "translated_description": "String"
}
```

</td></tr><tr><td>

segment.code.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.code.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.code.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.code.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.code.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.code.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.code.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.confirmed\_on

</td><td>

Date and time the submitted wrap-up segment is processed in the external CCaaS system.Data type: String

</td></tr><tr><td>

segment.external

</td><td>

Flag that indicates whether the interaction segment is from an external system.Valid values:

-   true: The interaction segment is from an external system.
-   false: The interaction segment is internal.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.interaction

</td><td id="interaction-id">

Sys\_id of the interaction.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

segment.notes

</td><td>

Additional notes added to the wrap-up by the agent.Data type: String

</td></tr><tr><td>

segment.opened\_on

</td><td>

The start date and time of the wrap-up period according to the external system.Data type: String

</td></tr><tr><td>

segment.segmented

</td><td>

Flag that indicates whether the wrap-up is segmented.Valid values:

-   true: The wrap-up is segmented into multiple parts.
-   false: The wrap-up is one complete segment.

Data type: Boolean

Default: false

</td></tr><tr><td>

segment.segment\_id

</td><td>

Sys\_id of the interaction segment.Data type: String

</td></tr><tr><td>

segment.segment\_table

</td><td>

Name of the table containing the interaction segment.Data type: String

</td></tr><tr><td>

segment.state

</td><td>

State of the interaction segment. Interaction segments that this endpoint updates successfully are in the closed state.Data type: String

</td></tr><tr><td>

segment.submitted\_on

</td><td>

Date and time the agent submitted the wrap-up segment.Data type: String

</td></tr><tr><td>

segment.sys\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr><tr><td>

segment.wrap\_up\_configuration

</td><td>

Object containing details about the wrap-up configuration used for the wrap-up segment.Data type: Object

```
"wrap_up_configuration": {  
  "allowed_codes": [Array],
  "default_code": {Object},
  "enable_codes": Boolean
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes

</td><td>

Array of objects each representing a wrap-up code the agent is allowed to use.Data type: Array

```
"allowed_codes": [
  {
    "active": Boolean, 
    "code": "String",
    "description": "String",
    "external": Boolean,
    "sys_id": "String",
    "translated_code": "String",
    "translated_description": "String"
  }
]
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.allowed\_codes.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code

</td><td>

Object containing the wrap-up code to use as the default.Data type: Object

```
"default_code": {
  "active": Boolean,
  "code": "String",
  "description": "String",
  "external": Boolean,
  "sys_id": "String",
  "translated_code": "String",
  "translated_description": "String"
}
```

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.active

</td><td>

Flag that indicates whether the wrap-up code is active.Valid values:

-   true: The wrap-up code is active.
-   false: The wrap-up code isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.code

</td><td>

Label of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.description

</td><td>

Description of the wrap-up code.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.external

</td><td>

Flag that indicates whether the wrap-up code is from an external system.Valid values:

-   true: The wrap-up code is from an external system.
-   false: The wrap-up code is internal.

Data type: Boolean

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.sys\_id

</td><td>

Sys\_id of the wrap-up code.Data type: String

Table: Interaction Wrap Up Code \[interaction\_wrap\_up\_code\]

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_code

</td><td>

A translation of the wrap-up code label. Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.default\_code.translated\_description

</td><td>

A translation of the wrap-up code description.Data type: String

</td></tr><tr><td>

segment.wrap\_up\_configuration.enable\_codes

</td><td>

Flag that indicates whether the agent must select a wrap-up code.Valid values:

-   true: Agent must select a wrap-up code.
-   false: Agent isn't required to select a wrap-up code.

Data type: Boolean

Default: false

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the API request was successfully processed.Valid values:

-   true: The API request was successful.
-   false: The API request failed.

Data type: Boolean

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the wrap-up segment.Data type: String

Table: Interaction Wrap Up Segment \[interaction\_wrap\_up\_segment\]

</td></tr></tbody>
</table>### cURL request

This example updates and closes a wrap-up segment for an interaction.

```
curl "https://instance.service-now.com/api/now/v1/wrapup/segment/update?segment_sys_id=98769876543254321fed1fedcba0cba0&agent_sys_id=123412345678567890ab90abcdefcdef&interaction_sys_id=213412345678567890ab90abcdefcde" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"wrap_up_code\": \"Billing Issue\",
  \"notes\": \"Customer's credit card expired. Had to switch to another one.\",
  \"confirmed_on\": \"2024-09-16 18:52:01\"
}" \
--user 'username':'password'
```

Response body.

```
{
  "success": true,
  "message": "Wrap-up segment updated successfully.",
  "sys_id": "98769876543254321fed1fedcba0cba0",
  "segment": {
    "agent": "123412345678567890ab90abcdefcdef",
    "segment_table": "sn_openframe_phone_log",
    "segment_id": "dgajbcef12345678defdbxef123435678",
    "external": true,
    "interaction": "213412345678567890ab90abcdefcdef",
    "state": "closed",
    "wrap_up_configuration": {
      "enable_codes": true,
      "allowed_codes": [
        {
          "code": "Billing Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "49c27b679f201210c89656effa0a1cd7",
          "translated_code": "Abrechnungsproblem",
          "translated_description": ""
        },
        {
          "code": "Store Issue",
          "description": "",
          "active": true,
          "external": true,
          "sys_id": "54327b679f201210c89656effa0a1cd7",
          "translated_code": " Einkaufsproblem",
          "translated_description": ""
        }
      ],
      "default_code": {
        "code": "Billing Issue",
        "description": "",
        "active": true,
        "external": true,
        "sys_id": "49c27b679f201210c89656effa0a1cd7",
        "translated_code": "Abrechnungsproblem",
        "translated_description": ""
      }
    },
    "code": {
      "code": "Billing Issue",
      "description": "",
      "active": true,
      "external": true,
      "sys_id": "49c27b679f201210c89656effa0a1cd7",
      "translated_code": "Abrechnungsproblem",
      "translated_description": ""
    },
    "notes": "Customer's credit card expired. Had to switch to another one.",
    "segmented": true,
    "sys_id": "dgajbcef12345678defdbxef123435678",
    "opened_on": "2024-09-16 17:52:01",
    "submitted_on": "2024-09-16 18:51:59",
    "confirmed_on": "2024-09-16 18:52:01",
    "awaiting_confirmation": false
  }
}
```

