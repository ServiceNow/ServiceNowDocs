---
title: openFrameAPI - Client
description: The openFrameAPI provides methods that interact with OpenFrame. OpenFrame is an omni-present frame that communication partners can use to integrate their systems into the ServiceNow platform.Returns the logged in agent’s current presence state.Hides the OpenFrame in the TopFrame.Initializes OpenFrame. This must be the first method that you call.Checks to see if the OpenFrame is visible in the TopFrame.Opens a custom URL in the UI16 interface.Opens a form URL.Opens a ServiceNow form with a child tab if invoked in a workspace or opens an entity if invoked in the UI16 interface.Opens a list URL in the UI16 interface.Sets the OpenFrame mode.Sets the OpenFrame height.Sets the context data related to the interaction controls on the client. Use this context data to determine the client UI to display in OpenFrame.Defines icons in the OpenFrame header that are placed next to the close icon.Sets the presence indicator to display agent availability in a workspace.Sets the OpenFrame size.Sets the OpenFrame subtitle.Sets the OpenFrame title.Sets the OpenFrame's title icon.Sets the OpenFrame width.Makes the OpenFrame visible in the TopFrame.Subscribes to a specified event.Displays an alert message.Returns the OpenFrame API version.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 38
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# openFrameAPI- Client

The openFrameAPI provides methods that interact with OpenFrame. OpenFrame is an omni-present frame that communication partners can use to integrate their systems into the ServiceNow platform.

One of the core requirements is the ability to connect and serve code from different domains that can connect seamlessly with partner subsystems. This cross domain connection is required to keep connections and callbacks registered into communication systems without any cross domain issues.

OpenFrame has two significant parts. One lives in the ServiceNow application \(referred to as TopFrame\) and this API that is sourced from the partner application. This API has the necessary methods to communicate with TopFrame and control the visual features of the [OpenFrame](https://www.servicenow.com/docs/access?context=c_OpenFrameOverview&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Note:** To stay current with reference to the OpenFrame library, use the following resource URI: `https://[servicenow instance]/scripts/openframe/latest/openFrameAPI.min.js`.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## openFrameAPI - getAWAAgentPresence\(String success, String failure\)

Returns the logged in agent’s current presence state.

|Name|Type|Description|
|----|----|-----------|
|success|String|If the method is successful, name of the callback function to invoke.|
|failure|String|If the method fails, name of the callback function to invoke.|

<table id="table_abt_mgn_sbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

presence

</td><td>

Results passed to the success callback function by the openFrame infrastructure.Data type: Object

```
"presence": {  
  "available": Boolean, 
  "channels": [Array],
  "name": "String", 
  "sys_id": "String"
}
```

</td></tr><tr><td>

presence.available

</td><td>

Flag that indicates whether the associated agent is available.Valid values:

-   true: Agent is available.
-   false: Agent isn't available.

Data type: Boolean

</td></tr><tr><td>

presence.channels

</td><td>

List of available channels of communication with the agent.Data type: Array of Objects

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

presence.channels.available

</td><td>

Flag that indicates whether the channel is available.Valid values:

-   true: Channel is available.
-   false: Channel isn't available.

Data type Boolean

</td></tr><tr><td>

presence.channels.name

</td><td>

Name of the channel, such as Chat or Phone.Data type: String

</td></tr><tr><td>

presence.channels.restrict\_update

</td><td>

Flag that indicates whether the user can restrict updates to the channel. Valid values:

-   true: User can restrict updates to the channel.
-   false: User can't restrict updates to the channel.

Data type Boolean

</td></tr><tr><td>

presence.channels.service\_channel\_type

</td><td>

Type of the service channel.Data type: String

</td></tr><tr><td>

presence.channels.sys\_id

</td><td>

Sys\_id of the channel record.Data type: String

Table: Service Channels \[awa\_service\_channel\]

</td></tr><tr><td>

presence.name

</td><td>

Name of the agent's presence state.Data type: String

</td></tr><tr><td>

presence.sys\_id

</td><td>

Sys\_id of the presence state record.Data type: String

Table: Presence States \[awa\_presence\_state\]

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
function failure(data)
{
  console.log("failure: " + JSON.stringify(data));
}
 
function success(data)
{
  console.log("success: " + JSON.stringify(data));
}
 
openFrameAPI.getAWAAgentPresence(success, failure)
```

Response to success callback function:

```
success: { 
  "presence": { 
    "name": "Available", 
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
    ] 
  } 
}
```

## openFrameAPI - hide\(\)

Hides the OpenFrame in the TopFrame.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.hide()
```

## openFrameAPI - init\(Object config, function successCallback, function failureCallback\)

Initializes OpenFrame. This must be the first method that you call.

This method initializes communication to TopFrame and initializes any visual elements passed in the **config** parameter.

<table id="table_vz3_jyw_kt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

config

</td><td>

Object

</td><td>

Name-value pairs to use during the initialization process.Possible keys:

-   height
-   subTitle
-   title
-   titleIcon
-   width

All keys are optional. Pass an empty object if you don't want to set these key-value pairs.

</td></tr><tr><td>

successCallback

</td><td>

function

</td><td>

