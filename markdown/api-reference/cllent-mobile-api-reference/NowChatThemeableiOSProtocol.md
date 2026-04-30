---
title: NowChatThemeable protocol - iOS
description: The NowChatThemeable protocol provides properties that enable you to override the colors used within chat pages hosted on your ServiceNow instance.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatThemeable protocol - iOS

The NowChatThemeable protocol provides properties that enable you to override the colors used within chat pages hosted on your ServiceNow instance.

```
public protocol NowChatThemeable {
    var color: NowChatColoring { get }
}
```

The [NowChatColoring](../../NowChatColoring/concept/NowChatColoringiOSProtocol.md#) protocol contains **NowUIColoring**. This property is used to reference default color variables that NowWebThemeable can use.

For additional information on how to theme the UI, see [Use NowUIColoring to theme NowWebTheme and NowChatTheme](../../../../../../integrate/guides/mobile_sdk/mobile_sdk-android/reference/mobsdk-and-color-theming.md) in the Mobile SDK Developer Guide - iOS.

## Define ChatColors using default colors

```
/// Sample structure for using default colors that comes with Mobile SDK.
struct ChatColors: NowUIColoring {
}

```

## Define ChatColors using custom colors

```
/// Use Custom Colors with light theme
struct ChatColors: NowUIColoring {
    private var defaultTheme: NowChatDefaultTheme {
        NowChatDefaultTheme(nowUITheme: NowUIDefaultTheme())
    }
 
    var brand: UIColor {
        lightBrand
    }
    var primary: UIColor {
        lightPrimary
    }
    var secondary: UIColor {
        lightSecondary
    }
    var textTertiary: UIColor {
        lightTextTertiary
    }
    var destructive: UIColor {
        lightDestructive
    }
    var textPrimary: UIColor {
        lightTextPrimary
    }
    var textSecondary: UIColor {
        lightTextSecondary
    }
    var textActionable: UIColor {
        lightTextActionable
    }
    var screenHeaderText: UIColor {
        lightScreenHeaderText
    }
    var backgroundPrimary: UIColor {
        lightBackgroundPrimary
    }
    var backgroundSecondary: UIColor {
        lightBackgroundSecondary
    }
    var backgroundTertiary: UIColor {
        lightBackgroundTertiary
    }
    var backgroundPrimaryActionable: UIColor {
        lightBackgroundPrimaryActionable
    }
    var backgroundSecondaryActionable: UIColor {
        lightBackgroundSecondaryActionable
    }
    var brandBackground: UIColor {
        lightBrandBackground
    }
    var linkPrimaryText: UIColor {
        lightLinkPrimary
    }
    var linkSecondary: UIColor {
        lightLinkSecondary
    }
    var separatorPrimary: UIColor {
        lightSeparatorPrimary
    }
    var separatorTertiary: UIColor {
        lightSeparatorTertiary
    }
    var borderTertiary: UIColor {
        lightBorderTertiary
    }
    var shadow: UIColor {
        lightShadow
    }
    var notification: UIColor {
        lightNotification
    }
    var alertCritical0: UIColor {
        lightAlertCritical0
    }
    var alertCritical3: UIColor {
        lightAlertCritical3
    }

    // Light Colors
    var lightBrand: UIColor { defaultTheme.color.nowUIColor.brand }
    var lightPrimary: UIColor { defaultTheme.color.nowUIColor.primary }
    var lightSecondary: UIColor { defaultTheme.color.nowUIColor.secondary }
    var lightDestructive: UIColor { defaultTheme.color.nowUIColor.destructive }
    var lightTextPrimary: UIColor { defaultTheme.color.nowUIColor.textPrimary }
    var lightTextSecondary: UIColor { defaultTheme.color.nowUIColor.textSecondary }
    var lightTextTertiary: UIColor { defaultTheme.color.nowUIColor.textTertiary }
    var lightTextActionable: UIColor { defaultTheme.color.nowUIColor.textActionable }
    var lightScreenHeaderText: UIColor { defaultTheme.color.nowUIColor.screenHeaderText }
    var lightBackgroundPrimary: UIColor { defaultTheme.color.nowUIColor.backgroundPrimary }
    var lightBackgroundSecondary: UIColor { defaultTheme.color.nowUIColor.backgroundSecondary }
    var lightBackgroundTertiary: UIColor { defaultTheme.color.nowUIColor.backgroundTertiary }
    var lightBackgroundPrimaryActionable: UIColor { defaultTheme.color.nowUIColor.backgroundPrimaryActionable
    }
    var lightBackgroundSecondaryActionable: UIColor { defaultTheme.color.nowUIColor.backgroundSecondaryActionable
    }
    var lightBrandBackground: UIColor { defaultTheme.color.nowUIColor.brandBackground }
    var lightLinkPrimary: UIColor { defaultTheme.color.nowUIColor.linkPrimaryText }
    var lightLinkSecondary: UIColor { defaultTheme.color.nowUIColor.linkSecondary }
    var lightSeparatorPrimary: UIColor { defaultTheme.color.nowUIColor.separatorPrimary }
    var lightSeparatorTertiary: UIColor { defaultTheme.color.nowUIColor.separatorTertiary }
    var lightBorderTertiary: UIColor { defaultTheme.color.nowUIColor.borderTertiary }
    var lightShadow: UIColor { defaultTheme.color.nowUIColor.shadow }
    var lightNotification: UIColor { defaultTheme.color.nowUIColor.notification }
    var lightAlertCritical0: UIColor { defaultTheme.color.nowUIColor.alertCritical0 }
    var lightAlertCritical3: UIColor { defaultTheme.color.nowUIColor.alertCritical3 }
}
```

## Define ChatTheme structure with NowChatThemeable protocol

```
struct CarrascoChatTheme: NowChatThemeable {
    var color: NowChatColoring
    
    struct Color: NowChatColoring {
        var nowUIColor: NowUIColoring
    
        var backgroundPrimary: UIColor
        var backgroundSecondary: UIColor
        var backgroundPrimaryActionable: UIColor
        var backgroundSecondaryActionable: UIColor
        var brandBackground: UIColor
        var backgroundTertiary: UIColor
        var separatorPrimary: UIColor
        var separatorTertiary: UIColor
        var borderTertiary: UIColor
        var shadow: UIColor
        var linkSecondary: UIColor

        init(inputs: ChatColors) {
            nowUIColor = ThemeColor(inputs)
            
            backgroundPrimary = inputs.backgroundPrimary
            backgroundSecondary = inputs.backgroundSecondary
            backgroundTertiary = inputs.backgroundTertiary
            backgroundPrimaryActionable = inputs.backgroundPrimaryActionable
            backgroundSecondaryActionable = inputs.backgroundSecondaryActionable
            brandBackground = inputs.brandBackground
            separatorPrimary = inputs.separatorPrimary
            separatorTertiary = inputs.separatorTertiary
            borderTertiary = inputs.borderTertiary
            shadow = inputs.shadow
            linkSecondary = inputs.linkSecondary
        }
    }

    init(chatColors: ChatColors) {
        color = Color(inputs: chatColors)
    }
}
```

## Instantiate ChatTheme object by passing ChatColor as input

```
let chatTheme = CarrascoChatTheme(chatColors: ChatColors())
```

## Pass ChatTheme object to NowChatService.makeChatUI \(\)

```
func makeChatScreen() -> UIViewController? {
  guard let chatService = chatService else { return nil }
  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors()))
        
  switch result {
  case .success(let chatViewController):
    return chatViewController
  case .failure(let error):
    debugPrint("Chat screen creation failed with error: \(error)")
    return nil
  }
}
```

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

