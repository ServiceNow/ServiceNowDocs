---
title: TranscriptMessage class - Android
description: Represents a single message in the voice session transcript.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/TranscriptMsgAndroidClass.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# TranscriptMessage class- Android

Represents a single message in the voice session transcript.

TranscriptMessages are passed to [NowVoiceCallbacks - onMessageReceived\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceCallbacksAndroidInt.md).

<table id="table_vx2_klw_nva5" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

role

</td><td>

Role

</td><td>

The Role object identifies the originator of the message. Possible values:

-   `Role.Assistant`: The message originated from the voice agent.
-   `Role.User`: The message originated from the app user.

</td></tr><tr><td>

content

</td><td>

String

</td><td>

The text content of the message.

</td></tr></tbody>
</table>The following code example shows TranscriptMessage used with NowVoiceCallbacks.

```
override fun onMessageReceived(message: TranscriptMessage) {
    runOnUiThread { appendTranscript(message) }
}
```

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

