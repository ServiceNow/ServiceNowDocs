---
title: NowAttachmentMetadata structure - iOS
description: The NowAttachmentMetadata structure provides functions that enable you to encode and manage attachment metadata.Encodes the current object value into data using the specified encoder.Creates a new NowAttachmentMetadata instance by decoding data into an object from the specified decoder.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAttachmentMetadata structure- iOS

The NowAttachmentMetadata structure provides functions that enable you to encode and manage attachment metadata.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

averageImageColor

</td><td>

String

</td><td>

Most dominant color in the associated image.

</td></tr><tr><td>

chunkSizeInBytes

</td><td>

Integer

</td><td>

Size of the chunk.Unit: Bytes

</td></tr><tr><td>

compressed​Size​InBytes

</td><td>

Integer

</td><td>

Compressed size of the attachment.Unit: Bytes

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

download

</td><td>

URL

</td><td>

URL of the attachment on the ServiceNow instance.

</td></tr><tr><td>

fileName

</td><td>

String

</td><td>

Name of the attachment file.

</td></tr><tr><td>

hash

</td><td>

String

</td><td>

Expected SHA256 digest for the attachment.A downloaded attachment is [validated](../../NowAttachment/concept/NowAttachmentiOSStructure.md#) by comparing its computed digest to this SHA256 digest.

</td></tr><tr><td>

imageHeight

</td><td>

Integer

</td><td>

Height of image.Unit: Pixels

</td></tr><tr><td>

imageWidth

</td><td>

Integer

</td><td>

Width of image.Unit: Pixels

</td></tr><tr><td>

isCompressed

</td><td>

Boolean

</td><td>

Flag that indicates whether the attachment file is compressed.Possible values:

-   true: Attachment is compressed.
-   false: Attachment in not compressed.

</td></tr><tr><td>

mimeType

</td><td>

String

</td><td>

Attachment MIME type.

</td></tr><tr><td>

modificationCount

</td><td>

Integer

</td><td>

Number of times that the attachment was modified.

</td></tr><tr><td>

sizeInBytes

</td><td>

Integer

</td><td>

Size of the attachment.Unit: Bytes

</td></tr><tr><td>

sourceSysId

</td><td>

String

</td><td>

Sys\_id of the attachment file.

</td></tr><tr><td>

sourceTableName

</td><td>

String

</td><td>

Name of the source table in which the attachment resides.

</td></tr><tr><td>

state

</td><td>

 

</td><td>

Availability state, such as conditionally, unavailable, available, and pending.

</td></tr><tr><td>

sysId

</td><td>

String

</td><td>

Unique 32-character Globally Unique ID \(GUID\), that identifies each record in a ServiceNow instance.

</td></tr><tr><td>

tags

</td><td>

String

</td><td>

List of tags associated with the attachment.

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

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowAttachmentMetadata - encode\(to encoder: Encoder\)

Encodes the current object value into data using the specified encoder.

If the object fails to be encoded into data, the encoder encodes an empty [keyed container](https://developer.apple.com/documentation/swift/keyeddecodingcontainer) in its place. This function also throws an error if any values are invalid for the specified encoder's format.

|Name|Type|Description|
|----|----|-----------|
|to encoder|[Encoder](https://developer.apple.com/documentation/swift/encoder)|Encoder that defines the structure of the encoded output.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
let query = "active=true^short_descriptionLIKEbroken"
let filter = Filter(query: query)
metadataPublisher(filter: filter, limit: 1)
private func metadataPublisher(filter: Filter?, limit: Int?) {
  let publisher = attachmentService.attachmentMetadata(filter: filter, limit: limit)
  publisher
  .receive(on: DispatchQueue.main)
  .encode(encoder: JSONEncoder())
  .sink { [weak self] completion in
    if case let .failure(error) = completion {
      // attachment published failed, return NowDataError
    }
  } receiveValue: { [weak self] (data) in
    // Attachment published successful, return data
  }
  .store(in: &subscriptions)
}
```

## NowAttachmentMetadata - init\(from decoder: Decoder\)

Creates a new NowAttachmentMetadata instance by decoding data into an object from the specified decoder.

This method throws an error if reading from the decoder fails or if the data read is corrupt or otherwise invalid.

|Name|Type|Description|
|----|----|-----------|
|decoder|Decoder|Decoder to read data from.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
guard 
  let metadataHeader = response.httpResponse?.value(forHTTPHeaderField: NowAttachment.attachmentMetadataHeaderKey),
  let metadataHeaderData = metadataHeader.data(using: .utf8) else {
    throw NowDataError.missingAttachmentMetadata
  }
            
let metadata = try coder.decode(NowAttachmentMetadata.self, from: metadataHeaderData)
let attachment = NowAttachment(metadata: metadata, data: response.data)
```

