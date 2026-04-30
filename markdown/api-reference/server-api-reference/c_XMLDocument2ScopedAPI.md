---
title: XMLDocument2 - Scoped, Global
description: The XMLDocument2 API is a JavaScript object wrapper for parsing and extracting XML data from an XML string.Creates an XMLDocument2 object.Creates an XMLDocument2 object from an attachment stream.Creates and adds an element node to the current node. The element name is the string passed in as a parameter. The new element has no text child nodes.Creates and adds an element node with a text child node to the current node.Gets the document element node of the XMLdocument2 object. The document element node is the root node.Gets the first node in the specified xPath.Gets the node after the specified node.Gets the node specified in the xPath.Gets all the text child nodes from the node referenced in the specified XPath.Parses the XML string and loads it into the XMLDocument2 object.Makes the node passed in as a parameter the current node.Sets whether nodes are treated as CDATA or regular text after parsing. CDATA reporting is deactivated by default.When set to true, the XMLDocument2 object processes the document with XML namespaces.Returns a string containing the XML.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# XMLDocument2 - Scoped, Global

The XMLDocument2 API is a JavaScript object wrapper for parsing and extracting XML data from an XML string.

Use this JavaScript class to create an object from an XML string, usually a return value from a web-service invocation, or the XML payload of ECC Queue. Using the XMLDocument2 object in a JavaScript business rule lets you query values from the XML elements and attributes directly.

An XML string has a tree structure, and the parts of the structure are called nodes. An XMLDocument2 object deals with two node types, element, and document element. An element node is a node with a name and possibly attributes and child nodes. A document-element node is the root node of the XML tree. It is the only node without a parent node.

**Note:** This API works for scoped or global applications.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped XMLDocument2 - XMLDocument2\(\)

Creates an XMLDocument2 object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## Scoped XMLDocument2 - XMLDocument2\( GlideScriptableInputStream inputStream\)

Creates an XMLDocument2 object from an attachment stream.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The input stream the XMLDocument2 object encapsulates.|

## Scoped XMLDocument2 - createElement\(String name\)

Creates and adds an element node to the current node. The element name is the string passed in as a parameter. The new element has no text child nodes.

|Name|Type|Description|
|----|----|-----------|
|name|String|The new element's name.|

|Type|Description|
|----|-----------|
|XMLNode|Current XML node.|

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
xmlDoc.createElement("new2"); 
 
gs.info(xmlDoc);
```

Output:

```
?xml version="1.0" encoding="UTF-8"?>
<test>  
    <one>    
        <two att="xxx">abcd1234</two>    
            <three att="yyy" boo="yah">1234abcd</three>    
        <two>another</two>  
    </one>  
    <number>1234</number>
    <new2></new2>
</test>
```

## Scoped XMLDocument2 - createElementWithTextValue\(String name, String value\)

Creates and adds an element node with a text child node to the current node.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the element to add.|
|value|String|Element's text value.|

|Type|Description|
|----|-----------|
|XMLNode|Current XML node.|

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
xmlDoc.createElementWithTextValue("new", "test");
gs.info(xmlDoc);
```

Output:

```
<?xml version="1.0" encoding="UTF-8"?>
    <test>
        <one>
            <two att="xxx">abcd1234</two>    
            <three att="yyy" boo="yah">1234abcd</three>    
            <two>another</two>  
        </one>  
        <number>1234</number>
        <new>test</new>
    </test>
```

## Scoped XMLDocument2 - getDocumentElement\(\)

