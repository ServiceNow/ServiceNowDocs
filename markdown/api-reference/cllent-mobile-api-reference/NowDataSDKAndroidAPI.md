---
title: NowDataSDK class - Android
description: The NowDataSDK class provides functions that enable the creation and initialization of various features services such as NowGraphQLService, NowAttachmentService, NowTableService, and NowAPIService.Creates and initializes an instance of the NowGraphQLService feature. This service enables access to the GraphQL API on your ServiceNow instance.Creates and initializes an instance of the NowAPIService service. This service allows you to access the public REST APIs exposed by your ServiceNow instance.Creates and initializes an instance of the NowAttachmentService feature.Creates and initializes an instance of the NowTableService feature.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowDataSDK class- Android

The NowDataSDK class provides functions that enable the creation and initialization of various features services such as NowGraphQLService, NowAttachmentService, NowTableService, and NowAPIService.

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowDataSDK - makeGraphQLService\(instanceURL: URL\)

Creates and initializes an instance of the NowGraphQLService feature. This service enables access to the GraphQL API on your ServiceNow instance.

For additional information on the ServiceNow GraphQL API, see [Query record data using the GraphQL API framework](../../../../../../integrate/graphql/concept/scripted-graph-ql.md).

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance to access. For example, `"https://instance.servicenow.com"`|

|Type|Description|
|----|-----------|
|Result&lt;NowGraphQLService&gt;|NowGraphQLService object wrapped in a [Kotlin Result object](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-result/).|

The following code example shows how to call this function.

```
private var nowGraphQLService: NowGraphQLService? = null

/**
  * Create the NowGraphQLService once in the lifetime of the application, inside the Application class
  * or another manager class that will be injected into other classes via dagger/hilt.
  * NowGraphQLService should be created after initializing the NowSDK.
  */
suspend fun getNowGraphQLService(): NowGraphQLService? {
  if (nowGraphQLService != null) return nowGraphQLService

  return NowDataSDK.makeGraphQLService(URL("https://instance-name.service-now.com")).getOrThrow()
    .also { this.nowGraphQLService = it }
}
```

## NowDataSDK - makeNowAPIService\(instanceURL: URL\)

Creates and initializes an instance of the NowAPIService service. This service allows you to access the public REST APIs exposed by your ServiceNow instance.

In addition, you can develop custom scripted REST APIs within your ServiceNow instance and access them within your Android application using the [NowAPIService](../../NowAPIService/concept/NowAPIServiceAndroidInterface.md#) API. For additional information on ServiceNow REST APIs, see [Scripted REST APIs](../../../../../../integrate/custom-web-services/concept/c_CustomWebServices.md).

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance to access. For example, `"https://instance.servicenow.com"`|

|Type|Description|
|----|-----------|
|Result&lt;NowAPIService&gt;|NowAPIService wrapped in a [Kotlin Result object](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-result/).|

The following code example shows how to call this function.

```
private var nowApiService: NowAPIService? = null

/**
  * Create the NowAPIService once in the lifetime of the application inside the Application class
  * or another manager class that will be injected into other classes via dagger/hilt.
  * NowAPIService should be created after initializing the NowSDK
  */
suspend fun getNowApiService(): NowAPIService? {
  if (nowApiService != null) return nowApiService

  return NowDataSDK.makeAPIService(URL("https://instance-name.service-now.com")).getOrThrow()
    .also { this.nowApiService = it }
}
```

## NowDataSDK - makeNowAttachmentService\(instanceURL: URL\)

Creates and initializes an instance of the NowAttachmentService feature.

This service enables you to upload, download, and delete attachment files from your ServiceNow instance. After you upload an attachment to your instance, it generates metadata for the attachment that you can then download into your Android application.

For additional information on ServiceNow attachments, see [Attachment API](../../../../../../integrate/inbound-rest/concept/c_AttachmentAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance to access. For example, `"https://instance.servicenow.com"`|

|Type|Description|
|----|-----------|
|Result&lt;NowAttachmentService&gt;|NowAttachmentService object wrapped in a [Kotlin Result object](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-result/).|

The following code example shows how to call this method.

```
private var nowAttachmentService: NowAttachmentService? = null

/**
  * Create the NowAttachmentService once in the lifetime of the application inside the Application
  * class or another manager class that will be injected into other classes via dagger/hilt.
  * NowAttachmentService should be created after initializing the NowSDK.
  */
suspend fun getNowAttachmentService(): NowAttachmentService? {
  if (nowAttachmentService != null) return nowAttachmentService

  return NowDataSDK.makeAttachmentService(URL("https://instance-name.service-now.com"))
    .getOrThrow()
    .also { this.nowAttachmentService = it }
}
```

## NowDataSDK - makeTableService\(instanceURL: URL\)

Creates and initializes an instance of the NowTableService feature.

This service enables you to access to the REST Table API on a ServiceNow instance. For additional information on the REST Table API, see [Table API](../../../../../../integrate/inbound-rest/concept/c_TableAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance to access. For example, `"https://instance.servicenow.com"`|

|Type|Description|
|----|-----------|
|Result&lt;NowTableService&gt;|NowTableService object wrapped in a [Kotlin Result object](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-result/).|

The following code example shows how to call this function.

```
private var nowTableService: NowTableService? = null

/**
  * Create the NowTableService once in the lifetime of the application inside the Application
  * class or another manager class that will be injected into other classes via dagger/hilt.
  * NowTableService should be created after initializing the NowSDK.
  */
suspend fun getNowTableService(): NowTableService? {
  if (nowTableService != null) return nowTableService

  return NowDataSDK.makeTableService(URL("https://instance-name.service-now.com")).getOrThrow()
    .also { this.nowTableService = it }
}
```

