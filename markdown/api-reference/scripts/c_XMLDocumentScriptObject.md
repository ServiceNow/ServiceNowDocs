---
title: Parsing and extracting XML data in server-side scripts
description: A JavaScript object wrapper for parsing and extracting XML data from an XML document \(String\).The XML helper script include makes it easy to parse XML in scripts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_XMLDocumentScriptObject.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Write server-side scripts, Scripting, API implementation, API implementation and reference]
---

# Parsing and extracting XML data in server-side scripts

A JavaScript object wrapper for parsing and extracting XML data from an XML document \(String\).

Use this Javascript class to instantiate an object from an XML string, usually a return value from a Web Service invocation, or the XML payload of ECC Queue. Using the XMLDocument object in a Javascript business rule lets you query values from the XML elements and attributes directly.

## Constructor

The constructor of a script object creates a new instance of the object to be used.

```javascript
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

```javascript
var xmlString = "<bk:book xmlns:bk='urn:loc.gov:books' xmlns:isbn='urn:ISBN:0-395-36341-6'>" +
                  "<bk:title>Cheaper by the Dozen</bk:title>" +
                  "<isbn:number>1568491379</isbn:number>" +
                "</bk:book>";

var xmldoc = new XMLDocument(xmlString, true); // XML document is name space aware

```

## Locating nodes and elements

Now that we have the XMLDocument object, we can call the following APIs to locate nodes and elements of the XML document, and extract text from it directly. The query syntax for locating nodes and attributes is based on XPath.

**Note:** XML parsing with this object is not namespace aware, this means that if you are locating a node name with namespace in it eg. "&lt;names:myelement&gt; ...", the XPath search string would be "//myelement"

The following are examples of locating a node by its XPath and getting the text value out of the resulting node.

```javascript
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

```javascript
var node = xmldoc.getNode("/test/one/two");
// node.getNodeName() == "two"
// node.getNodeType() == "1" // 1 == ELEMENT_NODE
// node.getLastChild().getNodeType() == "3" // 3 == TEXT_NODE
// node.getLastChild().getNodeValue() == "abcd1234"
```

Or you can use the following convenience functions to get the node name and type

```javascript
str = xmldoc.getNodeName("//three");
// str == "three"

str = xmldoc.getNodeType("//three");
// str == "1"
```

You can also get a list of nodes that you can iterate or access directly by position

```javascript
var nodelist = xmldoc.getNodes("//one/*"); // two, three, and two
// nodelist.getLength() == "3"
// nodelist.item(0).getNodeName() == "two"
// nodelist.item(1).getNodeName() == "three"
```

The following is an example of parsing an XML string that is qualifed with name spaces.

```javascript
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

```javascript
node = xmldoc.getNode("//two");
// node.getAttributes().item(0).getNodeValue() == "xxx"

str = xmldoc.getAttribute("//two", "att");
// str == "xxx"
```

XPath also has a query syntax for locating the attribute node directly, for example

```javascript
str = xmldoc.getNodeText("//*[@att=\"yyy\"]");
// str == "1234abcd"

str = xmldoc.getNode("//@boo").getNodeValue();
// str == "yah"

```

## Creating new elements

An XML element can be created at any level of the XML document once it has been created. Use the setCurrent function to position where the new element will be created as a child element, and use the createElement function to create the element.

```javascript
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

```xml
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

**Parent Topic:**[Writing server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/server-side-scripting-overview.md)

**Related topics**  


[XMLDocument2 - Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/c_XMLDocument2ScopedAPI.md)

## XMLHelper

The XML helper script include makes it easy to parse XML in scripts.

Use the following methods to export XML to JSON, or JSON to XML.

-   The toObject\(\) method returns the XML elements as JSON properties. This method works properly whether the supplied parameter is an XML document or an XML string. This method has an optional parameter of the XML input for conversion as an alternative to specifying the XML input in the constructor.
-   The toXMLDoc\(\) method returns JSON provided as XML elements.

**Note:** You must escape ampersand characters \(&amp;amp\) in your XML or the conversion silently fails.

### Example

The following example shows how to convert an XML document into JSON and uses a recursive function to output each member. The recursive function helps indicate how the XML document structure is rendered as JSON.

```javascript
var xmlString = "<company>" + "<employee>" + "<id>10</id>"
 + "<firstname>Tom</firstname>" + "<lastname>Cruise</lastname>" + "<test>test1</test>"
 + "<test>test3</test>" + "</employee>" + "<employee>" + "<id>20</id>" + "<firstname>Paul</firstname>"
 + "<lastname>Enderson</lastname>" + "<test>test6</test>" + "<test>test5</test>" + "</employee>" + "<employee>"
 + "<id>30</id>" + "<firstname>Paul</firstname>" + "<lastname>Bush</lastname>" + "<test>test2</test>"
 + "<test>test4</test>" + "</employee>" + "</company>";
var helper = new XMLHelper(xmlString);
var obj = helper.toObject();
logObj(obj, "*");

function logObj(obj, sep) {
  for (x in obj) {
    if (typeof obj[x] != "function") {
      gs.log(sep + x + ":: " + obj[x]);
    }
    logObj(obj[x], sep + "*");
  }
}
```

Output:

```javascript
*** Script: *employee:: [object Object],[object Object],[object Object]
*** Script: **2:: [object Object]
*** Script: ***id:: 30
*** Script: ***test:: test2,test4
*** Script: ****0:: test2
*** Script: ****1:: test4
*** Script: ***firstname:: Paul
*** Script: ***lastname:: Bush
*** Script: **0:: [object Object]
*** Script: ***id:: 10
*** Script: ***test:: test1,test3
*** Script: ****0:: test1
*** Script: ****1:: test3
*** Script: ***firstname:: Tom
*** Script: ***lastname:: Cruise
*** Script: **1:: [object Object]
*** Script: ***id:: 20
*** Script: ***test:: test6,test5
*** Script: ****0:: test6
*** Script: ****1:: test5
*** Script: ***firstname:: Paul
*** Script: ***lastname:: Enderson
```

