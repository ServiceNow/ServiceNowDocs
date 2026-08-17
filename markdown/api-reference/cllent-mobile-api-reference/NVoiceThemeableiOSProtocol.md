---
title: NowVoiceThemeable protocol - iOS
description: Sets the colors to apply to NowVoice UI elements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NVoiceThemeableiOSProtocol.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceThemeable protocol- iOS

Sets the colors to apply to NowVoice UI elements.

To match the voice UI to your app's visual identity, create a type conforming to NowVoiceThemeable and pass it to [NowVoiceService - startVoice\(endpoint:uiConfiguration:callbacks:theme:\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md) or [NowVoiceService - updateTheme\(theme:\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md).

|Name|Type|Description|
|----|----|-----------|
|color|[NowUIColoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/mobsdk-ios-use_nowUIcoloring.md)|Colors to apply to NowVoice UI elements.|

This example shows how to apply custom app colors to the voice UI.

```
import NowVoice

let instanceUrl = URL(string: "https://your-instance.service-now.com")!

do {
    let voiceService = try await NowVoice.makeVoiceService(instanceUrl: instanceUrl)
} catch {
    // Handle NowServiceError (see Error reference below)
    print("Failed to create voice service: \(error)")
}

struct MyVoiceTheme: NowVoiceThemeable {
    var color: NowUIColoring = MyAppColors()
}

// Apply at voice session launch
let vc = try await voiceService.startVoice(endpoint: endpoint, theme: MyVoiceTheme())

// Or update while a voice session is active
voiceService.updateTheme(theme: MyVoiceTheme())
```

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

**Related topics**  


[NowVoiceDefaultTheme structure - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NVoiceDefThemeiOSStruct.md)

