---
title: NowVoiceUIConfiguration structure - iOS
description: Specifies presentation options for the voice agent UI.Creates a NowVoiceUIConfiguration instance with the specified presentation options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowVoiceUIConfigiOSStruct.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceUIConfiguration structure- iOS

Specifies presentation options for the voice agent UI.

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

## NowVoiceUIConfiguration - init\(hidesPostCallTranscript: Bool, shouldBlockTranscriptSharing: Bool\)

Creates a NowVoiceUIConfiguration instance with the specified presentation options.

<table id="table_pft_qzv_nvo4" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

hidesPostCallTranscript

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the post-call transcript summary screen is displayed or hidden when the session ends.Valid values:

-   true: The post-call transcript summary screen is hidden.
-   false: The post-call transcript summary screen is displayed.

Default: False

</td></tr><tr><td>

shouldBlockTranscriptSharing

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the **Share** button is displayed or hidden on the transcript screen.Valid values:

-   true: The share button is hidden.
-   false: The share button is displayed.

Default: False

</td></tr></tbody>
</table>The following code example shows how to create an instance of NowVoiceUIConfiguration.

```
let uiConfiguration = NowVoiceUIConfiguration(
    hidesPostCallTranscript: true,
    shouldBlockTranscriptSharing: true
)
```

