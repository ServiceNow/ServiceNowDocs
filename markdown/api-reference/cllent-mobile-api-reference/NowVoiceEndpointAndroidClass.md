---
title: NowVoiceEndpoint class - Android
description: Describes a voice agent endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NowVoiceEndpointAndroidClass.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceEndpoint class- Android

Describes a voice agent endpoint.

A voice endpoint identifies the specific voice agent channel to connect to. Use [`NowVoiceService.nowVoiceEndpoints`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md) to obtain available NowVoiceEndpoints. Endpoints are retrieved from your ServiceNow instance's Mobile SDK settings. In most apps, there is a single endpoint.

|Name|Type|Description|
|----|----|-----------|
|voiceServiceId|String|The unique identifier of the voice service.|
|voiceWebhookURL|String|The WebSocket webhook URL for the voice agent.|
|mobileChannelType|String|The mobile channel type for the endpoint.|
|mobileChannelId|String|The mobile channel identifier.|

The following code example shows how to retrieve an instance of NowVoiceEndpoint from `NowVoiceService.nowVoiceEndpoints`.

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

val endpoint = voiceService.nowVoiceEndpoints.firstOrNull() ?: return
```

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

