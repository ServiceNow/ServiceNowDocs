---
title: NowWebViewServiceDelegate interface - Android
description: The NowWebViewServiceDelegate API provides callbacks for notification of issues within the NowWebService processing such as when a flow ends or a navigation fails.Callback that notifies the host application that the specified flow has ended.Callback that notifies the host application that navigation has failed with the specified error reason.Callback that notifies the host application that the screen should be dismissed.Callback that notifies the host application that the provided URL is unsupported.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebViewServiceDelegate interface- Android

The NowWebViewServiceDelegate API provides callbacks for notification of issues within the NowWebService processing such as when a flow ends or a navigation fails.

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowWebViewServiceDelegate - flowEnded\(flowName: String?\)

Callback that notifies the host application that the specified flow has ended.

|Name|Type|Description|
|----|----|-----------|
|flowName|String|Name of the flow that ended.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun getNowWebService(): NowWebService {
  return NowWebSDK.makeWebService(URL("https://instance-name.service-now.com"), object : NowWebViewServiceDelegate {
    override fun flowEnded(activity: Activity, flowName: String?) {
      Log.i("NowWebSdk", "flow ended")
    }
  }).getOrThrow()
}
```

## NowWebViewServiceDelegate - navigationFailed\(error : String\)

Callback that notifies the host application that navigation has failed with the specified error reason.

|Name|Type|Description|
|----|----|-----------|
|error|String|Error that describes why the navigation failed.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun getNowWebService(): NowWebService {
  return NowWebSDK.makeWebService(URL("https://instance-name.service-now.com"), object : NowWebViewServiceDelegate {
    override fun navigationFailed(activity: Activity, error: String) {
      Log.i("NebWebSdk", "navigation failed")
    }
  }).getOrThrow()
}
```

## NowWebViewServiceDelegate - requestedDismissal\(\)

Callback that notifies the host application that the screen should be dismissed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun getNowWebService(): NowWebService {
  return NowWebSDK.makeWebService(URL("https://instance-name.service-now.com"), object : NowWebViewServiceDelegate {
    override fun requestedDismissal(activity: Activity) {
      Log.i("NebWebSdk", "screen should be dismissed")
    }
  }).getOrThrow()
}
```

## NowWebViewServiceDelegate - unsupportedUrl\(uri: Uri\)

Callback that notifies the host application that the provided URL is unsupported.

|Name|Type|Description|
|----|----|-----------|
|uri|Uri|URL that is unsupported.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun getNowWebService(): NowWebService {
  return NowWebSDK.makeWebService(URL("https://instance-name.service-now.com"), object : NowWebViewServiceDelegate {
    override fun unsupportedUrl(activity: Activity, uri: Uri) {
      Log.i("NebWebSdk", "URL is unsupported")
    }
  }).getOrThrow()
}
```

