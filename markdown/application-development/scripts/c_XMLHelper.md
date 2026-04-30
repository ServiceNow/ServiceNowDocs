---
title: XMLHelper
description: The XML helper script include makes it easy to parse XML in scripts.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [XMLDocument script object, Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# XMLHelper

The XML helper script include makes it easy to parse XML in scripts.

Use the following methods to export XML to JSON, or JSON to XML.

-   The toObject\(\) method returns the XML elements as JSON properties. This method works properly whether the supplied parameter is an XML document or an XML string. This method has an optional parameter of the XML input for conversion as an alternative to specifying the XML input in the constructor.
-   The toXMLDoc\(\) method returns JSON provided as XML elements.

**Note:** You must escape ampersand characters \(&amp;amp\) in your XML or the conversion silently fails.

## Example

The following example shows how to convert an XML document into JSON and uses a recursive function to output each member. The recursive function helps indicate how the XML document structure is rendered as JSON.

```
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

```
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

**Parent Topic:**[XMLDocument script object](c_XMLDocumentScriptObject.md)

