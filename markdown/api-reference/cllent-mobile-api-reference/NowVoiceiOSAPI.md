---
title: NowVoice API - iOS
description: NowVoice is a top-level global API for embedding voice agent sessions in iOS applications.Creates an instance of NowVoiceService for the specified ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowVoiceiOSAPI.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoice API- iOS

NowVoice is a top-level global API for embedding voice agent sessions in iOS applications.

Use NowVoice to create a [NowVoiceService](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md) for a given ServiceNow instance, then use that service to start and manage voice agent sessions.

For more information about configuring NowVoice, including prerequisites and call order, see [Embed an AI voice agent with NowVoice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/developer-guides/mobsdk-ios-nowvoice.md).

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

## NowVoice - makeVoiceService\(instanceUrl: URL\) async throws

Creates an instance of NowVoiceService for the specified ServiceNow instance.

**Note:** Call this function from an async context, after calling [NowSDK.configure\(with:\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowSDKAPIiOS.md). This function fetches instance settings over the network; call it when launching a voice session, not at app startup.

This function validates that voice is enabled on the ServiceNow instance and retrieves available endpoint configurations. It throws a `NowServiceError` if setup fails.

|Case|Description|
|----|-----------|
|`.sdkNotConfigured`|NowSDK.configure\(with:\) was not called before creating the service.|
|`.serviceConfigurationInvalid`|The provided **instanceUrl** is malformed or can't be used to build a service configuration.|
|`.serviceSettingsRetrievalFailed(SettingsError)`|A network or authentication error occurred while fetching instance settings.|
|`.serviceSettingsNotFound`|The instance does not have `sdk.voice` settings configured.|
|`.serviceSettingsInvalid`|The `sdk.voice.enabled` key is missing from the instance settings.|
|`.serviceDisabled`|Voice is turned off on the instance \(`sdk.voice.enabled` is `false`\).|

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance, such as `https://instancename.service-now.com`.|

|Type|Description|
|----|-----------|
|[NowVoiceService](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md)|An initialized NowVoiceService ready to start voice sessions.|

The following code example shows how to create an instance of NowVoiceService.

```
import NowVoice

let instanceUrl = URL(string: "https://your-instance.service-now.com")!

do {
    let voiceService = try await NowVoice.makeVoiceService(instanceUrl: instanceUrl)
} catch {
    // Handle NowServiceError
    print("Failed to create voice service: \(error)")
}
```

