---
title: Conversation Member API
description: The Conversation Member API provides methods for changing a specific agent’s member state to removed or updated in a given Agent Chat conversation.Drops an agent from a conversation.Updates the agent's member type in a given conversation to a public fulfiller from an observer or private fulfiller type.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Conversation Member API

The Conversation Member API provides methods for changing a specific agent’s member state to removed or updated in a given Agent Chat conversation.

This API provides the ability to programmatically manage an agent member’s state in conversations in Agent Chat experience of Conversational Interfaces. See [Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ci-use-agent-chat.md) for more information.

This API is available by default. The calling user must have the awa\_integration\_user role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Conversation Member - PUT /now/conversation/member/\{user\_id\}/drop

Drops an agent from a conversation.

### URL format

Default URL: `/api/now/conversation/member/{user_id}/drop`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

user\_id

</td><td>

Sys\_id of the agent to drop from the conversation.Data type: String

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

interaction\_id

</td><td>

Required. Sys\_id of the conversation record to drop the agent from.Data type: String

Table: Interaction \[interaction\]

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

</td><td>

Error when processing Conversation Member operations. For example: -   Conversation is not found for the provided interaction.
-   User is not a member of the interaction conversation provided.

Provide a different user\_id or interaction\_id in the request.


</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code">

Forbidden. The user doesn't have access rights to the specified record.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conversation\_member

</td><td>

Object containing information about the agent status as a conversation member, after the drop request is processed.Data type: Object

```
"conversation_member": { 
  "active": Boolean, 
  "memberType": "String", 
  "conversation_id": "String"
}
```

</td></tr><tr><td>

conversation\_member.active

</td><td>

Flag that indicates whether the current user is present in the conversation.Possible values:

-   true: Agent is active in the conversation.
-   false: Agent is dropped from the conversation and is no longer an active participant in the chat.

Data type: Boolean

</td></tr><tr><td>

conversation\_member.memberType

</td><td>

Type of member agent.Possible values:

-   public\_fulfiller: Allows the agent to chat publicly with other agents and requestor in a the given conversation.
-   observer: Only available for the user with the manager role. Grants the right to look at the conversation content without joining the conversation.
-   private\_fulfiller: Allows agent to join a private chat between the agents to discuss the active conversation.

Data type: String

Table: Conversation Member \[sys\_cs\_conversation\_member\]

</td></tr><tr><td>

conversation\_member.conversation\_id

</td><td>

Required. Sys\_id of the conversation record that the agent was dropped from.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the drop agent process was successful. Valid values:

-   true: Agent dropped successfully.
-   false: Agent failed to be dropped and is still considered active in the conversation.

Data type: Boolean

</td></tr><tr><td>

message

</td><td>

Response message acknowledging successful assignment or exception.Success message: **Request to drop agent processed successfully.**

Possible exceptions:

-   **Invalid request. Insufficient input**: Agent sys\_id or interaction sys\_id isn’t provided in the request.
-   **Provided interaction is not a third party interaction**: Request only works for the third-party interaction and the given interaction\_id isn’t a third-party interaction.
-   **Conversation for corresponding interaction could not be found**: Can’t find the corresponding conversation record with the given interaction sys\_id.
-   **Invalid request. User is not a member of the interaction provided**: Agent sys\_id isn’t a member of the given interaction conversation.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example demonstrates how to drop the given Agent's user ID from the given interaction ID.

```
curl "https://instance.servicenow.com/api/now/conversation/member/0b10223c57a313005baaaa65ef94f970/drop" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\" interaction_id":\"27f675e3739713004a905ee515f6a7c3\"}" \ 
--user 'username':'password'
```

The response shows a successful drop operation for the given Agent from the interaction. Note that the active field is set to false and the message indicates a successful drop operation.

```
{
  "result": {
    "conversation_member": {
      "active": false,
      "memberType": "public_fulfiller",
      "conversation_id": "27f675e3739713004a905ee515f6a7c3"
    },
    "success": true,
    "message": "Request to drop agent processed successfully."
  }
}
```

## Conversation Member - PUT /now/conversation/member/\{user\_id\}/update

Updates the agent's member type in a given conversation to a public fulfiller from an observer or private fulfiller type.

You can only use this endpoint to update an agent's current observer or private fulfiller type to a public fulfiller type. This endpoint does not support switching the agent back to an observer or private type. The response returns a 500 status code if the given agent already holds a public fulfiller role.

