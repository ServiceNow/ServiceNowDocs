---
title: GlideConversation - Global
description: The GlideConversation API provides methods to access information in a Connect message.The conversation's description.The sysID of the document associated with the conversation.The name of the conversation.The queue entry associated with the conversation.The sys\_id of the conversation.The name of the table containing the record being discussed.The conversation type.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideConversation- Global

The GlideConversation API provides methods to access information in a Connect message.

**Important:**

Starting with the Paris release, Connect Support no longer receives enhancements or non-priority bug fixes. Consider moving to ServiceNow® Advanced Work Assignment and Agent Chat in workspace to automatically assign chat requests and other work items to agents. For details, see Move from Connect Support to Advanced Work Assignment and Agent Chat.

Access GlideConversation properties through a global object \(conversation\) that is available only in Connect action conditions and scripts.

Connect conversations are stored on the Live Group Profile \[live\_group\_profile\] table.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideConversation - description

The conversation's description.

|Name|Type|Description|
|----|----|-----------|
|description|String|The conversation's description.|

```
var c= conversation.description;
```

## GlideConversation - document

The sysID of the document associated with the conversation.

This field is set for feed conversations, and contains the sysID of the record being discussed.

|Name|Type|Description|
|----|----|-----------|
|document|GlideRecord|The document associated with the conversation.|

## GlideConversation - name

The name of the conversation.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the conversation.|

```
var c= conversation.name;
```

## GlideConversation - queueEntry

The queue entry associated with the conversation.

The queue entry is a reference field pointing to the chat\_queue\_entry table. This field is only available on support conversations. The queue chat entry is used to track the state of the conversation. This property is not changed if an incident record is created from the support conversation using the newRecord\(\) method.

|Name|Type|Description|
|----|----|-----------|
|queueEntry|GlideRecord|The queue entry associated with the conversation.|

```
var c= conversation.queueEntry;
```

## GlideConversation - sys\_id

The sys\_id of the conversation.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|The sys\_id of the conversation.|

```
var c= conversation.sys_id;
```

## GlideConversation - table

The name of the table containing the record being discussed.

This field is set for feed conversations, and is set to the table holding the record.

|Name|Type|Description|
|----|----|-----------|
|table|String|The name of the table holding the record being discussed.|

```
var c= conversation.table;
```

## GlideConversation - type

The conversation type.

This is not the message type.

Connect supports the following types.

-   peer - direct conversations, which consist of messages between two users.
-   connect - group conversations, which consist of messages between more than two users.
-   support - Connect Support conversations.
-   feed - record conversations, which consist of messages that correspond to comments and work notes on a specific record.

|Name|Type|Description|
|----|----|-----------|
|type|String|The conversation type.|

```
var c= conversation.type;
```

