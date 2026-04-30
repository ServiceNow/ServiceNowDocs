---
title: NowChatColoring protocol - iOS
description: The NowChatColoring protocol defines default colors for the elements in the Live Agent and Virtual Agent chat UI.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatColoring protocol - iOS

The NowChatColoring protocol defines default colors for the elements in the Live Agent and Virtual Agent chat UI.

You can modify these default colors and create your own themes for your specific chat implementation.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alertCritical0

</td><td>

Color applied to the alert pop-up background.Default dark color: \#7B1E28

Default light color: \#F8C8CD

</td></tr><tr><td>

alertCritical2

</td><td>

Alert text icon color.Default value: \#B61C2D

</td></tr><tr><td>

alertCritical3

</td><td>

This property is deprecated beginning with Mobile SDK Libraries - iOS version 2.11.0.

 Color applied to the alert pop-up icon and bar.

 Default dark color: \#E46876

 Default light color: \#B61C2D

</td></tr><tr><td>

backgroundPrimary

</td><td>

Background color applied to the chat view background, choice picker, input background, and the card background.Default dark color: \#07080B

Default light color: \#FFFFFF

</td></tr><tr><td>

backgroundPrimaryActionable

</td><td>

Background color applied to the pagination selected and pop-up backgrounds.Default dark color: \#FFFFFF

Default light color: \#151920

</td></tr><tr><td>

backgroundSecondary

</td><td>

Background color applied to the bottom bar, columns in cards, and the search background in a choice picker.Default dark color: \#151920

Default light color: \#F6F6F8

</td></tr><tr><td>

backgroundSecondaryActionable

</td><td>

Background color applied to selectable inputs such as the search background and the date/time background.Default dark color: \#C1C5CD

Default light color: \#2C323F

</td></tr><tr><td>

backgroundTertiary

</td><td>

Background color applied to the agent and bot chat bubbles.Default dark color: \#252A35

Default light color: \#E4E6EA

</td></tr><tr><td>

borderTertiary

</td><td>

Color applied to chat input borders.Default dark color: \#454D5B

Default light color: \#D3D6DC

</td></tr><tr><td>

brand

</td><td>

Color applied to the activity indicator shown while loading pages.Default dark color: \#302F4B

Default light color: \#302F4B

</td></tr><tr><td>

brandBackground

</td><td>

Background color applied to the user bubble background.Default dark color: \#28284D

Default light color: \#D1D2EE

</td></tr><tr><td>

destructive

</td><td>

Color applied to UI elements that trigger destructive actions \(e.g.: Delete\)Default dark color: \#E46876

Default light color: \#B61C2D

</td></tr><tr><td>

linkPrimaryText

</td><td>

Color applied to links and UI elements that behave like links.Default dark color: \#647BFD

Default light color: \#3C59E7

</td></tr><tr><td>

linkSecondary

</td><td>

Color applied to links on non-neutral \(non-white\) backgrounds.Default dark color: \#93A3FE

Default light color: \#293D9E

</td></tr><tr><td>

notification

</td><td>

Color applied to the new message indicator.Default dark color: \#E46876

Default light color:\#B61C2D

</td></tr><tr><td>

nowUIColor

</td><td>

Foundation UI color theme used for all NowSDK UI elements.

</td></tr><tr><td>

primary

</td><td>

Color applied to buttons or actionable text.Default dark color: \#8486FF

Default light color: \#4F52BD

</td></tr><tr><td>

screenHeaderText

</td><td>

Color applied to text in the chat screen header.Default dark color: \#FFFFFF

Default light color: \#FFFFFF

</td></tr><tr><td>

secondary

</td><td>

Color applied to swipe action.Default dark color: \#CECFFF

Default light color: \#1C1D42

</td></tr><tr><td>

separatorPrimary

</td><td>

Color applied to the chat input borders.Default dark color: \#8F95A1

Default light color: \#8F95A1

</td></tr><tr><td>

separatorTertiary

</td><td>

Color applied to dividers.Default dark color: \#353B49

Default light color: \#D3D6DC

</td></tr><tr><td>

shadow

</td><td>

Color applied to card shadow.Default dark color: \#151920

Default light color: \#151920

</td></tr><tr><td>

textActionable

</td><td>

Color applied to button text or highlighted backgrounds.Default dark color: \#07080B

Default light color: \#FFFFFF

</td></tr><tr><td>

textSecondary

</td><td>

Color applied to card content and search bar icon and text.Default dark color: \#C1C5CD

Default light color: \#2C323F

</td></tr><tr><td>

textTertiary

</td><td>

Color applied to weekdays in a calendar and as a placeholder.Default dark color: \#\#8F95A1

Default light color: \#454D5B

</td></tr></tbody>
</table>The following shows the default colors used for NowChatColoring. You can override any or all of these colors.

```
public extension NowChatColoring {
    var brand: UIColor {  nowUIColor.brand }
    var primary: UIColor {  nowUIColor.primary }
    var textActionable: UIColor { nowUIColor.textActionable }
    var screenHeaderText: UIColor { nowUIColor.screenHeaderText }
    var backgroundPrimary: UIColor { nowUIColor.backgroundPrimary }
    var backgroundSecondary: UIColor {
        nowUIColor.backgroundSecondary }
    var backgroundTertiary: UIColor {
        nowUIColor.backgroundTertiary }
    var backgroundPrimaryActionable: UIColor { nowUIColor.backgroundPrimaryActionable }
    var backgroundSecondaryActionable: UIColor { nowUIColor.backgroundSecondaryActionable }
    var brandBackground: UIColor { nowUIColor.brandBackground }
    var separatorPrimary: UIColor { nowUIColor.separatorPrimary }
    var separatorTertiary: UIColor { nowUIColor.separatorTertiary }
    var borderTertiary: UIColor { nowUIColor.borderTertiary }
    var shadow: UIColor { nowUIColor.shadow }
    var linkSecondary: UIColor { nowUIColor.linkSecondary }
    var notification: UIColor { nowUIColor.notification }
    var alertCritical0: UIColor { nowUIColor.alertCritical0 }
    var alertCritical3: UIColor { nowUIColor.alertCritical3 }
}
```

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

