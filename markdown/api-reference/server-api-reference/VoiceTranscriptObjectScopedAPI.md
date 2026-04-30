---
title: VoiceTranscriptObject - Scoped
description: The VoiceTranscriptObject scriptable API provides methods to save third-party voice conversation transcript data to a table within a ServiceNow instance.Adds the specified messages to the specified voice transaction record.Creates a conversation record within the Conversation \[sys\_cs\_conversation\] table for the specified interaction.Terminates the specified voice interaction. Once called, no additional voice messages are translated and stored for the phone conversation.Saves third-party voice conversation transcript data to tables within a ServiceNow instance that is then accessible through Customer Service Management \(CSM\).Creates a voice interaction record within the Interaction \[interaction\] table.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# VoiceTranscriptObject - Scoped

The VoiceTranscriptObject scriptable API provides methods to save third-party voice conversation transcript data to a table within a ServiceNow instance.

When calling the `VoiceTranscriptObject` class, use the `sn_cs` namespace identifier.

![](../../../../../integrate/inbound-rest/image/vir-agent_workspace.png)

## Availability

This API is available in the base ServiceNow system. Access is restricted by the ACLs imposed on the Interaction \[interaction\] and Conversation \[sys\_cs\_conversation\] tables.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## VoiceTranscriptObject - addVoiceInteractionMessage\(String interactionId, String Json\)

Adds the specified messages to the specified voice transaction record.

You can call this endpoint multiple times during real-time transcribing of the call or pass all messages in a single call if you are transcribing the call for historical purposes. If you are processing a real-time conversation, you should call this endpoint frequently, so that the messages appear in Agent Workspace in a timely manner. Messages are ordered based on their start and end times in relation to the start of the call.

<table id="table_v3s_ttl_x5b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="vto-interactionId-row"><td>

interactionId

</td><td>

String

</td><td id="VTO-interactionId-entry">

