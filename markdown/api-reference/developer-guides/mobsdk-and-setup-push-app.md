---
title: Setting up push notifications in your Android application
description: In addition to the tasks that you must perform on your ServiceNow instance to configure a push notification, you must also include specific code in your Android application.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure push notifications, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Setting up push notifications in your Android application

In addition to the tasks that you must perform on your ServiceNow® instance to configure a push notification, you must also include specific code in your Android application.

## Create the NowSDK NowPushService

One of the first things that needs to be done in your application is to retrieve the NowSDK NowPushService. Add code similar to the following snippet early within your main code body.

```
/**
 * Helper class used to handle different Now service instances.
 */
@Singleton
class SdkManager @Inject constructor() {

    private var nowPushService: NowPushService? = null

    /**
     * Create the NowPushService once in the lifetime of the application inside the Application
     * class or another manager class that will be injected into other classes via dagger/hilt.
     * NowPushService should be created after initializing the NowSDK
     */
    suspend fun getNowPushService(): NowPushService? {
        if (nowPushService != null) return nowPushService

        return NowPushSDK.makePushService(URL("https://instance-name.service-now.com")).getOrThrow()
            .also { this.nowPushService = it }
    }
}
```

For additional information on the NowPushSDK.makePushService\(\) method, refer to [NowPushSDK - makePushService\(instanceURL: URL\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowPushSDK/concept/NowPushSDKAndroidAPI.md#).

## Register the push token

Google Firebase provides a unique push token that identifies the device and application to receive push notifications. In order for an application to receive push notification, you must register this token using the NowPushService. Add a function similar to the following code snippet in your Android application. Ensure that you change **PushAppName** to the name of your Android application. This application must be registered with your ServiceNow® instance.

```
FirebaseMessaging.getInstance().token.addOnCompleteListener {task ->
  val token = task.result

  if (!task.isSuccessfull || token == null) {
    throw Exception("Unable to fetch token"))
  }

  pushService.registerPushToken(token, "PushAppName", {
      Log.v(TAF, "Successfully registered push token")
  }, { e ->
      Log.e(TAG, "Error registrating push", e)
  })
}
```

For additional information on the registerPushToken\(\) method, refer to [NowPushService - registerPushToken\(pushToken: String, pushApp: String, successCallback: Runnable, errorCallback: Consumer&lt;Throwable&gt;\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowPushService/concept/NowPushServiceAndroidAPI.md#).

## Unregister the push token

You need to unregister the push token whenever the user exits your application, such as when the user logs out. Use code similar to the following code snippet to unregister the push token. Ensure that you change **PushAppName** to the name of your Android application.

```
pushService.unregisterPushToken(token, "PushAppName", {
      Log.v(TAG, "Successfully unregistered push token")
}, { e ->
      Log.e(TAG, "Error unregistering push", e)
})
```

For additional information on the unregisterPushToken\(\) method, refer to [NowPushService - unregisterPushToken\(pushToken: String, pushApp: String, successCallback: Runnable, errorCallback: Consumer&lt;Throwable&gt;\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowPushService/concept/NowPushServiceAndroidAPI.md#).

## Implement the FirebaseMessagingService

You must implement the `FirebaseMessagingService` within your application. To setup and implement this service, follow the instructions in the [Android Firebase documentation](https://firebase.google.com/docs/cloud-messaging/android/receive).

Once setup, override the onMessageReceived\(\) method and pass the **RemoteMessage** through to the `NowPushService`. If the `NowPushService` recognizes the notification, it will process it and return the notification object for the application to handle. Currently, the only implemented notification is `NowPushVirtualAgent`. An unknown notification returns a `NotSupportedPushError` object.

```
//Custom coroutineScope created in the Firebase service class
private val serviceCoroutineScope = CoroutineScope(Dispatchers.IO)

override fun onMessageReceived(remoteMessage: RemoteMessage) {
  serviceCoroutineScope.launch {
    val result = handleNowPush(remoteMessage)

    if (result.isSuccess) {
      when (val push = result.getOrNull()) {
        is NowPushVirtualAgent -> handleVirtualAgentPush(push)
      }
    } else {
      // Not a NowPush. Handle host app push notification message here
    }
  }
}

private suspend fun handleNowPush(remoteMessage: RemoteMessage): Result<NowPushPayload> {
  val nowPushService = sdkManager.getNowPushService()

  return suspendCoroutine { cont ->
    nowPushService?.handlePush(remoteMessage,
      { cont.resume(Result.success(it)) }, { cont.resumeWithException(it) })
  }
}
```

For additional information on the handlePush\(\) method, refer to [NowPushService - handlePush\(remoteMessage: RemoteMessage, successCallback: Consumer&lt;NowPushPayload&gt;, errorCallback: Consumer&lt;Throwable&gt;\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowPushService/concept/NowPushServiceAndroidAPI.md#).

In addition, you must override onNewToken\(token: String\). Be sure to pass the token through to the pushService.registerPushToken\(\), similar to what was done in the "Register the push token" section.

