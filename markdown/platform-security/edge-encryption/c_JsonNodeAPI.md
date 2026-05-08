---
title: JsonNode
description: A global object that provides methods to iterate over the JSON content.Returns a JsonNodeIterator object for the JSON content.Returns a JsonNodeIterator object that iterates over all child nodes of the current node.Returns the current node value as a string.Returns the string value of the specified property.Returns the name of the current JSON node.Specifies that the JSON property maps to the specified field in the specified table.Specifies that the value of the JSON property is an encoded query for the specified table.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [JSON APIs, Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# JsonNode

A global object that provides methods to iterate over the JSON content.

You can access a JsonNode object by calling [getAsJsonContent\(\)](c_requestAPI.md#) on a request object.

You access JSON content from a [POST or URL parameter](param-apis.md#) by calling `request.postParms.<parameter name>.getAsJsonContent()` or `request.urlParms.<parameter name>.getAsJsonContent()`.

**Parent Topic:**[JSON APIs](json-overview.md)

## JsonNode - getIterator\(String xPath\)

Returns a JsonNodeIterator object for the JSON content.

This method can only be used on the root node, but can be used to traverse deep into the JSON object. Subsequent traversals must use the iterator\(\) method.

|Name|Type|Description|
|----|----|-----------|
|xPath|String|An xPath expression.|

|Type|Description|
|----|-----------|
|JsonNodeIterator|An object that can iterate over nodes in the JSON object.|

## JsonNode - iterator\(\)

Returns a JsonNodeIterator object that iterates over all child nodes of the current node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JsonNodeIterator|An object that can iterate over nodes in the JSON object.|

## JsonNode - getAsString\(\)

Returns the current node value as a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The current node value.|

## JsonNode - getAsString\(String propertyName\)

Returns the string value of the specified property.

|Name|Type|Description|
|----|----|-----------|
|propertyName|String|Name of the property.|

|Type|Description|
|----|-----------|
|String|The property value.|

## JsonNode - getName\(\)

Returns the name of the current JSON node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the current JSON node.|

## JsonNode - valueFor\(String tableName, String fieldName\)

Specifies that the JSON property maps to the specified field in the specified table.

Calling this method on a JSON property tells the proxy that the value for this property maps to the specified field in the specified table. The proxy then decides if the field must be encrypted. If the table and field names are unknown, you can call the valueFor\(\) method on a table and a field that are [dynamically assigned](json-overview.md#json-dynamic) based on the request.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table name.|
|fieldName|String|The field name.|

|Type|Description|
|----|-----------|
|void| |

## JsonNode - encodedQueryFor\(String tableName\)

Specifies that the value of the JSON property is an encoded query for the specified table.

Calling this function on a JSON node tells the proxy that the value is an Encoded query strings for the specified table. The proxy parses the encoded query and encrypts the values for fields in the encoded query that must be encrypted.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table that you expect the query to run on.|

|Type|Description|
|----|-----------|
|void| |

