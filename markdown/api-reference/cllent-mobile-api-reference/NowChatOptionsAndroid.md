---
title: NowChatConfiguration class - Android
description: The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.Configures options for the current chat session. This method enables you to show a prompt before closing a chat window, disable features while using chat, apply different conversation options when using chat, and configure UI components in NowChat.Defines the UI configurations to apply to the upload attachment button that appears next to the text input while talking with a live agent.Defines the configuration of the close button used for back navigation on the NowChat toolbar. You then pass this object into the NowChatConfiguration\(\) method to configure the close button to use within the chat session.Creates and returns a ClosePrompt object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) method to configure the close prompt options within the chat session.Creates and returns a UIConfiguration object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) constructor to configure UI components in NowChat.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatConfiguration class- Android

The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.

**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowChatConfiguration - NowChatConfiguration\(closePrompt: ClosePrompt? = null, disabledFeatures: List&lt;Feature&gt;? = null, conversationOptions: List&lt;ConversationOption&gt;? = null, uiConfiguration: UIConfiguration? = null\)

Configures options for the current chat session. This method enables you to show a prompt before closing a chat window, disable features while using chat, apply different conversation options when using chat, and configure UI components in NowChat.

<table id="table_ugs_wjd_kbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

closePrompt

</td><td>

[ClosePrompt](NowChatOptionsAndroid.md#) object

</td><td>

Prompt to display before closing the associated chat window.Call the [NowChatConfiguration.ClosePrompt\(\)](NowChatOptionsAndroid.md#) subclass to define the value of this parameter.

For example:

```
closePrompt = NowChatConfiguration.ClosePrompt(
  header = null,
  message = "Are you sure you want to leave?",
  acceptButtonTitle = "Yes",
  declineButtonTitle = "No"
)
```

If you don't want to display a close prompt, pass null.

</td></tr><tr><td>

disabledFeatures

</td><td>

List&lt;NowChatConfiguration.Feature&gt;

</td><td>

List of chat features to disable within the current chat session.Valid value:

START\_NEW\_CONVERSATION: Hide/disable the **StartNew Conversation** button that appears in a chat window.

The available chat features are defined in the NowChatConfiguration.Feature enum class.

For example:

```
disabledFeatures = listOf(NowChatConfiguration.Feature.START_NEW_CONVERSATION)
```

If you don't want to disable any features, pass null.

</td></tr><tr><td>

conversationOptions

</td><td>

List&lt;ConversationOption&gt;?

</td><td>

List of conversation options to apply to NowChat. Valid values:

-   END\_CONVERSATION\_ON\_EXIT: Ongoing conversation is terminated when exiting the NowChat window.
-   FORCE\_NEW\_CONVERSATION: Forces a new chat conversation when NowChat starts.

The available conversation options are defined in the NowChatConfiguration.ConversationOption enum class.

For example:

```
conversationOptions = listOf(NowChatConfiguration.ConversationOption.FORCE_NEW_CONVERSATION),
```

If you don't want to apply any options, pass null.

</td></tr><tr><td>

uiConfiguration

</td><td>

[UIConfiguration?](NowChatOptionsAndroid.md#)

</td><td>

UIConfiguration values to use to configure UI components in NowChat. Valid values:

-   **attachmentUploadButton**: Configuration for the `AttachmentUploadButton` that is shown next to the text input while talking with a live agent.
-   **closeButton**: Configuration for the `CloseButton` used for back navigation on the NowChat toolbar.

For example:

```
uiConfiguration = NowChatConfiguration.UIConfiguration(
  closeButton = NowChatConfiguration.CloseButton(
    icon = myDrawable
  ),
  attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible = false)
)
```

To use the default configuration, pass null.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|NowChatConfiguration|Returns a NowChatConfiguration object that you can pass when calling the [NowChatService - start\(activity: Activity, themeColors: NowChatTheme = object: NowChatTheme\{\}, contextData: Map&lt;String, Any&gt; = mapOf\(\), chatConfiguration: NowChatConfiguration? = null\)](../../NowChatService/concept/NowChatServiceAndroidAPI.md#) method.|

The following code example shows how to call this method.

```
suspend fun launchChat() {
  val chatService = getNowChatService()
 
  //Drawable to use instead of the default NowChat back button.
  val myDrawable = ContextCompat.getDrawable(activity, R.drawable.my_drawable)
     
  val chatConfiguration = NowChatConfiguration(
    closePrompt = NowChatConfiguration.ClosePrompt(
      header = null,
      message = "Are you sure you want to leave?",
      acceptButtonTitle = "Yes",
      declineButtonTitle = "No"
    ),
    disabledFeatures = listOf(NowChatConfiguration.Feature.START_NEW_CONVERSATION),
    conversationOptions = listOf(NowChatConfiguration.ConversationOption.FORCE_NEW_CONVERSATION),
    uiConfiguration = NowChatConfiguration.UIConfiguration(
      closeButton = NowChatConfiguration.CloseButton(
        icon = myDrawable
      ),
      attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible = false)
    )
  )

  chatService?.start(activity, chatConfiguration)
}
```

## NowChatConfiguration - AttachmentUploadButton\(isVisible: Boolean = true\)

Defines the UI configurations to apply to the upload attachment button that appears next to the text input while talking with a live agent.

AttachmentUploadButton is a subclass of the NowChatConfiguration class.

<table id="table_b2d_4yr_ddc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isVisible

</td><td>

Boolean

</td><td>

Flag that indicates the visibility of the upload attachment button.Valid values:

-   true: Upload attachment button is visible.
-   false: Upload attachment button is hidden.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|UI configuration object.|

The following code example shows how to hide the AttachmentUploadButton.

```
suspend fun launchChat() {
  val chatService = getNowChatService()

  val chatConfiguration = NowChatConfiguration(
    uiConfiguration = NowChatConfiguration.UIConfiguration(
      attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible = false)
    )
  )
 
  chatService?.start(activity, chatConfiguration)
}
```

## NowChatConfiguration - CloseButton\(icon: Drawable?\)

Defines the configuration of the close button used for back navigation on the NowChat toolbar. You then pass this object into the NowChatConfiguration\(\) method to configure the close button to use within the chat session.

CloseButton\(\) is a subclass of the NowChatConfiguration class.

<table id="table_sbp_zwr_ddc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

icon

</td><td>

Drawable?

</td><td>

Drawable object to use for the close \(back\) button.You can use the ContextCompat.getDrawable\(\) method to obtain this drawable object.

For example:

```
val myDrawable = ContextCompat.getDrawable(activity, R.drawable.my_drawable)
```

To use the default drawable, pass null.

Default: NowChat back button

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Close button configuration object.|

The following code example shows how to set a custom icon for the close button on the NowChat toolbar.

```
suspend fun launchChat() {
  val chatService = getNowChatService()
 
  //Drawable to use instead of the default NowChat back button.
  val myDrawable = ContextCompat.getDrawable(activity, R.drawable.my_drawable)

  val chatConfiguration = NowChatConfiguration(
    uiConfiguration = NowChatConfiguration.UIConfiguration(
      closeButton = NowChatConfiguration.CloseButton(
        icon = myDrawable
      )
    )
  )

  chatService?.start(activity, chatConfiguration)
}
```

## NowChatConfiguration - ClosePrompt\(header: String, message: String, acceptButtonTitle: String, declineButtonTitle: String\)

Creates and returns a ClosePrompt object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) method to configure the close prompt options within the chat session.

<table id="table_tts_2qz_ddc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

header

</td><td>

String

</td><td>

Text to display on the prompt's header.If you don't want to display a prompt header, pass null.

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Text to display as the prompt's main text.

</td></tr><tr><td>

acceptButtonTitle

</td><td>

String

</td><td>

Text to display on the prompt's primary button for closing the chat window.

</td></tr><tr><td>

declineButtonTitle

</td><td>

String

</td><td>

Text to display on the prompt's secondary button that dismisses the prompt.If you don't want to display a secondary button, pass null.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Prompt to display before closing the associated chat window.|

The following code example shows how to call this method to configure the close prompt.

```
suspend fun launchChat() {
  val chatService = getNowChatService()
 
  val chatConfiguration = NowChatConfiguration(
    closePrompt = NowChatConfiguration.ClosePrompt(
      header = null,
      message = "Are you sure you want to leave?",
      acceptButtonTitle = "Yes",
      declineButtonTitle = "No"
    )
  )
  chatService?.start(activity, chatConfiguration)
}
```

## NowChatConfiguration - UIConfiguration\(closeButton: CloseButton? = null, attachmentUploadButton: AttachmentUploadButton? = null\)

Creates and returns a UIConfiguration object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) constructor to configure UI components in NowChat.

UIConfiguration is a subclass of the NowChatConfiguration class.

<table id="table_p2y_2vr_ddc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

closeButton

</td><td>

[CloseButton?](NowChatOptionsAndroid.md#)

</td><td>

Configuration for the `CloseButton` that appears on the NowChat toolbar and is used for back navigation.Call the [NowChatConfiguration - CloseButton\(icon: Drawable?\)](NowChatOptionsAndroid.md#) subclass to define the value of this parameter.

For example:

```
val chatConfiguration = NowChatConfiguration( 
  uiConfiguration = NowChatConfiguration.UIConfiguration( 
    closeButton = NowChatConfiguration.CloseButton( 
      icon = myDrawable
  )
)
```

</td></tr><tr><td>

attachmentUploadButton

</td><td>

[AttachmentUploadButton?](NowChatOptionsAndroid.md#)

</td><td>

Configuration for the `AttachmentUploadButton` that is shown next to the text input while talking with a live agent.Call the [NowChatConfiguration - AttachmentUploadButton\(isVisible: Boolean = true\)](NowChatOptionsAndroid.md#) subclass to define the value of this parameter.

For example:

```
val chatConfiguration = NowChatConfiguration( 
  uiConfiguration = NowChatConfiguration.UIConfiguration(
    attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible = false)
  ) 
)
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|UI configuration object.|

The following code example shows how to call the UIConfiguration subclass to set the icon for the closeButton and to hide the attachment upload button.

```
suspend fun launchChat() {
  val chatService = getNowChatService() 
     
  //Drawable to use instead of the default NowChat back button. 
  val myDrawable = ContextCompat.getDrawable(activity, R.drawable.my_drawable) 
 
  val chatConfiguration = NowChatConfiguration( 
    uiConfiguration = NowChatConfiguration.UIConfiguration( 
      closeButton = NowChatConfiguration.CloseButton( 
        icon = myDrawable 
      ), 
      attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible = false)
    ) 
  ) 
 
  chatService?.start(activity, chatConfiguration) 
} 
```

