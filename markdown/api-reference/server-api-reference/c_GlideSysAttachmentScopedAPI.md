---
title: GlideSysAttachment - Scoped
description: The GlideSysAttachment API provides methods to handle attachments.Creates an instance of the GlideSysAttachment class.Adds a single attribute to an existing attachment record.Adds multiple attributes to an attachment record.Copies attachments from the source record to the target record.Deletes all attributes from an existing attachment record.Deletes the specified attachment.Deletes a specified attribute from attachment record.Fetches all attributes from a specified attachment record.Fetches a specified attribute from an attachment record.Returns a GlideRecord containing the matching attachment metadata such as name, type, or size.Returns the attachment content as a string.Returns the attachment content as a string with base64 encoding.Returns a GlideScriptableInputStream object given the sys\_id of an attachment.Updates all the attributes for an existing attachment record.Updates a single attribute for an existing attachment record.Attaches a specified attachment to the specified record.Inserts an attachment for the specified record using base64 encoded content.Inserts an attachment using the input stream.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSysAttachment- Scoped

The GlideSysAttachment API provides methods to handle attachments.

Content is returned as a string, not as a byte array when getContent\(\) is called.

Content is returned as a GlideScriptableInputStream object when getContentStream\(\) is called. The GlideScriptableInputStream contains the actual bytes not converted into a string.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideSysAttachment - GlideSysAttachment\(\)

Creates an instance of the GlideSysAttachment class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## Scoped GlideSysAttachment - addAttribute\(String sysAttachmentID, String attrKey, String attrValue\)

Adds a single attribute to an existing attachment record.

See also:

-   [addMultipleAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - addAttribute\(String attrKey, String attrValue\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|sysAttachmentID|String|Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.|
|attrKey|String|Key portion of a key-value pair for an attachment attribute.|
|attrValue|String|Value portion of a key-value pair for an attachment attribute.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add an attribute to a specified attachment with the key `author` and value `Fred Luddy`. The results can be viewed in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment();
attach.addAttribute("9e1b714601932210f877b455304df0af", "author", "Fred Luddy");

var result = attach.fetchAttribute("9e1b714601932210f877b455304df0af", "author");

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + " \nValue: " + result.getValue('value')); 
}
```

Output:

```
Key: author 
Value: Fred Luddy
```

## Scoped GlideSysAttachment - addMultipleAttributes\(String sysAttachmentID, Object attrsKeyValuePair\)

Adds multiple attributes to an attachment record.

See also:

-   [addAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - addMultipleAttributes\(Object attrsKeyValuePair\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

<table id="table_rql_3mg_5fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysAttachmentID

</td><td>

String

</td><td>

Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

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
var attach = new GlideSysAttachment();

var attachmentID = '9e1b714601932210f877b455304df0af';

var attrsKeyValuePair = { };
  attrsKeyValuePair["title"]  = "Add multiple attributes to an attachment";
  attrsKeyValuePair["category"] =  "KB";
  attrsKeyValuePair["length"] =  "5000";

attach.addMultipleAttributes(attachmentID, attrsKeyValuePair);

var result = attach.fetchAllAttributes(attachmentID);

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

## Scoped GlideSysAttachment - copy\(String sourceTable, String sourceID, String targetTable, String targetID\)

Copies attachments from the source record to the target record.

**Note:** Copying an attachment also copies any attributes assigned to it. You can view a list of assigned attributes in the Attachment Attributes \[sys\_attachment\_list\] table, or run the fetchAllAttributes\(\) method.

|Name|Type|Description|
|----|----|-----------|
|sourceTable|String|Name of the table with the attachments to be copied.|
|sourceID|String|Source table's sys\_id.|
|targetTable|String|Name of the table on which to add the attachments.|
|targetID|String|The sys\_id of the record in the target table on which to copy the attachment.|

<table id="id_db3_wjz_g5b" class="returns"><thead><tr><th>

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

## Scoped GlideSysAttachment - deleteAllAttributes\(String sysAttachmentID\)

Deletes all attributes from an existing attachment record.

See also:

-   [addAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [addMultipleAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - deleteAllAttributes\(\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|sysAttachmentID|String|Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.|

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
var attach = new GlideSysAttachment();

var attachmentID = '9e1b714601932210f877b455304df0af';

attach.deleteAllAttributes(attachmentID);

var result = attach.fetchAllAttributes(attachmentID);

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + ", Value: " + result.getValue('value')); 
}
```

Output:

```
Attribute "null" not found for attachment "04f48541083e2e50f877df7a115e31f3"

```

## Scoped GlideSysAttachment - deleteAttachment\(String attachmentID\)

