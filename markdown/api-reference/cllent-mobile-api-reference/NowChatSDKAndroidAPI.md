---
title: NowChatSDK class - Android
description: The NowChatService class provides the function necessary to create a NowChatService that interacts with NowChat. NowChat provides the ability to embed Live Agent and Virtual Agent within your application.Creates a NowChat service. This is a suspend function.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatSDK class - Android

The NowChatService class provides the function necessary to create a NowChatService that interacts with NowChat. NowChat provides the ability to embed Live Agent and Virtual Agent within your application.

For additional information on Live Agent and Virtual Agent, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowChatSDK - makeChatService\(instanceURL: URL, nowChatSdkCallbacks\)

Creates a NowChat service. This is a suspend function.

|Name|Type|Description|
|----|----|-----------|
|instanceURL|[URL](https://developer.android.com/reference/kotlin/java/net/URL.html)|URL of the ServiceNow instance that the NowChatService should interact with.|
|nowChatSdkCallbacks|[NowChatSdkCallbacks](../../NowChatSdkCallbacks/concept/NowChatSdkCallbacksAndroidInt.md#)|Callbacks for the host application to use to configure the NowChatService.|

|Type|Description|
|----|-----------|
|None| |

```
@Inject lateinit var sdkSettingsProvider: Provider<NowSDKSettings>
@Inject lateinit var chatCallbacks: SampleAppNowChatSDKCallbacks

private fun launchChat() {
  binding.progressBar.visibility = View.VISIBLE

  NowChatSDK.makeChatService(
    URL(sdkSettingsProvider.get().instanceBaseURL),
    chatCallbacks
  ) .onSuccess {
    it.start(this, chatCallbacks.nowChatThemeColors) }
  } .onFailure {
     Log.e("NowChat", "Unable to launch chat: $it")
  }
}
```

