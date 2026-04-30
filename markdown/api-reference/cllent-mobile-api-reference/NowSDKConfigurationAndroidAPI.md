---
title: NowSDKConfiguration class - Android
description: The NowSDKConfiguration class contains configuration information needed to initialize the NowSDK.Creates a new NowSDKConfiguration object.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowSDKConfiguration class - Android

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

Level of log messages for the associated logger to store.Valid values \(case-sensitive\):

-   Debug
-   Error
-   Fatal
-   Info
-   None

</td></tr><tr><td>

permissionDelegate

</td><td>

DevicePermissionDelegate

</td><td>

Delegate object called by the NowSDK to request permission from the host application to show system dialog for requesting the indicated device permission.

 For example:

```
override fun canRequestPermission(permission: DevicePermission): Boolean =
  when (permission) {
    DevicePermission.Camera -> true
    DevicePermission.Microphone -> false
  }
}
```

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowSDKConfiguration - NowSDKConfiguration\(authorizationProvider: NowSDKAuthorizationProviding, permissionDelegate: DevicePermissionDelegate, logLevel: NowLogLevel\)

Creates a new NowSDKConfiguration object.

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

Delegate object that is responsible for providing authorization tokens to the NowSDK upon request.

</td></tr><tr><td>

permissionDelegate

</td><td>

DevicePermissionDelegate

</td><td>

Delegate object called by the NowSDK to request permission from the host application to show system dialog for requesting the indicated device permission.

 For example:

```
override fun canRequestPermission(permission: DevicePermission): Boolean =
  when (permission) {
    DevicePermission.Camera -> true
    DevicePermission.Microphone -> false
  }
}
```

</td></tr><tr><td>

logLevel

</td><td>

NowLogLevel

</td><td>

Level of log messages for the associated logger to store.Valid values \(case-sensitive\):

-   Debug
-   Error
-   Fatal
-   Info
-   None

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
class SampleApplication : Application(), NowSDKAuthorizationProviding, DevicePermissionDelegate {

    private val nowSdkSettings = NowSDKSettings(
        instanceBaseURL = "https://instance-name.service-now.com",
        clientId = "client_id",
        user = "user"
    )

    private val coroutineScope = CoroutineScope(Dispatchers.IO)

    private val nowSDKConfiguration = NowSDKConfiguration(this, this, NowLogLevel.Debug)
    override fun onCreate() {
        super.onCreate()

        NowSDK.configure(this, nowSDKConfiguration)
    }


    override fun requestAuthorization(
        instanceURL: URL,
        callback: Consumer<List<AuthorizationToken>?>
    ) {
        coroutineScope.launch {
            when {
                nowSdkSettings.user.isNullOrBlank().not() -> authorizeWithJWT(
                    callback = callback,
                    user = nowSdkSettings.user,
                    clientId = nowSdkSettings.clientId
                )

                else -> authorizeWithGuest(callback = callback)
            }
        }
    }

    override fun canRequestPermission(permission: DevicePermission): Boolean {
        return true
    }
}
```

