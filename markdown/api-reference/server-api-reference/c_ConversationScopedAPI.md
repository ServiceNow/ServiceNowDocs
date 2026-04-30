---
title: Conversation - Scoped
description: The Conversation API enables you to create or modify Connect conversations.Adds a user to a conversation.Creates a Connect conversation.Returns an existing Connect conversation by sys\_id.Removes a user from a conversation.Sends a message to a conversation.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Conversation- Scoped

The Conversation API enables you to create or modify Connect conversations.

To use this class in a scoped application, use the `sn_connect` namespace identifier. The Connect Scriptable APIs plugin \(ID: com.glide.connect.scriptable\) should be enabled to access the Conversation API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Conversation - addSubscriber\(String sysID\)

Adds a user to a conversation.

|Name|Type|Description|
|----|----|-----------|
|sysID|String|Sys\_ID of the user you want to add to a conversation.|

|Type|Description|
|----|-----------|
|void| |

```
var conversation = sn_connect.Conversation.get("7caf49111309030034bb58a12244b06c");
conversation.addSubscriber("a8f98bb0eb32010045e1a5115206fe3a");
```

## Conversation - create\(String name\)

Creates a Connect conversation.

<table id="table_lwg_b4w_cbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Create a conversation with a specific name.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Include a specific conversation type. The type is determined by the type choice list. The base system includes the following type options: -   connect
-   support
-   group
-   peer
-   qanda
-   team

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Scriptable Conversation|

```
var conversation = sn_connect.Conversation.create({
    name: "Hello world",
    type: "connect"
});
```

## Conversation - get\(String sysID\)

Returns an existing Connect conversation by sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sysID|String|The sys\_id of the conversation record.|

|Type|Description|
|----|-----------|
|Object|Conversation object|

```
var conversation = sn_connect.Conversation.get("27b9844c1385030034bb58a12244b037");
```

## Conversation - removeSubscriber\(String sysID\)

Removes a user from a conversation.

|Name|Type|Description|
|----|----|-----------|
|SysID|String|The sys\_id of the user you want to remove from a conversation.|

|Type|Description|
|----|-----------|
|void| |

```
var conversation = sn_connect.Conversation.get("7caf49111309030034bb58a12244b06c");
conversation.removeSubscriber("a8f98bb0eb32010045e1a5115206fe3a");
```

## Conversation - sendMessage\(String body, String field\)

Sends a message to a conversation.

|Name|Type|Description|
|----|----|-----------|
|Body|String|The main text of the message.|
|Field|String|The field you want the message to appear as. Only use this option if adding a message to a record conversation. Choose from work\_notes, comments, or system. Using the field system treats the message as a system message.|

|Type|Description|
|----|-----------|
|void| |

```
var conversation = sn_connect.Conversation.get("2064fa3919010300964f5270e9840fbb");
conversation.sendMessage({body: "Hello world", field: "work_notes"});
```

