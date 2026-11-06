---
title: Virtual Agent Bot Integration API
description: The Virtual Agent Bot Integration API provides endpoints that allow users to integrate any chat interface or a bot ecosystem with the ServiceNow Virtual Agent and/or Live Agent.Sends a specified message, attachment, or URL to a specified secondary ServiceNow Virtual Agent \(VA\) bot.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/rest-apis/bot-api.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 38
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Virtual Agent Bot Integration API

The Virtual Agent Bot Integration API provides endpoints that allow users to integrate any chat interface or a bot ecosystem with the ServiceNow Virtual Agent and/or Live Agent.

This API is built on the conversational custom chat integration framework provided with Virtual Agent and operates in the `sn_va_as_service` namespace.

For additional information on installing and configuring the Virtual Agent Bot Integration API, see [Using Virtual Agent with a live agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/using-va-agent-chat.md).

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/api-rest.md)

## VA Bot Integration - POST /sn\_va\_as\_service/bot/integration

Sends a specified message, attachment, or URL to a specified secondary ServiceNow Virtual Agent \(VA\) bot.

A customer's site can have one or more secondary ServiceNow bots. In addition to passing messages to a ServiceNow VA secondary bot, the primary bot or chat client can use this endpoint to pass messages to an agent through Live Agent chat. Use the **action** parameter passed in the request body to specify how the specified content should be handled.

**Note:** This endpoint can be either synchronous or asynchronous depending on how it's configured. If asynchronous, when the request is received by the endpoint, it validates the request and responds with a call status of success or failure and the appropriate HTTP status code. The VA then processes the request and sends a second response to the configured response endpoint. For example, for a bot-to-bot integration, the second response would be to the URL of your primary bot. Both of these responses are defined below. For additional information on this configured response endpoint, see Configure the output response REST endpoint and outbound authentication for the Virtual Agent API.

**Note:** The responses in the code examples for this endpoint show what is sent from the VA to the configured response endpoint. They don't show the actual response to this endpoint which is a simple success or failure response.

### URL format

Default URL: `/api/sn_va_as_service/bot/integration`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="vabot-req-parms" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

Action that the VA should take.Valid values:

