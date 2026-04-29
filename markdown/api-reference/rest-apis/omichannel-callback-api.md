---
title: Omichannel Callback API
description: The Omnichannel Callback API provides methods for creating, updating, and initiating a callback request for live agent conversations.Provides actions for integrating third-party Contact Center as a Service \(CCaaS\) platforms with ServiceNow's Omnichannel Callback system. This API acts as a bridge, routing callback operations \(create, update, cancel, close\) to external CCaaS providers via configurable Workflow Studio subflows.Initiates an interaction for an existing callback, including retry attempts.Initiates a new immediate or scheduled callback request based on details you provide in the request body. For immediate callbacks, this API creates both the callback and interaction. For scheduled callbacks, creates the callback with an appointment ID.Fetches callback information based on query parameters.Updates an existing callback according to details provided in the request.Cancels a given callback request.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 38
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Omichannel Callback API

The Omnichannel Callback API provides methods for creating, updating, and initiating a callback request for live agent conversations.

The Omnichannel Callback API allows agents to programmatically call users back rather than waiting in the queue for an available agent. For example, agents can use the callback functionality to call users back when the agent wait time is long or when there are no agents available. You can do the following actions with this API:

-   Create a new, immediate callback request or schedule a new request.
-   Create an initial interaction and subsequent retry interactions.
-   Update an existing callback.

This API belongs to the sn\_omni\_callback namespace and requires the Administrator with callback API \[sn\_omni\_callback.callback\_api\] role.

