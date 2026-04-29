---
title: cabrillo.attachments - Client
description: The name space for Cabrillo JS attachment functions. This enables adding and viewing attachments.Presents a document picker and uploads the selected file.Presents a document picker to select and upload files.Presents a document picker and uploads the selected file.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.attachments - Client

The name space for Cabrillo JS attachment functions. This enables adding and viewing attachments.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.attachments - addFile\(String tableName, String sysId, Object params, String options\)

Presents a document picker and uploads the selected file.

**Important:** This method is deprecated. Use the [addFiles\(\)](cabrillo-attachments-namespace.md#) method instead.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Table name of the record to which to attach the attachment.|
|sysID|String|The sys\_id of the record to which to attach the attachment.|
|params|Object|Unused. Set to null.|
|options|String|Unused. Set to null.|

|Type|Description|
|----|-----------|
|promise|If successful a Cabrillo.Attachment object. If the operation fails, an error.|

```
var table = 'incident';
var sysID = 'a9e30c7dc61122760116894de7bcc7bd';

cabrillo.attachments.addFile(table,
    sysID, 
    null,
    null
).then(function(attachment) {
    if (attachment) {
        console.log('Added a new file.', attachment);
    } else {
        console.log('User cancelled adding an attachment.');
    }
}, function(error) {
    console.log('Failed to attach new file.', error);
});
```

## cabrillo.attachments - addFiles\(String tableName, String sysId, Object params, Object options\)

Presents a document picker to select and upload files.

<table id="table_yt5_3qw_2bb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Name of the table that contains the record to attach the file to.

</td></tr><tr><td>

sysID

</td><td>

String

</td><td>

Sys\_id of the record to attach the file to.

</td></tr><tr><td>

params

</td><td>

Object

</td><td>

Optional. Reserved for future use. Set to null.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. Additional settings for uploading files.```
{
  "isSingleSelection": Boolean
}
```

</td></tr><tr><td>

options.isSingleSelection

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the document picker for uploading files allows multi-selection.

 Valid values:

-   true: Only one file to upload can be selected at a time.
-   false: Multiple files to upload can be selected at a time.

 Default: False

</td></tr></tbody>
</table><table id="table_wgq_ynf_xwb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Promise

</td><td>

Contains any successfully created attachments and any errors.If multiple files were selected, a Cabrillo.Attachment is created for each successfully uploaded file while an error message is generated for each unsuccessful upload.

Data type: Object

```
{ 
   “attachments”: [Array], 
   “errors”: [Array] 
}
```

</td></tr><tr><td>

Promise.attachments

</td><td>

Contains any successfully created attachments.Data type: Array

```
“attachments”: [Cabrillo.Attachment]
```

</td></tr><tr><td>

Promise.errors

</td><td>

Contains any errors.Data type: Array

```
“errors”: ["String"]
```

</td></tr></tbody>
</table>This example creates a button for adding multiple attachments to an incident record and checks for any upload errors.

```
this.attachMultipleFilesButton = function() {
   c.log("Attempting to add multiple attachments to INC0010453");
   var table = 'incident';
   var sysID = 'fc74aefa1bfb2c10181499f1b24bcb3c';

   cabrillo.attachments.addFiles(table, sysID).then(function(result) {
      if (result) {
         handleMultipleResult(result)
      } else {
         c.log('User cancelled adding an attachment.');
      }
   }, function(error) {
      c.log('Failed to attach new files.', error);
   });
}

// A helper function to handle addFiles results 
function handleMultipleResult(result) {
   c.log('Added multiple attachments.', result);
   if (result.attachments) {
      c.log('Number of new attachments', result.attachments.length);
   }
   if (result.errors) {
      c.log('Number of errors during upload', result.errors.length);
   }
}
```

## cabrillo.attachments -viewFile\(Cabrillo.Attachment attachment, Cabrillo.Rect sourceRect, String sourceBase64Image\)

Presents a document picker and uploads the selected file.

**Note:** Scaling using a sourceRect parameter with a sourceBase64 image is only supported on iOS. Android ignores these parameters and opens the image without a scaling animation.

|Name|Type|Description|
|----|----|-----------|
|attachment|Cabrillo.Attachment|Describes the attachment to view.|
|sourceRect|Cabrillo.Rect|Optional. Describes the source rectangle of the image to scale up.|
|sourceBase64Image|String|Optional. A base64 representation of the source image to scale up.|

|Type|Description|
|----|-----------|
|promise|If successful, an unresolved object, otherwise an error.|

```
// A Cabrillo.Attachment dictionary to view
var attachment = {
    sys_id: '8e99daa3ff133100ba13ffffffffff2d',
    content_type: 'image/jpeg',
    path: '8e99daa3ff133100ba13ffffffffff2d.iix'
};

cabrillo.attachments.viewFile(attachment,
    null,
    null
).then(function() {
    // It worked. Nothing to do here.
}, function(error) {
    console.log('Failed to view file.', error);
});
```

To scale an image that was tapped into a native image viewer, the viewFile\(\) method accepts optional arguments for the image's rectangle on the page as well as a base64 encoded thumbnail of the image. The thumbnail is scaled into the full size image with an animation.

```
// Grab image metadata from an image that was tapped
var imageMetadata = imageMetadataFromEvent(event);

// Optional rect of image on page
var imageRect = imageMetadata.rect;

// Optional base64 encoded image to scale up into native viewer
var base64EncodedImage = imageMetadata.base64;

// A Cabrillo.Attachment dictionary to view
var attachment = {
    sys_id: '8e99daa3ff133100ba13ffffffffff2d',
    content_type: 'image/jpeg',
    path: '8e99daa3ff133100ba13ffffffffff2d.iix'
}

cabrillo.attachments.viewFile(attachment,
    imageRect,
    base64EncodedImage
).then(function() {
    // It worked. Nothing to do here.
}, function(error) {
    console.log('Failed to view file.', error);
});
```

