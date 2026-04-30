---
title: NowWebViewController class - iOS
description: The NowWebViewController class provides functions that enable you to manage a web viewer.If the request is authenticated, starts loading the initial URL provided during instantiation using the makeWebViewController\(\) method.Updates the NowWebView theme with the specified UI theme. Use this function to update the web UI theme after it has been initially set using the makeWebViewController\(\) function, such as when changing the theme from light to dark.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebViewController class - iOS

The NowWebViewController class provides functions that enable you to manage a web viewer.

![Web page load flow](../../image/mobsdk-web-start-flow.png)

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowWebViewController - loadPage\(\)

If the request is authenticated, starts loading the initial URL provided during instantiation using the makeWebViewController\(\) method.

If the request fails authentication, the method nowWebViewController\(\_:didFailNavigationWith:\) is called on the delegate that was passed when instantiating the object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
private func openScreen(_ screen: ArticleListViewModel.Screen) {
  switch screen {
  case .articleDetail(let sysId):
    guard let url = URL(string: "/mesp?id=me_kb_view&sys_kb_id=\(sysId)"), let webViewController = webViewController(for: url) else {
      debugPrint("Could not create web view")
      return
    }
    webViewController.loadPage()
    navigationController?.pushViewController(webViewController, animated: true)
  }
}
```

## NowWebViewController - updateTheme\(themeColors: NowWebThemeable\)

Updates the NowWebView theme with the specified UI theme. Use this function to update the web UI theme after it has been initially set using the makeWebViewController\(\) function, such as when changing the theme from light to dark.

|Name|Type|Description|
|----|----|-----------|
|themeColors|[NowWebThemeable](../../NowWebThemeable/concept/NowWebThemeableiOSProtocol.md)|Theme to update the web UI with.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to update a light UI theme implemented using the makeWebViewController\(\) function to the dark UI theme using the updateTheme\(\) function.

```
func nowWebViewController(_ nowWebViewController: NowWebViewController, systemThemeDidChange traitCollection: UITraitCollection) {
  // The systemThemeDidChange delegate method can be used to call updateTheme() to apply theme changes when the system theme changes.
  nowWebViewController.updateTheme(themeColors: traitCollection.userInterfaceStyle == .dark ? DarkNowWebTheme() : LightNowWebTheme())
}
```

