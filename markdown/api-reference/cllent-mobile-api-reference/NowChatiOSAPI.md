---
title: NowChat API - iOS
description: The NowChat API is a top-level global API that enables users to instantiate a NowChat service instance.Creates an instance of NowChatService with the specified configuration.Creates an instance of NowChatService with the specified configuration, and once complete, calls the specified completion handler.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChat API- iOS

The NowChat API is a top-level global API that enables users to instantiate a NowChat service instance.

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowChat - makeChatService\(instanceUrl: URL, delegate: NowChatServiceDelegate?\)

Creates an instance of NowChatService with the specified configuration.

**Note:** You must initialize the SDK prior to calling this function or the completion block is called with a `sdkNotConfigured` error. To initialize the SDK, call the `NowSDK.configure()` method with the desired configuration.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance providing chat services.|
|delegate|NowChatServiceDelegate|Optional. Delegate object that implements the NowChatServiceDelegate protocol.|

|Type|Description|
|----|-----------|
|AnyPublisher&lt;[NowChatService](../../NowChatService/concept/NowChatServiceiOSAPI.md#), NowServiceError&gt;|If successful, returns an initialized NowChatService object. If it fails, returns a NowServiceError object.|

The following code example shows how to call this function.

```
….
guard 
  let jwtUrl = URL(string: "http://xx.xx.xx.xxx:8080"),
  let instanceUrl = URL(string: "https://instance.service-now.com") else {
    return
  }
// AuthorizationProvider – struct conforming to NowSDKAuthorizationProviding protocol
let authorizationProvider = AuthorizationProvider(userEmail: "sdk@servicenow.com", jwtProviderUrl: jwtUrl, clientId: "deb8756b452d201039231ca568f26511")
        
// PermissionProvider – class conforming to DevicePermissionDelegate protocol
let permissionProvider = PermissionProvider()
let config = NowSDKConfiguration(authorizationProvider: authorizationProvider, permissionDelegate: permissionProvider, logLevel: .debug)
	
do {
  try NowSDK.configure(with: config)
  let chat = setup(with: instanceUrl)
} catch {
  // Return ConfigurationError.sdkError(error)
}
…..

func initializeChatService(with instanceURL: URL) -> AnyPublisher<NowService, ConfigurationError> {
  NowChat.makeChatService(instanceUrl: instanceURL, delegate: nil)
  .mapError { .sdkError($0) }
  .map { $0 as NowService }
  .eraseToAnyPublisher()
}
```

## NowChat - makeChatService\(instanceUrl: URL, delegate: NowChatServiceDelegate?, completion: @escaping \(\(Result&lt;NowChatService, NowServiceError&gt;\) -&gt; Void\)\)

Creates an instance of `NowChatService` with the specified configuration, and once complete, calls the specified completion handler.

**Note:** You must initialize the SDK prior to calling this function or the completion block is called with a `sdkNotConfigured` error. To initialize the SDK, call the `NowSDK.configure()` method with the desired configuration.

|Name|Type|Description|
|----|----|-----------|
|instanceUrl|URL|URL of the ServiceNow instance providing chat services.|
|delegate|NowChatServiceDelegate|Optional. Delegate object that implements the NowChatServiceDelegate protocol.|
|completion|@escaping \(\(Result&lt;[Now​Chat​Service](../../NowChatService/concept/NowChatServiceiOSAPI.md#), Now​Service​Error&gt;\) -&gt; Void\)|Completion handler that is called containing either an initialized `NowChatService` instance or a `NowServiceError` indicating why the initialization failed.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
func initializeChatService() {
  NowChat.makeChatService(instanceUrl: instanceUrl, delegate: self) { [weak self] result in
    guard let self = self else { return }
            
    switch result {
    case .success(let service):
      self.chatService = service
    case .failure(let error):
      debugPrint("Creating the chat service failed with error: \(error)")
    }
    self.viewState = self.makeViewState()
  }
}
```

