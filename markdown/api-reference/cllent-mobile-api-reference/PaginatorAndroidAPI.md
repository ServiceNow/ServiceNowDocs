---
title: Paginator class - Android
description: The Paginator class provides functions for paging through the return results passed back by a REST endpoint call, such as those returned by the NowTableService class.Fetches the first page of the return results.Checks whether there is a next page in the return results.Checks whether there in a previous page in the return results.Checks whether the Paginator is busy fetching data.Fetches the last page of the return results.Fetches the next page of the return results.Sets the Paginator object's callbacks. You must call this method before calling any other Paginator functions.Fetches the previous page of the return results.Resets the Paginator back to the first page but doesn’t return the first page of the return results.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# Paginator class - Android

The Paginator class provides functions for paging through the return results passed back by a REST endpoint call, such as those returned by the NowTableService class.

You must first call the [NowTableService - paginator\(from tableName: String, configuration: FetchConfiguration? = nil\)](../../../MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#) or [NowTableService - paginator&lt;Model: Decodable&gt;\(from tableName: String, path: String = Constants.resultPath, coder: Coder = .default, configuration: FetchConfiguration? = nil\)](../../../MobileSDKiOS/NowTableService/concept/NowTableServiceiOSAPI.md#) function to retrieve paginate return results.

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## Paginator - first\(\)

Fetches the first page of the return results.

The method throws a `PaginationError` if it cannot fetch the first page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  paginator.first()
}
```

## Paginator - hasNext\(\)

Checks whether there is a next page in the return results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_gxz_rww_rqb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there’s a next page in the return results.Possible values:

-   true: Next page available.
-   false: No next page available.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  if (paginator.hasNext() && !paginator.isBusy()) {
    paginator.next()
  }
}
```

## Paginator - hasPrevious\(\)

Checks whether there in a previous page in the return results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ry4_dxw_rqb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there is a previous page in the return results.Possible values:

-   true: Previous page available.
-   false: No previous page available.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  if (paginator.hasPrevious() && !paginator.isBusy()) {
    paginator.previous()
  }
}
```

## Paginator - isBusy\(\)

Checks whether the Paginator is busy fetching data.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_x3d_cyw_rqb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

None

</td><td>

Flag that indicates whether the Paginator is busy fetching data.Possible values:

-   true: Busy fetching data.
-   false: Not busy.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  if (paginator.hasNext() && !paginator.isBusy()) {
    paginator.next()
  }
}
```

## Paginator - last\(\)

Fetches the last page of the return results.

The method throws a `PaginationError` if it cannot fetch the last page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  if !paginator.isBusy()) {
    paginator.last()
  }
}
```

## Paginator - next\(\)

Fetches the next page of the return results.

The method throws a `PaginationError` if there are no more pages to fetch.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  if (paginator.hasNext() && !paginator.isBusy()) {
    paginator.next()
  }
}
```

## Paginator - observe\(callback: PaginatorCallBack&lt;T&gt;\)

Sets the Paginator object's callbacks. You must call this method before calling any other Paginator functions.

<table id="table_yj5_yyw_rqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

callback

</td><td>

PaginatorCallBack

</td><td>

Callbacks to call based on the success or failure of the Paginator creation.-   Success: `abstract fun onSuccess(response: Response<List<T>>)`
-   Failure: `abstract fun onFailure(e: NowDataError)`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginationCallBack = object : PaginatorCallBack<NowAttachmentMetadata> {
    override fun onFailure(e: NowDataError) {
      handleError(e)
    }

    override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
      handleResponse(response)
    }

  }

  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(paginationCallBack)
    ?: throw Exception("Response is null")
}
```

## Paginator - previous\(\)

Fetches the previous page of the return results.

The method throws a `PaginationError` if it cannot fetch the previous page.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  if (paginator.hasPrevious() && !paginator.isBusy()) {
    paginator.previous()
  }
}
```

## Paginator - reset\(\)

Resets the Paginator back to the first page but doesn’t return the first page of the return results.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun createAttachmentMetadataPaginator() {
  val paginator = nowServiceManager.getNowAttachmentService()?.attachmentMetadataPaginator(null, 10)
    ?.observe(object : PaginatorCallBack<NowAttachmentMetadata> {
      override fun onFailure(e: NowDataError) {
        handleError(e)
      }

      override fun onSuccess(response: Response<List<NowAttachmentMetadata>>) {
        handleResponse(response)
      }

    })
    ?: throw Exception("Response is null")

  paginator.reset()
}
```

