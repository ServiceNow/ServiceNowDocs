---
title: Implement Virtual and Live Agent chat
description: The Mobile SDK enables you to easily implement Virtual and Live Agent chat services within your Android application.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Implement Virtual and Live Agent chat

The Mobile SDK enables you to easily implement Virtual and Live Agent chat services within your Android application.

You use the [NowChatSDK](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowChatSDK/concept/NowChatSDKAndroidAPI.md#) API to create the chat service. Once the service is created, you must then start the chat user interface.

The following is a snippet that shows how to create the chat service and start the interface.

```
/**
 * Helper class used to handle different Now service instances.
 */
@Singleton
class SdkManager @Inject constructor() {

    private var chatService: NowChatService? = null

    /**
     * Create the NowChatService once in the lifetime of the application, inside the Application class or another manager class
     * that will be injected into other classes via dagger/hilt.
     * NowChatService should be created after initializing the NowSDK.
     */
    suspend fun getNowChatService(): NowChatService? {
        if (chatService != null) return chatService

        return NowChatSDK.makeChatService(URL("https://instance-name.service-now.com"),
            object : NowChatSdkCallbacks {})
            .getOrThrow()
            .also { this.chatService = it }
    }
}

//Activity that will start the NowChat
class MainActivity : AppCompatActivity() {

    @Inject
    lateinit var sdkManager: SdkManager

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        //Start NowChat using the activity
        lifecycleScope.launch {
            sdkManager.getNowChatService()?.start(this@MainActivity)
        }
    }
}
```

Before you can leverage the chat functionality within your application, you must configure Virtual Agent within your ServiceNow instance. For details, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Passing context variables to Live Agent and Virtual Agent chat

You can pass chat context variables when starting a chat session by passing the **contextData** parameter in the [NowChatService-start\(\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowChatService/concept/NowChatServiceAndroidAPI.md#) function. For additional information on chat context variables, see [Live agent chat context variables](https://www.servicenow.com/docs/access?context=live-agent-chat-context-vars&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

```
class MainActivity : AppCompatActivity() {
  @Inject

  lateinit var sdkManager: SdkManager

  override fun onCreate(savedInstanceState: Bundle?) { 
    super.onCreate(savedInstanceState)

    val contextData = mapOf("sys_id" to "123456789", "table" to "wm_task")
    //Start NowChat using the activity 
    lifecycleScope.launch {
      sdkManager.getNowChatService()?.start(this@MainActivity, contextData = contextData)
    }
  }
}
```

## Theme the chat user interface

You can customize the colors of the Live Agent and Virtual Agent chat UI by passing a theme object in the start\(\) call. For a list of elements that you can customize, see [NowChatService - launchIntent\(context:Context, nowChatTheme:NowChatTheme\):Intent](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowChatService/concept/NowChatServiceAndroidAPI.md#). By default, the chat UI uses the **nowUIColor** theme for all NowSDK UI elements. Refer to the sample application for an example on how to apply a theme to your chat UI.

