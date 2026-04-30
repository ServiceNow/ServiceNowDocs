---
title: GlideSysAttachment - Global
description: The GlideSysAttachment API provides methods for handling attachments.Creates an instance of the GlideSysAttachment class.Copies attachments from the source record to the target record.Deletes the specified attachment.Returns a GlideRecord containing the matching attachment metadata such as name, type, or size.Returns a GlideScriptableInputStream object given the sys\_id of an attachment.Attaches a specified attachment to the specified record.Inserts an attachment using the input stream.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-02-18"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSysAttachment- Global

The GlideSysAttachment API provides methods for handling attachments.

Content is returned as a GlideScriptableInputStream object when getContentStream\(\) is called. The GlideScriptableInputStream contains the actual bytes not converted into a string.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSysAttachment - GlideSysAttachment\(\)

Creates an instance of the GlideSysAttachment class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## GlideSysAttachment - copy\(String sourceTable, String sourceID, String targetTable, String targetID\)

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

## GlideSysAttachment - deleteAttachment\(String attachmentID\)

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

