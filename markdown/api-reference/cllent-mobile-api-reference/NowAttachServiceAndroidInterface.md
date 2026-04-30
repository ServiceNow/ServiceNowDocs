---
title: NowAttachmentService interface - Android
description: The NowAttachmentService interface provides functions that enable the manipulation of file attachments and their associated metadata.Retrieves the attachment with the specified sys\_id and optionally validates the attachment by comparing the computed hash of the attachment to the expected hash.Retrieves the metadata for the attachment associated with the specified sys\_id.Retrieves the metadata for all the attachments that meet the specified criteria.Retrieves the metadata for all the attachments that meet the specified criteria and creates a paginator for iterating through the pages of the returned metadata.Deletes the attachment with the specified sys\_id.Retrieves the metadata for all the attachments that meet the specified criteria and creates a paginator for iterating through pages of the returned metadata.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAttachmentService interface- Android

The NowAttachmentService interface provides functions that enable the manipulation of file attachments and their associated metadata.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationAndroidAPI.md)|Configuration to associate with the service.|

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowAttachmentService - attachment\(sysId: String, validateAttachment: Boolean = true\)

Retrieves the attachment with the specified sys\_id and optionally validates the attachment by comparing the computed hash of the attachment to the expected hash.

<table id="table_old_sp5_4pb" class="parameters"><thead><tr><th>

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

Sys\_id of the attachment to retrieve. This is the sys\_id for the attachment on your ServiceNow instance.

</td></tr><tr><td>

validateAttachment

</td><td>

Boolean

</td><td>

Flag that indicates whether to validate the attachment.

 Valid values:

-   true: Validate the attachment.
-   false: Do not validate the attachment.

 Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|[Call](../../Call/concept/CallAndroidInterface.md#)&lt;[NowAttachment](../../NowAttachment/concept/NowAttachmentAndroidAPI.md#)&gt;|NowAttachment object that contains the requested attachment.|

```
fun getAttachment(sysId: String, isValidateAttachment: Boolean) { 
  val call = attachmentService.attachment(sysId, isValidateAttachment) 
  call.enqueue( 
    { response -> 
      val attachment: NowAttachment? = response.body 
    }, 
      { nowDataError -> handleError(nowDataError) } 
  ) 
}
```

## NowAttachmentService - attachmentMetadata\(sysId: String\)

Retrieves the metadata for the attachment associated with the specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of the attachment whose metadata you want to retrieve.|

|Type|Description|
|----|-----------|
|[Call](../../Call/concept/CallAndroidInterface.md#)​&lt;[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataAndroidAPI.md#)&gt;|Object that contains the metadata for the specified attachment.|

```
fun fetchMetadata(sysId: String) { 
  val call = attachmentService.attachmentMetadata(sysId) 
  call.enqueue(
    { response -> 
      val metadata: NowAttachmentMetadata? = response.body 
    },
    { nowDataError -> handleError(nowDataError) } 
  )
}
```

## NowAttachmentService - attachmentMetadata\(filter: Filter? = null, limit: Int? = null\)

Retrieves the metadata for all the attachments that meet the specified criteria.

<table id="table_ujt_zc1_ppb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilterAndroidAPI.md#)

</td><td>

Optional. Query string to use to filter the attachments whose metadata to return.Default: null - Returns metadata for all available attachments. Takes into consideration the **limit** parameter.

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Maximum number of attachment file's metadata to return.Default: null - Returns all metadata that meets the **filter** parameter specifications.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|[Call](../../Call/concept/CallAndroidInterface.md#)&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/)​&lt;[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataAndroidAPI.md#)&gt;&gt;|List of objects that contain the metadata for the matching attachments.|

```
fun fetchMultipleMetadata(filterQuery: String, limit: Int) { 
  val call = attachmentService.attachmentMetadata(Filter(filterQuery), limit) 
  call.enqueue( 
    { response -> 
      val metadataList: List<NowAttachmentMetadata>? = response.body 
    },
    { nowDataError -> handleError(nowDataError) } 
  )
}
```

## NowAttachmentService - attachmentMetadataPaginator\(filter: Filter? = null, limit: Int? = null\)

Retrieves the metadata for all the attachments that meet the specified criteria and creates a paginator for iterating through the pages of the returned metadata.

You can use this paginator to navigate through the returned metadata, performing navigation operations such as fetching the first, last, previous, or next page, or checking whether there is next or previous page.

<table id="table_npz_zf1_ppb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

filter

</td><td>

[Filter](../../Filter/concept/FilterAndroidAPI.md#)

</td><td>

Optional. Query string to use to filter the attachments whose metadata to return.Default: null - Returns metadata for all available attachments. Takes into consideration the **limit** parameter.

</td></tr><tr><td>

limit

</td><td>

Integer

</td><td>

Optional. Maximum number of attachment file's metadata to return.Default: null - Returns all metadata that meets the **filter** parameter specifications.

</td></tr></tbody>
</table><table id="table_opz_zf1_ppb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Paginator​&lt;[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataAndroidAPI.md#)&gt;

</td><td>

Success: Paginator object along with the specified pages of metadata. Failure: NowDataError object.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val filterQuery: String = "content_type=text/plain"
  val filter = filterQuery.let(::Filter)
  val limit = 10
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(filter, limit)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")
}
```

## NowAttachmentService - delete\(sysId: String\)

Deletes the attachment with the specified sys\_id.

|Name|Type|Description|
|----|----|-----------|
|sysId|String|Sys\_id of the attachment to delete.|

<table id="table_eq4_dj1_ppb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Call](../../Call/concept/CallAndroidInterface.md#)&lt;[ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/)&gt;

</td><td>

Success: Nothing is returned.Failure: NowDataError returned.

</td></tr></tbody>
</table>```
fun deleteAttachment(sysId: String) { 
  val call = attachmentService.delete(sysId) 
  call.enqueue( 
    { response -> handleResponse(response) }, 
    { nowDataError -> handleError(nowDataError) } 
  )
} 
```

## NowAttachmentService - upload\(data: ByteArray, configuration: NowAttachmentUploadConfiguration\)

Retrieves the metadata for all the attachments that meet the specified criteria and creates a paginator for iterating through pages of the returned metadata.

|Name|Type|Description|
|----|----|-----------|
|data|[ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/)|Metadata to upload and associate with the attachment specified in the configuration object.|
|configuration|NowAttachmentUploadConfiguration|Upload configuration parameters.|

|Type|Description|
|----|-----------|
|[NowAttachmentMetadata](../../NowAttachmentMetadata/concept/NowAttachmentMetadataAndroidAPI.md#)|Uploaded metadata.|

```
fun uploadAttachment(tableName: String, recordSysId: String, fileName: String) { 
  val bitmap = BitmapFactory.decodeResource(resources, R.drawable.test_image) 
  val data = bitmap.compress(ImageType.JPEG) 
  val contentType = "image/jpg" 
  val config = NowAttachmentUploadConfiguration(tableName, recordSysId, fileName, contentType) 
  val call = attachmentService.upload(data, config) 
 
  call.enqueue( 
    { response -> 
      val uploadedAttachmentMetadata: NowAttachmentMetadata? = response.body 
    },
    { nowDataError -> handleError(nowDataError) } 
  )
}
```

