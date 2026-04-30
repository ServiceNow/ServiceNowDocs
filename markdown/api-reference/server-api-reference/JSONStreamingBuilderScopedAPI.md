---
title: JSONStreamingBuilder - Scoped
description: Create a builder object used to build a large streaming JSON payload to use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as a JSON string for a non-streaming option.Instantiates the JSONStreamingBuilder object.Returns a JSONStreamingAPI object.Sets a time when the attachment expires. Must also call the withAttachment\(\) method. If you do not call this method, the attachment expires two hours from the time the attachment is created.Creates the JSON object as a streaming attachment and stores it in the Streaming Attachments \[streaming\_attachment\] table. If you do not call this method, the API creates the payload as a JSON string.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# JSONStreamingBuilder- Scoped

Create a builder object used to build a large streaming JSON payload to use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as a JSON string for a non-streaming option.

Use these methods in the Workflow Studio script step with the `sn_ih` namespace identifier. For example, you can use this API to create a JSON payload in the Workflow Studio Script step and pass the returned value to the REST step to send the request to a third-party service. For more information, see the Workflow Studio [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

You can only use this API within the Workflow Studio environment.

## API call order

Generate JSON payloads using these APIs in the following order:

-   **JSONStreamingBuilder: Creates a builder object**

    Use these methods in the following order to create a builder object:

    1.  JSONStreamingBuilder\(\): Instantiates the JSONStreamingBuilder object.
    2.  withAttachment\(\): Optional. Creates the JSON object as a streaming attachment and stores it in the Streaming Attachments \[streaming\_attachment\] table. If you do not call this method, the API creates the payload as a JSON string.
    3.  expiresAt\(\): Optional. Sets a time when the attachment expires. Must also call the withAttachment\(\) method.
    4.  build\(\): Returns a JSONStreamingAPI object.
-   **JSONStreamingAPI: Builds the JSON payload**

    Use these methods in the following order to create the JSON payload:

    1.  startObject\(\): Creates the parent JSON object.
    2.  Methods to generate the JSON key-value pairs, such as writeFieldName\(\), writeString\(\), and writeNumberField\(\).
    3.  endObject\(\): Closes the parent JSON object.
    4.  getJSONString\(\) or getAttachmentId\(\): Returns the JSON string or attachment ID that you created.
    5.  close\(\): Closes the JSONStreamingAPI object.

## Size limits

Payloads generated through this API cannot exceed these size limits:

-   Attachments: 200 MB
-   Strings: 5 MB

## Examples

This example shows how to create a JSON object and store it in the Attachment \[sys\_attachment\] table with a defined expiration date.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.JSONStreamingBuilder()
    .withAttachment() // Creates the JSON object in streaming mode within an attachment.
    .expiresAt(ttl) // Sets an expiration date for the attachment.
    .build(); // Creates the JSONStreamingAPI object. 

  builder.startObject()  // Begins generating the JSON object.
	.writeFieldName("firstName")  // Adds a "firstName" field 
	.writeString("John")          // Writes the value of the "firstName" field
	.writeFieldName("lastName")
	.writeString("Smith")
	.writeNumberField("age","25") // Write a number field named "age" with value "25"
	.writeFieldName("address")
	.startObject()                // Start a new object nested under the parent object
		.writeStringField("streetAddress", "21 2nd Street")
		.writeStringField("city", "Santa Clara")
		.writeStringField("state", "CA")
		.writeStringField("postalCode", "11111")
	.endObject()
	.writeFieldName("phoneNumber")
	.startArray()                    // Start an array 
		.startObject()               // Add the first object to the array 
			.writeFieldName("type")
			.writeString("home")
			.writeFieldName("number")
			.writeString("212 555-1234")
		.endObject()
		.startObject()               // Add another object to the array 
			.writeFieldName("type")
			.writeString("fax")
			.writeFieldName("number")
			.writeString("646 555-4567")
		.endObject()
	.endArray()
	.endObject()

  gs.log(builder.getAttachmentId()); // Returns the sys_id of the attachment.
} 

catch (err) {
  gs.log(err);
} 