Gets the document element node of the XMLdocument2 object. The document element node is the root node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLNode|The document element.|

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
//returns the root node of the document tree.
var rootNode = xmlDoc.getDocumentElement();
gs.info(rootNode.getTextContent());
```

Output:

```
abcd1234    1234abcd    another    1234
```

## Scoped XMLDocument2 - getFirstNode\(String xPath\)

Gets the first node in the specified xPath.

This method only supports a subset of predicate xPath expressions. For example, assume the following document:

```
<store> 
    <resources company="ABC Inc"> 
        <resources type="servers" /> 
    </resources> 
    <resources company="XYZ Inc"> 
        <resource type="bookstore"> 
            <book> 
                <title>Windows</title> 
                <price>10</price> 
            </book> 
            <book year="2009"> 
                <title>Harry Potter</title> 
                <price>50</price> 
            </book> 
            <book year="1999"> 
                <title>Learning XML</title> 
                <price>120</price> 
            </book> 
            <book year="2019"> 
                <title>Learning Java</title> 
                <price>99</price> 
            </book> 
        </resource> 
    </resources> 
</store> 
```

This method supports the following xPath expressions with predicates:

```
"/store/resources/resource[@type='bookstore']/book[@year='1999']", 
"/store/resources/resource[@type='bookstore']/book[@year]", 
"/store/resources/resource[@type='bookstore']/book[price > 100]" 
```

However, it does not support the following xPath expressions with predicates:

```
"/store/resources/resource[@type='bookstore']/book[2]", 
"/store/resources/resource[@type='bookstore']/book[last()]", 
"/store/resources/resource[@type='bookstore']/book[position()>2]" 
```

To work around this, use xPath without predicates, such as `"/store/resources/resource[@type='bookstore']/book")` and then filter the nodes in the script using the getFirstNode\(\) and [getNextNode\(\)](c_XMLDocument2ScopedAPI.md#) methods.

|Name|Type|Description|
|----|----|-----------|
|xPath|String|The xPath to obtain the node from.|

|Type|Description|
|----|-----------|
|XMLNode|The first node.|

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
var foo = xmlDoc.getFirstNode('/test/one/two');
gs.info(foo.getTextContent());
```

Output:

```
abcd1234
```

## Scoped XMLDocument2 - getNextNode\(Object current\)

Gets the node after the specified node.

|Name|Type|Description|
|----|----|-----------|
|current|Object|The current node.|

|Type|Description|
|----|-----------|
|XMLNode|The next node.|

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
var foo = xmlDoc. getFirstNode('/test/one/two');
var foo2 = xmlDoc.getNextNode(foo);
gs.info(foo.getTextContent());
gs.info(foo2.getTextContent());
```

Output:

```
abcd1234

another
```

## Scoped XMLDocument2 - getNode\(String xPath\)

Gets the node specified in the xPath.

**Note:** This method is intended for use with small documents since it parses the entire document to match the xPath expression. If the document is too large, an out of memory error may occur. For large documents, use the [getFirstNode\(String xPath\)](c_XMLDocument2ScopedAPI.md#) and [getNextNode\(Object current\)](c_XMLDocument2ScopedAPI.md#) methods, which are designed to stream through the document without parsing the entire document.

|Name|Type|Description|
|----|----|-----------|
|xPath|String|xPath of the node to obtain.|

|Type|Description|
|----|-----------|
|XMLNode|Current XML node.|

```
/*
 * Checks if given node indeed of given tag.
 * Params:
 *  tag - String, name of tag to check
 *  node - XMLNode, node in which to check for the tag
 * Returns:
 *  true, if tag is present
 *  false, otherwise
 */
function isNodeOfTag (node, tag) {
  try {
    if (tag == node.getNodeName()) {
      gs.info("Given node belongs to tag " + tag);
      return true;
    }
  } catch (error) {
    gs.error("Given node might not belong to tag " + tag + ". Error while checking: " + error);
    return false;
  }
}

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

var node = xmlDoc.getNode("/test/one/two"); // tag 'two' is present in this XML.
isNodeOfTag(node, "two");

var node = xmlDoc.getNode("/test/one/four"); // tag 'four' is not present in this XML.
isNodeOfTag(node, "four");
```

Output:

```
Given node belongs to tag two
Given node might not belong to tag four. Error while checking: java.lang.NullPointerException
```

## Scoped XMLDocument2 - getNodeText\(String xPath\)

Gets all the text child nodes from the node referenced in the specified XPath.

|Name|Type|Description|
|----|----|-----------|
|xPath|String|XPath of the text to obtain.|

|Type|Description|
|----|-----------|
|String|Text children in the XPath.|

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
gs.info(xmlDoc.getNodeText("//two"));
```

