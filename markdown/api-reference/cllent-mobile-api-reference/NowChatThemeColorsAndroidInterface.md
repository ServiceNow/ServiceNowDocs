---
title: NowChatTheme interface - Android
description: The NowChatTheme interface defines default colors for the elements in the Live Agent and Virtual Agent chat UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/cllent-mobile-api-reference/NowChatThemeColorsAndroidInterface.html
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatTheme interface- Android

The NowChatTheme interface defines default colors for the elements in the Live Agent and Virtual Agent chat UI.

The NowChatTheme interface extends the NowUITheme interface and inherits the property **nowUIColoring**.

`val nowUIColoring: NowUIColoring?`

You can modify these default colors and create your own themes for your specific chat implementation. The default colors use the Coral theme.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

actionableIconPrimaryAI

</td><td>

AI assistant icon tint in output cards.Default value: \#004F65

</td></tr><tr><td>

actionablePrimaryAIBackgroundColorGradientEnd

</td><td>

End color of the AI actionable background gradient in voice chat.Default value: \#71D5FE

</td></tr><tr><td>

actionablePrimaryAIBackgroundColorGradientStart

</td><td>

Start color of the AI actionable background gradient in voice chat.Default value: \#86F673

</td></tr><tr><td>

alertCritical0

</td><td>

Alert text background.Default value: \#F9C8CE

</td></tr><tr><td>

alertCritical2

</td><td>

Alert text icon color.Default value: \#EC596B

</td></tr><tr><td>

alertCritical3

</td><td>

Alert text icon and bar.Default value: \#E52239

</td></tr><tr><td>

alertCritical4

</td><td>

New message divider.Default value: \#B31B2C

</td></tr><tr><td>

alertHigh3

</td><td>

High level alert.Default value: \#C25600

</td></tr><tr><td>

alertInfo0

</td><td>

Highlight conversation items.Default value: \#BDDCF1

</td></tr><tr><td>

alertInfo2

</td><td>

Highlight conversation items.Default value: \#409BD7

</td></tr><tr><td>

alertInfo3

</td><td>

Alert level three \(informational\).Default value: \#007AC9

</td></tr><tr><td>

alertLow2

</td><td>

Alert level two \(low\). Used in voice chat.Default value: \#96979F

</td></tr><tr><td>

alertModerate3

</td><td>

Alert, search result, and AI icons.Default value: \#7B56FF

</td></tr><tr><td>

alertPositive0

</td><td>

Positive alert background.Default value: \#C7DCB5

</td></tr><tr><td>

alertPositive2

</td><td>

Positive alert accent and icon \(mid-tone\).Default value: \#6CA33D

</td></tr><tr><td>

alertPositive3

</td><td>

Positive alert text and icon.Default value: \#3E8600

</td></tr><tr><td>

backgroundPrimary

</td><td>

Neutral background, choice picker, input background, and card background.Default value: \#FFFFFF

</td></tr><tr><td>

backgroundPrimaryActionable

</td><td>

Pagination selected, popup background.Default value: \#10171A

</td></tr><tr><td>

backgroundSecondary

</td><td>

Bottom bar, columns in cards, search background in choice picker.Default value: \#F5F6F7

</td></tr><tr><td>

backgroundSecondaryActionable

</td><td>

Clickable input such as search background \(15%\) or date and time background \(100%\).Default value: \#232E33

</td></tr><tr><td>

backgroundTertiary

</td><td>

Agent and bot bubble background.Default value: \#E2E5E7

</td></tr><tr><td>

backgroundTertiaryActionable

</td><td>

Offline banner background.Default value: \#37444A

</td></tr><tr><td>

borderTertiary

</td><td>

Chat input borders.Default value: \#CFD5D7

</td></tr><tr><td>

brand

</td><td>

Header background in toolbar and tables.Default value: \#032D42

</td></tr><tr><td>

brandBackground

</td><td>

User bubble background.Default value: \#BDDEE7

</td></tr><tr><td>

destructive

</td><td>

Destructive action on buttons.Default value: \#E52239

</td></tr><tr><td>

divider

</td><td>

Divider lines separating banners and content sections.Default value: \#F1F2F3

</td></tr><tr><td>

highlightBlue

</td><td>

Inline citation items.Default value: \#C4DBFE

</td></tr><tr><td>

highlightGray

</td><td>

Inline citation item background.Default value: \#DCDDDE

</td></tr><tr><td>

highlightGreen

</td><td>

Green highlight. Used in voice chat.Default value: \#BFE1D4

</td></tr><tr><td>

highlightYellow

</td><td>

Yellow highlight. Used in voice chat.Default value: \#F0E2BF

</td></tr><tr><td>

linkPrimary

</td><td>

Link on neutral background. For disabled links use 25% opacity with same color.Default value: \#1955BE

</td></tr><tr><td>

linkSecondary

</td><td>

Links on non-neutral \(not \#FFFFFF\) background.Default value: \#113A82

</td></tr><tr><td>

mandatory

</td><td>

Mandatory input field indicator.Default value: \#E52239

</td></tr><tr><td>

messagingIconPrimaryAI

</td><td>

AI sparkle icon and avatar tint in conversation messages.Default value: \#178BAB

</td></tr><tr><td>

navigation

</td><td>

Navigation icon background.Default value: \#737F84

</td></tr><tr><td>

notification

</td><td>

New message indicator.Default value: \#E52239

</td></tr><tr><td>

presenceAvailable

</td><td>

Presence available indicator. Used in voice chat.Default value: \#4EA800

</td></tr><tr><td>

primary

</td><td>

Actionable text and button background.Default value: \#00566E

</td></tr><tr><td>

primaryOne

</td><td>

Greeting message view gradient.Default value: \#0080A3

</td></tr><tr><td>

screenHeaderText

</td><td>

Text and icon elements with fixed color that appear on top of brand color \(screen header\).Default value: \#FFFFFF

</td></tr><tr><td>

secondary

</td><td>

User's swiping motion.Default value: \#002832

</td></tr><tr><td>

separatorSecondary

</td><td>

Dividers.Default value: \#AAB2B6

</td></tr><tr><td>

separatorTertiary

</td><td>

Divider lines.Default value: \#CFD5D7.

</td></tr><tr><td>

shadow

</td><td>

Card shadow \(15%\).Default value: \#10171A

</td></tr><tr><td>

textActionable

</td><td>

Text on buttons or highlighted background.Default value: \#FFFFFF

</td></tr><tr><td>

textPrimary

</td><td>

Chat bubble text, card header.Default value: \#10171A

</td></tr><tr><td>

textSecondary

</td><td>

Card content, search bar icon, and text.Default value: \#232E33

</td></tr><tr><td>

textTertiary

</td><td>

Weekday for calendar, placeholder.Default value: \#37444A

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - Android](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cllent-mobile-api-reference/MobileSDKAndroidAPI.md)

