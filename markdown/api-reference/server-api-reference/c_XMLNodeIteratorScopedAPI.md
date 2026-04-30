---
title: XMLNodeIterator - Scoped
description: The XMLNodeIterator API provides methods to iterate through a node of a XML document.Returns true if the iteration has more elements.Gets the next element in the iteration. The returned element may be a \#text node for the spaces/tabs if XML is "pretty formatted".
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# XMLNodeIterator- Scoped

The XMLNodeIterator API provides methods to iterate through a node of a XML document.

There are no constructors for creating a stand alone instance of a XMLNodeIterator object. To create a XMLNodeIterator object use the getChildNodeIterator\(\) method of the [XMLNode object](../../XMLNodeScopedAPI/concept/c_XMLNodeScopedAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## XMLNodeIterator - hasNext\(\)

Returns true if the iteration has more elements.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the iteration has more elements.|

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

## XMLNodeIterator - next\(\)

Gets the next element in the iteration. The returned element may be a \#text node for the spaces/tabs if XML is "pretty formatted".

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLNode|The next element in the iteration.|

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
while(iter.hasNext()) {
   var n = iter.next();
   gs.info('Node name: ' +  n.getNodeName());
   gs.info('Node value: ' +  n.getNodeValue());
}
```

Output:

```
Node name: #text
Node value:     
Node name: two
Node value: null
Node name: #text
Node value:     
Node name: three
Node value: null
Node name: #text
Node value:     
Node name: two
Node value: null
Node name: #text
Node value:
```

