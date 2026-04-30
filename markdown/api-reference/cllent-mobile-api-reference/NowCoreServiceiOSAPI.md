---
title: NowCoreService class - iOS
description: The NowCoreService class provides fundamental services to the various SDK feature services. This class should only be instantiated by NowSDK.Notifies the SDK core that the access token used to authorize the API requests to the ServiceNow instance for the specified service is no longer valid.Notifies the SDK core that the access token used to authorize the API requests to the ServiceNow instance for the specified service is no longer valid.Queries the host application as to whether the service is allowed to request the device permission.Checks whether the current user is a guest user.Refreshes all SDK settings for all services by re-fetching them from the active servers.Refreshes the SDK settings for the specified service by re-fetching them from the server.Refreshes the SDK settings for the specified service by re-fetching them from the server.Acquires an access token for the specified service.Acquires an access token for the specified service.Returns a reference to a shared network service that you can use to make API requests.Returns the SDK settings for the specified feature service.Returns the SDK settings for the specified feature service.Retrieves the settings for the publisher of the specified service.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowCoreService class- iOS

The NowCoreService class provides fundamental services to the various SDK feature services. This class should only be instantiated by NowSDK.

Feature services, such as Now Analytics and NowChat, can access a shared core instance through the NowSDK.core property.

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowCoreService - accessTokenDidFail\(for service: NowService\)

Notifies the SDK core that the access token used to authorize the API requests to the ServiceNow instance for the specified service is no longer valid.

The SDK core returns a valid access token if it is able to generate one or returns an error.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

