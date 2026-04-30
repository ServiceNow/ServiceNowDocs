---
title: XMLNode - Scoped, Global
description: The XMLNode API provides methods to query values from XML nodes. XMLNodes are extracted from XMLDocument2 objects, which contain XML strings.Gets the value of the attribute.Returns an object containing the node's attributes as properties with values.Gets a XMLNodeIterator object that can be used to walk through the list of child nodes.Gets the node's first child node.Gets the node's last child node.Gets the node's name. A node's name is determined by the node type. A document-element node's name is \#document. A text node's name is \#text. An element node's name is the element's name.Gets the node's value. A node's value is determined by the node type. Element and document-element nodes return null.Gets the text content of the current node. The text content of a node consists of all the node's child text nodesDetermines if the node has the specified attribute.Indicates whether the CDATA node is preserved as a separate node.Returns the string value of the current node.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# XMLNode - Scoped, Global

The XMLNode API provides methods to query values from XML nodes. XMLNodes are extracted from XMLDocument2 objects, which contain XML strings.

There are no constructors for creating a stand alone instance of an XMLNode object. Instead, use the createElement\(\) method of [XMLDocument2](../../XMLDocument2ScopedAPI/concept/c_XMLDocument2ScopedAPI.md#), which adds a node to an existing document.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped XMLNode - getAttribute\(String attribute\)

Gets the value of the attribute.

|Name|Type|Description|
|----|----|-----------|
|attribute|String|Name of the attribute.|

|Type|Description|
|----|-----------|
|String|The attribute's value.|

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//two');
gs.info(node.getAttribute('att'));
```

Output:

```
xxx
```

## Scoped XMLNode - getAttributes\(\)

Returns an object containing the node's attributes as properties with values.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Contains name-value pairs where the name is the attribute and the value is the attribute's value.|

## Scoped XMLNode - getChildNodeIterator\(\)

Gets a XMLNodeIterator object that can be used to walk through the list of child nodes.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLNodeIterator|The node iterator object.|

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//one');
var iter= node.getChildNodeIterator();
gs.info(iter.hasNext());
```

## Scoped XMLNode - getFirstChild\(\)

Gets the node's first child node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLNode|The node's first child node.|

```
var xmlString = "<test>" +
                "<one>" +
                "<two att=\"xxx\">abcd1234</two>" +
                "<three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "<two>another</two>" +
                "</one>" +
                "<number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//one');
gs.info(node.getFirstChild());
```

Output:

```
<two att="xxx">abcd1234</two>
```

## Scoped XMLNode - getLastChild\(\)

Gets the node's last child node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLNode|The node's last child.|

```
var xmlString = "<test>" +
                "<one>" +
                "<two att=\"xxx\">abcd1234</two>" +
                "<three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "<two>another</two>" +
                "</one>" +
                "<number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//one');
 
gs.info(node.getLastChild());
```

Output:

```
<two>another</two>
```

## Scoped XMLNode - getNodeName\(\)

Gets the node's name. A node's name is determined by the node type. A document-element node's name is \#document. A text node's name is \#text. An element node's name is the element's name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The node's name.|

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//two');
gs.info(node.getNodeName());
```

Output:

```
two
```

## Scoped XMLNode - getNodeValue\(\)

Gets the node's value. A node's value is determined by the node type. Element and document-element nodes return null.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The node's value.|

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//two');
gs.info(node.getNodeValue());
```

Output:

```
null
```

## Scoped XMLNode - getTextContent\(\)

Gets the text content of the current node. The text content of a node consists of all the node's child text nodes

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The text content of the current node.|

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";
var xmldoc = new XMLDocument2();
xmldoc.parseXML(xmlString);
var node = xmldoc.getNode('//one/two');
gs.info(node.getTextContent());
```

Output:

```
abcd1234
```

## Scoped XMLNode - hasAttribute\(String attribute\)

Determines if the node has the specified attribute.

|Name|Type|Description|
|----|----|-----------|
|attribute|String|The name of the attribute to check.|

|Type|Description|
|----|-----------|
|Boolean|True if the node has the attribute.|

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//two');
gs.info(node.hasAttribute('att'));
```

Output:

```
true
```

## Scoped XMLNode - isCDATANode\(\)

Indicates whether the CDATA node is preserved as a separate node.

Use the [Scoped XMLDocument2 - setEnableCDATAReporting\(Boolean enable\)](../../XMLDocument2ScopedAPI/concept/c_XMLDocument2ScopedAPI.md#) method to ensure that CDATA nodes are preserved and not handled as text.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ck3_rjy_3x" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether a queried node is CDATA or plain text.Valid values:

-   true: The node queried is CDATA.
-   false: The node queried is plain text.

</td></tr></tbody>
</table>The following example shows how to parse an XML string with CDATA reporting enabled using [Scoped XMLDocument2 - setEnableCDATAReporting\(Boolean enable\)](../../XMLDocument2ScopedAPI/concept/c_XMLDocument2ScopedAPI.md#). The code uses isCDATANode\(\) to show that the first node queried in the XML string is a CDATA node.

```
var xmlString = "<test>" +
  "  <one>" +
  "    <two att=\"xxx\">abcd1234</two>" +
  "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>"+
  "    <four><![CDATA[another]]>element</four>" +
  "  </one>" +
  "  <number>1234</number>" +
  "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.setEnableCDATAReporting(true); // Enables CDATA reporting
xmlDoc.parseXML(xmlString);
var content = xmlDoc.getFirstNode('/test/one/four');
gs.info(content.getFirstChild().isCDATANode());
```

Output:

```
true
```

## Scoped XMLNode - toString\(\)

Returns the string value of the current node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The string value of the current node.|

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.parseXML(xmlString);
var node = xmlDoc.getNode('//one');
gs.info(node.toString());
```

Output: Line breaks were added to the output.

```
<one>    
<two att="xxx">abcd1234</two>    
<three att="yyy" boo="yah">1234abcd</three>    
<two>another</two>  
</one>
```

