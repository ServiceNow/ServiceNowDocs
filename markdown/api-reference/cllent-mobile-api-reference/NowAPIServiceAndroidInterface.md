---
title: NowAPIService interface - Android
description: The NowAPIService interface provides the ability to perform requests on a specified ServiceNow REST API.Calls the specified REST API on the specified ServiceNow instance.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAPIService interface - Android

The NowAPIService interface provides the ability to perform requests on a specified ServiceNow REST API.

**Note:** Guest users only work for the NowAPIService interface if the REST API being accessed is configured for guest users.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationAndroidAPI.md)|Service configuration to associate with the protocol.|

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowAPIService - data\(endpoint: NowAPIService.Endpoint, queryParams: QueryParams, headers: Headers, body: String\)

Calls the specified REST API on the specified ServiceNow instance.

<table id="table_u3p_dkt_4pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

endpoint

</td><td>

NowAPIService.Endpoint

</td><td>

REST endpoint to call.

</td></tr><tr><td>

queryParams

</td><td>

QueryParams

</td><td>

Optional. Query parameter object that contains the query parameters to pass in the REST call.Default: null

</td></tr><tr><td>

headers

</td><td>

Headers

</td><td>

Optional. Headers object that contains the headers to pass in the REST call.Default: null

</td></tr><tr><td>

body

</td><td>

String

</td><td>

Optional. Object that contains the request body and content type to pass into the REST call.Default: null

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|[Call](../../Call/concept/CallAndroidInterface.md#)&lt;[ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/)&gt;|Return results from the called REST endpoint.|

```
suspend fun loadCases(): List<CaseItem> = withContext(Dispatchers.IO) {
  val apiService = nowServiceManager.getNowAPIService()

  val result = runCatching {
    val response = apiService.data(NowAPIService.Endpoint(
      relativePath = CASES_API,
      requestMethod = HttpMethod.GET,
      requireAuth = true)
    ).execute()

    val byteArray = response.body ?: throw Exception("Null Result")
    val buffer = Buffer()
    val reader = JsonReader.of(buffer.write(byteArray))
    val listType = Types.newParameterizedType(
      List::class.java,
      CaseItem::class.java
    )

    val resultType = Types.newParameterizedType(
      ResultResponse::class.java,
      listType
    )
    val adapter = moshi.adapter<ResultResponse<List<CaseItem>>>(resultType)
    adapter.fromJson(reader)
  }

  if (result.isSuccess) {
      result.getOrNull()?.result ?: throw Exception("Cases not in response")
  } else {
      throw result.exceptionOrNull() ?: Exception("Error Cases")
  }
}
```

