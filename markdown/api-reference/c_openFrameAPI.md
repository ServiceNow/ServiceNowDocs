---
title: openFrameAPI - Client
description: The openFrameAPI provides methods that interact with OpenFrame. OpenFrame is an omni-present frame that communication partners can use to integrate their systems into the ServiceNow platform.Returns the logged in agent’s current presence state.Hides the OpenFrame in the TopFrame.Initializes OpenFrame. This must be the first method that you call.Checks to see if the OpenFrame is visible in the TopFrame.Opens a custom URL in the UI16 interface.Opens a form URL.Opens a ServiceNow form with a child tab if invoked in a workspace or opens an entity if invoked in the UI16 interface.Opens a list URL in the UI16 interface.Sets the OpenFrame mode.Sets the OpenFrame height.Defines icons in the OpenFrame header that are placed next to the close icon.Sets the presence indicator to display agent availability in a workspace.Sets the OpenFrame size.Sets the OpenFrame subtitle.Sets the OpenFrame title.Sets the OpenFrame's title icon.Sets the OpenFrame width.Makes the OpenFrame visible in the TopFrame.Subscribes to a specified event.Returns the OpenFrame API version.
locale: en-US
release: xanadu
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 13
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# openFrameAPI- Client

The openFrameAPI provides methods that interact with OpenFrame. OpenFrame is an omni-present frame that communication partners can use to integrate their systems into the ServiceNow platform.

One of the core requirements is the ability to connect and serve code from different domains that can connect seamlessly with partner subsystems. This cross domain connection is required to keep connections and callbacks registered into communication systems without any cross domain issues.

OpenFrame has two significant parts: one that lives in the ServiceNow application \(referred to as TopFrame\) and this API that is sourced from the partner application. This API has the necessary methods to communicate with TopFrame and control the visual features of the OpenFrame.

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

Sys\_id of the channel record. Located in the Service Channels \[awa\_service\_channel\] table.Data type: String

</td></tr><tr><td>

presence.name

</td><td>

Name of the agent's presence state.Data type: String

</td></tr><tr><td>

presence.sys\_id

</td><td>

Sys\_id of the presence state record. Located in the Presence States \[awa\_presence\_state\] table.Data type: String

</td></tr></tbody>
</table>The following code exapmle shows how to call this method.

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

Name of the callback function to use if the init method succeeds. The [OpenFrame configuration](https://www.servicenow.com/docs/access?context=t_CreateAnOpenFrameConfiguration&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) stored in the system is passed as a parameter to the callback function.

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
-   query: [Encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

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

For more information on configuring OpenFrame, refer to [Create an OpenFrame configuration](https://www.servicenow.com/docs/access?context=t_CreateAnOpenFrameConfiguration&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

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

The event to subscribe to:-   openframe\_agent\_off\_interaction: Indicates the presence of an agent on chat as off or available.
-   openframe\_awa\_agent\_presence: In Advanced Work Assignment \(AWA\), this event occurs when there's any change in the agent presence state. Computer Telephony Integration \(CTI\) developers can subscribe to this event to receive presence state changes.
-   openframe\_awa\_workitem\_accepted: Occurs when a work item is accepted by an agent.
-   openframe\_awa\_workitem\_offered: Occurs when a work item is offered to an agent.
-   openframe\_awa\_workitem\_rejected: Occurs when a work item is rejected by an agent.
-   openframe\_before\_destroy: Occurs before the TopFrame is unloaded.
-   openframe\_collapse: Occurs when the collapse icon is selected on the OpenFrame header.
-   openframe\_communication: Application-specific and can be customized.
-   openframe\_communication\_failure: Occurs when communication to TopFrame fails.
-   openframe\_expand: Occurs when the expand icon is selected on the OpenFrame header.
-   openframe\_header\_icon\_clicked: Deprecated. Use openframe\_icon\_clicked or openframe\_title\_icon\_clicked instead.
-   openframe\_hidden: Occurs when the OpenFrame is hidden.
-   openframe\_icon\_clicked: Occurs when any icon other than the close icon is selected on the OpenFrame footer. The callback receives the icon object as a parameter.
-   openframe\_shown: Occurs when the OpenFrame is shown.
-   openframe\_title\_icon\_clicked: Occurs when the title icon is selected on the OpenFrame. The callback receives the titleIcon object as a parameter.

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
-   **workItem.isQueueTransferred**: Flag that indicates whether the work item is queue transferred. Set to true if the work item is queue transferred, false if it isn't. For more information on queue transfers, see [Transfer a chat to another queue](https://www.servicenow.com/docs/access?context=transfer-chat-queue&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
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
-   **workItem.isQueueTransferred**: Flag that indicates whether the work item is queue transferred. Set to true if the work item is queue transferred, false if it isn't. For more information on queue transfers, see [Transfer a chat to another queue](https://www.servicenow.com/docs/access?context=transfer-chat-queue&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
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