|Name|Type|Description|
|----|----|-----------|
|for service|[NowService](../../NowService/concept/NowServiceiOSProtocol.md#)|Feature service requesting the access token.|

<table id="table_q5n_vcb_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher&lt;NowSDK.AccessToken, AccessTokenProviderError&gt;

</td><td>

Success: Valid access token.Failure: AccessTokenProviderError

Possible values:

-   userSessionError
-   accessTokenRetrievalFailed
-   hostReturnedNoTokens - Indicates a guest user

</td></tr></tbody>
</table>```
NowSDK.core()?.accessTokenDidFail(for: someService)
  .mapError { YourCustomError.accessTokenFailed($0) }

.flatMap(self.handleFailedAccessToken())
  .eraseToAnyPublisher()
```

## NowCoreService - accessTokenDidFail\(for service: NowService\) async throws

Notifies the SDK core that the access token used to authorize the API requests to the ServiceNow instance for the specified service is no longer valid.

The SDK core returns a valid access token if it is able to generate one or returns an error.

|Name|Type|Description|
|----|----|-----------|
|for service|[NowService](../../NowService/concept/NowServiceiOSProtocol.md#)|Feature service requesting the access token.|

<table id="table_q5n_vcb_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NowSDK.AccessToken

</td><td>

Returned when the method is successful. Valid access token.

</td></tr><tr><td>

AccessTokenProviderError

</td><td>

Thrown when the method fails. Indicates an error retrieving an access token. Possible values:

-   userSessionError
-   accessTokenRetrievalFailed
-   hostReturnedNoTokens - Indicates a guest user

</td></tr></tbody>
</table>The following code examples shows how to call this method.

```
do {
    let accessToken = try await NowSDK.core()?.accessTokenDidFail(for: someService)
} catch {
    self.handleFailedAccessToken(error)
}
```

## NowCoreService - canRequestPermission\(\_ permission: DevicePermission\)

Queries the host application as to whether the service is allowed to request the device permission.

This function does not request the permission, only whether it is allowed to query the device permission. Feature services should call this function to determine if they are allowed to request a desired device permission.

<table id="table_t4p_c1b_npb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

permission

</td><td>

DevicePermission

</td><td>

Device for which the request is being made.Possible values \(case-sensitive\):

-   camera
-   location
-   microphone
-   photoLibrary
-   speachRecognition

</td></tr></tbody>
</table><table id="table_u4p_c1b_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the host application allows the SDK to request the specified device permission.Possible values:

-   true: Device permission can be requested.
-   false: Device permission cannot be requested.

</td></tr></tbody>
</table>```
extension AppDelegate: DevicePermissionDelegate {
  func canRequestPermission(_ permission: DevicePermission) -> Bool {
    return true
  }
}
```

## NowCoreService - isGuestUser\(for service: NowService\) async

Checks whether the current user is a guest user.

|Name|Type|Description|
|----|----|-----------|
|for service|NowService|Feature service for which to perform the guest user check.|

<table id="table_vgj_4w2_lxb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user is a guest user.Possible values:

-   true: Current user of the specified service is a guest user.
-   false: Current user of the specified service is not a guest user.

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
let isGuestUser = await NowSDK.core()?.isGuestUser(for: someService)
```

## NowCoreService - refreshAllSettings\(\)

Refreshes all SDK settings for all services by re-fetching them from the active servers.

To receive updated SDK settings values whenever they're refreshed, subscribe to the publisher provided by the [NowCoreService - settingsPublisher\(for service: NowService\)](NowCoreServiceiOSAPI.md#) function.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

```
NowSDK.core()?.refreshAllSettings()
```

## NowCoreService - refreshSettings\(for service: NowService\)

Refreshes the SDK settings for the specified service by re-fetching them from the server.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

|Name|Type|Description|
|----|----|-----------|
|for service|NowService|Feature service, such as NowChat or NowAnalytics, requesting the settings refresh.|

<table id="table_rv3_knb_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher&lt;Settings, SettingsError&gt;

</td><td>

Success: Dictionary of refreshed SDK settings. Feature services need to examine the returned data for the settings relevant to their specific features.Failure: SettingsError - Type and description of error encountered.

Possible values:

-   fetchError
-   fetchFailed
-   invalidJSON
-   invalidProvider
-   notAuthorized
-   sdkNotLicensed
-   settingNotFound
-   unknown

</td></tr></tbody>
</table>```
var subscriptions = Set<AnyCancellable>()
NowSDK.core?.refreshSettings(for: someService)
  .sink(receiveCompletion: { completion in
    if case .failure(let error) = completion {
      print("Refresh failed with error:\ (error)")
    }
  }, receiveValue: { settings in
    print("Received refreshed settings:\ (settings)")
  })
  .store(in: &subscriptions)
```

## NowCoreService - refreshSettings\(for service: NowService\) async throws

Refreshes the SDK settings for the specified service by re-fetching them from the server.

|Name|Type|Description|
|----|----|-----------|
|for service|NowService|Feature service, such as NowChat or NowAnalytics, requesting the settings refresh.|

<table id="table_rv3_knb_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Settings

</td><td>

Returned when the method is successful. Dictionary of refreshed SDK settings. Feature services need to examine the returned data for the settings relevant to their specific features.

</td></tr><tr><td>

SettingsError

</td><td>

Thrown when the method fails.Possible values:

-   fetchError
-   fetchFailed
-   invalidJSON
-   invalidProvider
-   notAuthorized
-   sdkNotLicensed
-   settingNotFound
-   unknown

</td></tr></tbody>
</table>The following code examples shows how to call this method.

```
do {
    let settings = try await NowSDK.core()?.refreshSettings(for: someService)
    print("Received refreshed settings: \(settings)")
} catch {
    print("Refresh failed with Settings error: \(error)")
}
```

## NowCoreService - requestAccessToken\(for service: NowService\)

Acquires an access token for the specified service.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

|Name|Type|Description|
|----|----|-----------|
|for service|[NowService](../../NowService/concept/NowServiceiOSProtocol.md#)|Feature service requesting the access token.|

<table id="table_et1_ftb_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher&lt;NowSDK.AccessToken, AccessTokenProviderError&gt;

</td><td>

Success: NowSDK.AccessToken - Access token to use to authorize API requests made to a ServiceNow instance.Failure: AccessTokenProviderError - Type and description of error encountered.

Possible values:

-   `accessTokenRetrievalFailed`
-   `hostReturnedNoTokens` - Indicates a guest user
-   `userSessionError`

</td></tr></tbody>
</table>```
NowSDK.core()?.requestAccessToken(for: someService)
```

## NowCoreService - requestAccessToken\(for service: NowService\) async throws

Acquires an access token for the specified service.

|Name|Type|Description|
|----|----|-----------|
|for service|[NowService](../../NowService/concept/NowServiceiOSProtocol.md#)|Feature service requesting the access token.|

<table id="table_et1_ftb_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NowSDK.AccessToken

</td><td>

Returned when the method is successful. Access token to use to authorize API requests made to a ServiceNow instance.

</td></tr><tr><td>

AccessTokenProviderError

</td><td>

Thrown when the method fails. Indicates an error retrieving an access token.Possible values:

-   `accessTokenRetrievalFailed`
-   `hostReturnedNoTokens` - Indicates a guest user
-   `userSessionError`

</td></tr></tbody>
</table>The following code examples shows how to call this method.

```
do {
    let accessToken = try await NowSDK.core()?.requestAccessToken(for: someService)
} catch {
    self.handleFailedAccessToken(error)
}
```

## NowCoreService - requestNetworkService\(for service: NowService\)

Returns a reference to a shared network service that you can use to make API requests.

**Note:** This is a shared service. Altering settings or ending the session can cause issues for other feature services that share this session.

|Name|Type|Description|
|----|----|-----------|
|for service|[NowService](../../NowService/concept/NowServiceiOSProtocol.md#)|Feature service requesting the network service.|

|Type|Description|
|----|-----------|
|NetworkService|Shared network service that you can use to make API calls.|

The following code example shows how to call this function.

```
NowSDK.core()?.settingsPublisher(for: chatService)
.sink(receiveCompletion: { completion in
  if case .failure(let error) = completion {
    // Setting publisher failed with error
  }
}, receiveValue: { updatedSettings in
  // Receive array of SDK settings for chatService
})
.store(in: &subscriptions)
```

## NowCoreService - requestSettings\(forservice: NowService\)

Returns the SDK settings for the specified feature service.

**Note:** This method has been deprecated. You should use the async/await implementation of the method instead.

|Name|Type|Description|
|----|----|-----------|
|forservice|NowService|Feature service requesting the settings.|

<table id="table_rwv_s5b_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AnyPublisher&lt;Settings, SettingsError&gt;

</td><td>

Success: Settings - Array of SDK settings for the specified feature service.Failure: SettingsError - Type and description of associated error.

Possible values:

-   fetchError
-   fetchFailed
-   invalidJSON
-   invalidProvider
-   notAuthorized
-   sdkNotLicensed
-   settingNotFound
-   unknown

</td></tr></tbody>
</table>```
NowSDK.core()?.requestSettings(for: someService)
```

## NowCoreService - requestSettings\(for service: NowService\) async throws

Returns the SDK settings for the specified feature service.

|Name|Type|Description|
|----|----|-----------|
|for service|NowService|Feature service requesting the settings.|

<table id="table_rwv_s5b_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Settings

</td><td>

Returned when the method is successful. Array of SDK settings for the specified feature service.

</td></tr><tr><td>

SettingsError

</td><td>

Thrown when the method fails. Type and description of associated error.Possible values:

-   fetchError
-   fetchFailed
-   invalidJSON
-   invalidProvider
-   notAuthorized
-   sdkNotLicensed
-   settingNotFound
-   unknown

</td></tr></tbody>
</table>The following code examples shows how to call this method.

```
do {
    let settings = try await NowSDK.core()?.requestSettings(for: someService)
    print("Received settings: \(settings)")
} catch {
    print("Refresh saved with Settings error: \(error)")
}
```

## NowCoreService - settingsPublisher\(for service: NowService\)

Retrieves the settings for the publisher of the specified service.

|Name|Type|Description|
|----|----|-----------|
|for service|[NowService protocol - iOS](../../NowService/concept/NowServiceiOSProtocol.md#)|Feature service requesting the publisher subscription.|

|Type|Description|
|----|-----------|
|AnyPublisher&lt;Settings, Never&gt;|Success: Settings - Array of SDK settings for the specified feature service.|

The following code example shows how to call this function.

```
NowSDK.core()?.settingsPublisher(for: chatService)
.sink(receiveCompletion: { completion in
  if case .failure(let error) = completion {
    // Setting publisher failed with error
  }
}, receiveValue: { updatedSettings in
  // Receive array of SDK settings for chatService
})
.store(in: &subscriptions)
```

