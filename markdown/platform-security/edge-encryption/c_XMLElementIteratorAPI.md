---
title: XMLElementIterator
description: Provides methods for iterating over XML elements.Determines if there is another element available.Returns the next element in the iterator.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [XML APIs, Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# XMLElementIterator

Provides methods for iterating over XML elements.

You get an XMLElementIterator object by calling the getIterator\(\) method of the XMLContent class.

**Parent Topic:**[XML APIs](xml-overview.md)

## XMLElementIterator - hasNext\(\)

Determines if there is another element available.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if another element is available.|

## XMLElementIterator - next\(\)

Returns the next element in the iterator.

You cannot call next\(\) without first calling hasNext\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLElement|The next XML element.|

