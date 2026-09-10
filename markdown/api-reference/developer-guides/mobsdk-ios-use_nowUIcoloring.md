---
title: Use NowUIColoring to create themes
description: Use NowUIColoring to create themes with NowWebThemeable, NowChatThemeable, and NowVoiceThemeable. The NowUIColoring interface contains all the colors used by all NowSDK modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/developer-guides/mobsdk-ios-use\_nowUIcoloring.html
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Use NowUIColoring to create themes

Use NowUIColoring to create themes with NowWebThemeable, NowChatThemeable, and NowVoiceThemeable. The NowUIColoring interface contains all the colors used by all NowSDK modules.

For scenarios where you use similar color variables across multiple SDK modules, you can implement the NowUIColoring interface. Using this interface you can override color values and then use that implementation to override the NowUIColoring values inside the theme classes [NowWebThemeable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowWebThemeableiOSProtocol.md), [NowChatThemeable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NowChatThemeableiOSProtocol.md), and [NowVoiceThemeable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/NVoiceThemeableiOSProtocol.md). If color variables aren’t overridden, the NowUIColoring interface uses the default colors.

NowWebThemeable contains specific colors that only pertain to NowWeb, NowChatThemeable contains specific colors that only pertain to NowChat, and NowVoiceThemeable contains specific colors that only pertain to NowVoice. Common colors are defined by NowUIColoring. NowUIColoring also contains all the default colors.

The default colors use the Coral theme \(light\).

|Name|Default|
|----|-------|
|alertCritical0|\#F8C8CD|
|alertCritical2|\#E42338|
|alertCritical3|\#B61C2D|
|alertLow0|\#DBDBDE|
|alertPositive0|\#C7DCB5|
|alertPositive3|\#3E8600|
|alertWarning0|\#FBF7BF|
|backgroundPrimary|\#FFFFFF|
|backgroundPrimaryActionable|\#10171A|
|backgroundSecondary|\#F3F8F9|
|backgroundSecondaryActionable|\#232E33|
|backgroundTertiary|\#E5EDF0|
|borderTertiary|\#CFD5D7|
|brand|\#032D42|
|brandBackground|\#BDDEE7|
|destructive|\#B61C2D|
|linkPrimaryText|\#1955BE|
|linkSecondary|\#113A82|
|notification|\#B61C2D|
|primary|\#00566E|
|screenHeaderBackground|\#CADFC0|
|screenHeaderText|\#FFFFFF|
|secondary|\#042731|
|separatorPrimary|\#859095|
|separatorTertiary|\#CFD5D7|
|shadow|\#0D1A1E|
|textActionable|\#FFFFFF|
|textPrimary|\#172B31|
|textSecondary|\#294149|
|textTertiary|\#4A5E65|