Output:

```
abcd1234
```

## Scoped XMLDocument2 - parseXML\(String xmlDoc\)

Parses the XML string and loads it into the XMLDocument2 object.

|Name|Type|Description|
|----|----|-----------|
|xmlDoc|String|The document to parse.|

|Type|Description|
|----|-----------|
|Boolean|Flag that indicates whether the content was parsed.|

This example parses the xmlString and loads it into the xmlDocument2 object.

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
var rootNode = xmlDoc.getDocumentElement();
```

## Scoped XMLDocument2 - setCurrentElement\(XMLNode element\)

Makes the node passed in as a parameter the current node.

|Name|Type|Description|
|----|----|-----------|
|element|XMLNode|The element node to set as the current node.|

|Type|Description|
|----|-----------|
|void| |

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
//returns the root node of the document tree.
var rootNode = xmlDoc.getDocumentElement(); //returns org.w3c.dom.Element
// sets the root node as the current element
xmlDoc.setCurrentElement(rootNode);
```

## Scoped XMLDocument2 - setEnableCDATAReporting\(Boolean enable\)

Sets whether nodes are treated as CDATA or regular text after parsing. CDATA reporting is deactivated by default.

This method must be called with [Scoped XMLDocument2 - parseXML\(String xmlDoc\)](c_XMLDocument2ScopedAPI.md#).

See also: [Scoped XMLNode - isCDATANode\(\)](../../XMLNodeScopedAPI/concept/c_XMLNodeScopedAPI.md#).

<table id="table_bk3_rjy_3x" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

enable

</td><td>

Boolean

</td><td>

Flag that indicates whether to handle CDATA nodes as CDATA or regular text nodes.Valid values:

-   true: Enable CDATA reporting.
-   false: Handle CDATA nodes as regular text nodes after parsing and concatenate it with the adjacent text.

Default: False

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how CDATA is parsed in an element with CDATA reporting activated. The result of content.getFirstChild\(\) is an element that holds the text value `another`. This element internally contains the information identifying it as a CDATA type. The result of content.getLastChild\(\) is an element that holds the text value `element`. This element internally contains the information as a text type.

```
var xmlString = "<test>" +
  "  <one>" +
  "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
  "    <two><![CDATA[another]]>element</two>" +
  "  </one>" +
  "  <number>1234</number>" 
  "</test>";
var xmlDoc = new XMLDocument2();
xmlDoc.setEnableCDATAReporting(true); // Enable CDATA reporting
xmlDoc.parseXML(xmlString);
var content = xmlDoc.getFirstNode('/test/one/two');
gs.info(content.getFirstChild().getTextContent()); // prints "another"
gs.info(content.getLastChild().getTextContent()); // prints "element"
```

Output:

```
another
element
```

**Note:** Without CDATA reporting activated in the example, the entire child concatenates the CDATA as text with the rest of the text \(`element`\) in each line as follows:

```
anotherelement
anotherelement
```

## Scoped XMLDocument2 - setNamespaceAware\(Boolean aware\)

When set to true, the XMLDocument2 object processes the document with XML namespaces.

If you don't set this, an XML document with namespaces won't be enumerated correctly, and an XPath search would fail. 

|Name|Type|Description|
|----|----|-----------|
|aware|Boolean|When true, the XMLDocument2 object processes the document with XML namespaces.|

|Type|Description|
|----|-----------|
|void| |

## Scoped XMLDocument2 - toString\(\)

Returns a string containing the XML.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A string containing the XML.|

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
gs.info(xmlDoc.toString());
```

Output - Line breaks were added to the output for readability.

```
<?xml version="1.0" encoding="UTF-8"?>
<test>  
<one>    
<two att="xxx">abcd1234</two>    
<three att="yyy" boo="yah">1234abcd</three>    
<two>another</two>  
</one>  
<number>1234</number>
</test>
```

