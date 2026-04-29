---
title: JSONStreamingAPI - Scoped
description: Build a large streaming JSON payload to use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as a JSON string for a non-streaming option.Closes the JSONStreamingAPI object. Must call this method to close the stream after building a JSON object.Ends pretty print JSON formatting.Adds pretty print formatting to a JSON object, or a section of a JSON object.Closes an array within the parent JSON object.Closes an object within the parent JSON object.Returns the sys\_id of the attachment record in the Streaming Attachments \[streaming\_attachment\] table that contains the JSON payload.Returns the JSON object as a string.Opens an array within the parent JSON object.Creates an array within the parent JSON object.Opens an object within the parent JSON object.Adds a Boolean value to the parent JSON object.Adds a Boolean field and value to the parent JSON object.Adds a field name to the parent JSON object.Adds a null value to the parent JSON object.Adds a field with a null value to the parent JSON object.Adds a number field and value to the parent JSON object.Adds a raw value to the parent JSON object.Adds a string value to the parent JSON object.Adds a string field and value to the parent JSON object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# JSONStreamingAPI- Scoped

Build a large streaming JSON payload to use in a REST or SOAP request to send bulk data to a third-party API. You can also create the payload as a JSON string for a non-streaming option.

Use these methods in the Workflow Studio script step with the `sn_ih` namespace identifier. For example, you can use this API to create a JSON payload in the Workflow Studio Script step and pass the returned value to the REST step to send the request to a third-party service. For more information, see the Workflow Studio [Script step](https://www.servicenow.com/docs/access?context=javascript-step-action-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

You can only use this API within the Workflow Studio environment.

To use this class, you must call the build\(\) method in the JSONStreamingBuilder class to return a JSONStreamingAPI object. See [JSONStreamingBuilder - Scoped](../../JSONStreamingBuilder/concept/JSONStreamingBuilderScopedAPI.md#).

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

## Example

This example create a JSON object and stores it in the Attachment \[sys\_attachment\] table with a defined expiration date. You can use this option to create payloads under 5 MB.

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

Alternatively, this example uses the API in the Script step and creates the payload as a JSON string. You can use this option to create payloads under 5 MB.

```
(function execute(inputs, outputs) {

  var builder = new sn_ih.JSONStreamingBuilder().build();
  
  builder.startObject()
    .enablePrettyPrint()
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

## JSONStreamingAPI - close\(\)

Closes the JSONStreamingAPI object. Must call this method to close the stream after building a JSON object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

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

## JSONStreamingAPI - disablePrettyPrint\(\)

Ends pretty print JSON formatting.

Before calling this method, you must first call enablePrettyPrint\(\) to add JSON formatting to a specific section.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

This example adds pretty print formatting to the `address` object.

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.startObject()
    .writeFieldName("firstName")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")  
    .writeNumberField("age","25")
    .enablePrettyPrint()
    .writeFieldName("address")
    .startObject()
    .writeStringField("streetAddress", "21 2nd Street")
    .writeStringField("city", "Santa Clara")
    .writeStringField("state", "CA")
    .writeStringField("postalCode", "11111")
    .endObject()
    .disablePrettyPrint()
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
{"firstName":"John","lastName":"Smith","age":25,
"address" : {
  "streetAddress" : "21 2nd Street",
  "city" : "Santa Clara",
  "state" : "CA",
  "postalCode" : "11111"
},"phoneNumber":[{"type":"home","number":"212 555-1234"},{"type":"fax","number":"646 555-4567"}]}
```

## JSONStreamingAPI - enablePrettyPrint\(\)

Adds pretty print formatting to a JSON object, or a section of a JSON object.

To disable pretty print formatting in a JSON object section, use the disablePrettyPrint\(\) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.enablePrettyPrint()
    .startObject()
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

## JSONStreamingAPI - endArray\(\)

Closes an array within the parent JSON object.

Call the startArray\(\) method first to open the array.

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

## JSONStreamingAPI - endObject\(\)

Closes an object within the parent JSON object.

Call the startObject\(\) method first to open the object.

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

## JSONStreamingAPI - getAttachmentId\(\)

Returns the sys\_id of the attachment record in the Streaming Attachments \[streaming\_attachment\] table that contains the JSON payload.

You must call the withAttachment\(\) method in the JSONStreamingBuilder class to save the JSON payload as an attachment before calling this method. See [JSONStreamingBuilder - Scoped](../../JSONStreamingBuilder/concept/JSONStreamingBuilderScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the attachment record in the Streaming Attachments \[streaming\_attachment\] table that contains the JSON payload.|

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

## JSONStreamingAPI - getJSONString\(\)

Returns the JSON object as a string.

To return the JSON object as a string, do not call the withAttachment\(\) method in the JSONStreamingBuilder class. See [JSONStreamingBuilder - Scoped](../../JSONStreamingBuilder/concept/JSONStreamingBuilderScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Contains the JSON object built using the JSONStreamingAPI.|

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

## JSONStreamingAPI - startArray\(\)

Opens an array within the parent JSON object.

Include the endArray\(\) method to close the array.

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

## JSONStreamingAPI - startArrayField\(String fieldName\)

Creates an array within the parent JSON object.

Surround this method with the startArray\(\) and endArray\(\) methods to open and close the array.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the array.|

|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

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
    .startArrayField("phoneNumber")
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

## JSONStreamingAPI - startObject\(\)

Opens an object within the parent JSON object.

Requires the endObject\(\) method to close the object.

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

## JSONStreamingAPI - writeBoolean\(Boolean state\)

Adds a Boolean value to the parent JSON object.

<table id="table_abc_4f2_1lb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

state

</td><td>

Boolean

</td><td>

The boolean value to add to the parent JSON object.Valid values:

-   true
-   false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.startObject()
    .writeFieldName("firstName")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")
    .writeFieldName("activeUser")
    .writeBoolean(true)
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

## JSONStreamingAPI - writeBooleanField\(String fieldName, Boolean value\)

Adds a Boolean field and value to the parent JSON object.

<table id="table_qtm_dh2_1lb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fieldName

</td><td>

String

</td><td>

The name of the field to add to the parent JSON object.

</td></tr><tr><td>

value

</td><td>

Boolean

</td><td>

The boolean value to add to the parent JSON object.Valid values:

-   true
-   false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.startObject()
    .writeFieldName("firstName")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")
    .writeBooleanField("activeUser", true)
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

## JSONStreamingAPI - writeFieldName\(String name\)

Adds a field name to the parent JSON object.

|Name|Type|Description|
|----|----|-----------|
|name|String|Field name to add to the parent JSON object.|

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

## JSONStreamingAPI - writeNull\(\)

Adds a null value to the parent JSON object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.startObject()
    .writeFieldName("firstName")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")
    .writeFieldName("activeUser")
    .writeNull()
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

## JSONStreamingAPI - writeNullField\(String fieldName\)

Adds a field with a null value to the parent JSON object.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the null field.|

|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.startObject()
    .writeFieldName("firstName")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")
    .writeNullField("activeUser")
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

## JSONStreamingAPI - writeNumberField\(String fieldName, String encodedValue\)

Adds a number field and value to the parent JSON object.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the number field.|
|encodedValue|String|The value of the number field.|

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

## JSONStreamingAPI - writeRaw\(String text\)

Adds a raw value to the parent JSON object.

|Name|Type|Description|
|----|----|-----------|
|text|String|Raw text to add to the parent JSON object.|

|Type|Description|
|----|-----------|
|JSONStreamingAPI|Streaming JSON object used to construct the payload.|

```
try {
  var builder = new sn_ih.JSONStreamingBuilder().build();

  builder.startObject()
    .writeFieldName("firstName")
    .writeString("John")
    .writeFieldName("lastName")
    .writeString("Smith")
    .writeFieldName("filePath")
    .writeRaw("C:\Users\profile\aboutme.html")
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

## JSONStreamingAPI - writeString\(String text\)

Adds a string value to the parent JSON object.

|Name|Type|Description|
|----|----|-----------|
|text|String|The string value to add to the parent JSON object.|

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

## JSONStreamingAPI - writeStringField\(String fieldName, String value\)

Adds a string field and value to the parent JSON object.

|Name|Type|Description|
|----|----|-----------|
|fieldName|String|The name of the field to add to the parent JSON object.|
|value|String|The value of the field.|

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

