---
title: NowSDK framework - iOS
description: The NowSDK framework contains methods that enable the instantiation of various feature services.Configures NowSDK for use. You must call this function before calling any of the feature services within the Mobile SDK.Returns a reference to the SDK core service.Convenience function that feature services can use to construct n NowServiceConfiguration object.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowSDK framework - iOS

The NowSDK framework contains methods that enable the instantiation of various feature services.

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowSDK - configure\(with configuration: NowSDKConfiguration\) throws

Configures NowSDK for use. You must call this function before calling any of the feature services within the Mobile SDK.

**Note:** If the configuration that you pass is invalid, a `NowSDKError` is thrown.

|Name|Type|Description|
|----|----|-----------|
|with configuration|[NowSDKConfiguration](../../NowSDKConfiguration/concept/NowSDKConfigurationiOSAPI.md#)|NowSDKConfiguration that contains the information necessary to initialize the service.|

|Type|Description|
|----|-----------|
|None, NowSDKError|NowSDKError is thrown if the configuration that you pass is invalid.|

The following code example shows how to call this function.

```
guard 
  let jwtUrl = URL(string: "http://13.57.38.237:8080"),
  let instanceUrl = URL(string: "https://mobilecoresdk.service-now.com") else {
    return
  }

// AuthorizationProvider – struct conforming to NowSDKAuthorizationProviding protocol
let authorizationProvider = AuthorizationProvider(userEmail: "sdk@servicenow.com", jwtProviderUrl: jwtUrl, clientId: "deb8756b452d201039231ca568f26511")
        
// PermissionProvider – class conforming to DevicePermissionDelegate protocol
let permissionProvider = PermissionProvider()
let config = NowSDKConfiguration(authorizationProvider: authorizationProvider, permissionDelegate: permissionProvider, logLevel: .debug)

do {
  try NowSDK.configure(with: config)
            …
} catch {
   print(“error is \(error.localizedDescription)”)
}
```

## NowSDK - core\(\)

Returns a reference to the SDK core service.

**Note:** Host applications don't need to call this function.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object conforming to the NowCoreServiceProviding protocol is returned if the SDK has been initialized by calling the [NowSDK - configure\(with configuration: NowSDKConfiguration\) throws](NowSDKAPIiOS.md#) method; otherwise `nil`.|

The following code example shows how to call this function.

```
guard let coreService = NowSDK.core() else {
  // Error with NowServiceError.sdkNotConfigured
  return
}
```

## NowSDK - makeServiceConfiguration\(for instanceUrl: URL\)

Convenience function that feature services can use to construct n NowServiceConfiguration object.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance that the service will access.|

|Type|Description|
|----|-----------|
|[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)|If the specified URL passes basic validity checks, and the service configuration can be properly constructed, returns the NowServiceConfiguration object; otherwise `nil`.|

The following code example shows how to call this function.

```
guard 
  let instanceUrl = URL(string: "https://mobilecoresdk.service-now.com"),
  let serviceConfig = NowSDK.makeServiceConfiguration(for: instanceUrl) else {
    logger.error(message: "Could not create service - service configuration invalid")
    return 
  }
```