For more information about the Omnichannel Callback application as an ServiceNow AI Platform capability, see [Omnichannel Callback](https://www.servicenow.com/docs/access?context=omnichannel-callback&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Omnichannel Callback - POST api/sn\_omni\_callback/actions

Provides actions for integrating third-party Contact Center as a Service \(CCaaS\) platforms with ServiceNow®'s Omnichannel Callback system. This API acts as a bridge, routing callback operations \(create, update, cancel, close\) to external CCaaS providers via configurable Workflow Studio subflows.

**Note:** This endpoint works similarly to [Omnichannel Callback - POST /api/sn\_omni\_callback/callback/create](omichannel-callback-api.md#) and [Omnichannel Callback - PATCH /api/sn\_omni\_callback/callback/update](omichannel-callback-api.md#), but is used to update or create callbacks in a third-party integration with routing context.

### Intelligent routing

The /actions endpoint intelligently routes callback requests based on the **routingContext** parameter. When a routing rule is configured, the API uses a single, unified payload structure for all actions and routes the request to a CCaaS subflow using `routingContext`. When routing is configured, the content of the request never changes. Only the top‑level **action** value differs.

**Note:** The API checks for routing rules in the Callback Routing Configuration \[sys\_cs\_callback\_routing\_config\] table based on the **routingContext** parameter. If a matching rule is found, the request is forwarded to the configured custom subflow. The subflow can integrate with external CCaaS platforms or implement custom business logic. The subflow processes the request and returns the response.

If **routingContext** is omitted or no routing rule matches, the API falls back to default ServiceNow behavior and expects the standard payload format of the corresponding POST /create, PATCH /update, or PATCH /cancel endpoints.

### URL format

Versioned URL: `/api/sn_omni_callback/v1/actions`

Default URL: `/api/sn_omni_callback/actions`

### Supported request parameters

<table id="table_ixc_cvl_k3c" class="rest_api_path_parameters"><thead><tr><th>

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

<table id="table_myd_yh1_zhc" class="create_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing the operation and details.Data type: Object

```
{
    "action": "String",
    "payload": {Object},
    "routingContext": {Object}
  }
```

</td></tr><tr><td>

action

</td><td>

Required. Defines the action to perform on the callback.Accepted values:

-   `create`: Creates a new callback record.
-   `update`: Updates an existing callback record based on the callback number.
-   `close`: Closes a callback record because the callback request has been fulfilled. Doesn't initiate the callback. Updates the reason field in the Callback \[sys\_cs\_callback\] table.
-   `cancel`: Cancels a callback record because the customer cancelled the request and doesn't need to connect with an agent. Updates the reason field in the Callback \[sys\_cs\_callback\] table.

Data type: String

</td></tr><tr><td>

payload

</td><td>

Required. Object containing specific data required for the given action when **routingContext** object is passed. For close and cancel operations, only **callbackID** is needed in the payload.**Note:** For create and update actions, if **routingContext** isn't passed, use the **payload** object structure documented in the [Omnichannel Callback - POST /api/sn\_omni\_callback/callback/create](omichannel-callback-api.md#) and [Omnichannel Callback - PATCH /api/sn\_omni\_callback/callback/update](omichannel-callback-api.md#) operations, respectively. The 'Examples' section demonstrates both routing and non-routing scenarios.

Data type: Object

**payload** structure for create and update actions.

```
{
  "callbackContext": {Object},
  "callbackDetails": {Object},
  "callbackId": "String",
  "phoneNumber": "String",
  "type": "String"
}
```

**payload** structure for close and cancel actions.

```
"payload": {
  "callbackId": "String"
}
```

</td></tr><tr><td>

payload.callbackContext

</td><td>

Optional. Object containing the context details about the callback request.Table: Callback Context \[sys\_cs\_callback\_context\]

Data type: Object

```
"callbackContext": {
  "customer_timezone": "String",
  "ivr_path": "String",
  "queue": "String"
}
```

</td></tr><tr><td>

payload.callbackContext.customer\_timezone

</td><td>

Time zone of customer who requested the callback. Time zones can be provided in the following formats. -   `Country/City`: For example, `America/Los_Angeles`.
-   `Country/Time zone`: For example, `US/Pacific`.
-   `Time zone abbreviation`: For example, `PST`.

For a complete list of valid timezones, see the Time zone field in the User \[sys\_user\] table. For more information about time zones, see [Time zones](https://www.servicenow.com/docs/access?context=r_TimeZones&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

payload.callbackContext.ivr\_path

</td><td>

The IVR \(Interactive Voice Response\) path that a customer follows before being transferred to a human agent.Typically contains a list of queues or menu options the customer navigated through in the IVR system. This string is passed by Contact Center as a Service \(CCaaS\). For example, `"ivr_path": "Technical Support > Account Management"`

Data type: String

</td></tr><tr><td>

payload.callbackContext.queue

</td><td>

Number assignments in the queue.Data type: String

</td></tr><tr><td>

payload.callbackDetails

</td><td>

Optional. Object containing the details about the callback request.Table: Callback \[sys\_cs\_callback\]

Data type: Object

```
"callbackDetails": {
  "description": "String",
  "end_time": "String",
  "expire_time": "String",
  "first_name": "String",
  "last_name": "String",
  "opened_by": "String",
  "phone_number": "String",
  "next_retry": "String",
  "reason": "String",
  "scheduled_start_time": "String",
  "short_description": "String",
  "state": "String", 
  "type": "String"
}
```

</td></tr><tr><td>

payload.callbackDetails.description

</td><td>

Detailed explanation of the callback request. Can include specific customer concerns, context, or notes from the agent.Data type: String

</td></tr><tr><td>

payload.callbackDetails.end\_time

</td><td>

The time window when the callback request is expected to be completed. After this timestamp, the callback is considered overdue or expired unless rescheduled. Only applicable to a `Scheduled` callback type.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

payload.callbackDetails.expire\_time

</td><td>

The final cutoff time after which the callback request should no longer be attempted. This is often used to automatically close or cancel stale requests.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

payload.callbackDetails.first\_name

</td><td>

First name of the customer requesting the callback.Data type: String

</td></tr><tr><td>

payload.callbackDetails.last\_name

</td><td>

Last name of the customer requesting the callback.Data type: String

</td></tr><tr><td>

payload.callbackDetails.opened\_by

</td><td>

Sys\_id of the user or agent who created or initiated the callback request.Table: User \[sys\_user\]

</td></tr><tr><td>

payload.callbackDetails.phone\_number

</td><td>

Phone number of the customer to call back.Data type: String

</td></tr><tr><td>

payload.callbackDetails.next\_retry

</td><td>

The next scheduled attempt time if previous callback attempts were unsuccessful. Useful for automated or manual retry logic.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

payload.callbackDetails.reason

</td><td>

Reason for the callback request. Helps with routing, analytics, and reporting by tagging the callback with a standardized reason.Valid values:

-   `Other issue`
-   Custom values defined by your implementation. For example, `“Billing Inquiry”`, `“Technical Support”`

Table: Callback \[sys\_cs\_callback\], Field: reason\_type

Data type: String

</td></tr><tr><td>

payload.callbackDetails.scheduled\_start\_time

</td><td>

Date and time value to when the callback window begins. Only applicable to a `Scheduled` callback type.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

payload.callbackDetails.short\_description

</td><td>

A brief summary of the callback request, usually used in lists or dashboards.Data type: String

</td></tr><tr><td>

payload.callbackDetails.state

</td><td>

The current workflow status of the callback request. Valid values:

-   `pending approval`
-   `in progress`
-   `completed`
-   `canceled`

Data type: String

</td></tr><tr><td>

payload.callbackDetails.type

</td><td>

The category of the request. Value is always `callback`.

</td></tr><tr><td>

payload.callbackId

</td><td>

Required. Sys\_id or external\_id of the callback.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

payload.phoneNumber

</td><td>

Required. Phone number of the user requesting the callback.Data type: String

</td></tr><tr><td>

payload.type

</td><td>

Required. Type of callback.Valid value: `callback_request`

Data type: String

</td></tr><tr><td>

routingContext

</td><td>

Required for routing configuration. If not passed or the routing rule doesn't match, the actions endpoint doesn't invoke a CCaaS subflow and falls back to using default ServiceNow processing.Contextual information used to find a custom subflow or routing rule. If omitted, the API uses default callback processing.

Data type: Object

```
"routingContext": {
 "sourceTable": "String",
 "sourceId": "String",
 "userId": "String"
}
```

</td></tr><tr><td>

routingContext.sourceId

</td><td>

Sys\_id of the source record initiating the callback. Corresponds to the value of **sourceTable**.Data type: String

</td></tr><tr><td>

routingContext.sourceTable

</td><td>

The table name where the request originated.Accepted values:

-   `sp_portal`
-   `sn_csm_ec_engmnt_center_module`
-   `sn_embeddable_core_module`

Data type: String

</td></tr><tr><td>

routingContext.userId

</td><td>

User initiating the request \(often the agent or system user\).Table: User \[sys\_user\]

Data type: String

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

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

body

</td><td>

Object containing success or failure information about the request.Data type: Object

```
{
  "status": 200,
  "body": {
    "message": "String",
    "number": "String"
 }
}
```

</td></tr><tr><td>

body.message

</td><td>

Message with a brief details about the action's success or failure.Data type: String

</td></tr><tr><td>

body.number

</td><td>

The callback reference number. For example, `"CAL0010012"`.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

status

</td><td>

Corresponding status code of the request.Data type: String

</td></tr></tbody>
</table>### Create example \(routing enabled\)

This action creates a new callback record with routing context configured.

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "action": "create",
  "routingContext": {
    "sourceTable": "sn_csm_ec_engmnt_center_module",
    "sourceId": "a1b2c3d4e5f6a7b8",
    "userId": "beth.anglin"
  },
  "payload": {
    "callbackId": "cb-98765",
    "callbackDetails": {
      "first_name": "Alice",
      "last_name": "Smith",
      "state": "Pending Approval",
      "reason": "Request updated by user",
      "end_time": "2025-12-17T23:00:00Z",
      "scheduled_start_time": "2025-12-17T22:00:00Z",
      "next_retry": "2025-12-18T10:00:00Z",
      "expiry_time": "2025-12-18T12:00:00Z",
      "phone_number": "+14155552671",
      "short_description": "Callback request for customer support",
      "description": "Customer requested a callback regarding their recent order.",
      "opened_by": "user_sys_id_12345",
      "type": "callback"
    },
    "type": "callback_request",
    "phoneNumber": "+14155552671",
    "callbackContext": {
      "queue": "Customer Support",
      "ivr_path": "support/ivr-path",
      "customer_timezone": "GMT-5"
    }
  },
  "additional_parameters": {}
}
```

### Create \(no routing context\)

The following example demonstrates how to create a new callback record without routing context.

**Note:** Create actions without routing context follow the request structure documented in [Omnichannel Callback - POST /api/sn\_omni\_callback/callback/create](omichannel-callback-api.md#).

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "action": "create",
  "payload": {
  "type": "asap",
  "callbackDetails": {
    "appointment": "68cc0a5a9314521060320dd548373cbd",
    "description": "Customer reported issue with order #12345",
    "short_description": "Order issue",
    "reason_type": "product_issue",
    "expire_time": "2025-09-01 17:00",
    "messaging_channel": "web_channel_sys_id",
    "channel_to_callback": "genesys_channel_sys_id",
    "scheduled_start_time": "2025-09-01 1:00",
    "end_time": "2025-09-01 17:00",
    "user_document": "abel.tuter",
    "user_table": "sys_user"
},
  },
  "callbackContext": {
    "queue": "sample queue",
    "ivr_path": "sample ivr path"
  },
  "inboundId": "ServiceNowVoice",
  "isExternal": true,
  "phoneNumber": "+123454768",
  "externalCallbackId": "new-external-id",
  "interactionDetails": {
    "clientSessionId": "f8453abb-a33d-45b7-bf01-52b7a821e99z",
    "userId": "32423424",
    "callerPhoneNumber": "+14089178877"
  }
}
```

### Update action \(routing enabled\)

This example action updates an existing callback record with routing context. The **callbackNumber** value identifies the record to update:

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "action": "update",
  "payload": {
    "callbackDetails": {
      "appointment": "68cc0a5a9314521060320dd548373cbd",
      "description": "Customer reported issue with order #12345",
      "short_description": "Order issue",
      "reason_type": "product_issue",
      "expire_time": "2025-09-01 17:00",
      "messaging_channel": "web_channel_sys_id",
      "channel_to_callback": "genesys_channel_sys_id",
      "scheduled_start_time": "2025-09-01 1:00",
      "end_time": "2025-09-01 17:00",
      "user_document": "abel.tuter",
      "user_table": "sys_user"
    },
    "callbackContext": {
      "queue": "5 value changed via api",
      "ivr_path": "5 some-ivr-path changed via api"
    },
    "inboundId": "AmazonConnect",
    "phoneNumber": "+14089178877",
    "callbackId": "a16ead53fff0621088c6ffffffffffce"
  }
}
```

### Update \(no routing context\)

The following example demonstrates how to update a callback record without routing context:

**Note:** Update actions without routing context follow the request structure documented in [Omnichannel Callback - PATCH /api/sn\_omni\_callback/callback/update](omichannel-callback-api.md#).

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "action": "update",
  "payload": {
    "callbackDetails": {
      "appointment": "68cc0a5a9314521060320dd548373cbd",
      "description": "Customer reported issue with order #12345",
      "short_description": "Order issue",
      "reason_type": "product_issue",
      "expire_time": "2025-09-01 17:00",
      "messaging_channel": "web_channel_sys_id",
      "channel_to_callback": "genesys_channel_sys_id",
      "scheduled_start_time": "2025-09-01 1:00",
      "end_time": "2025-09-01 17:00",
      "user_document": "abel.tuter",
      "user_table": "sys_user"
    },
    "callbackContext": {
      "queue": "5 value changed via api",
      "ivr_path": "5 some-ivr-path changed via api"
    },
    "inboundId": "AmazonConnect",
    "phoneNumber": "+14089178877",
    "callbackId": "a16ead53fff0621088c6ffffffffffce"
  }
}
```

### Cancel action

This example action cancels a given callback record with routing context and updates the reason field in the Callback \[sys\_cs\_callback\] table.

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
    "action": "cancel",
    "routingContext": {
        "sourceTable": "sn_csm_ec_engmnt_center_module",
        "sourceId": "a1b2c3d4e5f6a7b8",
        "userId": "beth.anglin"
    },
     "payload": {
        "callbackId": "CAL0001234"
    }
}
```

### Cancel \(no routing context\)

The following example demonstrates how to cancel a callback record without routing context:

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "action": "cancel",
  "payload": {
    "callbackId": "cb-98765"
  }
}
```

