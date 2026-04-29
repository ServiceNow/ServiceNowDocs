---
title: GlideSysAttachment - Global
description: The GlideSysAttachment API provides methods for handling attachments.Creates an instance of the GlideSysAttachment class.Adds a single attribute to an existing attachment record.Adds multiple attributes to an attachment record.Copies attachments from the source record to the target record.Deletes all attributes from an existing attachment record.Deletes the specified attachment.Deletes a specified attribute from attachment record.Fetches all attributes from a specified attachment record.Fetches a specified attribute from an attachment record.Returns a GlideRecord containing the matching attachment metadata such as name, type, or size.Returns a GlideScriptableInputStream object given the sys\_id of an attachment.Updates all the attributes for an existing attachment record.Updates a single attribute for an existing attachment record.Attaches a specified attachment to the specified record.Inserts an attachment using the input stream.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSysAttachment- Global

The GlideSysAttachment API provides methods for handling attachments.

Content is returned as a GlideScriptableInputStream object when getContentStream\(\) is called. The GlideScriptableInputStream contains the actual bytes not converted into a string.

## Encryption API scope restriction

Methods that manage encryption contexts, cryptographic modules, or encryption state are available only in the global application. These APIs are intentionally restricted because they modify platform‑level security configuration.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSysAttachment - GlideSysAttachment\(\)

Creates an instance of the GlideSysAttachment class.

**Note:** This constructor does not take a parameter unless managing attachment attributes.

Use the following methods for managing attachment attributes:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

<table id="table_iys_ctb_fv" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

idAttachmentAttributes

</td><td>

String

</td><td>

This parameter is only used when handling attachment attributes, otherwise leave empty. Sys\_id of an attachment with attributes.Table: Attachments \[sys\_attachment\]

</td></tr></tbody>
</table>The following script lists attachment file names for a record with two attachments.

```
var attachment = new GlideSysAttachment();

var agr = attachment.getAttachments('<table_name>', '<record_sys_id>');

while(agr.next())
gs.info(agr.getValue('file_name'));
```

Output:

```
*** Script: filename1.txt
*** Script: filename2.txt
```

The following example shows how to get all attributes assigned to a specified attachment.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");

var result = attach.fetchAllAttributes();

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + ", Value: " + result.getValue('value')); 
}
```

Output:

```
Key: title, Value: Add multiple attributes to an attachment
Key: author, Value: Abel Tuter
Key: category, Value: KB
Key: length, Value: 5000
```

## GlideSysAttachment - addAttribute\(String attrKey, String attrValue\)

Adds a single attribute to an existing attachment record.

See also:

-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - addAttribute\(String sysAttachmentID, String attrKey, String attrValue\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|attrKey|String|Key portion of a key-value pair for an attachment attribute.|
|attrValue|String|Value portion of a key-value pair for an attachment attribute.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add an attribute to a specified attachment with the key `author` and value `Fred Luddy`. The results can be viewed in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");
attach.addAttribute("author", "Fred Luddy");

var result = attach.fetchAttribute("author");

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + " \nValue: " + result.getValue('value')); 
}
```

Output:

```
Key: author 
Value: Fred Luddy
```

## GlideSysAttachment - addMultipleAttributes\(Object attrsKeyValuePair\)

Adds multiple attributes to an attachment record.

