---
title: XMLElement
description: Provides methods for iterating through XML elements and mapping values to fields in a table.Returns an XMLElementIterator object for the XML element based on the specified parameter.Returns an XMLElementIterator object that includes all sub-elements for the XML element based on the specified parameter.Specifies that the value of the element maps to the specified field in the specified table.Specifies that the value of the element is an encoded query for the specified table.Returns the element name.Returns the value of the specified attribute.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [XML APIs, Encryption rule objects and APIs, Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# XMLElement

Provides methods for iterating through XML elements and mapping values to fields in a table.

You get an XMLElement object by calling the next\(\) method of an XMLElementIterator object.

**Parent Topic:**[XML APIs](xml-overview.md)

## XMLElement - getIterator\(String xPath\)

Returns an XMLElementIterator object for the XML element based on the specified parameter.

|Name|Type|Description|
|----|----|-----------|
|xPath|String|An xPath-like expression that specifies where in the XMLElement object to start.|

|Type|Description|
|----|-----------|
|XMLElementIterator|An object that can be used to iterate over elements in the XMLElement object.|

## XMLElement - getIteratorOverAllChildren\(\)

Returns an XMLElementIterator object that includes all sub-elements for the XML element based on the specified parameter.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLElementIterator|An object that can be used to iterate over elements in the XMLElement object.|

## XMLElement - valueFor\(String tableName, String fieldName\)

Specifies that the value of the element maps to the specified field in the specified table.

Calling this method on an element value tells the proxy that the value for this element maps to the specified field in the specified table. The proxy then checks if the field must be encrypted. If the table and field names are unknown, you can call the valueFor\(\) method on a table and a field that are [dynamically assigned](xml-overview.md#xml-dynamic) based on the request.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table name.|
|fieldName|String|The field name.|

|Type|Description|
|----|-----------|
|void| |

## XMLElement - encodedQueryFor\(String tableName\)

Specifies that the value of the element is an encoded query for the specified table.

Calling this function on an element tells the proxy that the value of the element is an [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for the specified table. The proxy parses the encoded query and encrypts the fields in the encoded query that must be encrypted.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table that you expect the query to run on.|

|Type|Description|
|----|-----------|
|void| |

## XMLElement - getName\(\)

Returns the element name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The element name.|

## XMLElement - getAttributeValue\(String attribute\)

Returns the value of the specified attribute.

|Name|Type|Description|
|----|----|-----------|
|attribute|String|Attribute name.|

|Type|Description|
|----|-----------|
|String|The attribute value.|