### Close action \(routing enabled\)

This example closes a callback record with routing context and updates the reason field in the Callback \[sys\_cs\_callback\] table:

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
    "action": "close",
    "routingContext": {
        "sourceTable": "sn_csm_ec_engmnt_center_module",
        "sourceId": "a1b2c3d4e5f6a7b8",
        "userId": "beth.anglin"
    },
    "payload": {
        "callbackId": "CAL0001234"
    }
}
```

### Close \(no routing context\)

The following example demonstrates how to close a callback record without routing context:

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/actions \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "action": "close",
  "payload": {
    "callbackId": "cb-98765"
  }
}
```

## Omnichannel Callback - POST /api/sn\_omni\_callback/callback/attempt

Initiates an interaction for an existing callback, including retry attempts.

### URL format

Default URL: `/api/sn_omni_callback/callback/attempt`

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

callbackId

</td><td>

Required. Sys\_id or external\_id of the callback.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

interactionDetails

</td><td>

Optional. Details about the interaction. Meant for 'asap' \(immediate\) callback types so that interaction details are routed directly to the agent without waiting.All interaction details are passed in the payload of the [Voice Interaction Resource - POST /cs/voice-interactions](voice-interaction-resource-api.md#).

Data type: Object

```
"interactionDetails": {
  "callerPhoneNumber": "String",
  "clientSessionId": "String",
  "userId": "String"
}
```

</td></tr><tr><td>

interactionDetails.callerPhoneNumber

</td><td>

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops. Data type: String

Format: E.164 standard compliant

Default: None

</td></tr><tr><td>

interactionDetails.clientSessionId

</td><td>

Unique identifier of a record in an external system used to track this phone call. This information links the records between the two systems. Data type: String

Format: Typically a UUID or unique session token generated by the external system

Default: None

</td></tr><tr><td>

interactionDetails.userId

</td><td>

Sys\_id of the user to call back.Table: User \[sys\_user\]

Data type: String

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="d3003e85">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_xp5_5td_fgc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td id="omni-response-errors-entry">

Message containing details about the failures of the callback creation, like missing required request IDs.Data type: Array of strings

```
"errors": ["String", "String"]
```

</td></tr><tr><td>

messages

</td><td id="omni-response-messages-entry">

Message containing details about the success of the callback creation.Data type: Array of strings

```
"messages": ["String", "String"]
```

</td></tr><tr><td>

result

</td><td id="omni-response-result-row">

Result of the request.Data type: Object

```
"result": {
  "status": "String",
  "response": {Object},
  "errors": [Array],
  "messages": [Array]
}
```

</td></tr><tr><td>

result.response

</td><td id="omni-response-result.response-entry">

Object containing callback and interaction IDs of the callback request.Data type: Object

```
"response": {
  "callback_created": Boolean
  "callback_id": "String",
  "interaction_id": "String"
}
```

</td></tr><tr><td>

result.response.interaction\_id

</td><td id="omni-response-result.response.interaction_id-entry">

Sys\_id of the newly created interaction.Table: Interaction \[interaction\]

Data type: String

</td></tr><tr><td>

result.status

</td><td id="omni-response-result.status-entry">

Success or failure status of the request.Valid values:

-   success
-   failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example demonstrates a POST attempt request with details about the initial interaction and subsequent retry interactions.

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/callback/attempt' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "callbackId": "<ID#>",
  "interactionDetails": {
    "clientSessionId": "<ID#>",
    "userId": "<ID#>",
    "callerPhoneNumber": "+112345678901"
  }
}
```

Response body when a valid callback\_Id is provided and a new interaction was successfully created for the callback.

```
{
  "result": {
    "status": "success",
    "response": {
      "interaction_id": "<Interaction ID#>"
    }
  }
}
```

Response body when an invalid callback\_Id was provided in the request.

```
{
  "result": {
    "status": "failure",
    "response": {
      "interactionId": null
    },
    "errors": [
      "Callback not found for callback ID: <ID#>"
    ]
  }
}
```

Response body when the interaction already exists for the given callback \(message returns details about the existing interaction\):

```
{
  "result": {
    "status": "success",
    "response": {
      "interaction_id": "<Interaction ID#>"
    },
    "messages": [
      "Active Interaction <Interaction ID#> already exists for callback <ID#>"
    ]
  }
}
```

## Omnichannel Callback - POST /api/sn\_omni\_callback/callback/create

Initiates a new immediate or scheduled callback request based on details you provide in the request body. For immediate callbacks, this API creates both the callback and interaction. For scheduled callbacks, creates the callback with an appointment ID.

### URL format

Versioned URL: `/api/sn_omni_callback/v1/callback/create`

Default URL: `/api/sn_omni_callback/callback/create`

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

callbackContext

</td><td>

Object containing the context details about the callback request.Table: Callback Context \[sys\_cs\_callback\_context\]

Data type: Object

```
"callbackContext": {
  "customer_timezone": "String",
  "ivr_path": "String",
  "source_channel": "String",
  "queue": "String",
  "voicemail_duration": "String",
  "voicemail_recorded_at": "String",
  "voicemail_transcript": "String",
  "voicemail_url": "String"
}
```

</td></tr><tr><td>

callbackContext.customer\_timezone

</td><td>

Time zone of customer who requested the callback. Time zones can be provided in the following formats. -   `Country/City`. For example, `America/Los_Angeles`.
-   `Country/Time zone`. For example, `US/Pacific`.
-   `Time zone abbreviation`. For example, `PST`.

For a complete list of valid timezones, see the Time zone field in the User \[sys\_user\] table. For more information about time zones, see [Time zones](https://www.servicenow.com/docs/access?context=r_TimeZones&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

callbackContext.ivr\_path

</td><td>

The IVR \(Interactive Voice Response\) path that a customer follows before being transferred to a human agent.Typically contains a list of queues or menu options the customer navigated through in the IVR system. This string is passed by Contact Center as a Service \(CCaaS\). For example, `"ivr_path": "Technical Support > Account Management"`

Data type: String

</td></tr><tr><td>

callbackContext.queue

</td><td>

Number assignments in the queue.Data type: String

</td></tr><tr><td>

callbackContext.source\_channel

</td><td>

Source of the callback. For example, IVR, Web, or VA.Data type: String

</td></tr><tr><td>

callbackContext.voicemail\_duration

</td><td>

Length of the voicemail in hours, minutes, or seconds.Field: Voicemail Duration

Data type: Number

</td></tr><tr><td>

callbackContext.voicemail\_recorded\_at

</td><td>

Time stamp in which the voicemail was recorded.Field: Voicemail Recorded At

Data type: String

</td></tr><tr><td>

callbackContext.voicemail\_transcript

</td><td>

Transcribed text of the voicemail.Field: Voicemail Transcript

Data type: String

</td></tr><tr><td>

callbackContext.voicemail\_url

</td><td>

Relative link to the callback record containing the voicemail.Field: Voicemail URL

Data type: String

</td></tr><tr><td>

callbackDetails

</td><td>

Object containing the details about the callback request.Table: Callback \[sys\_cs\_callback\]

Data type: Object

```
"callbackDetails": {
  "appointment": "String",
  "channel_to_callback": "String",
  "description": "String",
  "end_time": "String",
  "expire_time": "String",
  "messaging_channel": "String",
  "reason_type": "String"
  "scheduled_start_time": "String",
  "short_description": "String",
  "user_document": "String",
  "user_table": "String"
}
```

</td></tr><tr><td>

callbackDetails.appointment

</td><td>

Sys\_id of the appointment. Only applicable to a `Scheduled` callback type.Table: Appointment Booking \[sn\_apptmnt\_booking\_appointment\_booking\]

Data type: String

</td></tr><tr><td>

callbackDetails.channel\_to\_callback

</td><td>

Target messaging channel to route the callback through.Table: Messaging Channel \[sys\_cs\_channel\], Field: sys\_id

Data type: String

</td></tr><tr><td>

callbackDetails.description

</td><td>

Full description describing the reason for the callback, if needed.Data type: String

</td></tr><tr><td>

callbackDetails.end\_time

</td><td>

Date and time value to stop the callback attempt. Only applicable to a `Scheduled` callback type.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

callbackDetails.expire\_time

</td><td>

Date and time to close the callback request.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

callbackDetails.messaging\_channel

</td><td>

Source of the callback. Identifies the client interface that initiated the callback request, such as a web client, mobile app, or embedded messenger.Table: Messaging Channel \[sys\_cs\_channel\], Field: sys\_id

Data type: String

</td></tr><tr><td>

callbackDetails.reason\_type

</td><td>

Reason for the callback request. Helps with routing, analytics, and reporting by tagging the callback with a standardized reason.Valid values:

-   `Other issue`
-   Custom values defined by your implementation. For example, `“Billing Inquiry”`, `“Technical Support”`

Table: Callback \[sys\_cs\_callback\], Field: reason\_type

Data type: String

</td></tr><tr><td>

callbackDetails.scheduled\_start\_time

</td><td>

Date and time value to initiate the callback. Only applicable to a `Scheduled` callback type.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

callbackDetails.short\_description

</td><td>

Provides a detailed explanation of the callback request. Can include specific customer concerns, context, or notes from the agent.Data type: String

</td></tr><tr><td>

callbackDetails.user\_document

</td><td>

Sys\_id of the user who requested the callback. Used with **callbackDetails.user\_table** to identify the user requesting the callback.Table: User \[sys\_user\], Field: sys\_id

Data type: String

</td></tr><tr><td>

callbackDetails.user\_table

</td><td>

Table where the user record resides. Used with **callbackDetails.user\_document** to identify the user requesting the callback. Value is always `sys_user`.Data type: String

</td></tr><tr><td>

externalCallbackId

</td><td>

External identifier for the callback that was created in a third party vendor.Data type: String

</td></tr><tr><td>

inboundId

</td><td>

Sys\_id of the inbound call associated with the callback. Provides traceability linking the callback request to a specific inbound call record that might originate from a third-party provider or CCaaS platform.Table: Callback \[sys\_cs\_callback\], Field: provider\_application\_id

Data type: String

</td></tr><tr><td>

interactionDetails

</td><td>

Optional. Details about the interaction. Meant for 'asap' \(immediate\) callback types so that interaction details are routed directly to the agent without waiting.All interaction details are passed in the payload of the [Voice Interaction Resource - POST /cs/voice-interactions](voice-interaction-resource-api.md#).

Data type: Object

```
"interactionDetails": {
  "callerPhoneNumber": "String",
  "clientSessionId": "String",
  "userId": "String"
}
```

</td></tr><tr><td>

interactionDetails.callerPhoneNumber

</td><td>

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops. Data type: String

Format: E.164 standard compliant

Default: None

</td></tr><tr><td>

interactionDetails.clientSessionId

</td><td>

Unique identifier of a record in an external system used to track this phone call. This information links the records between the two systems. Data type: String

Format: Typically a UUID or unique session token generated by the external system

Default: None

</td></tr><tr><td>

interactionDetails.userId

</td><td>

Sys\_id of the user to call back.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

isExternal

</td><td>

Flag that indicates whether the callback is external and was requested in different third-party vendor.Valid values:

-   true: Callback is external.
-   false: Callback is not external.

Default: false

</td></tr><tr><td>

type

</td><td>

Required. Type of callback.Valid values:

-   `asap`: The callback interaction is created instantly.
-   `scheduled`: The callback interaction is created and scheduled for a later time selected by the customer.

Data type: String

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="d3003e85">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td id="omni-response-result-row">

Result of the request.Data type: Object

```
"result": {
  "status": "String",
  "response": {Object},
  "errors": [Array],
  "messages": [Array]
}
```

</td></tr><tr><td>

result.errors

</td><td>

Message containing details about the failures of the callback creation, like missing required request IDs.Data type: Array of strings

```
"errors": ["String", "String"]
```

</td></tr><tr><td>

result.messages

</td><td>

Message containing details about the success of the callback creation.Data type: Array of strings

```
"messages": ["String", "String"]
```

</td></tr><tr><td>

result.response

</td><td id="omni-response-result.response-entry">

Object containing callback and interaction IDs of the callback request.Data type: Object

```
"response": {
  "callback_created": Boolean
  "callback_id": "String",
  "interaction_id": "String"
}
```

</td></tr><tr><td>

result.response.callback\_created

</td><td id="omni-response-result.response.callback_created-entry">

Flag indicating whether the new callback request was created or not.

 Possible values:

-   true: Callback was created successfully.
-   false: Callback was not created. For example, the callback already exists with the given callback\_id.

 Data type: Boolean

</td></tr><tr><td>

result.response.callback\_id

</td><td id="omni-response-result.response.callback_id-entry">

Sys\_id of the new callback, if applicable.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

result.response.interaction\_id

</td><td id="omni-response-result.response.interaction_id-entry">

Sys\_id of the newly created interaction.Table: Interaction \[interaction\]

Data type: String

</td></tr><tr><td>

result.status

</td><td id="omni-response-result.status-entry">

Success or failure status of the request.Valid values:

-   success
-   failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example creates a simple callback request according to details the agent provides in the request body.

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/callback/create' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "type": "asap",
  "callbackDetails": {
    "appointment": "68cc0a5a9314521060320dd548373cbd",
    "description": "Customer reported issue with order #12345",
    "short_description": "Order issue",
    "reason_type": "product_issue",
    "expire_time": "2025-09-01 17:00",
    "messaging_channel": "web_channel_sys_id",
    "channel_to_callback": "genesys_channel_sys_id",
    "scheduled_start_time": "2025-09-01 1:00",
    "end_time": "2025-09-01 17:00",
    "user_document": "abel.tuter",
    "user_table": "sys_user"
},
  },
  "callbackContext": {
    "queue": "sample queue",
    "ivr_path": "sample ivr path"
  },
  "inboundId": "ServiceNowVoice",
  "isExternal": true,
  "phoneNumber": "+123454768",
  "externalCallbackId": "new-external-id",
  "interactionDetails": {
    "clientSessionId": "f8453abb-a33d-45b7-bf01-52b7a821e99z",
    "userId": "32423424",
    "callerPhoneNumber": "+14089178877"
  }
}
```

