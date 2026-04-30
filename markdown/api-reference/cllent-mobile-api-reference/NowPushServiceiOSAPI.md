---
title: NowPushService class - iOS
description: The NowPushService class provides functions that enable interaction with the Push Notification service.Registers a unique token with the ServiceNow instance used to identify the push notifications for the current iOS device and specified application.Unregisters a previously registered push token.Parses the userInfo key-value pairs into a NowPushPayload object.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowPushService class - iOS

The NowPushService class provides functions that enable interaction with the Push Notification service.

<table class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

Configuration settings provided when the service was initialized.Data type: [NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowPushService - registerPushToken\(\_token: Data, pushAppName: String, environment: NowPushEnvironment, completion: @escaping \(Result&lt;Data, NowPushError&gt;\) -&gt; Void\)

Registers a unique token with the ServiceNow instance used to identify the push notifications for the current iOS device and specified application.

<table id="table_cr3_pgh_trb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\_token

</td><td>

Data

</td><td>

Data object of the push token to register. This is the token obtained from the Apple Developer site. For more information, see the Mobile SDK Developer Guide - iOS.

</td></tr><tr><td>

pushAppName

</td><td>

String

</td><td>

Name of the push application for which this token is being registered.

</td></tr><tr><td>

environment

</td><td>

NowPushEnvironment

</td><td>

Environment for which the token is being registered.Valid values:

-   production
-   sandbox

</td></tr><tr><td>

completion

</td><td>

@escaping \(Result​&lt;Data, NowPushError&gt;\) → Void

</td><td>

Completion handler to execute after the token has been attempted to be registered.-   Success: iOS push notification certificate.
-   Error: NowPushError - Information about the error that occurred when trying to register the token.

Possible values:

    -   decoding: Decoding error occurred.
    -   httpRequestFailure: Generic error that is returned whenever the http call is not a success \(2xx\).
    -   notAuthorized: Requestor is not authorized to perform the specified push notification operation.
    -   unsupportedData: Push payload is invalid.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to register a push notification token for the TestPushApp application.

```
func registerForPushNotifications(deviceToken: Data) {
  pushService.registerPushToken(deviceToken,
      pushAppName: "TestPushApp",
      environment: environment) { [weak self] result in
    guard let self = self else { return }
    switch result {
      case .success:
        UserDefaults.standard.set(true, forKey: "pushNotificationsRegistered")
        self.pushRegistrationState = .registrationSuccess
      case .failure:
        UserDefaults.standard.set(false, forKey: "pushNotificationsRegistered")
        self.pushRegistrationState = .registrationFailed
    }
  }
}
```

## NowPushService - unregisterPushToken\(\_token: Data, pushAppName: String, environment: NowPushEnvironment, completion: @escaping \(Result&lt;Data, NowPushError&gt;\) -&gt; Void\)

Unregisters a previously registered push token.

<table id="table_fvk_rjh_trb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\_token

</td><td>

Data

</td><td>

Data object of the push token to unregister.

</td></tr><tr><td>

pushAppName

</td><td>

String

</td><td>

Name of the push application for which this token is being unregistered.

</td></tr><tr><td>

environment

</td><td>

NowPushEnvironment

</td><td>

Environment for which the token is being registered.Valid values:

-   production
-   sandbox

</td></tr><tr><td>

completion

</td><td>

@escaping \(Result​&lt;Data, NowPushError&gt;\) → Void

</td><td>

Completion handler to execute after the token has been attempted to be unregistered.-   Success: API response data.
-   Error: `NowPushError` - Information about the error that occurred when trying to unregister the token.

Possible values:

    -   decoding: Decoding error occurred.
    -   httpRequestFailure: Generic error that is returned whenever the http call is not a success \(2xx\).
    -   notAuthorized: Requestor is not authorized to perform the specified push notification operation.
    -   unsupportedData: Push payload is invalid.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to unregister the push notification token associated with the TestPushApp application.

```
func unregisterFromPushNotifications(deviceToken: Data) {
  pushService.unregisterPushToken(deviceToken, pushAppName: "TestPushApp", environment: environment) { [weak self] result in
    guard let self = self else { return }
    switch result {
      case .success:
        UserDefaults.standard.set(false, forKey: "pushNotificationsRegistered")
        self.pushRegistrationState = .unregisterSuccess
      case .failure:
        self.pushRegistrationState = .unregisterFailed
    }
  }
}
```

## NowPushService - payloadFromUserInfo\(\_userInfo: \[AnyHashable: Any\]\)

Parses the `userInfo` key-value pairs into a `NowPushPayload` object.

|Name|Type|Description|
|----|----|-----------|
|\_userInfo|\[AnyHashable: Any\]|Push payload content received as part of the push notification.|

<table id="table_wqs_mkh_trb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Result&lt;NowPushPayload, NowPushError&gt;

</td><td>

Returns the results of the payload parsing.-   Success: Parsed `NowPushPayload` object.
-   Failure: `NowPushError` - Information about the error that was encountered while parsing the specified user payload.

Possible values:

    -   decoding: Decoding error occurred.
    -   httpRequestFailure: Generic error that is returned whenever the http call is not a success \(2xx\).
    -   notAuthorized: Requestor is not authorized to perform the specified push notification operation.
    -   unsupportedData: Push payload is invalid.

</td></tr></tbody>
</table>This example shows how to parser a user payload.

```
func userNotificationCenter(_ center: UNUserNotificationCenter,
    didReceive response: UNNotificationResponse,
    withCompletionHandler completionHandler: @escaping () -> Void) {
  guard let pushService = pushService else {
    completionHandler()
    return
  }
  let userInfo = response.notification.request.content.userInfo
  _ = pushService.payloadFromUserInfo(userInfo)
    .flatMap(handleNowPushPayload)
}


func handleNowPushPayload(_ payload: NowPushPayload) -> Result<Void, NowPushError> {
  guard payload is NowPushVirtualAgent else {
    return .failure(NowPushError.unsupportedData)
  }
  launchVirtualAgent()
  return .success(())
}
```

