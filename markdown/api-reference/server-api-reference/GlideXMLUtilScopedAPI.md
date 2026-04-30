---
title: GlideXMLUtil - Scoped, Global
description: The GlideXMLUtil API provides methods to remove invalid characters from an XML string and to validate an XML string.Removes invalid characters from an XML string.Determines if the specified string is valid XML.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideXMLUtil - Scoped, Global

The GlideXMLUtil API provides methods to remove invalid characters from an XML string and to validate an XML string.

Access these methods using the static object GlideXMLUtil. This class is available in scoped and global scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideXMLUtil - removeInvalidChars\(String xmlString\)

Removes invalid characters from an XML string.

|Name|Type|Description|
|----|----|-----------|
|xmlString|String|The string to be processed.|

|Type|Description|
|----|-----------|
|String|A string with invalid characters removed.|

```
var test = "test\btab";
var removedTest = GlideXMLUtil.removeInvalidChars(test);

gs.info(removedTest);
```

Output: testtab

## GlideXMLUtil - validateXML\(String xmlString, Boolean nsAware, Boolean forgiveUnclosed\)

Determines if the specified string is valid XML.

|Name|Type|Description|
|----|----|-----------|
|xmlString|String|The string to be validated.|
|nsAware|Boolean|When true, the validation is aware of name spaces. When false, the validation ignores name spaces.|
|forgiveUnclosed|Boolean|When true, the validation does not check for &lt;xml&gt; tags enclosing the string.|

|Type|Description|
|----|-----------|
|String|Returns null if the string is valid. Returns an error string describing the error if the specified string is not valid.|

```
var s = "<?xml version=\"1.0\" encoding=\"UTF-8\"?><unload unload_date=\"2017-11-27 21:56:14\"><incident action=\"INSERT_OR_UPDATE\"><active>true</active></incident></unload>";
var xml = GlideXMLUtil.validateXML(s,false, false);
gs.info(xml);

```

Output: null

