---
title: NowSDK - Android
description: The NowSDK class is a singleton that provides the public API for the NowSDK. This class is the gateway to all Android SDK feature services.Configures the NowSDK for use.Clears all user sessions persisted in memory.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowSDK - Android

The NowSDK class is a singleton that provides the public API for the NowSDK. This class is the gateway to all Android SDK feature services.

Before initializing a feature service, you must initialize the SDK itself by calling [NowSDK.configure\(\)](NowSDKAndroidAPI.md#). For additional information on getting started with the Android NowSDK, refer to the ServiceNow Mobile SDK Developers Guide - Android.

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowSDK - configure\(application: Application, configuration: NowSDKConfiguration\)

Configures the NowSDK for use.

You must call this function before attempting to use any of the feature services provided by the SDK.

|Name|Type|Description|
|----|----|-----------|
|application|[Application](https://developer.android.com/reference/kotlin/android/app/Application.html)|Reference to the hosting application object.|
|configuration|NowServiceConfiguration|Object containing the information necessary to initialize the NowSDK.|

|Type|Description|
|----|-----------|
|None|NowSDKError is thrown if the provided configuration is invalid.|

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

## NowSDK - logout\(\)

Clears all user sessions persisted in memory.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
class SampleApplication : Application() {

    private val nowSDKConfiguration = NowSDKConfiguration(authorizationProvider, permissionDelegate, NowLogLevel.Debug)

    override fun onCreate() {
        super.onCreate()
        NowSDK.configure(this, nowSDKConfiguration)
    }

    fun logout() {
        // Clear all user session when an application resets the user session
        NowSDK.logout()
    }
}
```

