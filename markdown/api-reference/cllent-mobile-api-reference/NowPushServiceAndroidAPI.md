---
title: NowPushService class - Android
description: The NowPushService class provides functions that enable interaction with the Push Notification service.Processes a push notification request.Registers a unique Firebase token with the ServiceNow instance used to identify the push notifications for the current Android device and specified application.Unregisters the specified Firebase push token with the associated ServiceNow instance.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowPushService class- Android

The NowPushService class provides functions that enable interaction with the Push Notification service.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

Service configuration to associate with the service.Data type: [NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationAndroidAPI.md)

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowPushService - handlePush\(remoteMessage: RemoteMessage, successCallback: Consumer&lt;NowPushPayload&gt;, errorCallback: Consumer&lt;Throwable&gt;\)

Processes a push notification request.

**Note:** Currently the only implemented push notification type is `NowPushVirtualAgent`. Any other passed push notification type returns a [NotSupportedPushError](../../NotSupportedPushError/concept/NotSupportedPushErrorAndroidAPI.md#) object.

|Name|Type|Description|
|----|----|-----------|
|remote Message|[Remote Message](https://firebase.google.com/docs/reference/android/com/google/firebase/messaging/RemoteMessage)|Notification as received by `com.google.firebase.messaging.FirebaseMessagingService.onMessageReceived`. For additional information, see [Receive messages in an Android app](https://firebase.google.com/docs/cloud-messaging/android/receive).|
|success Callback|[Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer) &lt;[NowPushPayload](../../NowPushPayload/concept/NowPushPayloadAndroidInterface.md#)&gt;|Callback to return the processed **NowPushPayload** to.|
|error Callback|[Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer) &lt;[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/)&gt;|Callback to return the thrown error to. If the error [NotSupportedPushError](../../NotSupportedPushError/concept/NotSupportedPushErrorAndroidAPI.md#) is thrown, the notification type is not supported by the mobile SDK, and must be processed outside of the mobile SDK framework.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to override onMessageReceived\(\) and pass the **RemoteMessage** through to the `NowPushService`. If the `NowPushService` recognizes the notification type, it processes the request and returns the notification object for the application to handle. Otherwise it throws the [NotSupportedPushError](../../NotSupportedPushError/concept/NotSupportedPushErrorAndroidAPI.md#).

```
override fun onMessageReceived(remodeeMessage: RemoteMessage){
  pushService.handlePush(remoteMessage, { push ->
    when (push) {
      is NowPushVirtualAgent → handleVirtualAgentPush(push)
    }, { error ->
        Log.e(TAG, "Unknown push", error)
        handleAppPushNotification(remoteMessage)
    })
}
```

## NowPushService - registerPushToken\(pushToken: String, pushApp: String, successCallback: Runnable, errorCallback: Consumer&lt;Throwable&gt;\)

Registers a unique Firebase token with the ServiceNow instance used to identify the push notifications for the current Android device and specified application.

In order for the ServiceNow instance to generate notifications Android device to receive notifications from the application, this token must be registered.

|Name|Type|Description|
|----|----|-----------|
|pushToken|String|Firebase token retrieved by either [com.google.firebase.messaging.FirebaseMessaging.getToken](https://firebase.google.com/docs/reference/js/v8/firebase.messaging.Messaging#gettoken) or [com.google.firebase.messaging.FirebaseMessagingService.onNewToken](https://firebase.google.com/docs/cloud-messaging/android/client).|
|pushApp|String|Name of the push application as specified in the Push Application table on the associated ServiceNow instance.|
|success Callback|[Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html)|Callback executed when the token registration is successful.|
|errorCallback|[Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer) &lt;[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/)&gt;|Callback executed when the token registration fails.|

|Type|Description|
|----|-----------|
|None| |

This example registers a push token for the current Android device and the application "PushAppName".

```
FirebaseMessaging.getInstance().token.addOnCompleteListener { task ->
  val token = task.result

  if (!task.isSuccessful || token == null) {
    throw Exception("Unable to fetch token"))
  }

  pushService.registerPushToken(token, "PushAppName", {
    Log.v(TAG, "Successfully registered push token")
  }, { e ->
    Log.e(TAG, "Error registering push", e)
  })
}
```

## NowPushService - unregisterPushToken\(pushToken: String, pushApp: String, successCallback: Runnable, errorCallback: Consumer&lt;Throwable&gt;\)

Unregisters the specified Firebase push token with the associated ServiceNow instance.

|Name|Type|Description|
|----|----|-----------|
|pushToken|String|Firebase token to unregister. Retrieved by either [com.google.firebase.messaging.FirebaseMessaging.getToken](https://firebase.google.com/docs/reference/js/v8/firebase.messaging.Messaging#gettoken) or [com.google.firebase.messaging.FirebaseMessagingService.onNewToken](https://firebase.google.com/docs/cloud-messaging/android/client).|
|pushApp|String|Name of the push application associated with the token to unregister. This information is stored in the Push Application table on the associated ServiceNow instance.|
|success Callback|[Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html)|Callback executed when the token unregistration is successful.|
|erro rCallback|[Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer) &lt;[Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/)&gt;|Callback executed when the token unregistration fails.|

|Type|Description|
|----|-----------|
|None| |

This code example shows how to unregister a push token such as when the user logs out of the application.

```
pushService.unregisterPushtoken(token, "PushAppName", {
  Log.v(TAG, "Successfully unregistered push token")
},  { e ->
  Log.e(TAG, "Error unregistering push", e)
})
```

