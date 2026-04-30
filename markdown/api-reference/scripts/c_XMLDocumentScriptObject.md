---
title: XMLDocument script object
description: A JavaScript object wrapper for parsing and extracting XML data from an XML document \(String\).
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# XMLDocument script object

A JavaScript object wrapper for parsing and extracting XML data from an XML document \(String\).

Use this Javascript class to instantiate an object from an XML string, usually a return value from a Web Service invocation, or the XML payload of ECC Queue. Using the XMLDocument object in a Javascript business rule lets you query values from the XML elements and attributes directly.

## Constructor

The constructor of a script object creates a new instance of the object to be used.

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";

var xmldoc = new XMLDocument(xmlString);
```

To perform XML parsing of an XML string that is name space qualified, specify "true" for the second argument for the XMLDocument constructor. The following is an example of parsing and XML string that contains name space qualification of its elements.

```
var xmlString = "<bk:book xmlns:bk='urn:loc.gov:books' xmlns:isbn='urn:ISBN:0-395-36341-6'>" +
                  "<bk:title>Cheaper by the Dozen</bk:title>" +
                  "<isbn:number>1568491379</isbn:number>" +
                "</bk:book>";

var xmldoc = new XMLDocument(xmlString, true); // XML document is name space aware

```

## Locating nodes and elements

Now that we have the XMLDocument object, we can call the following APIs to locate nodes and elements of the XML document, as well as extract text from it directly. The query syntax for locating nodes and attributes is based on XPath.

**Note:** XML parsing with this object is not namespace aware, this means that if you are locating a node name with namespace in it eg. "&lt;names:myelement&gt; ...", the XPath search string would be "//myelement"

The following are examples of locating a node by its XPath and getting the text value out of the resulting node.

```
var str = xmldoc.getNodeText("//two"); // returns the first occurrence of the node
// str == "abcd1234"

str = xmldoc.getNodeText("//three");
// str == "1234abcd"

str = xmldoc.getNodeText("/test/one/*");
// str == "abcd1234"

str = xmldoc.getNodeInt("//number");
// str == 1234

```

The following examples locates the node by XPath and uses the API on node and element to get attributes and value.

```
var node = xmldoc.getNode("/test/one/two");
// node.getNodeName() == "two"
// node.getNodeType() == "1" // 1 == ELEMENT_NODE
// node.getLastChild().getNodeType() == "3" // 3 == TEXT_NODE
// node.getLastChild().getNodeValue() == "abcd1234"
```

Or you can use the following convenience functions to get the node name and type

```
str = xmldoc.getNodeName("//three");
// str == "three"

str = xmldoc.getNodeType("//three");
// str == "1"
```

You can also get a list of nodes that you can iterate or access directly by position

```
var nodelist = xmldoc.getNodes("//one/*"); // two, three, and two
// nodelist.getLength() == "3"
// nodelist.item(0).getNodeName() == "two"
// nodelist.item(1).getNodeName() == "three"
```

The following is an example of parsing an XML string that is qualifed with name spaces.

```
var xmlString = "<bk:book xmlns:bk='urn:loc.gov:books' xmlns:isbn='urn:ISBN:0-395-36341-6'>" +
                  "<bk:title>Cheaper by the Dozen</bk:title>" +
                  "<isbn:number>1568491379</isbn:number>" +
                "</bk:book>";

var xmldoc = new XMLDocument(xmlString, true);
var str = xmldoc.getNodeText("//bk:title"); // returns the first occurence of the node
gs.log(str);

str = xmldoc.getNodeText("/bk:book/*");
gs.log(str);

str = xmldoc.getNodeInt("//isbn:number");
gs.log(str);
```

## Getting attribute values

An attribute is just an extension of a node and so it has all the same APIs.

The following example shows how to query for a node to get its attribute by position

```
node = xmldoc.getNode("//two");
// node.getAttributes().item(0).getNodeValue() == "xxx"

str = xmldoc.getAttribute("//two", "att");
// str == "xxx"
```

XPath also has a query syntax for locating the attribute node directly, for example

```
str = xmldoc.getNodeText("//*[@att=\"yyy\"]");
// str == "1234abcd"

str = xmldoc.getNode("//@boo").getNodeValue();
// str == "yah"

```

## Creating new elements

An XML element can be created at any level of the XML document once it has been created. Use the setCurrent function to position where the new element will be created as a child element, and use the createElement function to create the element.

```
var xmlString = "<test>" +
                "  <one>" +
                "    <two att=\"xxx\">abcd1234</two>" +
                "    <three boo=\"yah\" att=\"yyy\">1234abcd</three>" +
                "    <two>another</two>" +
                "  </one>" +
                "  <number>1234</number>" +
                "</test>";

var xmldoc = new XMLDocument(xmlString);
xmldoc.createElement("new", "test"); // creates the new element at the document element level if setCurrent is never called
xmldoc.createElement("new2"); // calling without a value will create a new element by itself

var el = xmldoc.createElement("new3");
xmldoc.setCurrent(el); // this is now the parent of any new elements created subsequently using createElement()
xmldoc.createElement("newChild", "test");
```

The resulting XML document looks like this

```
<test>
  <one>
    <two att="xxx">abcd1234</two>
    <three boo="yah" att="yyy">1234abcd</three>
    <two>another</two>
  </one>
  <number>1234</number>
  <new>test<new>
  <new2/>
  <new3>
      <newChild>test</newChild>
  </new3>
</test>
```

-   **[XMLHelper](c_XMLHelper.md)**  
The XML helper script include makes it easy to parse XML in scripts.

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

