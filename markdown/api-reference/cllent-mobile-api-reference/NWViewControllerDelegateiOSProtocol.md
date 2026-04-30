---
title: NowWebViewControllerDelegate protocol - iOS
description: The NowWebViewControllerDelegate protocol provides callbacks for notification of issues within the NowWebViewController processing such as when a flow ends or a navigation fails.Callback that notifies the host application that the specified Cabrillo \(mobile web\) flow has ended.Callback that notifies the host application that the web view navigation has failed.Callback that notifies the host application that the web view attempted to load an unsupported URL.Callback that notifies the host application that during a back navigation attempt, the stack was exhausted. The host application can then decide whether to dismiss the NowWebViewController instance.Callback that notifies the host application that the system web UI theme changed.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebViewControllerDelegate protocol- iOS

The NowWebViewControllerDelegate protocol provides callbacks for notification of issues within the NowWebViewController processing such as when a flow ends or a navigation fails.

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowWebViewControllerDelegate - nowWebViewController\(\_ nowWebViewController: NowWebViewController, didEndFlow flowName: String\)

Callback that notifies the host application that the specified Cabrillo \(mobile web\) flow has ended.

|Name|Type|Description|
|----|----|-----------|
|nowWebViewController|[NowWebViewController](../../NowWebViewController/concept/NWebViewControlleriOSAPI.md#)|Instance of NowWebViewController where the flow ended.|
|didEndFlow flowName|String|Name of the Cabrillo flow that ended|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
func nowWebViewController(_ nowWebViewController: NowWebViewController, didEndFlow flowName: String) {
  debugPrint("ended flow named: \(flowName)")
}
```

## NowWebViewControllerDelegate - nowWebViewController\(\_ nowWebViewController: NowWebViewController, didFailNavigationWith error: Swift.Error\)

Callback that notifies the host application that the web view navigation has failed.

|Name|Type|Description|
|----|----|-----------|
|nowWebViewController|[NowWebViewController](../../NowWebViewController/concept/NWebViewControlleriOSAPI.md#)|Instance of NowWebViewController in which the navigation failed.|
|didFailNavigationWith error|Swift.Error|Error raised from the navigation failure.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
func nowWebViewController(_ nowWebViewController: NowWebViewController, didFailNavigationWith error: Error) {
  debugPrint("NowWebViewController encountered a navigation error: \(error.localizedDescription)")
}
```

## NowWebViewControllerDelegate - nowWebViewController\(\_ nowWebViewController: NowWebViewController, didReceive unsupportedUrl: URL\)

Callback that notifies the host application that the web view attempted to load an unsupported URL.

An unsupported URL could be one for a different ServiceNow instance or an absolute URL with an invalid scheme.

**Note:** Valid schemes are http and https.

|Name|Type|Description|
|----|----|-----------|
|nowWebViewController|[NowWebViewController](../../NowWebViewController/concept/NWebViewControlleriOSAPI.md#)|Instance of NowWebViewController used when attempting to load the unsupported URL.|
|didReceive unsupportedUrl|URL|Invalid URL trying to be loaded.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
func nowWebViewController(_ nowWebViewController: NowWebViewController, didReceive unsupportedUrl: URL) {
  debugPrint("nowWebViewController:receivedUnsupportedUrl: \(unsupportedUrl.absoluteString)")
}
```

## NowWebViewControllerDelegate - nowWebViewControllerDidRequestDismissal\(\_ nowWebViewController: NowWebViewController\)

Callback that notifies the host application that during a back navigation attempt, the stack was exhausted. The host application can then decide whether to dismiss the NowWebViewController instance.

|Name|Type|Description|
|----|----|-----------|
|nowWebViewController|[NowWebViewController](../../NowWebViewController/concept/NWebViewControlleriOSAPI.md#)|Instance of NowWebViewController in which the back navigation was attempted.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
func nowWebViewControllerDidRequestDismissal(_ nowWebViewController: NowWebViewController) {
  navigationController?.popViewController(animated: true)
}
```

## NowWebViewControllerDelegate - nowWebViewController\(\_ nowWebViewController: NowWebViewController, systemThemeDidChange traitCollection: UITraitCollection\)

Callback that notifies the host application that the system web UI theme changed.

|Name|Type|Description|
|----|----|-----------|
|nowWebViewController|[NowWebViewController](../../NowWebViewController/concept/NWebViewControlleriOSAPI.md#)|Instance of NowWebViewController in which the web UI theme changed.|
|traitCollection|[UITraitCollection](https://developer.apple.com/documentation/uikit/uitraitcollection)|UITraitCollection object that contains the new theme.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to override the systemThemeDidChange\(\) delegate function to call the updateTheme\(\) function to apply theme changes when the system theme changes.

```
func nowWebViewController(_ nowWebViewController: NowWebViewController, systemThemeDidChange traitCollection: UITraitCollection) {

  /// Called when the system changes between dark and light mode

    /// You can call the corresponding updateTheme() method here to change the UI theme based on System Theme
    nowWebViewController.updateTheme(themeColors: traitCollection.userInterfaceStyle == .dark ? DarkNowWebTheme() : LightNowWebTheme())
      print(“System Theme Did Change)
}
```

