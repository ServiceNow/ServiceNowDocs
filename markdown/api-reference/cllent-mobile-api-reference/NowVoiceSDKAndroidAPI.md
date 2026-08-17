---
title: NowVoiceSDK object - Android
description: The NowVoiceSDK factory object creates NowVoiceService instances.Creates a NowVoiceService instance for the specified ServiceNow instance. This is a suspend function.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowVoiceSDKAndroidAPI.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceSDK object- Android

The NowVoiceSDK factory object creates NowVoiceService instances.

Use [`NowVoiceService`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md) to start and manage voice agent sessions.

For more information about configuring NowVoice, including prerequisites and call order, see [Embed an AI voice agent with NowVoice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/mobsdk-and-nowvoice.md).

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

## NowVoiceSDK - makeVoiceService\(instanceURL: URL\)

Creates a NowVoiceService instance for the specified ServiceNow instance. This is a suspend function.

Call from a coroutine after [NowSDK.configure\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowSDKAndroidAPI.md) has been called. This function fetches instance settings over the network, validates that voice is enabled on the instance, and retrieves available voice endpoint configurations.

Throws [NowServiceError](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowServiceErrorAndroidAPI.md) on failure.

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance, for example `URL("https://instancename.service-now.com")`.|

|Type|Description|
|----|-----------|
|Result&lt;[NowVoiceService](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md)&gt;|`Result.success(NowVoiceService)` if initialization succeeds, or `Result.failure(NowServiceError)` if setup fails.|

The following code example creates an instance of NowVoiceService.

```
import com.servicenow.nowsdk.voice.NowVoiceSDK
import kotlinx.coroutines.launch
import java.net.URL

lifecycleScope.launch {
    val result = NowVoiceSDK.makeVoiceService(
        instanceURL = URL("https://your-instance.service-now.com")
    )

    result
        .onSuccess { voiceService ->
            // Service is ready; proceed to select an endpoint
        }
        .onFailure { error ->
            // Handle NowServiceError
            Log.e("NowVoice", "Service creation failed: $error")
        }
}
```

