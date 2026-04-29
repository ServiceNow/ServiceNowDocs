---
title: Agent - Global
description: The Agent API provides methods for getting or setting agent presence and channel availability.Gets an agent by sys\_id.Gets the current presence state and channel availability of a provided agent.Sets the state of a provided agent's presence and sets the agent's channel availability for that state.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Agent- Global

The Agent API provides methods for getting or setting agent presence and channel availability.

The Agent API is provided within the `sn_awa` namespace.

Requires the following:

-   Advanced Work Assignment plugin \(com.glide.awa\)
-   Role: awa\_integration\_user or admin

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Agent - get\(String user\_sys\_id\)

Gets an agent by sys\_id.

|Name|Type|Description|
|----|----|-----------|
|user\_sys\_id|String|The sys\_id of the user listed in sys\_user table.|

|Type|Description|
|----|-----------|
|Boolean|True if the user exists, false otherwise.|

```
var agent = sn_awa.Agent.get("<user_sys_id>");
var presence  = agent.getPresence();
```

## Agent – getPresence\(\)

Gets the current presence state and channel availability of a provided agent.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Presence state sys\_id, presence state name, and channel information. Error message otherwise.|

```
var agent = sn_awa.Agent.get("<user_sys_id>");
        var presence  = agent.getPresence();
```

## Agent – setPresence\(Object setRequest\)

Sets the state of a provided agent's presence and sets the agent's channel availability for that state.

<table id="table_hqw_pbm_yfb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

setRequest

</td><td>

Object

</td><td>

The setRequest.sys\_id and setRequest.channels.

</td></tr><tr><td>

setRequest.sys\_id

</td><td>

String

</td><td>

The presence\_sys\_id from the AWA Presence State \[awa\_presence\_state\] table.

</td></tr><tr><td>

setRequest.channels

</td><td>

name/value pair

</td><td>

Optional.-   sys\_id: Channel\_sys\_id from the awa\_service\_channel table.
-   available: Agent availability to receive work for this channel \(true or false\).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Boolean|True if successful, false otherwise.|

```
var agent = sn_awa.Agent.get("<user_sys_id>");
var presence = agent.setPresence({
    sys_id: <presence_sys_id>,
    channels: [{
        sys_id: "<channel_sys_id>",
        available: true // or false
    }]
});
```

