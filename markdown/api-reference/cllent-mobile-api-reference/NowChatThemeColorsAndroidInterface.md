---
title: NowChatTheme interface - Android
description: The NowChatTheme interface defines default colors for the elements in the Live Agent and Virtual Agent chat UI.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatTheme interface - Android

The NowChatTheme interface defines default colors for the elements in the Live Agent and Virtual Agent chat UI.

The NowChatTheme interface extends the NowUITheme interface and inherits the property **nowUIColoring**.

`val nowUIColoring: NowUIColoring?`

You can modify these default colors and create your own themes for your specific chat implementation.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alertCritical0

</td><td>

Alert text background.Default value: \#F8C8CD

</td></tr><tr><td>

alertCritical2

</td><td>

Alert text icon color.Default value: \#E42338

</td></tr><tr><td>

alertCritical3

</td><td>

Alert text icon and bar.Default value: \#B61C2D

</td></tr><tr><td>

alertCritical4

</td><td>

New message divider.Default value: \#891522

</td></tr><tr><td>

alertInfoZero

</td><td>

Highlighting conversation items.Default value: \#BDDCF2

</td></tr><tr><td>

alertInfoTwo

</td><td>

Highlighting conversation items.Default value: \#0079CC

</td></tr><tr><td>

alertModerate3

</td><td>

Alert and search result icons.Default value: \#5D46B6

</td></tr><tr><td>

backgroundPrimary

</td><td>

Neutral background, choice picker, input background, and card background.Default value: \#FFFFFF

</td></tr><tr><td>

backgroundPrimaryActionable

</td><td>

Pagination selected, popup background.Default value: \#151920

</td></tr><tr><td>

backgroundSecondary

</td><td>

Bottom bar, columns in cards, search background in choice picker.Default value: \#F6F6F8

</td></tr><tr><td>

backgroundSecondaryActionable

</td><td>

Clickable input such as search background \(15%\) or date and time background \(100%\).Default value: \#2C323F

</td></tr><tr><td>

backgroundTertiary

</td><td>

Agent and bot bubble background.Default value: \#E4E6EA

</td></tr><tr><td>

backgroundTertiaryActionable

</td><td>

Offline banner background.Default value: \#454D5B

</td></tr><tr><td>

boarderTertiary

</td><td>

Chat input boardersDefault value: \#D3D6DC

</td></tr><tr><td>

brand

</td><td>

HeadersDefault value: \#302F4B

</td></tr><tr><td>

brandBackground

</td><td>

User bubble background.Default value: \#D1D2EE

</td></tr><tr><td>

destructive

</td><td>

Destructive action on buttons.Default value: \#B61C2D

</td></tr><tr><td>

highlightBlue

</td><td>

Inline citation items.Default value: \#D9F4F9

</td></tr><tr><td>

highlightGray

</td><td>

Inline citation item background.Default value: \#E8EAEA

</td></tr><tr><td>

linkPrimary

</td><td>

Link on neutral background. For disabled links use 25% opacity with same color.Default value: \#3C59E7

</td></tr><tr><td>

linkSecondary

</td><td>

Links on non-neutral \(not \#FFFFFF\) background.Default value: \#293D9E

</td></tr><tr><td>

mandatory

</td><td>

Mandatory input field indicator.Default value: \#E42338

</td></tr><tr><td>

navigation

</td><td>

Navigation icon background.Default value: \#454D58

</td></tr><tr><td>

notification

</td><td>

New message indicator.Default value: \#B61C2D

</td></tr><tr><td>

primary

</td><td>

Actionable text and button background.Default value: \#4F52BD

</td></tr><tr><td>

screenHeaderText

</td><td>

Text and icon elements with fixed color that appear on top of brand color \(screen header\).Default value: \#FFFFFF

</td></tr><tr><td>

secondary

</td><td>

User's swiping motion.Default value: \#1C1D42

</td></tr><tr><td>

separatorSecondary

</td><td>

Divider linesDefault value: \#B0B5BF

</td></tr><tr><td>

separatorTertiary

</td><td>

Divider linesDefault value: \#D3D6DC

</td></tr><tr><td>

shadow

</td><td>

Card shadow \(15%\)Default value: \#151920

</td></tr><tr><td>

textActionable

</td><td>

Text on buttons or highlighted background.Default value: \#FFFFFF

</td></tr><tr><td>

textPrimary

</td><td>

Chat bubble text, card header.Default value: \#151920

</td></tr><tr><td>

textSecondary

</td><td>

Card content, search bar icon, and text.Default value: \#2C323F

</td></tr><tr><td>

textTertiary

</td><td>

Weekday for calendar, placeholder.Default value: \#454D5B

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

