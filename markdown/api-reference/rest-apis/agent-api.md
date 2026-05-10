---
title: AWA Agent API
description: The AWA \(Advanced Work Assignment\) Agent API provides endpoints to manage agent presence, channel availability, and workload.Returns the current agent presence state and channel availability.Returns an agent's channel capacities, universal capacity, and the current workload to see if the agent can handle a case.Returns an agent's presence states and indicates whether the agent is available or in another presence state.Sets the state of a specified agent’s presence and, if provided, sets the agent’s channel availability for that state.Enables updating an agent's maximum capacity \(workload\) for channel capacities and universal capacity.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 23
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AWA Agent API

The AWA \(Advanced Work Assignment\) Agent API provides endpoints to manage agent presence, channel availability, and workload.

This API requires the Advanced Work Assignment \(com.glide.awa\) plugin and the awa\_integration\_user role. For more information, refer to [Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-overview.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AWA Agent - GET /now/awa/agents/\{user\_id\}

Returns the current agent presence state and channel availability.

### URL format

Versioned URL: `/api/now/{api_version}/awa/agents/{user_id}`

Default URL: `/api/now/awa/agents/{user_id}`

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

Sys\_id of the work item. The work item must meet the following criteria:

-   Work item must be assigned to the specified agent.
-   Work item must be in **Pending Accept** state.

Data type: String

Table: AWA Work Item \[awa\_work\_item\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

presence.channels.available

</td><td id="row-presence_channels_avil-awa">

Flag that indicates whether the channel is available. Possible values:

-   true: Channel is available.
-   false: Channel isn't available.

Data type: Boolean

</td></tr><tr><td>

presence.channels.sys\_id

</td><td id="entry-presence_channels_sys_id-awa">

Channel sys\_id. Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr><td>

presence.sys\_id

</td><td id="entry-presence_sys_id-awa">

Presence state sys\_id. Data type: String

Table: Presence States \[awa\_presence\_state\]

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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/installed-with-awa.md).

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_r2q_fbm_cmb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="awa-api-entry-error">

Details describing an error encountered during the request process.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process. Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. Each error message has a corresponding description in the **detail** property.Possible values:

-   `Record Not Found`: Information provided in the request body is inaccurate or doesn't exist.
-   `User Not Authenticated`: User doesn't have the awa\_integration\_user role.

Data type: String

</td></tr><tr id="row-presence-awa"><td>

presence

</td><td id="entry-presence-awa">

Information about an agent's current presence state and channel. Data type: Object

```
"presence": {
  "available": Boolean,
  "channels": [Array],
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="row-presence_available-awa"><td>

presence.available

</td><td id="entry-presence_available-awa">

Flag that indicates whether the agent is available. Possible values:

-   true: Agent is available.
-   false: Agent isn't available.

Data type: Boolean

</td></tr><tr id="row-presence_channels-awa"><td>

presence.channels

</td><td id="entry-presence_channels-awa">

List of objects that describe the available channels of communication with the agent. Data type: Array of Objects

```
"channels": [
  {
    "available": Boolean,
    "name": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr id="row-channels-avail"><td>

presence.channels.available

</td><td id="d3035e337">

Flag that indicates whether the channel is available. Possible values:

-   true: Channel is available.
-   false: Channel isn't available.

Data type: Boolean

</td></tr><tr id="row-presence_channels_name-awa"><td>

presence.channels.name

</td><td id="entry-presence_channels_name-awa">

Channel name, such as Chat or Phone. Data type: String

</td></tr><tr><td>

presence.channels.restrict\_update

</td><td>

Flag that indicates whether the user can restrict updates, that is, select the channel for availability.Possible values:

-   true: The user can select this channel for availability.
-   false: The user can't select this channel for availability.

Data type: Boolean

</td></tr><tr><td>

presence.channels.service\_channel\_type

</td><td>

Service channel type, such as chat. Possible values vary depending on plugins installed.Data type: String

</td></tr><tr id="row-channels-sysid"><td>

presence.channels.sys\_id

</td><td id="d3035e405">

Channel sys\_id. Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr id="row-presence_name-awa"><td>

presence.name

</td><td id="entry-presence_name-awa">

Name of the agent's presence state. Possible values:

-   Available
-   Unavailable

Data type: String

</td></tr><tr id="row-presence_restrict_update-awa"><td>

presence.restrict\_update

</td><td id="entry-presence_restrict_update-awa">

Flag that indicates whether the user can restrict updates. Possible values:

-   true: User can restrict updates.
-   false: User can't restrict updates.

Data type: Boolean

</td></tr><tr id="row-presence-sysid"><td>

presence.sys\_id

</td><td id="d3035e467">

Presence state sys\_id. Data type: String

Table: Presence States \[awa\_presence\_state\]

</td></tr><tr><td>

status

</td><td id="awa-api-entry_status">

Status of an unsuccessful request. This property is only included in the response if there is an error.Valid value: `failure`

Data type: String

</td></tr><tr id="row-sys_id-awa"><td>

sys\_id

</td><td id="entry-sys_id-awa">

Agent sys\_id. Data type: String

</td></tr><tr><td>

workItem

</td><td>

**workItem**: Information about the work item that is associated with the event.

 Data type: String

</td></tr><tr><td>

workItem.document

</td><td>

**workItem.document**: List of documents associated with the work item task.Data type: String

</td></tr><tr><td>

workItem.document.sys\_id

</td><td>

**workItem.document.sys\_id**: Sys\_id of the document assigned to the work item task.Data type: String

</td></tr><tr><td>

workItem.document.table

</td><td>

**workItem.document.table**: Name of the document table assigned to the task.Data type: String

</td></tr><tr><td>

workItem.previousWorkItem

</td><td>

**workItem.previousWorkItem**: Sys\_id of the previous work item for the same document ID. For the non-transfer work items this value is empty.Data type: String

</td></tr><tr><td>

workItem.serviceChannel

</td><td>

**workItem.serviceChannel**: List of service channels associated with the work item task.Data type: String

</td></tr><tr><td>

workItem.serviceChannel.name

</td><td>

**workItem.serviceChannel.name**: Name of the service channel, such as Chat or Phone.Data type: String

</td></tr><tr><td>

workItem.serviceChannel.sys\_id

</td><td>

**workItem.serviceChannel.sys\_id**: Sys\_id of the service channel.Data type: String

</td></tr><tr><td>

workItem.size

</td><td>

**workItem.size**: Agent's capacity used when this work item is assigned to the agent.Data type: String

</td></tr><tr><td>

workItem.sys\_id

</td><td>

**workItem.sys\_id**: Sys\_id of the work item that was accepted or offered.Data type: String

</td></tr><tr><td>

workItem.isQueueTransferred

</td><td>

**workItem.isQueueTransferred**: Flag that indicates whether the work item is queue transferred. Set to true if the work item is queue transferred, false if it isn't.Data type: Boolean

</td></tr><tr><td>

workitem.isAutoAccepted

</td><td>

**workItem.isAutoAccepted**: Flag that indicates whether the work item was automatically accepted by the system. Set to true if the work item was auto-accepted.Data type: Boolean

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X GET \
https://instance.servicenow.com/api/now/awa/agents/46d44a23a9fe19810012d100cca80666 \
-H 'Accept: application/json' \
-H 'Content-Type: application/json' \
-u 'username':'password'\
```

```
{
  "result": {
    "presence": {
      "name": "Available",
      "sys_id": "0b10223c57a313005baaaa65ef94f970",
      "available": true,
      "channels": [
        {
          "name": "Chat",
          "available": true,
          "sys_id": "27f675e3739713004a905ee515f6a7c3"
        }
      ]
    },
    "sys_id": "46d44a23a9fe19810012d100cca80666"
  }
}
```

## AWA Agent - GET /now/awa/agents/\{user\_id\}/capacities

Returns an agent's channel capacities, universal capacity, and the current workload to see if the agent can handle a case.

Use the [AWA Agent - PUT /now/awa/agents/\{user\_id\}/capacities](agent-api.md#) method to modify the channel and universal capacities of an agent.

See also:

-   [Service channel capacity and utilization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-service-channel-capacity.md)
-   [Create or configure a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-service-channel.md)
-   [Configure an agent's maximum universal capacity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-universal-capacity.md)

### URL format

Versioned URL: `/api/now/{api_version}/awa/agents/{user_id}/capacities`

Default URL: `/api/now/awa/agents/{user_id}/capacities`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table id="table_wg3_ydq_htb" class="rest_api_path_parameters"><thead><tr><th>

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

Sys\_id of the agent listed.Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None||

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_ah3_ydq_htb" class="rest_api_request_headers"><thead><tr><th>

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

<table id="table_dh3_ydq_htb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/installed-with-awa.md).

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_bgk_dmp_htb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channels

</td><td>

List of objects that describe the available channels of communication with the agent. ```
"channels": [
  {
    "channel_sys_id": "String",
    "current_workload": Number,
    "max_capacity": Number
  }
]
```

 Data type: Array

</td></tr><tr><td>

channels.channel\_sys\_id

</td><td>

Channel sys\_id. Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr><td>

channels.current\_workload

</td><td>

Number of work items on a specific service channel currently assigned to the agent.Data type: Number

</td></tr><tr><td>

channels.max\_capacity

</td><td>

Maximum workload on a specific service channel that the agent can be actively assigned to at a time. Data type: String

</td></tr><tr id="ordr-row-error"><td>

error

</td><td>

Details describing an error encountered during the request process.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process. Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. The description is provided in the **error.detail** property.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request. This property is only included in the response if there is an error.Valid value: `failure`

Data type: String

</td></tr><tr><td>

universal\_capacity

</td><td>

Maximum capacity for the agent across all service channels. If an agent's current workload equals the maximum universal capacity, additional work items won't be assigned to the agent. This property only returns if a universal capacity record exists for this agent.

Data type: Number

</td></tr><tr><td>

universal\_workload

</td><td>

Number of work items across all service channels currently assigned to the specified agent.This property only returns if a universal capacity record exists for the agent.

 Data type: Number

</td></tr></tbody>
</table>### Sample cURL request

The following example shows how to get the capacity and workload values for a user.

```
curl "https://instance.service-now.com/api/now/awa/agents/46d44a23a9fe19810012d100cca80666/capacities" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

A successful response includes capacity values and workload for each channel.

```
{
  "result": {
    "universal_workload": 2,
    "channels": [
      {
        "channel_sys_id": "27f675e3739713004a905ee515f6a7c3",
        "current_workload": 2,
        "max_capacity": 4
      }
    ],
    "universal_capacity": 10
  }
}
```

## AWA Agent - GET /now/awa/agents/\{user\_id\}/presence\_states

Returns an agent's presence states and indicates whether the agent is available or in another presence state.

### URL format

Versioned URL: `/api/now/{api_version}/awa/agents/{user_id}/presence_states`

Default URL: `/api/now/awa/agents/{user_id}/presence_states`

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

Sys\_id of the agent listed.Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None||

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

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/installed-with-awa.md).

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_bgk_dmp_htb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="ordr-row-error"><td>

error

</td><td>

Details describing an error encountered during the request process.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process. Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. The description is provided in the **error.detail** property.Data type: String

</td></tr><tr><td>

&lt;presence state&gt;

</td><td>

List of the agent's presence state definitions as objects. Each object describes the state and includes the agent's channels.Data type: Array

 ```
{
  "available": Boolean,
  "channels": [Array],
  "disable_inactivity_check": Boolean,
  "name": "String",
  "show_channels": Boolean,
  "sys_id": "String"
}
```

</td></tr><tr><td>

&lt;presence state&gt;.available

</td><td>

Flag that indicates whether the agent is available. Possible values:

-   true: Agent is available.
-   false: Agent isn't available.

Data type: Boolean

</td></tr><tr><td>

&lt;presence state&gt;.channels

</td><td>

List of objects that describe the available channels of communication with the agent. Data type: Array

 ```
"channels": [
 {
  "available": Boolean,
  "name": "String",
  "restrict_update": Boolean,
  "service_channel_type": "String",
  "sys_id": "String"
 }
]
```

</td></tr><tr><td>

&lt;presence state&gt;.channels.available

</td><td>

Flag that indicates whether the channel is available. Possible values:

-   true: Channel is available.
-   false: Channel isn't available.

Data type: Boolean

</td></tr><tr><td>

&lt;presence state&gt;.channels.name

</td><td>

Channel name, such as Chat or Phone. Data type: String

</td></tr><tr><td>

&lt;presence state&gt;.channels.sys\_id

</td><td>

Channel sys\_id. Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr><td>

&lt;presence state&gt;.disable\_inactivity\_check

</td><td>

Flag that indicates whether to check for inactivity of this presence state.Valid values:

-   true: The presence state inactivity check is disabled.
-   false: The presence state inactivity check is enabled.

 Data type: Boolean

 Default: false

 For information on how to modify this setting, see [Configure agent presence states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-configure-agent-presence.md).

</td></tr><tr><td>

&lt;presence state&gt;.name

</td><td>

Name of the agent's presence state. The presence states installed by default are `Available`, `Away`, and `Offline`.Data type: String

</td></tr><tr><td>

&lt;presence state&gt;.order

</td><td>

Order in which this state is displayed in the agent inbox.Data type: Number

</td></tr><tr><td>

&lt;presence state&gt;.show\_channels

</td><td>

Flag that indicates whether the agent has permission to change presence state, for example, from available to away.Valid values:

-   true: The user has permission to change the presence.
-   false: The user is restricted from changing the presence.

 Data type: Boolean

</td></tr><tr><td>

&lt;presence state&gt;.sys\_id

</td><td>

Presence state sys\_id. Data type: String

Table: Presence States \[awa\_presence\_state\]

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request. This property is only included in the response if there is an error.Valid value: `failure`

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

The following example shows how to get the presence states for a specified agent.

```
curl "https://instance.service-now.com/api/now/awa/agents/46d44a23a9fe19810012d100cca80666/presence_states" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

The response body lists the agent's possible presence states and indicates that the agent is available.

```
{
  "result": [
    {
      "name": "Available",
      "order": 0,
      "show_channels": false,
      "sys_id": "0b10223c57a313005baaaa65ef94f970",
      "available": true,
      "channels": [
        {
          "name": "Chat",
          "available": true,
          "sys_id": "27f675e3739713004a905ee515f6a7c3",
          "restrict_update": false,
          "service_channel_type": "chat"
        }
      ],
      "disable_inactivity_check": false
    },
    {
      "name": "Away",
      "order": 1000,
      "show_channels": false,
      "sys_id": "41f9b8dfb31313005baa6e5f26a8dcac",
      "available": false,
      "channels": [],
      "disable_inactivity_check": false
    },
    {
      "name": "Offline",
      "order": 2000,
      "show_channels": false,
      "sys_id": "9cd83267575313005baaaa65ef94f98b",
      "available": false,
      "channels": [],
      "disable_inactivity_check": false
    }
  ]
}
```

## AWA Agent - PUT /now/awa/agents/\{user\_id\}

Sets the state of a specified agent’s presence and, if provided, sets the agent’s channel availability for that state.

### URL format

Versioned URL: `/api/now/{api_version}/awa/agents/{user_id}`

Default URL: `/api/now/awa/agents/{user_id}`

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

Sys\_id of the agent.Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

presence.channels

</td><td>

List of objects that define which channels are available for the agent.Data type: Array of Objects

```
"channels": [
  { 
    "available": Boolean,
    "sys_id": "String"
  }
] 
```

</td></tr><tr><td>

presence.channels.available

</td><td>

Flag that indicates whether the channel is available. Possible values:

-   true: Channel is available.
-   false: Channel isn't available.

**Note:** This setting must be specified to include channels in the response body.

Data type: Boolean

Default: false

</td></tr><tr><td>

presence.channels.sys\_id

</td><td id="entry-presence_channels_sys_id-awa">

Channel sys\_id. Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr><td>

presence.sys\_id

</td><td id="entry-presence_sys_id-awa">

Presence state sys\_id. Data type: String

Table: Presence States \[awa\_presence\_state\]

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

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code-awa">

Forbidden.Possible reasons:

-   The user doesn't have the awa\_integration\_user role.
-   The value of the glide.awa.enabled property isn't `true`. This property is listed in the System Property \[sys\_property\] table if the Advanced Work Assignment \(com.glide.awa\) plugin is installed. For more information, see [Components installed with Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/installed-with-awa.md).

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table><table id="table_rcs_b2m_cmb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="awa-api-entry-error">

Details describing an error encountered during the request process.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process. Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. Each error message has a corresponding description in the **detail** property.Possible values:

-   `Record Not Found`: Information provided in the request body is inaccurate or doesn't exist.
-   `User Not Authenticated`: User doesn't have the awa\_integration\_user role.

Data type: String

</td></tr><tr id="row-presence-awa"><td>

presence

</td><td id="entry-presence-awa">

Information about an agent's current presence state and channel. Data type: Object

```
"presence": {
  "available": Boolean,
  "channels": [Array],
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr id="row-presence_available-awa"><td>

presence.available

</td><td id="entry-presence_available-awa">

Flag that indicates whether the agent is available. Possible values:

-   true: Agent is available.
-   false: Agent isn't available.

Data type: Boolean

</td></tr><tr id="row-presence_channels-awa"><td>

presence.channels

</td><td id="entry-presence_channels-awa">

List of objects that describe the available channels of communication with the agent. Data type: Array of Objects

```
"channels": [
  {
    "available": Boolean,
    "name": "String",
    "sys_id": "String"
  }
]
```

</td></tr><tr id="row-channels-avail"><td>

presence.channels.available

</td><td id="row-presence_channels_avil-awa">

Flag that indicates whether the channel is available. Possible values:

-   true: Channel is available.
-   false: Channel isn't available.

Data type: Boolean

</td></tr><tr id="row-presence_channels_name-awa"><td>

presence.channels.name

</td><td id="entry-presence_channels_name-awa">

Channel name, such as Chat or Phone. Data type: String

</td></tr><tr><td>

presence.channels.restrict\_update

</td><td>

Flag that indicates whether the user can restrict updates, that is, select the channel for availability.Possible values:

-   true: The user can select this channel for availability.
-   false: The user can't select this channel for availability.

Data type: Boolean

</td></tr><tr><td>

presence.channels.service\_channel\_type

</td><td>

Service channel type, such as chat. Possible values vary depending on plugins installed.Data type: String

</td></tr><tr id="row-channels-sysid"><td>

presence.channels.sys\_id

</td><td id="d3035e405">

Channel sys\_id. Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr id="row-presence_name-awa"><td>

presence.name

</td><td id="entry-presence_name-awa">

Name of the agent's presence state. Possible values:

-   Available
-   Unavailable

Data type: String

</td></tr><tr id="row-presence_restrict_update-awa"><td>

presence.restrict\_update

</td><td id="entry-presence_restrict_update-awa">

Flag that indicates whether the user can restrict updates. Possible values:

-   true: User can restrict updates.
-   false: User can't restrict updates.

Data type: Boolean

</td></tr><tr id="row-presence-sysid"><td>

presence.sys\_id

</td><td id="d3035e467">

Presence state sys\_id. Data type: String

Table: Presence States \[awa\_presence\_state\]

</td></tr><tr><td>

status

</td><td id="awa-api-entry_status">

Status of an unsuccessful request. This property is only included in the response if there is an error.Valid value: `failure`

Data type: String

</td></tr><tr id="row-sys_id-awa"><td>

sys\_id

</td><td id="entry-sys_id-awa">

Agent sys\_id. Data type: String

</td></tr><tr><td>

workItem

</td><td>

**workItem**: Information about the work item that is associated with the event.

 Data type: String

</td></tr><tr><td>

workItem.document

</td><td>

**workItem.document**: List of documents associated with the work item task.Data type: String

</td></tr><tr><td>

workItem.document.sys\_id

</td><td>

**workItem.document.sys\_id**: Sys\_id of the document assigned to the work item task.Data type: String

</td></tr><tr><td>

workItem.document.table

</td><td>

**workItem.document.table**: Name of the document table assigned to the task.Data type: String

</td></tr><tr><td>

workItem.previousWorkItem

</td><td>

**workItem.previousWorkItem**: Sys\_id of the previous work item for the same document ID. For the non-transfer work items this value is empty.Data type: String

</td></tr><tr><td>

workItem.serviceChannel

</td><td>

**workItem.serviceChannel**: List of service channels associated with the work item task.Data type: String

</td></tr><tr><td>

workItem.serviceChannel.name

</td><td>

**workItem.serviceChannel.name**: Name of the service channel, such as Chat or Phone.Data type: String

</td></tr><tr><td>

workItem.serviceChannel.sys\_id

</td><td>

**workItem.serviceChannel.sys\_id**: Sys\_id of the service channel.Data type: String

</td></tr><tr><td>

workItem.size

</td><td>

**workItem.size**: Agent's capacity used when this work item is assigned to the agent.Data type: String

</td></tr><tr><td>

workItem.sys\_id

</td><td>

**workItem.sys\_id**: Sys\_id of the work item that was accepted or offered.Data type: String

</td></tr><tr><td>

workItem.isQueueTransferred

</td><td>

**workItem.isQueueTransferred**: Flag that indicates whether the work item is queue transferred. Set to true if the work item is queue transferred, false if it isn't.Data type: Boolean

</td></tr><tr><td>

workitem.isAutoAccepted

</td><td>

**workItem.isAutoAccepted**: Flag that indicates whether the work item was automatically accepted by the system. Set to true if the work item was auto-accepted.Data type: Boolean

</td></tr></tbody>
</table>```
curl -X PUT \
 https://instance.servicenow.com/api/now/awa/agents/46d44a23a9fe19810012d100cca80666 \
-H 'Accept: application/json' \
-H 'Content-Type: application/json' \
-u 'username':'password'\
-d '{"presence": {\
  "sys_id": "0b10223c57a313005baaaa65ef94f970",\
  "channels": [{ \
  "sys_id": "0bbdedbb3b892300a2bac9bb34efc445",\
  "available": true
}] 
}}
```

```
{
  "result": {
    "presence": {
      "name": "Available",
      "sys_id": "0b10223c57a313005baaaa65ef94f970",
      "available": true,
      "channels": [
        {
          "name": "Chat",
          "available": true,
          "sys_id": "27f675e3739713004a905ee515f6a7c3"
        }
      ]
    },
    "sys_id": "46d44a23a9fe19810012d100cca80666"
  }
}
```

## AWA Agent - PUT /now/awa/agents/\{user\_id\}/capacities

Enables updating an agent's maximum capacity \(workload\) for channel capacities and universal capacity.

Use the [AWA Agent - GET /now/awa/agents/\{user\_id\}/capacities](agent-api.md#) method to retrieve the current channel and universal capacities of an agent.

See also:

-   [Service channel capacity and utilization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-service-channel-capacity.md)
-   [Create or configure a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-service-channel.md)
-   [Configure an agent's maximum universal capacity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-universal-capacity.md)

### URL format

Versioned URL: `/api/now/{api_version}/awa/agents/{user_id}/capacities`

Default URL: `/api/now/awa/agents/{user_id}/capacities`

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

Sys\_id of the agent listed.Data type: String

Table: User \[sys\_user\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channels

</td><td>

Mandatory if updating the maximum value of one or more channels for the specified agent. JSON object containing one or more key-value pairs mapping the channel to its maximum capacity for each channel assigned to the agent.Data type: Object

 The pair is in the following format:

-   Key \(channel sys\_id\) – Channel sys\_id.

Data type: String

-   Value \(maximum capacity\) – Maximum workload on a specific service channel that the agent can be actively assigned to at a time.

Data type: Number


 ```
channels: {"<channel_sys_id>": <max_capacity>}
```

</td></tr><tr><td>

universal\_capacity

</td><td>

Mandatory if universal capacity is being updated. Maximum capacity for the agent across all service channels. If an agent's current workload equals the maximum universal capacity, additional work items won't be assigned to the agent. Data type: Number

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

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table id="table_bgk_dmp_htb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

channels

</td><td>

List of objects that describe the available channels of communication with the agent. ```
"channels": [
  {
    "channel_sys_id": "String",
    "max_capacity": Number
  }
]
```

 Data type: Array

</td></tr><tr><td>

channels.channel\_sys\_id

</td><td>

Channel sys\_id. Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr><td>

channels.max\_capacity

</td><td>

Maximum workload on a specific service channel that the agent can be actively assigned to at a time. Data type: String

</td></tr><tr id="ordr-row-error"><td>

error

</td><td>

Details describing an error encountered during the request process.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details of the error encountered during the request process. Data type: String

</td></tr><tr><td>

error.message

</td><td>

Message for the error encountered during the request process. The description is provided in the **error.detail** property.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of an unsuccessful request. This property is only included in the response if there is an error.Valid value: `failure`

Data type: String

</td></tr><tr><td>

universal\_capacity

</td><td>

Maximum capacity for the agent across all service channels. If an agent's current workload equals the maximum universal capacity, additional work items won't be assigned to the agent. This property only returns if a universal capacity record exists for this agent.

Data type: Number

</td></tr></tbody>
</table>### Sample cURL request

The following example shows how to change the agent's universal capacity and the maximum capacity for a specified channel.

```
curl "https://instance.service-now.com/api/now/awa/agents/46d44a23a9fe19810012d100cca80666/capacities" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
 \"channels\": { \"27f675e3739713004a905ee515f6a7c3\": 6 },
 \"universal_capacity\" : 12
}" \
--user 'username':'password'
```

A successful response includes the updated capacity values.

```
{
  "result": {
    "channels": [
      {
        "channel_sys_id": "27f675e3739713004a905ee515f6a7c3",
        "max_capacity": 6
      }
    ],
    "universal_capacity": 12
  }
}
```