-   [AGENT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Switches the conversation from VA to Live Agent.
-   [CREATE\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Creates a chat interaction. Set **syncResponse** to `true` to process the request synchronously and eliminate timing issues.
-   [END\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Ends the chat conversation. The **message.text** parameter should be empty when using this action.
-   [FAULT\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Faults a conversation. When setting a FAULT\_CONVERSATION action, provide a description for the **cause** parameter.
-   [SEND\_HISTORY](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Updates only the chat history. The chat history can also be sent using standard message processing with the **history** parameter.
-   SET\_USER\_TIMEZONE: Sets the user’s time zone to the time zone specified in the **timezone** parameter. This time zone remains in effect until you reset it using this same parameter.
-   [START\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Starts a chat conversation.
-   [START\_CREATED\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Starts a chat conversation initiated using `CREATE_CONVERSATION`. Set **syncResponse** to `true` to process the request synchronously and eliminate timing issues.
-   [SWITCH](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): Switch the conversation to a topic that matches what is specified in the **intent.id** or **topic.name** parameters.

**Note:** Only use the `SWITCH` action for topic switching when the intent discovery happens in the primary bot. If the intent discovery happens in the ServiceNow® VA, use the **message.text** parameter.

-   TYPING/VIEWING: Displays the typing indicator in Live Agent. First send `TYPING` and then after the user finishes typing, send `VIEWING`.
-   [UPDATE\_MESSAGES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md): This action is used during live agent conversations and provides two message update functions for third-party chat integrations for the messages received from the live agent that are reflected on the agent chat panel:

    -   The latest message delivery status after sending a message from third-party.
    -   Updated text on the agent chat panel.
The third-party chat integration can update the text portion of the message before sending it to the end user. This action can be called to update the text on the agent chat panel so that the agent can see the updated text with an "Updated" tag.

This action is used with the **message.status** and **message.id** parameters.

This option is only valid if custom adapter property with name third\_party\_chat tied to provider application is set to `true`. This is a synchronous action irrespective of synchronous/asynchronous nature of the channel.

-   Null or parameter not passed: Sends the message to the ServiceNow VA.

The third-party chat integration can update the text message triggered from the live agent before sending it to the end user. This action can be called to update the text on the agent chat panel so that the agent can see the updated text with an "Updated" tag.

Data type: String

Default: Null

</td></tr><tr><td>

botToBot

</td><td>

Flag that indicates whether the conversation is between bots, such as between a primary bot and secondary bot.Possible values:

-   true: Bot-to-bot conversation.
-   false: Standalone ServiceNow bot conversation.

Data type: Boolean

Default: true

</td></tr><tr><td>

cause

</td><td>

Cause of a chat conversation fault, for example, `EXTERNAL_FAILURE`. This property is only used when the **action** property is set to **FAULT\_CONVERSATION**.Data type: String

</td></tr><tr><td>

clientSessionId

</td><td>

Unique client session identifier of the application/service that the end user is using to communicate with the ServiceNow botor the supported third-party chat applications.-   This ID helps identify the set of request/responses for a specific user conversation.
-   The format of this parameter is determined by the implementer.
-   This value is only updated if the value of the **third\_party\_chat** field is `true` in the **Custom Adapter Property** form.

Table: Interaction \[interaction\]

Data type: String

Default: Null

</td></tr><tr><td>

clientVariables

</td><td>

Pass-through JSON-formatted name-value pairs that are sent back in the response. These values aren't processed by the endpoint, but can be used to keep specific customer information attached to the conversation.Data type: Object

Default: Null

</td></tr><tr><td>

contextVariables

</td><td>

JSON-formatted name-value pairs that provide addition information about the user. Provide this information to customize the conversation experience. For additional information on context variables, see [Define and publish chat context variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/ac-configure-context-variables.md).For example:

```
"contextVariables": {
  "requester_session_language": "es", 
  "deviceTimeZone": "America/Los_Angeles"
  "live_agent_only": "true",
  "liveagent_deviceType": "test_device_type"
  "topic": "7c3c819073a3101066c7e9344ef6a7e4" 
} 
```

Data type: Object

Default: Null

</td></tr><tr><td>

emailId

</td><td>

Required when enabling account linking, otherwise all users are considered guest users. Email address of the chat client end user, the person the bot is interacting with. For additional information on account linking, see [Link your ServiceNow user account to a messaging application for Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/link-accounts-with-virtual-agent.md).Data type: String

</td></tr><tr><td>

history

</td><td>

History of the primary bot’s conversation with the user, starting with the initial request by the user.Data type: Object

```
"history": {
  "attachment": {Object},
  "displayName": "String",
  "isBotMessage": Boolean,
  "timestamp": "String",
  "type": "String",
  "value": "String"
}
```

</td></tr><tr><td>

history.attachment

</td><td>

Required when **history.type** is `attachment` \(ignored if **history.type** is `text`\). Details of each attachment sent in the historical message.Only a single attachment is allowed per **attachment** object.

Data type: Object

```
"attachment": {
    "clientAttachmentId": "String",
    "contentType": "String",
    "fileName": "String",
    "headers":{Object},
    "url": "String"
  }
```

</td></tr><tr><td>

history.attachment.clientAttachmentId

</td><td>

Unique identifier of the attachment. The format of this identifier is determined by the implementer. Data type: String

Default: Null

</td></tr><tr><td>

history.attachment.contentType

</td><td>

Required if **history.attachment** is specified. Standard mime type of the attachment. Valid values \(not case-sensitive\):

-   `application/pdf`
-   `application/msword`
-   `image/png`
-   `image/jpeg`
-   `text/plain`
-   `video/mpeg`

Data type: String

</td></tr><tr><td>

history.attachment.fileName

</td><td>

Required if **history.attachment** is specified. File name of the attachment.Data type: String

</td></tr><tr><td>

history.attachment.headers

</td><td>

Additional information needed if the attachment file is private and protected. Data type: Object

```
"headers": {
 "Authorization": "String"
}
```

</td></tr><tr><td>

history.attachment.headers.Authorization

</td><td>

Optional. Information needed to obtain authorization to access the attachment if it is private and protected, such as a user name and password.Data type: String

</td></tr><tr><td>

history.attachment.url

</td><td>

Required if **history.attachment** is specified. URL where the attachment is located.If the attachment isn't a public file, you must pass a **history.attachment.headers** object that contains the authorization information so that the attachment can be accessed. You must also ensure that the URL domain is present in the trusted domains field in the sys\_cs\_provider table.

Data type: String

</td></tr><tr><td>

history.displayName

</td><td>

Name of the user to whom the message was sent. If the primary bot, pass `Bot`.Data type: String

</td></tr><tr><td>

history.isBotMessage

</td><td>

Flag that indicates whether the message was sent by the primary bot.Valid values:

-   true: Message was sent by the primary bot.
-   false: Message was sent by the user.

Data type: Boolean

</td></tr><tr><td>

history.timestamp

</td><td>

Timestamp indicating the time at which the message was sent in milliseconds.Valid values: 13-digit Unix timestamp

Data type: String

</td></tr><tr><td>

history.type

</td><td>

Type of message sent.Valid values:

-   text
-   attachment

Data type: String

</td></tr><tr><td>

history.value

</td><td>

Content of the information. For example, the message text. Ignored when **history.type** is `attachment`.Data type: String

</td></tr><tr><td>

intent

</td><td>

Describes the intent of the conversation. Provide this information when the **action** parameter is set to `SWITCH`.Data type: Object

```
"intent": {
  "id": "String"
}
```

</td></tr><tr><td>

intent.id

</td><td>

NLU Intent ID of the system topic to switch the conversation to. The **intent.id** is resolved based on the language passed in the chat session. If no language is passed when starting a conversation, it obtains the language from the user's session/profile.Data type: String

Table: CS Topic Language \[sys\_cs\_topic\_language\]

</td></tr><tr><td>

message

</td><td>

Required. Details of the message to send to the ServiceNow bot.Data type: Object

```
"message": {
  "attachment": [Array of Objects],
  "clientMessageId": "String",
  "status": "String",
  "text": "String",
  "typed": Boolean
}
```

</td></tr><tr><td>

message.attachment

</td><td>

Required if sending attachments. Details of each attachment to send.You can only pass attachments as a URL. A virus scan is triggered on all attachments. There is no restriction on the size of an attachment, however, large files can take significant time to transfer.

Data type: Array of Objects

```
"attachment": [
  {
    "clientAttachmentId": "String",
    "contentType": "String",
    "fileName": "String",
    "headers":{Object},
    "id": "String",
    "url": "String"
  }
]
```

</td></tr><tr><td>

message.attachment.clientAttachmentId

</td><td>

Unique identifier of the attachment to send to the ServiceNow bot. The format of this identifier is determined by the implementer.Data type: String

Default: Null

</td></tr><tr><td>

message.attachment.contentType

</td><td>

Required if attachment specified. Standard mime type of the attachment.Valid values \(not case-sensitive\):

-   application/pdf
-   application/msword
-   image/png
-   image/jpeg
-   text/plain
-   video/mpeg

Data type: String

</td></tr><tr><td>

message.attachment.fileName

</td><td>

Required if attachment specified. File name of the attachment.Data type: String

</td></tr><tr><td>

message.attachment.headers

</td><td>

Additional information needed if the attachment file is private and protected.Data type: Object

```
"headers":{
  "Authorization":"String"	
}
```

</td></tr><tr><td>

message.attachment.headers.Authorization

</td><td>

Information needed to obtain authorization to access the attachment, such as a user name and password.Data type: String

</td></tr><tr><td>

message.attachment.url

</td><td>

Required if attachment specified. URL where the attachment is located. The VA obtains the attachment from this URL, runs a virus scan, and then processes the file. If the attachment isn't a public file, you must pass an **message.attachment.header** object that contains the authorization information so that the attachment can be accessed. You must also ensure that URL domain is present in the trusted domains filed in **sys\_cs\_provider**.Data type: String

</td></tr><tr><td>

message.clientMessageId

</td><td>

Unique alphanumeric identifier for the message. The format of this identifier is determined by the implementer.Data type: String

Default: Null

</td></tr><tr><td>

message.id

</td><td>

Only used with the **UPDATE\_MESSAGES** action. Unique ID of the chat message to be updated.Data type: String

</td></tr><tr><td>

message.status

</td><td>

Message status.Valid values \(not case-sensitive\):

-   external\_error - Used when message delivery is failed from third-party chat integration to end user. The agent chat panel will be reflected as a "Failed" tag.
-   sent\_to\_user - Initially a single tick mark displays for messages delivered from Live Agent to third- party chat integration. This status must be used when the message is successfully delivered from third-party chat integration to the end user. Upon success, the double tick mark displays on the agent chat panel.

Data type: String

</td></tr><tr><td>

message.text

</td><td>

Required if **attachment** parameter isn't specified. Message text. -   The language of the message should be passed in the **contextVariables** parameter.
-   Must be empty if the value of the action property is `END_CONVERSATION`.
-   Must be the updated text to be reflected on agent chat panel if the value of the action property is `UPDATE_MESSAGES`.

Data type: String

Maximum length: Unlimited

</td></tr><tr><td>

message.typed

</td><td>

Required. Flag that indicates whether the message was typed in or was an option selection \(selected\).Valid values:

-   true: Message was typed in by the user.
-   false: Message was an option selection.

Data type: Boolean

</td></tr><tr><td>

requestId

</td><td>

Required. Unique alphanumeric identifier for this request. The format of this identifier is determined by the implementer.Data type: String

</td></tr><tr><td>

silentMessage

</td><td>

Flag that indicates whether this is a silent message. A silent message is a message that doesn’t require a response.Valid values:

-   true: Silent message, no response message expected.
-   false: Regular message, response message expected.

**Note:** If a request with `silentMessage = true` is sent, all subsequent bot messages remain suppressed until a request to turn off silent mode is sent by passing `silentMessage = false`.

Data type: Boolean

Default: false

</td></tr><tr><td>

syncResponse

</td><td>

Applicable for CREATE\_CONVERSATION and START\_CREATED\_CONVERSATION actions. Flag that indicates whether to wait before returning a synchronous response from the API.

**Note:** This parameter prevents a potential race condition where the `Work Offer` API could be triggered before the `CREATE_CONVERSATION` and `START_CREATED_CONVERSATION` request finished processing. Making the response synchronous eliminates this timing issue.

 Valid values:

-   true: Returns a synchronous response.
-   false: Returns a response without waiting.

 Default: false

</td></tr><tr><td>

timestamp

</td><td>

Unix epoch time when the message was sent from the end user of the chat client.Data type: Number

Unit: Milliseconds

Default: Current time

</td></tr><tr><td>

timezone

</td><td>

GMT time zone of the end user of the chat client.For example:

```
"timezone":"Asia/Kolkata"
```

For a list of the available time zone values, see [https://en.wikipedia.org/wiki/List\_of\_tz\_database\_time\_zones](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).

Data type: String

Default: GMT time zone of the ServiceNow instance.

</td></tr><tr><td>

topic

</td><td>

Required if the user wants to switch to a particular topic by specifying a topic name. Name-value pair of the topic to switch to. You can either specify the topic name or the topic sys\_id.**Note:** You can only specify a single topic name or ID in the object.

Data type: Object

```
"topic": {
  "name": "String",
  "id": "String"
}
```

For example:

```
{​ 
  "requestId": "xxxx-xxxx-xxxx-xxxx",​
  "clientSessionId": "xxx-xxx-xxx-xxx",​
  "action":"SWITCH",​
  "topic":{​ 
    "name": "Topic Name"​
  },​ 
  "userId": "beth"​ 
}​ 
```

</td></tr><tr><td>

topic.name

</td><td>

Name of the topic to switch to.Data type: String

Table: In the name field of the Virtual Agent topics \[sys\_cs\_topic\] table.

</td></tr><tr><td>

topic.id

</td><td>

Sys\_id of the topic to switch to.Data type: String

Table: Virtual Agent topics \[sys\_cs\_topic\]

</td></tr><tr><td>

userId

</td><td>

Required. Unique user identifier. This is the identifier of the end user who is interacting with the bot.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr><tr><td>

token

</td><td>

Required if using token-based authentication; optional for Basic or OAuth authentication. Authentication token to use if token authentication has been set up for this endpoint.Data type: String

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Successful. The request was successfully processed.If you receive a 200 status code, but don’t receive a response back, check the following things:

-   Whether the request is failing in Static, JWT, or Hash Based Token validation, which generally happens in the worker thread of Virtual Agent.​
-   Whether the request body format is correct. If incorrect, the conversion doesn’t happen correctly.
-   Whether the request body is missing some required parameters. You can trace exceptions and errors in the System Logs on the ServiceNow instance.
-   Whether the site defined in the REST Message to receive the response is operational; able to detect in logs.
-   Ensure the REST Message that defines where to post the response is set correctly.

</td></tr><tr><td>

400

</td><td id="entry-400-status-code">

Bad Request. A bad request type or malformed request was detected.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

405

</td><td id="entry-405-status-code">

Invalid method. The functionality is disabled.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

Status of the endpoint call. This is sent in response when the initial call request is received. The request hasn’t yet been processed.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Description of the detected error. Only returned if an error occurs.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Details about the encountered error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message thrown.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the endpoint call.Valid values:

-   failure
-   success

Data type: String

</td></tr></tbody>
</table>### VA response body parameters

Response body sent from the VA to the configured response endpoint.

<table id="table_bql_jkx_zmb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agentChat

</td><td>

Flag that indicates whether the conversation is connected to the ServiceNow Live Agent.Possible values:

-   true: Chat messages are coming from a live agent.
-   false: Chat messages are coming from a bot and this parameter isn’t returned in the response.

Data type: Boolean

</td></tr><tr><td>

body

</td><td>

List of objects that describe the elements of the response message body.Data type: Array of Objects

```
"body": [
  {
    "actionType": "String",
    "agentInfo": {Object},
    "data": "String",
    "group": "String",
    "header": "String",
    "height": Number,
    "itemType": "String",
    "label": "String",
    "maskType": "String",
    "maxCount": Number,
    "maxSize": Number,
    "message": "String",
    "messageId": "String",
    "multiSelect": Boolean,
    "nluTextEnabled": Boolean,
    "options": {Object},
    "promptMsg": "String",
    "required": Boolean,
    "style": "String",
    "templateName": "String",
    "type": "String",
    "uiType": "String",
    "value": "String/{Object}",
    "width": Number
  }
]
```

</td></tr><tr><td>

body.actionType

</td><td>

Type of action message dispatched by the secondary bot to the primary bot. For example, typing indicator or agent wait time.Possible values:

-   EndTypingIndicator
-   StartSpinner
-   StartTypingIndicator

For example:

Sending `StartTypeIndicator` to the primary bot when the typing indicator is enabled.

```
"body": {​ 
  "uiType":"ActionMsg",​ 
  "actionType":"StartTypingIndicator"​ 
}  
```

Sending `StartSpinner` when transferring to Live Agent to display the wait time to the end user.

```
"body": { 
  "uiType":"ActionMsg", 
  "actionType":"StartSpinner", 
  "spinnerType":"wait_time",  
  "message":"Routing you to a live agent...", 
  "waitTime":"8 Seconds" 
} 
```

Data type: String

</td></tr><tr><td>

body.agentInfo

</td><td>

If enabled in the agent chat setup, the name and avatar of the associated agent. Data type: Object

```
"agentInfo":{   
  "agentAvatar":"String",
  "agentId":"String",
  "agentName": "String", 
  "sentFromAgent": Boolean
}
```

For example:

```
"agentInfo":{ 
  "sentFromAgent": true,
  "agentName":"Beth Anglin", 
  "agentAvatar":"https://instance.servicenow.com/ee4eebf30a0004d963b5c5ac0d734dc4.iix?t=small" 
} 
```

</td></tr><tr><td>

body.agentInfo.agentAvatar

</td><td>

URL of the agent's associated avatar file.For example: "https://instance.servicenow.com/ee4eebf30a0004d963b5c5ac0d734dc4.iix?t=small"

Data type: String

</td></tr><tr><td>

body.agentInfo.agentId

</td><td>

The sys\_id of the live agent.Table: Live Profile \[live\_profile\]

Data type: String

</td></tr><tr><td>

body.agentInfo.agentName

</td><td>

Display name of the agent.Data type: String

</td></tr><tr><td>

body.agentInfo.sentFromAgent

</td><td>

Flag that indicates whether the message was sent by a live agent.Possible values:

-   true: Sent by a live agent.
-   false: Sent by a virtual agent.

Data type: Boolean

</td></tr><tr><td>

body.data

</td><td>

JSON string that defines the data within the card.Data type: String

</td></tr><tr><td>

body.group

</td><td>

Rich control group to which the body element belongs. You can further transform these default controls by writing outbound transformation scripts. For additional information on these scripts, see [Virtual Agent action scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/va-action-scripts.md).Possible values:

-   DefaultOutputCard
-   DefaultDate
-   DefaultGroupedPartsOutputControl
-   DefaultHtml
-   DefaultOutputImage
-   DefaultOutputLink
-   DefaultText
-   DefaultPicker

Data type: String

</td></tr><tr><td>

body.header

</td><td>

Link header.Data type: String

</td></tr><tr><td>

body.height

</td><td>

Height of the HTML element.Data type: Number

Unit: Pixels

</td></tr><tr><td>

body.itemType

</td><td>

Type of body element.Possible values: \(case-sensitive\)

-   DefaultText
    -   File
    -   Image
    -   Inputtext
    -   outputtext
-   DefaultPicker
    -   Picture: Items appear in a carousel.
    -   List: Items appear in a dropdown-style list.

Data type: String

</td></tr><tr><td>

body.label

</td><td>

Label to display for the associated element.Data type: String

</td></tr><tr><td>

body.maskType

</td><td>

Sensitivity of the associated data.Possible values:

-   NONE: Associated data is of a general nature and doesn’t need to be secured.
-   SECURE: Associated data is of a sensitive nature and should be handled securely.

Data type: String

</td></tr><tr><td>

body.maxCount

</td><td>

Only returned when **uiType** is `FileUpload`. Maximum number of attachments that can be uploaded at one time.Data type: Number \(Integer\)

</td></tr><tr><td>

body.maxSize

</td><td>

Only returned when **uiType** is `FileUpload`. Maximum size of the attachment that can be uploaded.Data type: Number \(Integer\)

Unit: Megabytes

</td></tr><tr><td>

body.message

</td><td>

Only returned when **actionType** is `StartSpinner`. Message to display to user.Data type: String

</td></tr><tr><td>

body.messageId

</td><td>

Unique identifier for the message sent to the supported third-party chat applications from the ServiceNow Virtual Agent.Table: Conversation Message \[sys\_cs\_message\]

Data type: String

</td></tr><tr><td>

body.multiSelect

</td><td>

Flag that indicates whether the user can select multiple options.Possible values:

-   true: Multiple selections.
-   false: Single selection.

Data type: Boolean

</td></tr><tr><td>

body.nluTextEnabled

</td><td>

Flag that indicates whether the user chat client can receive Natural Language Understanding \(NLU\) text messages.Possible values:

-   true: Can receive NLU messages.
-   false: Can’t receive NLU messages.

Data type: Boolean

</td></tr><tr><td>

body.options

</td><td>

List that describes the options available for a picker control.Data type: Array of Objects

```
"options": [
  {
    "attachment": "String",
    "description": "String",
    "enabled": Boolean,
    "label": "String",
    "renderStyle": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

body.options.attachment

</td><td>

URL of the image in the carousel to retrieve.Data type: String

</td></tr><tr><td>

body.options.description

</td><td>

Description of the carousel item.Data type: String

</td></tr><tr><td>

body.options.enabled

</td><td>

Flag that indicates whether the picker control is enabled on the end user's chat client. In bot-to-bot implementations, the primary bot is responsible for ensuring the picker control is disabled.Possible values:

-   true: Enabled
-   false: Disabled

Data type: Boolean

</td></tr><tr><td>

body.options.label

</td><td>

Label to display for the associated **body.options.value** parameter.Data type: String

</td></tr><tr><td>

body.options.renderStyle

</td><td>

Style to use when rendering the associated element.Possible value: data

Data type: String

</td></tr><tr><td>

body.options.value

</td><td>

Value to display for the associated **body.options.label** parameter.Data type: String

</td></tr><tr><td>

body.promptMsg

</td><td>

Prompt message to display with the picker control.Data type: String

</td></tr><tr><td>

body.required

</td><td>

Flag that indicates whether the end user must respond to the query in the body element.Possible values:

-   true: Required
-   false: Optional

Data type: Boolean

</td></tr><tr><td>

body.spinnerType

</td><td>

Only returned when **actionType** is `StartSpinner`. Type of spinner shown to chat user.Possible values:

`wait_time:` Message indicating the amount of delay before being transferred to a live agent.

Data type: String

</td></tr><tr><td>

body.style

</td><td>

Style of body element.Possible values:

-   button
-   carousel
-   list
-   null

Data type: String

</td></tr><tr><td>

body.templateName

</td><td>

Name of the template to use to display the associated card.Data type: String

</td></tr><tr><td>

body.type

</td><td>

Only returned for DefaultOutputLink. Type of return data.Possible values: link

Data type: String

</td></tr><tr><td>

body.uiType

</td><td>

Type of body element. The possible values depend on the value in the **body.group** parameter. These values map back to the controls defined in the Virtual Agent Designer. For more information, see [Getting started with Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/conversation-designer-virtual-agent.md).Possible values:

-   ActionMsg
-   DefaultOutputCard

OutputCard

-   DefaultDate
    -   Date
    -   DateTime
    -   Time
-   DefaultGroupedPartsOutputControl

GroupedPartsOutputControl

-   DefaultHtml

OutputHtml

-   DefaultOutputImage

OutputImage

-   DefaultOutputLink

OutputLink

-   DefaultText
    -   InputText
    -   OutputText
    -   FileUpload
-   DefaultPicker
    -   Picker
    -   TopicPickerControl
    -   Boolean

Data type: String

</td></tr><tr><td>

body.value

</td><td>

Data to use to process the body element. The type of information that is passed back depends on the type of body element.OutputLink: Object.

```
"value": {
  "action": "String"
}
```

OutputImage: String. Image URL.

OutputHtml: String. HTML that the client needs to render.

Data type: String or Object

</td></tr><tr><td>

body.value.action

</td><td>

Only returned for DefaultOutputLink. URL of returned link.Data type: String

</td></tr><tr><td>

body.waitTime

</td><td>

Amount of time that the user has to wait before being connected to a live agent.Data type: String

</td></tr><tr><td>

body.width

</td><td>

Width of the associated HTML element.Data type: Number

Unit: Pixels

</td></tr><tr><td>

clientSessionId

</td><td>

Unique client session identifier of the chat application/service that the end user is using to communicate with the ServiceNow bot.Data type: String

</td></tr><tr><td>

clientVariables

</td><td>

JSON-formatted name-value pairs that are copied from what is passed in the **clientVariables** parameter in the request body. These values aren’t processed by the endpoint, but can be used to keep specific customer information attached to the conversation.Data type: Object

</td></tr><tr><td>

completed

</td><td>

Flag that indicates whether the ServiceNow Virtual Agent has successfully completed the conversation.Possible values:

-   true: Conversation has been successfully completed.
-   false: Conversation isn’t complete and this parameter isn’t returned in the response.

Data type: Boolean

</td></tr><tr><td>

enterpriseId

</td><td>

Currently unused.

</td></tr><tr><td>

interactionId

</td><td>

Unique identifier for each conversation between the ServiceNow Virtual Agent and the supported third-party chat applications.Data type: String

</td></tr><tr><td>

message

</td><td>

Details of the message sent to the ServiceNow VA. This is the same as the passed in message object.Data type: Object

```
"message": {
  "attachment": {Object},
  "clientMessageId": "String",
  "text": "String",
  "typed": Boolean
}
```

</td></tr><tr><td>

message.attachment

</td><td>

Details of the attachment. Attachments can be either a file or a URL.Data type: Object

```
"attachment": {
  "clientAttachmentId": "String",
  "contentType": "String",
  "fileName": "String",
  "url": "String"
```

</td></tr><tr><td>

message.attachment.clientAttachmentId

</td><td>

Unique identifier of the attachment sent to the ServiceNow VA. The format of this identifier is determined by the implementer.Data type: String

</td></tr><tr><td>

message.attachment.contentType

</td><td>

Standard mime type of the attachment.Possible values \(not case-sensitive\):

-   application/msword
-   application/pdf
-   image/jpeg
-   image/png
-   text/plain
-   video/mpeg

Data type: String

</td></tr><tr><td>

message.attachment.fileName

</td><td>

File name of the attachment.Data type: String

</td></tr><tr><td>

message.attachment.url

</td><td>

URL where the attachment is located.Data type: String

</td></tr><tr><td>

message.clientMessageId

</td><td>

Unique alphanumeric identifier for the message.Data type: String

</td></tr><tr><td>

message.text

</td><td>

Message text.Data type: String

Maximum length: Unlimited

</td></tr><tr><td>

message.typed

</td><td>

Flag that indicates whether the message was typed in or was an option selection \(selected\).Possible values:

-   true: Message was typed in by the user.
-   false: Message was an option selection.

Data type: Boolean

</td></tr><tr><td>

nowBotId

</td><td>

Currently unused.

</td></tr><tr><td>

nowSessionId

</td><td>

Currently unused.

</td></tr><tr><td>

requestId

</td><td>

Unique identifier for this request.Data type: String

</td></tr><tr><td>

score

</td><td>

Intent confidence score from the ServiceNow NLU model, specified as a percent, such as 87.3%. This score enables the primary bot to make the decision whether to surface the associated intent based on the primary bot’s NLU model’s confidence threshold. The ServiceNow NLU model’s confidence threshold is ignored on the ServiceNow instance so that the primary bot’s NLU model’s confidence threshold can be consistently applied across all secondary bots.Data type: Number

</td></tr><tr><td>

takeControl

</td><td>

Flag that indicates that the ServiceNow Virtual Agent wants to hand control back over to the primary bot.Possible values:

-   true: Return control to the primary bot.
-   false: Keep control.

Data type: Boolean

Default: false

</td></tr><tr><td>

userId

</td><td>

Identifier of the end user who is interacting with the bot.Data type: String

</td></tr></tbody>
</table>### Start a conversation using the START\_CONVERSATION action

This example starts a new conversation for the user jane.doe by using the [START\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action. Because the message text is empty, Virtual Agent responds with its greeting and a list of topics the user can choose from.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-001",
  "action": "START_CONVERSATION",
  "enterpriseId": "ExampleCompany",
  "nowBotId": "EXAMPLE_BOT_ID",
  "clientSessionId": "",
  "nowSessionId": "",
  "message":{
    "text": "",
    "typed": true,
    "clientMessageId": "msg-001"
  },
  "userId": "jane.doe",
  "emailId": "jane.doe@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It contains a greeting message and a topic picker with two available topics.

```
{
  "requestId":"example-request-001",
  "clientSessionId":"",
  "nowSessionId":"",
  "message":{
    "text":"",
    "typed":true,
    "clientMessageId":"msg-001"
  },
  "userId":"jane.doe",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "value":"Hi, I'm your Virtual Agent. Let me know how I can help you today.",
      "maskType":"NONE"
    },
    {
      "uiType":"TopicPickerControl",
      "group":"DefaultPicker",
      "nluTextEnabled":false,
      "promptMsg":"Hi guest, please enter your request or make a selection of what I can help with. You can type help any time when you need help.",
      "label":"Show me everything",
      "options":[
        {
          "label":"Order Status",
          "value":"1111aaaa1111aaaa1111aaaa1111aaaa",
          "enabled":true
        },
        {
          "label":"Live Agent Support.",
          "value":"2222bbbb2222bbbb2222bbbb2222bbbb",
          "enabled":true
        }
      ]
    }
  ],
  "score":1
}
```

### Create a chat interaction

This example uses the [CREATE\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action to create a chat interaction for the user john.smith. The response returns the IDs of the new conversation, interaction, and message, which you can use in later requests.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-002",
  "clientSessionId": "",
  "action": "CREATE_CONVERSATION",
  "message": {
    "text": "hi",
    "typed": false
  },
  "userId": "john.smith",
  "emailId": "john.smith@example.com"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It confirms that the conversation was created and includes the generated IDs.

```
{
  "requestId": "example-request-002",
  "clientSessionId": "",
  "message": {
    "text": "hi",
    "typed": false
  },
  "userId": "john.smith",
  "interactionId": "abcd1234abcd1234abcd1234abcd1234",
  "body": [
    {
      "uiType": "ActionMsg",
      "actionType": "CreateConversation",
      "conversationId": "bcde2345bcde2345bcde2345bcde2345",
      "interactionId": "abcd1234abcd1234abcd1234abcd1234",
      "messageId": "cdef3456cdef3456cdef3456cdef3456"
    }
  ],
  "score": 1
}
```

### Start a synchronous CREATE\_CONVERSATION conversation

This example creates a conversation for jane.doe by using the [CREATE\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action with **syncResponse** set to `true`. Virtual Agent finishes processing the request before it responds, which avoids timing issues with follow-up requests. The context variables route the conversation to a live agent and pass an external session identifier.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
  --request POST \
  --header "Accept:application/json" \
  --header "Content-Type:application/json" \
  --data '{
    "requestId": "example-request-003",
    "userId": "jane.doe",
    "emailId": "jane.doe@example.com",
    "action": "CREATE_CONVERSATION",
    "syncResponse": true,
    "message": {},
    "contextVariables": {
      "live_agent_only": "true",
      "interaction_client_session_id": "external-session-001"
    },
    "appInboundId": "EXAMPLE_APP"
  }' \
  --user "username":"password"
```

Because the request is synchronous, the response is returned directly with the IDs of the new conversation, interaction, and message.

```
{
  "requestId": "example-request-003",
  "message": {},
  "userId": "jane.doe",
  "appInboundId": "EXAMPLE_APP",
  "body": [
    {
      "uiType": "ActionMsg",
      "actionType": "CreateConversation",
      "conversationId": "def04567def04567def04567def04567",
      "interactionId": "ef015678ef015678ef015678ef015678",
      "messageId": "f0126789f0126789f0126789f0126789"
    }
  ],
  "score": 1
}
```

### Start a conversation initiated using the START\_CREATED\_CONVERSATION action

This example starts a conversation that was previously created with the CREATE\_CONVERSATION action. The request identifies the user, and Virtual Agent responds with a greeting and a list of available topics.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-004",
  "clientSessionId": "",
  "action": "START_CREATED_CONVERSATION",
  "userId": "john.smith",
  "emailId": "john.smith@example.com"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It contains a greeting message and a topic picker listing nine example topics.

```
{
  "requestId":"example-request-004",
  "clientSessionId":"",
  "message":{},
  "userId":"john.smith",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "value":"Hi, I'm your Virtual Agent. Let me know how I can help you today.",
      "maskType":"NONE"
    },
    {
      "uiType":"TopicPickerControl",
      "group":"DefaultPicker",
      "nluTextEnabled":false,
      "promptMsg":"Hi guest, please enter your request or make a selection of what I can help with. You can type help any time when you need help.",
      "label":"Show me everything",
      "options":[
        {
          "label":"Order Status",
          "value":"1111aaaa1111aaaa1111aaaa1111aaaa",
          "enabled":true
        },
        {
          "label":"Reset Password",
          "value":"3333cccc3333cccc3333cccc3333cccc",
          "enabled":true
        },
        {
          "label":"Request Time Off",
          "value":"4444dddd4444dddd4444dddd4444dddd",
          "enabled":true
        },
        {
          "label":"Submit an IT Request",
          "value":"5555eeee5555eeee5555eeee5555eeee",
          "enabled":true
        },
        {
          "label":"Report an Issue",
          "value":"6666ffff6666ffff6666ffff6666ffff",
          "enabled":true
        },
        {
          "label":"Frequently Asked Questions",
          "value":"7777aaaa7777aaaa7777aaaa7777aaaa",
          "enabled":true
        },
        {
          "label":"Update Profile",
          "value":"8888bbbb8888bbbb8888bbbb8888bbbb",
          "enabled":true
        },
        {
          "label":"Live Agent Support.",
          "value":"2222bbbb2222bbbb2222bbbb2222bbbb",
          "enabled":true
        },
        {
          "label":"Track a Request",
          "value":"9999cccc9999cccc9999cccc9999cccc",
          "enabled":true
        }
      ]
    }
  ],
  "score":1
}
```

### Start a synchronous START\_CREATED\_CONVERSATION conversation

This example starts a previously created conversation for jane.doe with **syncResponse** set to `true`. Virtual Agent processes the request before it responds, and the response includes the conversation details and the messages needed to connect the user to a live agent.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
  --request POST \
  --header "Accept:application/json" \
  --header "Content-Type:application/json" \
  --data '{
  "requestId": "example-request-005",
  "userId": "jane.doe",
  "emailId": "jane.doe@example.com",
  "action": "START_CREATED_CONVERSATION",
  "syncResponse": true,
  "message": {},
  "appInboundId": "EXAMPLE_APP"
  }' \
  --user "username":"password"
```

The response returns the conversation ID, the support queue subscription, a wait-time message, and the chat presence details for the user.

```
{
  "requestId": "example-request-005",
  "message": {},
  "userId": "jane.doe",
  "appInboundId": "EXAMPLE_APP",
  "body": [
    {
      "uiType": "ActionMsg",
      "actionType": "StartConversation",
      "conversationId": "def04567def04567def04567def04567",
      "messageId": "0123789a0123789a0123789a0123789a"
    },
    {
      "uiType": "ActionMsg",
      "actionType": "SubscribeToSupportQueue",
      "supportQueue": "{@type=InteractionQueue, external=false, type=interaction, queueAmbChannel=/cs/support_queue/c3lzX2lkPW51bGw=}",
      "messageId": "1234890b1234890b1234890b1234890b"
    },
    {
      "uiType": "ActionMsg",
      "actionType": "StartSpinner",
      "spinnerType": "none",
      "message": "Routing you to a live agent...",
      "waitTime": "13 Seconds",
      "messageId": "2345901c2345901c2345901c2345901c"
    },
    {
      "uiType": "ActionMsg",
      "actionType": "SubscribeToChatPresence",
      "channel": "/sn/rp/sys_cs_conversation/def04567def04567def04567def04567",
      "userDetails": "{name=Guest, sysId=7890456b7890456b7890456b7890456b, avatarPath=null, displayName=Guest, initials=G, showNameInHeader=false, userName=guest, email=guest@example.com, channel=null}",
      "chatSessionId": "def04567def04567def04567def04567",
      "messageId": "3456012d3456012d3456012d3456012d"
    }
  ],
  "agentChat": true,
  "score": 1
}
```

### Fault a conversation using

This example uses the [FAULT\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action to mark a conversation as failed for john.smith. The **cause** parameter describes the reason for the fault, and the response returns control to the primary bot.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-006",
  "clientSessionId": "",
  "action": "FAULT_CONVERSATION",
  "cause": "EXTERNAL_FAILURE",
  "userId": "john.smith",
  "emailId": "john.smith@example.com"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. The empty body and **takeControl** value of `true` indicate that the primary bot now has control of the conversation.

```
{
  "requestId": "example-request-006",
  "clientSessionId": "",
  "userId": "john.smith",
  "body": [],
  "takeControl": true,
  "score": 0
}
```

### Update the message on the agent chat panel

This example uses the [UPDATE\_MESSAGES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action during a live agent conversation to report that delivery of a message to the end user failed. The agent chat panel then shows a `Failed` tag on that message. The action accepts a list of messages, so you can update several messages in one request.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-007",
  "clientSessionId": "",
  "message": [
    {
      "status": "external_error",
      "id": "4567123e4567123e4567123e4567123e"
    }
  ],
  "userId": "john.smith",
  "emailId": "john.smith@example.com",
  "action": "UPDATE_MESSAGES"
}"
--user "username":"password"
```

Virtual Agent sends the following confirmation message to the configured response endpoint.

```
Message Processed Successfully
```

### Update only chat history

This example uses the [SEND\_HISTORY](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action to send the earlier part of a conversation, including one attachment, from the primary bot to Virtual Agent. The history gives a live agent context for the conversation without starting a new message exchange.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-008",
  "clientSessionId": "",
  "userId": "jane.doe",
  "emailId": "jane.doe@example.com",
  "action": "SEND_HISTORY",
  "history": [
    {
      "isBotMessage": true,
      "value": "How can I help you?",
      "displayName": "Bot",
      "type": "text",
      "timestamp": "1760000000000"
    },
    {
      "isBotMessage": false,
      "value": "I am facing an issue while creating an incident.",
      "displayName": "User",
      "type": "text",
      "timestamp": "1760000030000"
    },
    {
      "isBotMessage": false,
      "displayName": "User",
      "type": "attachment",
      "timestamp": "1760000060000",
      "attachment": {
        "clientAttachmentId": "attachment-001",
        "contentType": "application/pdf",
        "fileName": "sample.pdf",
        "url": "https://example.com/files/sample.pdf"
      }
    },
    {
      "isBotMessage": true,
      "value": "Okay. I am routing you to an agent.",
      "displayName": "Bot",
      "type": "text",
      "timestamp": "1760000090000"
    },
    {
      "isBotMessage": false,
      "value": "Thanks.",
      "displayName": "User",
      "type": "text",
      "timestamp": "1760000120000"
    }
  ]
}"
--user "username":"password"
```

Virtual Agent sends the following success response to the configured response endpoint.

```
{"status": "success"}
```

### Transfer a conversation to Live Agent using utterance

This example transfers a conversation to Live Agent without going through the greeting topic. The request passes `agent` as the utterance in **message.text** and includes a bot token in the request header. Possible utterance values are defined in the sys\_cs\_contextual\_action table. Virtual Agent responds with a list of options so the user can confirm what they want to do.

For additional information on contextual actions, see [Contextual actions for custom chat integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/contextual-actions.md).

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--header "token: BOT_TOKEN" \
--data " {
  "requestId": "example-request-009",
  "botToBot": true,
  "clientSessionId": "",
  "silentMessage": false,
  "message":{
    "text": "agent",
    "typed": true
  },
  "userId": "jane.doe",
  "emailId": "jane.doe@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
```

Virtual Agent sends the following response to the configured response endpoint. It asks the user to confirm the intended action from a list of options.

```
{
  "requestId":"example-request-009",
  "clientSessionId":"",
  "message":{
    "text":"agent",
    "typed":true
  },
  "userId":"jane.doe",
  "body":[
    {
      "uiType":"Picker",
      "group":"DefaultPicker",
      "required":true,
      "nluTextEnabled":false,
      "label":"I want to be sure I got this right. What item best describes what you want to do?",
      "itemType":"List",
      "style":"list",
      "multiSelect":false,
      "options":[
        {
          "label":"Live Agent Support.",
          "value":"Live Agent Support.",
          "renderStyle":"data",
          "enabled":false
        },
        {
          "label":"Virtual Agent Capabilities.",
          "value":"Virtual Agent Capabilities.",
          "renderStyle":"data",
          "enabled":false
        },
        {
          "label":"I want something else",
          "value":"-1",
          "renderStyle":"data",
          "enabled":false
        }
      ],
      "scriptedData":null
    }
  ],
  "score":1
}
```

### Transfer a conversation to Live Agent Support based on the user's selection

This example continues the previous one. The user selected Live Agent Support from the list, and the request sends that selection as the message text. Virtual Agent then connects the user to a live agent.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--header "token: BOT_TOKEN" \
--data "{
  "requestId": "example-request-010",
  "botToBot": true,
  "clientSessionId": "",
  "silentMessage": false,
  "message":{
    "text": "Live Agent Support.",
    "typed": true
  },
  "userId": "jane.doe",
  "emailId": "jane.doe@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
} "
```

Virtual Agent sends the following response to the configured response endpoint. The **agentChat** value of true indicates that the conversation is now connected to Live Agent.

```
{
  "requestId":"example-request-010",
  "clientSessionId":"",
  "message":{
    "text":"Live Agent Support.",
    "typed":true
  },
  "userId":"jane.doe",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "value":"Please stand by while I connect you to a live agent."
    }
  ],
  "agentChat":true,
  "score":1
}
```

### End a Virtual Agent conversation by setting the action parameter

This example ends a conversation with Virtual Agent by setting the **action** parameter to [END\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md). The message text is empty, as this action requires.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-011",
  "action": "END_CONVERSATION",
  "enterpriseId": "ExampleCompany",
  "nowBotId": "EXAMPLE_BOT_ID",
  "clientSessionId": "",
  "nowSessionId": "",
  "message":{
    "text": "",
    "typed": true,
    "clientMessageId": "msg-002"
  },
  "userId": "jane.doe",
  "emailId": "jane.doe@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It shows a message confirming that the conversation has ended.

```
{
  "requestId":"example-request-011",
  "clientSessionId":"",
  "nowSessionId":"",
  "message":{
    "text":"",
    "typed":true,
    "clientMessageId":"msg-002"
  },
  "userId":"jane.doe",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "value":"The conversation has ended. If you need help again, type hi.",
      "maskType":"NONE"
    }
  ],
  "score":1
}
```

### End a Live Agent conversation by setting the action parameter

This example ends a conversation that is connected to a live agent by setting the **action** parameter to [END\_CONVERSATION](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md). The request is the same as for a Virtual Agent conversation, but the response also includes the completed flag.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-012",
  "action": "END_CONVERSATION",
  "enterpriseId": "ExampleCompany",
  "nowBotId": "EXAMPLE_BOT_ID",
  "clientSessionId": "",
  "nowSessionId": "",
  "message":{
    "text": "",
    "typed": true,
    "clientMessageId": "msg-003"
  },
  "userId": "jane.doe",
  "emailId": "jane.doe@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. The completed value of true indicates that the conversation finished successfully.

```
{
  "requestId":"example-request-012",
  "clientSessionId":"",
  "nowSessionId":"",
  "message":{
    "text":"",
    "typed":true,
    "clientMessageId":"msg-003"
  },
  "userId":"jane.doe",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "value":"The conversation has ended. If you need help again, type hi.",
      "maskType":"NONE"
    }
  ],
  "completed":true,
  "score":1
}
```

### Use commands defined in the sys\_cs\_contextual\_action table as an utterance to start a conversation with Virtual Agent

This example starts a conversation by sending the Spanish greeting “hola” as the message text instead of setting the action parameter to `START_CONVERSATION`. Virtual Agent recognizes “hola” as a language variant of the **Hi** command \(defined in the sys\_cs\_contextual\_action table as an utterance\) and responds with its greeting and a list of topics.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--header "token: BOT_TOKEN" \
--data "{
  "requestId": "example-request-013",
  "botToBot": true,
  "clientSessionId": "",
  "silentMessage": false,
  "message":{
    "text": "hola",
    "typed": true
  },
  "userId": "john.smith",
  "emailId": "john.smith@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
```

