---
title: XMLStreamingAPI - Scoped
description: Builds a large streaming XML payload for use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as an XML string for a non-streaming option.Closes the XMLStreamingAPI object. You must call this method to close the stream after building your XML document.Ends pretty print XML formatting.Adds pretty print formatting to an XML element or tree of elements.Ends the structure of your XML document.Adds a closing tag to an XML element.Returns the XML document as a string.Begins building an XML document.Adds a starting tag for an XML element.Adds a list of nested elements with predefined text to your streaming XML document.Adds an attribute to an element in your XML document.Adds attributes to an element in your XML document.Adds CDATA to your XML document.Adds a CDATA element to your XML document.Adds text to your XML document.Adds a comment to your XML document.Adds a document type definition to your XML document.Adds a namespace to an element in your XML document.Adds namespaces to the root element in your XML document.Adds a single XML element to your XML document.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 16
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# XMLStreamingAPI- Scoped

Builds a large streaming XML payload for use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as an XML string for a non-streaming option.

Use these methods in a Workflow Studio Script step with the `sn_ih` namespace identifier. For example, you can use this API to create an XML payload in the Workflow Studio Script step and pass the returned value to the REST step to send the request to a third-party service. For more information, see the Workflow Studio [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

**Note:** You can only use this API within the Workflow Studio environment.

There is no constructor for this class. Instead, you must call the build\(\) method in the [XMLStreamingBuilder](../../XMLStreamingBuilder/concept/XMLStreamingBuilderScopedAPI.md#) class to return an XMLStreamingAPI object.

## API call order

Generate XML payloads by first instantiating a builder object with XMLStreamingBuilder and then calling the methods in the XMLStreamingAPI class:

-   **1. XMLStreamingBuilder: Creates a builder object**

    Use these method in the following order to create a builder object:

    1.  XMLStreamingBuilder\(\): Instantiates the XMLStreamingBuilder object.
    2.  withAttachment\(\): Optional. Creates an XML document as an attachment and stores it in the Streaming Attachments \[streaming\_attachment\] table. If you don't call this method, the API builds the payload as an XML string.
    3.  expiresAt\(\): Optional. Sets a time when the attachment expires. False is the default. Must also call the withAttachment\(\) method.
    4.  build\(\): Returns an XMLStreamingAPI object.
-   **2. XMLStreamingAPI: Builds the XML payload**

    Use these methods in the following order to create the XML payload:

    1.  startDocument\(\): Creates the top-level parent element in the XML document.
    2.  Methods to generate child elements in the XML document, such as writeTextElement\(\), startElement\(\), and writeArray\(\).
    3.  Methods to generate attributes for an element, such as writeAttribute\(\), writeNamespace\(\), and writeDtd\(\).
    4.  endElement\(\): Closes an XML element.
    5.  endDocument: Closes the top-level parent element.
    6.  getXMLString\(\) or getAttachmentId\(\): Returns the XML string or attachment ID that you created.
    7.  close\(\): Closes the XMLStreamingAPI object.

## Size limits

Payloads generated through this API cannot exceed these size limits:

-   Attachments: 200 MB
-   Strings: 5 MB

The following example shows how to create an XML document and store it in the Streaming Attachments \[streaming\_attachment\] table with a defined expiration date.

```

try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment() // Creates the XML document in streaming mode within an attachment.
    .expiresAt(ttl) // Sets an expiration date for the attachment.
    .build(); // Creates the XMLStreamingAPI object.

  builder.startDocument("Employee") // Begins generating the XML document.
    .writeTextElement("firstName","John") // Writes a "firstName" element and value.
    .writeTextElement("lastName","Smith")
    .writeTextElement("age","25")
    .startElement("address") // Adds an "address" parent element.
      .writeTextElement("streetAddress", "21 2nd Street") // Writes a child element and value.
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement() // Adds a closing tag for the "address" element.
    .startElement("phoneNumber")
      .writeTextElement("type","home")
      .writeTextElement("number","212 555-1234")
      .writeTextElement("type","fax")
      .writeTextElement("number","646 555-4567")
    .endElement()
  .endDocument() // Stops generating the XML document.
      
  gs.log(builder.getAttachmentId()); // Returns the sys_id of the attachment.
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

Alternatively, this example shows how to use the API in the Script step and create the payload as an XML string. You can use this option to create payloads under 5 MB.

```
(function execute(inputs, outputs) {

  var builder = new sn_ih.XMLStreamingBuilder().build();
  
  builder.startDocument("Employee")
    .enablePrettyPrint()
    .writeTextElement("firstName","John")
    .writeTextElement("lastName","Smith")
    .writeTextElement("age","25")
    .startElement("address")
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement()
    .startElement("phoneNumber")
      .writeTextElement("type","home")
      .writeTextElement("number","212 555-1234")
      .writeTextElement("type","fax")
      .writeTextElement("number","646 555-4567")
    .endElement()
  .endDocument()

  outputs.payload = builder.getXMLString();
  
})(inputs, outputs);
```

Output:

```
<?xml version="1.0" encoding="UTF-8"?>
<firstName>John</firstName>
<lastName>Smith</lastName>
<age>25</age>
<address>
  <streetAddress>21 2nd Street</streetAddress>
  <city>Santa Clara</city>
  <state>CA</state>
  <postalCode>11111</postalCode>
</address>
<phoneNumber>
  <type>home</type>
  <number>212 555-1234</number>
  <type>fax</type>
  <number>646 555-4567</number>
</phoneNumber>
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## XMLStreamingAPI - close\(\)

Closes the XMLStreamingAPI object. You must call this method to close the stream after building your XML document.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

### Example

The following example shows how to create an XML document and store it in the Streaming Attachments \[streaming\_attachment\] table with a defined expiration date.

```

try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment() // Creates the XML document in streaming mode within an attachment.
    .expiresAt(ttl) // Sets an expiration date for the attachment.
    .build(); // Creates the XMLStreamingAPI object.

  builder.startDocument("Employee") // Begins generating the XML document.
    .writeTextElement("firstName","John") // Writes a "firstName" element and value.
    .writeTextElement("lastName","Smith")
    .writeTextElement("age","25")
    .startElement("address") // Adds an "address" parent element.
      .writeTextElement("streetAddress", "21 2nd Street") // Writes a child element and value.
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement() // Adds a closing tag for the "address" element.
    .startElement("phoneNumber")
      .writeTextElement("type","home")
      .writeTextElement("number","212 555-1234")
      .writeTextElement("type","fax")
      .writeTextElement("number","646 555-4567")
    .endElement()
  .endDocument() // Stops generating the XML document.
      
  gs.log(builder.getAttachmentId()); // Returns the sys_id of the attachment.
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - disablePrettyPrint\(\)

Ends pretty print XML formatting.

Before calling this method, you must first call enablePrettyPrint\(\) to add XML formatting to a section.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to add pretty print formatting to the `address` element.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment()
    .expiresAt(ttl)
    .build();

  builder.startDocument("Employee")
    .writeTextElement("firstName","John")
    .writeTextElement("lastName","Smith")
    .writeTextElement("age","25")
    .enablePrettyPrint()
    .startElement("address")
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement()
    .disablePrettyPrint()
    .startElement("phoneNumber")
      .writeTextElement("type","home")
      .writeTextElement("number","212 555-1234")
      .writeTextElement("type","fax")
      .writeTextElement("number","646 555-4567")
    .endElement()
  .endDocument()
      
  gs.log(builder.getAttachmentId());
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - enablePrettyPrint\(\)

Adds pretty print formatting to an XML element or tree of elements.

Use the disablePrettyPrint\(\) method to end the formatting.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to add pretty print formatting to the `address` element.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment()
    .expiresAt(ttl)
    .build();

  builder.startDocument("Employee")
    .writeTextElement("firstName","John")
    .writeTextElement("lastName","Smith")
    .writeTextElement("age","25")
    .enablePrettyPrint()
    .startElement("address")
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement()
    .disablePrettyPrint()
    .startElement("phoneNumber")
      .writeTextElement("type","home")
      .writeTextElement("number","212 555-1234")
      .writeTextElement("type","fax")
      .writeTextElement("number","646 555-4567")
    .endElement()
  .endDocument()
      
  gs.log(builder.getAttachmentId());
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - endDocument\(\)

Ends the structure of your XML document.

After calling the startDocument\(\) method and organizing your streaming XML document, call the endDocument\(\) method at the end of your document's structure. You must use these two methods together to successfully build your streaming XML document's structure.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to create an XML document containing elements about a user.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
        .writeTextElement('firstName', 'John')
        .writeTextElement('lastName', 'Smith')
        .writeTextElement('age', '25')
        .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - endElement\(\)

Adds a closing tag to an XML element.

Use the following methods in this sequence to create a valid XML element:

1.  Use the startElement\(\) method to add a starting tag.
2.  Use the endElement\(\) method to add the closing tag.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to build a parent element named `address` and then write four child elements.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment()
    .expiresAt(ttl)
    .build();

  builder.startDocument("Employee")
      .startElement("address")
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement()
  .endDocument()
      
  gs.log(builder.getAttachmentId());
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - getXMLString\(\)

Returns the XML document as a string.

To return the XML document as a string, don't call the getAttachementId\(\) method in the XMLStreamingBuilder class. For more information, see [XMLStreamingBuilder - Scoped](../../XMLStreamingBuilder/concept/XMLStreamingBuilderScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|XML document created using the XMLStreamingAPI methods, as a string.|

The following example shows how to create an XML document and then return it as a string.

```
(function execute(inputs, outputs) {

  var builder = new sn_ih.XMLStreamingBuilder().build();
  
  builder.startDocument("Employee")
    .enablePrettyPrint()
    .writeTextElement("firstName","John")
    .writeTextElement("lastName","Smith")
    .writeTextElement("age","25")
    .startElement("address")
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement()
    .startElement("phoneNumber")
      .writeTextElement("type","home")
      .writeTextElement("number","212 555-1234")
      .writeTextElement("type","fax")
      .writeTextElement("number","646 555-4567")
    .endElement()
  .endDocument()

  outputs.payload = builder.getXMLString();
  
})(inputs, outputs);
```

Output:

```
<?xml version="1.0" encoding="UTF-8"?>
<firstName>John</firstName>
<lastName>Smith</lastName>
<age>25</age>
<address>
  <streetAddress>21 2nd Street</streetAddress>
  <city>Santa Clara</city>
  <state>CA</state>
  <postalCode>11111</postalCode>
</address>
<phoneNumber>
  <type>home</type>
  <number>212 555-1234</number>
  <type>fax</type>
  <number>646 555-4567</number>
</phoneNumber>
```

## XMLStreamingAPI - startDocument\(String rootElement, Object namespaceDefinitionMap\)

Begins building an XML document.

After calling the build\(\) method, call the startDocument\(\) method to start organizing your XML document. You must also call the endDocument method at the end of your document's structure.

<table id="table_yyj_tqg_dlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

rootElement

</td><td>

String

</td><td>

Optional. Root element, or top-level parent element, for your XML document.

</td></tr><tr><td>

namespaceDefinitionMap

</td><td>

Object

</td><td>

Optional. Map of keys and values for the namespaces and their associated values in a subsequent list of elements. For example: ```
{
'namespaceOne':'namespaceValue',
'namespaceTwo':'namespaceValue'
}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to create an XML document containing elements with information about an employee.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
        .writeTextElement('firstName', 'John')
        .writeTextElement('lastName', 'Smith')
        .writeTextElement('age', '25')
        .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - startElement\(String name, Object namespaceMap, Object attributeMap, String prefix\)

Adds a starting tag for an XML element.

Use the following methods in this sequence to create a valid XML element:

1.  Use the startElement\(\) method to add a starting tag.
2.  Use the endElement\(\) method to add the closing tag.

<table id="table_d1l_cjh_dlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the XML element.

</td></tr><tr><td>

namespaceMap

</td><td>

Object

</td><td>

Optional. Map of keys and values for the namespaces and their associated values in a subsequent list of elements. For example:```
{
'namespaceOne':'namespaceValue',
'namespaceTwo':'namespaceValue'
}
```

</td></tr><tr><td>

attributeMap

</td><td>

Object

</td><td>

Optional. Map of keys and values for the attributes and their associated values in a subsequent list of elements.

</td></tr><tr><td>

prefix

</td><td>

String

</td><td>

Optional. Prefix for the XML element.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to build a parent element named address and then write four child elements.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment()
    .expiresAt(ttl)
    .build();

  builder.startDocument("Employee")
      .startElement("address")
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
    .endElement()
  .endDocument()
      
  gs.log(builder.getAttachmentId());
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - writeArray\(String elementName, Array data, String wrappingElement\)

Adds a list of nested elements with predefined text to your streaming XML document.

After calling the startDocument\(\) method, you can call the writeArray\(\) method to add a block of nested elements to your streaming XML document.

|Name|Type|Description|
|----|----|-----------|
|elementName|String|Name of the XML element associated with each string listed in the **data** array.|
|data|Array|List of values to assign to each element nested inside **wrappingElement**.|
|wrappingElement|String|Parent element containing each **elementName**.|

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to build a parent element named `officeLocations`, and then nest an array of five `city` elements.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment()
    .expiresAt(ttl)
    .build();

  builder.startDocument("Employee")
      .writeArray('city', ['Santa Clara','San Diego','Chicago','Sydney','London'], 'officeLocations')
  .endDocument()
      
  gs.log(builder.getAttachmentId());
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - writeAttribute\(String name, String value\)

Adds an attribute to an element in your XML document.

After calling the startDocument\(\), startElement\(\), or writeTextElement\(\) method, you can call the writeAttribute\(\) method to add an attribute to the associated XML element.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the XML element's attribute.|
|value|String|Value for the XML element's attribute.|

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

This example adds an attribute named idNumber to the employee element.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
    .writeAttribute('idNumber','12345')
        .writeTextElement('firstName', 'John')
        .writeTextElement('lastName', 'Smith')
        .writeTextElement('age', '25')
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - writeAttributes\(Object attributeMap\)

Adds attributes to an element in your XML document.

After calling the startDocument\(\), startElement\(\), or writeTextElement\(\) method, you can call the writeAttributes\(\) method to add attributes to the associated XML element.

<table id="table_nzt_gbt_jlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attributeMap

</td><td>

Object

</td><td>

Map of keys and values containing attribute names and values to associate with the XML element. For example:```
{
'attributeOne':'attributeValue',
'attributeTwo':'attributeValue'
}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

This example adds attributes named idNumber, officeLocation, and department to the employee element.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
    .writeAttributes({'idNumber':'12345', 'officeLocation':'San Diego', 'department':'Sales'})
        .writeTextElement('firstName', 'John')
        .writeTextElement('lastName', 'Smith')
        .writeTextElement('age', '25')
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - writeCData\(String data\)

Adds CDATA to your XML document.

After calling the writeCDataElement\(\) method, you can call the writeCData\(\) method to add CDATA within the element.

|Name|Type|Description|
|----|----|-----------|
|data|String|Value to include after the CDATA keyword in your CDATA element.|

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

This example adds CDATA to the CDATA element `timeWorked`.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
        .writeTextElement('firstName', 'John')
        .writeTextElement('lastName', 'Smith')
        .writeTextElement('age', '25')
        .writeCDataElement('timeWorked')
        .writeCData('< 2 years')
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - writeCDataElement\(String name, String data, Object prefix\)

Adds a CDATA element to your XML document.

After calling the startDocument\(\) method, you can call the writeCDataElement\(\) method to add a CDATA element to your XML document.

<table id="table_z31_tbt_jlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the CDATA element.

</td></tr><tr><td>

data

</td><td>

String

</td><td>

Optional. Type of data to parse the CDATA element as.

</td></tr><tr><td>

prefix

</td><td>

Object

</td><td>

Optional. Map of child elements and values that the CDATA element includes. For example: ```
{
'prefixOne':'prefixValue',
'prefixTwo':'prefixValue'
}
```

You must associate an XML element's prefix with a namespace using [writeNamespace\(\)](XMLStreamingAPIScopedAPI.md#).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

This example uses a document type definition named `address` to define an internal document type definition for the XML document.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment()
    .expiresAt(ttl)
    .build();

  builder.startDocument("Employee")
  .writeDtd('address')
  .writeCDataElement('home', '#PCDATA', {'streetAddress', 'city', 'state', 'postalCode'})
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
  .endDocument()
      
  gs.log(builder.getAttachmentId());
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - writeCharacters\(String text\)

Adds text to your XML document.

Use the writeCharacters\(\) method to insert string data to a section in your XML document.

|Name|Type|Description|
|----|----|-----------|
|text|String|Text to add to a section of your XML document.|

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to add text values to elements in your XML document.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
        .startElement('firstName')
        .writeCharacters('John')
        .EndElement()
        .startElement('lastName')
        .writeCharacters('Smith')
        .endElement()
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - writeComment\(String comment\)

Adds a comment to your XML document.

After calling the startDocument\(\) method, you can call the writeComment\(\) method to add a comment to your XML document.

|Name|Type|Description|
|----|----|-----------|
|comment|String|Comment text to include.|

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to add a comment to an XML document.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
        .writeComment('Element for information related to active employees.')
        .writeTextElement('firstName', 'John')
        .writeTextElement('lastName', 'Smith')
        .writeTextElement('age', '25')
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - writeDtd\(String dtd\)

Adds a document type definition to your XML document.

After calling the startDocument\(\) method, you can call the writeDtd\(\) method to add a valid XML document type definition to your XML document.

|Name|Type|Description|
|----|----|-----------|
|dtd|String|Name of a valid XML document type definition.|

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

This example uses a document type definition named address to define an internal document type definition for the XML document.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.XMLStreamingBuilder()
    .withAttachment()
    .expiresAt(ttl)
    .build();

  builder.startDocument("Employee")
  .writeDtd('address')
  .writeCDataElement('home', '#PCDATA', {'streetAddress', 'city', 'state', 'postalCode'})
      .writeTextElement("streetAddress", "21 2nd Street")
      .writeTextElement("city", "Santa Clara")
      .writeTextElement("state", "CA")
      .writeTextElement("postalCode", "11111")
  .endDocument()
      
  gs.log(builder.getAttachmentId());
} catch (err) {
  gs.log(err);
} finally {
  builder.close();
}
```

## XMLStreamingAPI - writeNamespace\(String prefix, String namespaceURI\)

Adds a namespace to an element in your XML document.

After calling the startDocument\(\), startElement\(\), or writeTextElement\(\) method, you can call the writeNamespace\(\) method to add a namespace to the associated XML element.

|Name|Type|Description|
|----|----|-----------|
|prefix|String|Prefix for the XML namespace.|
|namespaceURI|String|Optional. URI for the namespace.|

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to add a namespace and URI to the `company` root element, and then assign the prefix to the nested `companyName` element.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('company')
    .writeNamespace('x','https://www.servicenow.com')
        .writeTextElement('companyName', 'ServiceNow')
        .writeNamespace('x')
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - writeNamespaces\(Object namespaceMap\)

Adds namespaces to the root element in your XML document.

After calling the startDocument\(\) or startElement\(\) method, you can call the writeNamespaces\(\) method to declare namespaces for the associated XML element.

<table id="table_z4l_21t_jlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

namespaceMap

</td><td>

Object

</td><td>

Map of keys and values containing namespace prefixes and URIs to associate with the root element of the XML document. For example: ```
{
'namespaceOne':'namespaceValue',
'namespaceTwo':'namespaceValue'
}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

This example adds two namespaces and URIs to the company root element, and then assigns the appropriate prefixes to the nested elements.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('company')
    .writeNamespaces({'x':'https://www.servicenow.com', 'y':'https://www.developer.servicenow.com'})
        .writeTextElement('companyName', 'ServiceNow')
        .writeNamespace('x')
        .writeTextElement('devFramework', 'UI Framework')
        .writeNamespace('y')
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

## XMLStreamingAPI - writeTextElement\(String name, String text, Object prefix\)

Adds a single XML element to your XML document.

After calling the startDocument\(\) method, you can call the writeTextElement\(\) method to add a single XML element to your XML document's structure.

<table id="table_ryd_zkh_dlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Name of the XML element.

</td></tr><tr><td>

text

</td><td>

String

</td><td>

Value for the XML element.

</td></tr><tr><td>

prefix

</td><td>

Object

</td><td>

Optional. Map of prefixes and values associated with the XML element. For example: ```
{
'prefixOne':'prefixValue',
'prefixTwo':'prefixValue'
}
```

You must associate an XML element's prefix with a namespace using [writeNamespace\(\)](XMLStreamingAPIScopedAPI.md#).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

The following example shows how to create an XML document containing three elements with information about an employee.

```
try {
    var ttl = new GlideDateTime('2011-01-01 12:00:00');
    var builder = new sn_ih.XMLStreamingBuilder().withAttachment().expiresAt(ttl);
    var streamingDocument = builder.build();

    streamingDocument.startDocument('Employee')
        .writeTextElement('firstName', 'John')
        .writeTextElement('lastName', 'Smith')
        .writeTextElement('age', '25')
    .endDocument();
    gs.log(streamingDocument.getAttachmentId());
} catch (err) {
    gs.log(err);
} finally {
    streamingDocument.close();
}
```

