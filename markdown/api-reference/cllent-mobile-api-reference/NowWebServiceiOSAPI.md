---
title: NowWebService class - iOS
description: The NowWebService class provides functions that enable the browsing of web pages on a ServiceNow instance.Initializes a NowWebService instance.Creates a UIViewController object that hosts the web view.Preloads a list of specified pages with cacheable resources in the background \(by NowWeb\) to improve initial load times.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWebService class- iOS

The NowWebService class provides functions that enable the browsing of web pages on a ServiceNow instance.

|Name|Type|Description|
|----|----|-----------|
|configuration|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)|Configuration parameters to use when initializing the NowWebService instance.|

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowWebService - init\(configuration: NowServiceConfiguration, coreServiceProvider: NowCoreServiceProviding? = nil\)

Initializes a NowWebService instance.

<table id="table_lc2_n13_ppb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)

</td><td>

Configuration parameters to use when initializing the NowWebService instance.

</td></tr><tr><td>

coreServiceProvider

</td><td>

NowCoreServiceProviding

</td><td>

Optional. Service provider to associate with the NowWebService instance.Default: nil

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
guard let coreService = NowSDK.core() else {
  // Error with NowServiceError.sdkNotConfigured
  return
}
guard 
  let instanceUrl = URL(string: "http://sample.service-now.com") , 
  let serviceConfig = NowSDK.makeServiceConfiguration(for: instanceUrl) else {
    // Could not create service – 
    // NowServiceError.serviceConfigurationInvalid
    return
}

let webService = NowWebService(configuration: serviceConfig, coreServiceProvider: coreService)
```

## NowWebService - makeWebViewController\(for url: URL, delegate: NowWebViewControllerDelegate, theme: NowWebThemeable\)

Creates a UIViewController object that hosts the web view.

<table id="table_pnt_hb3_ppb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

for url

</td><td>

URL

</td><td>

URL of the web page to load. This web page must be on the target ServiceNow instance that the service was initialized with.

</td></tr><tr><td>

delegate

</td><td>

NowWebViewControllerDelegate

</td><td>

Optional. Object that receives callback events from the WebViewController into the native application.

</td></tr><tr><td>

theme

</td><td>

[NowWebThemeable protocol - iOS](../../NowWebThemeable/concept/NowWebThemeableiOSProtocol.md)

</td><td>

Optional. NowUIThemeable protocol to apply to the UI elements of the view controller, such as color.Default: NowWebDefaultTheme\(nowUITheme: NowUIDefaultTheme\(\)\)

</td></tr></tbody>
</table><table id="table_qnt_hb3_ppb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Result&lt;NowWebViewController, NowWebServiceError&gt;

</td><td>

Success: NowWebViewController objectFailure: NowWebServiceError object

</td></tr></tbody>
</table>```
private func webViewController(for url: URL) -> NowWebViewController? {
  guard let webService = webService else {
    debugPrint("Web service not initialized")
    return nil
  }
        
  let result = webService.makeWebViewController(for: url, delegate: self, theme: CarrascoWebTheme(nowUITheme: CarrascoTheme()))
  switch result {
    case .success(let viewController):
      return viewController
    case .failure(let error):
      debugPrint("Web view creation failed with error: \(error.localizedDescription)")
  }
  return nil
}
```

## NowWebService - preloadWebCache\(urls: \[URL\], completion: PreloadWebCacheCompletion? = nil\) throws

Preloads a list of specified pages with cacheable resources in the background \(by NowWeb\) to improve initial load times.

|Name|Type|Description|
|----|----|-----------|
|urls|Array of URL objects|URLs of the pages to preload.|
|completion|PreloadWebCacheCompletion|Optional. Closure to inform the caller that the web pages have completed loading.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to use the webService.preloadWebCache\(\) function to pre-load specified pages.

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

