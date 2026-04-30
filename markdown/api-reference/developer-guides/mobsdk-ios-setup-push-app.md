---
title: Setting up push notifications in your iOS application
description: In addition to the tasks that you must perform on your ServiceNow instance to configure a push notification, you must also include specific code in your iOS application.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure push notifications, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Setting up push notifications in your iOS application

In addition to the tasks that you must perform on your ServiceNow instance to configure a push notification, you must also include specific code in your iOS application.

## Create the NowSDK NowPushService

One of the first things that needs to be done in your application is to create a `NowPushService`. The `NowPush` SDK provides a factory function to create this service. Add code similar to the following snippet early within your main code body.

```
func setup(with instanceURL: URL) -> AnyPublisher<NowService, ConfigurationError> {
  NowPush.makePushService(instanceUrl: instanceURL)
    .mapError { .sdkError($0) }
    .map { $0 as NowService }
    .eraseToAnyPublisher()
}
```

For additional information on the NowPush.makePushService\(\) method, refer to [NowPush API - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowPush/concept/NowPushiOSAPI.md#).

## Register the push token

Apple provides a unique push notification token that identifies the device and application to receive push notifications. In order for an application to receive push notification, you must register this token using the `NowPushService`. Add a function similar to the following code snippet in your iOS application. This application must be registered with your ServiceNow instance.

```
func registerForPushNotifications(deviceToken: Data) {
  pushService.registerPushToken(deviceToken,
      pushAppName: "TestPushApp", // Modify this to be your iOS application name
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

For additional information on the registerPushToken\(\) method, refer to [NowPushService - registerPushToken\(\_token: Data, pushAppName: String, environment: NowPushEnvironment, completion: @escaping \(Result&lt;Data, NowPushError&gt;\) -&gt; Void\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowPushService/concept/NowPushServiceiOSAPI.md#).

## Unregister the push token

You need to unregister a push token whenever the user exits your application, such as when the user logs out. Use code similar to the following code snippet to unregister a push token. Ensure that you change **pushAppName** to the name of your iOS application.

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

For additional information on the unregisterPushToken\(\) method, refer to [NowPushService - unregisterPushToken\(\_token: Data, pushAppName: String, environment: NowPushEnvironment, completion: @escaping \(Result&lt;Data, NowPushError&gt;\) -&gt; Void\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowPushService/concept/NowPushServiceiOSAPI.md#).

## Parse push payload

You will need to parse push notification payloads into a `NowPushPayload` object to collect information and to use the data in other parts of the application. Currently, this is only available for Virtual Agent push notifications. Use code similar to the following

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

