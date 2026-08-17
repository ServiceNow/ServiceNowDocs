---
title: Embed an AI voice agent with NowVoice
description: Use the NowVoice module to embed a real-time AI voice agent session into your iOS application.Configure NowVoice to add a real-time voice agent to your iOS application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/developer-guides/mobsdk-ios-nowvoice.html
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 5
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Embed an AI voice agent with NowVoice

Use the NowVoice module to embed a real-time AI voice agent session into your iOS application.

## NowVoice features

NowVoice gives your app a complete, ready-to-present voice agent UI. When a user starts a voice agent session, the SDK:

-   Authenticates against your ServiceNow instance using the token your app provides.
-   Opens a WebSocket connection to the configured voice agent endpoint.
-   Renders a full-screen native SwiftUI view with microphone controls and a live transcript.
-   Delivers real-time transcript messages and mute-state changes to your app through callbacks.
-   Shows an optional post-call transcript summary screen on session end.

## Theming

NowVoice integrates with the NowUI theming system. Pass any type conforming to [`NowVoiceThemeable`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NVoiceThemeableiOSProtocol.md) to apply custom colors. [`NowVoiceDefaultTheme`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NVoiceDefThemeiOSStruct.md) is provided as a default.

## NowChat integration

If your app uses NowChat, you can enable NowVoice in the chat interface. Set [`NowChatConfiguration`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatOptionsiOS.md) properties to configure voice within the NowChat UI and add a voice button. Tapping it launches the voice agent UI as a full-screen overlay within the chat flow.

## Mobile SDK instance settings

The NowVoice module reads the following keys from your ServiceNow instance's Mobile SDK settings response.

```
{
  "sdk": {
    "voice": {
      "enabled": true,
      "configurations": [
        {
          "voiceServiceId": "String",
          "voiceWebhookURL": "String",
          "mobileChannelType": "String",
          "mobileChannelId": "String"
        }
      ]
    }
  }
}
```

## Configure NowVoice

Configure NowVoice to add a real-time voice agent to your iOS application.

### Before you begin

Role required: admin

-   Mobile SDK 2.22.0 or later must be added to your Xcode project via Swift Package Manager.
-   Your ServiceNow instance must have voice agent services enabled. Confirm that `sdk.voice.enabled` is `true` in the Mobile SDK settings.

### Procedure

1.  Add microphone usage description.

    Add the `NSMicrophoneUsageDescription` key to your app's `Info.plist`:

    ```xml
    <key>NSMicrophoneUsageDescription</key>
    <string>This app uses your microphone to communicate with the ServiceNow voice agent.</string>
    ```

    **Note:** Omitting this key can cause iOS to crash the app when the voice session begins.