Sys\_id of the interaction record to add the specified messages to. This value is returned by the [VoiceTranscriptObject - startVoiceInteraction\(String Json\)](VoiceTranscriptObjectScopedAPI.md#) method and stored in the Interaction \[interaction\] table.

</td></tr><tr id="vto-json_string-row"><td>

&lt;json\_string&gt;

</td><td>

String \(Array of Objects\)

</td><td id="vto-json_string-entry">

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

</td></tr><tr id="vto-json_string_attributes-row"><td>

&lt;json\_string&gt;.attributes

</td><td>

Array of Objects

</td><td id="vto-json_string_attributes-entry">

Key-value pairs to associate to the voice interaction.

These can be any type of data object, from simple objects to complex compound objects. They are used as unique identifiers when invoking Amazon Web Services APIs.

 Default: None

</td></tr><tr id="vto-json_string_beginOffsetMillis-row"><td>

&lt;json\_string&gt;.beginOffsetMillis

</td><td>

Long

</td><td id="vto-json_string_beginOffsetMillis-entry">

Required. Time offset between the start of the voice interaction and the start of the associated message. For example: "beginOffsetMillis": 2650. Unit: Milliseconds

</td></tr><tr id="vto-json_string_content-row"><td>

&lt;json\_string&gt;.content

</td><td>

String

</td><td id="vto-json_string_content-entry">

Required. Text of the message to add to the voice interaction.

</td></tr><tr id="vto-json_string_endOffsetMillis-row"><td>

&lt;json\_string&gt;.endOffsetMillis

</td><td>

Long

</td><td id="vto-json_string_endOffsetMillis-entry">

Required. Time offset between the start of the voice interaction and the end of the message. For example: "endOffsetMillis": 9380. Unit: Milliseconds

</td></tr><tr id="vto-json_string_id-row"><td>

&lt;json\_string&gt;.id

</td><td>

String

</td><td id="vto-json_string_id-entry">

Message UUID of the source of this voice conversation, such as for AmazonConnect. Sets the source message ID column value. Default: None

</td></tr><tr id="vto-json_string_isEvent-row"><td>

&lt;json\_string&gt;.isEvent

</td><td>

Boolean

</td><td id="vto-json_string_isEvent-entry">

Set by Amazon Connect but not currently used by the method. Flag that indicates whether the associated message is an event.

Valid values:

-   true: Message is an event.
-   false: Message is not an event.

 Default: false

</td></tr><tr id="vto-json_string_isInternalMessage-row"><td>

&lt;json\_string&gt;.isInternalMessage

</td><td>

Boolean

</td><td id="vto-json_string_isInternalMessage-entry">

Flag that indicates whether this is an internal message and should not be shown to the caller.

Transcriptions are typically considered internal messages and only appear for the agent and not to the caller. In addition, Agent Whisper is used when a silent third-party is chatting with or is brought into a phone conversation without the caller knowing and offers advice to an agent. The caller does not hear or see these messages, but the agent does.

Valid values:

-   true: Internal message, do not display to the caller.
-   false: Not an internal message, display to caller.

 Default: false

</td></tr><tr id="vto-json_string_loudnessScore-row"><td>

&lt;json\_string&gt;.loudnessScore

</td><td>

Number

</td><td id="vto-json_string_loudnessScore-entry">

Measurement as to how loudly a customer or agent is speaking during a call.

Contact Lens displays an analysis of the conversation that shows where they may be talking loudly and have a negative sentiment.

 Default: Null

</td></tr><tr id="vto-json_string_participantId-row"><td>

&lt;json\_string&gt;.participantId

</td><td>

String

</td><td id="vto-json_string_participantId-entry">

Required. Participant associated with the message.

Valid values:

-   CUSTOMER
-   AGENT

</td></tr><tr id="vto-json_string_sentiment-row"><td>

&lt;json\_string&gt;.sentiment

</td><td>

String

</td><td id="vto-json_string_sentiment-entry">

Sentiment of the message.

This value is generated by a third-party provider. Based on the ServiceNow instance configuration settings, this value is then translated to be either positive, negative, or neutral and is stored in the conversation and interaction record.

Valid values:

-   NEGATIVE
-   NEUTRAL
-   POSITIVE

 Default: Null

</td></tr></tbody>
</table><table id="table_w3s_ttl_x5b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Message that describes the results of the call.

</td></tr><tr><td>

String

</td><td>

If successful, sys\_id of the voice interaction message record that was created. Located in the Voice Transcript Conversation Message \[sys\_cs\_message\_voice\_transcript\] table.If an error occurred, an error message describing the reason for the failure.

</td></tr></tbody>
</table>The following example shows how to add messages to an existing voice interaction record.

```
var request = [ 
  { 
    "isEvent":"False",
    "isInternalMessage":"False",
    "beginOffsetMillis":100000,
    "content":"This is John. How can I help you?",
    "endOffsetMillis":150000, 
    "id":"954c4edc-31a8-48b0-8f6e-7fa0c4ca00a8",
    "participantId":"AGENT",
    "sentiment":"NEUTRAL"
  }, 
  {
    "isEvent":"False",
    "isInternalMessage":"False",
    "beginOffsetMillis":200000,
    "content":"Uh, yes, John. Um, I'm a little very frustrated right now.",
    "endOffsetMillis":25000,
    "id":"18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f",
    "participantId":"CUSTOMER",
    "sentiment":"NEGATIVE" 
  } 
]; 

gs.log(sn_cs.VoiceTranscriptObject.addVoiceInteractionMessage("1f4ed6fdb7471110b6e8bc15ae11a971", JSON.stringify(request))); 
```

Output:

```
// Success
Voice conversation transcript has been successfully saved. Conversation id: ea01113cb7f71110b6e8bc15ae11a94d

// Error
Exception occurred while adding the message: <error message>
```

## VoiceTranscriptObject - createConversation\(String interactionId, String Json\)

Creates a conversation record within the Conversation \[sys\_cs\_conversation\] table for the specified interaction.

<table id="table_fhh_rbg_vvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

interactionId

</td><td>

String

</td><td>

Sys\_id of the interaction record for which to create a conversation record. This value is returned by the [VoiceTranscriptObject - startVoiceInteraction\(String Json\)](VoiceTranscriptObjectScopedAPI.md#) method and stored in the Interaction \[interaction\] table.

</td></tr><tr><td>

&lt;json\_string&gt;

</td><td>

String

</td><td id="vto-json_string-start-entry">

JSON string of the input parameters.```
"<json_string>": {
  "agentId": "String",
  "callerPhoneNumber": "String",
  "clientSessionId": "String",
  "inboundId": "String",
  "userId": "String"

```

</td></tr><tr><td>

&lt;json\_string&gt;.agentId

</td><td>

String

</td><td id="vto-json_string-agentId-entry">

Unique identifier of the agent to assign the voice interaction to. Located in the User ID field in the User \[sys\_user\] table. Default: None. Assigned to the next available agent.

</td></tr><tr><td>

&lt;json\_string&gt;.callerPhoneNumber

</td><td>

String

</td><td id="vto-json_string-callerPhoneNumber-entry">

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops. Format: E.164 standard compliant

 Default: None

</td></tr><tr><td>

&lt;json\_string&gt;.clientSessionId

</td><td>

String

</td><td id="vto-json_string-clientSessionId-entry">

Unique identifier of a record in an external system used to track this phone call. This information links the records between the two systems. Default: None

</td></tr><tr><td>

&lt;json\_string&gt;.inboundId

</td><td>

String

</td><td id="vto-json_string-inboundId-entry">

Unique identifier of the application provider for the voice service. Located in the Inbound ID field in the Provider Channel Application \[sys\_cs\_provider\_application\] table. Default: Pull from chat

</td></tr><tr><td>

&lt;json\_string&gt;.userId

</td><td>

String

</td><td id="vto-json_string-userId-entry">

Required. Phone number of the caller who made the call associated with the voice transaction. Format: Defined by the software that created the voice conversation script. Typically E.164 standard compliant.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|If successful, returns the sys\_id of the newly created conversation record. Located in the Conversation \[sys\_cs\_conversation\] table. If an error occurs, returns a detailed error message.|

The following code example shows how to create a new conversation record using this method.

```
var request = { 
  "userId": "+14089178877"
}; 

var response = sn_cs.VoiceTranscriptObject.createConversation("e0fc03d7b7a21110b6e8bc15ae11a96c", JSON.stringify(request)); 
gs.log("Conversation id: " + JSON.stringify(response)); 
```

Output:

```
// Success
{"conversationId":"28435dbcb7f71110b6e8bc15ae11a972","status":"SUCCESS"}

// Error
{"error":"Exception occurred while creating a conversation: <error message>","status":"FAILED"}
```

## VoiceTranscriptObject - endVoiceInteraction\(String interactionId, String Json\)

Terminates the specified voice interaction. Once called, no additional voice messages are translated and stored for the phone conversation.

<table id="table_ozg_d4l_x5b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

interactionId

</td><td>

String

</td><td>

Sys\_id of the interaction record whose voice interaction to terminate. Located in the Interaction \[interaction\] table.

</td></tr><tr><td>

&lt;json\_string&gt;

</td><td>

JSON String

</td><td>

Optional. Parameters that contain additional information about the voice interactions.```
"<json_string>": {
  "recordingURL": "String"
}
```

</td></tr><tr><td>

&lt;json\_string&gt;.recordingURL

</td><td>

String

</td><td>

Optional. URL where the original voice recording is located.If configured to do so, this URL appears in Agent Workspace.

 Default: None

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|If successful, returns `Success`. If an error occurs, returns a detailed error message.|

The following code example shows how to end an active voice interaction and pass in the original voice recording URL.

```
var request = { 
  "recordingURL": "https://servicenow.zoom.us/rec/QbF7XmPFHPlX1LG" 
}; 

gs.log(sn_cs.VoiceTranscriptObject.endVoiceInteraction("1f4ed6fdb7471110b6e8bc15ae11a971", JSON.stringify(request))); 
```

Output:

```
// Success
Success

// Error
Exception occurred while ending the interaction: <error message>
```

## VoiceTranscriptObject - saveVoiceConversationTranscript\(String voiceConversationJson\)

Saves third-party voice conversation transcript data to tables within a ServiceNow instance that is then accessible through Customer Service Management \(CSM\).

These voice conversations are typically generated using third-party vendor software. This method parses the passed JSON and saves the data into the Conversation \[sys\_cs\_conversation\], Conversation Message \[sys\_cs\_message\], and Voice Transcript Conversation Message \[sys\_cs\_message\_voice\_transcript\] tables within the ServiceNow instance. CSM accesses the information in these tables to display the voice conversation transcripts.

<table id="table_tcz_mly_prb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

voiceConversationJson

</td><td>

String

</td><td>

JSON that represents the voice conversation to store. This JSON is sent by another ServiceNow plugin, such as OpenFrame. Third-party vendors, such as Amazon, send the JSON to the plugin. The associated plugin parses out the voice conversation and sends the JSON in the required format to Virtual Agent.For example, the following is an example of an Amazon Connect conversation:

 ```
{ 
  "interactionId":"bgr09b5a-7308-47b2-jy97-737de9f45d19", 
  "source":"AmazonConnect", 
  "conversationStarted":"2021-08-06 15:07:51", 
  "transcript":[ 
    { 
      "isEvent":"False", 
      "isInternalMessage":"False", 
      "beginOffsetMillis":2650, 
      "content":"This is John. How can I help you? Yeah,", 
      "endOffsetMillis":9380, 
      "id":"954c4edc-31a8-48b0-8f6e-7fa0c4ca00a8", 
      "participantId":"AGENT", 
      "Sentiment":"NEUTRAL", 
      "loudnessScore":"null,null", 
      "attributes": [{ 
        "key":"key1", 
        "value":"value1" 
      },{ 
        "key":"key2", 
        "value":"value2" 
      }] 
    }, 
    { 
      "isEvent":"False", 
      "isInternalMessage":"False", 
      "beginOffsetMillis":9120, 
      "content":"Uh, yes, John. I'm a little very frustrated right now.", 
      "endOffsetMillis":22900, 
      "id":"18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f", 
      "participantId":"CUSTOMER", 
      "sentiment":"NEGATIVE", 
      "loudnessScore":"null,null", 
      "attributes": [{ 
        "key":"key1", 
        "value":"value1" 
      },{ 
        "key":"key2", 
        "value":"value2" 
      } ] 
    }, 
    { 
      "isEvent":"True", 
      "isInternalMessage":"True", 
      "beginOffsetMillis":23590, 
      "content":"Agent asked for help in chat", 
      "endOffsetMillis":30610, 
      "id":"ab09b3b6-23fd-4e41-be05-6b2b53c19059", 
      "participantId":"CUSTOMER", 
      "sentiment":"NEUTRAL", 
      "loudnessScore":"null,null,null,null", 
      "attributes": [] 
    } 
  ] 
}
```

</td></tr></tbody>
</table><table id="table_ucz_mly_prb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Results of the method call.Possible return results:

-   Voice conversation transcript has been successfully saved. Conversation id: `<transcript_record_sys_id>`
-   Voice conversation transcript could not be saved. Detail error: `<error details>`
-   ERROR: InteractionId is missing in the request.
-   ERROR: Interaction specified in the request has already been processed.

</td></tr></tbody>
</table>This example shows how to call the saveVoiceConversationTranscript\(\) method to save an Amazon Connect transcript.

```
var voiceConversationJson = "{\n" +
  "   \"interactionId\":\"e67a6c30c7233010967a34c91dc26068\",\n" +
  "   \"source\":\"AmazonConnect\",\n" +
  "   \"conversationStarted\":\"2021-08-06 15:07:51\",\n" +
  "   \"transcript\":[\n" +
  "      {\n" +
  "         \"isEvent\":\"False\",\n" +
  "         \"isInternalMessage\":\"False\",\n" +
  "         \"beginOffsetMillis\":2650,\n" +
  "         \"content\":\"This is John. How can I help you? Yeah,\",\n" +
  "         \"endOffsetMillis\":9380,\n" +
  "         \"id\":\"954c4edc-31a8-48b0-8f6e-7fa0c4ca00a8\",\n" +
  "         \"participantId\":\"AGENT\",\n" +
  "         \"sentiment\":\"NEUTRAL\",\n" +
  "         \"loudnessScore\":\"null,null\",\n" +
  "         \"attributes\": [{\n" +
  "           \"key\":\"key1\",\n" +
  "           \"value\":\"value1\"\n" +
  "         },{\n" +
  "           \"key\":\"key2\",\n" +
  "           \"value\":\"value2\"\n" +
  "         }\n" +
  " ]\n" +
  "      },\n" +
  "      {\n" +
  "         \"isEvent\":\"False\",\n" +
  "         \"isInternalMessage\":\"False\",\n" +
  "         \"beginOffsetMillis\":9120,\n" +
  "         \"content\":\"Uh, yes, John. I'm a little frustrated right now.\",\n" +
  "         \"endOffsetMillis\":22900,\n" +
  "         \"id\":\"18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f\",\n" +
  "         \"participantId\":\"CUSTOMER\",\n" +
  "         \"sentiment\":\"NEGATIVE\",\n" +
  "         \"loudnessScore\":\"null,null\",\n" +
  "         \"attributes\": [{\n" +
  "           \"key\":\"key1\",\n" +
  "           \"value\":\"value1\"\n" +
  "         },{\n" +
  "           \"key\":\"key2\",\n" +
  "           \"value\":\"value2\"\n" +
  "         }\n" +
  " ]\n" +
  "      },\n" +
  "      {\n" +
  "         \"isEvent\":\"False\",\n" +
  "         \"isInternalMessage\":\"False\",\n" +
  "         \"beginOffsetMillis\":9120,\n" +
  "         \"content\":\"I am sorry to hear that\",\n" +
  "         \"endOffsetMillis\":22900,\n" +
  "         \"id\":\"18bcf19c-4a9b-4af1-9bd7-7bfb5ba53b9f\",\n" +
  "         \"participantId\":\"AGENT\",\n" +
  "         \"sentiment\":\"NEGATIVE\",\n" +
  "         \"loudnessScore\":\"null,null\",\n" +
  "         \"attributes\": [{\n" +
  "           \"key\":\"key1\",\n" +
  "           \"value\":\"value1\"\n" +
  "         },{\n" +
  "           \"key\":\"key2\",\n" +
  "           \"value\":\"value2\"\n" +
  "         }\n" +
  " ]\n" +
  "      },\n" +
  "      {\n" +
  "         \"isEvent\":\"false\",\n" +
  "         \"isInternalMessage\":\"false\",\n" +
  "         \"beginOffsetMillis\":23590,\n" +
  "         \"content\":\"I am having problems with my computer\",\n" +
  "         \"endOffsetMillis\":30610,\n" +
  "         \"id\":\"ab09b3b6-23fd-4e41-be05-6b2b53c19059\",\n" +
  "         \"participantId\":\"CUSTOMER\",\n" +
  "         \"sentiment\":\"NEUTRAL\",\n" +
  "  \"loudnessScore\":\"null,null,null,null\",\n" +
  "         \"attributes\": [\n" +
  "  ]\n" +
  "      },\n" +
  "      {\n" +
  "         \"isEvent\":\"True\",\n" +
  "         \"isInternalMessage\":\"True\",\n" +
  "         \"beginOffsetMillis\":23590,\n" +
  "         \"content\":\"Agent asked for help in chat\",\n" +
  "         \"endOffsetMillis\":30610,\n" +
  "         \"id\":\"ab09b3b6-23fd-4e41-be05-6b2b53c19059\",\n" +
  "         \"participantId\":\"CUSTOMER\",\n" +
  "         \"sentiment\":\"NEUTRAL\",\n" +
  "  \"loudnessScore\":\"null,null,null,null\",\n" +
  "         \"attributes\": [\n" +
  "  ]\n" +
  "      }\n" +
  "   ]\n" +
  "}\n";
var result = sn_cs.VoiceTranscriptObject.saveVoiceConversationTranscript(voiceConversationJson);
gs.log(result);
```

Output:

```
Voice conversation transcript has been successfully saved. Conversation id: 9c573169c611228700193229fff72400
```

## VoiceTranscriptObject - startVoiceInteraction\(String Json\)

Creates a voice interaction record within the Interaction \[interaction\] table.

You must create this record before trying to save any transcribed voice messages. You can also use this method to assign a call to a specific agent by passing in their specific user ID.

<table id="table_lkt_hkl_x5b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;json\_string&gt;

</td><td>

String

</td><td id="vto-json_string-start-entry">

JSON string of the input parameters.```
"<json_string>": {
  "agentId": "String",
  "callerPhoneNumber": "String",
  "clientSessionId": "String",
  "inboundId": "String",
  "userId": "String"

```

</td></tr><tr><td>

&lt;json\_string&gt;.agentId

</td><td>

String

</td><td id="vto-json_string-agentId-entry">

Unique identifier of the agent to assign the voice interaction to. Located in the User ID field in the User \[sys\_user\] table. Default: None. Assigned to the next available agent.

</td></tr><tr><td>

&lt;json\_string&gt;.callerPhoneNumber

</td><td>

String

</td><td id="vto-json_string-callerPhoneNumber-entry">

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops. Format: E.164 standard compliant

 Default: None

</td></tr><tr><td>

&lt;json\_string&gt;.clientSessionId

</td><td>

String

</td><td id="vto-json_string-clientSessionId-entry">

Unique identifier of a record in an external system used to track this phone call. This information links the records between the two systems. Default: None

</td></tr><tr><td>

&lt;json\_string&gt;.inboundId

</td><td>

String

</td><td id="vto-json_string-inboundId-entry">

Unique identifier of the application provider for the voice service. Located in the Inbound ID field in the Provider Channel Application \[sys\_cs\_provider\_application\] table. Default: Pull from chat

</td></tr><tr><td>

&lt;json\_string&gt;.userId

</td><td>

String

</td><td id="vto-json_string-userId-entry">

Required. Phone number of the caller who made the call associated with the voice transaction. Format: Defined by the software that created the voice conversation script. Typically E.164 standard compliant.

</td></tr></tbody>
</table><table id="table_mkt_hkl_x5b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Results of the method call.Possible return results:

-   Success: \{"interactionId":"&lt;interaction\_sys\_id&gt;","status":"SUCCESS"\}
-   Error: \{"error":"&lt;error message&gt;","status":"FAILED"\}

</td></tr></tbody>
</table>The following code example shows how to create a voice interaction record.

```
var request = { 
  "userId": "+14089178877", 
  "callerPhoneNumber": "+14089178878", 
  "clientSessionId": "f8453abb-a33d-45b7-bf01-52b7a821e99z" 
}; 
var response = sn_cs.VoiceTranscriptObject.startVoiceInteraction(JSON.stringify(request)); 
gs.log(JSON.stringify(response)); 
```

Output:

```
// Success 
{"interactionId":"ea01113cb7f71110b6e8bc15ae11a950","status":"SUCCESS"}

// Error
{"error":"Exception occurred while starting the interaction: <error message>","status":"FAILED"}
```

