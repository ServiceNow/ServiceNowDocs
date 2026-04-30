---
title: Voice Interaction Resource API
description: The Voice Interaction API provides endpoints to transcribe and store voice interactions between agents and callers during a telephone conversation. It works in conjunction with Virtual Agent and Live Agent chats.Terminates the specified voice interaction. Once called, no additional voice messages are translated and stored for the phone conversation.Creates a voice interaction record within the Interaction \[interaction\] table.Creates a conversation record within the Conversation \[sys\_cs\_conversation\] table for the specified interaction.Adds the specified voice conversations messages to the specified voice transaction record. These messages are typically generated using third-party vendor software. Currently, only Amazon Connect is supported.Adds messages to an existing voice interaction after a call is completed. You can use this API to attach transcribed messages of a voice call between an agent and caller.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 20
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Voice Interaction Resource API

The Voice Interaction API provides endpoints to transcribe and store voice interactions between agents and callers during a telephone conversation. It works in conjunction with Virtual Agent and Live Agent chats.

You can use this API to persist transcribed messages from an on-going phone call in real-time or to transcribe and store an existing voice conversation recording for historical purposes. Transcribed messages appear in Agent Workspace, allowing agents to leverage features such as agent assist and search, while talking to a caller. Transcribed messages are persisted in the Conversation Message \[sys\_cs\_message\] table.

![Transcribed messages in Agent Workspace](../image/vir-agent_workspace.png)

## Call flow

The following call flow shows how to use the Voice Interaction API to create a voice interaction record, transcribe and store the messages within that voice conversation, and then close the voice conversation record. You can also use business rules and other scripts to perform this functionality, however, this type of implementation is not covered in this section.

