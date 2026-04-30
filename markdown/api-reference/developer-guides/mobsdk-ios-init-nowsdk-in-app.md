---
title: Initialize the NowSDK in your application
description: To access the functionality provided by the NowSDK, you must first initialize the NowSDK in your application.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Initialize the NowSDK in your application

To access the functionality provided by the NowSDK, you must first initialize the NowSDK in your application.

The Mobile SDK initialization is asynchronous. It is a good practice to start the initialization process as early as possible, such as in the application delegate’s `application(application:didFinishLaunchingWithOptions:)` function. Initialization only needs to occur once per application launch. There is no need to reinitialize when foregrounded or when a new scene is detected.

The following diagram shows the initialization sequence for NowSDK and feature services:

![MobileSDK integration flow diagram](../image/mobsdk-init-diagram.png)

To initialize the ServiceNow Mobile SDK in your iOS application you’ll need an authorization provider conforming to `NowSDKAuthorizationProviding`, which uses your JWT provider information, and a delegate conforming to `DevicePermissionDelegate`.

The following is an example of a structure of an SDK initialization. For additional code examples, refer to the ServiceNow Mobile SDK sample application.

```
// 

//  JWTProvider.swift 

import Foundation 
import NowSDK 

class JWTProvider: NowSDKAuthorizationProviding { 
  let token: String 

  init(token: String) { 
    self.token = token 
  } 

  func requestAuthorization(for instanceUrl: URL, completion: @escaping ([AuthorizationToken]?) -> Void) { 
    completion([AuthorizationToken(type: .jwt, token: token)]) 
  } 
} 
```

```
//
//  PermissionProvider.swift 

import Foundation
import NowSDK 

class PermissionProvider: DevicePermissionDelegate { 
  var isUserPermissionAllowed: Bool { Bool.random() } 

  func canRequestPermission(_ permission: DevicePermission) -> Bool { 
    guard isUserPermissionAllowed else { false } 
    return true 
  } 
}
```

```
//  
//  AppDelegate.swift  

import Foundation  
import NowSDK  

@main 
class AppDelegate: UIResponder, UIApplicationDelegate { 
  func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool { 

    let jwtProvider = JWTProvider(token: "a_valid_token”) 
    let permissionDelegate = PermissionProvider()  
    let logLevel: NowLogLevel = .debug 

    let config = NowSDKConfiguration(authorizationProvider: jwtProvider, permissionDelegate: permissionProvider, logLevel: logLevel)  

    do { 
      try NowSDK.configure(with: config) 
    } catch { 
      // Handle 'error' 
    }

    return true 

}
```

## Guest users

If the current user is not authenticated, it is possible to for them to access SDK functionality as a guest. To indicate that the current user is a guest, the requestAuthorization function in the authorization provider should complete with a guest type of AuthorizationToken, as shown below. The token value in this case is not important so long as the AuthorizationTokenType is set to `.guest`. For additional information on guest users, see [Configure guest user access](../../task/mobsdk-config-guest-access.md).

```
//  GuestTokenProvider.swift 
import Foundation 
import NowSDK 
class GuestTokenProvider: NowSDKAuthorizationProviding { 
    func requestAuthorization(for instanceUrl: URL,  
        completion: @escaping ([AuthorizationToken]?) -> Void) { 
        completion([AuthorizationToken(type: .guest, token: "")]) 
    } 
} 
```

## Logging users out of the SDK

After a user is logged out of a host application, you should call the `NowSDK.logout()` method to clear that user's ServiceNow sessions and tokens from the SDK. For example:

```
func onLogout() {
  NowSDK.logout()
} 
```