2.  Configure NowSDK.

    If you have not already done so, configure NowSDK once at app launch. NowVoice requires NowSDK to be configured before any voice operations.

    1.  Call [`NowSDK.configure(with:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowSDKAPIiOS.md).

        ```swift
        import NowSDK
        
        try NowSDK.configure(with: NowSDKConfiguration(
            authorizationProvider: self,
            permissionDelegate: self,
            logLevel: .error
        ))
        ```

    2.  Implement `NowSDKAuthorizationProviding` to supply OAuth tokens for your instance.

        ```swift
        func requestAuthorization(for instanceUrl: URL, completion: @escaping ([AuthorizationToken]?) -> Void) {
            // Retrieve and return your OAuth tokens here.
            completion(yourTokens)
        }
        ```

    3.  Implement `DevicePermissionDelegate` to allow microphone access.

        ```swift
        func canRequestPermission(_ permission: DevicePermission) -> Bool {
            return true
        }
        ```

3.  Create a NowVoiceService.

    Import NowVoice and call [`makeVoiceService(instanceUrl:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceiOSAPI.md) with the URL of your ServiceNow instance. This is an async function; call it from an async context or a Task.

    ```swift
    import NowVoice
    
    let instanceUrl = URL(string: "https://your-instance.service-now.com")!
    
    do {
        let voiceService = try await NowVoice.makeVoiceService(instanceUrl: instanceUrl)
    } catch {
        // Handle NowServiceError
        print("Failed to create voice service: \(error)")
    }
    ```

4.  Select a voice endpoint.

    Use [`NowVoiceService.configurations`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md) to retrieve the available voice endpoints. In most apps, there is a single endpoint.

    ```swift
    guard let endpoint = voiceService.configurations.first else {
        // No voice endpoints configured on this instance.
        return
    }
    ```

5.  Launch the voice UI.

    Call [`startVoice(endpoint:uiConfiguration:callbacks:theme:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md) to obtain a `UIViewController` with the voice agent UI. Present it full-screen.

    ```swift
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
                print("[\(message.role)]: \(message.text)")
            },
            onCallEnded: { conversationId, error in
                // Called when the voice session ends.
                if let error {
                    print("Session ended with error: \(error)")
                } else {
                    print("Session complete. Conversation ID: \(conversationId ?? "unknown")")
                }
            }
        ),
        theme: NowVoiceDefaultTheme()
    )
    
    vc.modalPresentationStyle = .fullScreen
    present(vc, animated: true)
    ```

    **Note:** `startVoice()` fetches an OAuth access token automatically before launching the voice UI.

6.  Apply a custom theme.

    To match the voice UI to your app's visual identity, create a type conforming to [`NowVoiceThemeable`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NVoiceThemeableiOSProtocol.md) and pass it to [`startVoice(endpoint:uiConfiguration:callbacks:theme:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md) or [`updateTheme(theme:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md).

    ```swift
    struct MyVoiceTheme: NowVoiceThemeable {
        var color: NowUIColoring = MyAppColors()
    }
    
    // Apply at voice session launch
    let vc = try await voiceService.startVoice(endpoint: endpoint, theme: MyVoiceTheme())
    
    // Or update while a voice session is active
    voiceService.updateTheme(theme: MyVoiceTheme())
    ```

7.  Embed voice inside NowChat.

    If your app already uses NowChat, you can enable NowVoice in the chat interface. Pass the voice configuration directly to [`NowChatConfiguration`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatOptionsiOS.md). A voice button appears in the chat UI automatically when a valid voice endpoint is provided.

    **Note:** When using NowChat with voice, don't call [`startVoice(endpoint:uiConfiguration:callbacks:theme:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceiOSAPI.md) to launch the voice UI. NowChat manages the voice session lifecycle internally.

    ```swift
    import NowChat
    import NowVoice
    
    // voiceConfiguration is optional — omit it to have the SDK use instance settings automatically
    let chatConfig = NowChatConfiguration(
        closePrompt: NowChatConfiguration.ClosePrompt(
            header: "Leave chat?",
            message: "Your conversation will end.",
            acceptButtonTitle: "Leave",
            declineButtonTitle: "Stay"
        ),
        disabledFeatures: [],
        conversationOptions: [.forceNewConversation],
        uiConfiguration: NowChatConfiguration.UIConfiguration(
            closeButton: .text("Close"),
            attachmentUploadButton: .init(isVisible: true),
            hideBranding: false
        ),
        voiceConfiguration: voiceService.configurations.first, // optional endpoint override
        voiceUIConfiguration: NowVoiceUIConfiguration(
            hidesPostCallTranscript: false,
            shouldBlockTranscriptSharing: false
        ),
        voiceCallbacks: NowVoiceCallbacks(
            onMuteStateChanged: { isMuted in
                print("Muted: \(isMuted)")
            },
            onMessageReceived: { message in
                print("Transcript: \(message)")
            },
            onCallEnded: { conversationId, error in
                // Called when the embedded voice session ends
            }
        )
    )
    
    let chatVC = try await chatService.startChat(configuration: chatConfig)
    present(chatVC, animated: true)
    ```


### Result

The voice agent UI is presented full-screen. The user can begin a real-time voice session with transcript and mute-state updates delivered to your app through the configured callbacks.

### Complete example

```swift
import NowSDK
import NowVoice

// --- App launch ---
try NowSDK.configure(with: NowSDKConfiguration(
    authorizationProvider: self,
    permissionDelegate: self
))

// --- When the user taps "Start Voice" ---
func startVoiceSession() async {
    let instanceUrl = URL(string: "https://your-instance.service-now.com")!

    do {
        let voiceService = try await NowVoice.makeVoiceService(instanceUrl: instanceUrl)

        guard let endpoint = voiceService.configurations.first else { return }

        let vc = try await voiceService.startVoice(
            endpoint: endpoint,
            callbacks: NowVoiceCallbacks(
                onMuteStateChanged: { [weak self] isMuted in
                    self?.updateMuteIndicator(isMuted: isMuted)
                },
                onMessageReceived: { [weak self] message in
                    self?.appendTranscript(message)
                },
                onCallEnded: { [weak self] _, error in
                    self?.dismiss(animated: true)
                }
            )
        )
        vc.modalPresentationStyle = .fullScreen
        present(vc, animated: true)

    } catch let error as NowServiceError {
        handleServiceError(error)
    }
}
```