finally {
  builder.close();
}
```

Alternatively, this example shows how to use the API in the Script step and create the payload as a JSON string. You can use this option to create payloads under 5 MB.

```
(function execute(inputs, outputs) {

  var builder = new sn_ih.JSONStreamingBuilder().build();
  
  builder.startObject()
    .enablePrettyPrint()
    .writeTextElement("firstName","John")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")
    .writeNumberField("age","25")
    .writeFieldName("address")
    .startObject()
      .writeStringField("streetAddress", "21 2nd Street")
      .writeStringField("city", "Santa Clara")
      .writeStringField("state", "CA")
      .writeStringField("postalCode", "11111")
    .endObject()
    .writeFieldName("phoneNumber")
    .startArray()
      .startObject()
        .writeFieldName("type")
        .writeString("home")
        .writeFieldName("number")
        .writeString("212 555-1234")
      .endObject()
      .startObject()
        .writeFieldName("type")
        .writeString("fax")
        .writeFieldName("number")
        .writeString("646 555-4567")
      .endObject()
    .endArray()
    .endObject()

  outputs.payload = builder.getJSONString();
  
})(inputs, outputs);
```

Output:

```
{
"firstName" : "John",
"lastName" : "Smith",
"age" : 25,
"address" : {
  "streetAddress" : "21 2nd Street",
  "city" : "Santa Clara",
  "state" : "CA",
  "postalCode" : "11111"
},
"phoneNumber" : [ {
  "type" : "home",
  "number" : "212 555-1234"
}, {
  "type" : "fax",
  "number" : "646 555-4567"
} ]
}
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## JSONStreamingBuilder - JSONStreamingBuilder\(\)

Instantiates the JSONStreamingBuilder object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var builder = new sn_ih.JSONStreamingBuilder()
```

## JSONStreamingBuilder - build\(\)

Returns a JSONStreamingAPI object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

This example shows how to create a JSON object and store it in the Attachment \[sys\_attachment\] table with a defined expiration date.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.JSONStreamingBuilder()
    .withAttachment() // Creates the JSON object in streaming mode within an attachment.
    .expiresAt(ttl) // Sets an expiration date for the attachment.
    .build(); // Creates the JSONStreamingAPI object. 

  builder.startObject()  // Begins generating the JSON object.
	.writeFieldName("firstName")  // Adds a "firstName" field 
	.writeString("John")          // Writes the value of the "firstName" field
	.writeFieldName("lastName")
	.writeString("Smith")
	.writeNumberField("age","25") // Write a number field named "age" with value "25"
	.writeFieldName("address")
	.startObject()                // Start a new object nested under the parent object
		.writeStringField("streetAddress", "21 2nd Street")
		.writeStringField("city", "Santa Clara")
		.writeStringField("state", "CA")
		.writeStringField("postalCode", "11111")
	.endObject()
	.writeFieldName("phoneNumber")
	.startArray()                    // Start an array 
		.startObject()               // Add the first object to the array 
			.writeFieldName("type")
			.writeString("home")
			.writeFieldName("number")
			.writeString("212 555-1234")
		.endObject()
		.startObject()               // Add another object to the array 
			.writeFieldName("type")
			.writeString("fax")
			.writeFieldName("number")
			.writeString("646 555-4567")
		.endObject()
	.endArray()
	.endObject()

  gs.log(builder.getAttachmentId()); // Returns the sys_id of the attachment.
} 

catch (err) {
  gs.log(err);
} 

finally {
  builder.close();
}
```

## JSONStreamingBuilder - expiresAt\(Object expiresAt\)

Sets a time when the attachment expires. Must also call the withAttachment\(\) method. If you do not call this method, the attachment expires two hours from the time the attachment is created.

<table id="table_wlk_hzt_hlb" class="parameters"><thead><tr><th>

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

Object that is set when the attachment expires. -   Minimum value: 7200 seconds, or two hours, from the time the attachment is created. Default.
-   Maximum value: 172800 seconds, or 48 hours, from the time the attachment is created.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|JSONStreamingBuilder|Builder object used to initiate the JSON payload.|