1.  First, call the [Voice Interaction Resource - POST /cs/voice-interactions](voice-interaction-resource-api.md#) endpoint to create a voice interaction record in the Interaction \[interaction\] table.
2.  Then call the [Voice Interaction Resource - POST /cs/voice-interactions/\{interactionId\}/messages](voice-interaction-resource-api.md#) endpoint to store translated messages from the voice conversation into the Conversation Message table. If you are processing a real-time conversation, you should call this endpoint frequently, so that the messages appear in Agent Workspace in a timely manner. When processing a recording for historical purposes, you can pass all messages in a single endpoint call.
3.  Once you are finished persisting the voice messages, call the [Voice Interaction Resource - PATCH /cs/voice-interactions/\{interactionId\}/state](voice-interaction-resource-api.md#) endpoint to terminate the capture and close the voice interaction record.

## Availability

This API is available in the base ServiceNow system. Access is restricted by the ACLs imposed on the Interaction \[interaction\] and Conversation \[sys\_cs\_conversation\] tables.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Voice Interaction Resource - PATCH /cs/voice-interactions/\{interactionId\}/state

Terminates the specified voice interaction. Once called, no additional voice messages are translated and stored for the phone conversation.

### URL format

Versioned URL: `/api/now/{api_version}/cs/voice-interactions/{interactionId}/state`

Default URL: `/api/now/v1/cs/voice-interactions/{interactionId}/state`

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

interactionId

</td><td>

Sys\_id of the interaction record whose voice interaction to terminate. Passed back by the [Voice Interaction Resource - POST /cs/voice-interactions](voice-interaction-resource-api.md#) endpoint.Data type: String

Table: Interaction \[interaction\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

recordingURL

</td><td>

URL where the original voice recording is located.If configured to do so, this URL appears in Agent Workspace.

 Data type: String

 Default: None

</td></tr><tr><td>

state

</td><td>

Required. State of the voice interaction.Only supported value: closed\_complete

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
|400|Bad Request. Badly formed JSON or required parameters were not passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Status of the operation. Possible values:

-   `Success`
-   `Failed`

 If an error is encountered, a message that describes the error is also returned. If the error is on the ServiceNow instance, the instance logs the associated stack trace.

</td></tr></tbody>
</table>### cURL request

The following example shows how to terminate a voice instance.

```
curl "http://instance.servicenow.com/api/now/v1/ cs/voice-interactions/86837a386f0331003b3c498f5d3ee4ca/state" \ 
--request PATCH \
--header "Content-Type: application/json" \
--header "Accept:application/json" \
--user 'username':'password' \
-d {
  "state": "closed_complete",
  "recordingURL": "https: //zoom_instance/rec/QbF7XmPFHPlX1LG"
}’
```

Response:

```
{
  "result": "Success"
}
```

## Voice Interaction Resource - POST /cs/voice-interactions

Creates a voice interaction record within the Interaction \[interaction\] table.

You must create this record before trying to save any transcribed voice messages. You can also use this endpoint to assign a call to a specific agent by passing in their specific user ID.

### URL format

Versioned URL: `/api/now/{api_version}/cs/voice-interactions`

Default URL: `/api/now/v1/cs/voice-interactions`

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

agentId

</td><td>

Unique identifier of the agent to assign the voice interaction to. Data type: String

Default: Invoke Virtual Agent

</td></tr><tr><td>

callerPhoneNumber

</td><td>

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops. Data type: String

Format: E.164 standard compliant

Default: None

</td></tr><tr><td>

clientSessionId

</td><td>

Unique identifier of a record in an external system used to track this phone call. This information links the records between the two systems. Data type: String

Default: None

</td></tr><tr><td>

inboundId

</td><td>

Unique identifier of the application provider for the voice service. Data type: String

Default: Pulled from chat

</td></tr><tr><td>

userId

</td><td>

Required. Phone number of the caller who made the call associated with the voice transaction. Data type: String

Format: Defined by the software that created the voice conversation script. Typically E.164 standard compliant.

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
|400|Bad Request. Badly formed JSON or required parameters were not passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

interactionId

</td><td>

Sys\_id of the newly created voice interaction record. Use this sys\_id when:

-   Calling the [Voice Interaction Resource - POST /cs/voice-interactions/\{interactionId\}/messages](voice-interaction-resource-api.md#) endpoint to add a message to the voice interaction.
-   Calling the [Voice Interaction Resource - PATCH /cs/voice-interactions/\{interactionId\}/state](voice-interaction-resource-api.md#) endpoint to end the voice interaction.

Data type: String

Table: Interaction \[interaction\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to initiate a voice interaction and transfer the call to a specific agent.

```
curl "http://instance.servicenow.com/api/now/v1/cs/voice-interactions" \ 
--request POST \ 
--header "Accept:application/json" \ 
--user 'username':'password' \ 
--header "Content-Type: application/json"\ 
-d '{ 
  "userId": "+14089178877",
  "agentId": "beth.anglin",
  "callerPhoneNumber": "+14089178878",
  "clientSessionId": "f8453abb-a33d-45b7-bf01-52b7a821e99z"
}'
```

Response:

```
{
  "result": {
    "interactionId": "4462cb4753751110b6e8ddeeff7b12ca"
  }
}
```

## Voice Interaction Resource - POST /cs/voice-interactions/\{interactionId\}/conversation

Creates a conversation record within the Conversation \[sys\_cs\_conversation\] table for the specified interaction.

### URL format

Versioned URL: `/api/now/{api_version}/cs/voice-interactions/{interactionId}/conversation`

Default URL: `/api/now/v1/cs/voice-interactions/{interactionId}/conversation`

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

interactionId

</td><td>

Sys\_id of the interaction record for which to create the conversation record. This value is returned by the [Voice Interaction Resource - POST /cs/voice-interactions](voice-interaction-resource-api.md#) endpoint and stored in the Interaction \[interaction\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agentId

</td><td>

Unique identifier of the agent to assign the voice interaction to. Data type: String

Default: Invoke Virtual Agent

</td></tr><tr><td>

callerPhoneNumber

</td><td>

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops. Data type: String

Format: E.164 standard compliant

Default: None

</td></tr><tr><td>

clientSessionId

</td><td>

Unique identifier of a record in an external system used to track this phone call. This information links the records between the two systems. Data type: String

Default: None

</td></tr><tr><td>

inboundId

</td><td>

Unique identifier of the application provider for the voice service. Data type: String

Default: Pull from the chat

</td></tr><tr><td>

userId

</td><td>

Required. Phone number of the caller who made the call associated with the voice transaction. Data type: String

Format: Defined by the software that created the voice conversation script. Typically E.164 standard compliant.

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
|400|Bad Request. Badly formed JSON or required parameters were not passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conversationId

</td><td>

Sys\_id of the newly created conversation record.Data type: String

Table: Conversation \[sys\_cs\_conversation\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "http://instance.servicenow.com/api/now/v1/cs/voice-interactions/7662cb4721751ea0b6e8dda1b27b131f/conversation" \  
--request POST \  
--header "Accept:application/json" \  
--user 'username':'password' \  
--header "Content-Type: application/json"\  
-d '{  
  "userId": "+14089178877", 
  "agentId": "admin@example.com", 
  "callerPhoneNumber": "+14089178878", 
  "clientSessionId": "f8453abb-a33d-45b7-bf01-52b7a821e99z" 
}' 
```

Response:

```
{ 
  "result": "a47e1afdb7471110b6e8bc15ae11a934" 
} 
```

## Voice Interaction Resource - POST /cs/voice-interactions/\{interactionId\}/messages

Adds the specified voice conversations messages to the specified voice transaction record. These messages are typically generated using third-party vendor software. Currently, only Amazon Connect is supported.

You can call this endpoint multiple times during real-time transcribing of the call or pass all messages in a single call if you are transcribing the call for historical purposes. If you are processing a real-time conversation, you should call this endpoint frequently, so that the messages appear in Agent Workspace in a timely manner. Messages are ordered based on their start and end times in relation to the start of the call.

### URL format

Versioned URL: `/api/now/{api_version}/cs/voice-interactions/{interactionId}/messages`

Default URL: `/api/now/v1/cs/voice-interactions/{interactionId}/messages`

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

interactionId

</td><td>

Sys\_id of the interaction record to add the specified messages to. This value is returned by the [Voice Interaction Resource - POST /cs/voice-interactions](voice-interaction-resource-api.md#) endpoint and stored in the Interaction \[interaction\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;json\_string&gt;

</td><td>

List of messages to attach to the specified voice interaction.

```
"<json_string>":[
  {
    "attributes": [Array],
    "beginOffsetMillis": Long,
    "content": "String"
    "endOffsetMillis": Long,
    "id": "String",
    "isEvent": Boolean,
    "isInternalMessage": Boolean,
    "loudnessScore": "Number",
    "participantId": "String",
    "sentiment": "String"
  }
]
```

</td></tr><tr><td>

&lt;json\_string&gt;.attributes

</td><td>

Key-value pairs to associate to the voice interaction.

These can be any type of data object, from simple objects to complex compound objects. They are used as unique identifiers when invoking Amazon Web Services APIs.

 Data type: Array of Objects

 Default: None

</td></tr><tr><td>

&lt;json\_string&gt;.beginOffsetMillis

</td><td>

Required. Time offset between the start of the voice interaction and the start of the associated message. For example: "beginOffsetMillis": 2650. Data type: Long

Unit: Milliseconds

</td></tr><tr><td>

&lt;json\_string&gt;.content

</td><td>

Required. Text of the message to add to the voice interaction. Data type: String

</td></tr><tr><td>

&lt;json\_string&gt;.endOffsetMillis

</td><td>

Required. Time offset between the start of the voice interaction and the end of the message. For example: "endOffsetMillis": 9380. Data type: Long

Unit: Milliseconds

</td></tr><tr><td>

&lt;json\_string&gt;.id

</td><td>

Message UUID of the source of this voice conversation, such as for AmazonConnect. Sets the source message ID column value. Data type: String

Default: None

</td></tr><tr><td>

&lt;json\_string&gt;.isEvent

</td><td>

Set by Amazon Connect but not currently used by the method. Flag that indicates whether the associated message is an event.

Valid values:

-   true: Message is an event.
-   false: Message is not an event.

 Data type: Boolean

 Default: false

</td></tr><tr><td>

&lt;json\_string&gt;.isInternalMessage

</td><td>

Flag that indicates whether this is an internal message and shouldn't be shown to the caller.

Transcriptions are typically considered internal messages and only appear for the agent and not to the caller. In addition, Agent Whisper is used when a silent third-party is chatting with or is brought into a phone conversation without the caller knowing and offers advice to an agent. The caller doesn't hear or see these messages, but the agent does.

Valid values:

-   true: Internal message, don't display to the caller.
-   false: Not an internal message, display to caller.

 Data type: Boolean

 Default: false

</td></tr><tr><td>

&lt;json\_string&gt;.loudnessScore

</td><td>

Measurement as to how loudly a customer or agent is speaking during a call.

Contact Lens displays an analysis of the conversation that shows where they may be talking loudly and have a negative sentiment.

 Data type: Number

 Range: -1.0 \(negative\) to 1.0 \(positive\)

 Default: Null

</td></tr><tr><td>

&lt;json\_string&gt;.participantId

</td><td>

Required. Participant associated with the message.

Valid values:

-   AGENT
-   CUSTOMER

 Data type: String

</td></tr><tr><td>

&lt;json\_string&gt;.sentiment

</td><td>

Sentiment of the message.

This value is generated by a third-party provider. Based on the ServiceNow instance configuration settings, this value is then translated to be either positive, negative, or neutral and is stored in the conversation and interaction record.

Valid values:

-   NEGATIVE
-   NEUTRAL
-   POSITIVE

 Data type: String

 Default: Null

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
|400|Bad Request. Badly formed JSON or required parameters were not passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Message that describes the results of the call.Data type: String

</td></tr><tr><td>

Conversation id

</td><td>

Sys\_id of the voice interaction message record that was created.Data type: String

Table: Voice Transcript Conversation Message \[sys\_cs\_message\_voice\_transcript\]

</td></tr></tbody>
</table>### cURL request

The following example shows how to add messages to an existing voice interaction record.

```
curl "http://instance.servicenow.com/api/now/v1/cs/voice-interactions/86837a386f0331003b3c498f5d3ee4ca/messages" \ 
--request POST \
--header "Accept:application/json" \
--header "Content-Type: application/json"\ 
--user 'username':'password' \
-d ' [ 
  { 
    "isEvent": "false",  
    "isInternalMessage": "false",  
    "beginOffsetMillis": 10000,  
    "content": "This is John. How can I help you?",  
    "endOffsetMillis": 15000,  
    "id": "954c4edc-31a8-48b0-8f6e-7fa0c4ca00a8",  
    "participantId": "AGENT",  
    "sentiment": "NEUTRAL",  
    "loudnessScore": "null",  
    "attributes": [{  
      "key": "key1",  
      "value": "value1"  
      }, {  
      "key": "key2",  
      "value": "value2"  
    }] 
  },  
  {  
    "isEvent": "false",  
    "isInternalMessage": "false",  
    "beginOffsetMillis": 20000,  
    "content": "Uh, yes, John. Um, I'm a little very frustrated right now.",  
    "endOffsetMillis": 25000,  
    "id": "18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f",  
    "participantId": "CUSTOMER",  
    "sentiment": "NEGATIVE"  
  },  
  {  
    "isEvent": "false",  
    "isInternalMessage": "false",  
    "beginOffsetMillis": 30000,  
    "content": "I am sorry to hear that",  
    "endOffsetMillis": 35000,  
    "id": "18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f",  
    "participantId": "AGENT",  
    "sentiment": "NEGATIVE",  
 
  },  
  {  
    "isEvent":"false",
    "isInternalMessage":"false",
    "beginOffsetMillis":40000,
    "content":"Can you help me with my insurance? My ssn is 123-12-1234",
    "endOffsetMillis":45000,
    "id":"ab09b3b6-23fd-4e41-be05-6b2b53c19059",
    "participantId":"CUSTOMER",
    "sentiment":"NEUTRAL" 
  },  
  {  
    "isEvent":"False",
    "isInternalMessage":"False",
    "beginOffsetMillis":50000, 
    "content":"Of course, let me check your account",
    "endOffsetMillis":55000,
    "id":"18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f",
    "participantId":"AGENT",
    "sentiment":"NEUTRAL" 
  }  
]'
```

Response:

```
{ 
  "result": "Voice conversation transcript has been successfully saved. Conversation id: 8439d3c753b51110b6e8ddeeff7b12e2" 
}
```

## Voice Interaction Resource - POST /cs/voice-interactions/transcript

Adds messages to an existing voice interaction after a call is completed. You can use this API to attach transcribed messages of a voice call between an agent and caller.

### URL format

Versioned URL: `/api/now/{api_version}/cs/voice-interactions/{interactionId}/transcript`

Default URL: `/api/now/v1/cs/voice-interactions/{interactionId}/transcript`

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

conversationStarted

</td><td>

Start time of the conversation.Data type: String

Format: YYYY-MM-DD HH:MM:SS

Table: Interaction \[interaction\]

</td></tr><tr><td>

interactionId

</td><td id="vto-interactionId-REST-entry">

Sys\_id of the interaction record to add the specified messages to. This value is returned by the [Voice Interaction Resource - POST /cs/voice-interactions](voice-interaction-resource-api.md#) endpoint.Data type: String

Table: Interaction \[interaction\]

</td></tr><tr><td>

source

</td><td>

Name of the channel that originally created the conversation interaction transcript.Currently, the only supported value is `Amazon Connect`.

 Data type: String

</td></tr><tr><td>

transcript

</td><td>

List of messages to attach to the specified voice interaction.```
"transcript":[
  {
    "attributes": [Array],
    "beginOffsetMillis": Long,
    "content": "String"
    "endOffsetMillis": Long,
    "id": "String",
    "isEvent": Boolean,
    "isInternalMessage": Boolean,
    "loudnessScore": "String",
    "participantId": "String",
    "sentiment": "String"
  }
]
```

 Data type: Array of Objects

</td></tr><tr><td>

transcript.attributes

</td><td>

Key-value pairs to associate to the voice interaction.

These can be any type of data object, from simple objects to complex compound objects. They are used as unique identifiers when invoking Amazon Web Services APIs.

 Data type: Array of Objects

 Default: None

</td></tr><tr><td>

transcript.beginOffsetMillis

</td><td>

Required. Time offset between the start of the voice interaction and the start of the associated message. For example: "beginOffsetMillis": 2650. Data type: Long

 Unit: Milliseconds

</td></tr><tr><td>

transcript.content

</td><td>

Required. Text of the message to add to the voice interaction. Data type: String

</td></tr><tr><td>

transcript.endOffsetMillis

</td><td>

Required. Time offset between the start of the voice interaction and the end of the message. For example: "endOffsetMillis": 9380. Data type: Long

 Unit: Milliseconds

</td></tr><tr><td>

transcript.id

</td><td>

Message UUID of the source of this voice conversation, such as for AmazonConnect. Sets the source message ID column value. Data type: String

 Default: None

</td></tr><tr><td>

transcript.isEvent

</td><td>

Set by Amazon Connect but not currently used by the method. Flag that indicates whether the associated message is an event.

Valid values:

-   true: Message is an event.
-   false: Message is not an event.

 Data type: Boolean

 Default: false

</td></tr><tr><td>

transcript.isInternalMessage

</td><td>

Flag that indicates whether this is an internal message and shouldn't be shown to the caller.

Transcriptions are typically considered internal messages and only appear for the agent and not to the caller. In addition, Agent Whisper is used when a silent third-party is chatting with or is brought into a phone conversation without the caller knowing and offers advice to an agent. The caller doesn't hear or see these messages, but the agent does.

Valid values:

-   true: Internal message, don't display to the caller.
-   false: Not an internal message, display to caller.

 Data type: Boolean

 Default: false

</td></tr><tr><td>

transcript.loudnessScore

</td><td>

Measurement as to how loudly a customer or agent is speaking during a call.

Contact Lens displays an analysis of the conversation that shows where they may be talking loudly and have a negative sentiment.

 Data type: Number

 Range: -1.0 \(negative\) to 1.0 \(positive\)

 Default: Null

</td></tr><tr><td>

transcript.participantId

</td><td>

Required. Participant associated with the message.

Valid values:

-   AGENT
-   CUSTOMER

 Data type: String

</td></tr><tr><td>

transcript.sentiment

</td><td>

Sentiment of the message.

This value is generated by a third-party provider. Based on the ServiceNow instance configuration settings, this value is then translated to be either positive, negative, or neutral and is stored in the conversation and interaction record.

Valid values:

-   NEGATIVE
-   NEUTRAL
-   POSITIVE

 Data type: String

 Default: Null

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
|400|Bad Request. Badly formed JSON or required parameters were not passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Message that describes the results of the call.Data type: String

</td></tr><tr><td>

Conversation id

</td><td>

Sys\_id of the voice conversation table where the messages were attached.Data type: String

Table: Conversation \[sys\_cs\_message\_conversation\]

</td></tr></tbody>
</table>### cURL request

The following example shows how to add messages to an existing voice interaction record.

```
curl "http://instance.servicenow.com/api/now/v1/cs/voice-interactions/transcript" \  
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type: application/json"\  
--user 'username':'password' \ 
-d ' { 
  "interactionId": "e67a6c30c7233010967a34c91dc26068", 
  "source": "Amazon Connect", 
  "conversationStarted": "2021-08-06 15:07:51", 
  "transcript": [ 
    { 
      "isEvent": "False", 
      "isInternalMessage": "False", 
      "beginOffsetMillis": 100000, 
      "content": "This is John. How can I help you?", 
      "endOffsetMillis": 150000, 
      "id": "954c4edc-31a8-48b0-8f6e-7fa0c4ca00a8", 
      "participantId": "AGENT", 
      "sentiment": "NEUTRAL" 
    }, 
    { 
      "isEvent": "False",
      "isInternalMessage": "False", 
      "beginOffsetMillis": 200000, 
      "content": "Uh, yes, John. Um, I'm a little frustrated right now.", 
      "endOffsetMillis": 25000, 
      "id": "18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f", 
      "participantId": "CUSTOMER", 
      "sentiment": "NEGATIVE" 
    } 
  ] 
} ' 
```

Response:

```
{  
  "result": "Voice conversation transcript has been successfully saved. Conversation id: 8439d3c753b51110b6e8ddeeff7b12e2"  
}
```