Name of the callback function to use if the init method succeeds. The [OpenFrame configuration](https://www.servicenow.com/docs/access?context=t_CreateAnOpenFrameConfiguration&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) stored in the system is passed as a parameter to the callback function.

</td></tr><tr><td>

failureCallback

</td><td>

function

</td><td>

Name of the callback function to use if the init method fails.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var config = {
height: 300,
width: 200
}
function handleCommunicationEvent(context) {
console.log("Communication from Topframe", context);
}
function initSuccess(snConfig) {
console.log("openframe configuration", snConfig);
//register for communication event from TopFrame
openFrameAPI.subscribe(openFrameAPI.EVENTS.COMMUNICATION_EVENT,
handleCommunicationEvent);
}
function initFailure(error) {
console.log("OpenFrame init failed...", error);
}
openFrameAPI.init(config, initSuccess, initFailure);
```

## openFrameAPI - isVisible\(function callback\)

Checks to see if the OpenFrame is visible in the TopFrame.

|Name|Type|Description|
|----|----|-----------|
|callback|function|The callback function receives a parameter with a value of true or false. True if OpenFrame is visible and false if not visible.|

|Type|Description|
|----|-----------|
|void| |

```
function callback(isVisible) {
console.log(isVisible)
}
openFrameAPI.isVisible(callback)
```

## openFrameAPI - openCustomURL\(String details\)

Opens a custom URL in the UI16 interface.

<table id="table_ob3_ryd_lt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Url

</td><td>

String

</td><td>

Text of the custom URL.Maximum size: 2083 characters

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.openCustomURL('10_cool_things.do');

```

## openFrameAPI - openServiceNowForm\(Object details\)

Opens a form URL.

When an agent receives an incoming call, the OpenFrame window displays information such as the account, contact, or consumer. Clicking a link in the OpenFrame window displays the corresponding record.

-   In the platform interface, this API opens a form URL in TopFrame.
-   For Agent Workspace, this API supports interaction tab management. In Agent Workspace, an interaction record opens in a parent tab and the specified entity record opens in a child tab under the interaction tab.

<table id="table_ulq_vwd_lt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

details

</td><td>

Object

</td><td>

Key-value pairs that identify the form URL to open. ```
"details": {
  "entity": "String";
  "interaction_sys_id": "String";
  "query": "String"
}
```

</td></tr><tr><td>

details.entity

</td><td>

String

</td><td>

Table or entity name.

</td></tr><tr><td>

details.interaction\_sys\_id

</td><td>

String

</td><td>

Optional. Sys\_id of the interaction record to open as parent tab in Agent Workspace.**Note:** In the platform interface the **interaction\_sys\_id** is ignored.

</td></tr><tr><td>

details.query

</td><td>

String

</td><td>

Query to identify the record to open, such as: `query:'sys_id=<record_sys_id>'`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows basic usage in platform:

```
openFrameAPI.openServiceNowForm({entity:'customer_account', 
query:'sys_id=447832786f0331003b3c498f5d3ee452', 'interaction_sys_id':'3be092313b711300758ce9b534efc4dd'});
```

The following example shows how to use the **query** parameter to create a new record with data provided in the form by using sysparm\_query and an encoded query to populate the first and last name fields in Workspace:

```
openFrameAPI.openServiceNowForm({ entity: 'sys_user',
query: 'sys_id=-1&sysparm_query=first_name=Ivan^last_name=Greggor' });
```

## openFrameAPI - openServiceNowFormwithChildTab\(\)

Opens a ServiceNow form with a child tab if invoked in a workspace or opens an entity if invoked in the UI16 interface.

<table id="table_j13_hwv_hyb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

openServiceNowFormwithChildTab

</td><td>

Object

</td><td>

Defines if the API opens a ServiceNow form with a child tab if invoked in a workspace or opens an entity if invoked in the UI16 interface.```
openFrameAPI.openServiceNowFormwithChildTab({
  entity: "String",
  sys_id: String", 	
  parent_entity: "String",	
  parent_entity_sys_id: "String"
})
```

</td></tr><tr><td>

openServiceNowFormwithChildTab.entity

</td><td>

String

</td><td>

Name of the table that contains the record to open.

</td></tr><tr><td>

openServiceNowFormwithChildTab.sys\_id

</td><td>

String

</td><td>

Sys\_id of the record to open.

</td></tr><tr><td>

openServiceNowFormwithChildTab.parent\_entity

</td><td>

String

</td><td>

Name of the table to open as a parent tab.

</td></tr><tr><td>

openServiceNowFormwithChildTab.parent\_entity\_sys\_id

</td><td>

String

</td><td>

Sys\_id of the parent record to open.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example opens the parent entity as a parent tab on a configured workspace, or opens just the entity if invoked in UI16.

```
openFrameAPI.openServiceNowFormwithChildTab({
  entity: "customer_account", 
  sys_id: "447832786f0331003b3c498f5d3ee452", 	
  parent_entity: "interaction", 
  parent_entity_sys_id: "3be092313b711300758ce9b534efc4dd"
});
```

## openFrameAPI - openServiceNowList\(Object details\)

Opens a list URL in the UI16 interface.

<table id="table_fpq_5xd_lt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

details

</td><td>

Object

</td><td>

Key value pairs that describe the content to use when opening the list URL.Valid values:

-   entity: Table name
-   query: [Encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.openServiceNowList({entity:'case', query:'active=true'});
```

## openFrameAPI - setFrameMode\(mode\)

Sets the OpenFrame mode.

The mode passed in this API:

-   Sets the appropriate icon in the header: collapse or expand
-   Raises the relevant event for CTI:
    -   openFrameAPI.EVENTS.COLLAPSE
    -   openFrameAPI.EVENTS.EXPAND

<table id="table_yzb_mxx_kt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mode

</td><td>

String

</td><td>

Set OpenFrame Mode. Enumerated options:1.  openFrameAPI.FRAME\_MODE.COLLAPSE
2.  openFrameAPI.FRAME\_MODE.EXPAND

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setFrameMode(openFrameAPI.FRAME_MODE.COLLAPSE);

```

## openFrameAPI - setHeight\(height\)

Sets the OpenFrame height.

|Name|Type|Description|
|----|----|-----------|
|Height|Number|Height in pixels|

|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setHeight(100);
```

## openFrameAPI - setICContext\(String Type, Object &lt;Context&gt;\)

Sets the context data related to the interaction controls on the client. Use this context data to determine the client UI to display in OpenFrame.

For additional information on interactive controls, see [Interaction Controls Component](https://www.servicenow.com/docs/access?context=interaction-controls-component&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

For additional information on interaction records, see [CSM voice interaction record page](https://www.servicenow.com/docs/access?context=csm-native-voice-record-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

<table id="table_xlq_rhg_zdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

String

</td><td>

Type of context data to set. Valid values:

-   activeCall: Sets the context for the ongoing Active call component. When you pass this context type, you must also pass the `activeCall[]`**Context** parameter.
-   idleState: Sets the idle state capabilities for the current user. When this type is set, the idle state UI \(dial pad\) appears in OpenFrame. When you pass this context type, you must also pass the `<idleState>{}` JSON as the **Context** parameter.
-   offerContext: Sets the current participant's offer context for resiliency. When you pass this context type, you must also pass the `offerContext{}` JSON as the **Context** parameter.
-   searchTargetList: Sets the telephone directory context. When this type is set, it enables **Transfer call** on the Active call component. When you pass this context type, you must also pass the `searchTargetList[]` JSON as the **Context** parameter.

</td></tr><tr><td>

&lt;Context&gt;

</td><td>

Object

</td><td>

Context data to set. Each context data type is a unique set of input data.Valid **Context** data objects:

-   `activeCall`
-   `idleState`
-   `offerContext`
-   `searchTargetList`

</td></tr><tr><td>

activeCall

</td><td>

Array of Objects

</td><td>

Context details about an active call. Each object represents an ongoing active call.```
"activeCall": [
  { 
    "callbackContext": {Object},
    "currentParticipant": {Object},
    "customPayload: {Object},
    "direction": "String",
    "externalId": "String",
    "nowRecordId": "String",
    "nowRecordTable": "String",
    "participants": [Array],
    "type": "String"
  }
]
```

</td></tr><tr><td>

activeCall.callbackContext

</td><td>

Object

</td><td>

Only used if the **activeCall.type** property is `callback`. Callback context information for the ongoing callback component.```
"callbackContext": {
  "callAttemptedByAgent": Boolean,
  "callbackNumbers": [Array],
  "closeInEndTime": "String",
  "customerName": "String",
  "dialInEndTime": "String"
}
```

</td></tr><tr><td>

activeCall. callbackContext. callAttemptedByAgent

</td><td>

Boolean

</td><td>

Flag that indicates whether callback was attempted by a customer service agent.Valid values:

-   true: The callback was attempted by a customer service agent. If true, set **closeInEndTime**.
-   false: The callback wasn’t attempted by a customer service agent. If false, set **dialInEndTime**.

Default: False

</td></tr><tr><td>

activeCall. callbackContext. callbackNumbers

</td><td>

Array

</td><td>

List of phone numbers provided as strings.

</td></tr><tr><td>

activeCall. callbackContext. closeInEndTime

</td><td>

String

</td><td>

Set only if **callAttemptedByAgent** is true. End time for callback in UTC format.

</td></tr><tr><td>

activeCall. callbackContext. customerName

</td><td>

String

</td><td>

Name of the customer.

</td></tr><tr><td>

activeCall. callbackContext. dialInEndTime

</td><td>

String

</td><td>

Set only if **callAttemptedByAgent** is false and the type of callback is auto-dial. Dial-in end time for callback in UTC format.

</td></tr><tr><td>

activeCall.currentParticipant

</td><td>

Object

</td><td>

Required. Details about the current participant's call capabilities and call status.```
"currentParticipant": {
  "actor": "String",
  "callStartTime": "String",
  "capabilities": {Object},
  "connectedTime": "String",
  "custom-capability-state-1": Boolean,
  "flagged": Boolean,
  "held": Boolean,
  "id": "String",
  "muted": Boolean,
  "name": "String",
  "paused": Boolean,
  "recording": "String",
  "state": "String",
  "wrapUP": {Object}
}
```

</td></tr><tr><td>

activeCall.currentParticipant.​actor

</td><td>

String

</td><td>

Type of participant on the call.Valid values:

-   agent

**Note:** Other participant types to be added in the future.

</td></tr><tr><td>

activeCall.currentParticipant.​callStartTime

</td><td>

String

</td><td>

Date and time that the call started.Time standard: UTC

Format: RSS - "&lt;day of week&gt;, dd mmm yyyy hh:MM:ss GMT". For example: "Wed, 17 Dec 2024 05:23:41 GMT"

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities

</td><td>

Object

</td><td>

Details about the capabilities that the current \(agent\) participant can perform during a call. The associated icons appear in the Active call component for the capabilities that are enabled.![Screen shot of Active call component with capabilities icons](../image/OF-active_call-capabilities.png)

```
"capabilities": {
  "callbackTransferStatus": "String",
  "cancelCallbackTransferEligible": Boolean,
  "closeCallback": Boolean,
  "dtmf": Boolean,
  "endCall": Boolean,
  "flag": Boolean,
  "hold": Boolean,
  "initiateCall": Boolean,
  "leaveAndTransfer": Boolean,
  "mergeCall": Boolean,
  "mute": Boolean,
  "resumeRecording": Boolean,
  "pauseRecording": Boolean,
  "startRecording": Boolean,
  "stopRecording": Boolean,
  "transfer": Boolean
}
```

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.callbackTransferStatus

</td><td>

String

</td><td>

CCaaS \(Contact Center as a Service\) callback transfer status.Possible values:

-   Failed
-   Empty string \(default\)

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.cancelCallbackTransferEligible

</td><td>

Boolean

</td><td>

Flag that indicates if the cancel callback transfer option is enabled.Valid values:

-   true: Cancel callback transfer option is enabled.
-   false: Cancel callback transfer option is disabled.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.closeCallback

</td><td>

Boolean

</td><td>

Flag that indicates whether the close callback button is enabled.Valid values:

-   true: Close callback button is enabled.
-   false: Close callback button is disabled.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​dtmf

</td><td>

Boolean

</td><td>

Flag that indicates whether the agent has dual tone multi-frequency \(DTMF\) capability for the current call.Valid values:

-   true: Participant has DTMF capability.
-   false: Participant doesn't have DTMF capability.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​endCall

</td><td>

Boolean

</td><td>

Flag that indicates whether the associated participant can end the call.Valid values:

-   true: Participant can end the call. The end call button is enabled in the UI.
-   false: Participant can't end the call. The end call button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​flag

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can flag the call for quality issues, such as voice quality problems.Valid values:

-   true: Participant can flag problem calls.
-   false: Participant can't flag problem calls.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​hold

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can put the call on hold.Valid values:

-   true: Participant can put the call on hold. The hold button is enabled in the UI.
-   false: Participant can't put the call on hold. The hold button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​initiateCall

</td><td>

Boolean

</td><td>

Flag that indicates whether the associated participant can start the call.Valid values:

-   true: Participant can start the call. The initiate call button is enabled in the UI.
-   false: Participant can't start the call. The initiate call button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​leaveAndTransfer

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can transfer the call to another agent and then drop off the call. Enable this capability for actions such as consult transfers, where the user who is consulted is not the owner of the call.Valid values:

-   true: Participant can transfer and drop off the call.
-   false: Participant can't transfer and drop off the call.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​mergeCall

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can merge the call. Use this capability when the participant's call legs are capable of merging.Valid values:

-   true: Participant can merge the call. The merge button is enabled in the UI.
-   false: Participant can't merge the call. The merge button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​mute

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can mute the call.Valid values:

-   true: Participant can mute the call. The mute button is enabled in the UI.
-   false: Participant can't mute the call. The mute button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​resumeRecording

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can resume recording the call.Valid values:

-   true: Participant can resume recording the call. The pause recording button is enabled in the UI.
-   false: Participant can't resume recording the call. The pause recording button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​pauseRecording

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can pause recording the call.Valid values:

-   true: Participant can pause recording the call. The pause recording button is enabled in the UI.
-   false: Participant can't pause recording the call. The pause recording button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​startRecording

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can start recording the call.Valid values:

-   true: Participant can start recording the call. The recording button is enabled in the UI.
-   false: Participant can't start recording the call. The recording button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​stopRecording

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can stop recording the call.Valid values:

-   true: Participant can stop recording the call. The stop recording button is enabled in the UI.
-   false: Participant can't stop recording the call. The stop recording button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​capabilities.​transfer

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can transfer the call.Valid values:

-   true: Participant can transfer the call. The transfer button is enabled in the UI.
-   false: Participant can't transfer the call. The transfer button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​connectedTime

</td><td>

String

</td><td>

Date and time that the call initially connected.Time base: UTC

Format: RSS - "&lt;day of week&gt;, dd mmm yyyy hh:MM:ss GMT". For example: "Wed, 17 Dec 2024 05:23:41 GMT"

</td></tr><tr><td>

activeCall.currentParticipant.​custom-capability-state-1

</td><td>

Boolean

</td><td>

Flag that indicates whether there are any current participants on the call.Valid values:

-   true: Current participants on the call.
-   false: No current participants on the call.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​flagged

</td><td>

Boolean

</td><td>

Flag that indicates whether the call is flagged for an issue, such as a voice quality issue.Valid values:

-   true: Call has been flagged for an issue.
-   false: Call hasn't been flagged for an issue.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​held

</td><td>

Boolean

</td><td>

Flag that indicates the participant’s held state.Valid values:

-   true: Participant is on-hold.
-   false: Participant isn't on-hold.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​id

</td><td>

String

</td><td>

Required. Sys\_id of the associated participant record, such as the sys\_id of the agent.Table: User \[sys\_user\]

</td></tr><tr><td>

activeCall.currentParticipant.​muted

</td><td>

Boolean

</td><td>

Flag that indicates the participant’s muted state.Valid values:

-   true: Participant is muted.
-   false: Participant isn't muted.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​name

</td><td>

String

</td><td>

Participant's name.

</td></tr><tr><td>

activeCall.currentParticipant.​paused

</td><td>

Boolean

</td><td>

Flag that indicates the participant’s paused state.Valid values:

-   true: Participant is paused.
-   false: Participant isn't paused.

Default: false

</td></tr><tr><td>

activeCall.currentParticipant.​recording

</td><td>

String

</td><td>

Current recording state of the call.Valid values:

-   in\_progress
-   none

</td></tr><tr><td>

activeCall.currentParticipant.​wrapUP

</td><td>

Object

</td><td>

Future use.

</td></tr><tr><td>

activeCall.customPayload

</td><td>

Object

</td><td>

Custom payload to pass to OpenFrame as part of OpenFrame events. This is a free-form object and can contain any data needed to customize the active call component, such as adding buttons or text.

</td></tr><tr><td>

activeCall.direction

</td><td>

String

</td><td>

Direction of the call for the associated participant.Valid values:

-   inbound
-   outbound

</td></tr><tr><td>

activeCall.externalId

</td><td>

 

</td><td>

Required. Unique value that identifies the current active call on the associated external system.

</td></tr><tr><td>

activeCall.​nowRecordId

</td><td>

String

</td><td>

Required. Sys\_id of the active call record.Table: Interaction \[interaction\] Only supported option for base system.

</td></tr><tr><td>

activeCall.​nowRecordTable

</td><td>

String

</td><td>

Required. Table to which the active call belongs. Table: Interaction \[interaction\] Only supported option for base system.

</td></tr><tr><td>

activeCall.​participants

</td><td>

Array of Objects

</td><td>

Required. List of the additional participants on the call. A participant can be an agent, a customer, an external person who is not an agent or a customer, or a queue.```
"participants": [
  {
    "actor": "String",
    "ani": "String",
    "address": "String",
    "capabilities": {Object},
    "callStartTime" "String",
    "connectedTime": "String",
    "customPayload": {Object},
    "dnis": "String",
    "held": Boolean,
    "heldAtTime": "String",
    "id": "String",
    "muted": Boolean,
    "name": "String",
    "requestACW": Boolean,
    "requireWrapup": Boolean,
    "state": "String"
  }
]
```

</td></tr><tr><td>

activeCall.​participants.​actor

</td><td>

String

</td><td>

Type of actor for the associated participant. For example:

-   agent
-   customer
-   external
-   queue

</td></tr><tr><td>

activeCall.​participants.​ani

</td><td>

 

</td><td>

Automatic number identification. Telephone number to display to the receiver of the phone call.

</td></tr><tr><td>

activeCall.​participants.​address

</td><td>

String

</td><td>

Participant's telephone number.

</td></tr><tr><td>

activeCall.​participants.​capabilities

</td><td>

Object

</td><td>

Details about the type of capabilities that the participant has for the associated call.```
"capabilities": {
  "endCall": Boolean,
  "hold": Boolean,
  "mute": Boolean
}
```

</td></tr><tr><td>

activeCall.​participants.​capabilities.​endCall

</td><td>

Boolean

</td><td>

Flag that indicates whether the associated participant can end the call.Valid values:

-   true: Participant can end the call. The end call button is enabled in the UI.
-   false: Participant can't end the call. The end call button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.​participants.​capabilities.​hold

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can put the call on hold.Valid values:

-   true: Participant can put the call on hold. The hold button is enabled in the UI.
-   false: Participant can't put the call on hold. The hold button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.​participants.​capabilities.​mute

</td><td>

Boolean

</td><td>

Flag that indicates whether the participant can mute the call.Valid values:

-   true: Participant can mute the call. The mute button is enabled in the UI.
-   false: Participant can't mute the call. The mute button is disabled in the UI.

Default: false

</td></tr><tr><td>

activeCall.​participants.​connectedTime

</td><td>

String

</td><td>

Required. Date and time that the participant initially connected to the call.Time standard: UTC

Format: RSS - "&lt;day of week&gt;, dd mmm yyyy hh:MM:ss GMT". For example: "Wed, 17 Dec 2024 05:23:41 GMT"

</td></tr><tr><td>

activeCall.​participants.​customPayload

</td><td>

Object

</td><td>

Custom payload to pass to OpenFrame as part of Open Frame custom events. This is a free-form object and can contain any data needed to customize the Active call component, such as adding buttons or text.

</td></tr><tr><td>

activeCall.​participants.​dnis

</td><td>

String

</td><td>

Dialed Number Identification Service. Telephone number the participant dialed.

</td></tr><tr><td>

activeCall.​participants.​held

</td><td>

Boolean

</td><td>

Flag that indicates the participant’s held state.Valid values:

-   true: Participant is on-hold.
-   false: Participant isn't on-hold.

Default: false

</td></tr><tr><td>

activeCall.​participants.​heldAtTime

</td><td>

String

</td><td>

Date and time that the participant's connection to the call was put on hold.Time base: UTC

Format: RSS - "&lt;day of week&gt;, dd mmm yyyy hh:MM:ss GMT". For example: "Wed, 17 Dec 2024 05:23:41 GMT"

</td></tr><tr><td>

activeCall.​participants.​id

</td><td>

String

</td><td>

Required. Participant's unique ID from the Contact Center as a Service \(CCaaS\) system.

</td></tr><tr><td>

activeCall.​participants.​muted

</td><td>

Boolean

</td><td>

Flag that indicates the participant’s mute state.Valid values:

-   true: Participant is muted.
-   false: Participant isn't muted.

Default: false

</td></tr><tr><td>

activeCall.​participants.​name

</td><td>

String

</td><td>

Name of the participant.

</td></tr><tr><td>

activeCall.​participants.​requestACW

</td><td>

Boolean

</td><td>

For agent use case only - only valid when the **activeCall.currentParticipant.actor** is "agent".Flag that indicates whether the participant is to follow up with the customer.

Valid values:

-   true: Follow-up required.
-   false: No follow-up required.

Default: false

</td></tr><tr><td>

activeCall.​participants.​requireWrapup

</td><td>

Boolean

</td><td>

For agent use case only - only valid when the **activeCall.currentParticipant.actor** is "agent".Flag that indicates whether to display the **Wrap up** component once the call is complete.

![Screen shot of Wrap up component](../image/OF-active_call-wrapup.png)

Valid values:

-   true: Display the **Wrap up** component at call completion.
-   false: Don't display the **Wrap up** component at call completion.

Default: false

</td></tr><tr><td>

activeCall.​participants.​state

</td><td>

String

</td><td>

State of the participant's call leg. Appears beneath the phone number in the **Active call** component.![Active call window showing state](../image/OF-active_call-state.png)

This can be any meaningful text, such as:

-   Alerting
-   Connected
-   Ringing

</td></tr><tr><td>

activeCall.type

</td><td>

String

</td><td>

Type of call.Valid values:

-   call
-   callback

**Note:** If set, you must include the **activeCall.callbackContext** object details.

-   voicemail

</td></tr><tr><td>

idleState

</td><td>

Object

</td><td>

Describes the idle state context of the agent. This context data determines the information that appears on the dial pad when an agent is waiting for a call and the capabilities they have through this dial pad.```
idleState {
 "capability": {Object},
 "currentInboundId": "String",
 "dialpadInfoMessage": {Object},
 "enableState": {Object}
}
```

</td></tr><tr><td>

idleState.capability

</td><td>

Object

</td><td>

Description of the current user's idle state capabilities.```
"capability": {
  "globalContactSearch": Boolean,
  "logOut": Boolean,
  "outBoundCall": Boolean
}
```

</td></tr><tr><td>

idleState.capability.​globalContactSerarch

</td><td>

Boolean

</td><td>

Flag that indicates whether to display the global contact list while in the idle state.Valid values:

-   true: Display the global contact list.
-   false: Don't display the global contact list.

Default: false

</td></tr><tr><td>

idleState.capability.​logOut

</td><td>

Boolean

</td><td>

Flag that indicates whether the user can logout while in the idle state.Valid values:

-   true: User can log out when the call is idle. The log out button appears on the dial pad.
-   false: User can't log out when the call is idle.

Default: false

</td></tr><tr><td>

idleState.capability.​outBoundCall

</td><td>

Boolean

</td><td>

Flag that indicates whether the user can make an outbound call while in the idle state.Valid values:

-   true: User can make an outbound call when the call is idle.
-   false: User can't make an outbound call when the call is idle.

Default: false

</td></tr><tr><td>

idleState.​currentInboundId

</td><td>

String

</td><td>

Inbound identifier of the provider application used to create the outbound call interaction.Table: Located in the id field of the Provider Channel Identities \[sys\_cs\_provider\_application\] table.

Default: Base system provider application

</td></tr><tr><td>

idleState.​dialpadInfoMessage

</td><td>

Object

</td><td>

Details about the information message to display on the user's dial pad, such as the currently selected queue.```
"dialpadInfoMessage": {
   "label": "String",
   "value": "String"
 }
```

In the following example, the **label** is **Selected queue:** and the **value** is **Customer Inquiries**. You can also just use either the **label** or the **value** parameter with **Selected queue: Customer Inquiries**.

![Screen shot of dial pad with information message](../image/OF-dialpadInfoMessage.png)

</td></tr><tr><td>

idleState.​dialpadInfoMessage.​label

</td><td>

String

</td><td>

Free-form label to display on the dial pad.

</td></tr><tr><td>

idleState.​dialpadInfoMessage.​value

</td><td>

String

</td><td>

Free-form message text to display after the label on the dial pad.

</td></tr><tr><td>

idleState.​enableState

</td><td>

Object

</td><td>

Details about the enable state of the buttons on the dial pad.```
"enableState": {
   "logOut": Boolean,
   "outBoundCall": Boolean
 }
```

</td></tr><tr><td>

idleState.​enableState.​logOut

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the logout button in the UI while in the idle state.Valid values:

-   true: Display the logout button while in the idle state.
-   false: Don't display the logout button while in the idle state.

Default: false

</td></tr><tr><td>

idleState.​enableState.​outBoundCall

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable the outbound call button in the UI while in the idle state.Valid values:

-   true: Display the outbound call button while in the idle state.
-   false: Don't display the outbound call button while in the idle state.

Default: false

</td></tr><tr><td>

offerContext

</td><td>

Object

</td><td>

Details about the current participant's offer context for resiliency.```
{
  "assignment": {Object},
  "creationTime": "String",
  "description": "String",
  "displayContent": {Object},
  "externalId": "String",
  "externalSegmentId": "String",
  "isResilient": Boolean,
  "metadata": {Object},
  "nowRecordId": "String",
  "nowRecordTable": "String",
  "providerAppInboundId": "String",
  "queueId": "String",
  "requesterId": "String",
  "transferContent": {Object},
  "type": "String"
}
```

</td></tr><tr><td>

offerContext.assignment

</td><td>

Object

</td><td>

Details about the agent assignment.```
"assignment": {
  "allowedToDecline": Boolean,
  "enableAutoAssign": Boolean,
  "offeredOn": "String",
  "timeout": "String"
}
```

</td></tr><tr><td>

offerContext.assignment. allowedToDecline

</td><td>

Boolean

</td><td>

Required. Flag that indicates whether the agent is allowed to decline the assignment.Valid values:

-   true: The agent is allowed to decline the assignment.
-   false: The agent is not allowed to decline the assignment.

Default: false

</td></tr><tr><td>

offerContext.assignment. enableAutoAssign

</td><td>

Boolean

</td><td>

Required. Flag that indicates whether an agent receive the assignment automatically.Valid values:

-   true: An agent can receive the assignment automatically.
-   false: An agent can not receive the assignment automatically.

Default: false

</td></tr><tr><td>

offerContext.assignment. offeredOn

</td><td>

String

</td><td>

Date at which the offer was made in UTC format \(Www, dd Mmm yyyy HH:mm:ss GMT\).

</td></tr><tr><td>

offerContext.assignment. timeout

</td><td>

String

</td><td>

Time in milliseconds to assign to an agent before timeout.

</td></tr><tr><td>

offerContext.creationTime

</td><td>

String

</td><td>

Optional. Call creation date and time in UTC format \(YYYY-MM-DDTHH:MM:SS\).

</td></tr><tr><td>

offerContext.description

</td><td>

String

</td><td>

Optional. Description of the offer.

</td></tr><tr><td>

offerContext.displayContent

</td><td>

Object

</td><td>

Optional. Unique JSON payload values representing values displayed on screen.

</td></tr><tr><td>

offerContext.externalId

</td><td>

String

</td><td>

Unique value that identifies the current active call on the associated external system.

</td></tr><tr><td>

offerContext.isResilient

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the offer context is resilient.Valid values:

-   true: The offer context is resilient.
-   false: The offer context is not resilient.

Default: true

</td></tr><tr><td>

offerContext.metadata

</td><td>

Object

</td><td>

Optional. Free-form custom JSON payload values.

</td></tr><tr><td>

offerContext.​nowRecordId

</td><td>

String

</td><td>

Required. Sys\_id of the active call record.Table: Interaction \[interaction\] Only supported option for base system.

</td></tr><tr><td>

offerContext.​nowRecordTable

</td><td>

String

</td><td>

Optional. Use this property to set the work item and segment for transfers.

</td></tr><tr><td>

offerContext. providerAppInboundId

</td><td>

String

</td><td>

Optional. Unique ID from the inbound third-party provider.

</td></tr><tr><td>

offerContext.​queueId

</td><td>

String

</td><td>

Required for regular \(non-transfer\) assignments. Unique ID representing the assignment queue. Use the **transferContent.targetId** property for transfer assignments.

</td></tr><tr><td>

offerContext.​requesterId

</td><td>

String

</td><td>

Required. Unique ID of the offer requester. For voice, this value can be the phone number of the user.

</td></tr><tr><td>

offerContext.transferContent

</td><td>

Object

</td><td>

Details required for transfer assignments.```
"transferContent": {
  "sourceQueueId": "String",
  "targetId": "String",
  "targetType": "String",
  "transferType": "String"
}
```

</td></tr><tr><td>

offerContext.transferContent. sourceQueueId

</td><td>

String

</td><td>

The sys\_id or external ID of the assignment queue.

</td></tr><tr><td>

offerContext.transferContent. targetId

</td><td>

String

</td><td>

The sys\_id or external ID of the queue transfer.

</td></tr><tr><td>

offerContext.transferContent. targetType

</td><td>

String

</td><td>

Type of transfer target.Valid values:

-   agent
-   queue

</td></tr><tr><td>

offerContext.transferContent. transferType

</td><td>

String

</td><td>

Type of transfer.Valid values:

-   blind
-   consult

</td></tr><tr><td>

offerContext.type

</td><td>

String

</td><td>

Type of call.Valid values:

-   call
-   callback request
-   voicemail

</td></tr><tr><td>

searchTargetList

</td><td>

Array of Objects

</td><td>

Context details of the transfer related data for a ServiceNow table.```
"searchTargetList": [
  {
    "externalId": "String",
    "nowRecordId": "String",
    "nowRecordTable": "String",
    "participantID": "String",
    "targets": [Array]
  }
]
```

</td></tr><tr><td>

searchTargetList.​externalId

</td><td>

String

</td><td>

Unique identifier of the associated call on the CCaaS system.

</td></tr><tr><td>

searchTargetList.​nowRecordId

</td><td>

String

</td><td>

Required. Sys\_id of the record to which the searchTargetList belongs. **Note:** Only records in the Interaction \[interaction\] table are currently supported.

</td></tr><tr><td>

searchTargetList.​nowRecordTable

</td><td>

String

</td><td>

Required. ServiceNow table to which the searchTargetList belongs.Table: Only valid value - `"interaction"`

</td></tr><tr><td>

searchTargetList.​participantID

</td><td>

String

</td><td>

Unique identifier for the participant from the CCaaS system.

</td></tr><tr><td>

searchTargetList.​targets

</td><td>

Array of Objects

</td><td>

Details about the agents, external users, and/or queues to whom the call can be transferred.```
"targets": [
  {
    "payload": {Object},
    "transferSubtypes": [Array],
    "type": "String"
  }
]
```

</td></tr><tr><td>

searchTargetList.​targets.​payload

</td><td>

Object

</td><td>

Details about the information to display in the transfer call control.The following is an example of a **Transfer call** control that contains a list of agents that the call can be transferred to. The screen shot shows what elements of the UI that each parameter in the **list.payload** controls.

![Screen shot of Transfer call window showing parameter association](../image/OF-search_payload_parms.png)

```
"payload": {
  "list": [Array]
}
```

This example shows an agent payload \(`"searchTargetList.targets.type" : "agent"`\).

```
"payload": {
  "list": [
    {
      "name": "Alice Anderson",
      "id": "agent1Id",
      "hasStats": "true",
      "presence": "available",
      "moreInfo": [
        {
          "label": "Skill",
          "value": "CRM certified"
        }
      ]
    }
  ]
}
```

The following shows an example of a queue payload \(`"searchTargetList.targets.type" : "queue"`\).

```
"payload": {
  "list": [
    {
      "name": "Product Support Queue",
      "id": "queue1Id",
      "hasStats": "true",
      "moreInfo": [
        {
          "label": "Skill",
          "value": "10sec"
        },
        {
          "label": "Queue Skill",
          "value": "German"
        }
      ]
    },
    {
      "name": "Billing Queue",
      "id": "queue2Id",
      "hasStats": "true",
      "moreInfo": [
        {
           "label": "Skill",
           "value": "10sec"
        }
      ]
    }
  ]
}
```

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list

</td><td>

Array of Objects

</td><td>

Details about the payload for each type of target.```
"list": [
  {
    "hasStats": Boolean,
    "id": "String",
    "moreInfo": [Array],
    "name": "String",
    "presence": "String"
  }
]
```

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list.​hasStats

</td><td>

Boolean

</td><td>

Flag that indicates whether the associated target has additional statistics such as a wait-time for a queue.Valid values:

-   true: Target has additional statistics. An information icon appears next to the agent name or queue.
-   false: Target doesn't have additional statistics.

Default: false

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list.​id

</td><td>

String

</td><td>

Unique identifier of the agent or queue in the CCaaS system.

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list.​moreInfo

</td><td>

Array of Objects

</td><td>

Required if **searchTargetList.targets.payload.list.hasStats** is set to `"true"`. List of skills that the agent or queue has. This information appears in a pop-up window when the user selects the information icon at the end of the entities name.```
"moreInfo": [
  {
    "label": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list.​moreInfo.​label

</td><td>

String

</td><td>

Free-form label for the information to display in the pop-up window, such as a **Skill** or **Language**.

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list.​moreInfo.​value

</td><td>

String

</td><td>

Text to display in the pop-up window after the label, such as **CRM certified** or **German**.

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list.​name

</td><td>

String

</td><td>

Name of the agent, external user, or queue. Located in the CCaaS system.

</td></tr><tr><td>

searchTargetList.​targets.​payload.​list.​presence

</td><td>

String

</td><td>

Presence state of the associated agent. This parameter is only valid for a**searchTargetList.targets.type** of `"agent"`.Valid values:

-   available
-   away
-   busy
-   offline

</td></tr><tr><td>

searchTargetList.​targets.​transferSubtypes

</td><td>

Array of Objects

</td><td>

Details about the type of transfer supported for the specified **searchTargetList.targets.type**. This information appears when the user clicks the ellipse next to the target's name in the UI.

![Transfer call component showing transfer types](../image/OF-transferSuptypes.png)

For example, if only a consult type is supported for the current target type, say queue, this array will contain one object to denote the consult type of transfer.

```
"transferSubtypes": [
  {
    "id": "String",
    "label": "String"
  }
]
```

</td></tr><tr><td>

searchTargetList.​targets.​transferSubtypes.​id

</td><td>

String

</td><td>

Identifier of the transfer subtype.Valid values:

-   blind: Agent directly transfers the customer call to another agent or queue without first speaking to the agent.
-   consult: Agent contacts the agent to whom they want to consult, then merges the customer into the call with the consulting agent.

This must correspond to the value in **searchTargetList.targets.transferSubtypes.label**.

</td></tr><tr><td>

searchTargetList.​targets.​transferSubtypes.​label

</td><td>

String

</td><td>

Label of the transfer subtype. If you don't pass a label, nothing appears in the UI for transfer subtype.Valid values:

-   Blind
-   Consult

This must correspond to the value in **searchTargetList.targets.transferSubtypes.id**.

</td></tr><tr><td>

searchTargetList.​targets.​type

</td><td>

String

</td><td>

Type of target.Valid values:

-   agent
-   external
-   queue

</td></tr></tbody>
</table><table id="table_ylq_rhg_zdc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

 

</td></tr><tr><td>

Error \(offerContext\)

</td><td>

Error messages associated with the **offerContext** object used for resiliency. To view these messages, use the [subscribe\(\)](c_openFrameAPI.md#) method to subscribe to **openframe\_awa\_client\_offer** event.Context values are represented as follows:

1.  success
2.  error
3.  partialSuccess

-   **AWA\_EXTUSER\_ROLE\_CHECK\_FAILED**

Message: User does not have the awa\_external\_user role.

This event indicates that the required role 'awa\_external\_user' or 'admin' is not present for the agent.

-   **AWA\_AGENT\_NOT\_AVAILABLE**

Message: Agent is not available to receive work.

This event indicates that the agent selected is unavailable.

-   **AWA\_OFFER\_ASSIGNMENT\_PAYLOAD\_MISSING**

Message: Assignment payload is empty or undefined in the offerContext.

This event indicates that the payload is empty or undefined in the **offerContext** object.

-   **AWA\_OFFER\_QUEUEID\_MISSING**

Message: Transfer Source queue ID is missing in the offerContext.

This event indicates that the required transfer queue ID \(**transferContent.targetId**\) is missing from the **offerContext** object.

-   **AWA\_ASSIGNMENT\_OFFEREDON\_FUTURE**

Message: OfferedOn time is in future.

This event indicates that the value of the **assignment.offeredOn** property is a future date and invalid. The date must be present or earlier.

-   **AWA\_ASSIGNMENT\_OFFEREDON\_INVALID\_FORMAT**

Message: OfferedOn date format is invalid, Please send it in "Www, dd Mmm yyyy HH:mm:ss GMT" UTC format.

This event indicates that the value provided for the **offerContext.assignment.offeredOn** property is not in the proper time date format.

-   **AWA\_OFFER\_EXTERNALID\_MISSING**

Message: ExternalId is missing in the offerContext.

This event indicates that the required externalId property has not been provided for the offer. This value identifies the current active call on the associated external system.


</td></tr></tbody>
</table>The following code example shows how to set the active state context.

```
openFrameAPI.setICContext("activeCall", {
  "activeCall": [
    { 
      "nowRecordTable": "interaction",
      "nowRecordId": "12345675678903456",
      "externalId": "1234567890",
      "type": "call",
      "direction": "inbound",
      "currentParticipant": {
        "id": "participant1",
        "name": "John 1",
        "actor": "agent",
        "state": "connected",
        "connectedTime": "Fri, 12 Jul 2024 05:23:41 GMT",
        "callStartTime": "Fri, 12 Jul 2024 04:20:22 GMT",
        "muted": false,
        "held": true,
        "paused": true,
        "flagged": true,
        "recording": "in_progress",
        "capabilities": {
          "hold": false,
          "mute": true,
          "endCall": true,
          "startRecording": true,
          "pauseRecording": true,
          "stopRecording": true,
          "resumeRecording": true,
          "transfer": true,
          "mergeCall": true,
          "leaveAndTransfer": true,
          "dtmf": true,
          "flag": true
        }
      },
      "participants": [
        {
          "id": "customer1",
          "name": "Gilly 1",
          "actor": "customer",
          "address": "+18582359874",
          "ani": "+16193287356", 
          "dnis": "+18004346258",
          "state": "connected",
          "connectedTime": "Fri, 12 Jul 2024 00:23:41 GMT",
          "callStartTime": "Fri, 12 Jul 2024 20:55:04 GMT",
          "muted": false,
          "held": false,
          "heldAtTime": "Fri, 12 Jul 2024 20:55:04 GMT", 
          "capabilities": {
            "mute": true,
            "hold": true,
            "endCall": true
          }
        },
        {
          "id": "agent2",
          "name": "Ned",
          "actor": "agent",
          "address": "+3134787324",
          "ani": "+13134787324", 
          "dnis": "+14773286943",
          "state": "Ringing...",
          "requireWrapup": true,
          "requestACW": true,
          "connectedTime": "Fri, 12 Jul 2024 20:24:41 GMT",
          "callStartTime": "Fri, 12 Jul 2024 20:56:34 GMT",
          "muted": true,
          "held": true,
          "heldAtTime": "Fri, 12 Jul 2024 20:55:41 GMT",
          "capabilities": {
            "mute": true,
            "endCall": true,
            "hold": true 
          }
        }
      ]
    },
    {
      "nowRecordTable": "interaction",
      "nowRecordId": "12345yhedfh534576u5",
      "externalId": "1234567890",
      "type": "call",
      "direction": "inbound",
      "currentParticipant": {
        "id": "participant1",
        "name": "John 1",
        "actor": "agent",
        "state": "connected",
        "muted": true,
        "held": false,
        "recording": "in_progress",
        "paused": true,
        "flagged": true,
        "capabilities": {
          "hold": false,
          "mute": true,
          "endCall": true,
          "record": true,
          "startRecording": true,
          "stopRecording": true,
          "transfer": true,
          },
          "mergeCall": false,
          "dtmf": true,
          "flag": true
        }
      },
      "participants": [
        {
          "id": "customer1",
          "name": "Gilly 2",
          "actor": "customer",
          "address": "+123456789",
          "state": "connected",
          "connectedTime": "Wed, 04 Dec 2024 00:23:41 GMT",
          "muted": true,
          "held": false,
          "heldAtTime": "Fri, 12 Jul 2024 20:24:41 GMT”,
          "capabilities": {
            "mute": true,
            "hold": true,
            "endCall": true
          }
        },
        {
          "id": "agent2",
          "name": "Ned 2",
          "actor": "agent",
          "address": "+123456789",
          "state": "Ringing...",
          "connectedTime": "Fri, 12 Jul 2024 20:24:41 GMT",
          "muted": true,
          "held": true,
          "heldaAtTime": "Fri, 12 Jul 2024 20:24:41 GMT”,
          "capabilities": {
            "mute": true,
            "endCall": true,
            "hold": true
          }
        }
      ]
     }
    ]
  }
);

```

The following example shows how to set the idle state context.

```
openFrameAPI.setICContext("idleState", {
  "capability": {
    "outBoundCall": true,
    "logOut": true 
  },
  "enableState": {
    "outBoundCall": true,
    "logOut": true
  },
  "dialpadInfoMessage": {
    "label": "Info Message Label",
    "value": "Info Message Value"
  },
  "currentInboundId": "1234"
});
```

The following example shows how to set the search target list context.

```
openFrameAPI.setICContext("searchTargetList",
  {
    "searchTargetList": [
      {
        "nowRecordTable": "interaction",
        "nowRecordId": "1234",
        "externalId": "5678",
        "participantID": "participant1",
        "targets": [
          {
            "type": "agent",
            "transferSubtypes": [
              {
                "id": "consult",
                "label": "Consult"
              },
              {
                "id": "blind",
                "label": "Blind"
              }
            ],
            "payload": {
              "list": [
                {
                  "name": "John Jason",
                  "id": "agent1Id",
                  "hasStats": "true",
                  "presence": "away",
                  "moreInfo": [
                    {
                      "label": "Skill",
                      "value": "10sec"
                    }
                  ]
                }
              ]
            }
          },
          {
            "type": "queue",
            "transferSubtypes": [
              {
                "id": "consult",
                "label": "Consult"
              },
              {
                "id": "blind",
                "label": "Blind"
              }
            ],
            "payload": {
              "list": [
                {
                  "name": "Product Support Queue",
                  "id": "queue1Id",
                  "hasStats": "true",
                  "moreInfo": [
                    {
                      "label": "Skill",
                      "value": "10sec"
                    },
                    {
                      "label": "Queue Skill",
                      "value": "German"
                    }
                  ]
                },
                {
                  "name": "Billing Queue",
                  "id": "queue2Id",
                  "hasStats": "true",
                  "moreInfo": [
                    {
                      "label": "Skill",
                      "value": "10sec"
                    }
                  ]
                }
              ]
            }
          }
        ],
        "customPayload": {}
      }
    ],
    "customPayload": {}
  });
```

The following example suggests how to set callback context and related capabilities settings.

```
openFrameAPI.setICContext('activeCall', callbackContext);

var callbackContext = {
  "activeCall": [
    {
      "nowRecordTable": "Customer interaction",
      "nowRecordId": "12345yhedfh534576u5",
      "externalId": "1234567890",
      "type": "callback",
      "currentParticipant": {
        "id": "agent1",
        "capabilities": {
          "initiateCall": "true",
          "closeCallback": "true",
          "transfer": "true",
          "cancelCallbackTransferEligible": "false",
          "callbackTransferStatus": ""
        }
      },
      "callbackContext": {
        "customerName": "Fred Luddy",
        "callbackNumbers": [
          "8665551234"
        ],
        "callAttemptedByAgent": "true",
        "closeInEndTime": "Mon, 05 Dec 2024 09:25:08 GMT",
        "dialInEndTime": ""
      }
    }
  ]
}
```

The following example shows how to set resiliency call response details using the offerContext property.

```
// Set offerContext
openFrameAPI.setICContext('offerContext', offerContext);

var offerContext = {
  "offerContext": [
    {
      "nowRecordTable": "interaction",
      "type": "phone",
      "externalId": "1234567890",
      "externalSegmentId": "12345yhedfh534576u5",
      "queueId": "10111ad087063250df52fe66cebb3520",
      "creationTime": "19-12-2025 11:23:45",
      "requesterId": "4085018550",
      "assignment": {
        "offeredOn": "Fri, 19-12-2025  13:07:59",
        "timeout": "4000",
        "allowedToDecline": true,
        "enableAutoAssign": true
      },
      "displayContent": {
        "title": "Phone",
        "displayContent1": "Abel Tuter",
        "displayContent2": "Priority - 4-Low",
        "displayContent3": "category - Product Issue"
      }
    }
  ]
};
```

## openFrameAPI - setIcons\(Array icons\)

Defines icons in the OpenFrame header that are placed next to the close icon.

<table id="table_dg3_lny_kt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

icons

</td><td>

Array of objects

</td><td>

A list of icon configurations, where each icon configuration is an object with key values **imageURL**, **imageTitle**, and any other needed context.Maximum size: Icons can be a maximum of 16x16 pixels. Larger images are automatically adjusted to this maximum.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setIcons([{imageURL:'https://mydomian.com/image/mute.png',
imageTitle:'mute', id:101}, {imageURL:'https://mydomian.com/image/hold.png',
imageTitle:'hold', id:102}]);
```

## openFrameAPI - setPresenceIndicator\(presence\)

Sets the presence indicator to display agent availability in a workspace.

For more information on configuring OpenFrame, refer to [Create an OpenFrame configuration](https://www.servicenow.com/docs/access?context=t_CreateAnOpenFrameConfiguration&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)

<table id="table_o4l_p1c_jhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

state

</td><td>

String

</td><td>

Presence state of the agent.Default states:

 -   Available
-   Away
-   Offline

 You can also specify custom states.

</td></tr><tr><td>

color

</td><td>

String

</td><td>

Presence indicator color on workspace. Supported colors:

 -   red
-   orange
-   grey
-   green

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
openframeAPI.setPresenceIndicator('Available', 'green');
```

## openFrameAPI - setSize\(Number width, Number height\)

Sets the OpenFrame size.

|Name|Type|Description|
|----|----|-----------|
|width|Number|Should be greater than zero.|
|height|Number|Should be greater than zero.|

|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setSize(300, 370);
```

## openFrameAPI - setSubtitle\(String subTitle\)

Sets the OpenFrame subtitle.

|Name|Type|Description|
|----|----|-----------|
|subTitle|String|A string of 256 or fewer characters.|

|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setSubtitle('+18888888888');
```

## openFrameAPI - setTitle\(String title\)

Sets the OpenFrame title.

|Name|Type|Description|
|----|----|-----------|
|title|String|A string of 256 or fewer characters.|

|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setTitle('Incoming Call');
```

## openFrameAPI - setTitleIcon\(Object icon\)

Sets the OpenFrame's title icon.

<table id="table_w42_kky_kt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

icon

</td><td>

Object

</td><td>

Object of key value pairs. Keys include **imageURL**, **imageTitle**, and any other context needed.Maximum size: Icons can be a maximum of 16x16 pixels. Larger images are automatically adjusted to this maximum.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setTitleIcon({imageURL:'/my/image/path.png', imageTitle:'mute', id:101});
```

```
openFrameAPI.setTitleIcon({imageURL:'https://mydomian.com/image/path.png',
imageTitle:'mute', id:101});
```

## openFrameAPI - setWidth\(width\)

Sets the OpenFrame width.

|Name|Type|Description|
|----|----|-----------|
|Width|Number|Width in pixels|

|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.setWidth(100);
```

## openFrameAPI - show\(\)

Makes the OpenFrame visible in the TopFrame.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
openFrameAPI.show()
```

## openFrameAPI - subscribe\(openFrameAPIEVENT event, function eventCallback\)

Subscribes to a specified event.

<table id="table_znv_gvd_lt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

event

</td><td>

openFrameAPIEVENT

</td><td>

The event to subscribe to:-   interaction\_control\_action: Receives the interaction lifecycle event or calls control updates from OpenFrame and updates the UI accordingly. Call control update examples include call initiated, muted, held, ended, and transfer requests.
-   openframe\_agent\_off\_interaction: Indicates the presence of an agent on chat as off or available.
-   openframe\_awa\_agent\_presence: In Advanced Work Assignment \(AWA\), this event occurs when there's any change in the agent presence state. Computer Telephony Integration \(CTI\) developers can subscribe to this event to receive presence state changes.
-   openframe\_awa\_client\_offer: Occurs when an offer or transfer is made on a resiliency-related offer.
-   openframe\_awa\_workitem\_accepted: Occurs when a work item is accepted by an agent.
-   openframe\_awa\_workitem\_offered: Occurs when a work item is offered to an agent.
-   openframe\_awa\_workitem\_rejected: Occurs when a work item is rejected by an agent.
-   openframe\_before\_destroy: Occurs before the TopFrame is unloaded.
-   openframe\_collapse: Occurs when the collapse icon is selected on the OpenFrame header.
-   openframe\_communication: Application-specific and can be customized.
-   openframe\_communication\_failure: Occurs when communication to TopFrame fails.
-   openframe\_expand: Occurs when the expand icon is selected on the OpenFrame header.
-   openframe\_heart\_beat: Occurs when the user session is extended or logged out.
-   openframe\_header\_icon\_clicked: Deprecated. Use openframe\_icon\_clicked or openframe\_title\_icon\_clicked instead.
-   openframe\_hidden: Occurs when the OpenFrame is hidden.
-   openframe\_icon\_clicked: Occurs when any icon other than the close icon is selected on the OpenFrame footer. The callback receives the icon object as a parameter.
-   openframe\_shown: Occurs when the OpenFrame is shown.
-   openframe\_title\_icon\_clicked: Occurs when the title icon is selected on the OpenFrame. The callback receives the titleIcon object as a parameter.
-   openframe\_wrap\_up\_submitted: Occurs when the wrap up periods ends on the [wrap-up modeless dialog](https://www.servicenow.com/docs/access?context=interaction-wrapup-modeless-dialog&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US). The event is triggered only when the wrap up is external.

</td></tr><tr><td>

eventCallback

</td><td>

function

</td><td>

Function to call when the specified event occurs.

</td></tr></tbody>
</table><table id="table_a4v_gvd_lt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

results

</td><td>

Most event subscriptions have no return values. The event subscriptions that do return values are described in the following table entries.

</td></tr><tr><td>

openframe\_awa\_agent\_presence

</td><td>

In AWA, the **openframe\_awa\_agent\_presence** event returns the `presence` object:```
"presence":{
  "available": Boolean,
  "channels":[
    {
      "available": Boolean,
      "name": "String",
      "restrict_update": Boolean,
      "sys_id": "String"
    }
  ],
  "name": "String",
  "sys_id": "String"
}
```

**presence**: Information about an agent's current presence state and channel.

-   **presence.available**: Flag that indicates whether the agent is available.
-   **presence.channels**: List of objects that describe the available channels of communication with the agent.
    -   **presence.channels.available**: Flag that indicates whether the channel is available.
    -   **presence.channels.name**: Channel name, such as Chat or Phone.
    -   **presence.channels.restrict\_update**: Flag that indicates whether the user can restrict updates.
    -   **presence.channels.sys\_id**: Channel sys\_id.
-   **presence.name**: Name of the agent's presence state.
-   **presence.sys\_id**: Presence state sys\_id.

</td></tr><tr><td>

openframe\_awa\_workitem\_accepted and openframe\_awa\_workitem\_offered

</td><td>

In AWA, the **openframe\_awa\_workitem\_accepted** and **openframe\_awa\_workitem\_offered** events return the `workItem` object:```
"workItem": {
  "document": {
    "sys_id": "String",
    "table": "String"
  },
  "isAutoAccepted": Boolean,
  "isQueueTransferred": Boolean,
  "previousWorkItem": "String",
  "serviceChannel": {
    "name": "String",
    "sys_id": "String"
  },
  "size": Number,
  "sys_id": "String"
}
```

**workItem**: Information about the work item that is associated with the event.

-   **workItem.document**: List of documents associated with the work item task.
    -   **workItem.document.sys\_id**: Sys\_id of the document assigned to the work item task.
    -   **workItem.document.table**: Name of the document table assigned to the task.
-   **workItem.isAutoAccepted**: Flag that indicates whether the work item was automatically accepted by the system. Set to true if the work item was auto-accepted.
-   **workItem.isQueueTransferred**: Flag that indicates whether the work item is queue transferred. Set to true if the work item is queue transferred, false if it isn't. For more information on queue transfers, see [Transfer a chat to another queue](https://www.servicenow.com/docs/access?context=transfer-chat-queue&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   **workItem.previousWorkItem**: Sys\_id of the previous work item for the same document ID. For the non-transfer work items this value is empty.
-   **workItem.serviceChannel**: List of service channels associated with the work item task.
    -   **workItem.serviceChannel.name**: Name of the service channel, such as Chat or Phone.
    -   **workItem.serviceChannel.sys\_id**: Sys\_id of the service channel.
-   **workItem.size**: Agent's capacity used when this work item is assigned to the agent.
-   **workItem.sys\_id**: Sys\_id of the work item that was accepted or offered.

</td></tr><tr><td>

openframe\_awa\_workitem\_rejected

</td><td>

In AWA, the **openframe\_awa\_workitem\_rejected** event returns the `workItem` object:```
"workItem": {
  "document": {
    "sys_id": "String",
    "table": "String"
  },
  "isQueueTransferred": Boolean,
  "previousWorkItem": "String",
  "rejection": {
    "reason": "String",
    "sys_id": "String"
  },
  "serviceChannel": {
    "name": "String",
    "sys_id": "String"
  },
  "size": Number,
  "sys_id": "String"
}
```

**workItem**: Information about the work item that is associated with the event.

-   **workItem.document**: List of documents associated with the work item task.
    -   **workItem.document.sys\_id**: Sys\_id of the document assigned to the work item task.
    -   **workItem.document.table**: Name of the document table assigned to the task.
-   **workItem.isQueueTransferred**: Flag that indicates whether the work item is queue transferred. Set to true if the work item is queue transferred, false if it isn't. For more information on queue transfers, see [Transfer a chat to another queue](https://www.servicenow.com/docs/access?context=transfer-chat-queue&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   **workItem.previousWorkItem**: Sys\_id of the previous work item for the same document ID. For the non-transfer work items this value is empty.
-   **workItem.rejection**: List of reasons for the rejection of the work item.
    -   **workItem.rejection.reason**: Name of the reason for rejecting the work items.
    -   **workItem.rejection.sys\_id**: Sys\_id of the rejection reason.

Table: Reject Reasons \[awa\_reject\_reason\]

-   **workItem.serviceChannel**: List of service channels associated with the work item task.
    -   **workItem.serviceChannel.name**: Name of the service channel, such as Chat or Phone.
    -   **workItem.serviceChannel.sys\_id**: Sys\_id of the service channel.
-   **workItem.size**: Agent's capacity used when this work item is assigned to the agent.
-   **workItem.sys\_id**: Sys\_id of the work item that was accepted or offered.

</td></tr><tr><td>

openframe\_heart\_beat

</td><td>

The **openframe\_heart\_beat** event returns the following object:```
{
  "lastUiActivity": "String",
  "sessionLoggedIn": Boolean
}
```

-   **lastUiActivity**: Optional. Time stamp of last UI activity that extended the user session.
-   **sessionLoggedIn** Flag that indicates whether the user is logged in.
    -   true: User is logged in.
    -   false: User isn't logged in.

</td></tr><tr><td>

openframe\_wrap\_up\_submitted

</td><td>

The **openframe\_wrap\_up\_submitted** event returns the following object:```
{ 
  "wrapUp": {
    "external": Boolean,
    "externalSegmentId": "String", 
    "recordId": "String",
    "recordTable": "String",
    "wrapUpCode": "String",
    "wrapUpNotes": "String",
    "wrapUpSegmentId": "String"
  }
}
```

-   **external**: Flag that indicates whether the wrap up is handled internally by the ServiceNow instance or managed outside of the ServiceNow instance by some other call system.
    -   true: Wrap up is handled by an external call system.
    -   false: Wrap up is handled by the ServiceNow instance.
-   **externalSegmentId**: Unique identifier of the external data object that triggered the external wrap up.
-   **recordId**: Sys\_id of the interaction record that is undergoing wrap up.
-   **recordTable**: Name of the table containing the record. Always set as “interaction".
-   **wrapUpCode**: Code selected by the user during the wrap up that indicates how the interaction was resolved.
-   **wrapUpNotes**: Free-form text entered by the user during wrap up that describes how the interaction was resolved.
-   **wrapUpSegmentId**: Sys\_id of the interaction wrap up segment record associated with the interaction. Located in the Wrap Up Segment \[interaction\_wrap\_up\_segment\] table. Contains the wrap up data.

</td></tr></tbody>
</table>The following code example shows how to call this method for an `openframe_awa_agent_presence` event.

```
function handleIconClick(context) {
console.log("Icon was clicked", context);
}
openFrameAPI.subscribe(openFrameAPI.events.openframe_awa_agent_presence, handleIconClick);
```

Output:

```
// Sample presence object output
// openframe_awa_agent_presence event only

{
  "result":{
    "presence":{
      "name":"Available",
      "sys_id":"27f675e3739713004a905ee515f6a7c3",
      "available":true,
      "channels":[
        {
          "name":"Chat",
          "available":true,
          "sys_id":"36f675e4239713124a905fe515f6a832",
          "restrict_update":false
        },
        {
          "name":"Phone",
          "available":true,
          "sys_id":"9378a530a1820610f809018efd9bc01e",
          "restrict_update":false
        }
      ]
    }
  }
}
```

The following code example shows how to call this method for an `openframe_awa_workitem_accepted` event.

```
function handleIconClick(context) {
console.log("Icon was clicked", context);
}
openFrameAPI.subscribe(openFrameAPI.events.openframe_awa_workitem_accepted, handleIconClick);
```

Output:

```
// Sample workItem object output
// openframe_awa_workitem_accepted event only
{
  "result": {
    "workItem": {
      "sys_id": "14c86c40a1650610f87701807d9bc0be",
      "size": 1,
      "serviceChannel": {
        "name": "Chat",
        "sys_id": "27f675e3739713004a905ee515f6a7c3"
      },
      "document": {
        "sys_id": "aa582040a1650610f87701807d9bc076",
        "table": "interaction"
      },
      "previousWorkItem": "7c78a440a1650610f87701807d9bc02b",
      "isQueueTransferred": true,
      "isAutoAccepted": true
    }
  }
}
```

The following code example shows how to call this method for an `openframe_awa_workitem_rejected` event.

```
function handleIconClick(context) {
console.log("Icon was clicked", context);
}
openFrameAPI.subscribe(openFrameAPI.events.openframe_awa_workitem_rejected, handleIconClick);
```

Output:

```
// Sample workItem object output
// openframe_awa_workitem_rejected event only
{
  "payload": {
    "workItem": {
      "sys_id": "2c3bdc4824250610f8775e73b116f8de",
      "size": "1",
      "serviceChannel": {
        "name": "Chat",
        "sysID": "27f675e3739713004a905ee515f6a7c3"
      },
      "document": {
        "sys_id": "cf0a180824250610f8775e73b116f80c",
        "table": "interaction"
      },
      "rejection": {
        "reason": "Busy",
        "sys_id": "4e93fa29b38023002e7b6e5f26a8dc20"
      },
      "previousWorkItem": "831b9c4824250610f8775e73b116f841",
      "isQueueTransferred": true
    }
  }
}
```

The following example shows how to subscribe to the **interaction\_control\_action** event.

```
openFrameAPI.subscribe("interaction_control_action", function(action) {
    // Can perform the action based on the name
    if (action.name == "mute") {
        mute();
        openFrameAPI.setICContext("activeCall", context); // Update context representing the change
    } else if (action.name == "getSearchTarget") {
        action.payload.searchType == "queue" ? fetchQueueTransferList(action.payload.searchTerm) : fetchAgentTransferList(action.payload.searchTerm);
        openFrameAPI.setICContext("searchTargetList", context); // Call context will have the transfer list
    } else if (action.name == "logout") {
        logout();
        openFrameAPI.showIframe(); // Show iframe api
    }
});
```

## openFrameAPI - toastMessage\(String message, String type, Number duration\)

Displays an alert message.

<table id="table_mqv_lqt_tgc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

String

</td><td>

Message to display in the alert.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Type of message. Possible values:

-   info
-   warning
-   error

</td></tr><tr><td>

duration

</td><td>

Number

</td><td>

Optional. Duration to display the message before it is auto-dismissed.Units: Milliseconds

Default: The message is displayed until it is manually closed.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example displays info, warning, and error messages.

```
openFrameAPI.toastMessage("Testing info message", "info", 10000); //display for 10 seconds
openFrameAPI.toastMessage("Testing warning message", "warning"); //display until manually closed
openFrameAPI.toastMessage("Testing error message", "error");
```

## openFrameAPI - version\(\)

Returns the OpenFrame API version.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The OpenFrame API version|

```
var version = openFrameAPI.version();

console.log("API version " + version);
```

