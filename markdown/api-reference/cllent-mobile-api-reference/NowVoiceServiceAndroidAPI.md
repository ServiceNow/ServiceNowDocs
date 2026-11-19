---
title: NowVoiceService class - Android
description: Manages voice agent sessions for a single ServiceNow instance.Launches the full-screen voice agent Activity. This is a suspend function that returns after the session ends.Updates the visual theme of the currently active voice UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceService class- Android

Manages voice agent sessions for a single ServiceNow instance.

**Note:** Initialize a NowVoiceService by calling [NowVoiceSDK - makeVoiceService\(instanceURL: URL\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceSDKAndroidAPI.md).

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowServiceConfigurationAndroidAPI.md)|The service configuration for the ServiceNow instance.|
|nowVoiceEndpoints|List&lt;[NowVoiceEndpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceEndpointAndroidClass.md)&gt;|Read-only. The list of available voice endpoint configurations retrieved from the instance.|

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

## NowVoiceService - start\(context: Context, endpoint: NowVoiceEndpoint, uiConfiguration: NowVoiceUiConfiguration, callbacks: NowVoiceCallbacks?, theme: NowVoiceTheme\)

Launches the full-screen voice agent Activity. This is a suspend function that returns after the session ends.

<table id="table_pft_qzv_nva2" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

context

</td><td>

[Context](https://developer.android.com/reference/kotlin/android/content/Context.html)

</td><td>

An Android `Context` used to launch the voice Activity. Typically your current `Activity`.

</td></tr><tr><td>

endpoint

</td><td>

[NowVoiceEndpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceEndpointAndroidClass.md)

</td><td>

The voice agent endpoint to connect to. Obtain from `NowVoiceService.nowVoiceEndpoints`.

</td></tr><tr><td>

uiConfiguration

</td><td>

[NowVoiceUiConfiguration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NVoiceUiConfigAndroidClass.md)

</td><td>

Optional. Presentation options for the voice agent UI. If omitted, uses the default values for NowVoiceUiConfiguration.

</td></tr><tr><td>

callbacks

</td><td>

[NowVoiceCallbacks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceCallbacksAndroidInt.md)?

</td><td>

Optional. Callbacks for voice session events. If `null`, events are silently ignored.

</td></tr><tr><td>

theme

</td><td>

[NowVoiceTheme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.md)

</td><td>

Optional. The visual theme applied to the voice UI.Default: The prebuilt light theme.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
//voiceService is an initialized NowVoiceService
val endpoint = voiceService.nowVoiceEndpoints.firstOrNull() ?: return

voiceService.start(
    context = this@MainActivity,
    endpoint = endpoint,
    uiConfiguration = NowVoiceUiConfiguration(
        hidePostCallTranscript = false,
        shouldBlockAttachmentSharing = false
    ),
    callbacks = object : NowVoiceCallbacks {
        override fun onCallEnd(conversationId: String?, error: NowVoiceError?) {
            if (error != null) {
                Log.e("NowVoice", "Session ended with error: $error")
            } else {
                Log.d("NowVoice", "Session complete. ID: $conversationId")
            }
        }

        override fun onMuteStateChanged(isMuted: Boolean) {
            // Update your UI to reflect the current mute state
            Log.d("NowVoice", "Microphone muted: $isMuted")
        }

        override fun onMessageReceived(message: TranscriptMessage) {
            // Receive real-time transcript messages
            Log.d("NowVoice", "${message.role}: ${message.content}")
        }
    },
    theme = object : NowVoiceTheme {}  // Uses default light theme
)
```

## NowVoiceService - updateTheme\(theme: NowVoiceTheme\)

Updates the visual theme of the currently active voice UI.

This function has no effect if no voice session is currently active. To apply a visual theme at voice session launch, provide a theme when calling [start\(context:endpoint:uiConfiguration:callbacks:theme:\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md).

|Name|Type|Description|
|----|----|-----------|
|theme|[NowVoiceTheme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.md)|The theme to apply to the active voice UI.|

|Type|Description|
|----|-----------|
|None| |

The following code example updates the visual theme of the currently active voice UI.

```
//voiceService is an initialized NowVoiceService
voiceService.updateTheme(NowVoiceThemeDark())
```

