---
title: GlideTextReader - Scoped
description: The GlideTextReader API provides the ability to read single lines from an input stream. Because an input stream is used, it is not subject to the 5MB attachment size limit.Creates a scoped GlideTextReader object for the specified input stream.Returns the character encoding of the input stream.Returns a single line from the input stream and returns a string. Since this is working off of a stream, it is not subject to the 5MB size limit.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideTextReader- Scoped

The GlideTextReader API provides the ability to read single lines from an input stream. Because an input stream is used, it is not subject to the 5MB attachment size limit.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideTextReader - GlideTextReader\( GlideScriptableInputStream inputStream\)

Creates a scoped GlideTextReader object for the specified input stream.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The input stream to be read.|

## GlideTextReader - getEncoding\(\)

Returns the character encoding of the input stream.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The character encoding of the input stream.|

## GlideTextReader - readLine\(\)

Returns a single line from the input stream and returns a string. Since this is working off of a stream, it is not subject to the 5MB size limit.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A single line of input up to the carriage return. Does not include the carriage return. Returns null if there is no content.|

```
var is = new GlideSysAttachment().getContentStream(attachmentSysId);
var reader = new GlideTextReader(is);
var ln = ' ';
while((ln = reader.readLine()) != null) {
  gs.info(ln);
}
```

