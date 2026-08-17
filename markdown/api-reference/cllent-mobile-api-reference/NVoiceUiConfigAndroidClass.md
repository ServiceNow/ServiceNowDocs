---
title: NowVoiceUiConfiguration class - Android
description: Specifies presentation options for the voice agent UI.Creates a NowVoiceUiConfiguration instance with the specified presentation options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NVoiceUiConfigAndroidClass.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceUiConfiguration class- Android

Specifies presentation options for the voice agent UI.

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

## NowVoiceUiConfiguration - NowVoiceUiConfiguration\(hidePostCallTranscript: Boolean = false, shouldBlockAttachmentSharing: Boolean = false\)

Creates a NowVoiceUiConfiguration instance with the specified presentation options.

<table id="table_pft_qzv_nva4" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hidePostCallTranscript

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the post-call transcript summary screen is displayed or hidden when the session ends.Valid values:

-   true: The post-call transcript summary screen is hidden.
-   false: The post-call transcript summary screen is displayed.

Default: False

</td></tr><tr><td>

shouldBlockAttachmentSharing

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the share button is displayed or hidden on the transcript screen.Valid values:

-   true: The share button is hidden.
-   false: The share button is displayed.

Default: False

</td></tr></tbody>
</table>The following code example shows how to create an instance of NowVoiceUiConfiguration.

```
val uiConfiguration = NowVoiceUiConfiguration(
    hidePostCallTranscript = true,
    shouldBlockAttachmentSharing = true
)
```