See also:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - addMultipleAttributes\(String sysAttachmentID, Object attrsKeyValuePair\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

<table id="table_rql_3mg_5fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attrsKeyValuePair

</td><td>

Object

</td><td>

Attachment attributes in a set of key-value pairs. Each attribute key and its value must be provided as a string.For example:

```
var attachmentAttributes = { 
    "description" : "Photo of the solar system",
    "dimensions" : "1600 x 300"
}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to add attributes to a specified attachment. The results can also be verified in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");

var attrsKeyValuePair = { };
  attrsKeyValuePair["title"]  = "Add multiple attributes to an attachment";
  attrsKeyValuePair["category"] =  "KB";
  attrsKeyValuePair["length"] =  "5000";

attach.addMultipleAttributes(attrsKeyValuePair);

var result = attach.fetchAllAttributes();

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + ", Value: " + result.getValue('value'));
}
```

Output:

```
Key: title, Value: Add multiple attributes to an attachment
Key: author, Value: Abel Tuter
Key: category, Value: KB
Key: length, Value: 5000
```

## GlideSysAttachment - copy\(String sourceTable, String sourceID, String targetTable, String targetID\)

Copies attachments from the source record to the target record.

**Note:** Copying an attachment also copies any attributes assigned to it. You can view a list of assigned attributes in the Attachment Attributes \[sys\_attachment\_list\] table, or run the fetchAllAttributes\(\) method.

|Name|Type|Description|
|----|----|-----------|
|sourceTable|String|Name of the table with the attachments to be copied.|
|sourceID|String|Source table's sys\_id.|
|targetTable|String|Name of the table on which to add the attachments.|
|targetID|String|The sys\_id of the record in the target table on which to copy the attachment.|

<table id="id_afm_yjz_g5b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Array of sys\_ids of the attachments that were copied.Table: Attachments \[sys\_attachment\]

</td></tr></tbody>
</table>This example shows how to copy attachments from an incident record to a problem record.

```
var attachment = new GlideSysAttachment();
var incidentSysID = 'ab1b30031b04ec101363ff37dc4bcbfc';
var incGR = new GlideRecord('incident');
incGR.get(incidentSysID);

var copiedAttachments = attachment.copy('incident', incidentSysID, 'problem', incGR.getValue('problem_id'));
gs.info('Copied attachments: ' + copiedAttachments);
```

Output:

```
Copied attachments: 6e4621df1bc420501363ff37dc4bcbb0,a87769531b0820501363ff37dc4bcba2
```

## GlideSysAttachment - deleteAllAttributes\(\)

Deletes all attributes from an existing attachment record.

See also:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - deleteAllAttributes\(String sysAttachmentID\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_sql_3mg_5fc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the attributes were successfully deleted.Valid values:

-   true: The attributes were successfully deleted.
-   false: The attributes were not successfully deleted.

</td></tr></tbody>
</table>The following example shows how to delete all attributes assigned to a specified attachment. The results can also be verified in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");

attach.deleteAllAttributes();

var result = attach.fetchAllAttributes();

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + ", Value: " + result.getValue('value')); 
}
```

Output:

```
Attribute "null" not found for attachment "04f48541083e2e50f877df7a115e31f3"

```

## GlideSysAttachment - deleteAttachment\(String attachmentID\)

Deletes the specified attachment.

**Note:** Deleting an attachment also deletes any attributes assigned to it. You can view a list of assigned attributes in the Attachment Attributes \[sys\_attachment\] table, or run the fetchAllAttributes\(\) method.

<table id="id_ywb_ykz_g5b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attachmentID

</td><td>

String

</td><td>

Attachment's sys\_id.Table: Attachments \[sys\_attachment\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var attachment = new GlideSysAttachment();
var attachmentSysID = 'a87769531b0820501363ff37dc4bcba2';
attachment.deleteAttachment(attachmentSysID);
```

## GlideSysAttachment - deleteAttribute\(String attrKey\)

Deletes a specified attribute from attachment record.

See also:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - deleteAllAttributes\(String sysAttachmentID\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|attrKey|String|Key portion of a key-value pair for an attachment attribute.|

<table id="table_sql_3mg_5fc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the attachment attribute was successfully deleted.Valid values:

-   true: The attachment attribute was successfully deleted.
-   false: The attachment attribute was not successfully deleted.

</td></tr></tbody>
</table>The following example shows how to delete an attribute assigned to a specified attachment with the key `author`. The results can also be verified in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3v");

attach.deleteAttribute("author");

var result = attach.fetchAttribute("author");

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + " \nValue: " + result.getValue('value')); 
}
```

Output:

```
Attribute "author" not found for attachment "04f48541083e2e50f877df7a115e31f3"
```

## GlideSysAttachment - fetchAllAttributes\(\)

Fetches all attributes from a specified attachment record.

See also:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - fetchAllAttributes\(String sysAttachmentID\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|The attachment record and all of its attributes.|

The following example shows how to get all attributes assigned to a specified attachment.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");

var result = attach.fetchAllAttributes();

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + ", Value: " + result.getValue('value')); 
}
```

