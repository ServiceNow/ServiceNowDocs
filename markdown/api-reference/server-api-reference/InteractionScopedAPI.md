---
title: Interaction - Scoped
description: The Interaction API provides methods that enable you to define the behavior for interaction records.Accepts a new interaction.Creates an interaction.Returns an interaction record.Transfers an interaction record to an agent using the sys\_id for the agent.Transfers an interaction record to an interaction queue.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Interaction- Scoped

The Interaction API provides methods that enable you to define the behavior for interaction records.

This class requires the Interaction Logging, Routing, and Queueing plugin \(com.glide.interaction\) and runs in the `sn_interaction` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Interaction - accept\(\)

Accepts a new interaction.

Accepting a transfer only works for pending transfers. Find any pending transfers in the Interaction Agent Transfer \[interaction\_agent\_transfer\] table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|Returns true if the transfer is accepted.|

```
var now_GR = new GlideRecord('interaction');
GR.get('b2c0a3af202a1300964f959e0488de75');
var interaction = sn_interaction.Interaction.getInteraction(GR).accept();
```

## Interaction - create\(Object options\)

Creates an interaction.

<table id="table_ubv_mql_d2b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

options

</td><td>

Object

</td><td>

Field values for an interaction record. The channel field with the channel sys\_id and channel metadata are required. If a queue is not included in the parameter, the system returns `Interaction b2c0a3af202a1300964f959e0488de75 has no queue specified... running queue matching rules.`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Interaction|

```
var interactionObj = sn_interaction.Interaction.create({
	channel: '28a59893873103002ae97e2526cb0b5d',
	channel_metadata:{},
	opened_for: '46d44a23a9fe19810012d100cca80666',
	queue: 'f3a50867b30303002186a72256a8dcb7'
});
```

## Interaction - getInteraction\(GlideRecord interaction\)

Returns an interaction record.

|Name|Type|Description|
|----|----|-----------|
|interaction|GlideRecord|Interaction record from the interaction table \[interaction\] that is retrieved from the system.|

|Type|Description|
|----|-----------|
|Object|Interaction|

```
var now_GR = new GlideRecord('interaction');
now_GR.get('608a21bd096a9300964ffbd57ba7dd8d');
var interaction = sn_interaction.Interaction.getInteraction(now_GR);
```

## Interaction - transferToAgent\(String sysID\)

Transfers an interaction record to an agent using the sys\_id for the agent.

When an interaction is transferred from one agent to another, the interaction needs to be accepted or rejected using GlideRecord APIs. Use the GlideRecord API to change the state of the interaction and update. For more information, see the GlideRecord - update method.

**Note:** This method has been deprecated.

|Name|Type|Description|
|----|----|-----------|
|SysID|String|The sys\_id of the user you want to transfer an interaction record to.|

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord('interaction');
GR.get('24b927ef202a1300964f959e0488de2d');
var interaction = sn_interaction.Interaction.getInteraction(GR);
interaction.transferToAgent('6816f79cc0a8016401c5a33be04be441');
```

## Interaction - transferToQueue\(String sysID\)

Transfers an interaction record to an interaction queue.

Transferring an interaction from one queue to another closes the original interaction and creates an interaction in the new queue.

**Note:** This method has been deprecated.

|Name|Type|Description|
|----|----|-----------|
|SysID|String|The sys\_id of the interaction queue you want to transfer the interaction record to.|

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord('interaction');
GR.get('24b927ef202a1300964f959e0488de2d');
var interaction = sn_interaction.Interaction.getInteraction(GR);
interaction.transferToQueue('86fee1933b101300088d832b44efc474');
```

