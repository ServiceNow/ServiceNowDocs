---
title: Pass NowChatConfiguration to modify the behavior of NowChat
description: You can pass an optional NowChatConfiguration parameter when starting a chat session to modify some of the behavior of NowChat.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Implement Virtual and Live Agent chat, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Pass NowChatConfiguration to modify the behavior of NowChat

You can pass an optional **NowChatConfiguration** parameter when starting a chat session to modify some of the behavior of NowChat.

The NowChatConfiguration object contains the following options:

-   **closePrompt**: Prompt text that appears before exiting a chat window. You define this prompt text through the following parameters:
    -   **header**: Nullable string value that appears on the prompt’s header.
    -   **message**: String value that appears on the prompt’s main body.
    -   **acceptButtonTitle**: String value that appears on the primary button of the prompt. This button closes the chat window.
    -   **declineButtonTitle**: String value that appears on the secondary button of the prompt. This button dismisses the prompt without closing the chat window.
-   **disabledFeatures**: List of NowChat features to disable. Refer to the NowChatConfiguration.Feature enum class for the list of features that you can disable.
-   **conversationOptions**: List of conversation options to apply to NowChat. Refer to the NowChatConvestation.ConversationOption enum class for the list of options that you can apply.
-   **uiConfiguration**: UIConfiguration value used to configure UI components in NowChat.

The following code example shows how to use NowChatConfiguration\(\) to configure NowChat.

```
class MainActivity : AppCompatActivity() {
  @Inject

  lateinit var sdkManager: SdkManager
 
  override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
 
    //Drawable to use instead of the default NowChat back button.
    val myDrawable = ContextCompat.getDrawable(activity, R.drawable.my_drawable)
 
    val nowChatConfiguration = NowChatConfiguration(
      closePrompt = NowChatConfiguration.ClosePrompt(
        header = null,
        message = "Are you sure you want to leave?",
        acceptButtonTitle = "Yes",
        declineButtonTitle = "No"
      ),
      disabledFeatures = listOf(NowChatConfiguration.Feature.START_NEW_CONVERSATION), 
      conversationOptions = listOf(NowChatConfiguration.ConversationOption.FORCE_NEW_CONVERSATION), 
      uiConfiguration = NowChatConfiguration.UIConfiguration( 
        closeButton =  NowChatConfiguration.CloseButton( 
          icon = myDrawable
        ),
        attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible = false)
      )
    )
 
    //Start NowChat 
    lifecycleScope.launch { 
      sdkManager.getNowChatService()?.start(this@MainActivity, nowChatConfiguration = nowChatConfiguration) 
    }
  }
} 
```

For additional information, see [NowChatConfiguration class - Android](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowChatOptions/concept/NowChatOptionsAndroid.md#) and [NowChatService - start\(activity: Activity, themeColors: NowChatTheme = object: NowChatTheme\{\}, contextData: Map&lt;String, Any&gt; = mapOf\(\), chatConfiguration: NowChatConfiguration? = null\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/NowChatService/concept/NowChatServiceAndroidAPI.md#).