Output:

```
Key: title, Value: Add multiple attributes to an attachment
Key: author, Value: Abel Tuter
Key: category, Value: KB
Key: length, Value: 5000
```

## GlideSysAttachment - fetchAttribute\(String attrKey\)

Fetches a specified attribute from an attachment record.

See also:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - fetchAttribute\(String sysAttachmentID, String attrKey\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|attrKey|String|Key portion of a key-value pair for an attachment attribute.|

|Type|Description|
|----|-----------|
|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|The GlideRecord of the attachment and the specified attribute.|

The following example shows how to get an attachment attribute with the key `author`.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");

var result = attach.fetchAttribute("author");

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + " \nValue: " + result.getValue('value')); 
}
```

Output:

```
Key: author 
Value: Abel Tuter
```

## GlideSysAttachment - getAttachments\(String tableName, String sys\_id\)

Returns a GlideRecord containing the matching attachment metadata such as name, type, or size.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table to which the attachment belongs; for example, incident.|
|sys\_id|String|Sys\_id of record to which the attachment belongs.|

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord object containing the matching attachment metadata such as name, type, or size.|

The following script lists attachment file names for a record with two attachments.

```
var attachment = new GlideSysAttachment();

var agr = attachment.getAttachments('<table_name>', '<record_sys_id>');

while(agr.next())
gs.info(agr.getValue('file_name'));
```

Output:

```
*** Script: filename1.txt
*** Script: filename2.txt
```

## GlideSysAttachment - getContentStream\(String sysID\)

Returns a GlideScriptableInputStream object given the sys\_id of an attachment.

You can use the [GlideTextReader](../../GlideTextReaderScoped/concept/c_GlideTextReaderScopedAPI.md#) API to read the content stream.

|Name|Type|Description|
|----|----|-----------|
|sysID|String|Attachment sys\_id.|

|Type|Description|
|----|-----------|
|GlideScriptableInputStream|Stream that contains the attachment content.|

```
var attachment = new GlideSysAttachment();
var attachmentSysID = '6e4621df1bc420501363ff37dc4bcbb0';
var attachmentContentStream = attachment.getContentStream(attachmentSysID);
gs.info('Attachment content stream: ' + attachmentContentStream);
```

Output:

```
Attachment content stream: com.glide.communications.GlideScriptableInputStream@14bd299
```

## GlideSysAttachment - updateAllAttributes\(Object attrsKeyValuePair\)

Updates all the attributes for an existing attachment record.

See also:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - updateAllAttributes\(String sysAttachmentID, Object attrsKeyValuePair\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

<table id="table_rql_3mg_5fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

attrsKeyValuePair

</td><td>

Object

</td><td>

Attachment attributes in a set of key-value pairs. Each attribute key and its value must be provided as a string.For example:

```
var attachmentAttributes = { 
    "description" : "Photo of the solar system",
    "dimensions" : "1600 x 300"
}
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to update each attribute for a specified attachment. The results can also be verified in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");

var attachmentAttributes = {
    "category" : "Training",
    "title" : "Updating attachment attributes", 
    "author" : "Abraham Lincoln",
    "length" : "6000"
}

attach.updateAllAttributes(attachmentAttributes);

