---
title: Call interface - Android
description: The Call interface represents a request that is prepared for processing.Cancels the associated call, if possible \(best effort.\)Schedules the request to be executed as soon as the system\\thread is available to execute this request.Invokes the request immediately. Blocks until the response is processed or is in error.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# Call interface - Android

The Call interface represents a request that is prepared for processing.

Possible processing options include:

-   cancel
-   enqueue
-   execute
-   map

A call object cannot be processed twice.

|Name|Type|Description|
|----|----|-----------|
|request|Request|Original request that initiated this call.|

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## Call - cancel\(\)

Cancels the associated call, if possible \(best effort.\)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
private var inFlightDataRequestCall: Call<*>? = null 
fun cancelTransfer() = inFlightDataRequestCall?.cancel() 
```

## Call - enqueue\(onSuccess: Consumer&lt;Response&lt;T&gt;&gt;, onError: Consumer&lt;NowDataError&gt;\)

Schedules the request to be executed as soon as the system\\thread is available to execute this request.

<table id="table_tnq_3nt_4pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

onSuccess

</td><td>

[Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html)​&lt;Response&lt;T&gt;&gt;

</td><td>

Callback to execute if the call is successful. HTTP response with the body parsed to the data type specified by the **T** parameter. **Note:** Consumer is a OOB Java type for asynchronous consumption of an object. In this case, the call uses generic to return a type `Response<T>` where `T` is the object type.

</td></tr><tr><td>

onError

</td><td>

[Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html)​&lt;NowDataError&gt;

</td><td>

Callback to execute if the call fails.NowDataError

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
fun makeGraphQLRequest(query: String) { 
  val call = graphQLService.graphQLRequest(query) 
  call.enqueue( 
    { response -> handleResponse(response) }, 
    { nowDataError -> handleError(nowDataError) } 
  ) 
} 
```

## Call - execute\(\)

Invokes the request immediately. Blocks until the response is processed or is in error.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Response&lt;T&gt;|Response data in the format defined in the **T** parameter.|

The following code example shows how to call this function.

```
val response = apiService.data(NowAPIService.Endpoint( 
  relativePath = CASES_API, 
  requestMethod = HttpMethod.GET, 
  requireAuth = true) 
).execute()
```

