---
title: NowWeb API - iOS
description: The NowWeb API is a top-level global API that enables uses to instantiate a NowWeb service instance.Creates an instance of NowWebService using the previously specified configuration.Creates an instance of NowWebService using the previously specified configuration. When finished, calls the specified completion handler.Creates an instance of NowWebService using the previously specified configuration.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowWeb API- iOS

The NowWeb API is a top-level global API that enables uses to instantiate a NowWeb service instance.

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowWeb - makeWebService\(instanceUrl: URL\) async throws

Creates an instance of NowWebService using the previously specified configuration.

You must initialize the SDK prior to calling this function or the completion block is called with a `sdkNotConfigured` error. To initialize the SDK, call NowSDK.configure\(\) with the desired configuration.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance whose web services are to be accessed by the service.|

<table id="table_xct_ldx_kqb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[NowWebService](../../NowWebService/concept/NowWebServiceiOSAPI.md#)

</td><td>

If successful, returns an initialized NowWebService object.

</td></tr><tr><td>

NowServiceError

</td><td>

Throws one of the following errors if the method fails.Possible values:

-   sdkNotConfigured
-   serviceConfigurationInvalid
-   serviceDisabled
-   serviceSettingsInvalid
-   serviceSettingsNotFound
-   serviceSettingsRetrievalFailed

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
do {
    let service = try await NowWeb.makeWebService(instanceUrl: instanceUrl)
    self.webService = service
} catch {
    debugPrint("Web Service creation failed with error: \(error.localizedDescription)") 
}
```

## NowWeb - makeWebService\(instanceUrl: URL, completion: @escaping \(\(Result&lt;NowWebService, NowServiceError&gt;\) -&gt; Void\)\)

Creates an instance of NowWebService using the previously specified configuration. When finished, calls the specified completion handler.

You must initialize the SDK prior to calling this function or the completion block is called with a `sdkNotConfigured` error. To initialize the SDK, call NowSDK.configure\(\) with the desired configuration.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance whose web services are to be accessed by the service.|
|completion|@escaping \(\(Result&lt;[NowWebService](../../NowWebService/concept/NowWebServiceiOSAPI.md#), Now​Service​Error&gt;\) -&gt; Void\)|Completion handler that is called with a `Result<NowWebService, NowServiceError>` containing either an initialized `NowWebService` instance or a `NowServiceError` indicating why the initialization failed.|

|Type|Description|
|----|-----------|
|None| |

```
func initializeNowSDK(userEmail: String) {
  currentUser = userEmail
  let sdkConfig = NowSDKConfiguration(authorizationProvider: self, permissionDelegate: self, logLevel: .debug)
        
  do {
      try NowSDK.configure(with: sdkConfig)
      configureAnalytics()
  } catch {
      debugPrint("Could not initialize NowSDK. Error: \(error.localizedDescription)")
  }
}
```

## NowWeb - makeWebService\(instanceUrl: URL\)

Creates an instance of NowWebService using the previously specified configuration.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

You must initialize the SDK prior to calling this function or the completion block is called with a `sdkNotConfigured` error. To initialize the SDK, call NowSDK.configure\(\) with the desired configuration.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance whose web services are to be accessed by the service.|

|Type|Description|
|----|-----------|
|AnyPublisher&lt;[NowWebService](../../NowWebService/concept/NowWebServiceiOSAPI.md#), NowServiceError&gt;|If successful, returns an initialized NowWebService object. If it fails, returns a NowServiceError object.|

```
func initializeWebService() {
  NowWeb.makeWebService(instanceUrl: instanceUrl)
    .sink { completion in
      if case .failure(let error) = completion {
        debugPrint("Web Service creation failed with error: \(error.localizedDescription)")
      }
    } receiveValue: { [weak self] service in
        self?.webService = service
    }
    .store(in: &subscriptions)
  }
```