var result = attach.fetchAllAttributes();

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + ", Value: " + result.getValue('value'));
}
```

Output:

```
Key: title, Value: Updating attachment attributes
Key: author, Value: Abraham Lincoln
Key: category, Value: Training
Key: length, Value: 6000
```

## GlideSysAttachment - updateAttribute\(String attrKey, String attrValue\)

Updates a single attribute for an existing attachment record.

See also:

-   [addAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [addMultipleAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [deleteAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [fetchAttribute\(\)](GlideSysAttachmentGlobalAPI.md#)
-   [updateAllAttributes\(\)](GlideSysAttachmentGlobalAPI.md#)

For the scoped equivalent of this method, use [Scoped GlideSysAttachment - updateAttribute\(String sysAttachmentID, String attrKey, String attrValue\)](../../GlideSysAttachmentScoped/concept/c_GlideSysAttachmentScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|attrKey|String|Key portion of a key-value pair for an attachment attribute.|
|attrValue|String|Value portion of a key-value pair for an attachment attribute.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to update an attribute assigned to a specified attachment with the key `author` and changes the value to Abel Tuter. The results can also be verified in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment("04f48541083e2e50f877df7a115e31f3");

var originalVal = attach.fetchAttribute("author");
while(originalVal.next()) {
   gs.info("Original attribute value: " + originalVal.getValue('value') + "\n"); 
}

attach.updateAttribute("author", "Abel Tuter");

var updatedVal = attach.fetchAttribute("author"); 
while(updatedVal.next()) {
   gs.info("Updated attribute value: " + updatedVal.getValue('value')); 
}
```

Output:

```
Original attribute value: Fred Luddy

Updated attribute value: Abel Tuter
```

## GlideSysAttachment - write\(GlideRecord record, String fileName, String contentType, String content\)

Attaches a specified attachment to the specified record.

|Name|Type|Description|
|----|----|-----------|
|record|GlideRecord|Record to which to attach the attachment.|
|fileName|String|Attachment file name.|
|contentType|String|MIME type of the attachment, such as `image/png`. Located in the Attachment \[sys\_attachment\] table in the **Content type** field.|
|content|String|Attachment content.|

|Type|Description|
|----|-----------|
|String|Attachment sys\_id. Returns null if the attachment was not added.|

```
var attachment = new GlideSysAttachment();

//set up inputs
var rec = new GlideRecord('incident');
rec.get('78271e1347c12200e0ef563dbb9a7109');
var fileName = 'example.txt';
var contentType = 'text/csv';
var content = 'The text that is stored inside my file';

var agr = attachment.write(rec, fileName, contentType, content);

gs.info('The attachment sys_id is: ' + agr);
```

Output:

```
The attachment sys_id is: 01271e4317c13311e0ef563dbb9abe34
```

## GlideSysAttachment - writeContentStream\(GlideRecord now\_GR, String fileName, String contentType, GlideScriptableInputStream inputStream\)

Inserts an attachment using the input stream.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|Record to which to attach the attachment.|
|fileName|String|Attachment file name.|
|contentType|String|MIME type of the attachment, such as `image/png`. Located in the Attachment \[sys\_attachment\] table in the **Content type** field.|
|content|GlideScriptableInputStream|Attachment content.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the attachment created.|

Attaches a content stream from the sys\_attachment table to a test\_table record.

```
function copyAttachmentToGlideRecord(conceptSysId) {

  // Get record from test_table using sys_id
  var targetGlideRecord = new GlideRecord("test_table");
  if (!targetGlideRecord.get(conceptSysId)) {
     throw ("Cannot find record created by test with sys_id: " + conceptSysId);
  }

  // Get record from sys_attachment table
  var sourceAttachmentGlideRecord = new GlideRecord('sys_attachment');    
  sourceAttachmentGlideRecord.query();
  sourceAttachmentGlideRecord.next();

  // Get field values from retrieved sys_attachment record
  var fileName = sourceAttachmentGlideRecord.getValue('file_name');
  var contentType = sourceAttachmentGlideRecord.getValue('content_type');
  var sourceAttachmentSysId = sourceAttachmentGlideRecord.getValue('sys_id');

  // Attach sys_attachment record content stream to test_table record
  var gsa = new GlideSysAttachment();
  gsa.writeContentStream(
    targetGlideRecord,
    fileName,
    contentType,
    gsa.getContentStream(sourceAttachmentSysId));
  gs.info("Attachment created");
}
```

