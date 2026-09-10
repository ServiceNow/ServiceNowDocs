---
title: NowVoiceService class - iOS
description: The NowVoiceService class manages voice agent sessions for a single ServiceNow instance.Ends the current voice call.Checks whether there is a currently active voice call.Creates a UIViewController containing the voice agent UI, ready to be presented in a modal.Toggles the microphone mute state of the current call.Updates the visual theme of the currently active voice UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 5
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceService class- iOS

The NowVoiceService class manages voice agent sessions for a single ServiceNow instance.

**Note:** Initialize a NowVoiceService by calling [NowVoice - makeVoiceService\(instanceUrl: URL\) async throws](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceiOSAPI.md).

<table id="table_vx2_klw_nv1" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

[NowServiceConfiguration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowServiceConfigurationiOSStruct.md)

</td><td>

The service configuration for the ServiceNow instance.

</td></tr><tr><td>

configurations

</td><td>

Array of [NowVoiceEndpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceEndpointiOSStruct.md)

</td><td>

List of available voice endpoint configurations retrieved from the instance.

</td></tr><tr><td>

isMuted

</td><td>

Bool

</td><td>

Flag that indicates the microphone mute state for the current call. Setting this property has no effect if no call is currently active.Valid values:

-   true: The microphone is muted.
-   false: The microphone is unmuted or no call is active.

</td></tr><tr><td>

voiceEnabled

</td><td>

Bool

</td><td>

Flag that indicates whether voice is enabled on the instance. Valid values:

-   true: Voice is enabled.
-   false: Voice is turned off.

 Always `true` after a NowVoiceService is successfully initialized with [makeVoiceService\(instanceUrl:\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceiOSAPI.md).

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

## NowVoiceService - endCall\(\)

Ends the current voice call.

Has no effect if no call is active.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
let voiceService = try? await NowVoice.makeVoiceService(instanceUrl: instanceUrl)
let endpoint = voiceService?.configurations.first

if let voiceService, let endpoint {
    if let vc = try? await voiceService.startVoice(endpoint: endpoint, theme: theme) {
        vc.modalPresentationStyle = .fullScreen
        present(vc, animated: true)
    }
}

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
</table>The following code example shows how to call this function.

```
let voiceService = try? await NowVoice.makeVoiceService(instanceUrl: instanceUrl)
let endpoint = voiceService?.configurations.first

if let voiceService, let endpoint {
    if let vc = try? await voiceService.startVoice(endpoint: endpoint, theme: theme) {
        vc.modalPresentationStyle = .fullScreen
        present(vc, animated: true)
    }
}

// Guard UI state or prevent starting a second call
if voiceService?.hasActiveCall() == true {
    // A voice call is currently in progress
}
```

## NowVoiceService - startVoice\(endpoint: NowVoiceEndpoint, uiConfiguration: NowVoiceUIConfiguration, callbacks: NowVoiceCallbacks, theme: NowVoiceThemeable\) async throws

Creates a UIViewController containing the voice agent UI, ready to be presented in a modal.

The UIViewController manages the full voice session lifecycle, including teardown on dismissal.

This function fetches an OAuth access token automatically before launching the voice UI.

<table id="table_pft_qzv_nvo2" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

endpoint

</td><td>

[NowVoiceEndpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceEndpointiOSStruct.md)

</td><td>

The voice agent channel to connect to. Obtain from [`NowVoiceService.configurations`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md). Endpoints are retrieved from your ServiceNow instance's Mobile SDK settings.

</td></tr><tr><td>

uiConfiguration

</td><td>

[NowVoiceUIConfiguration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceUIConfigiOSStruct.md)

</td><td>

Optional. Presentation options for the voice agent UI. If omitted, uses the default values for NowVoiceUIConfiguration.

</td></tr><tr><td>

callbacks

</td><td>

[NowVoiceCallbacks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceCallbacksiOSStruct.md)

</td><td>

Optional. Callbacks for voice session events. If omitted, events are silently ignored.

</td></tr><tr><td>

theme

</td><td>

[NowVoiceThemeable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NVoiceThemeableiOSProtocol.md)

</td><td>

Optional. The visual theme applied to the voice UI.Default: [`NowVoiceDefaultTheme`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NVoiceDefThemeiOSStruct.md)

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|UIViewController|A UIViewController containing the full-screen voice agent interface. Present it in a modal. Set `modalPresentationStyle = .fullScreen` for the intended experience.|

The following code example shows how to call this function.

```
import NowVoice

let instanceUrl = URL(string: "https://your-instance.service-now.com")!

let voiceService = try? await NowVoice.makeVoiceService(instanceUrl: instanceUrl)

guard let voiceService, let endpoint = voiceService.configurations.first else {
    // Either the service failed to initialize, or no voice endpoints are configured.
    return
}

// Launch the voice agent UI
let vc = try await voiceService.startVoice(
    endpoint: endpoint,
    uiConfiguration: NowVoiceUIConfiguration(
        hidesPostCallTranscript: false,
        shouldBlockTranscriptSharing: false
    ),
    callbacks: NowVoiceCallbacks(
        onMuteStateChanged: { isMuted in
            // Update your UI to reflect the current mute state.
            print("Microphone muted: \(isMuted)")
        },
        onMessageReceived: { message in
            // Receive real-time transcript messages during the session.
            print("[\(message.role)]: \(message.content)")
        },
        onCallEnded: { conversationId, error, endedFromCallKitUI in
            // Called when the voice session ends.
            if let error {
                print("Session ended with error: \(error)")
            } else {
                print("Session complete. Conversation ID: \(conversationId ?? "unknown")")
            }
        },
        onCallMinimized: {
            // Called when the voice UI is minimized.
            print("Voice chat is minimized")
        }
    ),
    theme: NowVoiceDefaultTheme()
)

//Present the voice agent UI in a full-screen modal
vc.modalPresentationStyle = .fullScreen
present(vc, animated: true)
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

Bool

</td><td>

Flag that indicates the new microphone mute state for the current call.Valid values:

-   true: The microphone is now muted.
-   false: The microphone is now unmuted or no call is active.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
let voiceService = try? await NowVoice.makeVoiceService(instanceUrl: instanceUrl)

let endpoint = voiceService?.configurations.first

if let voiceService, let endpoint {
    if let vc = try? await voiceService.startVoice(endpoint: endpoint, theme: theme) {
        vc.modalPresentationStyle = .fullScreen
        present(vc, animated: true)
    }
}

// Wire to a custom mute button or auto-mute on backgrounding
voiceService?.toggleMute()

// Check mute state to update a custom mute button icon
let muted = voiceService?.isMuted ?? false
```

## NowVoiceService - updateTheme\(theme: NowVoiceThemeable\)

Updates the visual theme of the currently active voice UI.

This function has no effect if no voice session is currently active. To apply a visual theme at voice session launch, provide a theme when calling [startVoice\(endpoint:uiConfiguration:callbacks:theme:\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md).

|Name|Type|Description|
|----|----|-----------|
|theme|NowVoiceThemeable|The theme to apply to the active voice UI.|

|Type|Description|
|----|-----------|
|None| |

The following code example updates the visual theme of the currently active voice UI.

```
import NowVoice

let instanceUrl = URL(string: "https://your-instance.service-now.com")!
let voiceService = try? await NowVoice.makeVoiceService(instanceUrl: instanceUrl)

struct MyVoiceTheme: NowVoiceThemeable { var color: NowUIColoring = MyAppColors()}

// Update the theme while a voice session is active
voiceService?.updateTheme(theme: MyVoiceTheme())
```