The response body returns a success response with callback and interaction IDs for the newly created callback request.

```
{
  "status": "success",
  "response": {
    "callback_id": "a16ead53fff0621088c6ffffffffffce",
    "interaction_id": "696e6d57fff0621088c6ffffffffff7d"
  }
}
```

Response body when interaction details were not provided:

```
{
  "status": "success",
  "response": {
    "callback_created": true,
    "callback_id": "7df2059ffffc221088c6ffffffffff0c"
  }
}
```

Response body when the callback ID already exists but new interaction details were provided:

```
{
  "result": {
    "status": "success",
    "response": {
      "interaction_id": "84054fff53786210011eddeeff7b12d6",
      "callback_id": "8b43c3fb53786210011eddeeff7b12a6",
      “callback_created”: false
    },
    "messages": [
      "Successfully updated the callback 8b43c3fb53786210011eddeeff7b12a6",
      "Successfully created the interaction 84054fff53786210011eddeeff7b12d6"
    ]
  }
}
```

Response body when the callback ID already exists but new interaction details were not provided:

```
{
  "result": {
    "status": "success",
    "response": {
      "callback_id": "8b43c3fb53786210011eddeeff7b12a6"
    },
    "messages": [
      "Successfully updated the callback 8b43c3fb53786210011eddeeff7b12a6"
    ]
  }
}
```

