---
title: NowVoiceEndpoint structure - iOS
description: Describes a voice agent endpoint.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NowVoiceEndpointiOSStruct.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceEndpoint structure- iOS

Describes a voice agent endpoint.

A voice endpoint identifies the specific voice agent channel to connect to. Use **NowVoiceService.configurations** to obtain available NowVoiceEndpoints. Endpoints are retrieved from your ServiceNow instance's Mobile SDK settings. In most apps, there is a single endpoint.

|Name|Type|Description|
|----|----|-----------|
|mobileChannelType|String|The mobile channel type for the endpoint.|
|mobileChannelId|String|The mobile channel identifier.|
|voiceServiceId|String|The unique identifier of the voice service.|
|voiceWebHookURL|String|The WebSocket webhook URL for the voice agent.|

The following code example shows how to retrieve an instance of NowVoiceEndpoint from **NowVoiceService.configurations**.

```
import NowVoice

let instanceUrl = URL(string: "https://your-instance.service-now.com")!

do {
    let voiceService = try await NowVoice.makeVoiceService(instanceUrl: instanceUrl) //creates a NowVoiceService
} catch {
    // Handle NowServiceError
    print("Failed to create voice service: \(error)")
}

guard let endpoint = voiceService.configurations.first else {
    // No voice endpoints configured on this instance.
    return
}
```

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