The following scenario is an example of how an agent's member type is updated using the Conversation Member PUT update endpoint:

1.  The supervisor opens and observes an ongoing conversation which the agent is asking for help.
2.  The supervisor decides to join the conversation to offer help and clicks the 'Join Conversation' button in the UI. The join conversation request is sent to the third-party server.
3.  The third-party server processes the join conversation request and calls the Conversation Member PUT update endpoint and updates the supervisor's member type from observer to public fulfiller.
4.  The agent’s client UI reflects the updated conversation state.

### URL format

Versioned URL: `/api/now/{api_version}/conversation/member/{user_id}/update`

Default URL: `/api/now/conversation/member/{user_id}/update`

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

Sys\_id of the agent to update with a new member type in the conversation.Data type: String

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

interaction\_id

</td><td>

Required. Sys\_id of the conversation record in which to update the agent member type.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

member\_type

</td><td>

Required. Type of member to update the agent to in the given conversation.Only valid value: public\_fulfiller

Data type: String

Table: Conversation Member \[sys\_cs\_conversation\_member\], Field: Member Type

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

<table id="table_xbw_3v5_bfc"><thead><tr><th>

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

Error when processing Conversation Member operations. For example:

-   Conversation is not found for the provided interaction.
-   User is not a member of the interaction conversation provided.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

403

</td><td id="entry-403-status-code">

Forbidden. The user doesn't have access rights to the specified record.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_d1f_k55_bfc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conversation\_member

</td><td>

Object containing information about the agent member's state once the update request is processed.Data type: Object

```
"conversation_member": { 
  "active": Boolean, 
  "memberType": "String", 
  "conversation_id": "String"
}
```

</td></tr><tr><td>

conversation\_member.active

</td><td>

Flag that indicates whether the current user is present in the conversation.Possible values:

-   true: Agent is active in the conversation.
-   false: Agent is dropped from the conversation and is no longer an active participant in the chat.

Data type: Boolean

</td></tr><tr><td>

conversation\_member.memberType

</td><td>

Type of member agent.Possible values:

-   public\_fulfiller: Allows the agent to chat publicly with other agents and requestor in a the given conversation.
-   observer: Only available for the user with the manager role. Grants the right to look at the conversation content without joining the conversation.
-   private\_fulfiller: Allows agent to join a private chat between the agents to discuss the active conversation.

Data type: String

Table: Conversation Member \[sys\_cs\_conversation\_member\]

</td></tr><tr><td>

conversation\_member.conversation\_id

</td><td>

Sys\_id of the conversation record that the agent was updated in.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

success

</td><td>

Flag that indicates whether the update process was successful. Valid values:

-   true: Agent updated successfully.
-   false: Agent failed to be updated.

Data type: Boolean

</td></tr><tr><td>

message

</td><td>

Response message acknowledging successful assignment or exception.Success message: **Request to update agent member type processed successfully.**

Possible exceptions:

-   **Invalid request. Insufficient input**: agent sys\_id or interaction sys\_id is not provided in the request.
-   **Provided interaction is not a third party interaction**: the request only works for the third-party interaction and the given one is not third-party interaction.
-   **Invalid request. Member type must be one of \[allowed member type\]**: The member type provided in the request is not in one of the allowed type to be updated to.
-   **Conversation for corresponding interaction could not be found**: Cannot find the corresponding conversation record with the given interaction sys\_id.
-   **Invalid request. User is not a member of the interaction provided**: The given agent sys\_id is not a member of the given interaction conversation.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following request demonstrates how to update a Agent user to a public fulfiller role in a given conversation.

```
curl "https://instance.servicenow.com/api/now/conversation/member/{user_id}/update" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
 \"interaction_id"":\"< interaction_sys_id" >\", 
 \"member_type\":\"public_fulfiller\" 
}" \ 
--user 'username':'password'
```

The response returns information about the successful update to a public fulfiller role. Note that the memberType is updated but the active field remains true, indicating that the agent's type has changed but is still active in the conversation.

```
{
  "result": {
    "conversation_member": {
      "active": true,
      "memberType": "public_fulfiller",
      "conversation_id": " <conversation_sys_id>"
    },
    "success": true,
    "message": "Request to update agent member type processed successfully."
  }
}
```

