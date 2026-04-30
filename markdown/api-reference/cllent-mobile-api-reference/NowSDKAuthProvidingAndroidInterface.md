---
title: NowSDKAuthorizationProviding interface - Android
description: The NowSDKAuthorizationProviding interface provides a function that configures the link to the ServiceNow instance for which authorization is needed and any associated callbacks.Authorizes the currently logged-in user on the specified ServiceNow instance using the specified AuthorizationToken objects.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowSDKAuthorizationProviding interface - Android

The NowSDKAuthorizationProviding interface provides a function that configures the link to the ServiceNow instance for which authorization is needed and any associated callbacks.

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowSDKAuthorizationProviding - requestAuthorization\(instanceURL: URL, callback: Consumer&lt;List&lt;AuthorizationToken&gt;?&gt;\)

Authorizes the currently logged-in user on the specified ServiceNow instance using the specified AuthorizationToken objects.

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|ServiceNow instance for which the authorization is being requested.|
|callback|[Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html)​&lt;[List](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/)​&lt;[AuthorizationToken](../../AuthorizationToken/concept/AuthorizationTokenAndroidAPI.md#)&gt;?&gt;|Array of logged-in user specific Authorization Token objects.|

|Type|Description|
|----|-----------|
|None| |

```
class NowSDKAuthorizationManager: NowSDKAuthorizationProviding {
  override fun requestAuthorization(
    instanceURL: URL,
    callback: Consumer<List<AuthorizationToken>?>
  ){
    val token = JWTService.fetchJwt()
    val authorizationToken = AuthorizationToken(AuthorizationTokenType.JWT, token)
    val result = listOf(authorizationToken)
    callback.accept(result)
  }
}
```

