---
title: NowPushSDK class - Android
description: The NowPushSDK class provides the function necessary to create a NowPushService that enables the sending of unsolicited \(push\) notifications to Android devices.Creates a NowPush service.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowPushSDK class - Android

The NowPushSDK class provides the function necessary to create a `NowPushService` that enables the sending of unsolicited \(push\) notifications to Android devices.

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowPushSDK - makePushService\(instanceURL: URL\)

Creates a NowPush service.

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance that the NowPushService should interact with.|

|Type|Description|
|----|-----------|
|Result&lt;NowPushService&gt;|NowPushService object wrapped in a [Kotlin Result object](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-result/).|

This example shows how to setup to makePushService\(\) method to create the Push Service.

```
private var nowPushService: NowPushService? = null

/**
  * Create the NowPushService once in the lifetime of the application inside the Application
  * class or another manager class that will be injected into other classes via dagger/hilt.
  * NowPushService should be created after initializing the NowSDK.
  */
suspend fun getNowPushService(): NowPushService? {
  if (nowPushService != null) return nowPushService

  return NowPushSDK.makePushService(URL("https://instance-name.service-now.com")).getOrThrow()
    .also { this.nowPushService = it }
}
```