Response body when mandatory fields are missing in the request:

```
{
  "result": {
    "status": "failure",
    "response": {
      "callbackId": null
    },
    "errors": [
      "Parameter 'type' is required in request"
    ]
  }
}
```

## Omnichannel Callback - POST api/sn\_omni\_callback/callback/get

Fetches callback information based on query parameters.

### URL format

Versioned URL: `/api/sn_omni_callback/v1/callback/get`

Default URL: `/api/sn_omni_callback/callback/get`

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

queryParameters

</td><td>

Object containing the key-value pair of the query parameters to filter results on.Data type: Object

```
"queryParameters": {
  "number": "String",
  "state": "String",
  "opened_by": "String",
  "sys_id", "String",
  "callback_type": "String",
  "external_callback_id": "String",
  "callback_number": "String"
}
```

</td></tr><tr><td>

queryParameters.number

</td><td>

The callback reference number to look up. For example, `"CAL0010012"`.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

queryParameters.state

</td><td>

Number representing the current state of the callback.Possible values:

-   `1`: Open
-   `2`: Work in Progress
-   `3`: Closed Complete
-   `4`: Closed Abandoned
-   `7`: Cancelled

Data type: Number

</td></tr><tr><td>

queryParameters.opened\_by

</td><td>

User ID of the user requesting the callback.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

queryParameters.sys\_id

</td><td>

Sys\_id of the callback record.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

queryParameters.callback\_type

</td><td>

Type of callback.Valid values:

-   `asap`: The callback interaction is created instantly.
-   `scheduled`: The callback interaction is created and scheduled for a later time selected by the customer.

Data type: String

</td></tr><tr><td>

queryParameters.external\_callback\_id

</td><td>

External identifier for the callback created in a third-party system.Data type: String

</td></tr><tr><td>

queryParameters.callback\_number

</td><td>

Phone number of the caller to call back.Data type: String

</td></tr><tr><td>

responseParameters

</td><td>

Optional. Specifies which fields to return in the response. If omitted, the endpoint returns default fields.Data type: Object

```
"responseParameters": {
  "callback": [Array],
  "context": [Array]
}
```

</td></tr><tr><td>

responseParameters.callback

</td><td>

Optional. Returns fields from the callback record \(for example, `number`, `phone_number`\).Table: Callback \[sys\_cs\_callback\]

Data type: Object

