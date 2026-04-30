---
title: XMLStreamingBuilder - Scoped
description: Creates a builder object to build a large XML payload for use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as an XML string for a non-streaming option.Instantiates the XMLStreamingBuilder object.Returns an XMLStreamingAPI object.Sets a time when the attachment expires. Must also call the withAttachment\(\) method. Creates an XML document as an attachment and stores it in the Streaming Attachments \[streaming\_attachment\] table. If you don't call this method, the API creates the XML document as a string.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# XMLStreamingBuilder- Scoped

Creates a builder object to build a large XML payload for use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as an XML string for a non-streaming option.

Use these methods in a Workflow Studio Script step with the `sn_ih` namespace identifier. For example, you can use this API to create an XML payload in the Workflow Studio Script step and pass the returned value to the REST step to send the request to a third-party service. For more information, see the Workflow Studio [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

**Note:** You can only use this API within the Workflow Studio environment.

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

## XMLStreamingBuilder - XMLStreamingBuilder\(\)

Instantiates the XMLStreamingBuilder object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

This example shows how to instantiate a `builder` object.

```
var builder = new sn_ih.XMLStreamingBuilder()
```

## XMLStreamingBuilder - build\(\)

Returns an XMLStreamingAPI object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLStreamingAPI|Streaming XML object for constructing the payload.|

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

## XMLStreamingBuilder - expiresAt\(Object expiresAt\)

Sets a time when the attachment expires. Must also call the withAttachment\(\) method.

<table id="table_kc4_25s_jlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

expiresAt

</td><td>

[GlideDateTime](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#)

</td><td>

Object that is set when the attachment expires. -   Minimum value: 7200 seconds, or two hours, from the time the attachment is created. This is the default value if you don't call the expiresAt\(\) method.
-   Maximum value: 172800 seconds, or 48 hours, from the time the attachment is created.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|XMLStreamingBuilder|Builder object used to initiate the XML payload.|

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

## XMLStreamingBuilder - withAttachment\(\)

Creates an XML document as an attachment and stores it in the Streaming Attachments \[streaming\_attachment\] table. If you don't call this method, the API creates the XML document as a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|XMLStreamingBuilder|Builder object used to initiate the XML payload.|

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

This example shows how to build the XML payload and save it as a string.

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

