---
title: NowAttachment structure - iOS
description: The NowAttachment structure provides functions that enable you to validate attachments by comparing their computed hash.Validates the attachment by comparing the computed hash for the attachment data to the digest stored in the attachment metadata.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAttachment structure - iOS

The NowAttachment structure provides functions that enable you to validate attachments by comparing their computed hash.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Data

</td><td>

Attachment data.

</td></tr><tr><td>

hash

</td><td>

String

</td><td>

Computed digest for the attachment data.This computed digest is used to [validate](NowAttachmentiOSStructure.md#) the attachment by comparing it to the known digest stored in the [attachment metadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#). Calculating the computed digest is expensive; avoid using it in the UI. Instead, consider using the hash property in the [NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#) class. If you must use the computed hash, use it sparingly, and consider caching it.

</td></tr><tr><td>

metadata

</td><td>

[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataiOSStructure.md#)

</td><td>

Metadata associated with the attachment.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowAttachment - validate\(\)

Validates the attachment by comparing the computed hash for the attachment data to the digest stored in the attachment metadata.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pvt_cgr_5pb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the attachment is valid.Possible values:

-   true: Attachment is valid.
-   false: Attachment is invalid.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
guard 
  let metadataHeader = response.httpResponse?.value(forHTTPHeaderField: NowAttachment.attachmentMetadataHeaderKey),
  let metadataHeaderData = metadataHeader.data(using: .utf8) else {
    throw NowDataError.missingAttachmentMetadata
  }
            
let metadata = try coder.decode(NowAttachmentMetadata.self, from: metadataHeaderData)
let attachment = NowAttachment(metadata: metadata, data: response.data)
            
if !attachment.validate() {
  throw NowDataError.attachmentValidation
}
// Attachment is valid
return attachment
```

