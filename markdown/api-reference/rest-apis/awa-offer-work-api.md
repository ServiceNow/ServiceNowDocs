---
title: AWA Offer Work API
description: The AWA Offer Work API provides an endpoint to assign or transfer work items to agents.Assigns or transfers work items to agents.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AWA Offer Work API

The AWA Offer Work API provides an endpoint to assign or transfer work items to agents.

This API is intended for use with Contact Center as a Service \(CCAAS\) integrations where the routing and assignment decision takes place in the external CCAAS system. This API allows an [inbox card](https://www.servicenow.com/docs/access?context=awa-inbox-layout&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) to be shown to an agent in the ServiceNow Agent Workspace as a notification to accept the work item.

This API requires the Advanced Work Assignment \(com.glide.awa\) plugin. To call this API, you must have either the awa\_manager or awa\_integration\_user role.

For more information about AWA, see [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AWA Offer Work - POST /now/awa/documents/\{document\_table\}/\{document\_sys\_id\}/offer

Assigns or transfers work items to agents.

A work item is a single piece of work handled by an AWA agent from start to finish. A work item is created based on a document, such as an interaction or task.

All agents receiving or transferring work items with this API must have the awa\_agent and awa\_external\_user roles.

### URL format

Versioned URL: `/api/now/{api_version}/awa/documents/{document_table}/{document_sys_id}/offer`

Default URL: `/api/now/awa/documents/{document_table}/{document_sys_id}/offer`

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

document\_table

</td><td>

Name of the table associated with the document, such as the Interaction \[interaction\] table or Task \[task\] table.Data type: String

</td></tr><tr><td>

document\_sys\_id

</td><td>

Sys\_id of the document to route to the agent or queue.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assignment

</td><td>

Required for new assignments. Object containing information about the assignment.Data type: Object

```
{ 
   "after_timeout_presence": "String",
   "agent_sys_id": "String", 
   "allowed_to_decline": Boolean,
   "display_option": "String", 
   "enable_auto_assign": Boolean, 
   "offered_on": "String",
   "timeout": Number 
} 
```

</td></tr><tr><td>

assignment.after\_timeout\_presence

</td><td>

Sys\_id of the presence state that the agent switches to if the **timeout** parameter expires.If the **timeout** parameter isn't passed, this parameter is ignored.

For additional information on presence states, see [Configure agent presence states](https://www.servicenow.com/docs/access?context=awa-configure-agent-presence&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

Data type: String

Default: Empty string \(Agent presence state doesn't change\).

Table: AWA Presence State \[awa\_presence\_state\]

</td></tr><tr><td>

assignment.agent\_sys\_id

</td><td>

Required for new assignments. Sys\_id of the available agent to receive the work item. The agent must have the awa\_agent and awa\_external\_user roles.For information on how to determine if an agent is available, refer to [Agent Inbox controls](https://www.servicenow.com/docs/access?context=agent-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

assignment.allowed\_to\_decline

</td><td>

Flag that indicates whether agents are allowed to reject work items. If this parameter is `true`, the inbox card displays both the **Accept** and **Reject** buttons on the inbox card.Valid values:

-   true/yes/1: Agent can reject work items.
-   false/no/0: Agent can't reject work items.

Data type: Boolean

Default: true

</td></tr><tr><td>

assignment.display\_option

</td><td>

Display option for the card and tab when a work item is automatically assigned. This parameter is only valid if **enable\_auto\_assign** is `true`.

Valid values:

-   card\_and\_tab: Display both the card and tab.
-   card\_only: Display only the card.

Data type: String

Default: card\_only

</td></tr><tr><td>

assignment.enable\_auto\_assign

</td><td>

Flag that indicates whether the work item should be automatically accepted or should allow the agent to manually accept or reject the work item.Valid values:

-   true/yes/1: Automatically accept.
-   false/no/0: Allow agent to manually accept or reject.

Data type: Boolean

Default: false

</td></tr><tr><td>

assignment.offered\_on

</td><td>

Work item offer time. The offer time is used to calculate the remaining time the agent has left to accept the work item in the inbox. It helps account for the discrepancy between the time when the API request gets processed, and when the third-party routing system invokes the API request. This parameter allows external systems calling this endpoint to configure the offer time of the work item so that it stays in synchronization with the external system’s internal tracking of the work item.For example, if the work item was offered on 11:30:30, the timeout is 30 seconds, and the current time is 11:30:45, the countdown timer displays 00:15 \(as in 15 seconds remaining\).

This value is stored in the offered\_on field on the work item.

This parameter is ignored if the **timeout** parameter isn't passed.

Data type: String

Format: UTC timestamp \(yyyy-MM-dd'T'HH:mm:ss.SSS\)

</td></tr><tr><td>

assignment.timeout

</td><td>

Amount of time that the work item stays in the agent’s inbox waiting for the agent to accept the work assignment.Data type: Number

Unit: Seconds

Default: Empty string \(No time limit\).

</td></tr><tr><td>

external\_segment\_id

</td><td>

External identifier from the CCAAS system of the call segment offered to the agent.Data type: String

</td></tr><tr><td>

queue\_id

</td><td>

Required for new assignments. Sys\_id of the queue record or the queue identifier in an external system.If using a queue\_id from an external system, it must be mapped to the Provider queue ID \(external\_id\) field on the awa\_queue record.

Data type: String

Table: Queue \[awa\_queue\]

</td></tr><tr><td>

transfer

</td><td>

Required for transfer assignments. Object containing information about the transfer.If a value is provided for this parameter, the assignment is considered a transfer assignment.

Data type: Object

```
{
   "source_queue_id": "String",
   "target_id": "String",
   "target_type": "String",
   "transfer_type": "String"
}
```

</td></tr><tr><td>

transfer.source\_queue\_id

</td><td>

Required for transfer assignments.Source queue from where the transfer is initiated. Sys\_id of the queue record or the queue identifier in an external system.

If using a queue\_id from an external system, it must be mapped to the Provider queue ID \(external\_id\) field on the awa\_queue record.

This parameter is used to create a work item before initiating the transfer if an active work item is not found. It enables transfers to be performed if the original interaction was created without any routing, such as for outbound calls.

Data type: String

Table: Queue \[awa\_queue\]

</td></tr><tr><td>

transfer.target\_id

</td><td>

Required for transfer assignments. Sys\_id of the agent or queue record to transfer the assignment to.-   If **target\_type** is `agent`, **target\_id** is the sys\_id of the agent user record in the User \[sys\_user\] table.
-   If **target\_type** is `queue`, **target\_id** is the sys\_id of the queue record in the Queue \[awa\_queue\] table or the queue identifier in an external system.

Data type: String

</td></tr><tr><td>

transfer.target\_type

</td><td>

Required for transfer assignments. Type of record to transfer the assignment to.Valid values:

-   agent
-   queue

Data type: String

</td></tr><tr><td>

transfer.transfer\_type

</td><td>

Required for transfer assignments. Type of transfer.Valid values:

-   blind
-   consult

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
|409|Conflict. The request couldn't be processed due to an error with the provided document’s work item or agent sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Response message with information about the assignment success or failure.Possible values:

-   `Manual assignment successfully requested` - Success.
-   `Caller <API_caller_sys_id> does not have the awa_manager or awa_integration_user role` – The authenticated user making the API request must have either the awa\_manager or awa\_integration\_user role.
-   `Work Item accepted can not be assigned` – Work item can't be assigned because it is already accepted by an agent. For more information, see [Check work items and AWA events](https://www.servicenow.com/docs/access?context=awa-work-items-all&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
-   `<agent_sys_id> is not a valid agent` – Agent doesn't have the awa\_agent role.
-   `Transfer failed - couldn't blind transfer to agent` - Assignment wasn't transferred because the agent isn't in the Available state in AWA.
-   `Work Item is already assigned to <agent_sys_id>` – Provided work item is assigned to another agent.
-   `Agent is not available` – Agent isn't in the Available state in AWA. For more information, see [Agent Inbox controls](https://www.servicenow.com/docs/access?context=agent-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
-   `Timeout value cannot be negative` – Provided timeout value can't be negative.
-   `<presence_state_sys_id> is not a valid presence state` – Provided presence state sys\_id doesn't exist in the AWA Presence State \[awa\_presence\_state\] table.
-   `Offered time (<offered_on_timestamp>) must be in the following format: yyyy-MM-dd'T'HH:mm:ss.SSS` – Provided offered\_on timestamp must use the specified format.
-   `Offered time (<offered_on_timestamp>) must be before the current time, otherwise agent will have more time to accept the work item` – Provided offered\_on timestamp can't be before the time the request is made.
-   `Timestamp after timeout (<offered_on_timestamp >) must be after the current time, otherwise agent has no time to accept the work item` – The timestamp after adding the timeout value to the provided offered\_on timestamp must be after the time the request was made.
-   `<display_option> is not a valid display option` – Provided display\_option must be one of the following values: `card_only` or `card_and_tab`.
-   `%s is not a valid boolean value` – Provided Boolean value must use one of the following formats: `yes/no`, `true/false`, `1/0`.
-   `The user does not have the 'awa_external_user' role` - Agent receiving the assignment must have the awa\_external\_user role.
-   `Document is not active` - Provided document must be active and not in a closed state.

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the assignment is successful.Possible values:

-   true: Assignment successful.
-   false: Assignment unsuccessful.

Data type: Boolean

</td></tr><tr><td>

work\_item

</td><td>

Details about the created or updated work item.Data type: Object

```
{ 
   "display_name": "String",
   "document_id": "String", 
   "document_table": "String", 
   "queue": "String", 
   "sys_id": "String" 
}
```

</td></tr><tr><td>

work\_item.display\_name

</td><td>

Display name of the document record.Data type: String

</td></tr><tr><td>

work\_item.document\_id

</td><td>

Sys\_id of the document record.Data type: String

</td></tr><tr><td>

work\_item.document\_table

</td><td>

Name of the table associated with the document.Data type: String

</td></tr><tr><td>

work\_item.queue

</td><td>

Sys\_id of the queue record or the queue identifier in an external system.Data type: String

Table: Queue \[awa\_queue\]

</td></tr><tr><td>

work\_item.sys\_id

</td><td>

Sys\_id of the work item.Data type: String

Table: Work Item \[awa\_work\_item\]

</td></tr></tbody>
</table>### cURL request

This example shows how to assign a work item to an agent.

```
curl "https://instance.servicenow.com/api/now/awa/documents/interaction/59616aba87bd5210be070d48dabb35e6/offer" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data '{ 
    "external_segment_id": "segment_59616aba87bd5210be070d48dabb35e6", 
    "queue_id": "92f8942787851210be070d48dabb35fb", 
    "assignment": { 
        "agent_sys_id": "0d584509c323120095ccd02422d3ae5b", 
        "allowed_to_decline": "true", 
        "enable_auto_assign": "false", 
        "timeout": 30, 
        "offered_on":"2024-04-03T23:09:31.000" 
    } 
}' 
--user 'username':'password'
```

The response shows that the work item is successfully assigned to the agent. You can verify the result in the Assigned to field of the Work Item \[awa\_work\_item\] record.

```
{ 
   "result": { 
      "work_item": { 
         "display_name": "Interaction: IMS0000221", 
         "sys_id": "bfa3a27e87bd5210be070d48dabb3588", 
         "document_id": "59616aba87bd5210be070d48dabb35e6", 
         "document_table": "interaction", 
         "queue": "92f8942787851210be070d48dabb35fb" 
      }, 
      "success": true, 
      "message": "Manual assignment successfully requested." 
   } 
}
```

