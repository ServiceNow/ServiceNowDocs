---
title: i18N - Client
description: The i18N API provides methods to get and format translated messages.Formats a string containing named tokens with values from a map.Retrieves a translated message.Retrieves a set of messages.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# i18N- Client

The i18N API provides methods to get and format translated messages.

The i18N methods are accessed using the `g_i18n` global object.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## i18N - format\(String message, Object map\)

Formats a string containing named tokens with values from a map.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to have the tokens added.|
|map|Object|The map of name/value pairs to replace in the message.|

|Type|Description|
|----|-----------|
|String|The formatted string|

```
// Returns: "The rich young ruler was very very rich"
nowapi.g_i18n.format("The {p1} {p2} {p3} was very very {p1}",{p1: "rich", p2: "young", p3: "ruler"});
```

## i18N - getMessage\(String msgKey, Function callback\)

Retrieves a translated message.

If the specified string exists in the database for the current language, then the translated message is returned. If the specified string does not exist for the current language, then the English version of the string is returned. If the string does not exist at all in the database, then the ID itself is returned.

|Name|Type|Description|
|----|----|-----------|
|msgKey|String|The message to be retrieved.|
|callback|Function|The function to be called when the message has been retrieved. The callback function has one argument, a string that is the translated message.|

|Type|Description|
|----|-----------|
|void| |

## i18N - getMessages\(Array msgKeys, Function callback\)

Retrieves a set of messages.

If the specified string exists in the database for the current language, then the translated message is returned. If the specified string does not exist for the current language, then the English version of the string is returned. If the string does not exist at all in the database, then the ID itself is returned.

|Name|Type|Description|
|----|----|-----------|
|msgKeys|Array|An array of keys specifying the messages to be retrieved.|
|callback|Function|The function to be called when the messages have been retrieved. The callback function has one argument, an object containing key-value pairs, where key is the requested message key, and the value is the translated string.|

|Type|Description|
|----|-----------|
|void| |

