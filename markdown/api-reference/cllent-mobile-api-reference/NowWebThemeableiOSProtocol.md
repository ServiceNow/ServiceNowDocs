---
title: NowWebThemeable protocol - iOS
description: The NowWebThemeable protocol provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebThemeable protocol- iOS

The NowWebThemeable protocol provides properties that enable you to override the colors used within web pages hosted on your ServiceNow instance in a native web view.

```
public protocol NowWebThemeable {
    var color: NowWebColoring { get }
}
```

The [NowWebColoring](../../NowWebColoring/concept/NowWebColoringiOSProtocol.md) protocol contains **NowUIColoring**. This property is used to reference default color variables that NowWebThemeable can use.

For additional information on how to theme the UI, see [Use NowUIColoring to theme NowWebTheme and NowChatTheme](../../../../../../integrate/guides/mobile_sdk/mobile_sdk-android/reference/mobsdk-and-color-theming.md) in the Mobile SDK Developer Guide - iOS.

## Define WebColors using default colors

```
/// Sample structure for using default colors that come with Mobile SDK.
struct WebColors: NowUIColoring {
}
```

## Define WebColors using custom colors

```
/// Use custom colors with light theme
struct WebColors: NowUIColoring {
    private var defaultTheme: NowWebDefaultTheme { NowWebDefaultTheme(nowUITheme: NowUIDefaultTheme())
    }
    
    var brand: UIColor { lightBrand }
    var primary: UIColor { lightPrimary }
    var textPrimary: UIColor { lightTextPrimary }
    var screenHeaderText: UIColor { lightScreenHeaderText }
    var screenHeaderBackground: UIColor { lightScreenHeaderBackground }
    var textActionable: UIColor { lightTextActionable }
    var alertCritical0: UIColor { lightAlertCritical0 }
    var alertCritical3: UIColor { lightAlertCritical3 }
    var alertPositive0: UIColor { lightAlertPositive0 }
    var alertPositive3: UIColor { lightAlertPositive3 }
    var alertLow0: UIColor { lightAlertLow0 }
    var alertWarning0: UIColor { lightAlertWarning0 }
    var backgroundPrimary: UIColor { lightBackgroundPrimary }
    
    // Light Colors
    var lightBrand: UIColor { defaultTheme.color.brand }
    var lightPrimary: UIColor { defaultTheme.color.primary }
    var lightTextPrimary: UIColor { defaultTheme.color.textPrimary }
    var lightScreenHeaderText: UIColor { defaultTheme.color.screenHeaderText }
    var lightScreenHeaderBackground: UIColor { defaultTheme.color.screenHeaderBackground }
    var lightTextActionable: UIColor { defaultTheme.color.textActionble }
    var lightAlertCritical0: UIColor { defaultTheme.color.alertCritical0 }
    var lightAlertCritical3: UIColor { defaultTheme.color.alertCritical3 }
    var lightAlertPositive0: UIColor { defaultTheme.color.alertPositive0 }
    var lightAlertPositive3: UIColor { defaultTheme.color.alertPositive3 }
    var lightAlertLow0: UIColor { defaultTheme.color.alertLow0 }
    var lightAlertWarning0: UIColor { defaultTheme.color.alertWarning0 }
    var lightBackgroundPrimary: UIColor { defaultTheme.color.backgroundPrimary }
}
```

## Define WebTheme structure with NowWebThemeable protocol

```
struct CarrascoWebTheme: NowWebThemeable {
    var color: NowWebColoring
    
    struct Color: NowWebColoring {
        var nowUIColor: NowUIColoring
    
        var alertPositive0: UIColor
        var alertPositive3: UIColor
        var alertLow0: UIColor
        var alertWarning0: UIColor
        var backgroundPrimary: UIColor
        
        init(inputs: WebColors) {
            nowUIColor = ThemeColor(inputs)
            
            alertPositive0 = inputs.alertPositive0
            alertPositive3 = inputs.alertPositive3
            alertLow0 = inputs.alertLow0
            alertWarning0 = inputs.alertWarning0
            backgroundPrimary = inputs.backgroundPrimary
        }
    }
    
    public init(webColors: WebColors) {
        color = Color(inputs: webColors)
    }
}

```

## Instantiate a WebTheme object by passing WebColor as input

```
let webTheme = CarrascoWebTheme(webColors: WebColors())
```

## Pass a WebTheme object to NowWebService.makeWebViewController

```
func webViewController(for url: URL, delegate: NowWebViewControllerDelegate) -> NowWebViewController? {
  guard let webService = webService else {
    debugPrint("Web service not initialized")
    return nil
  }
  let result = webService.makeWebViewController(for: url, delegate: delegate, theme: CarrascoWebTheme(webColors: WebColors()) )
    
  switch result {
  case .success(let viewController):
    return viewController
  case .failure(let error):
    debugPrint("Web view creation failed with error: \(error.localizedDescription)")
  }
  return nil
}
```

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