```
"callback": [String, String]
```

Valid values:

-   `number`: Unique reference number for that callback \(for example, `"CAL0010012"`\).
-   `phone_number`: Phone number of the caller.

</td></tr><tr><td>

responseParameters.context

</td><td>

Optional. Returns contextual information of the callback, such as queue, assignment, or related metadata in the form of key:value pairs.Table: Callback Context \[sys\_cs\_callback\_context\]

Data type: Array of Strings

```
"callbackContext": {
  "customer_timezone": "String",
  "ivr_path": "String",
  "source_channel": "String",
  "queue": "String",
  "voicemail_duration": "String",
  "voicemail_recorded_at": "String",
  "voicemail_transcript": "String",
  "voicemail_url": "String"
}
```

</td></tr><tr><td>

responseParameters.context.customer\_timezone

</td><td>

Time zone of the user requesting the callback.String

</td></tr><tr><td>

responseParameters.context.ivr\_path

</td><td>

The IVR \(Interactive Voice Response\) path that a customer follows before being transferred to a human agent.Typically contains a list of queues or menu options the customer navigated through in the IVR system. This string is passed by Contact Center as a Service \(CCaaS\). For example, `"ivr_path": "Technical Support > Account Management"`

Data type: String

</td></tr><tr><td>

responseParameters.context.source\_channel

</td><td>

Source of the callback. For example, IVR, Web, or VA.String

</td></tr><tr><td>

responseParameters.context.queue

</td><td>

Name or ID of the queue where the callback is assigned.String

</td></tr><tr><td>

responseParameters.context.voicemail\_duration

</td><td>

Length of the voicemail in hours, minutes, or seconds.Table: Callback Context \[sys\_cs\_callback\_context\], Field: Voicemail Duration

String

</td></tr><tr><td>

responseParameters.context.voicemail\_recorded\_at

</td><td>

Time stamp in which the voicemail was recorded.Table: Callback Context \[sys\_cs\_callback\_context\], Field: Voicemail Recorded At

Data type: String

</td></tr><tr><td>

responseParameters.context.voicemail\_transcript

</td><td>

Transcribed text of the voicemail.Table: Callback Context \[sys\_cs\_callback\_context\], Field: Voicemail Transcript

Data type: String

</td></tr><tr><td>

responseParameters.context.voicemail\_url

</td><td>

Relative link to the callback record containing the voicemail.Table: Callback Context \[sys\_cs\_callback\_context\], Field: Voicemail URL

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing the callback record or callback information that matched the specified search criteria.Date type: Object

```
"result": {
  "response": {Object},
  "status": "String"
}
```

</td></tr><tr><td>

result.response

</td><td>

Callback information.Data type: Object

```
"response": {
 "callbacks": [Array],
 "count": "Number"
}
```

</td></tr><tr><td>

result.response.callbacks

</td><td>

Object containing details about the callback record in the form of key:value pairs. **Note:** Displays all default fields if **responseParameters** wasn't specified in the request.

Data type: Array of Strings

```
"callbacks": [
  {
    "number": "String",
    "state": "String",
    "first_name": "Virtual",
    "last_name": "Agent",
    "user_table": "sys_user",
    "opened_by": "Virtual Agent",
    "assigned_to": ""
  }
]
```

</td></tr><tr><td>

result.response.callbacks.assigned\_to

</td><td>

ID of the agent assigned to the request.Data type: String

</td></tr><tr><td>

result.response.callbacks.context

</td><td>

Contextual information of the callback record. Varies based on the request input.Table: Callback Context \[sys\_cs\_callback\_context\]

Data type: Array of Strings

```
"callbackContext": {
  "customer_timezone": "String",
  "ivr_path": "String",
  "source_channel": "String",
  "queue": "String",
  "voicemail_duration": "String",
  "voicemail_recorded_at": "String",
  "voicemail_transcript": "String",
  "voicemail_url": "String"
}
```

</td></tr><tr><td>

result.response.callbacks.context.customer\_timezone

</td><td>

Time zone of user requesting the callback.String

</td></tr><tr><td>

result.response.callbacks.context.ivr\_path

</td><td>

The IVR \(Interactive Voice Response\) path that a customer follows before being transferred to a human agent.Typically contains a list of queues or menu options the customer navigated through in the IVR system. This string is passed by Contact Center as a Service \(CCaaS\). For example, `"ivr_path": "Technical Support > Account Management"`

Data type: String

</td></tr><tr><td>

result.response.callbacks.context.source\_channel

</td><td>

Source of the callback. For example, IVR, Web, or VA.String

</td></tr><tr><td>

result.response.callbacks.context.queue

</td><td>

Name or ID of the queue where the callback is assigned.String

</td></tr><tr><td>

result.response.callbacks.context.voicemail\_duration

</td><td>

Length of the voicemail in hours, minutes, or seconds.String

</td></tr><tr><td>

result.response.callbacks.context.voicemail\_recorded\_at

</td><td>

Time stamp in which the voicemail was recorded.Data type: String

</td></tr><tr><td>

result.response.callbacks.context.voicemail\_transcript

</td><td>

Transcribed text of the voicemail.Data type: String

</td></tr><tr><td>

result.response.callbacks.context.voicemail\_url

</td><td>

Relative link to the callback record containing the voicemail.Data type: String

</td></tr><tr><td>

result.response.callbacks.created\_on

</td><td>

Time stamp when callback was created.Data type: String

</td></tr><tr><td>

result.response.callbacks.first\_name

</td><td>

First name of the user who initiated or is associated with the callback.Data type: String

</td></tr><tr><td>

result.response.callbacks.last\_name

</td><td>

Last name of the associated user. Completes the user’s full name for logging, routing, and display.Data type: String

</td></tr><tr><td>

result.response.callbacks.number

</td><td>

Unique callback reference number. For example, `"CAL0010012"`.Data type: String

</td></tr><tr><td>

result.response.callbacks.opened\_by

</td><td>

User ID of the user requesting the callback.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

result.response.callbacks.phone\_number

</td><td>

Phone number of the caller.Data type: String

</td></tr><tr><td>

result.response.callbacks.status

</td><td>

Current status of the callback. Possible values:

-   `1`: Open
-   `2`: Work in Progress
-   `3`: Closed Complete
-   `4`: Closed Abandoned
-   `7`: Cancelled

Data type: String

</td></tr><tr><td>

result.response.callbacks.user\_table

</td><td>

Table to reference when looking up callback user details. For example, sys\_user.Data type: String

</td></tr><tr><td>

result.response.count

</td><td>

Number of matching records according to search criteria.Data type: Number

</td></tr><tr><td>

result.status

</td><td>

Success or error status of the request.Possible values:

