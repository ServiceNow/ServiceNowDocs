---
title: NowWebColoring protocol - iOS
description: The NowWebColoring protocol provides default values for the colors used within web pages hosted on your ServiceNow instance in a native web view.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebColoring protocol- iOS

The NowWebColoring protocol provides default values for the colors used within web pages hosted on your ServiceNow instance in a native web view.

The colors specified in the table below define the default web interface colors.

<table class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alertCritical0

</td><td>

Background color applied to the error banner.Default dark color: \#7B1E28

Default light color: \#F8C8CD

</td></tr><tr><td>

alertCritical3

</td><td>

Text color applied to the error text banner.Default dark color: \#E46876

Default light color: \#B61C2D

</td></tr><tr><td>

alertLow0

</td><td>

Background color applied to the info banner.Default dark color: \#DBDBDE

Default light color: \#DBDBDE

</td></tr><tr><td>

alertPositive0

</td><td>

Background color of the banner that displays success messages.Default dark color: \#CADFC0

Default light color: \#CADFC0

</td></tr><tr><td>

alertPositive3

</td><td>

Text color of the banner that displays success messages.Default dark color: \#3B7F00

Default light color: \#3B7F00

</td></tr><tr><td>

alertWarning0

</td><td>

Background color applied to the warning banner.Default dark color: \#FBF7BF

Default light color: \#FBF7BF

</td></tr><tr><td>

backgroundPrimary

</td><td>

Background color applied to the view containing the web view.Default dark color: \#07080B

Default light color: \#FFFFFF

</td></tr><tr><td>

brand

</td><td>

Color applied to the activity indicator shown while loading pages.Default dark color: \#302F4B

Default light color: \#302F4B

</td></tr><tr><td>

primary

</td><td>

Tint color applied to action sheet on the web screen.Default dark color: \#8486FF

Default light color: \#4F52BD

</td></tr><tr><td>

screenHeaderBackground

</td><td>

Text color applied to button badges. This color is also applied to a thin border around the badge.Default dark color: \#CADFC0

Default light color: \#CADFC0

</td></tr><tr><td>

screenHeaderText

</td><td>

-   Text color applied to button badges
-   Tint color applied to disabled navigation bar buttons, banner text, and banner icon tint on the web screen.

 Default dark color: \#FFFFFF

 Default light color: \#FFFFFF

</td></tr><tr><td>

textActionble

</td><td>

Text color for action button.Default dark color: \#07080B

Default light color: \#FFFFFF

</td></tr><tr><td>

textPrimary

</td><td>

Text color applied to font.Default dark color: \#FFFFFF

Default light color: \#151920

</td></tr><tr><td>

webPageThemeId

</td><td>

Sys\_id of the theme to apply to the ServiceNow web pages loaded by NowWeb. Default: Configured default theme

Table: Located in the UX Theme \[sys\_ux\_theme\] table.

</td></tr><tr><td>

webPageThemeVariantId

</td><td>

Sys\_id of the theme variant to apply to the ServiceNow web pages loaded by NowWeb. Default: Configured default theme variant

Table: Located in the UX Style \[sys\_ux\_style\] table.

</td></tr></tbody>
</table>The following shows the default colors used for NowWebColoring. You can override any or all of these colors.

```
public extension NowWebColoring {
    var brand: UIColor { nowUIColor.brand }
    var primary: UIColor { nowUIColor.primary }
    var textPrimary: UIColor {
        nowUIColor.textPrimary.withAlphaComponent(0.25)
    }
    var screenHeaderText: UIColor { nowUIColor.screenHeaderText }
    var screenHeaderBackground: UIColor { nowUIColor.screenHeaderBackground }
    var textActionble: UIColor {
        nowUIColor.textActionable
    }
    var alertCritical0: UIColor { nowUIColor.alertCritical0 }
    var alertCritical3: UIColor { nowUIColor.alertCritical3 }
    var alertPositive0: UIColor { nowUIColor.alertPositive0 }
    var alertPositive3: UIColor { nowUIColor.alertPositive3 }
    var alertLow0: UIColor { nowUIColor.alertLow0 }
    var alertWarning0: UIColor { nowUIColor.alertWarning0 }
    var backgroundPrimary: UIColor { nowUIColor.backgroundPrimary }
}
```

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

