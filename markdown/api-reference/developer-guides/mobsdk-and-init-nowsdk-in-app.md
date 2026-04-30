---
title: Initialize the NowSDK in your application
description: In order to use the Mobile SDK in your application, you need to perform SDK initialization, authorization, and logging.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Initialize the NowSDK in your application

In order to use the Mobile SDK in your application, you need to perform SDK initialization, authorization, and logging.

As you use the NowSDK, it makes a request to configure the SDK and provides callbacks from the SDK. Once the SDK is configured, an application can use the feature services and their associated APIs. This setup/configuration helps to make an authenticated call to a ServiceNow instance.

The following is an example of how to initialize the NowSDK in your Android application.

```
//Helper class to encapsulate value needed to initialize the sdk
data class NowSDKSettings(val instanceBaseURL : String, val clientId: String, val user: String?)

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

    private fun authorizeWithJWT(
        callback: Consumer<List<AuthorizationToken>?>,
        user: String?,
        clientId: String
    ) {
        //Get JWT token needed for the sdk initialization.
        val jwtToken ="jwt_token"

        callback.accept(listOf(AuthorizationToken(AuthorizationTokenType.JWT, jwtToken)))
    }

    private fun authorizeWithGuest(callback: Consumer<List<AuthorizationToken>?>) {
        callback.accept(
            listOf(
                AuthorizationToken(
                    AuthorizationTokenType.Guest,
                    ""
                )
            )
        )
    }
}
```

