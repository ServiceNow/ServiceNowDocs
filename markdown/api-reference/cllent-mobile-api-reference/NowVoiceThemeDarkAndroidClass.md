---
title: NowVoiceThemeDark class - Android
description: A prebuilt dark theme implementation of NowVoiceTheme.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowVoiceThemeDarkAndroidClass.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowVoiceThemeDark class- Android

A prebuilt dark theme implementation of NowVoiceTheme.

Apply the dark theme to the voice agent UI by passing it to [NowVoiceService - start\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md) or [NowVoiceService - updateTheme\(\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceServiceAndroidAPI.md).

|Name|Default|Description|
|----|-------|-----------|
|actionablePrimaryAIBackgroundColorGradientEnd|\#71D5FE|AI gradient background end color.|
|actionablePrimaryAIBackgroundColorGradientStart|\#86F673|AI gradient background start color.|
|alertCritical0|\#7B1D28|Error and critical alert background \(close button\).|
|alertCritical4|\#ED9AA3|Error and critical alert icon color.|
|alertInfo0|\#00446B|Info alerts background.|
|alertInfo3|\#3F9CD1|Info alerts level 3.|
|alertLow2|\#717681|Low priority alerts.|
|backgroundPrimary|\#050809|Neutral background and dialog background.|
|backgroundSecondary|\#161F23|Secondary background and user message bubbles.|
|brandBackground|\#002934|Transcript button background when selected.|
|destructive|\#E46775|Destructive actions and error states.|
|highlightGreen|\#1E4A25|Green highlight in voice chat.|
|highlightYellow|\#4A3C00|Yellow highlight in voice chat.|
|messagingIconPrimaryAIColor|\#178BAB|Primary color for AI assistant icons.|
|presenceAvailable|\#4EA800|Presence available indicator in voice chat.|
|primary|\#6CBBD0|Primary action color, transcript icon when selected.|
|secondary|\#99C6D2|Animated background gradient shown during a voice interaction.|
|textActionable|\#050809|Text on action buttons or highlighted background.|
|textPrimary|\#FFFFFF|Primary text color for UI elements.|
|textSecondary|\#E2E5E7|Secondary text color.|
|textTertiary|\#BCC3C7|Tertiary text color, connection state text.|

\[Omitted image "NowVoiceThemeDarkAnd.png"\] Alt text: Color palette for NowVoiceThemeDark

The following code example shows how to use NowVoiceThemeDark.

```
//voiceService is an initialized NowVoiceService

// Apply theme at voice session launch
voiceService.start(context, endpoint, theme = NowVoiceThemeDark())

// Or update theme while a voice session is active
voiceService.updateTheme(NowVoiceThemeDark())
```

**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

**Related topics**  


[NowVoiceTheme interface - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowVoiceThemeAndroidInterface.md)

