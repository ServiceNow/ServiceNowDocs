---
title: NowVoiceService class - Android
description: Manages voice agent sessions for a single ServiceNow instance.Ends the current voice call.Checks whether there is a currently active voice call.Launches the full-screen voice agent Activity. This is a suspend function that returns after the session ends.Toggles the microphone mute state of the current call.Updates the visual theme of the currently active voice UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 4
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceService class- Android

Manages voice agent sessions for a single ServiceNow instance.

**Note:** Initialize a NowVoiceService by calling [NowVoiceSDK - makeVoiceService\(instanceURL: URL\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceSDKAndroidAPI.md).

<table id="table_vx2_klw_nva1" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

[NowServiceConfiguration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowServiceConfigurationAndroidAPI.md)

</td><td>

The service configuration for the ServiceNow instance.

</td></tr><tr><td>

isMuted

</td><td>

Boolean

</td><td>

Flag that indicates the microphone mute state for the current call. Setting this property has no effect if no call is currently active.Valid values:

-   true: The microphone is muted.
-   false: The microphone is unmuted or no call is active.

</td></tr><tr><td>

nowVoiceEndpoints

</td><td>

List&lt;[NowVoiceEndpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceEndpointAndroidClass.md)&gt;

</td><td>

Read-only. The list of available voice endpoint configurations retrieved from the instance.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

## NowVoiceService - endCall\(\)

Ends the current voice call.

Has no effect if no call is active.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example ends the active voice call.

```
val voiceService = NowVoiceSDK.makeVoiceService(instanceUrl).getOrNull()

val endpoint = voiceService?.nowVoiceEndpoints?.first()
voiceService?.start(activity, endpoint = endpoint, theme = theme)

// End a call on timeout, navigation, or from a custom hang-up button
voiceService?.endCall()
```

## NowVoiceService - hasActiveCall\(\)

Checks whether there is a currently active voice call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qft_qzv_nva8" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether there is an active voice call.Valid values:

-   true: There is an active voice call.
-   false: There isn't an active voice call.

</td></tr></tbody>
</table>The following code example checks if a voice call is in progress.

```
val voiceService = NowVoiceSDK.makeVoiceService(instanceUrl).getOrNull()

val endpoint = voiceService?.nowVoiceEndpoints?.first()
voiceService?.start(activity, endpoint = endpoint, theme = theme)

// Guard UI state or prevent starting a second call
if (voiceService?.hasActiveCall() == true) {
    // A voice call is currently in progress
}
```

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

[NowVoiceEndpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceEndpointAndroidClass.md)

</td><td>

The voice agent endpoint to connect to. Obtain from `NowVoiceService.nowVoiceEndpoints`.

</td></tr><tr><td>

uiConfiguration

</td><td>

[NowVoiceUiConfiguration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NVoiceUiConfigAndroidClass.md)

</td><td>

Optional. Presentation options for the voice agent UI. If omitted, uses the default values for NowVoiceUiConfiguration.

</td></tr><tr><td>

callbacks

</td><td>

[NowVoiceCallbacks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceCallbacksAndroidInt.md)?

</td><td>

Optional. Callbacks for voice session events. If `null`, events are silently ignored.

</td></tr><tr><td>

theme

</td><td>

[NowVoiceTheme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.md)

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

## NowVoiceService - toggleMute\(\)

Toggles the microphone mute state of the current call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qft_qzv_nva7" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates the new microphone mute state for the current call.Valid values:

-   true: The microphone is now muted.
-   false: The microphone is now unmuted or no call is active.

</td></tr></tbody>
</table>The following code example toggles and reads the microphone mute state.

```
val voiceService = NowVoiceSDK.makeVoiceService(instanceUrl).getOrNull()

val endpoint = voiceService?.nowVoiceEndpoints?.first()
voiceService?.start(activity, endpoint = endpoint, theme = theme)

// Wire to a custom mute button or auto-mute on backgrounding
voiceService?.toggleMute()

// Check mute state to update a custom mute button icon
val muted = voiceService?.isMuted ?: false
```

## NowVoiceService - updateTheme\(theme: NowVoiceTheme\)

Updates the visual theme of the currently active voice UI.

This function has no effect if no voice session is currently active. To apply a visual theme at voice session launch, provide a theme when calling [start\(context:endpoint:uiConfiguration:callbacks:theme:\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md).

|Name|Type|Description|
|----|----|-----------|
|theme|[NowVoiceTheme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.md)|The theme to apply to the active voice UI.|

|Type|Description|
|----|-----------|
|None| |

The following code example updates the visual theme of the currently active voice UI.

```
val voiceService = NowVoiceSDK.makeVoiceService(instanceUrl).getOrNull()

val endpoint = voiceService?.nowVoiceEndpoints?.first()
voiceService?.start(activity, endpoint = endpoint, theme = theme)

// React to dark mode changes or apply brand colors at runtime
voiceService?.updateTheme(NowVoiceThemeDark())
```

