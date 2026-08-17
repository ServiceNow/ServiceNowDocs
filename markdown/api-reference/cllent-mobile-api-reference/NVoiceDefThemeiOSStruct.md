---
title: NowVoiceDefaultTheme structure - iOS
description: The default implementation of NowVoiceThemeable.Creates an instance of NowVoiceDefaultTheme using the specified NowUIThemeable as the source for voice UI colors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NVoiceDefThemeiOSStruct.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceDefaultTheme structure- iOS

The default implementation of NowVoiceThemeable.

**Parent Topic:**[Mobile SDK - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKiOSAPI.md)

**Related topics**  


[NowVoiceThemeable protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NVoiceThemeableiOSProtocol.md)

## NowVoiceDefaultTheme - init\(nowUITheme: NowUIThemeable\)

Creates an instance of NowVoiceDefaultTheme using the specified NowUIThemeable as the source for voice UI colors.

<table id="table_pft_qzv_nvo6" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

nowUITheme

</td><td>

NowUIThemeable

</td><td>

Optional. Theme to use as the source for voice UI colors. Default: `NowUIDefaultTheme`

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
// Use the default NowUI theme
let theme = NowVoiceDefaultTheme()

// Or derive voice UI colors from a custom NowUI theme
let customTheme = NowVoiceDefaultTheme(nowUITheme: MyNowUITheme())
```

