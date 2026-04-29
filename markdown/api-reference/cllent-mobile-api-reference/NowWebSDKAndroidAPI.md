---
title: NowWebSDK class - Android
description: The NowWebSDK class provides a single function that enables you to load web pages hosted on your ServiceNow instance in a native web view and Cabrillo. It automatically handles user authentication and session management instead of forcing users to log into the instance through a login web page.Creates a NowWeb service.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebSDK class- Android

The NowWebSDK class provides a single function that enables you to load web pages hosted on your ServiceNow instance in a native web view and Cabrillo. It automatically handles user authentication and session management instead of forcing users to log into the instance through a login web page.

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowWebSDK - makeWebService\(instanceURL: URL, nowWebSdkCallbacks: NowWebViewServiceDelegate? = null\)

Creates a NowWeb service.

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance to access. For example, `"https://instance.servicenow.com"`|
|nowWebSdkCallbacks|NowWebViewServiceDelegate|Callbacks for the host application to configure NowWebService.|

|Type|Description|
|----|-----------|
|Result&lt;NowWebService&gt;|NowWebService object wrapped in a [Kotlin Result object](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-result/).|

The following code example shows how to call this function.

```
 private var nowWebService: NowWebService? = null

/**
  * Create the NowWebService once in the lifetime of the application, inside the Application
  * class or another manager class that will be injected into other classes via dagger/hilt.
  * NowWebService should be created after initializing the NowSDK.
  */
suspend fun getNowWebService(): NowWebService? {
  if (nowWebService != null) return nowWebService

  return NowWebSDK.makeWebService(URL("https://instance-name.service-now.com"), object :
    NowWebViewServiceDelegate {
    override fun flowEnded(activity: Activity, flowName: String?) {
      Log.i("NowWebSdk", "flow ended")
    }

    override fun requestedDismissal(activity: Activity) {
      Log.i("NebWebSdk", "screen should be dismissed")
    }

    override fun navigationFailed(activity: Activity, error: String) {
      Log.i("NebWebSdk", "navigation failed")
    }

    override fun unsupportedUrl(activity: Activity, uri: Uri) {
      Log.i("NebWebSdk", "URL is unsupported")
    }
  }).getOrThrow()
      .also { this.nowWebService = it }
}
```

