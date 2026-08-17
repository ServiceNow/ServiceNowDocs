---
title: NowVoiceCallbacks structure - iOS
description: Specifies callbacks for voice session lifecycle and content events.Creates a NowVoiceCallbacks instance with the specified voice session event handlers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowVoiceCallbacksiOSStruct.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceCallbacks structure- iOS

Specifies callbacks for voice session lifecycle and content events.

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

## NowVoiceCallbacks - init\(onMuteStateChanged: \(\(Bool\) -&gt; Void\)?, onMessageReceived: \(\(NowVoiceTranscriptMessage\) -&gt; Void\)?, onCallEnded: NowVoiceDismissHandler?\)

Creates a NowVoiceCallbacks instance with the specified voice session event handlers.

A `NowVoiceAgentError` is delivered as the second parameter of the **onCallEnded** callback.

|Case|Description|
|----|-----------|
|`.connectionTimeout`|The connection to the voice agent timed out.|
|`.connectionFailed`|A connection to the voice agent could not be established.|
|`.disconnectedUnexpectedly`|The connection dropped during an active session.|
|`.serverEnded`|The server terminated the session.|

<table id="table_pft_qzv_nvo5" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

onMuteStateChanged

</td><td>

\(\(Bool\) -&gt; Void\)?

</td><td>

Called each time the user mutes or unmutes the microphone. The **Bool** parameter is `true` when the microphone is muted.

</td></tr><tr><td>

onMessageReceived

</td><td>

\(\([NowVoiceTranscriptMessage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NVoiceTrnstMsgiOSta.md)\) -&gt; Void\)?

</td><td>

Called each time a new transcript message arrives during the session.

</td></tr><tr><td>

onCallEnded

</td><td>

NowVoiceDismissHandler?

</td><td>

Called when the voice UI is dismissed. Delivers the conversation identifier and an optional error.```
public typealias NowVoiceDismissHandler = (String?, NowVoiceAgentError?) -> Void
```

</td></tr><tr><td>

onCallMinimized

</td><td>

\(\(\) -&gt; Void\)?

</td><td>

Called when the voice session UI is minimized by the user.

</td></tr></tbody>
</table>The following code example shows how to initialize a NowVoiceCallbacks. In each callback function, implement the desired functionality for handling the event.

```
let callbacks = NowVoiceCallbacks(
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
    },
    onCallMinimized: {
        // Called when the voice UI is minimized.
        print("Voice chat is minimized")
    }
)
```

