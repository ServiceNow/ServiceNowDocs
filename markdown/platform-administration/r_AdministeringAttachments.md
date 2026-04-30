---
title: Administering attachments
description: Administrators can configure system properties for how files are uploaded and attached to records. Uploading, viewing, and deleting file attachments triggers a single event that can be used for notifications or in scripts.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Administer, Form administration, Forms, fields, and lists, Configure core features, Administer]
---

# Administering attachments

Administrators can configure system properties for how files are uploaded and attached to records. Uploading, viewing, and deleting file attachments triggers a single event that can be used for notifications or in scripts.

## Attachment tables

When you store an attachment to any table, a record is created in the Attachment \[sys\_attachment\] table that contains attachment metadata. The file data is stored in the Attachment Document \[sys\_attachment\_doc\] table, in 4k chunks. For example, if you attach a 12k file called **My\_attachment.pdf**, then there is an Attachment entry with three related Attachment Document entries.

To learn how to upload attachments to records, see [Add and manage attachments](https://www.servicenow.com/docs/access?context=t_AddingAnAttachment&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## Activity stream thumbnail scaling

The **glide.ui.activity\_stream.scale\_images** property scales large images down and creates thumbnails for the activity stream view of the images. This property is active by default. It applies to images retroactively, so any attachments included in an activity stream in the past also see the effects.

-   Maximum dimensions for thumbnails using this property are 525 pixels width by 350 pixels height. The system favors the pixel height first, so you can end up with images that are wider than 525 pixels.
-   Attaching image files over 5 MB can create an out of memory error and cause the instance to restart. An out of memory error and restart occur when the system generates the thumbnail when you attach a new image. The error and restart can also occur the first time you load existing images on a record.
-   The administrator can add the **com.glide.attachment.max\_get\_size** system property to control the maximum image scaling dimensions.

Enter the following information into the \[sys\_properties.list\] table:

|Field|Description|
|-----|-----------|
|Name|com.glide.attachment.max\_get\_size|
|Type|integer|
|Value|5242880|

The value field represents the size in bytes.

-   The base system value is 5242880 bytes \(5 MB\). You can change the value as necessary.
-   With this property set, images that are larger than 5 MB are not scaled and the system creates a link instead. Images smaller than 5 MB are scaled down.

## Configure the max image size property for Activity Streams

When attaching an image in an Activity Stream, the system controls the maximum size of the image. Use the **com.glide.attachment.max\_get\_size** property to control the maximum image scaling dimensions.

## Attachment events and logging

A script action or notification can process attachment events. Only one event is created when action is taken on a record with attachments, even when the record has multiple attachments. The following events are provided.

Only one event is created when action is taken on a record with attachments, even when the record has multiple attachments. The following events are provided.

|Event|Description|
|-----|-----------|
|attachment.read|An attachment has been read or downloaded.|
|attachment.uploaded|An attachment has been uploaded. If multiple attachments are uploaded to a record at one time, only one event is created.|
|attachment.deleted|An attachment has been deleted. This event is also triggered when the record containing the attachment is deleted. If a record is deleted that contains multiple attachments, a separate event is triggered for each attachment in the deleted record.|
|attachment.renamed|An attachment has been renamed.|

## Attachment logging

When an attachment is downloaded, the **attachment.read** event record is written, and you can do something with this event. For example, you can record when and by whom certain attachments are downloaded. For this functionality, **current** is a sys\_attachment record, and the event record uses the following parameters:

-   **parm1:** File name
-   **parm2:** Table name

## Debug attachment indexing

To change debugging options for attachment indexing, add these system properties.

-   **glide.ts.index.attachment.debug**: When the value is set to **true**, enables log messages for exceptions that occur when indexing attachments \(default is **false**\).

    You can leave this property enabled during normal operations to capture stack trace information about any exceptions.

-   **glide.ts.index.attachment.list\_terms.debug**: When the value is set to **true**, logs all indexed terms when an attachment is indexed \(default is **false**\).

    \[Recommended\] For optimal performance, set this property to **false** during normal operations. Only enable this property when you are actively debugging an issue.


**Note:** To learn more about the properties that affect attachments processing, see Attachments \(instance security hardening\) in Instance Security Hardening Settings.

-   **[Configure attachment system properties](../task/t_DisablingTheDragAndDropFeature.md#)**  
You can disable the drag-and-drop feature. \(Users can still upload attachments by browsing to the file.\) You can also limit the attachment file size, restrict who can upload attachments, and restrict what file extensions can be uploaded.
-   **[Disable attachments on a table](../task/disable-attachments-on-table.md)**  
You can prevent users from adding attachments to records on a specific table.
-   **[Index attachments on a table](../task/t_DisablingAttachmentsOnATable.md)**  
You can enable attachment indexing for a table so text searches can return matches from the record and its file attachments.
-   **[Hide the attachment \[view\] link](../task/t_HidingTheAttachmentViewLink.md)**  
Users can open an attachment by clicking either the file name or the **\[view\]** link. The **\[view\]** link opens the file from within the browser, which executes JavaScript code as part of the attachment. You can hide the **\[view\]** link. Users can still view attachments by clicking the file name.
-   **[Configure attachment icons](../task/t_ConfiguringAttachmentIcons.md)**  
Configure the icon that appears beside an attachment of a particular file type.

**Parent Topic:**[Administering forms on the ServiceNow AI Platform](../concept/form-administration.md)

