---
title: Display web pages hosted on your ServiceNow instance
description: You can display web pages hosted within your ServiceNow instance in your native iOS application.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Display web pages hosted on your ServiceNow instance

You can display web pages hosted within your ServiceNow instance in your native iOS application.

The Mobile SDK provides seamless handling of the required authentication and session management, while the [NowWebService](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowWebService/concept/NowWebServiceiOSAPI.md#) API provides the functionality required to handle pages residing on your ServiceNow instance. These web pages have all the dynamic interactions that are possible on the ServiceNow platform.

When the webview is requested to load a web page hosted on a ServiceNow instance, it creates an HTTP request with the appropriate bearer header containing the OAuth access token provided by the NowSDK. When the instance receives this request, it starts a new user session and returns cookies related to that session. As the user interacts with the web pages in the webview, the instance uses the cookies to validate that the session is still valid. At this point, the bearer header is no longer relevant, only the cookies are used for session validation. The web session expires if the user stops interacting with the website for longer than the timeout period. After the session expires, if the user tries to interact with the web page, they are automatically redirected to the login page. The NowWebViewController detects the redirection and attempts to start a new web session by requesting a refreshed access token from the NowSDK and using the token to create a HTTP request \(with bearer header\) for the last known loaded page.

To use these features, you must first create an instance of the NowWebService. To do this you must call the makeWebService\(\) method and provide the URL to your ServiceNow instance and an already initialized `NowSDK`. In addition, you must have imported `NowWeb` within your application. You should hold a reference to the NowWebService for as long as you are using the `NowWeb` service.

The following shows an example of how to create a NowWebService object using async/await:

```
do {
    let service = try await NowWeb.makeWebService(instanceUrl: instanceUrl)
    self.webService = service
} catch {
    debugPrint("Web Service creation failed with error: \(error.localizedDescription)") 
}
```

The following shows an example of how to create a NowWebService object using a completion handler:

```
import Combine
import NowWeb
import UIKit
...
public func makeWebService(instanceUrl: URL, 
  completion: @escaping ((Result<NowWeb.NowWebService, NowSDK.NowServiceError>) -> Void)) 
```

## Pre-load pages to improve NowWeb load time

You can pre-load pages with cacheable resources in the background to improve initial NowWeb load times. The following example shows how to use the webService.preloadWebCache\(\) function to pre-load specified pages.

```
private func preloadURLs(urls: [URL]) {
  guard let webService = webService else {
    debugPrint("Web service not initialized")
    return
  }
  do {
       try webService.preloadWebCache(urls: urls) {
         debugPrint("URLs did complete preloading")
       }
            
  } catch {
      debugPrint(error.localizedDescription)
  }
}
```

## Create views to display web content

Once you have instantiated an instance of NowWebService, you can use it to create views to display web pages hosted on your ServiceNow instance.

The following example shows how to create a [NowWebViewController](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowWebViewController/concept/NWebViewControlleriOSAPI.md#) view:

```
let result = webService.makeWebViewController(for: url, 
  delegate: self, theme: MyWebTheme(nowUITheme: MyUITheme()))
switch result { 
case .success(let viewController): 
  return viewController 
case .failure(let error): 
  debugPrint("Web view creation failed with error: \(error.localizedDescription)") 
}
```

In this example, **url** is the URL of the initial page to load within the view. This URL must point to a page that is hosted on the specified ServiceNow instance. Relative URLs also work and are relative to the ServiceNow instance targeted by the NowWebService.

Once created, you can push the NowWebViewController onto an existing navigation stack. The initial page is not loaded until you call the [loadPage\(\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowWebViewController/concept/NWebViewControlleriOSAPI.md#) method.

## Theme the web user interface

You can customize the colors of the web UI by passing a theme object in the makeWebViewController\(\) call. For a list of all of the elements that you can customize, see [NowWebColoring protocol - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowWebColoring/concept/NowWebColoringiOSProtocol.md). By default, the web UI uses the NowUIColor theme for all NowSDK UI elements. Refer to the [NowWebThemeable protocol - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowWebThemeable/concept/NowWebThemeableiOSProtocol.md) for sample code snippets on how to apply a theme to your web UI.