Virtual Agent sends the following response to the configured response endpoint. It contains a greeting message and a topic picker listing nine example topics.

```
{
  "requestId":"example-request-013",
  "clientSessionId":"",
  "message":{
    "text":"hola",
    "typed":true
  },
  "userId":"john.smith",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "value":"Hi, I'm your Virtual Agent. Let me know how I can help you today.",
      "maskType":"NONE"
    },
    {
      "uiType":"TopicPickerControl",
      "group":"DefaultPicker",
      "nluTextEnabled":false,
      "promptMsg":"Hi guest, please enter your request or make a selection of what I can help with. You can type help any time when you need help.",
      "label":"Show me everything",
      "options":[
        {
          "label":"Order Status",
          "value":"1111aaaa1111aaaa1111aaaa1111aaaa",
          "enabled":true
        },
        {
          "label":"Reset Password",
          "value":"3333cccc3333cccc3333cccc3333cccc",
          "enabled":true
        },
        {
          "label":"Request Time Off",
          "value":"4444dddd4444dddd4444dddd4444dddd",
          "enabled":true
        },
        {
          "label":"Submit an IT Request",
          "value":"5555eeee5555eeee5555eeee5555eeee",
          "enabled":true
        },
        {
          "label":"Report an Issue",
          "value":"6666ffff6666ffff6666ffff6666ffff",
          "enabled":true
        },
        {
          "label":"Frequently Asked Questions",
          "value":"7777aaaa7777aaaa7777aaaa7777aaaa",
          "enabled":true
        },
        {
          "label":"Update Profile",
          "value":"8888bbbb8888bbbb8888bbbb8888bbbb",
          "enabled":true
        },
        {
          "label":"Live Agent Support.",
          "value":"2222bbbb2222bbbb2222bbbb2222bbbb",
          "enabled":true
        },
        {
          "label":"Track a Request",
          "value":"9999cccc9999cccc9999cccc9999cccc",
          "enabled":true
        }
      ]
    }
  ],
  "score":1
}
```