Deletes the specified attachment.

**Note:** Deleting an attachment also deletes any attributes assigned to it. You can view a list of assigned attributes in the Attachment Attributes \[sys\_attachment\] table, or run the fetchAllAttributes\(\) method.

<table id="id_ajy_dlz_g5b" class="parameters"><thead><tr><th>

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
|void| |

```
var attachment = new GlideSysAttachment();
var attachmentSysID = 'a87769531b0820501363ff37dc4bcba2';
attachment.deleteAttachment(attachmentSysID);
```

## Scoped GlideSysAttachment - deleteAttribute\(String sysAttachmentID, String attrKey\)

Deletes a specified attribute from attachment record.

See also:

-   [addAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [addMultipleAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - deleteAttribute\(String attrKey\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|sysAttachmentID|String|Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.|
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
var attach = new GlideSysAttachment();

var attachmentID = '9e1b714601932210f877b455304df0af';

attach.deleteAttribute(attachmentID, "author");

var result = attach.fetchAttribute(attachmentID, "author");

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + " \nValue: " + result.getValue('value')); 
}
```

Output:

```
Attribute "author" not found for attachment "04f48541083e2e50f877df7a115e31f3"
```

## Scoped GlideSysAttachment - fetchAllAttributes\(String sysAttachmentID\)

Fetches all attributes from a specified attachment record.

See also:

-   [addAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [addMultipleAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - fetchAllAttributes\(\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|sysAttachmentID|String|Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.|

|Type|Description|
|----|-----------|
|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|The attachment record and all of its attributes.|

The following example shows how to get all attributes assigned to a specified attachment.

```
var attach = new GlideSysAttachment();

var attachmentID = '9e1b714601932210f877b455304df0af';

var result = attach.fetchAllAttributes(attachmentID);

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

## Scoped GlideSysAttachment - fetchAttribute\(String sysAttachmentID, String attrKey\)

Fetches a specified attribute from an attachment record.

See also:

-   [addAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [addMultipleAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - fetchAttribute\(String attrKey\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|sysAttachmentID|String|Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.|
|attrKey|String|Key portion of a key-value pair for an attachment attribute.|

|Type|Description|
|----|-----------|
|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|The GlideRecord of the attachment and the specified attribute.|

The following example shows how to get an attachment attribute with the key `author`.

```
var attach = new GlideSysAttachment();

var attachmentID = '9e1b714601932210f877b455304df0af';

var result = attach.fetchAttribute(attachmentID, "author");

while(result.next()) {
   gs.info("Key: " + result.getValue('key') + " \nValue: " + result.getValue('value')); 
}
```

Output:

```
Key: author 
Value: Abel Tuter
```

## Scoped GlideSysAttachment - getAttachments\(String tableName, String sys\_id\)

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

## Scoped GlideSysAttachment - getContent\(GlideRecord sysAttachment\)

Returns the attachment content as a string.

This method is for use in scoped applications only. This method returns `undefined` when used in the global scope. To read attachment content in the global scope, use the getContentStream\(\) method from the GlideSysAttachment - Global API.

This method supports the following file types for attachments.

-   CSV \(\*.csv\)
-   JSON \(\*.json\)
-   Text \(\*.txt\)

|Name|Type|Description|
|----|----|-----------|
|sysAttachment|GlideRecord|Attachment record.|

|Type|Description|
|----|-----------|
|String|Attachment contents as a string. Returns up to 5MB of data.|

```
var attachment = new GlideSysAttachment();

var agr = attachment.getAttachments('incident', '78271e1347c12200e0ef563dbb9a7109'); //create attachment GlideRecord

while(agr.next()) { //for each attachment on the incident record
   gs.info(agr.getValue('file_name')); //print file name of attachment
   var attachmentContent = attachment.getContent(agr);
   gs.info('Attachment content: ' + attachmentContent); //print attachment content
}
```

Output:

```
Doc1.txt
Attachment content: I am text in a txt file attached to a record.
```

## Scoped GlideSysAttachment - getContentBase64\(GlideRecord sysAttachment\)

Returns the attachment content as a string with base64 encoding.

This method is for use in scoped applications only. This method returns `undefined` when used in the global scope. To read attachment content in the global scope, use the getContentStream method from the GlideSysAttachment - Global API.

|Name|Type|Description|
|----|----|-----------|
|sysAttachment|GlideRecord|Attachment record.|

|Type|Description|
|----|-----------|
|String|Attachment contents as a string with base64 encoding. Returns up to 5MB of data.|

```
var attachment = new GlideSysAttachment();

var agr = attachment.getAttachments('incident', '78271e1347c12200e0ef563dbb9a7109'); //create attachment GlideRecord

while(agr.next()) { //for each attachment on the incident record
   gs.info(agr.getValue('file_name')); //print file name of attachment
   var attachmentContent = attachment.getContentBase64(agr);
   gs.info('Attachment content: ' + attachmentContent); //print attachment content
}
```

Output:

```
Doc1.txt
Attachment content: SSBhbSB0ZXh0IGluIGEgdHh0IGZpbGUgYXR0YWNoZWQgdG8gYSByZWNvcmQuIA0=
```

## Scoped GlideSysAttachment - getContentStream\(String sysID\)

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

## Scoped GlideSysAttachment - updateAllAttributes\(String sysAttachmentID, Object attrsKeyValuePair\)

Updates all the attributes for an existing attachment record.

See also:

-   [addAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [addMultipleAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - updateAllAttributes\(Object attrsKeyValuePair\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

<table id="table_rql_3mg_5fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysAttachmentID

</td><td>

String

</td><td>

Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.

</td></tr><tr><td>

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
var attach = new GlideSysAttachment();

var attachmentID = '9e1b714601932210f877b455304df0af';

var attachmentAttributes = {
    "category" : "Training",
    "title" : "Updating attachment attributes", 
    "author" : "Abraham Lincoln",
    "length" : "6000"
}

attach.updateAllAttributes(attachmentID, attachmentAttributes);

var result = attach.fetchAllAttributes(attachmentID);

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

## Scoped GlideSysAttachment - updateAttribute\(String sysAttachmentID, String attrKey, String attrValue\)

Updates a single attribute for an existing attachment record.

See also:

-   [addAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [addMultipleAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [deleteAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [fetchAttribute\(\)](c_GlideSysAttachmentScopedAPI.md#)
-   [updateAllAttributes\(\)](c_GlideSysAttachmentScopedAPI.md#)

For the global equivalent of this method, use [GlideSysAttachment - updateAttribute\(String attrKey, String attrValue\)](../../GlideSysAttachmentGlobal/concept/GlideSysAttachmentGlobalAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|sysAttachmentID|String|Sys\_id of the attachment listed in the Attachments \[sys\_attachment\] table.|
|attrKey|String|Key portion of a key-value pair for an attachment attribute.|
|attrValue|String|Value portion of a key-value pair for an attachment attribute.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to update an attribute assigned to a specified attachment with the key `author` and changes the value to Abel Tuter. The results can also be verified in the Attachment Attributes \[sys\_attachment\_attribute\] table.

```
var attach = new GlideSysAttachment();

var attachmentID = '9e1b714601932210f877b455304df0af';

var originalVal = attach.fetchAttribute(attachmentID, "author");
while(originalVal.next()) {
   gs.info("Original attribute value: " + originalVal.getValue('value') + "\n"); 
}

attach.updateAttribute(attachmentID, "author", "Abel Tuter");

var updatedVal = attach.fetchAttribute(attachmentID, "author"); 
while(updatedVal.next()) {
   gs.info("Updated attribute value: " + updatedVal.getValue('value')); 
}
```

Output:

```
Original attribute value: Fred Luddy

Updated attribute value: Abel Tuter
```

## Scoped GlideSysAttachment - write\(GlideRecord record, String fileName, String contentType, String content\)

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

## Scoped GlideSysAttachment - writeBase64\(GlideRecord now\_GR, String fileName, String contentType, String content\_base64Encoded\)

Inserts an attachment for the specified record using base64 encoded content.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|Record to which to attach the attachment.|
|fileName|String|Attachment file name.|
|contentType|String|MIME type of the attachment, such as `image/png`. Located in the Attachment \[sys\_attachment\] table in the **Content type** field.|
|content|String|Attachment content in base64 format.|

|Type|Description|
|----|-----------|
|String|Sys\_id of the attachment created.|

```
var attachment = new GlideSysAttachment();

var rec = new GlideRecord('incident');
var incidentSysID = 'ab1b30031b04ec101363ff37dc4bcbfc';
rec.get(incidentSysID);
var fileName = 'example.txt';
var contentType = 'text/csv';
var base64Encodedcontent = 'SSBhbSB0ZXh0Lg==';

var agr = attachment.writeBase64(rec, fileName, contentType, base64Encodedcontent);

gs.info('The attachment sys_id is: ' + agr);
```

Output:

```
The attachment sys_id is: 10cde9971b0820501363ff37dc4bcba6
```

## Scoped GlideSysAttachment - writeContentStream\(GlideRecord now\_GR, String fileName, String contentType, GlideScriptableInputStream inputStream\)

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

