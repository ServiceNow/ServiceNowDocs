---
title: NowVoiceCallbacks interface - Android
description: Provides callback functions for voice session lifecycle and content events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NowVoiceCallbacksAndroidInt.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceCallbacks interface- Android

Provides callback functions for voice session lifecycle and content events.

Implement this interface and pass it when calling [`NowVoiceService.start()`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md).

A `NowVoiceError` is delivered as the second parameter of the `onCallEnd()` callback.

|Type|Description|
|----|-----------|
|ConnectionTimeout|The connection to the voice agent timed out.|
|CallInitializationFailed\(message\)|The voice session could not be initialized. The **message** field contains additional detail.|
|ConnectionLost|The network connection dropped during an active session.|
|ServerErrorNow\(message\)|A server error occurred over the data channel.|
|ServerEndedCall|The server terminated the session normally, such as when a session limit is reached.|
|UnexpectedServiceTermination|The system destroyed the voice service unexpectedly.|

|Name|Description|
|----|-----------|
|`onCallEnd(conversationId: String?, error: NowVoiceError? = null)`|Called once when the voice session ends. **conversationId** identifies the completed session and may be `null` if a session was never fully established. **error** is a `NowVoiceError`, or `null` for normal termination.|
|`onMuteStateChanged(isMuted: Boolean)`|Called each time the user mutes or unmutes the microphone. **isMuted** is `true` when the microphone is muted.|
|`onMessageReceived(message: TranscriptMessage)`|Called each time a new transcript message arrives during the session. For more information, see [`Transcript Message`](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/TranscriptMsgAndroidClass.md).|
|`onCallMinimized()`|Called when the voice session UI is minimized by the user.|

The following code example shows how to implement NowVoiceCallbacks. In each callback function, implement the desired functionality for handling the event.

```
val callbacks = object : NowVoiceCallbacks {
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

    override fun onCallMinimized() {
        Log.e("NowVoice", "Voice chat is minimized")
    }
}
```

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

