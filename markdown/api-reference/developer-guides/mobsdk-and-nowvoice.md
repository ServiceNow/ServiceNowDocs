---
title: Embed an AI voice agent with NowVoice
description: Use the NowVoice module to embed a real-time AI voice agent session into your Android application.Configure NowVoice to add a real-time voice agent to your Android application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/mobsdk-and-nowvoice.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 4
breadcrumb: [Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Embed an AI voice agent with NowVoice

Use the NowVoice module to embed a real-time AI voice agent session into your Android application.

## NowVoice features

NowVoice gives your app a complete, ready-to-launch voice agent experience. When a user starts a voice agent session, the SDK:

-   Authenticates against your ServiceNow instance using the token your app provides.
-   Opens a WebSocket connection to the configured voice agent endpoint.
-   Launches a full-screen `Activity` with microphone controls and a live transcript.
-   Delivers real-time transcript messages and mute-state changes to your app through callbacks.
-   Shows an optional post-call transcript summary screen on session end.

All public types in the NowVoice module are in the `com.servicenow.nowsdk.voice` package.

## Theming

NowVoice integrates with the NowUI theming system. Implement [`NowVoiceTheme`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.md) to apply custom colors. [`NowVoiceThemeDark`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceThemeDarkAndroidClass.md) is provided as a built-in alternative to the default light theme.

## Mobile SDK instance settings

The NowVoice module reads the following keys from your ServiceNow instance's Mobile SDK settings response.

```
{
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
```

## Configure NowVoice

Configure NowVoice to add a real-time voice agent to your Android application.

### Before you begin

Role required: admin

-   Mobile SDK 2.22.0 or later must be added to your project via Gradle.
-   Your ServiceNow instance must have voice agent services enabled. Confirm that `sdk.voice.enabled` is `true` in the Mobile SDK settings.

### Procedure

1.  Declare permissions in your app's `AndroidManifest.xml`.

    NowVoice requires microphone and internet permissions:

    ```xml
    <uses-permission android:name="android.permission.RECORD_AUDIO" />
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    ```

    **Note:** `RECORD_AUDIO` is a classified as a dangerous \(runtime\) permission. It must also be requested at runtime on Android 6.0 \(API 23\) and later. When permission is needed, NowVoice SDK automatically triggers a request before calling [`NowVoiceService.start()`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md).

2.  Configure NowSDK.

    If you have not already done so, call [`NowSDK.configure()`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowSDKAndroidAPI.md) once at app launch. NowVoice requires NowSDK to be configured before any voice operations.

    ```kotlin
    import com.servicenow.nowsdk.NowSDK
    import com.servicenow.nowsdk.NowSDKConfiguration
    
    NowSDK.configure(
        NowSDKConfiguration.Builder(this)
            .authorizationProvider(yourAuthProvider)
            .build()
    )
    ```

3.  Create a NowVoiceService.

    Import NowVoice and call [`NowVoiceSDK.makeVoiceService(instanceURL)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceSDKAndroidAPI.md). This is a suspend function; call it from a coroutine scope.

    ```kotlin
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

4.  Select a voice endpoint.

    Use [`NowVoiceService.nowVoiceEndpoints`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md) to retrieve the available voice endpoints. In most apps there is a single endpoint.

    ```kotlin
    val endpoint = voiceService.nowVoiceEndpoints.firstOrNull() ?: return
    ```

5.  Launch the voice UI.

    Call [`start(context:endpoint:uiConfiguration:callbacks:theme:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md) to launch the full-screen voice agent Activity. This is a suspend function that returns after the session ends.

    ```kotlin
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

6.  Apply a custom theme.

    To apply custom colors, implement [`NowVoiceTheme`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.md) and pass it to [`start(context:endpoint:uiConfiguration:callbacks:theme:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md) or [`updateTheme(theme:)`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md). Or, use the [prebuilt dark theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceThemeDarkAndroidClass.md).

    ```kotlin
    // Prebuilt dark theme
    voiceService.start(context, endpoint, theme = NowVoiceThemeDark())
    
    // Custom theme
    val myTheme = object : NowVoiceTheme {
        override val primary: Int = Color.parseColor("#0072C6")
        override val backgroundPrimary: Int = Color.parseColor("#FFFFFF")
        // ... override additional properties as needed
    }
    
    // Apply theme at voice session launch
    voiceService.start(context, endpoint, theme = myTheme)
    
    // Or update theme while a voice session is active
    voiceService.updateTheme(NowVoiceThemeDark())
    ```


### Result

The voice agent Activity launches full-screen. The user can begin a real-time voice session with transcript and mute-state updates delivered to your app through the configured callbacks.

### Complete example

```kotlin
import com.servicenow.nowsdk.voice.*
import kotlinx.coroutines.launch
import java.net.URL

class MainActivity : AppCompatActivity() {

    private fun launchVoiceSession() {
        lifecycleScope.launch {
            val result = NowVoiceSDK.makeVoiceService(
                instanceURL = URL("https://your-instance.service-now.com")
            )

            result.onSuccess { voiceService ->
                val endpoint = voiceService.nowVoiceEndpoints.firstOrNull() ?: return@onSuccess

                voiceService.start(
                    context = this@MainActivity,
                    endpoint = endpoint,
                    callbacks = object : NowVoiceCallbacks {
                        override fun onCallEnd(conversationId: String?, error: NowVoiceError?) {
                            runOnUiThread { updateUI(ended = true) }
                        }

                        override fun onMuteStateChanged(isMuted: Boolean) {
                            runOnUiThread { updateMuteButton(isMuted) }
                        }

                        override fun onMessageReceived(message: TranscriptMessage) {
                            runOnUiThread { appendTranscript(message) }
                        }
                    }
                )
            }.onFailure { error ->
                Log.e("NowVoice", "Failed: $error")
            }
        }
    }
}
```

