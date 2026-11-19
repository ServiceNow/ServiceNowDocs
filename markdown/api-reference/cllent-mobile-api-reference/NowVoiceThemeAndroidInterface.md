---
title: NowVoiceTheme interface - Android
description: Customizes the visual appearance of the voice agent UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.html
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceTheme interface- Android

Customizes the visual appearance of the voice agent UI.

Implement NowVoiceTheme to customize the voice agent UI colors. All properties have default light theme implementations; override only what you need. [NowVoiceThemeDark](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowVoiceThemeDarkAndroidClass.md) can be used as a prebuilt dark theme implementation.

This interface extends NowUITheme.

|Name|Default|Description|
|----|-------|-----------|
|actionablePrimaryAIBackgroundColorGradientEnd|\#71D5FE|AI gradient background end color.|
|actionablePrimaryAIBackgroundColorGradientStart|\#86F673|AI gradient background start color.|
|alertCritical0|\#F9C8CE|Error and critical alert background \(close button\).|
|alertCritical4|\#B31B2C|Error and critical alert icon color.|
|alertInfo0|\#BDDCF1|Info alerts background.|
|alertInfo3|\#007AC9|Info alerts level 3.|
|alertLow2|\#96979F|Low priority alerts.|
|backgroundPrimary|\#FFFFFF|Neutral background and dialog background.|
|backgroundSecondary|\#F5F6F7|Secondary background and user message bubbles.|
|brandBackground|\#BDDEE7|Transcript button background when selected.|
|destructive|\#E52239|Destructive actions and error states.|
|highlightGreen|\#BFE1D4|Green highlight in voice chat.|
|highlightYellow|\#F0E2BF|Yellow highlight in voice chat.|
|presenceAvailable|\#4EA800|Presence available indicator in voice chat.|
|primary|\#00566E|Primary action color, transcript icon when selected.|
|secondary|\#002832|Animated background gradient shown during a voice interaction.|
|textActionable|\#FFFFFF|Text on action buttons or highlighted background.|
|textPrimary|\#10171A|Primary text color for UI elements.|
|textSecondary|\#232E33|Secondary text color.|
|textTertiary|\#37444A|Tertiary text color, connection state text.|

Default colors used in the prebuilt light theme.

\[Omitted image "NVoiceThemeAnd.png"\] Alt text: Color palette for NowVoiceTheme prebuilt light theme

The following code example shows a custom implementation of NowVoiceTheme.

```
val myTheme = object : NowVoiceTheme {
    override val primary: Int = Color.parseColor("#0072C6")
    override val backgroundPrimary: Int = Color.WHITE
}

//voiceService is an initialized NowVoiceService
voiceService.start(context, endpoint, theme = myTheme)
```

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