This example shows how to create a JSON object and store it in the Attachment \[sys\_attachment\] table with a defined expiration date.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.JSONStreamingBuilder()
    .withAttachment() // Creates the JSON object in streaming mode within an attachment.
    .expiresAt(ttl) // Sets an expiration date for the attachment.
    .build(); // Creates the JSONStreamingAPI object. 

  builder.startObject()  // Begins generating the JSON object.
	.writeFieldName("firstName")  // Adds a "firstName" field 
	.writeString("John")          // Writes the value of the "firstName" field
	.writeFieldName("lastName")
	.writeString("Smith")
	.writeNumberField("age","25") // Write a number field named "age" with value "25"
	.writeFieldName("address")
	.startObject()                // Start a new object nested under the parent object
		.writeStringField("streetAddress", "21 2nd Street")
		.writeStringField("city", "Santa Clara")
		.writeStringField("state", "CA")
		.writeStringField("postalCode", "11111")
	.endObject()
	.writeFieldName("phoneNumber")
	.startArray()                    // Start an array 
		.startObject()               // Add the first object to the array 
			.writeFieldName("type")
			.writeString("home")
			.writeFieldName("number")
			.writeString("212 555-1234")
		.endObject()
		.startObject()               // Add another object to the array 
			.writeFieldName("type")
			.writeString("fax")
			.writeFieldName("number")
			.writeString("646 555-4567")
		.endObject()
	.endArray()
	.endObject()

  gs.log(builder.getAttachmentId()); // Returns the sys_id of the attachment.
} 

catch (err) {
  gs.log(err);
} 

finally {
  builder.close();
}
```

## JSONStreamingBuilder - withAttachment\(\)

Creates the JSON object as a streaming attachment and stores it in the Streaming Attachments \[streaming\_attachment\] table. If you do not call this method, the API creates the payload as a JSON string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JSONStreamingBuilder|Builder object used to initiate the JSON payload.|

This example shows how to build the JSON payload and save it as an attachment.

```
try {
  var ttl = new GlideDateTime("2011-01-01 12:00:00");
  var builder = new sn_ih.JSONStreamingBuilder()
    .withAttachment() // Creates the JSON object in streaming mode within an attachment.
    .expiresAt(ttl) // Sets an expiration date for the attachment.
    .build(); // Creates the JSONStreamingAPI object. 

  builder.startObject()  // Begins generating the JSON object.
	.writeFieldName("firstName")  // Adds a "firstName" field 
	.writeString("John")          // Writes the value of the "firstName" field
	.writeFieldName("lastName")
	.writeString("Smith")
	.writeNumberField("age","25") // Write a number field named "age" with value "25"
	.writeFieldName("address")
	.startObject()                // Start a new object nested under the parent object
		.writeStringField("streetAddress", "21 2nd Street")
		.writeStringField("city", "Santa Clara")
		.writeStringField("state", "CA")
		.writeStringField("postalCode", "11111")
	.endObject()
	.writeFieldName("phoneNumber")
	.startArray()                    // Start an array 
		.startObject()               // Add the first object to the array 
			.writeFieldName("type")
			.writeString("home")
			.writeFieldName("number")
			.writeString("212 555-1234")
		.endObject()
		.startObject()               // Add another object to the array 
			.writeFieldName("type")
			.writeString("fax")
			.writeFieldName("number")
			.writeString("646 555-4567")
		.endObject()
	.endArray()
	.endObject()

  gs.log(builder.getAttachmentId()); // Returns the sys_id of the attachment.
} 

catch (err) {
  gs.log(err);
} 

finally {
  builder.close();
}
```

This example shows how to build the JSON payload and save it as a string.

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.startObject()
    .writeFieldName("firstName")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")
    .writeNumberField("age","25")
    .writeFieldName("address")
    .startObject()
    .writeStringField("streetAddress", "21 2nd Street")
    .writeStringField("city", "Santa Clara")
    .writeStringField("state", "CA")
    .writeStringField("postalCode", "11111")
    .endObject()
    .writeFieldName("phoneNumber")
    .startArray()
    .startObject()
    .writeFieldName("type")
    .writeString("home")
    .writeFieldName("number")
    .writeString("212 555-1234")
    .endObject()
    .startObject()
    .writeFieldName("type")
    .writeString("fax")
    .writeFieldName("number")
    .writeString("646 555-4567")
    .endObject()
    .endArray()
    .endObject()

  gs.log(builder.getJSONString());
} 

catch (err) {
  gs.log("Exception: " + err);
} 

finally {
  builder.close();
}
```

Output:

```
{
"firstName" : "John",
"lastName" : "Smith",
"age" : 25,
"address" : {
  "streetAddress" : "21 2nd Street",
  "city" : "Santa Clara",
  "state" : "CA",
  "postalCode" : "11111"
},
"phoneNumber" : [ {
  "type" : "home",
  "number" : "212 555-1234"
}, {
  "type" : "fax",
  "number" : "646 555-4567"
} ]
}
```