-   error: Internal or unexpected failure, such as a database connection failure, server exception, or uncaught runtime error.
-   failed: Operation couldn't be completed. For example: No record found, validation failed, or unsupported parameter.
-   not\_found: Queried entity doesn’t exist.
-   unauthorized: Caller lacks permissions, credentials, or access.
-   invalid\_request: For malformed parameters, wrong types, or missing required fields.
-   timeout: Upstream system or database didn’t return on time.
-   partial\_success: Some records processed successfully or some failed.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following POST example queries callback records specifically opened by a Virtual Agent \(`"opened_by": "virtual.agent"`\) and is in a closed state \(`4`\), and directs the API to return only the callback record's reference number and phone number \(`"callback": ["number", "callback_number"]`\) within a queue context \(`"context": ["queue"]`\).

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/callback/get' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -u 'username':'password' \ 
  -d {
  "queryParameters": {
    "opened_by": "virtual.agent",
    "state": 4,
  },
  "responseParameters": {
    "callback": ["number", "callback_number"],
    "context": ["queue"]
  }
}
```

Response body.

```
{
  "result": {
    "status": "success",
    "response": {
      "callbacks": [
        {
          "number": "CAL0010036",
          "callback_number": "+14089178878",
          "context": {
            "queue": "21 value changed via api"
          }
        },
        {
          "number": "CAL0010037",
          "callback_number": "+14089178878",
          "context": {
            "queue": "21 value changed via api"
          }
        },
        {
          "number": "CAL0010001",
          "callback_number": "+918008509174",
          "context": {
            "queue": "queue"
          }
        },
        {
          "number": "CAL0010033",
          "callback_number": "+14089178878",
          "context": {
            "queue": "21 value changed via api"
          }
        },
        {
          "number": "CAL0010003",
          "callback_number": "+918008509174",
          "context": {
            "queue": "Soumya queue"
          }
        },
        {
          "number": "CAL0010035",
          "callback_number": "+14089178878",
          "context": {
            "queue": "21 value changed via api"
          }
        },
        {
          "number": "CAL0010038",
          "callback_number": "+14089178878",
          "context": {
            "queue": "21 value changed via api"
          }
        },
        {
          "number": "CAL0010034",
          "callback_number": "+14089178878",
          "context": {
            "queue": "21 value changed via api"
          }
        }
      ],
      "count": 8
    }
  }
}
```

The following example retrieves callback information based on a matching external ID, `new-external-2325`. Because the call doesn't provide **responseParameters** in the request, the response returns the full default record.

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/callback/get' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -u 'username':'password' \ 
  -d {
  "queryParameters": {
    "external_callback_id": "new-external-2325"
  }
}
```

Response body:

```
{
  "result": {
    "status": "success",
    "response": {
      "callbacks": [
        {
          "number": "CAL0010038",
          "state": "Closed Abandoned",
          "first_name": "Virtual",
          "last_name": "Agent",
          "user_table": "sys_user",
          "opened_by": "Virtual Agent",
          "assigned_to": ""
        }
      ]
    }
  }
}
```

## Omnichannel Callback - PATCH /api/sn\_omni\_callback/callback/update

Updates an existing callback according to details provided in the request.

Only provide request parameters in the request body that you want to update.

### URL format

Default URL: `/api/sn_omni_callback/callback/update`

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

callbackContext

</td><td>

Object containing the context details about the callback request.Table: Callback Context \[sys\_cs\_callback\_context\]

Data type: Object

```
"callbackContext": {
  "customer_timezone": "String",
  "ivr_path": "String",
  "source_channel": "String",
  "queue": "String",
  "voicemail_duration": "String",
  "voicemail_recorded_at": "String",
  "voicemail_transcript": "String",
  "voicemail_url": "String"
}
```

</td></tr><tr><td>

callbackContext.customer\_timezone

</td><td>

Time zone of customer who requested the callback. Time zones can be provided in the following formats. -   `Country/City`. For example, `America/Los_Angeles`.
-   `Country/Time zone`. For example, `US/Pacific`.
-   `Time zone abbreviation`. For example, `PST`.

