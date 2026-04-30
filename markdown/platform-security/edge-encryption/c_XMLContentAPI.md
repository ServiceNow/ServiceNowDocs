---
title: XMLContent
description: A global object that provides methods to iterate over the XML content.Returns an XMLElementIterator object for the XML content.Returns an XMLElementIterator object for the XML content based on the specified parameter.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [XML APIs, Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# XMLContent

A global object that provides methods to iterate over the XML content.

You can access an XMLContent object by calling [getAsXmlContent\(\)](c_requestAPI.md#) on a request object.

You access XML data in a [POST or URL parameter](param-apis.md#) by calling `request.postParams.<parameter name>.getAsXmlContent()` or `request.urlParams.<parameter name>.getAsXmlContent()`.

**Parent Topic:**[XML APIs](xml-overview.md)

## XMLContent - getIterator\(\)

Returns an XMLElementIterator object for the XML content.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLElementIterator|An object that can be used to iterate over elements in the XMLContent object.|

## XMLContent - getIterator\(String xPath\)

Returns an XMLElementIterator object for the XML content based on the specified parameter.

|Name|Type|Description|
|----|----|-----------|
|xPath|String|An xPath-like expression that specifies where in the XMLContent object to start.|

|Type|Description|
|----|-----------|
|XMLElementIterator|An object that can be used to iterate over elements in the XMLContent object.|