### Use commands defined in the sys\_cs\_contextual\_action table as an utterance to end a conversation

This example ends a conversation by sending the Spanish farewell “chao” as the message text instead of setting the action parameter to `END_CONVERSATION`. Virtual Agent recognizes “chao” as a language variant of the **Bye** command and asks the user to confirm before it ends the conversation.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--header "token: BOT_TOKEN" \
--data "{
  "requestId": "example-request-014",
  "botToBot": true,
  "clientSessionId": "",
  "silentMessage": false,
  "message":{
    "text": "chao",
    "typed": true
  },
  "userId": "john.smith",
  "emailId": "john.smith@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
```

Virtual Agent sends the following response to the configured response endpoint. It asks the user to choose between ending the conversation and canceling.

```
{
  "requestId":"example-request-014",
  "clientSessionId":"",
  "message":{
    "text":"chao",
    "typed":true
  },
  "userId":"john.smith",
  "body":[
    {
      "uiType":"Picker",
      "group":"DefaultPicker",
      "required":true,
      "nluTextEnabled":false,
      "label":"Please make a selection.",
      "itemType":"List",
      "style":"list",
      "multiSelect":false,
      "options":[
        {
          "label":"End conversation",
          "value":"1",
          "renderStyle":"data",
          "enabled":false
        },
        {
          "label":"Cancel",
          "value":"0",
          "renderStyle":"data",
          "enabled":false
        }
      ],
      "scriptedData":null
    }
  ],
  "score":1
}
```

### Change an ongoing conversation using the SWITCH action parameter

This example uses the [SWITCH](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action to move an ongoing conversation to a different topic. The **intent.id** parameter identifies the topic to switch to, in this case a topic for checking order status. Virtual Agent responds with the first prompt of that topic.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-015",
  "enterpriseId": "ExampleCompany",
  "nowBotId": "EXAMPLE_BOT_ID",
  "clientSessionId": "",
  "nowSessionId": "",
  "action": "SWITCH",
  "intent" : {
    "id": "Check Order Status"
  },
  "message":{
    "typed": true,
    "clientMessageId": "msg-004"
  },
  "userId": "Guest",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It shows that the conversation switched to the new topic and is now asking for an order number.

```
{
   "requestId":"example-request-015",
   "clientSessionId":"",
   "nowSessionId":"",
   "message":{
      "typed":true,
      "clientMessageId":"msg-004"
   },
   "userId":"Guest",
   "body":[
      {
         "uiType":"InputText",
         "group":"DefaultText",
         "required":true,
         "nluTextEnabled":false,
         "label":"Enter your order number:",
         "maskType":"NONE"
      }
   ],
   "score":1
}
```

### Obtain a \(NLU\) confidence score for an utterance

This example sends a free-text utterance to Virtual Agent when Natural Language Understanding \(NLU\) is enabled. Virtual Agent matches the utterance to a topic and returns an NLU confidence score along with the first prompt of that topic. The primary bot can use the score to decide whether to surface the matched intent.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-016",
  "enterpriseId": "ExampleCompany",
  "nowBotId": "EXAMPLE_BOT_ID",
  "clientSessionId": "",
  "nowSessionId": "",
  "message":{
    "text": "I want to check my order status",
    "typed": true,
    "clientMessageId": "msg-005"
  },
  "userId": "Guest",
  "timestamp": 1588824102,
  "timezone": "America/New_York"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. The score value is the NLU confidence score for the matched topic.

```
{
  "requestId":"example-request-016",
  "clientSessionId":"",
  "nowSessionId":"",
  "message":{
    "text":"I want to check my order status",
    "typed":true,
    "clientMessageId":"msg-005"
  },
  "userId":"Guest",
  "body":[
    {
      "uiType":"InputText",
      "group":"DefaultText",
      "required":true,
      "nluTextEnabled":false,
      "label":"Enter your order number:",
      "maskType":"NONE"
    }
  ],
  "score":"0.92"
}
```

### Transfer a conversation to Live Agent in a specific queue

This example uses the [AGENT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/bot-api.md) action to transfer a conversation to a live agent in a specific queue. The queue is selected by the condition passed in **contextVariables**, here a category value of `humanresource`. You must set up the queue with a matching condition before you send this request. For additional information on creating a work item queue, see [Create a work item queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-create-queue.md).

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "requestId": "example-request-017", // Unique value for a message (hash)
  "enterpriseId": "ExampleCompany", // Enterprise name (optional)
  "nowBotId": "EXAMPLE_BOT_ID", // In case of multiple ServiceNow secondary bots (one for HR, one for ITSM)
  "action":"AGENT", // Actions to close conversation. Other possible value is END_CONVERSATION
  "clientSessionId": "", // Client conversation id
  "nowSessionId": "", // ServiceNow conversation id
  "message":{
    "text": "How are you?", // User passed message
    "typed": true, // typed or clicked
    "clientMessageId": "msg-006"
  },
  "userId": "jane.doe", // User's id in their system
  "emailId": "jane.doe@example.com",
  "timestamp": 1588824102,
  "timezone": "America/New_York",
  "contextVariables":{
    "b2b_category":"humanresource"
  }
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. In this example, the message wasn’t understood, so Virtual Agent asks the user to rephrase and offers the Live Agent Support topic.

```
{
  "requestId":"example-request-017",
  "clientSessionId":"",
  "nowSessionId":"",
  "message":{
    "text":"How are you?",
    "typed":true,
    "clientMessageId":"msg-006"
   },
   "userId":"jane.doe",
   "body":[
     {
       "uiType":"OutputText",
       "group":"DefaultText",
       "value":"I am sorry but I didn't understand your request.",
       "maskType":"NONE"
    },
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "value":"Please try giving me your request in a different way. I'm currently better at understanding short sentences.",
      "maskType":"NONE"
    },
    {
      "uiType":"TopicPickerControl",
      "group":"DefaultPicker",
      "nluTextEnabled":false,
      "promptMsg":"Hi guest, please enter your request or make a selection of what I can help with. You can type help any time when you need help.",
      "label":"Show me everything",
      "options":[
        {
          "label":"Live Agent Support.",
          "value":"2222bbbb2222bbbb2222bbbb2222bbbb",
          "enabled":true
        }
      ]
    }
  ],
  "score":0
}
```

### Transfer a public application/pdf attachment file

This example sends a publicly accessible PDF file to Virtual Agent as an attachment. Virtual Agent retrieves the file from the URL, scans it for viruses, and processes it. The file is public, so no authorization information is needed.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--header "token: BOT_TOKEN" \
--data "{
  "requestId": "example-request-018",
  "clientSessionId": "example-session-001",
  "message": {
    "attachment": {
    "clientAttachmentId": "attachment-001",
    "contentType": "application/pdf",
    "fileName": "sample.pdf",
    "url": "https://example.com/files/sample.pdf"
    }
  },
  "userId": "example.user",
  "emailId": "jane.doe@example.com"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It confirms that the file was received and that the conversation is complete.

```
{
  "requestId":"example-request-018",
  "clientSessionId":"example-session-001",
  "message":{
    "attachment":{
      "clientAttachmentId":"attachment-001",
      "contentType":"application/pdf",
      "fileName":"sample.pdf",
      "url":"https://example.com/files/sample.pdf"}
    },
    "userId":"example.user",
    "body":[
      {
        "uiType":"OutputText",
        "group":"DefaultText",
        "required":false,
        "nluTextEnabled":false,
        "label":"File got",
        "maskType":"NONE",
        "itemType":"outputtext"
      },
      {
        "uiType":"OutputText",
        "group":"DefaultText",
        "required":false,
        "nluTextEnabled":false,
        "label":"The conversation has ended. If you need help again, type hi.",
        "maskType":"NONE",
        "itemType":"outputtext"
       }
    ],
  "completed":true,
  "score":1
}
```

### Transfer a video/mpeg attachment

This example sends a video file to Virtual Agent as an attachment by specifying its MIME type and URL. The response echoes the attachment details, including an Authorization header that Virtual Agent uses to retrieve a protected file.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--header "token: BOT_TOKEN" \
--data "{
  "requestId": "example-request-019",
  "clientSessionId": "example-session-001",
  "message": {
    "attachment": {
    "clientAttachmentId": "attachment-002",
    "contentType": "video/mpeg",
    "fileName": "sample-video.mp4",
    "url": "https://example.com/media/sample-video.mp4"
    }
  },
  "userId": "example.user",
  "emailId": "jane.doe@example.com"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It confirms that the file was received and that the conversation is complete.

```
{
  "requestId":"example-request-019",
  "clientSessionId":"example-session-001",
  "message":{
    "attachment":{
      "headers":{
        "Authorization":"Basic <base64-encoded-credentials>"
      },
      "clientAttachmentId":"attachment-002",
      "contentType":"video/mpeg",
      "fileName":"sample-video.mp4",
      "url":"https://example.com/media/sample-video.mp4"
    }
  },
  "userId":"example.user",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "required":false,
      "nluTextEnabled":false,
      "label":"File got",
      "maskType":"NONE",
      "itemType":"outputtext"
    },
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "required":false,
      "nluTextEnabled":false,
      "label":"The conversation has ended. If you need help again, type hi.",
      "maskType":"NONE","itemType":"outputtext"
    }
  ],
  "completed":true,
  "score":1
}
```

### Transfer a image/jpeg attachment

This example sends an image file to Virtual Agent as an attachment by specifying its MIME type and URL. Virtual Agent retrieves the image, scans it for viruses, and processes it.

```
curl "https://instance.servicenow.com/api/sn_va_as_service/bot/integration" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--header "token: BOT_TOKEN" \
--data "{
  "requestId": "example-request-020",
  "clientSessionId": "example-session-001",
  "message": {
    "attachment": {
      "clientAttachmentId": "attachment-003",
      "contentType": "image/jpeg",
      "fileName": "sample-image.jpg",
      "url": "https://example.com/images/sample-image.jpg"
    }
  },
  "userId": "example.user",
  "emailId": "jane.doe@example.com"
}"
--user "username":"password"
```

Virtual Agent sends the following response to the configured response endpoint. It confirms that the file was received and that the conversation is complete.

```
{
  "requestId":"example-request-020",
  "clientSessionId":"example-session-001",
  "message":{
    "attachment":{
      "headers":{
        "Authorization":"Basic <base64-encoded-credentials>"
      },
      "clientAttachmentId":"attachment-003",
      "contentType":"image/jpeg",
      "fileName":"sample-image.jpg",
      "url":"https://example.com/images/sample-image.jpg"
    }
  },
  "userId":"example.user",
  "body":[
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "required":false,
      "nluTextEnabled":false,
      "label":"File got",
      "maskType":"NONE",
      "itemType":"outputtext"
    },
    {
      "uiType":"OutputText",
      "group":"DefaultText",
      "required":false,
      "nluTextEnabled":false,
      "label":"The conversation has ended. If you need help again, type hi.",
      "maskType":"NONE",
      "itemType":"outputtext"
    }
  ],
  "completed":true,
  "score":1
}
```

