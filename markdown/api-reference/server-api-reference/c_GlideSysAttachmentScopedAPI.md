---
title: GlideSysAttachment - Scoped
description: The GlideSysAttachment API provides methods to handle attachments.Creates an instance of the GlideSysAttachment class.Copies attachments from the source record to the target record.Deletes the specified attachment.Returns a GlideRecord containing the matching attachment metadata such as name, type, or size.Returns the attachment content as a string.Returns the attachment content as a string with base64 encoding.Returns a GlideScriptableInputStream object given the sys\_id of an attachment.Attaches a specified attachment to the specified record.Inserts an attachment for the specified record using base64 encoded content.Inserts an attachment using the input stream.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
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

## Scoped GlideSysAttachment - copy\(String sourceTable, String sourceID, String targetTable, String targetID\)

Copies attachments from the source record to the target record.

|Name|Type|Description|
|----|----|-----------|
|sourceTable|String|Name of the table with the attachments to be copied.|
|sourceID|String|Source table's sys\_id.|
|targetTable|String|Name of the table on which to add the attachments.|
|targetID|String|Target table's sys\_id.|

|Type|Description|
|----|-----------|
|String|Array of sys\_ids of the attachments that were copied.|

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

## Scoped GlideSysAttachment - deleteAttachment\(String attachmentID\)

Deletes the specified attachment.

|Name|Type|Description|
|----|----|-----------|
|attachmentID|String|Attachment's sys\_id.|

|Type|Description|
|----|-----------|
|void| |

```
var attachment = new GlideSysAttachment();
var attachmentSysID = 'a87769531b0820501363ff37dc4bcba2';
attachment.deleteAttachment(attachmentSysID);
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