For a complete list of valid timezones, see the Time zone field in the User \[sys\_user\] table. For more information about time zones, see [Time zones](https://www.servicenow.com/docs/access?context=r_TimeZones&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Data type: String

</td></tr><tr><td>

callbackContext.ivr\_path

</td><td>

The IVR \(Interactive Voice Response\) path that a customer follows before being transferred to a human agent.Typically contains a list of queues or menu options the customer navigated through in the IVR system. This string is passed by Contact Center as a Service \(CCaaS\). For example, `"ivr_path": "Technical Support > Account Management"`

Data type: String

</td></tr><tr><td>

callbackContext.queue

</td><td>

Number assignments in the queue.Data type: String

</td></tr><tr><td>

callbackContext.source\_channel

</td><td>

Source of the callback. For example, IVR, Web, or VA.Data type: String

</td></tr><tr><td>

callbackContext.voicemail\_duration

</td><td>

Length of the voicemail in hours, minutes, or seconds.Field: Voicemail Duration

Data type: Number

</td></tr><tr><td>

callbackContext.voicemail\_recorded\_at

</td><td>

Time stamp in which the voicemail was recorded.Field: Voicemail Recorded At

Data type: String

</td></tr><tr><td>

callbackContext.voicemail\_transcript

</td><td>

Transcribed text of the voicemail.Field: Voicemail Transcript

Data type: String

</td></tr><tr><td>

callbackContext.voicemail\_url

</td><td>

Relative link to the callback record containing the voicemail.Field: Voicemail URL

Data type: String

</td></tr><tr><td>

callbackDetails

</td><td>

Object containing the details about the callback request.Table: Callback \[sys\_cs\_callback\]

Data type: Object

```
"callbackDetails": {
  "appointment": "String",
  "channel_to_callback": "String",
  "description": "String",
  "end_time": "String",
  "expire_time": "String",
  "messaging_channel": "String",
  "reason_type": "String"
  "scheduled_start_time": "String",
  "short_description": "String",
  "user_document": "String",
  "user_table": "String"
}
```

</td></tr><tr><td>

callbackDetails.appointment

</td><td>

Sys\_id of the appointment. Only applicable to a `Scheduled` callback type.Table: Appointment Booking \[sn\_apptmnt\_booking\_appointment\_booking\]

Data type: String

</td></tr><tr><td>

callbackDetails.channel\_to\_callback

</td><td>

Target messaging channel to route the callback through.Table: Messaging Channel \[sys\_cs\_channel\], Field: sys\_id

Data type: String

</td></tr><tr><td>

callbackDetails.description

</td><td>

Full description describing the reason for the callback, if needed.Data type: String

</td></tr><tr><td>

callbackDetails.end\_time

</td><td>

Date and time value to stop the callback attempt. Only applicable to a `Scheduled` callback type.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

callbackDetails.expire\_time

</td><td>

Date and time to close the callback request.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

callbackDetails.messaging\_channel

</td><td>

Source of the callback. Identifies the client interface that initiated the callback request, such as a web client, mobile app, or embedded messenger.Table: Messaging Channel \[sys\_cs\_channel\], Field: sys\_id

Data type: String

</td></tr><tr><td>

callbackDetails.reason\_type

</td><td>

Reason for the callback request. Helps with routing, analytics, and reporting by tagging the callback with a standardized reason.Valid values:

-   `Other issue`
-   Custom values defined by your implementation. For example, `“Billing Inquiry”`, `“Technical Support”`

Table: Callback \[sys\_cs\_callback\], Field: reason\_type

Data type: String

</td></tr><tr><td>

callbackDetails.scheduled\_start\_time

</td><td>

Date and time value to initiate the callback. Only applicable to a `Scheduled` callback type.Format: glide\_date\_time value, such as `yyyy-MM-dd HH:mm:ss`

Data type: String

</td></tr><tr><td>

callbackDetails.short\_description

</td><td>

Provides a detailed explanation of the callback request. Can include specific customer concerns, context, or notes from the agent.Data type: String

</td></tr><tr><td>

callbackDetails.user\_document

</td><td>

Sys\_id of the user who requested the callback. Used with **callbackDetails.user\_table** to identify the user requesting the callback.Table: User \[sys\_user\], Field: sys\_id

Data type: String

</td></tr><tr><td>

callbackDetails.user\_table

</td><td>

Table where the user record resides. Used with **callbackDetails.user\_document** to identify the user requesting the callback. Value is always `sys_user`.Data type: String

</td></tr><tr><td>

callbackId

</td><td>

Required. Sys\_id or external\_id of the callback.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

inboundId

</td><td>

Sys\_id of the inbound call associated with the callback. Provides traceability linking the callback request to a specific inbound call record that might originate from a third-party provider or CCaaS platform.Table: Callback \[sys\_cs\_callback\], Field: provider\_application\_id

Data type: String

</td></tr><tr><td>

phoneNumber

</td><td>

Phone number of the caller.Data type: String of numbers

Format: E.164 standard compliant

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
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="d3003e85">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_xp5_5td_fgc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td id="omni-response-errors-entry">

Message containing details about the failures of the callback creation, like missing required request IDs.Data type: Array of strings

```
"errors": ["String", "String"]
```

</td></tr><tr><td>

messages

</td><td id="omni-response-messages-entry">

Message containing details about the success of the callback creation.Data type: Array of strings

```
"messages": ["String", "String"]
```

</td></tr><tr><td>

result

</td><td id="omni-response-result-row">

Result of the request.Data type: Object

```
"result": {
  "status": "String",
  "response": {Object},
  "errors": [Array],
  "messages": [Array]
}
```

</td></tr><tr><td>

result.response

</td><td id="omni-response-result.response-entry">

Object containing callback and interaction IDs of the callback request.Data type: Object

```
"response": {
  "callback_created": Boolean
  "callback_id": "String",
  "interaction_id": "String"
}
```

</td></tr><tr><td>

result.response.callback\_created

</td><td id="omni-response-result.response.callback_created-entry">

Flag indicating whether the new callback request was created or not.

 Possible values:

-   true: Callback was created successfully.
-   false: Callback was not created. For example, the callback already exists with the given callback\_id.

 Data type: Boolean

</td></tr><tr><td>

result.response.callback\_id

</td><td id="omni-response-result.response.callback_id-entry">

Sys\_id of the new callback, if applicable.Table: Callback \[sys\_cs\_callback\]

Data type: String

</td></tr><tr><td>

result.response.interaction\_id

</td><td id="omni-response-result.response.interaction_id-entry">

Sys\_id of the newly created interaction.Table: Interaction \[interaction\]

Data type: String

</td></tr><tr><td>

result.status

</td><td id="omni-response-result.status-entry">

Success or failure status of the request.Valid values:

-   success
-   failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example updates some callback details in the associated callback request.

```
curl -X POST 'https://instance.servicenow.com/api/sn_omni_callback/callback/update' \ 
  -H 'Accept: application/json' \ 
  -H 'Content-Type: application/json' \ 
  -u 'username':'password' \ 
  -d ' {
  "callbackDetails": {
    "appointment": "68cc0a5a9314521060320dd548373cbd",
    "description": "Customer reported issue with order #12345",
    "short_description": "Order issue",
    "reason_type": "product_issue",
    "expire_time": "2025-09-01 17:00",
    "messaging_channel": "web_channel_sys_id",
    "channel_to_callback": "genesys_channel_sys_id",
    "scheduled_start_time": "2025-09-01 1:00",
    "end_time": "2025-09-01 17:00",
    "user_document": "abel.tuter",
    "user_table": "sys_user"
},
  "callbackContext": {
    "queue": "5 value changed via api",
    "ivr_path": "5 some-ivr-path changed via api"
  },
  "inboundId": "AmazonConnect",
  "phoneNumber": "+14089178877",
  "callbackId": "a16ead53fff0621088c6ffffffffffce"
}
```

Response of a successful update to the valid, existing callback ID.

```
{
  "result": {
    "status": "success",
    "response": {
      "callback_id": "952f763b53786210011eddeeff7b1297"
    },
    "messages": [
      "Successfully updated the callback 952f763b53786210011eddeeff7b1297"
    ]
  }
}
```

Response when an invalid callback ID is provided in the request:

```

  "result": {
    "status": "failure",
    "response": {
      "callbackId": null
    },
    "errors": [
      "Callback not found for callback ID: 952f763b53786210011eddeef7b1297"
    ]
  }
}
```

Response when a callback ID is missing in the request:

```

  "result": {
    "status": "failure",
    "response": {
      "callbackId": null
    },
    "errors": [
      "Parameter 'callbackId' is required in request"
    ]
  }
}
```

## Omnichannel Callback - PATCH /api/sn\_omni\_callback/callback/close/\{callback\_number\}

Cancels a given callback request.

### URL format

Versioned URL: `/api/{api_version}/sn_omni_callback/callback/close/{callback_number}`

Default URL: `/api/sn_omni_callback/callback/close/{callback_number}`

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

callback\_number

</td><td>

Sys\_id or external\_id of the callback to cancel.Table: Callback \[sys\_cs\_callback\]

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

reason

</td><td>

Optional. Specifies to cancel the given callback. Value is always `Cancelled`. If **reason** isn't passed, the request is closed rather than cancelled.Data type: String

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

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

reason

</td><td>

Reason for updating the callback request. Value is always `Cancelled` or `Closed`.Table: Callback \[sys\_cs\_callback\], Field: Reason

Data type: String

```
{
"reason": "Cancelled"
}
```

</td></tr></tbody>
</table>### cURL request

The following request cancels the callback request with callback ID CAL0001234.

```
curl -X POST "https://instance.servicenow.com/api/sn_omni_callback/callback/close/CAL0001234" \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -u "username:password" \
  -d '{
    "reason": "Cancelled"
  }'

```

The response body confirms the cancellation.

```
{
"reason":"Cancelled"
}
```

