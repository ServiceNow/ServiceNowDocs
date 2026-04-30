---
title: NowSDKConfiguration class - iOS
description: The NowSDKConfiguration class contains configuration information needed to initialize the NowSDK.Creates a NowSDKConfiguration object.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowSDKConfiguration class - iOS

The NowSDKConfiguration class contains configuration information needed to initialize the NowSDK.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

authorizationProvider

</td><td>

NowSDKAuthorizationProviding

</td><td>

Delegate object that is responsible for providing authorization tokens to the NowSDK upon request.

</td></tr><tr><td>

logLevel

</td><td>

NowLogLevel

</td><td>

Level of log messages for the associated logger to store.Valid values:

-   debug
-   error
-   fatal
-   info
-   none

</td></tr><tr><td>

permisionDelegate

</td><td>

DevicePermissionDelegate

</td><td>

Delegate object called by the NowSDK to request permission from the host application to show system dialog requesting the indicated device permission.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowSDKConfiguration - init\(authorizationProvider: NowSDKAuthorizationProviding, permissionDelegate: DevicePermissionDelegate, logLevel: NowLogLevel\)

Creates a NowSDKConfiguration object.

<table id="table_rmy_jvq_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

authorizationProvider

</td><td>

NowSDKAuthorizationProviding

</td><td>

Delegate object that is responsible for providing authorization tokens to the NowSDK on request.

</td></tr><tr><td>

permissionDelegate

</td><td>

DevicePermissionDelegate

</td><td>

Delegate object called by the NowSDK to request permission from the host application to show the system dialog for requesting the indicated device permission. For example:```
class PermissionProvider:
DevicePermissionDelegate {
  func canRequestPermission(_ permission: DevicePermission) → Bool {
    return true
  }
}
```

</td></tr><tr><td>

logLevel

</td><td>

NowLogLevel

</td><td>

Level of log messages for the associated logger to store.This sets the logging level for the core services logger. You can also use the [NowLoggingService](../../NowLoggingService/concept/NowLoggingServiceiOSAPI.md#) API to set service log levels.

Valid values:

-   debug
-   error
-   fatal
-   info
-   none

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
guard 
  let instanceUrl = URL(string: "https://sn-instance.service-now.com") else {
  return
}

NowServiceConfiguration(instanceUrl: instanceUrl, appBundleId: "com.servicenow.appBundle")
```

