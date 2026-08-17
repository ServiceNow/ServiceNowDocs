---
title: NowVoiceTranscriptMessage typealias - iOS
description: Represents a single message in the voice session transcript.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NVoiceTrnstMsgiOSta.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceTranscriptMessage typealias- iOS

Represents a single message in the voice session transcript.

NowVoiceTranscriptMessage is a type alias for `TranscriptMessage`.

|Name|Type|Description|
|----|----|-----------|
|role|String|The originator of the message. Typical values are `"user"` and `"assistant"`.|
|text|String|The text content of the message.|

The following code example shows NowVoiceTranscriptMessage used with `[NowVoiceCallbacks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceCallbacksiOSStruct.md)`.

```
onMessageReceived: { message in
    print("[\(message.role)]: \(message.text)")
}
```

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

