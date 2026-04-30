---
title: NowAttachmentMetadata class - Android
description: The NowAttachmentMetadata class provides functions that enable you to encode and manage attachment metadata.Class returned by NowAttachement class. This object is Parcelable.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAttachmentMetadata class - Android

The NowAttachmentMetadata class provides functions that enable you to encode and manage attachment metadata.

<table id="id_ekm_nwf_4qb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="NAMA-averageImageColor-row"><td>

averageImageColor

</td><td>

String

</td><td>

Most dominant color in the associated image.

</td></tr><tr id="NAMA-chunckSizeInBytes-row"><td>

chunkSizeInBytes

</td><td>

Integer

</td><td>

If the attachment is too large to be transferred in a single packet, the maximum of bytes \(chunk\) of the attachment file to send in an individual packet.Unit: Bytes

</td></tr><tr id="NAMA-compressedSizeInBytes-row"><td>

compressed​Size​InBytes

</td><td>

Integer

</td><td>

Compressed size of the attachment.Unit: Bytes

</td></tr><tr id="NAMA-created-row"><td>

created

</td><td>

Date

</td><td>

Date on which the attachment was created.

</td></tr><tr id="NAMA-createdBy-row"><td>

createdBy

</td><td>

String

</td><td>

Entity that created the attachment.

</td></tr><tr id="NAMA-download-row"><td>

download

</td><td>

URL

</td><td>

Full download URL of the attachment associated with the metadata.

</td></tr><tr id="NAMA-fileName-row"><td>

fileName

</td><td>

String

</td><td>

Name of the attachment file.

</td></tr><tr id="NAMA-hash-row"><td>

hash

</td><td>

String

</td><td>

Expected SHA256 digest for the attachment.A downloaded attachment is validated by comparing its computed digest to this SHA256 digest.

</td></tr><tr id="NAMA-imageHeight-row"><td>

imageHeight

</td><td>

Integer

</td><td>

Height of image.Unit: Pixels

</td></tr><tr id="NAMA-imageWidth-row"><td>

imageWidth

</td><td>

Integer

</td><td>

Width of image.Unit: Pixels

</td></tr><tr id="NAMA-isCompressed-row"><td>

isCompressed

</td><td>

Boolean

</td><td>

Flag that indicates whether the attachment file is compressed.Possible values:

-   true: Attachment is compressed.
-   false: Attachment in not compressed.

</td></tr><tr id="NAMA-mimeType-row"><td>

mimeType

</td><td>

String

</td><td>

Attachment MIME type.

</td></tr><tr id="NAMA-modificationCount-row"><td>

modificationCount

</td><td>

Integer

</td><td>

Number of times that the attachment was modified.

</td></tr><tr id="NAMA-sizeInBytes-row"><td>

sizeInBytes

</td><td>

Integer

</td><td>

Size of the attachment.Unit: Bytes

</td></tr><tr id="NAMA-sourceSysId-row"><td>

sourceSysId

</td><td>

String

</td><td>

Sys\_id of the attachment record to which the metadata is associated.

</td></tr><tr id="NAMA-sourceTableName-row"><td>

sourceTableName

</td><td>

String

</td><td>

Name of the source table in which the attachment resides.

</td></tr><tr id="NAMA-state-row"><td>

state

</td><td>

 

</td><td>

Availability state.Valid values:

-   AVAILABLE
-   CONDITIONALLY
-   PENDING
-   UNAVAILABLE

</td></tr><tr id="NAMA-sysId-row"><td>

sysId

</td><td>

String

</td><td>

Unique 32-character Globally Unique ID \(GUID\), that identifies each record in a ServiceNow instance.

</td></tr><tr id="NAMA-tags-row"><td>

tags

</td><td>

String

</td><td>

List of tags associated with the attachment.

</td></tr><tr id="NAMA-updated-row"><td>

updated

</td><td>

Date

</td><td>

Date on which the attachment was last modified.

</td></tr><tr id="NAMA-updatedBy-row"><td>

updatedBy

</td><td>

String

</td><td>

Entity that updated the attachment.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowAttachmentMetadata - NowAttachmentMetadata\(sysId: String, fileName: String, mimeType: String, \_isCompressed: String, \_sizeInBytes: String, \_compressedSizeInBytes: String, \_chunkSizeInBytes: String, \_modificationCount: String, created: Date, createdBy: String, updated: Date, updatedBy: String, download: String?, hash: String, state: NowAttachmentMetadata.State, averageImageColor: String, \_imageWidth: String, \_imageHeight: String, sourceTableName: String, sourceSysId: String, tags: String\)

Class returned by NowAttachement class. This object is Parcelable.

<table id="table_fdd_ynv_wpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysId

</td><td>

String

</td><td>

Unique 32-character Globally Unique ID \(GUID\), that identifies each record in a ServiceNow instance.

</td></tr><tr><td>

fileName

</td><td>

String

</td><td>

Name of the attachment file.

</td></tr><tr><td>

mimeType

</td><td>

String

</td><td>

Attachment MIME type.

</td></tr><tr><td>

isCompressed

</td><td>

Boolean

</td><td>

Flag that indicates whether the attachment file is compressed.Possible values:

-   true: Attachment is compressed.
-   false: Attachment in not compressed.

</td></tr><tr><td>

sizeInBytes

</td><td>

Integer

</td><td>

Size of the attachment.Unit: Bytes

</td></tr><tr><td>

compressed​Size​InBytes

</td><td>

Integer

</td><td>

Compressed size of the attachment.Unit: Bytes

</td></tr><tr><td>

chunkSizeInBytes

</td><td>

Integer

</td><td>

If the attachment is too large to be transferred in a single packet, the maximum of bytes \(chunk\) of the attachment file to send in an individual packet.Unit: Bytes

</td></tr><tr><td>

modificationCount

</td><td>

Integer

</td><td>

Number of times that the attachment was modified.

</td></tr><tr><td>

created

</td><td>

Date

</td><td>

Date on which the attachment was created.

</td></tr><tr><td>

createdBy

</td><td>

String

</td><td>

Entity that created the attachment.

</td></tr><tr><td>

updated

</td><td>

Date

</td><td>

Date on which the attachment was last modified.

</td></tr><tr><td>

updatedBy

</td><td>

String

</td><td>

Entity that updated the attachment.

</td></tr><tr><td>

download

</td><td>

URL

</td><td>

Full download URL of the attachment associated with the metadata.

</td></tr><tr><td>

hash

</td><td>

String

</td><td>

Expected SHA256 digest for the attachment.A downloaded attachment is validated by comparing its computed digest to this SHA256 digest.

</td></tr><tr><td>

state

</td><td>

 

</td><td>

Availability state.Valid values:

-   AVAILABLE
-   CONDITIONALLY
-   PENDING
-   UNAVAILABLE

</td></tr><tr><td>

averageImageColor

</td><td>

String

</td><td>

Most dominant color in the associated image.

</td></tr><tr><td>

imageWidth

</td><td>

Integer

</td><td>

Width of image.Unit: Pixels

</td></tr><tr><td>

imageHeight

</td><td>

Integer

</td><td>

Height of image.Unit: Pixels

</td></tr><tr><td>

sourceTableName

</td><td>

String

</td><td>

Name of the source table in which the attachment resides.

</td></tr><tr><td>

sourceSysId

</td><td>

String

</td><td>

Sys\_id of the attachment record to which the metadata is associated.

</td></tr><tr><td>

tags

</td><td>

String

</td><td>

List of tags associated with the attachment.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|sysId \(SysIdentifiable\)|Unique 32-character GUID of the associated metadata record.|

```

```

