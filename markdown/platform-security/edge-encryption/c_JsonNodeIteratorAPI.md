---
title: JsonNodeIterator
description: You get a JsonNodeIterator object by calling the getIterator\(\) or iterator\(\) methods of the JsonNode class.Determines if there is another property available.Returns the next property in the iterator.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [JSON APIs, Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# JsonNodeIterator

You get a JsonNodeIterator object by calling the getIterator\(\) or iterator\(\) methods of the JsonNode class.

**Parent Topic:**[JSON APIs](json-overview.md)

## JsonNodeIterator - hasNext\(\)

Determines if there is another property available.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if another property is available.|

## JsonNodeIterator - next\(\)

Returns the next property in the iterator.

You cannot call next\(\) without first calling hasNext\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JsonNode|The next JsonNode.|

